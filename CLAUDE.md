# CLAUDE.md

Guidance for Claude Code in this repo. README.md covers the page itself.

## What this is

The source of `mylandurray.github.io`: one self-contained `index.html`, no build
step. Push to `main` and GitHub Pages republishes (a minute or two).
Preview locally with the `home` entry in `.claude/launch.json`.

## Desktop downloads

- The `DOWNLOADS` array lists desktop tools. Each `id` is the tag prefix of its
  releases on the public `mylandurray/downloads` repo (`<id>-v<version>`);
  the page fetches that repo's releases API (cached 10 min in localStorage)
  and shows the newest non-draft, non-prerelease per tool. Nothing about a
  release is hard-coded here: publishing a new version needs no edit to this repo.
- `latestFor()` picks the Windows file (`.exe`/`.msi`/`.zip` without "mac") and
  the Mac files by `apple-silicon|arm64` / `intel|x64`. Keep it in step with the
  asset names the tools' release workflows produce.
- Releases are made by `release.yml` in each tool's private repo on a `v*` tag
  (KongCut, Pre-Press-QuickCheck); see `downloads/CLAUDE.md`.
- **ProofHub/Printlogic Bridge was removed from `DOWNLOADS` on 2026-11-24 and
  must not be re-added**: its installer bundles a Zoho client secret.
