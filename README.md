# Recipe Box

A personal recipe book, published as a single web page with GitHub Pages and designed to be used on a phone.

Live site: https://grovebrent1-ui.github.io/recipe-box/

## What it does

- Browse recipes as cards, tap one to see ingredients and method.
- Search by recipe title or ingredient.
- Works on any phone browser. Use the browser's "Add to Home Screen" option for an app-style icon.

## How it is built

The whole site is one file, `index.html`. All recipes live in the `recipes` array inside the script in that file. There is no build step, no server and no external data. Fonts load from Google Fonts.

## Adding or changing recipes

Recipes are added by sending them to Claude, which edits `index.html` and pushes the change to `main`. GitHub Pages republishes automatically, usually within a minute or two. See `CLAUDE.md` for the exact format Claude follows.

To edit by hand instead, change the `recipes` array in `index.html`, commit, and push to `main`.
