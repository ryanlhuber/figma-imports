# Library Dependencies

This repository separates assets by responsibility rather than assuming every library provides the same kind of resource.

## Dependency model

```text
Primitive tokens
  ↓
Semantic tokens
  ↓
Component tokens
  ↓
Figma components and templates
```

## Library roles

| Library | Primary role | Typical dependencies |
|---|---|---|
| Tailwind CSS | Primitive utility scales | None |
| Radix Colors | Primitive color scales | None |
| Radix Primitives | Headless component anatomy and behavior | A semantic theme and component styling |
| Base UI | Headless component anatomy and behavior | A semantic theme and component styling |
| shadcn/ui | Semantic theme and styled component recipes | Tailwind, Radix or Base UI, Lucide |
| Mantine | Theme primitives, semantic configuration, and components | Mantine theme configuration |

## Rules

- Primitive sources must not depend on semantic or component collections.
- Semantic collections may alias one primitive source or intentionally combine several.
- Component tokens should alias semantic roles whenever possible.
- Component libraries must document which token package and version they expect.
- Icons remain independent assets even when a component library commonly uses them.

## Example combinations

```text
Tailwind primitives → shadcn semantic tokens → shadcn components
Radix Colors → custom semantic tokens → Radix Primitives components
Custom primitives → custom semantic tokens → Base UI components
Mantine primitives → Mantine semantic theme → Mantine components
```

Avoid nesting shadcn, Radix Primitives, or Base UI under Tailwind. Tailwind may be a dependency, but it is not the parent asset type.