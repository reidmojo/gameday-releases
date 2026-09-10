# Gameday 0.1 RC3 — build 7

A compact league-selector update for the first leaguemate beta. Requires iOS 17+. Scores still come from the shared hosted service; no backend setup is needed.

## New since RC2/build 6

- Vertically center each league's logo, details, and trailing chevron.
- Remove the LAST label and the bottom row it occupied, reducing empty space below league details.
- Preserve pre-draft badges and unsupported-league explanations.
- Set the checked-in Xcode build number to 7 so source installations show the same version as this IPA.
- Document source installation for invited engineers using Xcode, their own Apple account, and the hosted backend.

The Games tab, custom Whiskey DST scoring, player logs, and shared score refresh remain as in RC2. This update changes no backend code.

## Download and install

Download **Gameday-0.1-build-7.ipa** below and follow the [current installation guide](https://github.com/reidmojo/gameday-releases). Invited engineers with access to the private source can build `main` in Xcode on a Mac. The IPA route still has the documented AltServer and Sideloadly authentication blockers on the maintainer's Mac. A source invitation or ability to build does not count as a successful external installation test.

Keep any existing Gameday installation. Use the same signing team and bundle identifier for updates. Free Personal Team signing expires after seven days and must be renewed. The IPA is unsigned and contains no development profile, certificate, source, or debugging symbols.

## Candidate status

Release Simulator build and visual checks passed for both real league cards. Opening a league and returning to the selector passed. Existing server, iOS, and packaging configuration suites run on the exact source revision before promotion to main. Prior backend validation remains applicable because no service changes are included.

**Still pending:** free-account installation and Home Screen reopening on another tester's phone, that tester's own Sleeper username over cellular, signing renewal and an in-place update, and a genuine uninterrupted idle-start check. This remains a prerelease; it is not stable v0.1.

## Build details

- Version **0.1 (7)**; arm64; minimum iOS 17.
- Bundle identifier: `com.personal.FantasyGameday`.
- Private app source checkpoint: `4877bb506c4decedcfa83ae4ac9238d4ce2449cf`.
- Hosted backend at packaging: `04de1de3d28232d2d3410ae169053384dcf32f7b`.
- SHA-256: `c7b414956b343f9bfa4b816aba781635b431ddbd27d281df60d340bfceb82e55`.
- `SHA256SUMS.txt` and `build.json` provide verification metadata. Source and debugging symbols stay private.
- RC1/build 3 and RC2/build 6 remain available under their original release tags.
