# Changelog

All notable Kpop Stan Vault changes are tracked here. The repository code remains private; issue and release links are included for project tracking.

# Kpop Stan Vault v6.8.0-261008
 
V6.8.0 gives the Member Statistics window a little more room for the History tab, and brings Bias history to public Snapshots. The History tab also keeps its "Viewing" bar pinned to the top while you scroll and scrub. It also adds a History Trend pill and a nicer trend graph for Last.fm, a link detector that suggests the group when you share or paste an Apple Music or YouTube link, album names on Last.fm top tracks, clearer dates and release details in Notifications, Excel and CSV exports, a small vibration on Android when you save a rating or tier, an error log you can copy when something goes wrong, and group pages that pick up their group's color.
 
### Added
- **History Trend pill in Last.fm Statistics**: the Last.fm window (and the same window on public Snapshots) now shows **History Trend: Rising / Stable / Dropping** next to the connected badge, just like Member Statistics. It reads your saved Last.fm samples, one per day, with the same rules, and hovering it shows the points and change behind it.
- **Group auto-detect for shared and pasted links**: when you share or paste an **Apple Music** or **YouTube** link (the phone share sheet, or Vault Tools, Attach a link), the vault looks the link up and suggests the group. Apple Music uses the artist on the link; YouTube uses the video title and channel. You always confirm: tap **Yes** to use it, **Choose another** to pick a group yourself. If two groups fit (for example a collab), you get a short "Which one is it?" list instead.
- **Apple Music links now extract right away**: once the group is confirmed (or picked), **Auto Extract** runs by itself and adds the release to that group's Discography, so there is no second tap.
- **MV link auto-detect for YouTube**: after the group is confirmed, the vault also suggests the release the video belongs to (matching the title track or release name in the video title) and offers **Yes, save MV link**. If it can't tell, you pick the release as before.
- **Bias history on public Snapshots**: open a member on a shared Snapshot and the same **History** tab you see in your own vault is there, with the same look. It only shows when the member has recorded changes, and only when the Snapshot was shared with stats included. Snapshots shared before this update won't show #rank changes until you refresh the link.
- **Excel and CSV export**: in Cloud Sync, next to **Download Backup**, there is now **Export Excel (.xlsx)** and **Export CSV**. The Excel file has a **Members** sheet (one row per member with group details, tier, affinity and rank) and a **Groups** sheet, with sized columns, a colored header row, filters and a frozen top row, so nothing shows up as "#####". The CSV is there for other spreadsheet apps: dates are written so Excel no longer shows "########", and columns with nothing in them are left out. Both are extra safety copies, not replacements for the normal backup, because they can't be restored from.
- **Vibration feedback (Android)**: a short buzz when you save a rating, a longer double buzz when a tier changes, and a soft buzz when you tap **Undo**. It does nothing on iPhone and desktop, and it stays off if your phone is set to reduce motion.
- **Error log**: **Settings, Diagnostics** now has an **Error log** card. If the app hits a problem behind the scenes it is noted there, on your device only. Tap **Copy log** and send it with your bug report. Nothing is sent anywhere automatically.
- **Group colors on group pages**: highlights, text selection, sliders, focus outlines and scrollbars on a group's page now follow that group's color.
- **Album name on Last.fm top tracks**: the Top Tracks rows in the Listening Activity window, in a group's Last.fm Statistics window, and on public Snapshots now show the album each track is from. Last.fm's top-tracks list does not include albums, so it is looked up once per track from Last.fm and remembered; the line stays hidden when Last.fm has no album for that track.
- **Clearer Notifications dates**: **Today** and **Tomorrow** now show their date too (for example "Tomorrow · Thu, Oct 8"), and the live countdown moved from every card onto its date header on the right, so each day shows it once.
- **Release anniversaries now have details**: a release anniversary card shows which anniversary it is, the release name, the years, and the original release date (for example "Drama turns 3 years · released Oct 7, 2023"). If several releases share the date it shows the first plus how many more.

### Changed
- **Last.fm Statistics chart uses the same line style**: the chart in the Last.fm Statistics window (and on public Snapshots) now draws the same smooth, glowing line as the group card, with the soft fill, a fade along the line and a pulsing "now" dot. The line passes through your real saved samples and never makes up values in between.
- **Better chart tooltip**: hovering or touching the Last.fm charts now snaps to the nearest real sample and shows its date and time, the percentage in large text, a **Latest**, **Peak** or **Low** tag when it applies, and how much it changed versus the previous sample (and versus the start of the window). It stays inside the chart instead of covering the line.
- **Last.fm widget shows 1M**: the Trend History graph on a group's Last.fm Listening card now shows the last month (marked **1M**) instead of squeezing the whole history into one line, so recent movement is easy to see. If there are fewer than two samples in the last month it shows everything.
- **Nicer Last.fm Trend History graph**: the small graph on a group's Last.fm Listening card has a smooth curve (it never invents peaks that did not happen), a soft glow and fade on the line, labelled top, middle and bottom values, dates at the start, middle and end, a green peak dot and a pulsing "now" dot. Touch and drag along it to read any sample. A flat history reads as "steady" instead of a dramatic wiggle. Public Snapshots use the same graph.
- **A little more room in Member Statistics**: the window is slightly wider and taller so the History tab fits comfortably. Text sizes and the look are unchanged.
- **Pinned "Viewing" bar in History**: the date, tier and affinity (or rank) you are looking at stay pinned at the top while you scrub the chart or scroll the list, and the "Changed on this date" details have their own card.

### Fixed
- **Recent scrobbles missed your newest plays**: once the deeper scrobble history had loaded, the Recent lists (Home Listening Activity, a group's Last.fm Statistics, the Recent Scrobbles preview on the group card, and the list saved into a Snapshot) stopped using the fresh feed, so tracks you played afterwards did not appear until you reopened the window. The two feeds are now merged, newest first, with duplicates removed.
- **Refresh and Load More no longer lose your place**: refreshing used to throw away the older scrobbles you had already loaded and reset Load More. New scrobbles now go on top and the older ones stay. Refresh also updates the Recent list from any tab of the Last.fm Statistics window, not only the Recent tab.
- **"Now playing" no longer sticks**: only the freshest feed can show a Now Playing row, so a track that finished no longer stays marked as playing.
- **Recent updates by itself**: while a Recent list is open and the app is visible, it checks for new scrobbles about once a minute.
- **Snapshots get a fuller, fresher Recent list**: updating a Snapshot link now saves up to 100 recent scrobbles for the group (it was 60), taken from the newest feed. A Snapshot is a saved copy, so it shows what was saved when you updated the link; press Update Link to refresh it.

### Good to know
- Your data format is unchanged, so older backups and other devices keep working.


# Kpop Stan Vault v6.6.0-261007
 
V6.6 adds a scrubbable Bias history for every member, an Undo for rating and tier edits, a milestone engine (Day 100 / 500 / 1,000 since debut or since you started stanning, plus release anniversaries) with toasts and push, a search box in Settings, smarter photo uploads that warn you about duplicates, and safer backups. Home and your scrobble history now stay smooth even with a big vault, and the heavier windows only load when you open them. It also fixes right-click menus closing while you scroll them and the "This app cannot be installed" message in Chrome.
 
### Added
- **Bias history**: open any member's profile and tap **Bias history**. A slider scrubs back through time and shows the member's tier and affinity (or #rank in Manual Bias groups) on that date, with a chart of tier-coloured bands, previous / next buttons that jump between days with changes, a **Changed on this date** list, and a full list of changes you can tap to jump to. It uses the history the app already keeps, so nothing new is stored. It is hidden until a member has at least one recorded change, and is not shown on public Snapshots.
- **Undo for rating and tier edits**: saving a group's rating, a member's tier or affinity (from Group info, Edit Members, or the single-member editor) now shows the same 10-second **Undo** toast as deleting. Undo only reverts values that are still exactly as that save left them, so it never overwrites a newer change. The history points written by the edit are rolled back too.
- **Milestones**: new calendar and notification events for **Day 100 / 500 / 1,000 / 1,500 / 2,000 / 2,500 / 3,000 / 3,500 / 4,000 / 4,500 / 5,000 / 6,000 / 7,000 / 8,000 / 9,000 / 10,000** since a group's debut, the same day counts since you started stanning it, and the **1st, 2nd, 3rd, 5th, 10th, 15th, 20th and 25th anniversary** of any release in its discography. Each one gets a toast on the day, and a push notification when push is on. Several on the same day are grouped into one. They appear under the **Stan** tab in Calendar and under a new **Milestones** chip on the notification board. Yearly stan anniversaries (including "1 year") already existed and are unchanged. Disbanded and unstanned groups don't get milestones.
- **Settings search**: a **Search settings** box under the Settings header. Type a word like "backup", "push" or "gemini", pick a result, and Settings jumps to the right tab, scrolls to the card and highlights it. Esc or the X clears it.
- **Duplicate-photo check**: after you pick a photo, the vault compares it with every photo you already have, even if it is a different size or file type. If it looks like the same picture, the photo editor shows a **Possible duplicate** note naming where it is used, and member uploads show a toast. It only informs: you can still save, since one group photo on several members is sometimes intentional.
- **Backup format version**: every backup file (download, linked JSON, copied data) now includes a format version.
- **Automatic backup upgrades**: when you restore or load a backup, older backups (including very old ones that were just a list of groups) are upgraded step by step to the current format first. If the confirm dialog says "Backup format v1 will be upgraded to v4 on import", that is this. A backup from a newer, unknown format shows a warning instead of being guessed at.

### Changed
- **Smaller photos on upload**: new photos are resized and compressed to a size limit (about 150 KB for member photos, 110 KB for logos, 360 KB for covers). Quality is lowered only as far as needed. Smaller photos mean less cloud storage, faster backups and sync, and a faster Home. Saving also removes hidden camera data (such as location) from the photo. Photos you already saved are not changed.
- **Home only draws what you can see**: with more than 30 groups, Home keeps just the cards near the screen and fills the rest with empty space, so scrolling stays smooth with a big vault. The **Show more** button is gone; just scroll. Card looks, density modes and returning to your scroll position are unchanged.
- **Scrobble history only draws what you can see**: the Home Last.fm Recent list and a group's Recent Scrobbles tab do the same once they pass 60 rows.
- **Windows load when opened**: Settings, Vault Stats, Stan Statistics, Wrapped, Cloud Sync, Recent Changes, the photo editor, the sync conflict screen, Tutorial and What's new are not loaded until you open them, so the app starts faster. Open and close animations are unchanged.
- **Charts load on demand**: the chart drawing is no longer part of the first load. Statistics windows still have their charts ready when they open; the few charts on the main page appear after a brief placeholder the first time.
- **Protection against request floods**: Last.fm and push features now answer "Too many requests" with a retry time if one device sends far more requests than the app ever does. It is a safety net, not a hard cap.

### Fixed
- **Right-click menus closed while scrolling**: when a context menu was tall enough to scroll, scrolling inside it closed it. Scrolling the menu now works; scrolling the page behind it still closes it.
- **Chrome said "This app cannot be installed"**: the app's install information was incomplete (no Android adaptive icon, no long-press shortcuts, no share option, wrong theme color) and was listed twice. It is restored in full and listed once, and a protected deployment can no longer block it.

### Removed
- **Unused Spotify features**: leftover Spotify code that nothing used is gone. The Spotify artist details used by AI profile fill are untouched.

### Good to know
- Photos you already saved are not recompressed. Only new uploads use the size limit.
- Backups kept in the cloud are not versioned yet; only backup files are.

# Kpop Stan Vault v6.4-261004

V6.4 brings the public Snapshot page in line with the main group page (same info chips, Stanned For / Since Debut cards, Last.fm window and Discography 2.0), gives every group one stable, readable share link per account, shows when Cloud last synced and what a sync conflict is about, and adds a quiet review queue for old affinity ratings, an MV link on every release that works in any browser, proper Android app icons, and a screen-reader pass over the buttons.

### Added
- **"Last synced 2 min ago"**: the Cloud panel's status line now reads as a live relative time ("just now", "2 min ago", "3 h ago") that keeps updating while the panel is open. It turns amber if the last sync failed or is over an hour old, and hovering it still shows the exact date and time.
- **Conflict preview**: when a sync finds a field changed on two devices, the toast and the Cloud panel now say what differed, for example "Haum's affinity: 90 here, 85 on the other device (kept this device's)", with a Review button that opens the conflict screen.
- **Make link readable**: a Share popup button for old random-number links. It switches the group to a readable link and disables the old one (you are asked first).
- **Affinity review**: Settings → Data → Vault Tools → **Affinity review** lists active members whose rating hasn't been changed in 90+ days, oldest first, with how long ago it was rated. **Review** opens the member, **Still right** confirms the rating, **Snooze 30d** hides it for a month. It is a list you open on purpose: no pop-ups, no badges. Confirming or snoozing never edits the rating or its history, and is remembered on this device only.
- **MV link on every release**: open a release in a group's discography and tap **+ MV link** (or **Edit MV link**). Paste a YouTube link and Save; leave it empty and tap Remove to clear it. It is a normal text box, so it works in every browser, including Samsung Internet and Vivaldi. The link shows as the ▶ MV chip.
- **Maskable app icon**: the installed app now has an Android adaptive icon (the S/V mark centered on the app's dark background), so the launcher can round it instead of putting it in a box.
- **Load More Scrobbles on Snapshots**: the Recent tab lists only scrobbles matched to the group's Last.fm artist, 10 at a time, with a Load More Scrobbles button. A snapshot can hold up to 60 saved scrobbles (it was 5), plus 10 top tracks and 12 top albums.
- **Added / Updated dates on Snapshots**: shown as chips, like the main page.

### Changed
- **One share link per account, not per device**: the Share popup now finds a group's link from your account, so a link made on one device can be copied, updated or disabled from any other signed-in device.
- **Update Link keeps the same URL**: it used to create a brand-new link and disable the old one every time. Now it refreshes the snapshot behind the link you already shared. **New Link** still creates a different URL on purpose.
- **Readable share links**: new links look like `/share?shareId=kiiikiii-jhuzty` (group name + account name) instead of random digits. If that name is already taken by another account or another group, it becomes `-2`, `-3` and so on, so two links can never collide. Existing random links keep working until you choose to switch them.
- **Snapshot info chips match the group page**: the same icons and order as the main entry (label, generation, flag, Debuted, Stanned, Added, Latest/Upcoming, Updated), instead of emoji. The Active / Pre-debut / Planned / Disbanded badge uses the same rules as the main app.
- **Snapshot Stanned For / Since Debut cards match**: the same icon-box layout, including "Debuting In" and "Debuts Today".
- **Snapshot Latest Release card matches**: it now shows the same release count chips ("8 releases", "4 singles", "4 EPs", "Since 2025") and the same Discography footer button.
- **Snapshot Last.fm window matches the main one**: same header, tab strip and info bar. Statistics has the chart, timeframe strip and stat cards. Ranges has the range chart. Top Music shows numbered tracks (#1, #2, #3 ...) with real track artwork and a larger album grid. Source has the artist link.
- **Snapshot Discography is now Discography 2.0**: the same window as the main app, read-only: overall rating, search, release type filters, year timeline, release cards, and the release detail view with cover art, rating, release notes, ▶ MV link and the full tracklist. Edit tools (scan, add, remove, rate) are not shown.
- **Theme colors agree**: the installed app's theme color was pink while the page was dark blue, so the status bar and splash screen could mismatch. Both now use the app's dark blue (#0f172a).
- **One icon set**: the app now uses a single, sharp icon set. The unused blurry second set is removed.

### Accessibility
- **Icon-only buttons now have names**: 26 buttons that screen readers announced as just "button" are labeled: every popup's close (X) button, the clear-search buttons, Remove member, Delete this entry, Remove from comparison, and the Home header buttons (Stan Profile, How to use, Stan Statistics, Vault Doctor, Cloud Sync, Wrapped, Settings).

### Fixed
- **MV links were wiped by discography refreshes**: refreshing or auto-extracting a group's discography blanked any saved MV link. Saved MV links are now kept.
- **Snapshot member popup on phones**: a popup that fails to open no longer crashes the whole Snapshot page: it closes and shows a short notice, and the popup's code is now fetched in the background so the first tap doesn't wait on a slow connection.
- **Manifest was linked twice**: the app's web manifest was declared twice in the page head. The duplicate is removed.

### Under the hood
- All public snapshot routes (`/share`, `/snapshot`, with or without an id) now render from one shared page, so they can't drift apart. The Discography release card, its helpers and the group lifecycle helpers moved out of the main page into shared code that the Snapshot page also uses; the main page is about 700 lines shorter.
- **Stylesheet `!important` clean-up (first pass)**: 474 declarations that a later rule with the same selector, media query and property already overrode were removed (3,942 → 3,476 `!important`). The winning value for every selector, media query and property is identical before and after, and likely browser fallbacks (`dvh`, `calc()`, `color-mix()` and similar) were kept. Layered rules were left alone.

### Removed
- **Pull to refresh in a group's Last.fm stats window**: pulling down at the top no longer triggers a refresh there. The Last.fm home window keeps it.
- An 830 KB leftover backup file from the repo.

### Good to know
- New fields (full release details, more scrobbles, Added / Updated dates) only exist in snapshots created or refreshed after this update. Open the Share popup and tap **Update Link** on each existing snapshot link; the URL stays the same.

# Kpop Stan Vault v6.0.3-261002

V6.0.3 fixes group tier history (issue #74) the "updated" toast missing on other devices, shows how fresh your Last.fm data is, adds a backup reminder, adds app-icon shortcuts, and gives deletes a proper 10-second Undo. Also adds a share target so you can send Apple Music and YouTube links straight into the vault, and remembers your Home sort  and filters. This update was supposedly to ship with 6.0

## Tracking Links

- [Issue #74 - Group stats bugs](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/74)

### Added
- **Share Apple Music / YouTube links into the vault** — on a phone with Stan Vault installed, use Share on a link and pick Stan Vault. Choose a group: an **Apple Music** link opens that group's discography import with the link filled in (tap Auto Extract), and a **YouTube** link lets you pick a release and saves it as that release's **▶ MV** link, shown in the release details. Other links are not attached. After updating, remove and re-add the app to your home screen so the phone picks up the new share option.
- **Home sort and filters are remembered** — your sort (including Most / Least Scrobbled), status tab, tier, agency, type and search scope are kept between visits on this device. The search text itself is not saved. If a remembered filter would show nothing, Home falls back to All.
- **Last.fm freshness label and pull-to-refresh** — the Last.fm Listening card on group and soloist pages, the group Last.fm Statistics window and the Home Listening Activity window now say "Updated 5 min ago". The label turns amber after 10 minutes. On a phone, pull down from the top of either Last.fm window to refresh. Coming back to the app after 10+ minutes also refreshes Last.fm quietly in the background, instead of only once per session.
- **Backup reminder** — if 7 days pass with no backup file and no cloud sync, a gentle "Time for a backup" toast appears when you open the app (tap it to download a backup). It shows at most once every 3 days and never for an empty vault. New users are counted from their first visit, so there is no nagging on day one.
- **App-icon shortcuts** — long-press (or right-click) the installed Stan Vault icon for **Add group**, **Notifications** and **Wrapped**.
- **Undo for deletes** — deleting a group or member now shows an **Undo** toast for 10 seconds (was about 6). Anything deleted can still be restored later from **Vault Tools → Recently deleted**, which keeps up to 30 items for 14 days (was 16). Restoring is safe with Cloud Sync: the restored item is not removed again by another device.

### Changed
- **Cloud sync counts as a backup** — a successful cloud sync now updates **Settings → Diagnostics → Last backup** (shown as "Cloud sync"), because your vault is then safe in the cloud. Downloads and linked JSON saves count as before.
- **"Soft Delete Bin" is now "Recently deleted"** in Vault Tools and in the delete messages.

### Fixed
- **Group tier slots not recording the tier properly (#74)** — changing the Main / Sub / Casual Ult slots used to redraw the whole group tier line from today's slots, so past tiers were rewritten and nothing was actually saved. Group tier changes are now recorded when they happen, the same way member tier changes are, and Group Stats draws its tier line from those records. Tiers from before this update are not known, so a group's line starts flat at its tier before the first recorded change.
- **"Stan Vault is updated to ..." toast missing on other devices** — a device that opened Stan Vault with groups or soloists already in it, but had never recorded a version, silently skipped the toast. It now shows once. A brand-new visitor with an empty vault still sees no toast.


# Kpop Stan Vault v6.0.2-261002

V6.0.2 is a small fix release for scrolling on phones.

## Tracking Links

- [Issue #73 - Lastfm widget on group entry lag on mobile](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/73)

### Fixed
- **Last.fm widget lagging when scrolling on mobile** — scrolling past the Last.fm Listening card on a group or soloist page no longer stutters. The card no longer jumps in height while you scroll, and swiping up or down over its small trend graph now scrolls the page instead of getting stuck. Dragging sideways on the graph still shows the values.


# Kpop Stan Vault v6.0.1-261002

V6.0.1 fixes adds a new features and fixes that are supposedly ship with v6.0 with bunch of fixes and changes
### Added
- **Backup reminder** — Settings → Diagnostics has a new **Last backup** tile ("Today", "3 days ago" or "Never"). It turns to the warning style after 7 days without a backup. Downloading a backup, saving the linked JSON, creating a new JSON database, or the auto-write to your linked JSON file all count. Cloud sync does not.
- **Backup version check** — every backup now records the app version. Restoring a backup from a **newer** version shows a warning, and so does linking a JSON file from a newer version. Older backups restore as before.
- **Update available toast** — when a new version is ready, a toast says "Tap to update". Tapping it switches to the new version and reloads. The app re-checks when you return to the tab and once an hour.
- **What's new window** — after an update, a toast says "Stan Vault is updated to vX.X.X-YYMMDD" with a link to the changelog. It shows once per version. You can also open it from Settings → About → **What's new**.

### Changed
- **Rounded corners** — corners now share four sizes across the app, so some moved by 1–4px.
- **Reduced motion** — the app now respects your device's reduced-motion setting.
- **Automatic cache reset** — the offline cache follows the app version, so updates no longer need a manual bump.
- **Last.fm naming cleanup** — internal rename of leftover "spotify" names. Nothing changes for you and no saved data is affected.
- **Code cleanup** — the home header and group detail screen moved into their own files for faster experience.

### Fixed
- **Last.fm Refresh button** — it no longer grows while loading.
- **Snapshot showing "Manual Bias System"** — groups on Affinity Assist now show the right system. Press **Update Link** once on affected groups to refresh their snapshots.


# Kpop Stan Vault V6.0-261001

V6.0 fixes a mix-up between real names and stage names that was breaking AI mode, brings full Last.fm stats to Share and Snapshot links, and cleans up several visual bugs on those shared pages.

## Tracking Links

- [Issue #72 - AI mode improvements](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/72)
- [Issue #71 - Improve the Experience of the Snapshot](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/71)

## What's new

- **Stage Name and Birth Name are now separate fields.** Every member can have both a Stage Name (their public/idol name) and a Birth Name (their real name) — each one editable by hand or filled in by AI mode, and both always shown in the member's profile popup once set.
- **Last.fm now shows up on Share and Snapshot links.** Turn it on in the Share Snapshot popup and anyone with the link sees the same Last.fm card you do — trend percentage, ranks across all six Last.fm ranges, scrobble counts, and recent scrobbles.
- **Last.fm history and a "View Full Stats" button on shared links.** The Last.fm card on Share/Snapshot pages now shows how many real samples it's based on plus a small trend graph over time, and a new "View Full Stats" button expands a full rank/score/scrobble breakdown for every range (1W, 1M, 3M, 6M, 12M, All).

## Changes
- **Redesigned Members profile info popup.** The Members profile info popup received a redesigned UI to see infos clearly and easy to read. 
- **Redesigned Settings Menu.** The settings menu has been redesigned
- **Updated Icons in Home page.** Toolbar icons has been updated

## Improved

- **AI mode now looks up idols by Stage Name instead of Real/Birth Name.** Real names rarely turn up anything on the sites AI mode checks, so it used to come back empty and show a misleading "quota reached" message instead of the real problem. It now searches by Stage Name first and only falls back to Birth Name if no Stage Name is set.
- **AI mode can now find and fill in Birth Name**, the same way it already does for birthday, height, MBTI, and everything else.
- **The Last.fm Ranges graph now labels each point by its range** (1W, 1M, 3M, 6M, 12M, All) instead of a confusing clock time like "19:45" or "21:00", which never meant anything there in the first place.
- **Last.fm widget statistics improvement.** Updated Last.fm widget statistics on Group/Soloist entry includes additions of Mini graph of listening stats, detailed info and Recent scrobbles album art. 

## Fixed

- **A big blank gap between Discography and Members List on Share and Snapshot links.** Members List was accidentally set to always start below the side panel's full height instead of right after Discography, leaving a large empty space whenever the side panel had more in it than the main content did.
- **Country flags on Share and Snapshot member cards showed as plain text** ("KR", "JP") **instead of real flag icons**, unlike the main app.
- **The Group/Member Statistics popup on Share and Snapshot links closed instantly with no animation**, instead of fading out smoothly like every other popup in the app.

## Removed
-**Removed Sources.** KPopping sources is completely removed

# Kpop Stan Vault V5.3-260925

V5.3 adds a snooze action right on push notification reminders and a way to test push notifications, tightens up a couple of security/reliability gaps, and restores real offline support.

## What's new

- **Snooze reminders right from the push notification** — birthday/comeback/anniversary push notifications now show "Snooze 1 day" and "Snooze 3 days" actions. Tapping one snoozes it on the notification board without opening the app first, whether the app was already running, backgrounded, or fully closed.
- **"Send test reminder" button in Settings** — once push notifications are turned on, a button next to "Remove this device" sends one immediate test push, so you can confirm it actually works on this device before trusting it for real reminders.

## Improved

- **Sync Improvements** — The Cloud/JSON sync icon's status dot now shows more than just "syncing" — it lights up amber when offline, red when the last sync failed, and violet when there's an unresolved sync conflict waiting for review, with a matching tooltip. Previously only syncing and a local-JSON-reconnect state showed up there at all.
- Shared vault cards (Share and Snapshot links) are no longer indexable by search engines by default, since a share link is meant for whoever you send it to, not for search results.
- **Wrapped ranking is now accurate** — anything you added partway through a month or year no longer gets penalized for the days before you added it, so new additions show up in Wrapped where they belong.
- **Wrapped now matches Top Members** — when several members are tied at 100%, Wrapped now orders them the same way Top Members (Smart) does instead of alphabetically.
- **Top Group breaks ties by listening** — when two groups are tied, the one you played more on Last.fm now comes first.
- **Applies to both Monthly and Yearly Wrapped.**

## Fixed

- **Offline mode wasn't actually caching anything.** — The service worker's offline fallback called `caches.match()` on every request, but nothing ever wrote a response into any cache, so it silently returned nothing every time you went offline. Rebuilt it with a real strategy: network-first (and cache-writing) for page loads, stale-while-revalidate for everything else.
- **The nightly reminder cron endpoint could run unauthenticated.** — If `CRON_SECRET` was ever unset in a deployment, the auth check silently skipped itself instead of refusing turning the route into a public endpoint that could push a notification to every user. It now fails closed and refuses to run without a configured secret.

# Kpop Stan Vault V5.2.1-260921
 
V5.2.1 makes the Edit Members popup faster and easier to use, adds a proper Add Member popup, and stops deleted members and entries from coming back when you use more than one device. Feature update from 5.0
 
## Tracking Links
 
- [Issue #67 - Improve the use of the members sortation popup](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/67)
- [Issue #68 - Improve the UI of the members list sortation popup](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/68)
- [Issue #69 - Dont pin to top the Pinned Group and Soloist entry](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/69)
- [Issue #70 - Recent scrobbles issue in the Lastfm statistics popup recents tab](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/70)\

## What's new
 
- **New Add Member popup** — adding a member now opens a full popup that looks just like Edit Member: photo, name, birthday, bias tier, nationality, roles and notes. Open it with the new **+** button in Edit Members, the new **Add Member** button next to **Compare All**, or from Top Members.
- **Undo and Redo** — Edit Members now has Undo and Redo buttons at the top. They work for reordering, sorting, adding and removing members (Ctrl+Z to undo, Ctrl+Shift+Z to redo).
- **Faster reordering** — every row has small up and down arrows. Tap a member's rank number to type a new rank or send them straight to the top or bottom. On a keyboard, Alt + ↑ / ↓ moves the selected member (add Shift to jump to the top or bottom).
- **Select a member and move them** — tap a member in Edit Members and they light up in your group's colour. Then use Alt + ↑ / ↓ to move them (Alt + Shift + ↑ / ↓ for the top or bottom). They stay highlighted as they move, and the popup's subtitle tells you who is selected. Tap an empty spot to deselect.
- **Sort buttons** — sort members A–Z or by birthday with one tap.
- **Unsaved changes warning** — closing Edit Members with changes you haven't saved now asks you first.
- **Auto-scroll while dragging** — dragging a member in a long list now scrolls the list for you.

## Improved
 
- The Edit Members popup is wider and roomier, with bigger pictures and buttons. The Global Bias List got the same spacing.
- The member rows are tidier: no more big empty gap, and the rank numbers line up.
- Member cards on the group page now show country flags instead of letters like "KR".
- The "Reordered" pop-up after every move is gone, since Undo and Redo do the job.
- The Back button and Escape now close the popup you're actually looking at — including notifications, the calendar, the photo editor, dropdown lists and right-click menus.
- The sync conflict notice is clearer. It only appears for something new, tells you what changed (for example "Kim ChaeYeon's birthday"), and stays quiet when you already have the conflict screen open.

## Fixed
 
- **Deleted members and entries coming back** when you use more than one device. A deletion on one device now sticks on all of them.
- **Restored items disappearing again.** Members and entries restored from the Recently Deleted bin or a backup now stay restored.
- **Flags showing as letters** like "JP" and "KR" on Windows.
- **Pinned groups and soloists** no longer jump to the top of the main Home grid; pinning only affects the Pinned Stans shelf.
- **Refresh on the Last.fm Recent tab** now actually refreshes the list.
- **Closing the single-member editor** from inside Edit Members now returns you to the popup properly.
- **Escape and Back on a member profile** now take you back to the Bias List or Calendar you came from.
- **Undo** no longer carries over into a different group, and Ctrl+Z no longer interferes while you type a name.
- **Sorting** no longer marks every member as freshly edited, which could win over your other devices.
- Fixed an issue where context menu with 10+ items are overflowed.
- Fixed a wiring issue where "Members" and "Edit group" on a group card's right-click menu (Home grid and the Pinned Stans shelf) silently navigated into that group's detail page behind the popup. Both actions reused the same flag that switches Home into the detail view, needed to make their modals work, but nothing ever cleared it afterward — so closing the popup left you stranded on a detail page you never asked to open, instead of back on Home. Closing either popup now returns to Home when it was opened this way from a card; opening the same popups from inside a group's own detail page still behaves as before and stays there on close.
- Cleaned up a hidden glitch that could add junk to saved member data. Existing data is tidied automatically.



# Kpop Stan Vault V5.1-260918

V5.1 focuses on Stan highlights add-on, several QoL improvement on countdown and a fix


### Added

- Added a "Top 3 Groups" card to Stan Statistics → Overview, below Stan Highlights — tap a row to jump to that group. Ranks each group by a blended score (60% affinity + 40% Last.fm listening), falling back to affinity alone when a group has no Last.fm match, same as Wrapped's peak-affinity fallback. Documented in the in-app Tutorial's Vault Statistics section.

### Improved

- Compact live countdown ("2d 3h" / "9h 17m" / "15m 52s", or "4m 24d" once a target is a calendar month or more out) — rewrote the countdown formatter to only show the two largest non-zero units instead of the old verbose "17 days 4h 26m 52s" style, and to switch to calendar-accurate months + days (not a flat 30-day guess) once the target is 30+ days away, so a 146-day countdown now reads "4m 24d" instead of "146d 3h". The calendar's "Upcoming · Next 30 days" list (Today / "in 3d" / "in 4d") now uses this same live, ticking countdown instead of a static day-count pill; "Today" and "Xd ago" stay as plain text since there's no meaningful sub-day target for those. The notification bell's countdown badges now use the same tighter format too, so both places read consistently.
- Notification popup split by date — the Notifications bell popup now groups entries under a date header ("Today", "Tomorrow", or the actual weekday + date) instead of one continuous list, with each section only containing events landing on that day.
- Marked the context menu's dismiss-on-scroll listener as passive, matching every other scroll/touch listener in the app — the browser no longer has to wait on JS before it can start compositing scroll on mobile while a context menu is open.

### Fixed

- Fixed the Entry Type toggle (Group / Soloist) rendering invisible or unreadable text on lighter theme colors — the active pill picked its text color with `readableOnBg`, a function meant to tint a brand color for visibility against the app's dark page background, not to pick text for a pill whose background *is* that color. For light pastel theme colors this just returned the color unchanged, making the label blend into its own background. Switched to `getContrastYIQ`, which is already used for this exact case elsewhere in the app, so the toggle is now legible for the full theme color range.

# Kpop Stan Vault V5.0-260917

V5.0 focuses on Bunch of added features, several improvements and changes

## Added

- Added right-click (long-press) context menus across Home group cards, Pinned Stans shortcuts, Active/Former Members lists, Top Members, Notifications, Listening Activity, and Stan Statistics
- Added "View Statistics" and "Members" quick actions to group context menus
- Added a live countdown timer to the notification board (e.g. "17 days 4h 26m 52s") instead of a flat day count
- Added member and group photos to the calendar day hover preview instead of plain color dots
- Added a "Refreshed ..." freshness label to Listening Activity that updates live (Just now / 5m ago / 2h ago)
- Added a yearly "Wrapped" recap — #1 bias and #1 group by peak affinity, biggest affinity climber, rising bias, tier promotions, groups and members added that year, a top 5 by peak affinity, and a Last.fm listening card with total scrobbles and estimated hours. Opens from Vault Tools, steps back through previous years, and copies to the clipboard as a shareable summary
- Added a Monthly view to Wrapped alongside the original Yearly one — same recap (top bias/group, climbers, promotions, additions, top 5, listening card), scoped to a single calendar month instead of a year. Switch between Yearly and Monthly with a tab inside Wrapped, and step back through previous months the same way years already worked. The listening card uses Last.fm's rolling 1-month window in Monthly mode (12-month in Yearly), and is only shown for the current month/year since Last.fm doesn't expose calendar-accurate history
- Added a dedicated Wrapped button to the Home screen header (next to the Cloud/JSON sync icon), so Wrapped no longer requires opening Settings → Vault Tools first
- Added a Cloud Sync conflict screen — when the same field was edited on two devices since the last sync, the merge now records it and shows both versions side by side (This device / Other device) with the timestamps and which one was auto-kept, so you can flip the decision
- Added a "Tap to review" conflict toast that opens the conflict screen directly
- Added dismissible issues to Vault Doctor — each row can be dismissed with a "Dismiss" button, collects in a new Dismissed tab, and can be restored one at a time or all at once
- Added "Tap to undo" on the toast after deleting a member or group — restores instantly without a second confirmation, on top of the existing 14-day Soft Delete Bin recovery
- Added a Compact / Comfortable / Spacious density toggle for the home grid and list views
- Added drag-to-reorder on Pinned Stans shortcuts, independent of the real group ranking
- Added "Unread only" filter, "Snooze until tomorrow", and a bulk "Show all snoozed" control to the notification board
- Added saved filter presets on Home — save the current search/status/sort combo as a named chip and reapply it later
- Added Quick-look peek — hover-hold a home group card (desktop) to see a compact summary (photo, rank, affinity, member count, tier breakdown, debut date, members list) without opening the full card. Skipped on touch devices since long-press there already opens the context menu, and stacking two long-press gestures on the same card would just create a confusing conflict.

## Improved

- Improved the context menu with a header (photo + name), keyboard navigation (arrows, Home/End, Escape), and a new opening animation with a staggered row reveal
- Improved app performance by fixing a cloud sync bug that was silently recreating functions on every render, which had been defeating the group grid's re-render protection almost constantly
- Improved the boot loading screen to use the app's actual branded wordmark and a richer status pill instead of plain placeholder text
- Improved the "4H"/"4M" relative-time badges so hours read as "hr" instead of a single letter, removing the mix-up at small sizes
- Updated the in-app "How to use" tutorial with every new feature added this session

## Fixed

- Fixed the search bar breaking into an oversized, unstyled stacked layout at certain window widths (1024–1179px)
- Fixed a loading-screen flicker on boot for signed-in Cloud Sync users, caused by the auth check not being awaited correctly
- Fixed notification timing lag caused by background-tab throttling by re-checking the moment the app is foregrounded again
- Fixed a dead/unused state variable left over from an earlier build
- Fixed Top Members rows re-rendering on every modal update regardless of whether that row's own data changed — the row click/remove handlers were being recreated fresh on every render instead of reused
- Fixed the same tier-badge styling being rebuilt from scratch on every row render across both Top Members and the group's Active Members list — now computed once and reused
- Fixed the notification board's live countdown re-rendering the entire notification list every second instead of just the countdown number itself
- Member icon sortation in the group card has been fixed. Linked to Members list

## Changes

- Manual Bias sorting now disables affinity sorting mode
- Changed Cloud icon to dynamic icon whether if its JSON linked or Cloud sync

# Kpop Stan Vault V4.5-260911

V4.5 focuses on QoL Updates, Polishes, New features and several improvements and fixes

## Tracking Links

- [Issue #63 - Update Gemini deprecated models](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/63)
- [Issue #64 - Scan discography bug](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/64)
- [Issue #65 - Cloud sync when signed out issue](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/65)


## Added

- Added MBTI and Top Picks in Stan Statistics
- Added Last.fm cloud sync
- Added a hover preview on calendar days
- Added No. of scrobbles each group and soloist


## Improved

- Stan Statistics can now display Smart Top 1 from Top Members
- Gemini Models has been updated and improved
- Slightly Improved and Repolished Notification popup
- Improved Sign Out experience, now deletes entry when signing out of Cloud sync
- Slightly repolished tabs
- "A to Z"/"Z to A" now sort by group/soloist name (case-insensitive),
- "Newest Debut"/"Oldest Debut" now sort by debutDate, with the same "unknown date parses to 0" convention the existing "First Stan" sort already used.


## Fixed

- Scan discography bug scan has been fixed
- Top Member mismatch in Stan Statistics from Top member smart has been fixed

# Kpop Stan Vault V4.2-260907

V4.2 focuses on UI changes, Several Improvements and fixes

## Tracking Links

- [Issue #60 - Settings needs rearrangement](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/60)
- [Issue #61 - AI mode still needs consistency](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/61)

## Added

- New Loading vault screen when opening the Stan Vault

## Improved

- Some UI elements has been improved
- Recent Scrobble activity usability has been improved
- Settings UI has been rearranged
- Member info Group Button now redirects to its group entry
- Notification messages has been improved
- General Performance Improvements
- Cloud Sync now includes Last.fm Statistics

## Fixed

- No Push Notification has been addressed
- AI mode consistency on 2nd scan is fixed, I guess

## Removed

- Install Stan Vault Button

# Kpop Stan Vault V4.0-260905

V4.0 focuses on Real time push notification and Several improvements.

## Tracking Links

- [Issue #56 - Rank statistics bug](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/56)
- [Issue #57 - Notification support](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/57)
- [Issue #58 - Recent scrobbles visibility](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/58)
- [Issue #59 - Improve the QoL and functionality of Last session restore.](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/59)


## Added

- Real time push notifications (Settings -> General -> Push Notifications)

## Improved

- Cloud performance improvements
- Security of Cloud Database improvements
- QoL improvements of the Last Session Restore New LAST_ACTIVE_TS_KEY (kpop_vault_last_active_ts) is stamped the moment the user genuinely leaves — tab hidden, pagehide, or beforeunload — not just on navigation. New LAST_SESSION_RESTORE_MIN_AWAY_MS = 2 minutes. On load, restoreLastViewedGroup now computes awayMs = now - lastActiveTs. If under 2 min, it skips the restore and lands on Hub. If 2+ min (or no timestamp at all, e.g. first-ever load), it restores as before
- Recent Scrobble visibility can now show up to 14D


## Fixed

- Rank Statistics Bug on All and 1Y has been fixed
- AI mode sometimes doesn't detect new group such as TUIDE and OURBIRTHDAY

## Removed

- Several Dead codes has been removed and refactored


# Kpop Stan Vault V3.2.1-260818

This update focuses on AI mode scan improvements. 

## Tracking lists
- [Issue #55 - AI mode can read former members and it will flagged as Former member](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/55)

## Added

- AI mode can read Former members "ifMember: Former" then it will flag as Former Member of the Group.

# Kpop Stan Vault V3.2-260817

This update focuses on Manual Bias rank accuracy, soloist share-page parity, and a handful of fixes across the main app.

## Tracking lists
- [Issue #52 - Fix Snapshot for both Soloist and Groups](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/52)
- [Issue #53 - Add Filter for both Group and Soloist](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/53)
- [Issue #54 - Rank statistics of each member in group entry and soloist is not working](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/54)

## Added

- Advanced Filter: "Groups" option, alongside the existing "Soloists" filter
- Soloist Details card: subtle entrance animation

## Improved

- Share page: "Group Description," "Group Stan Info," "Group Profile," "Group Affinity," "Group Affinity Graph," and "Members List" now read correctly for soloist entries instead of always saying "Group"
- Renamed "Edit Group Stan info" to Edit Soloist Stan Info" for Soloist Entry

## Fixed

- Build error: duplicate closing tag in the Last.fm Top Songs modal
- Manual Bias rank (#N) not saving, and rank history not recording, when reordering via Edit Members
- Global Bias List: rank history could be off by one when a former/hiatus member was mixed into a group
- Share page: soloist profile icon showed a placeholder instead of the member's own photo
- Share page: large empty gap between the description and Members List sections
- Member Statistics → Rank tab: 1Y/ALL charts back-dated the current rank all the way to the window edge even for members added days ago — now starts from the entry's actual creation date, matching the Statistics tab

# Kpop Stan Vault V3.0-260808

V3.0 focuses on Soloist Support, Last.fm Add-ons, Few QoL improvements and Performance Improvements

## Tracking Links

- [Issue #44 - AI Mode still detects Disbanded status on the Active Groups](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/44)
- [Issue #46 - Add a checkbox in AI review field](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/46)
- [Issue #49 - Fix all buttons not the same rounded corners as One UI 8.5 and the Loading Animation uses RefreshCW on some buttons](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/49)
- [Issue #51 - Add Recent Scrobbles](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/51)


## Added

- Last Session Restore 
- Checkbox "Flag as Wrong" in AI review Field
- Soloist Stan Support same functionality as Group Stan
- Last.fm Recent Scrobbles

## Improved

- Renamed Top Music to Listening Activity in Home Page
- AI Mode still detects disbanded Groups

## Fixed

- Some Buttons, Loading Animation and Mobile UI inconsistencies has been fixed
- Performance Improvements especially on the Mobile UI

## Removed

- Completely Removed Audio Badges 

# Kpop Stan Vault V2.5-260716

V2.5 focuses on last.fm and Spotify Support Drop and QoL Improvements

## Tracking Links

- [Issue #43 - Audio Badge issues](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/43)
- [Issue #42 - Header Improvements](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/42)
- [Issue #47 - Last.fm integration](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/47)


## Added

- Last.fm integration uses only last.fm username

## Improved

- Improved Handling for the last.fm with no scrobbles between last.fm and group entry

## Fixed

- Performance Improvements

## Removed

- Spotify Integration
- Audio Badges on the Discography Entry
  

# Kpop Stan Vault V2.0-260709

V2.0-260709 focuses on Discography 2.0, Spotify Integration, Spotify read-only listening context, trusted profile source links, unified Sync & Backup, and updated in-app guidance.

## Tracking Links

- [Issue #36 - Spotify listening trends as a later/beta feature](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/36)
- [Issue #37 - Discography 2.0 with release details, tracks, pictures, and rating display](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/37)
- [Issue #38 - KProfiles source link per group, placed cleanly inside Group Info](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/38)
- [Issue #39 - JSON sync fallback for mobile/no cloud sync](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/39)

## Added

- Added Spotify read-only listening context for saved groups.
- Added Home Top Music with matched top tracks and derived top albums across linked groups.
- Added Spotify Top Music search for tracks, albums, groups, artists, and saved album-track text.
- Added Spotify range controls for LM, 4W, 6M, and ALL, with clearer labels for recent-play and top-item windows.
- Added per-group Spotify Statistics, Ranges, Top Music, and Source surfaces.
- Added Spotify listening trend snapshots that stay separate from affinity, bias tiers, manual order, ranking history, and Stats history.
- Added Group Edit AI Mode support for exact Spotify artist-link lookup when Spotify is connected.
- Added trusted KProfiles/KPopping source-link support inside Group Info and Edit Group.
- Added Discography 2.0 release detail view inside the Discography modal.
- Added Apple Music/iTunes-backed release cover art, collection IDs, release type, track counts, and exact tracklists when available.
- Added personal release ratings without changing source-backed release metadata.
- Added source-backed audio badges for DOLBY ATMOS, HI-RES LOSSLESS, and LOSSLESS.
- Added a unified Sync & Backup popup for Cloud Sync and JSON fallback workflows.
- Added updated Quick Tour sections for Spotify Top Music, Discography 2.0, Sync & Backup, source links, and safer chart/timeframe guidance.

## Improved

- Improved Spotify matching safety by using saved Spotify artist IDs, direct Spotify links, names, aliases, Korean names, discography hints, album hints, and trusted profile source hints.
- Improved Group Edit AI Mode so the same AI review flow can include an exact Spotify artist link without directly changing affinity, bias tiers, manual order, ranking history, or Stats history.
- Improved Spotify UI clarity by keeping Top Music, Ranges, and Statistics labels visually consistent and less confusing.
- Improved Apple Music/iTunes scan acceptance so valid collection URLs and route match maps can be used more reliably.
- Improved Apple release matching by separating broad search hints from stricter artist-identity approval.
- Improved Discography scans so older saved entries can be enriched with exact tracklists instead of requiring manual repair first.
- Improved tracklist merging by comparing actual track title/order signatures instead of only matching track counts.
- Improved Discography detail navigation so release details can be opened and backed out of inside the same modal flow.
- Improved audio badge parsing so only source-confirmed labels are shown.
- Improved Sync & Backup clarity by showing JSON mode as paused while Cloud Sync is active.
- Improved Settings Data behavior by moving backup/restore work into the unified Sync & Backup flow.
- Improved chart timeframe chip styling across Spotify Statistics, Spotify Ranges, Spotify Top Music, Affinity Stats, compare series, and Compare All Members.
- Improved chart hover tooltip behavior so compare overlays stay compact and less intrusive.

## Fixed

- Fixed Apple Music/iTunes scan results that could be found by the route but rejected by the client as “no update.”
- Fixed incorrect Apple/iTunes match keys that caused valid release results to be harder to merge safely.
- Fixed false DOLBY ATMOS labels caused by loose parsing of false audio fields.
- Fixed wrong same-count tracklists being kept when the actual track titles/order did not match.
- Fixed mojibake by switching corrupted visible text and affected alias text back to proper Unicode.
- Fixed Group Info profile source pill support for saved KProfiles/KPopping links.
- Fixed JSON restore being available while Cloud Sync is active, preventing cloud/local restore conflict.


# Kpop Stan Vault V1.6-260703

V1.6 focuses on AI progress feedback, mobile responsiveness polish, cloud-sync login clarity, and cleaner review surfaces.

## Tracking Links

- [Issue #33 - Mobile site UI laggy on some devices](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/33)
- [Issue #34 - Cloud sync log in experience](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/34)
- [Issue #35 - AI mode progress bar, percentage](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/35)

## Added

- Added an AI progress toast for source-backed AI review with a progress bar and percentage.
- Added scan-progress text inside the Discography scan control while release checks are running.
- Added member familiarity bulk editing in the Bulk Edit Workspace.

## Improved

- Improved AI progress estimates with phase-capped progress for source lookup, review parsing, and ready-to-review states.
- Improved AI review readability on desktop and mobile, including long saved values, suggested values, source chips, and review summary cards.
- Improved mobile responsiveness on constrained Android/iOS browser layouts while keeping the same desktop-style visual language.
- Improved Cloud Sync login/status wording so the sign-in experience is cleaner and less cluttered.
- Improved toast stack behavior, special toast visuals, and AI progress feedback so they share the same notification placement and motion style.
- Improved Bulk Edit Workspace usability for member-facing fields without changing affinity, tier, rank, or manual order.

## Fixed

- Fixed mobile AI review cards splitting or truncating important review text.
- Fixed AI progress feedback feeling disconnected from normal toast notifications.
- Fixed Discography scan progress appearing in the wrong place during active scans.
- Fixed mobile-only lag from heavier visual/rendering paths on some devices.


# Kpop Stan Vault V1.4-260701

V1.4 focuses on source-backed AI recognition for group profile pages, clearer home-card Familiarity, better discography categorization, and updated in-app guidance.

## Tracking Links

- [Issue #6 - Add overall member familiarity on group cards](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/6)
- [Issue #31 - Improve AI recognition for group and member info](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/31)
- [Issue #32 - Add an ability to view all changes in AI review info](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/32)

## Added

- Added compact member familiarity summaries to home group cards.
- Added home-card familiarity tooltips with average progress and mastered-member count.
- Added a View All control in AI review so every suggested field change can be inspected before applying.
- Added refreshed Quick Tour coverage for AI Fill review, source-backed group/member matching, member Familiarity, discography filters, personal release ratings, Date Dashboard, Recent Changes, Cloud Sync, and installable app support.

## Improved

- Improved the home group-card familiarity meter width so it lines up with the logo/content lane and affinity area instead of stretching across the whole card.
- Improved the home group-card familiarity placement so it stays near the release pill lane without crowding the affinity percentage or footer controls.
- Improved Discography type filters so Mini Album, EP, and Album releases use separate buckets and no longer inflate each other's counts.
- Improved release type badges so saved album-title fields display as Mini Album, EP, Single, or Album based on the actual release category.
- Improved member-list readability so long member names and tier labels wrap cleanly instead of cutting off with ellipses.
- Improved AI Fill review readability so long reviewed field values and source labels wrap instead of truncating.
- Improved AI review behavior so large reviews no longer hide remaining items behind a passive "+more review items" message.
- Improved Quick Tour search wording so Familiarity, discography rating, AI mode, backup, sync, PWA, and safety topics are easier to find.
- Improved KProfiles group profile parsing for pages where members are embedded directly inside the group page.
- Improved member lookup for groups whose members do not have separate individual profile pages.
- Improved group-page member merging so verified lineup names are kept when detailed member sections are partial.
- Improved direct profile matching for stylized/common names such as BTS and IZ*ONE.
- Improved entertainment/agency extraction from KProfiles intro text when no separate agency field is present.
- Improved short group-name matching so names like IVE must match exact profile tokens instead of being detected inside unrelated names.
- Improved entertainment/label extraction so member facts and stage-name meanings cannot be saved as the group agency.
- Improved disbanded-group detection for KProfiles pages that clearly say the target group officially disbanded or is now unofficially disbanded, plus exact-name fallback checks against KProfiles disbanded group lists while avoiding member-history false positives.
- Improved active/former/hiatus member status accuracy by requiring member-section or target-group evidence.

## Fixed

- Fixed source-backed AI lookup missing members that are present inside their group profile page.
- Fixed IVE-style short-name lookups being able to open the wrong KProfiles page.
- Fixed Weeekly-style profile pages parsing member fact text as the group company.
- Fixed group cards missing overall member familiarity progress.
- Fixed tripleS returning too many members; the verified KProfiles lineup now resolves to 24 current members.
- Fixed sidebar/navigation text leaking into profile member counts.
- Fixed KProfiles fact bullets being treated as member names.
- Fixed debut date extraction choosing unrelated anniversary/reveal dates.
- Fixed active/former member-list names being clipped in compact two-column member cards.


## V1.3-260629

Tracking links:

- [Issue #21 - Autocorrect Members and Group in AI mode](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/21)
- [Issue #22 - AI gathers wrong information](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/22)
- [Issue #23 - Cloud Sync Improvements](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/23)
- [Issue #24 - Installable app support](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/24)
- [Issue #25 - Pre-debut handling in notifications board](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/25)
- [Issue #27 - Vault Doctor UI messed up in Mobile UI](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/27)
- [Issue #28 - Add overall personal rating in the discography tracker](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/28)
- [Issue #29 - Add delete confirmation popup on recent changes](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/29)
- [Issue #30 - Edit modal popup picture preview rounded corners](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/30)
- [Repository](https://github.com/Jhuztyyy/kpopstanvaultmain)
- [Releases](https://github.com/Jhuztyyy/kpopstanvaultmain/releases)

### Added

- Added source-backed AI review support for member name corrections.
- Added AI member schema fields for official `name` and `stageName`.
- Added AI member lifecycle fields for `active`, `hiatus`, and `former` status review.
- Added support for extracting member data from KProfiles group profile pages when individual member pages do not exist.
- Added direct source URL propagation into AI review suggestions.
- Added installable app support through the Next.js app manifest, app icons, and service worker registration.
- Added app logo/icon metadata for browser install surfaces.
- Added pre-debut notification handling so future debut dates show as debuting events instead of anniversaries.
- Added an overall personal rating summary in the Discography modal based on saved release ratings.
- Added a confirmation warning before clearing the Recent Changes action log.

### Improved

- Strengthened AI Fill source policy for Member Info and Group Info.
- Preferred KProfiles first, then KPopping, for profile facts.
- Improved member matching so safe casing/spelling/stylization corrections can be reviewed instead of blocked.
- Improved member status matching so AI can suggest Former/Hiatus only when an allowed source clearly confirms it.
- Improved newer/niche group support where KProfiles stores all members inside one group profile page.
- Improved AI prompts so official member names come from profile headers/member rows.
- Improved KProfiles group-page parsing for member rows, active-name extraction, former-member detection, debut dates, company, country, fandom, and disband status.
- Improved cloud sync conflict protection with last-known cloud snapshots and safer outgoing group/member reconciliation.
- Improved cloud sync so stale device saves reconcile with newer cloud rows before upload.
- Improved cloud sync safety so a device delays upload instead of overwriting another device when the latest cloud row cannot be compared.
- Improved cloud restore bookkeeping so restored cloud data updates the local sync snapshot baseline.
- Improved AI member-description review so generic source membership sentences do not replace richer saved member notes.
- Improved browser install compatibility with explicit manifest id, app icons, and maskable icon metadata.
- Improved pre-debut date handling across notification filters, notification rows, calendar grouping, and event opening.
- Improved Vault Doctor mobile readability with larger small text, safer wrapping, and stacked narrow grids.
- Improved edit-photo crop preview corner consistency while panning or zooming images.

### Fixed

- Fixed `AI could not confidently match this member` for source-backed group-profile member rows.
- Fixed styled-name corrections such as `ME:U` resolving to the official KProfiles spelling `Meu` when the group page confirms the member.
- Fixed typo-like member lookups such as `Hyeren` resolving to official `Hyerin` when KProfiles confirms the group/member.
- Fixed AI review not offering source-backed active/hiatus/former member status corrections.
- Fixed profile-source handling so Kpop Fandom is not used as an automatic Member Info/Profile source.
- Fixed wrong-info risk for birthdays, roles, height, weight, blood type, MBTI, and nationality by keeping uncertain fields empty.
- Fixed notification board labeling for pre-debut groups with future debut dates.
- Fixed pre-debut groups appearing as normal group anniversaries in Notifications.
- Fixed stale-device cloud pushes that could revert newer profile/member info after an affinity-only edit.
- Fixed cloud push fallback behavior so failed conflict preflight keeps edits local instead of pushing stale data.
- Fixed synced local state after cloud upload so conflict-reconciled rows and uploaded image URLs stay aligned on the current device.
- Fixed KProfiles group-page member fallback suggesting generic descriptions such as `KProfiles lists Newy as a member of Keyveatz.`
- Fixed Recent Changes clearing too quickly without a warning.
- Fixed media crop previews losing rounded corners inside the edit photo popup.


## V1.0-260628

### Added

- Added app version display in Settings -> About.
- Added GitHub repository and GitHub Releases links in Settings -> About.
- Added manual personal rating per discography/release item.
- Added Date Dashboard month grouping for birthdays and debuts.

### Improved

- Improved Settings -> About layout, spacing, and rounded-corner consistency.
- Improved Date Dashboard scroll behavior.
- Improved discography rating UI, save responsiveness, and toast behavior.
- Improved cover photo button readability.
- Improved Open Discography tooltip placement.

### Fixed

- Fixed Group Affinity Stats line-splitting so old chart history is not repainted using only the current tier.
- Fixed broken GitHub icon import by replacing it with a local inline GitHub mark.
- Fixed Turbopack compile panic caused by decorative Unicode comment lines.
- Removed the debut-month member/detail list from Date Dashboard.
- Removed the "Saved" text from the personal rating UI.
