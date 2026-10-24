# YapperSMP (starter build)

This is a single custom Paper plugin project. Land claims are intentionally NOT included, as requested.

## Included
- `/bal`, `/balance`, `/money`, `/pay`
- `/shop` inventory shop using `config.yml` prices
- `/sell [all|hand]`
- `/tpa`, `/tpaccept`, `/tpdeny`
- `/rtp` with safe-ish overworld spot search and cooldown
- `/ah` basic in-memory player auction house
- `/kit starter`
- `/crate common|rare|legendary` (requires keys; see note)
- `/yadmin give <player> <amount>`, `/yadmin set <player> <amount>`, `/yadmin reload`
- Basic movement alerts (not a robust anti-cheat)

## Build
Requires Java 21 and Maven. This starter targets Paper 1.21.4 API.
1. Install JDK 21 and Maven.
2. From this folder run `mvn package`.
3. Copy `target/YapperSMP.jar` to your server's `plugins/` directory.
4. Start server once, then stop and edit `plugins/YapperSMP/config.yml`.

## Important limitations
- The project targets Paper 1.21.4, not an unspecified newest release. Change the Paper API dependency and `api-version` after checking the API for your server version.
- Auction listings, crate keys and kit cooldowns are currently memory-only and reset on restart. Balances persist.
- Crate keys have no player/admin grant command yet; an admin key command should be added before production use.
- Auction listings are not persisted; only use for testing.
- Basic movement alerts are experimental and are NOT a replacement for a maintained anti-cheat. It does not auto-ban.
- Shop buys one item per click. `/sell` only sells materials with configured shop prices.
- Test on a backup server first.
