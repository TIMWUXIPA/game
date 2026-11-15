# WYDNS Games

Local static site intended for https://game.wydns.dpdns.org/.

## Run locally

From this directory run `python3 -m http.server 8748 --bind 127.0.0.1`, then open http://127.0.0.1:8748/ and http://127.0.0.1:8748/2048/.
No build, package manager, runtime API, or external font service is required. Publish the directory contents as a static Pages root; `.nojekyll` is included. Domain/Pages settings are intentionally left to the owner. Nothing has been pushed or deployed by this task.

## Provenance and license

- Source: https://github.com/TIMWUXIPA/2048, branch `master`.
- Exact source commit: `478b6ec346e3787f589e4af751378d06ded4cbbc` (2024-10-24, “Update README.md”).
- Repository metadata and commit were read through GitHub MCP, then a shallow git clone supplied the binary assets and complete source tree.
- Original game by Gabriele Cirulli, based on 1024 by Veewo Studio and conceptually similar to Threes by Asher Vollmer.
- The original MIT license and copyright are preserved in `2048/LICENSE.txt`; original in-game attribution remains.
- `2048/js/`, `2048/style/` (including original bundled fonts), `2048/meta/`, `2048/favicon.ico`, and the game HTML derive from that commit.

## Deliberate changes

- Added an ivory/terracotta magazine-style directory at `/`, using native system and Georgia fonts. Shared WYDNS navigation uses ordinary same-tab anchors for Home, Blog, Games and TV.
- Moved the original game to `/2048/`; its existing relative asset references remain valid under that subpath.
- Replaced the source HTML’s misleading official-site claim with a personal-deployment notice, original-site link, source and license links.
- Added a subtle relative return link to the game directory. No gameplay, translation or visual restyling of the original game.
- Namespaced game state, best score, and storage-support probe keys as `wydns.2048.gameState`, `wydns.2048.bestScore`, and `wydns.2048.test`. No old-save migration on this new origin.

## Verification

See `tests/RESULTS.md` for actual local checks and browser execution results. All deployment/DNS/remote changes are out of scope.
