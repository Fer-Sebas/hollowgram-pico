# Hollowgram Pico

A minimal-usable CSS design system that styles HTML tags directly. No classes, no IDs, no framework — just a drop-in stylesheet that brings visual structure to plain HTML.

## Philosophy

- **Tag-first.** Styles target vanilla HTML elements. Any markup works out of the box.
- **Token-driven.** All values flow from CSS custom properties. Nothing is hardcoded.
- **Layered.** Tokens, theme, and style are separate concerns. Swap one without touching the others.
- **Minimal-usable.** The smallest surface area that produces a coherent, usable UI hierarchy.

## Structure
```
index.css              # Entry point — import this

tokens/
  color.css            # Color primitives + semantic aliases (light & dark)
  space.css            # Spacing primitives + semantic aliases
  typography.css       # Type primitives + semantic aliases
  shape.css            # Radius + border-width primitives + aliases
  motion.css           # Duration + easing primitives + aliases

style/
  type.css             # Typography applied to HTML elements
  layout.css           # Space + shape applied to structural elements
  components.css       # All tokens applied to interactive elements
```

## Usage
```html
<link rel="stylesheet" href="hollowgram-pico/index.css">
```

That's it. No build step, no configuration.

## Status

Early development. Structure and tokens are being defined.

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to use and modify with attribution.