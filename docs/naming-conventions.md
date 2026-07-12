# Naming Conventions

## Repository paths

Organize assets by layer, source, and version:

```text
tokens/<layer>/<source>/<version>/<category>/<file>
```

Examples:

```text
tokens/primitives/tailwind/v4.3.2/colors/tw_colors_hex.tokens.json
tokens/primitives/radix-colors/v3.0.0/colors/radix_gray.tokens.json
```

## File names

Use lowercase source prefixes and snake case:

- `tw_` for Tailwind
- `radix_` for Radix
- `shadcn_` for shadcn/ui
- `baseui_` for Base UI
- `mantine_` for Mantine

Token files must end with `.tokens.json`.

## Token paths

Use slash-delimited names inside Figma:

```text
color/gray/01
color/gray/02
spacing/100
radius/md
```

Use zero-padded Radix steps (`01` through `12`) so variables sort correctly.

## Collections and modes

Use human-readable collection names:

```text
Radix / Gray
Tailwind / Spacing
Shadcn / Theme
```

Use title case for modes:

```text
Light
Dark
Compact
Regular
```

## Versioning

Keep source versions in directory names, manifests, and README files. Do not add versions to individual variable names because versioning is repository metadata rather than a design token role.