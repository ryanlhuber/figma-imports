# Radix Colors 3.0.0

Starter primitive color collections sourced from the official `@radix-ui/colors` 3.0.0 package.

## Included scales

- Gray
- Mauve
- Slate
- Sage

Each scale contains 12 steps and is provided as separate light and dark import files. The files use the official sRGB hexadecimal values.

## Import order

These files are independent primitive collections. Import only the neutral scale or scales needed by the target design system, then alias them from semantic tokens.

## Naming

Files follow this pattern:

```text
radix_<scale>_<mode>.tokens.json
```

Variables follow this pattern:

```text
color/<scale>/<step>
```

Steps are zero-padded from `01` through `12` for predictable sorting.

## Scope

This starter package intentionally excludes alpha and Display-P3 variants. They should be introduced as separate selectable formats rather than mixed into the base sRGB collections.