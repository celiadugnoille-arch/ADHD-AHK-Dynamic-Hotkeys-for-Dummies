---
name: clone-select-to-autocomplete-repo
description: >-
  Shallow-clone Célia's selectToAutocomplete fork (jQuery autocomplete
  for select tags) into external/selectToAutocomplete. Use when the user
  asks to clone selectToAutocomplete or runs
  /clone-select-to-autocomplete-repo.
disable-model-invocation: true
---

# Clone selectToAutocomplete

- Fork: https://github.com/celiadugnoille-arch/selectToAutocomplete
- Upstream: https://github.com/jamieholst/selectToAutocomplete
- Default branch: `master` (not `main`)
- Destination: `external/selectToAutocomplete`

Turns a `<select>` into an autocomplete field with weighted options, synonyms, and loose matching. It is an old jQuery plugin (bundled jQuery 1.11) — read it for the matching logic, do not adopt it as a dependency in new work.

## Steps

1. If `external/selectToAutocomplete` is already a git checkout, fetch and fast-forward `master`.
2. Otherwise: `git clone --depth 1 --branch master https://github.com/celiadugnoille-arch/selectToAutocomplete.git external/selectToAutocomplete`.
3. Leave the clone untracked. `external/` is gitignored.
4. Report the path, branch, and upstream. The logic lives in `jquery.select-to-autocomplete.js`; `index.html` is the demo.
