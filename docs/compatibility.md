# Compatibility

## Token format

Token files use a Figma-compatible JSON token structure with `$type`, `$value`, and Figma extension metadata where required by the importer.

Import behavior can vary between plugins. Verify that the selected plugin supports:

- Color variables
- Multiple collection modes
- Slash-delimited variable names
- Token aliases
- Eight-digit hexadecimal colors before using alpha scales

## Source versions

| Source | Version | Layer | Notes |
|---|---:|---|---|
| Tailwind CSS | 4.3.2 | Primitive | Existing repository token source |
| Radix Colors | 3.0.0 | Primitive | Official sRGB color scales with 12 steps |

## Radix support

The Radix starter set includes the foundational neutral scales:

- Gray
- Mauve
- Slate
- Sage

Each scale contains `Light` and `Dark` modes. These values are primitive colors, not semantic roles. Consumers should alias them into semantic tokens such as background, surface, text, border, accent, and focus ring.

## Color spaces

The initial Radix set uses sRGB hexadecimal values for broad Figma importer compatibility. Radix Display-P3 and alpha scales should be stored in separate files so users can select the format appropriate to their workflow.

## Library distinctions

Radix Colors is a primitive color source. Radix Primitives and Base UI are headless component libraries and should be represented under component assets rather than treated as token scales. shadcn/ui and Mantine may span semantic tokens, component tokens, components, and icons.