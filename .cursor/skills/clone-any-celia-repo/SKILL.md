---
name: clone-any-celia-repo
description: >-
  Index of every repo on github.com/celiadugnoille-arch with its upstream,
  default branch, and dedicated clone skill. Use when the user asks which
  repos exist, asks to clone a repo with no dedicated skill, or runs
  /clone-any-celia-repo.
disable-model-invocation: true
---

# Célia's GitHub repos

All 35 public repos on https://github.com/celiadugnoille-arch. Every clone lands in `external/<dir>`, which is gitignored.

If the repo has a dedicated skill, run that skill. Otherwise follow the generic procedure at the bottom.

## Agents and LLM tooling

| Repo | Upstream | Branch | Skill |
| --- | --- | --- | --- |
| openai-agents-python | openai/openai-agents-python | `main` | `/clone-openai-agents-python-repo` |
| LightAgent | wanxingai/LightAgent | `main` | `/clone-lightagent-repo` |
| instructor | 567-labs/instructor | `main` | `/clone-instructor-repo` |
| Guardrails (NeMo) | NVIDIA-NeMo/Guardrails | `develop` | `/clone-nemo-guardrails-repo` |
| garde-fou-1 (Portkey gateway) | Portkey-AI/gateway | `main` | `/clone-portkey-gateway-repo` |
| TencentDB-Agent-Memory | TencentCloud/TencentDB-Agent-Memory | `feat/server_team` | `/clone-tencentdb-agent-memory-repo` |
| mistral-vibe | mistralai/mistral-vibe | `main` | `/clone-mistral-vibe-repo` |
| claude-code | anthropics/claude-code | `main` | `/clone-claude-code-repo` |
| claude-plugins-official | anthropics/claude-plugins-official | `main` | `/clone-claude-plugins-official-repo` |
| QueryGym | ls3-lab/QueryGym | `main` | `/clone-querygym-repo` |

## ADHD, focus, and mental health

| Repo | Upstream | Branch | Skill |
| --- | --- | --- | --- |
| i-have-adhd | ayghri/i-have-adhd | `main` | `/clone-i-have-adhd-repo` |
| claude-adhd | shaheer-00/claude-adhd | `master` | `/clone-claude-adhd-repo` |
| awesome-adhd | XargsUK/awesome-adhd | `main` | `/clone-awesome-adhd-repo` |
| adhd-focus-mate | skainguyen1412/adhd-focus-mate | `main` | `/clone-adhd-focus-mate-repo` |
| leantime | Leantime/leantime | `master` | `/clone-leantime-repo` |
| Mindwtr | dongdongbh/Mindwtr | `main` | `/clone-mindwtr-repo` |
| Ai-psychologue-bot | nvikou/Ai-psychologue-bot | `main` | `/clone-ai-psychologue-bot-repo` |
| Mental_Health_App | Shreyg-27/Mental_Health_App | `main` | `/clone-mental-health-app-repo` |

## Voice, dictation, and transcription

| Repo | Upstream | Branch | Skill |
| --- | --- | --- | --- |
| NotelyVoice | Notely-Voice/NotelyVoice | `main` | `/clone-notelyvoice-repo` |
| iDictate | petepiet/iDictate | `main` | `/clone-idictate-repo` |
| sayso | stevengonsalvez/sayso | `main` | `/clone-sayso-repo` |
| katip | odest/katip | `master` | `/clone-katip-repo` |

## Writing, documents, and ideas

| Repo | Upstream | Branch | Skill |
| --- | --- | --- | --- |
| Logyc | bienwech6-sudo/Logyc | `main` | `/clone-logyc-repo` |
| atelier-visuel | yaya56vv/atelier-visuel | `main` | `/clone-atelier-visuel-repo` |
| sinceerly-humanize-ai-slop | SediraYasser20/sinceerly-humanize-ai-slop | `main` | `/clone-humanizer-repo` clones `blader/humanizer` instead; for this fork, use the generic procedure |
| retext-simplify | retextjs/retext-simplify | `main` | `/clone-retext-simplify-repo` |
| accelerated-text | accelerated-text/accelerated-text | `master` | `/clone-accelerated-text-repo` |
| Cahier-de-charges | Arol-123/Cahier-de-charges | `main` | `/clone-cahier-de-charges-repo` |
| Realisez-un-cahier-des-charges-…-application | OpenClassrooms-Student-Center/… | `main` | `/clone-cahier-des-charges-openclassrooms-repo` |

## Web and framework forks

| Repo | Upstream | Branch | Skill |
| --- | --- | --- | --- |
| react-native | react/react-native | `main` | `/clone-react-native-repo` |
| angular | angular/angular | `main` | `/clone-angular-repo` |
| selectToAutocomplete | jamieholst/selectToAutocomplete | `master` | `/clone-select-to-autocomplete-repo` |

## Nothing to clone

- **ecrire** and **tdahh** are empty repos: created, never pushed to. `git clone` returns a warning and an empty checkout. Create a first commit before expecting content.
- **ADHD-AHK-Dynamic-Hotkeys-for-Dummies** (upstream `evilC/…`, branch `topitop`) is this repository — the one the skills live in. Do not clone it into `external/`.

## Generic procedure

For any repo without a dedicated skill:

1. Confirm the default branch: `gh api repos/celiadugnoille-arch/<repo> --jq .default_branch`. Several repos use `master` or a feature branch, so do not assume `main`.
2. If `external/<repo>` is already a git checkout, fetch and fast-forward that branch instead of re-cloning.
3. Otherwise: `git clone --depth 1 --branch <branch> https://github.com/celiadugnoille-arch/<repo>.git external/<repo>`.
4. Leave the clone untracked. `external/` is gitignored. Never commit `.env` files, tokens, keystores, or API keys found in a clone.
5. Report the path, branch, and upstream, and read the repo's `README.md` before changing anything.

## Size warnings

Keep `--depth 1` everywhere. These are the heavy ones, and cloning them takes minutes: react-native (~970 MB), angular (~670 MB), leantime (~260 MB), Mindwtr (~235 MB), QueryGym (~215 MB), Guardrails (~155 MB), openai-agents-python (~100 MB), NotelyVoice (~85 MB), instructor (~80 MB), garde-fou-1 (~65 MB), TencentDB-Agent-Memory (~65 MB). To read one or two files from them, use the GitHub API instead of cloning.
