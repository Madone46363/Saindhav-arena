# SAINDHAV ARENA

Free online games arcade with 59 fully playable browser games, no download, no sign-up.

Latest version: flat portal interface with no animations, simple gamepad logo with SAINDHAV ARENA wordmark, laptop + mobile friendly, and local 2-player modes for selected games.

## Deploy on Cloudflare Pages

- Connect this repository in Cloudflare Pages.
- Framework preset: None / Static.
- Build command: none.
- Build output directory: `/` (root, where `index.html` lives).

## Games

Arcade, Puzzle, Word, Board, Racing, Platform, Cards, Casual, Sports and Brain games, all in the single self-contained `index.html` with no external requests after the page loads.

## Notes

- Single-player and local multiplayer games are in this page. Online multiplayer via Cloudflare Workers / Durable Objects is planned separately and is not simulated in this page.
- True PWA manifest + service worker install is a separate deployment step on Cloudflare Pages, not included in this Muse static artifact export.
