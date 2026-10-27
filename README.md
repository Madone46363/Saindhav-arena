# SAINDHAV ARENA

Free online games arcade with 83 fully playable browser games, no download, no mandatory sign-up for browsing or guest play.

Latest version: premium purple/white/gold design, brand-only website content, Instructions button for every game, unified alignment and corners, header/footer alignment to one shared margin system, progressive levels with Easy/Medium/Hard difficulty for every game, a fixed game setup UI (no nested scrollable setup panel, no duplicate toolbar/stat tiles in setup, level bar no longer clipped under the header), homepage MULTIPLAYER GAMES — SAME DEVICE with exactly 4 games (Ludo Kingdom, Chess, Checkers, Pong Duel) and RECENTLY ADDED with exactly 4 games (Gem Cascade, Turret Defense, Time Trial Circuit, Bowling Strike), mobile homepage hero alignment, fit-to-screen guard, and icon integrity pass. Snake Sprint was removed at the user's request, reducing the catalog from 84 to 83 games.

- Brand: main background #0B0714, secondary #140D23, card #1C1430, primary purple #8B5CF6, bright purple accent #A78BFA, white text #FFFFFF, secondary text #B9B2C9, gold accent #D4AF37, borders #302343. SA logo recreated from the uploaded SA monogram shape (purple S, white A, small gold crossbar).
- Website content is brand-only: the site itself does not mention GitHub, Cloudflare, repositories, deployments, or project-work/QA processes. This README is repo documentation, not website content.
- Homepage first: site opens on the homepage as a Guest profile, no forced login gate. Login opens only from the account menu, cancel/success returns to the previous page, invalid email shows a clear in-place error.
- Email profiles in this static build are unverified and device-local only, clearly labelled in the site. Supabase is not yet connected, so there is no cross-device sync or verified account yet.
- Games: 83 games, including the original 59 plus a later batch (including Ludo Kingdom and Carrom Clash), minus Snake Sprint which was removed at the user's request. Each game has its own logo/icon, accent colour, and illustration, with the same card/panel layout. Galaxy Invaders has 3 lives in this version, with alien speed/rows scaling by level and difficulty.
- Levels and difficulty: every game has a setup screen with Easy/Medium/Hard cards, Starting Level 1-10, and Start Game; a level bar during play; per-game level objectives (win-type, score-target, or time-threshold where applicable); a gold Level Complete screen with Continue preserving run score; and a Game Over screen with final score, highest level reached, Retry, and Back to Games where a loss ends the run. Local multiplayer is preserved, with progression per match.
- Honest testing note for this version: all 7 script blocks passed node syntax checks and a structural pass confirmed all 84 games resolve a level objective and all onclick handlers resolve. The latest levels/difficulty build did NOT manually play-test all 84 games in a live browser in that pass, so per-game gameplay, Pause/Resume, and local multiplayer turn order for that build are NOT TESTED, not claimed as PASS. Earlier builds had flow-tested the original 59 games in a headless harness; that is not a substitute for testing this version's new level/difficulty layer on every game. The Checkers setup UI fix WAS live-probed (setup fully visible, centred 8x8 board, legal move, Restart, Pause/Resume, Exit/reopen, Hard difficulty, mobile fit, 0 console errors), but a complete Checkers win through to Level 2, win/draw end states, and the other 83 games individually remain NOT TESTED live in that pass. Known copy contradiction left in this version: the homepage "MY GAMING PROGRESS" text still says no levels are invented for games without a level system, which now contradicts the levels feature; fix that copy in a later version.
- Player counts (real, from catalog at Stage 3, minus Snake Sprint): Single Player 83 games, local multiplayer 14 games, Ludo the only 3- and 4-player local game, 5-6 players 0 games. 500+ games are later staged work, not claimed now.
- Online multiplayer: not implemented in this build. Local multiplayer only where actually implemented, labelled as not available for online play in plain brand terms in the site.
- Progress: best score, attempts, completions, last played per game per email/guest profile, saved at checkpoints, flushed on exit/switch/sign-out.
- Known limitation: true PWA (manifest, service worker, install) is NOT implemented in this static build. Do not treat any offline wording as installable offline PWA until manifest + service worker are added in a real deployment and tested.

## Deploy on Cloudflare Pages

- Connect this repository in Cloudflare Pages.
- Framework preset: None / Static.
- Build command: none.
- Build output directory: `/` (root, where `index.html` lives).
- Cloudflare Pages redeploys automatically when this repo's main branch is updated, though redeploy may take several minutes to appear live.

## Games

Arcade, Puzzle, Word, Board, Racing, Platform, Cards, Casual, Sports and Brain games, all in the single self-contained `index.html` with no external requests after the page loads, except where a future backend (Supabase) is connected separately.
