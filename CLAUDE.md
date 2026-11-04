# Instructions for working in this repo

This repo is a personal recipe book, published with GitHub Pages from the `main` branch. The repo is public, so never add anything sensitive (personal details, contact info, keys or passwords) to any file or commit message.

## Structure

- `index.html` is the entire site: styles, markup and script in one file.
- All recipes are objects in the `recipes` array near the top of the `<script>` block.
- `README.md` describes the project for readers. Keep it accurate if the structure changes.

## Recipe format

Each recipe is an object with these fields:

```js
{
  id: "kebab-case-unique-id",
  title: "Recipe Title",
  tag: "Bake",            // short category label, e.g. Bake, Drink, Dinner, Side, Fried, Sauce
  servings: "4",          // string, may be empty
  cookTime: "35-40 min",  // string, may be empty
  calories: "",           // string, usually empty
  ingredients: [
    { qty: "2 cups", name: "flour" }
  ],
  steps: [
    "One step per string."
  ],
  note: "Optional. Tips, assumptions, serving ideas."   // omit if not needed
}
```

## Adding a recipe

1. Append the new object to the end of the `recipes` array. Do not reorder or change existing recipes unless asked.
2. Use a unique `id` in kebab-case.
3. Keep the person's quantities and wording faithful. If something is missing or unclear (no title, no amount, unclear method), flag it in `note` and tell the person, rather than guessing silently.
4. If the person names the recipe, use that exact title.
5. Reuse existing tags where they fit before inventing a new one.
6. Keep ingredient `qty` and `name` fields short. Put grouping hints in the name, for example "(pastry)" or "(gravy)".

## Editing a recipe

Change only what was asked. When scaling a recipe, update `servings` and every quantity, and mention any awkward conversions to the person.

## Publishing

Commit and push to `main`. GitHub Pages republishes automatically within a minute or two. Before pushing, fetch from origin and rebase if needed so the push is clean.

## Style

- Do not use em dashes anywhere, in the site or in messages to the person.
- If a request is unclear, ask a short clarifying question before making changes.
- After a change, say briefly what was added or changed and the new recipe count.
