# SAINDHAV ARENA

Free online games arcade with 59 fully playable browser games, no download, no sign-up required for guest play.

Latest version: premium black-and-gold platform, refined SA logo, About section, every page properly created, all-devices alignment fixes, Stage 1-2 game catalog with accurate player-count filters, persistent progress per email profile, and premium animations with High/Balanced/Low effects settings.

- Email-only login: Enter email → Continue → Start. No password, no OTP, no verification in this version. Profiles are unverified and progress is device-local only in this static build, clearly labelled in the site. Supabase is not yet connected.
- Homepage: Game Library grid removed from homepage; full library lives in Explore Games with search, category filters, and player-count filters.
- Player counts (real, from catalog): Single Player 59 games, 2 Players 11 local games, 3/4/5/6 Players 0 games — 3-6 player modes and 500+ games are later staged work, not claimed now.
- Online multiplayer: not implemented in this build. Local 2-player modes only where actually implemented.
- Progress: best score, attempts, completions, last played per game per email profile, saved at checkpoints with debouncing, flushed on exit/switch/sign-out. No levels invented for games without a level system.
- Animations: subtle premium animations, reduced-motion support, and High/Balanced/Low effects setting. Performance fixes include animation-frame and keyup listener leak fixes.

## Deploy on Cloudflare Pages

- Connect this repository in Cloudflare Pages.
- Framework preset: None / Static.
- Build command: none.
- Build output directory: `/` (root, where `index.html` lives).
- Cloudflare Pages redeploys automatically when this repo's main branch is updated.

## Games

Arcade, Puzzle, Word, Board, Racing, Platform, Cards, Casual, Sports and Brain games, all in the single self-contained `index.html` with no external requests after the page loads, except where a future backend (Supabase) is connected separately.
