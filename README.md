# CSS Fluid Text

CSS custom properties for responsive typography using quadratic scaling.

## Formula

```
clamp(base, base + grow * (viewport_px)^2, max)
```

## Available Variables

```css
--text-fluid-xs
--text-fluid-sm
--text-fluid-md
--text-fluid-lg
--text-fluid-xl
--text-fluid-2xl
--text-fluid-3xl
--text-fluid-4xl
```

## Configuration

Each size has three control variables:

- `--{size}-base` - Minimum font size
- `--{size}-grow` - Growth rate multiplier
- `--{size}-max` - Maximum font size

## Usage

Install the package:

```bash
npm install @bienbien/css-fluid-text
```

Import in your CSS:

```css
@import '@bienbien/css-fluid-text/dist/index.css';
```

Override defaults as needed:

```css
:root {
    --xl-base: 1.2rem;
    --xl-grow: 1.5;
    --xl-max: 3rem;
}
```

Use in your styles:

```css
h1 {
    font-size: var(--text-fluid-xl);
}
```

## Default Values

```css
:root {
    --xs-base: 0.625rem;
    --xs-grow: 0.5;
    --xs-max: 1rem;

    --sm-base: 0.7rem;
    --sm-grow: 0.5;
    --sm-max: 1.25rem;

    --md-base: 0.8rem;
    --md-grow: 0.6;
    --md-max: 1.75rem;

    --lg-base: 1.25rem;
    --lg-grow: 0.8;
    --lg-max: 2.5rem;

    --xl-base: 1.5rem;
    --xl-grow: 1;
    --xl-max: 4rem;

    --2xl-base: 1.75rem;
    --2xl-grow: 1.5;
    --2xl-max: 6rem;

    --3xl-base: 2rem;
    --3xl-grow: 2;
    --3xl-max: 8rem;

    --4xl-base: 2.25rem;
    --4xl-grow: 3;
    --4xl-max: 10rem;
}
```
