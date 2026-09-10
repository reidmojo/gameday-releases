# Gameday for iPhone

A read-only fantasy football companion for your Sleeper leagues. Follow matchups, NFL games, player stats, and drive-by-drive action without ads, roster changes, or a Sleeper password. Scores come from one shared online service; testers do not run a backend.

## Download

**Current candidate: [Gameday 0.1 RC2 — build 6](https://github.com/reidmojo/gameday-releases/releases/tag/v0.1.0-rc.2).**

- [Download Gameday-0.1-build-6.ipa](https://github.com/reidmojo/gameday-releases/releases/download/v0.1.0-rc.2/Gameday-0.1-build-6.ipa)
- [Release notes](RELEASE_NOTES_0.1.0-rc.2.md)
- [All releases, including older builds](https://github.com/reidmojo/gameday-releases/releases)

Requires an iPhone running **iOS 17 or later**, a Mac or Windows PC, a USB cable for initial pairing, your own Apple account, and your Sleeper username. No GitHub account, source checkout, Xcode, developer membership, or paid hosting is required. The IPA is unsigned; your installer signs it for your phone.

**Installation testing is currently blocked:** build 6 passed automated checks and was installed and opened using the maintainer's development signing setup, but both Sideloadly and AltServer have failed during Apple authentication on the test Mac. No free-account installation, signing refresh, or installer update has passed yet. The instructions below are reference steps, not a verified onboarding path. Hold off on inviting the whole league until installation testing succeeds.

## Install on your iPhone

### AltStore Classic — blocked by an observed sign-in error

Use **AltStore Classic** with **AltServer** on your computer.

Our Mac test of AltServer 1.7.2 (build 90) failed while installing AltStore with **“Encountered unknown tag html on line 1” / `NSCocoaErrorDomain 3840`**. It received HTML where its Apple sign-in parser expected a property list; this happened before Gameday was imported. The [upstream report](https://github.com/altstoreio/AltStore/issues/1781) matches the error. AltStore's maintainer [merged a related authentication fix on September 8, 2026](https://github.com/rileytestut/AltSign/pull/52), but a successful install with an official fixed build has not yet been verified here. This error alone does not establish that the Apple password is incorrect. Rebuilding or deleting Gameday does not address this stage of installation.

The official Mac download checked on September 10 still identified itself as 1.7.2 (build 90). The next AltStore acceptance attempt should use an official release confirmed to include the authentication fix; repeated attempts with the failing build do not count as a workaround.

1. Install AltServer using the official [Mac guide](https://faq.altstore.io/altstore-classic/how-to-install-altstore-macos) or [Windows guide](https://faq.altstore.io/altstore-classic/how-to-install-altstore-windows). Windows requires Apple's iTunes/iCloud components; follow the current guide for supported installers.
2. Connect and unlock your iPhone over USB. Complete the computer/phone Trust prompts. Enable Wi-Fi device syncing in Finder on Mac or iTunes on Windows so later refreshes can work wirelessly.
3. Open AltServer's menu, choose **Install AltStore**, and select your iPhone. Enter your own Apple account in AltServer and complete its authentication prompts yourself.
4. On iPhone, follow the developer trust prompt under **Settings → General → VPN & Device Management**. Enable **Developer Mode** under **Settings → Privacy & Security** if iOS requests it, including its restart/confirmation. Open AltStore Classic.
5. Download the build 6 IPA from the link above in Safari on your iPhone and save it in Files. In AltStore, open **My Apps → +**, select that IPA, and complete any sign-in prompts. Keep AltServer running and your phone connected during installation.
6. Open **Gameday** from your Home Screen, enter your Sleeper username, and select a league. No Sleeper password is needed.

Downloading an IPA alone does not install it. AltStore handles the signing/import step. Do not send Apple passwords or verification codes to the maintainer or league chat.

### Already have Gameday installed?

**Keep the existing app until the new installation is working.** For routine updates, use the same installer, Apple account, and app identifier and install over the existing copy. Do not delete Gameday first.

Changing from an Xcode-installed copy or another signing tool can change the signed app identifier and produce a separate Gameday icon, or an installation conflict. Settings may not transfer to a separate copy; enter your Sleeper username there. If the installer reports a conflict, record the exact error and contact the maintainer before deleting anything. A successful Xcode update does not establish that an installer migration preserves data.

### Sideloadly — alternative with a known unresolved issue

[Sideloadly](https://sideloadly.io/) can sign the same IPA on Mac or Windows: pair the phone, load the IPA on the computer, sign in inside Sideloadly, enable automatic refresh, and install. Follow its [official FAQ](https://sideloadly.io/faq.html) for prerequisites, trust prompts, and updates.

Our Mac test of Sideloadly 0.60 failed at **Obtaining team ID** with `Guru Meditation f65043@1006:23a71c Invalid file`, before signing or installing. The same attempt failed with the phone in Airplane Mode. The archive and build validate successfully, but this installer path remains unverified. Do not delete Gameday or repeatedly change your password to address that error.

## Keep it working

Free signing expires after **seven days**. AltStore attempts background refresh through AltServer; you can also use **My Apps → Refresh All**. Leave AltServer running and let your phone connect to that computer regularly over the same Wi-Fi or USB. Automatic refresh is not guaranteed while the computer is asleep or unreachable. See [AltStore refresh behavior](https://faq.altstore.io/altstore-classic/your-altstore).

If AltStore itself expires, reinstall AltStore through AltServer with the same Apple account, then refresh Gameday. If an error appears, keep the installed apps and share the error with the maintainer.

The computer supports signing and refresh. Once installed, Gameday gets scores directly from the shared service over Wi-Fi or cellular.

## Install updates

Download the next IPA from this repository and import it through the same installer and Apple account. Install over the existing copy; do not delete it first. Check **… → About and help** in Gameday for the version/build. Build 6 is version **0.1 (6)**.

Some wording in build 6's Help sheet still names Sideloadly. Its installation link opens this current guide, which also covers the AltStore path.

## First beta session

- Open the app from the Home Screen and enter your own Sleeper username.
- Check your league, Matchups/Games switching, a game, and a player log.
- Turn off Wi-Fi temporarily and confirm data works over cellular, then restore your normal connection.
- Try closing and reopening Gameday. Later, verify a signing refresh and an update through the same installer.
- Share problems via **… → About and help → Share feedback**. Add what happened, what you expected, and the league/week/game or player, then choose the league chat yourself. Attach a screenshot if useful. Gameday sends nothing automatically.

## First load and connection problems

The free service sleeps after quiet periods. A first load may take about a minute; leave Gameday open while it connects. If it fails, check your connection and tap retry. Quota exhaustion can also temporarily suspend the free service. There is no automatic paid upgrade.

The source repository and debugging symbols stay private. This public repository contains installation information and release artifacts only.
