# Gameday 0.1 RC2 — build 6

The current installation candidate for the first leaguemate beta. Requires iOS 17+ and a Mac or Windows PC for free Apple signing. A shared HTTPS service supplies scores; testers do not run infrastructure.

## New since RC1/build 3

- Matchups and Games pills on league home, with tap and swipe switching.
- Every NFL game for the selected week in earliest-kickoff order. Completed games keep their place.
- Compact centered game rows with larger team logos, team codes, scores, and short times such as SUN @ 1PM.
- Existing game fantasy details open directly from the Games list; shared score refresh and current-week preloading include the weekly schedule.
- Player photos and NFL defense logos in game-log headers; defense logs omit snap share.
- Custom-defense trigger columns for the configured Whiskey league, before baseline defense stats.
- Manager usernames beside matchup records with mirrored, single-line layout.

## Download and install

Download **Gameday-0.1-build-6.ipa** below, then follow the [current installation guide](https://github.com/reidmojo/gameday-releases#install-on-your-iphone). We are verifying AltStore Classic with AltServer after the documented Sideloadly authentication failure. Keep your existing app installed during the transition. The IPA is unsigned and contains no development provisioning profile or certificate.

Free signing lasts seven days and needs periodic refresh through your computer. Gameday itself works over Wi-Fi or cellular using the shared free service. A first connection after inactivity may take about a minute.

## Candidate status

Passed: 76 server tests and type-check/build on the feature backend, 51 iOS tests on build 6, packaging checks, Release Simulator visual checks, and development-signed installation/opening on the maintainer's iPhone. Hosted checks covered both leagues and the full Weeks 1/2 schedules, score consistency, custom DST totals/projections, analytics, and drive play-by-play. A separate gesture check on the Games feature passed. Existing capacity testing covered 24 simulated clients without throttling or failures.

**Still pending:** free-account installer installation and Home Screen reopening, signing refresh, an update through that installer, another tester using their own username over cellular, and a genuine uninterrupted idle-start check. AltStore has not yet been confirmed working for this candidate. Sideloadly 0.60 failed at Obtaining team ID before signing/installing. This is a prerelease for installation testing; it has not been promoted to stable v0.1.

## Build details

- Version **0.1 (6)**; arm64; minimum iOS 17.
- Bundle identifier: `com.personal.FantasyGameday`.
- Private app source checkpoint: `777b59f367481fe48adbefdd14655de567a77295`.
- Hosted backend at packaging: `04de1de3d28232d2d3410ae169053384dcf32f7b`.
- SHA-256: `cac5e4bf8b13998e79241ad3189567d8471bf65628cbab116fd867966b276a82`.
- `SHA256SUMS.txt` and `build.json` provide verification metadata. Source and debugging symbols remain private.
- RC1/build 3 remains available under its original release tag.
