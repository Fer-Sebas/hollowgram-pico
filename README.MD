# Hollowgram Pico

An opinionated minimal-usable CSS design system that styles HTML tags directly. No classes, no IDs, no framework — just a drop-in stylesheet that brings visual structure to plain HTML.

## Philosophy

- **Tag-first.** Styles target vanilla HTML elements. Any markup works out of the box.
- **Token-driven.** All values flow from CSS custom properties. Nothing is hardcoded.
- **Layered.** Color, shape, and typography are independent axes. Each is hot-swappable without touching the others.
- **Minimal-usable.** The smallest surface area that produces a coherent, usable UI hierarchy.

## Usage

Add one line to your HTML. No install, no build step.
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/hollowgram-pico@latest/index.css">
```

To pin to a specific version:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/hollowgram-pico@0.1.0/index.css">
```

## Structure
```
index.css                  # Entry point — imports everything

theme/
  light.css                # Color tokens, light mode
  dark.css                 # Color tokens, dark mode

core/
  space.css                # Space tokens + semantic aliases
  typography.css           # Typography tokens + semantic aliases
  shape.css                # Radius + border-width tokens + aliases
  motion.css               # Duration + easing tokens + aliases
  type.css                 # Typography applied to HTML elements
  layout.css               # Space + shape applied to structural elements
  components.css           # All tokens applied to interactive elements
```

`index.css` imports both theme files. Light and dark mode are toggled via a CSS class or `prefers-color-scheme` media query. Color and form never mix — swapping a theme file does not affect layout or typography.

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to use and modify with attribution.

## Status

Early development. Structure and tokens are being defined.