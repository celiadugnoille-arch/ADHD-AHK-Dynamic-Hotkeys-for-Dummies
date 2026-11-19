---
name: clone-cahier-des-charges-openclassrooms-repo
description: >-
  Shallow-clone Célia's OpenClassrooms "Réalisez un cahier des charges"
  fork into external/cahier-des-charges-openclassrooms. Use when the user
  asks to clone that exercise or runs
  /clone-cahier-des-charges-openclassrooms-repo.
disable-model-invocation: true
---

# Clone Réalisez un cahier des charges (OpenClassrooms)

- Fork: https://github.com/celiadugnoille-arch/Realisez-un-cahier-des-charges-fonctionnel-et-technique-pour-une-application
- Upstream: https://github.com/OpenClassrooms-Student-Center/Realisez-un-cahier-des-charges-fonctionnel-et-technique-pour-une-application
- Default branch: `main`
- Destination: `external/cahier-des-charges-openclassrooms`

The OpenClassrooms starter repo for writing a functional and technical specification. The destination is shortened because the repo name is very long. The other spec repo is `Cahier-de-charges`.

## Steps

1. If `external/cahier-des-charges-openclassrooms` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/Realisez-un-cahier-des-charges-fonctionnel-et-technique-pour-une-application.git external/cahier-des-charges-openclassrooms`.
3. Leave the clone untracked. `external/` is gitignored.
4. Report the path, branch, and upstream. The repo is tiny: `README.md`, `app/`, and `db/`.
