# Import Guide

This repository contains reusable assets for importing into Figma. Import primitive collections before semantic or component-level collections so aliases can resolve correctly.

## Recommended order

1. Primitive colors
2. Primitive dimensions
3. Primitive typography
4. Primitive effects
5. Semantic theme tokens
6. Component tokens
7. Components, icons, and templates

## Choosing a source

Import only the primitive libraries needed by a project. Tailwind and Radix collections may coexist, but avoid importing overlapping palettes unless both sources are intentionally required.

For color collections with multiple modes, keep the mode names supplied by the file. Do not flatten light and dark values into separate variables.

## Radix Colors

The Radix starter collection is stored under `tokens/primitives/radix-colors/v3.0.0/`. Import each scale as its own Figma collection or combine them through the import plugin when supported.

The included files use the official sRGB values and provide `Light` and `Dark` modes. Alpha and Display-P3 variants are intentionally excluded from the starter set and may be added separately.

## Validation

After importing:

- Confirm collection and mode names.
- Confirm all 12 steps exist for every Radix scale.
- Check that color values are recognized as colors rather than strings.
- Verify aliases before importing semantic collections.
- Avoid importing both an older and newer version of the same source into one Figma file.