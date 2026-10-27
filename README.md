# SAINDHAV ARENA

Free online games arcade with 59 fully playable browser games, no download, no mandatory sign-up for browsing or guest play.

Latest version: premium purple/white/gold design, QA-tested, homepage-first optional login.

- Brand: main background #0B0714, secondary #140D23, card #1C1430, primary purple #8B5CF6, bright purple accent #A78BFA, white text #FFFFFF, secondary text #B9B2C9, gold accent #D4AF37, borders #302343. SA logo recreated from the uploaded SA monogram shape (purple S, white A, small gold crossbar).
- Homepage first: site opens on the homepage as a Guest profile, no forced login gate. Login opens only from the account menu, cancel/success returns to the previous page, invalid email shows a clear in-place error.
- Email profiles in this static build are unverified and device-local only, clearly labelled in the site. Supabase is not yet connected, so there is no cross-device sync or verified account yet.
- QA: 59/59 games flow-tested in a headless Chromium harness (open, start, input, pause, resume, restart, exit, reopen) with 0 console errors in that harness, 11/11 local 2-player modes launched, no horizontal overflow at 320-2560px widths, QA Report page included. A timer leak (setTimeout bypassing pause/cleanup) was fixed at source.
- Player counts (real, from catalog): Single Player 59 games, 2 Players 11 local games, 3/4/5/6 Players 0 games — 3-6 player modes and 500+ games are later staged work, not claimed now.
- Online multiplayer: not implemented in this build. Local 2-player modes only where actually implemented.
- Progress: best score, attempts, completions, last played per game per email/guest profile, saved at checkpoints, flushed on exit/switch/sign-out. No levels invented for games without a level system.
- Known limitation: the site still displays "OFFLINE READY" / "Offline" badges, but true PWA (manifest, service worker, install) is NOT implemented in this static build. Do not treat those badges as installable offline PWA until manifest + service worker are added in a real deployment and tested.

## Deploy on Cloudflare Pages

- Connect this repository in Cloudflare Pages.
- Framework preset: None / Static.
- Build command: none.
- Build output directory: `/` (root, where `index.html` lives).
- Cloudflare Pages redeploys automatically when this repo's main branch is updated, though redeploy may take several minutes to appear live.

## Games

Arcade, Puzzle, Word, Board, Racing, Platform, Cards, Casual, Sports and Brain games, all in the single self-contained `index.html` with no external requests after the page loads, except where a future backend (Supabase) is connected separately.
