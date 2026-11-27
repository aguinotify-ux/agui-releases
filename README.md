# AGUI

AGUI is a Windows companion for Dota 2, with ranked hero recommendations, in-match item and skill guidance, timing reminders, and post-match reviews. The interface and built-in reminder recordings support English, Chinese, and Russian.

[Download the Windows installer](https://github.com/aguinotify-ux/agui-releases/releases/latest) · [Gitee downloads for mainland China](https://gitee.com/aguicoach/agui-releases/releases)

## What AGUI does

- **Draft with your team in mind.** Choose your rank and role, confirm the visible picks and bans, and review hero matchups and team composition. Hero pools and preferences can narrow the suggestions.
- **Plan the next purchase.** Item guidance considers your role, the revealed enemy lineup, gold, and owned components. The compact popup shows the next item and its alternative, and Match Coach lets you skip the current target. Open the full route to see when to change direction.
- **Check skill and talent choices.** View skill recommendations based on the matchup and reported skill levels, alongside the talent tree and neutral-item references.
- **Keep track of match timings.** Configure advance reminders for runes, lotuses, wisdom, day and night, the first Tormentor, stacking, and rotations. Each language has ten built-in recordings. Voice and alert sounds are mutually exclusive. Custom reminders can repeat and use an installed Windows system voice when speech is enabled.
- **Review your matches.** Inspect recorded stats, match events, and observed purchases. Available details depend on the game data received and any public records you choose to import.
- **Use an optional AI coach.** Sign in to AGUI and add your own DeepSeek, Doubao, or OpenAI API key. Enable AI-first recommendations for drafting, items, and opened match reviews. AGUI recommendations appear while AI is pending or unavailable, and the active recommendation provider is shown. Ask Coach supports questions about a live match or a selected review.

## First launch

1. Install AGUI on **64-bit Windows 10 or Windows 11**, then start it from the desktop or Start menu. The installer includes the application runtime.
2. Open **Getting started** on the home page. Follow the steps to install the game connection configuration.
3. Add `-gamestateintegration` to Dota 2's Steam launch options, keeping any existing options. Restart Dota 2 and enter a match to check the connection.
4. Set your role and rank in **Ranked picks**. Check the detected lineup and correct it when needed. The popup opens with **F8** by default. See **Settings → Hotkeys** for the current shortcuts.
5. Optionally register and verify an email account to fetch updated public statistics. Configure AI under **Settings → AI coach**, then use **Ask Coach** in Match coach or an opened match review.

The interface uses Microsoft Edge WebView2. If the runtime is missing, install the [Microsoft WebView2 Evergreen Runtime](https://developer.microsoft.com/microsoft-edge/webview2/#download-section) and restart AGUI. Cached resources remain available when offline. Account services, fresh statistics, public match imports, and AI require a network connection.

## Updating

Use **Settings → About → Check app updates**. Choose the overseas route for GitHub or the domestic route for Gitee. AGUI verifies the installer's size and SHA-256 before **Exit and install**. You can also close AGUI and run the latest installer in the existing installation directory to retain local settings and match records.

Public statistics refresh separately from application releases. The server starts its daily refresh at **08:00 UTC+8**. The client checks for published data on startup and during normal use.

## Your data

Game-state integration and normal screen recognition run locally. AGUI uses game-reported state and visible draft information. Local preferences, match records, and cached resources are stored in the installation's `data` folder.

AI is optional and may incur charges from your chosen provider. When you enable it or send a question, the relevant match summary and question go directly to that provider. API keys are encrypted on the local Windows account. Steam public-record access is optional. Feedback diagnostics and selected image attachments are sent when you submit a report. See **Settings → Data & privacy** for details.

## Feedback

Use **Report a problem** in the app. Describe what happened, preview the diagnostics, and attach screenshots if needed. For public reports, open an [issue](https://github.com/aguinotify-ux/agui-releases/issues) with the application version and reproduction steps. Keep passwords, API keys, login files, and personal screenshots private.

This repository distributes AGUI installers and release notes. AGUI is an independent project. Dota 2 artwork, names, and trademarks belong to Valve and their respective owners. Recommendations can be incomplete or mistaken, especially when game information is unavailable or a patch changes mechanics. Third-party notices are included with the installation.
