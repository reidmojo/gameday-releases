# Gameday 0.1 — release candidate 1 (build 3)

An iPhone companion for your Sleeper leagues with league selection, matchups, live game fantasy scoring, player game logs, and expandable drive play-by-play. No Sleeper password, ads, roster changes, or local backend setup.

This candidate uses the shared free HTTPS service. A first load after inactivity may take about a minute. The app includes connection retry handling, About/help, and an editable feedback report you can share yourself.

## Install

Download **Gameday-0.1-build-3.ipa** below on a Mac or Windows PC, then follow the [installation guide](https://github.com/reidmojo/gameday-releases#install-on-your-iphone). iOS 17+ is required. The IPA is unsigned; Sideloadly signs it with your own free Apple account. Signing lasts seven days, so enable Sideloadly refresh and reconnect to your computer regularly.

For updates, use the same Apple account and bundle identifier and install over the existing app. Do not delete Gameday first.

## Candidate status

Automated server and iOS checks passed. A 24-client, two-league load simulation completed 385 requests without throttling or failures and peaked at 271 MiB of process memory. The IPA passed configuration, architecture, signature, provisioning, and content validation.

**Installation testing is still pending:** actual free-account Sideloadly installation, reopening from the Home Screen, signing refresh, an in-place update, and another tester using their own username over cellular. This is a prerelease for those checks, not the final v0.1 approval.

A Mac installation attempt currently fails in Sideloadly 0.60 at **Obtaining team ID** with `Guru Meditation f65043@1006:23a71c Invalid file`. This occurs before app signing/installing; a successful Sideloadly installation is still required. The optional AltServer fallback is unverified. See the guide's current installation issue section before testing.

## Build details

- Version 0.1, build 3; arm64; minimum iOS 17.
- Bundle identifier: `com.personal.FantasyGameday`.
- Private source checkpoint: `c5e1d08144d2d1594ea0cd8d2e3ceb3c31aae077`.
- `SHA256SUMS.txt` verifies the IPA; `build.json` records the app source and service revision observed during packaging. The hosted service may later move to compatible tested commits.
- Debugging symbols and source are retained privately.
