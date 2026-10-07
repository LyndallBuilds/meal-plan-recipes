# meal-plan-recipes

Public, copyright-safe staging of household meal-plan recipes for [LyndallBuilds/meal-plan-recipes](https://github.com/LyndallBuilds/meal-plan-recipes).

This repo is meant for meal-plan bots and humans who need a shareable recipe library **without** republishing third-party publisher text.

## Layout

```
recipes/
  adult-breakfast/
  adult-dinner-add/
  adult-snack/
  bakes/
  breakfast/
  brunch/
  bundt-cakes/
  dinner/
  hosting-dinner/
  lunch/
  salads/
MANIFEST.md   # full vs stub index + counts
LICENSE       # MIT
README.md
```

Folder names and filenames mirror the private library so clones and bots can map paths 1:1.

## Copyright policy

- **Original / household-written recipes** (for example MIND-aligned plates, Family meal planner weeknight dishes, household product-based dinners) are included **in full**, including out-of-rotation notes and `active: false` when present.
- **Third-party publisher recipes are stubs only** — frontmatter (title, meal_type, tags, active, source, source_url, and common planning fields) plus a short note. Bodies are **not** published. That includes:
  - New York Times Cooking / nytimes.com
  - Solid Starts / solidstarts.com
  - Other clearly copyrighted publishers or blogs with full copied methods (for example Epicurious/Nigel Slater, Yummy Toddler Food, MJ and Hungryman)
  - Social / Instagram saves and screenshots (stubbed conservatively)
- Stubs keep a similar path/filename so private notes and bot mappings still work.

If you have a subscription or licensed access, open `source_url` (or the named source) and cook from there. Keep any full private copies local — do not paste them into this public tree.

## How meal-plan bots should use this

1. Treat each file under `recipes/` as one recipe card keyed by relative path.
2. Read YAML frontmatter for `title`, `meal_type`, `tags`, `active`, `source`, `source_url`, and timing fields when present.
3. If the body starts with `## Note` and mentions third-party copyright, treat the recipe as a **stub**: you may plan/schedule by title and tags, but **do not** invent or expand full ingredients/instructions from this repo. Prefer the linked source, or a private local note store.
4. If the body has `## Ingredients` / `## Instructions` (or equivalent), treat it as a **full** original recipe and use it directly.
5. Respect `active: false` / out-of-rotation notes when scoring candidates; inclusion here does not mean currently in rotation.
6. See `MANIFEST.md` for an explicit full-vs-stub listing and counts.

## License

MIT — see [LICENSE](LICENSE). Copyright (c) 2026 LyndallBuilds.

Full original recipe text in this repository is shared under MIT. Stub files intentionally omit third-party recipe bodies; those remain the property of their respective publishers.
