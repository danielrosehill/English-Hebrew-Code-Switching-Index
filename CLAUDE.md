# CLAUDE.md — English-Hebrew-Code-Switching-Index

Public index of Daniel's own English-Hebrew code-switching work (HF models, datasets, Spaces, companion GitHub repos). Created 2026-10-15. Scope is in `SCOPE.md`.

## Two files move together

- `README.md` is the human-facing list.
- `data/index.json` is the machine-readable mirror and is hand-maintained.

When you add or change an entry, edit both in the same commit and bump the `Snapshot` line and the `snapshot` field.

## Finding new entries

The Hub author listing **silently omits repos** when it is called with `full=true&limit=1000`. On 2026-10-15 that call left out `hebrew-latin-token-classifier`. Sort by recency instead:

```bash
curl -s "https://huggingface.co/api/models?author=danielrosehill&sort=lastModified&direction=-1&limit=50"
curl -s "https://huggingface.co/api/datasets?author=danielrosehill&sort=lastModified&direction=-1&limit=50"
curl -s "https://huggingface.co/api/spaces?author=danielrosehill&sort=lastModified&direction=-1&limit=50"
```

The HF collection `danielrosehill/code-switching-english-and-hebrew-6acfdcb1e11911797af4c3b3` is the Hub-side list, so check it for drift too. On GitHub, grep `gh repo list danielrosehill --limit 4000` for `hebr|code.?switch|parakeet|whisper`.

## Linked from

These indexes link here. If you rename this repo, update all of them:

- `Subindices` README H3 block. Then run `scripts/build-indices-json.py`. `Index` pulls the list from there.
- `Israeli-AI` README "Related Indexes" table and `hebrew.md`.
- `Hebrew-Language-Projects-Index` "Code-Switching & Speech Recognition" section.
- `Speech-Tech-Index` "ASR Fine-Tuning" section.
