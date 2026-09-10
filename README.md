# Gameday for iPhone

A read-only fantasy football companion for your Sleeper leagues. No ads, roster changes, or Sleeper password. This is a v0.1 dogfood release for leaguemates; send feedback in the league chat.

## Download

Get the newest **release candidate** from [Gameday downloads](https://github.com/reidmojo/gameday-releases/releases). Download the `.ipa` file on your computer. It is intentionally unsigned: Sideloadly signs it with your own free Apple account. Downloading it in Safari on your phone will not install it.

Requires an iPhone running iOS 17 or later and a Mac or Windows PC. You do not need Xcode, GitHub access, a developer membership, or a local data server.

## Install on your iPhone

1. Install [Sideloadly from its official website](https://sideloadly.io/). Use the Mac or Windows installer for your computer.
2. On Windows, follow Sideloadly's current iTunes/iCloud prerequisites. Its instructions currently call for Apple's web installers rather than the Microsoft Store versions. On Mac, follow any installer prompts for its required components.
3. Connect and unlock your iPhone with a USB cable. Tap **Trust** when asked to trust the computer.
4. Open Sideloadly, select the iPhone, and drag the downloaded Gameday `.ipa` into it. Enter your own Apple account inside Sideloadly and follow its authentication prompts. Never send your Apple password or verification code to the league chat or maintainer.
5. Enable **automatic app refresh** in Sideloadly and start installation. Keep the default app/bundle identifier; use the same Apple account for future refreshes and updates.
6. If iOS asks for Developer Mode, enable it under **Settings → Privacy & Security → Developer Mode**, restart, and confirm. If you see **Untrusted Developer**, cancel the alert, then go to **Settings → General → VPN & Device Management**, select your developer account, and trust it. Only trust the account you just used to sign this build.
7. Open **Gameday** from your Home Screen. Enter your Sleeper username and choose your league. No Sleeper password is requested.

## Current candidate installation issue

During Mac testing, Sideloadly 0.60 reported `Guru Meditation f65043@1006:23a71c Invalid file` immediately after **Obtaining team ID**, before app signing or installation. The same attempt failed with the phone in Airplane Mode. The IPA passes archive and build validation, but a successful physical installation has not yet been observed. Do not repeatedly change your Apple password or delete Gameday in response to this error.

An optional free fallback is [AltServer's direct IPA installation](https://faq.altstore.io/release-notes/altserver): Option-click its Mac menu-bar icon (Shift-click on Windows), choose **Sideload .ipa…**, select your phone and the same Gameday IPA, then complete Apple sign-in inside AltServer. This fallback is also **unverified for this candidate**. Direct AltServer installs need manual reinstallation every seven days; AltStore is needed for its automatic refresh workflow. Use the same signing account and app identifier for updates.

## Keep it working

Free signing expires after **seven days**. Sideloadly's refresh daemon can re-sign the app before then while your computer is available and your phone is connected by USB or paired for Wi-Fi access on the same network. Enable Wi-Fi device syncing in Finder on Mac, or follow Sideloadly's Windows instructions. Let your phone reconnect to that computer regularly; refresh is not guaranteed if the computer is asleep, offline, or unreachable.

The computer is needed for signing refreshes, **not** for scores. After installation, Gameday gets data from a shared online service over Wi-Fi or cellular.

If Gameday stops opening after a week, connect the phone and run Sideloadly's refresh/install again. Keep the same account and app identifier. **Do not delete the app first.**

## Install updates

Download the next `.ipa` from the same releases page, load it into Sideloadly, and install over the existing app with the same Apple account and bundle identifier. Keep automatic refresh enabled. Your selected Sleeper account should remain connected.

## First load and connection problems

The free service sleeps after quiet periods. Its first load may take about a minute; leave the app open while it connects. Later requests are usually faster. If it fails, check your internet connection and tap retry. Free hosting can also pause if its monthly allowance is exhausted; the maintainer will post an update if that happens.

## Send feedback

On the league-selection screen, tap **… → About and help → Share feedback**. Fill in what happened, what you expected, and the league/week/game or player. Share the report to the league chat and attach a screenshot there if useful. You choose the destination; Gameday sends nothing automatically.

## Help

- [Sideloadly FAQ](https://sideloadly.io/faq.html)
- [Apple: Developer Mode](https://developer.apple.com/documentation/xcode/enabling-developer-mode-on-a-device)
- [Apple: free-account signing limits](https://developer.apple.com/help/account/basics/about-your-developer-account)

The source repository is private. This public repository contains only installation information and app releases.
