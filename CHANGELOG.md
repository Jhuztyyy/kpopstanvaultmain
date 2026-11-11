# Changelog

All notable Kpop Stan Vault changes are tracked here. The repository code remains private; issue and release links are included for project tracking.

# Kpop Stan Vault v8.5.1-261112

## Improved

- **Older listening dates**: opening a month in the listening calendar checks that month directly on Last.fm. Full history gathering continues in the background for artists saved in your vault.
- **History across devices and backups**: gathered scrobbles, checked months and unfinished history gathering are included in Cloud Sync, downloaded JSON and linked JSON files. Profile details, manual member positions and saved photo crops remain included too.
- **Linked backup updates**: linked JSON files keep saving while Cloud Sync is connected, including fresh listening statistics and Wrapped results. File updates run in order so an older save cannot replace a newer one.

## Fixed

- **Update notices and What's New**: the updated-version notice waits until your vault finishes loading, and unread release notes open automatically once the screen is free. Missed notices from an earlier startup can recover without repeating after you read the notes.
- **Missing older scrobbles**: older completion records are checked again instead of assuming a small saved sample contains your whole history. Incomplete Last.fm replies no longer mark a scan finished.
- **Misleading empty dates**: the calendar distinguishes history that has not loaded yet from a checked month with no matching listens.
- **Newest listens first**: selecting a day or date range lists scrobbles from latest to oldest, including history restored from a file.
- **Full mobile Recent list**: date controls scroll with the scrobbles instead of covering them. The group list uses one scrolling area, so you can reach every loaded listen without a second cramped scrollbar.
- **Clearer scrobble loading**: Recent uses the same saved-history loader throughout the vault. New results appear as each batch arrives, interrupted checks offer a retry, and the end of your available history is clearly marked instead of showing an ineffective Load More button. Reopening or refreshing Recent keeps your already-loaded listens visible.

# Kpop Stan Vault v8.5.0-261111

## What's new

- **Notification history**: notices shown in the vault now stay in the notification panel after their popup closes. Open History directly from a popup, mark notices read or delete them, and revisit the latest 200 notices on this device. Upcoming dates, reminders and their existing controls remain available in their own view. Each signed-in account keeps its own history.
- **Clearer notification panel**: notices are grouped by day, unread notices stand out, and empty history explains what will be saved. The familiar Statistics-style tabs separate History and Upcoming dates. Clear history asks before removing saved notices.
- **Sort by listening score**: order your vault by the highest or lowest Last.fm percentage, alongside the existing total-scrobble sorts. Groups without listening data appear last.
- **Change one member's position**: in Edit Member, choose #1, #2 or another position in Manual Bias mode. Saving moves other members into place automatically and records affected members' rank changes. The information popup stays read-only.

## Changes

- **Shared affinity ranks**: groups with equal affinity share the same rank, such as #1, #1, #2. A small position label beneath affinity shows where an entry sits within the full rated list. Rank history uses the same shared ranking.
- **Longest stans in Stan Journey**: the longest-running stans and their next day-count milestone now live in the Timeline tab.
- **Simpler listening dates**: pick a listening day directly from the calendar, use a recent-day shortcut or choose a date range. Saved dates update automatically while Recent is open, including older history when needed, without a separate update button.
- **Listening at a glance**: calendar markers show days with saved scrobbles. Hover or focus a day for its exact count and see a summary for the month. Listening search stays beside Tracks, Albums and Recent on wider screens, and directly below them on phones.
- **Clearer vault controls**: affinity sorts say highest or lowest first, and the tier filter makes it clearer that it includes groups and soloists.

## Improved

- **Lighter everyday browsing**: showing and closing notices no longer refreshes the whole vault screen. Long listening histories merge with fewer repeated sorts, saved dates reuse their loaded archive, and unchanged history avoids unnecessary saves. Existing animations and glass effects are retained.
- **Smoother editor scrolling**: Add to Stan, profile editors and Edit Photo keep scrolling separate from the popup frame. Small photo previews reuse suitable thumbnails, and duplicate-photo checks share ongoing work, give scrolling time to respond and stop when their editor closes. Saved photos, crops, animations and transparency are preserved.
- **Simpler everyday navigation**: settings has direct shortcuts for Last.fm, your AI key, backups and notifications, with advanced tier rules tucked away. Search opens the section you need, including collapsed options. Last.fm keeps Tracks, Albums and Recent above its filters, and Connect Last.fm opens the right settings section directly. Adding a group opens its page without launching a second editor.
- **Clearer editing on phones**: optional profile links, matching controls and extra member facts can be expanded when needed. Closing an editor still checks for unsaved changes, including a changed manual position. The group back button says Vault on small screens. Existing animation and glass styling are preserved.
- **Compact group calendars**: the popup keeps a compact width and evenly sized day buttons, with a height limit for long event lists. Month, Schedule, Birthdays and Discography stay visible without a tab scrollbar.
- **Manual Bias history trend**: the member editor and statistics show movement from recorded manual position changes, separately from affinity.
- **More useful AI context**: profile requests read the saved group and member details, including the current draft, while keeping private keys and large photo files out of the request. Changes to a draft no longer reuse an earlier draft's review.

## Fixed

- **Misleading Gemini limit messages**: profile checks use directly read source text instead of relying on a Search feature unavailable on the free tier. A supported free model handles extraction when needed. Messages distinguish unavailable model access, temporary limits and daily project quotas, and users sharing a network no longer share the app's AI lookup allowance.
- **Former and hiatus members**: profile checks recognize former pre-debut members mentioned in introductions as well as members under status headings. Linked profiles fill missing birthdays, birth names, nationality and other confirmed personal facts, alongside separate departure and hiatus dates. Roles remain specific to the correct group. Missing former or hiatus members can be added through review; unspecified facts stay blank.
- **Now-playing waves**: the live listening indicator keeps animating when the app enters its idle state or lighter graphics mode, while continuing to respect the device's reduced-motion preference.

# Kpop Stan Vault v8.1.0-261108

V8.1.0 adds Spotify release imports, improves discography scanning and makes the calendar easier to use on mobile.

## What's new

- **Spotify in Add Release**: paste a Spotify album or track link to import its release details, cover and tracklist with Auto Extract. Save Manual also accepts Spotify links. Auto Extract uses your Spotify connection or the vault's configured Spotify access.

## Improved

- **Apple Music scanning stays available**: Scan Discography continues to scan Apple Music/iTunes. Spotify imports are added alongside it, and saved releases are kept when the catalog is refreshed.
- **Fresher discography scans**: recent Apple Music catalog results are reused for five minutes instead of twelve hours, so scans can pick up newer releases sooner. Simultaneous lookups share a request to reduce repeated work.
- **Lighter release imports**: repeated Spotify imports reuse recent results and share an ongoing check. Slow Spotify requests time out instead of waiting indefinitely.
- **Roomier mobile tabs**: Calendar and Stan Journey tabs have wider buttons and larger touch targets. Swipe across the tabs on narrow screens; selecting a tab brings it into view. Arrow keys, Home and End also move between tabs. Existing animations and transparency are preserved.

## Fixed

- **Recent releases showing “1Y ago”**: calendar releases now show days or completed months when they are less than a year old, with clearer labels such as “Yesterday” and “2 months ago.” Month ends and leap years are handled too.
- **Edits made during an import**: incoming release details merge with the current vault, keeping changes made while the import was running.

# Kpop Stan Vault v8.0.0-261106

V8.0.0 adds Stan Journey, a calendar on every group, and a calmer notification stack, and makes context menus fully block the page behind them.

## Changes

- **Clearer Stan Journey timeline**: uses the familiar Group and Member Statistics graph, with stan counts, Journey’s purple accent and a compact tooltip showing the month, new and ended stans, and the change from the previous month. Choose 1M, 3M, 6M, 1Y, 3Y or ALL, then hover, tap or use the arrow keys to inspect a month. A new Latest stan summary shows your most recently started group and opens its entry. Journey also uses Stan Vault’s standard fonts throughout.
- **Listening inside Discography 2.0**: one track list now shows song lengths, your Last.fm scrobbles and the last played date for each song and album when available in loaded history. Every release card also shows its all-time album scrobbles when a matching count is available. Album totals come from Last.fm’s album record, so plays on other releases are not added to them. Trailing EP and Single labels are matched to Last.fm’s plain album names while different editions remain separate.
- **Every saved-artist scrobble date**: Recent has a searchable listening-date selector and full dates and times in Manila time. **Gather all dates** reads your available Last.fm history and keeps only artists saved in your vault, including their aliases. Stop and resume without losing gathered dates. Album counts, song counts and gathered listening dates are included in Cloud Sync, linked JSON files and downloaded backups, with each Last.fm account kept separate. Later updates check new dates without gathering the whole history again.
- **Filter your listening dates**: choose a day from the calendar, browse a month, use Today or the last 7 or 30 days, or set your own start and end dates. Previous and next buttons skip between days with saved listens. The filter stays visible while you scroll, shows how many scrobbles match, and works alongside search. Dates use Manila time, and Clear brings back all loaded dates.
- **Interactive activity charts**: in Stan Journey, hover, tap or focus an hour or day to see exact play and edit counts. Click to keep a selection, or use the arrow keys to move between bars.
- **Calendar beside Delete**: open the group’s birthdays and release calendar directly from its detail header.
- **Your own group schedules**: add and edit broadcasts, concerts, fan meetings and other events with a date, optional time and notes. They appear on the group calendar and its Schedule tab, survive reloads and use Cloud Sync when connected. Birthday rows open the member’s information, and release rows open the corresponding Discography detail.
- **Stan Journey**: a new window in the Home toolbar with three tabs. **Activity** scores how active you are from your listening (hours, plays, and the time of day you listen) and your edits, with a 14-day strip and your current streak. **Timeline** shows the stans you started each year and a month-by-month line of how many stans you have. **For you** suggests what to do next from your own vault: favorites you have not played lately, ratings that have gone stale, day-count milestones and anniversaries coming up, comebacks, planned stans and incomplete entries.
- **Calendar on every group**: each group card has a calendar button (also in its right-click menu) showing that group's member birthdays, discography and debut day on a month grid, with a full birthday list and a release list.

## Improved

- **Better small-screen layouts**: group navigation stays centered, action buttons have room to fit, and Recent scrobbles place dates below the song details so long timestamps do not squeeze the title. Date controls have larger touch targets while keeping the existing glass and animation effects.
- **Less work on phones and desktops**: short listening previews read just the songs they need instead of sorting an artist’s entire saved history. Timeline pointer updates run at most once per display frame, and its labels stay readable as the chart resizes.
- **One scan for releases and listening**: every Scan Discography action checks your connected Last.fm album and song counts after updating the catalog, and gathers saved-artist listening dates for Recent. Expand the scan details to see each release, returned counts and why a match needs another check. Large tracklists are checked in smaller batches, repeated songs share checks, and Retry incomplete keeps finished counts without rescanning the catalog.
- **Roomier Last.fm statistics**: the main vault and shared snapshots have wider, scrollable tabs on smaller screens, with readable labels and larger touch targets. Selecting a tab brings it into view; keyboard navigation works too.
- **Faster large-vault browsing**: unchanged group filters reuse their results, and long top-song and album lists load only the rows near the screen. Gathered dates store repeated song details once to keep backups and syncing lighter.
- **Lighter large vaults**: listening activity, Stan Journey and discography search do less repeated work when you have many saved groups and releases. Missing album artwork loads as you approach it, and recent listening checks are reused to reduce waiting and repeated requests.
- **Faster browsing through long listening histories**: choosing another date avoids rereading the whole history, long scrobble lists show only the rows near the screen, and reopening Recent avoids loading the same saved archive again during your visit.
- **Consistent popup styling**: the group calendar and Stan Journey use Stan Vault’s existing adapted modal surfaces and sliding tabs. Existing animation timings and transparency effects are preserved.
- **Calmer notifications**: several notifications at once now stack as a compact deck, newest in front, instead of a tall column covering the screen. Hover, focus or tap the notification chip to spread them out; countdowns pause while spread out. Notifications slide smoothly when others arrive or leave, and **Clear all** dismisses the stack.

## Fixed

- **Mobile notification width**: single notifications, stacked messages and scan progress fit the phone’s width with even side margins and room for screen cutouts.
- **Clicking through context menus**: while a context menu is open, the page behind it can no longer be clicked. Closing it by clicking outside no longer lets the same click or tap reach a card underneath, and clicks inside the menu no longer open the card it came from.

# Kpop Stan Vault v7.5.1-261025

V7.5.1 makes subscribed push reminders more resilient, makes Gemini key checks clearer and more reliable, and refines listening statistics and everyday icons.

## Changes

- **First recorded listens**: the Scrobbles tab now shows your earliest saved listening total and its date under **First recorded**, replacing the lowest-total card. This appears in both your main vault and shared snapshots.
- **More consistent icons**: settings, filters, editors, empty lists, sharing controls and statistics use matching outline icons in place of decorative emoji. Country flags, music symbols and the familiar bias-tier colors remain.

## Improved

- **Push reminders stay connected**: already-subscribed devices check their connection when you return, come back online or renew your sign-in. Missing or expired subscriptions can reconnect without asking you to opt in again. Your own paused or removed-device choices are respected.
- **One Gemini key check**: verification checks your key directly with Google without waiting for an AI-generated reply. Temporary connection or service problems receive a short automatic retry and no longer label a valid key as failed.

## Fixed

- **Push switch appearing off**: a temporary connection or sign-in error no longer replaces your last confirmed notification choice with an off state.
- **Repeated key-verification taps**: repeated taps share one check, editing a key cancels the previous check, and a result for an old key cannot overwrite the new one. Successful verification remains visible until the key changes.

# Kpop Stan Vault V7.5.0-261022

V7.5.0 brings back your complete Last.fm listening timeline, keeps public snapshots in step with it, and makes Stan Vault lighter to open while keeping its animations and transparent look.

## Changes

- **Recover your whole Last.fm history**: Recover missing history now starts at your earliest available Last.fm scrobble, including listening from before Stan Vault added Last.fm. It rebuilds missing days through yesterday and keeps days you already saved.
- **Complete history on public snapshots**: shared Last.fm statistics and scrobble graphs keep every saved date instead of cutting off older listening after a fixed number of samples. Larger full-vault snapshots keep their Last.fm timeline too.
- **Older listening keeps its daily record**: recovered days remain available even after a year, so you can revisit the whole timeline.

## Improved

- **Quicker opening with Cloud Sync**: returning users can open this account's saved vault while the latest cloud changes are checked in the background. Independent checks run together, and unchanged groups take less work to check again.
- **Lighter first load**: large editors, discography, comparison and vault tools load when needed. Background preparation waits until your vault is ready instead of competing with startup.
- **Faster photo-heavy vaults**: photos begin loading as they approach the screen, small avatars use sharp thumbnail copies when suitable, and opening Home no longer reads every cached photo into memory. Unused thumbnail copies are released as you browse; your original photos and crops stay intact.
- **Smoother large lists**: Home starts with fewer offscreen cards, and scrolling reuses measured row sizes instead of measuring the whole visible grid on every movement.
- **More responsive history recovery**: reads your listening in pages instead of asking for every day separately, shows progress across the complete record, and lets the page respond while rebuilding a long timeline. Cancelling or an incomplete read leaves your saved history untouched.
- **Same look and motion**: existing animations, timing, colors, blur and transparency are preserved.

## Fixed

- **Album covers beside long titles**: covers stay at the top beside a title that wraps onto two lines, including on public snapshots.
- **Deleted entries returning after reopening**: a newer save stays newer even when you remove your most recently edited group or leave the vault empty. Closing or refreshing also saves an empty vault.
- **Snapshots missing recovered listening**: automatic snapshot updates now notice listening-history changes even when no group profile was edited. Existing links receive the complete saved timeline on their next update.

# Kpop Stan Vault v7.2.0-261020
 
V7.2.0 gives the group photo editor a fresh look, adds a proper date picker, makes calendar search show its results right on the calendar, fills the Stan tab with your whole stan story and makes popups easier to read and smoother on phones.

## Tracking Links


### Added
- **New date picker**: every date field (debut, stan date, planned date, disband and unstan dates, birthdays, leave and hiatus dates) now opens a calendar that matches Stan Vault instead of the plain browser one. Pick a month or year quickly, jump to Today, clear the date, or just type it in. It works with the keyboard and turns into a bottom sheet on phones.
- **Search results on the calendar**: type in the calendar search and press Enter to see every match on the calendar itself. A strip of months with results lets you jump between them, the arrows step to the next or previous month with results, and Clear brings back the normal view.
- **Notification preferences**: a new **Preferences** button in Notifications opens its own window where you choose which tab Notifications opens on (Last used, Today, Tomorrow, 7 Days or 30 Days), which category is selected and whether it shows unread only. Reset and Restore defaults use your choices.
- **All your stans in the shared Rank tab**: a shared group link now shows where that group stands among every group in your vault, for example #3 of 57, instead of only itself. Update an existing share link once to include it.
- **Discography on the Stan tab**: every release day of your groups now shows on the Stan tab and comes back each year as a release anniversary, with several releases on one day shown together.
- **Debut days on the Stan tab**: debut days and debut anniversaries now appear next to your stan dates, with their own shape on the calendar.

### Changed
- **Photo editor rework**: the Edit Group Logo window is redesigned with a larger preview showing exactly how the photo will look in the app, easy position buttons, zoom controls and quick zoom choices, and a simpler Upload or Image link switch.
- **Stan tab gathers everything**: the Stan tab now has All, Stan dates, Milestones, Debut and Discography views, showing stan dates, planned days, day-count milestones, debuts and releases in one place. Events no longer show in years before they could have happened.
- **Clearer tab labels on phones**: tabs inside popups now have bigger, easier to read labels with the icon above the text.
- **Same fonts everywhere**: the photo editor, date picker and Cloud Sync window now use the same fonts as the rest of Stan Vault, so titles, labels and buttons look consistent.
- **Planned to Stan icon**: the little emoji calendar on the Planned to Stan tile is replaced with a clean icon.
- **Faster and lighter**: popups use less drawing work on phones, the looping glow and pulse animations behind an open popup now pause on every screen size and resume when it closes, and the Cloud Sync window and calendar do less work behind the scenes.

### Fixed
- **Recent Changes shows other devices**: when another device pushes changes, this device now adds them to Recent Changes right away, marked as coming from another device and with what changed (for example the affinity or a member edited), instead of waiting for that device's own log. Recent Changes also shows when it was last fetched and has a new Other devices filter, and Cloud Sync's Last fetched has a See what changed link.
- **Preferences window on top**: the Notifications Preferences window now opens above Notifications instead of behind it.
- **Home board remembers your choice**: the Smart Upcoming Board keeps the range and category you picked after you refresh the page.
- **Right-click and long-press menus**: while a menu is open, the page behind it can no longer be clicked by accident. The first click or tap outside only closes the menu. The page behind no longer turns darker while a menu is open, and a menu no longer closes itself when the press that opened it is released.
- **Hover tips above Quick Peek**: the little hover tip on a group card (for example "Stanned since November") is no longer hidden behind the Quick Peek card of the group next to it. The tip now always shows on top.
- **Shared Stats match the app**: the Stats window on a shared link now reads history the same way the app does, so the graph, tier colors and numbers match.
- **Laggy Cloud Sync window on phones**: opening and switching tabs in Cloud Sync is now smooth, because the page behind it is paused while it is open and its heavy effects are lighter on phones.


# Kpop Stan Vault v7.1.1-261016
 
V7.1.1 fixes Wrapped so finished months show your scrobbles after Recover history, makes the Cloud Sync window smoother, makes Last fetched and Last synced honest, adds your settings to JSON backups and makes Free up photo space really delete.

## Tracking Links


### Added
- **Free up photo space**: in **Cloud Sync, Data** there is a new **Free up photo space** button that opens its own window with a **Scan unused photos** button, a progress bar and the space that can be freed. It finds old photo files in your cloud storage that no group uses any more and are over a week old, shows how much space they take, and deletes them only after you confirm. Your current photos, their small copies and any group you deleted are never touched.
- **Last fetched and Last synced**: the Cloud Sync window now shows two separate times. **Last fetched** is the last push to the database by any device, yours or another one, and says which one wrote it. **Last synced** is the last time this device really sent or received changes. Neither follows the moment you opened Stan Vault any more: the settings row that Stan Vault rewrites in the background (Last.fm samples, Wrapped results, the action log) is not counted as a push, checks that find nothing new change neither, and both times are still right when you reopen the app (Last synced is remembered, and Last fetched is read from the database with the device that wrote it worked out from the last push this device made). The Home status pill (**DB: Cloud Sync Active**) ends with **Fetched N min ago** and refreshes itself every 30 seconds.

### Changed
- **Smoother Cloud Sync window**: the window no longer re-draws itself every time something else on the page changes. While it is closed it is left alone completely, while it is open it only updates when something it shows changes (a group edit that does not change the counts no longer redraws it), and the "N min ago" labels refresh on their own small timer instead of re-drawing the whole window. The Backups tab loads its list once and reuses it for a minute instead of asking the cloud on every tab switch. Dates in backup and Recent Changes lists use one shared formatter, and each Recent Changes row no longer reads the device name from storage again. Nothing looks different.
- **Backups now include your settings**: every JSON backup (download, linked file, Copy Raw JSON) also contains your tier affinity rules, vault rules, bias control mode and Last.fm username. **Import & Replace** and **Restore backup** apply them. **Import & Merge** only fills in what this device has not set yet: missing tier rules are added, vault rules and bias mode are used only while this device still has the defaults, and the Last.fm username connects only if this device is not connected. Older backup files without settings import exactly as before. Recent Changes is still not included, because it is a 7 day log.
- **Free up photo space really deletes (issue #80)**: the count now comes from what storage confirms it deleted. If storage blocks the delete (a missing delete rule on the photo bucket), you now get a clear message instead of a false success. The window shows a loading orb while it scans or deletes, how much space was freed, and a note if some files could not be removed.

### Fixed
- **Wrapped reads finished months straight from Last.fm**: if the saved history could not give a finished month or year its scrobbles, Wrapped now asks Last.fm directly for the scrobbles of that exact calendar month or year (Last.fm keeps every scrobble with its time), counts the ones that belong to your groups and shows them, with a short loading note while it reads. The result is saved with that Wrapped result so it only has to be read once. No more empty Last.fm card after Recover history.
- **Wrapped shows scrobbles for finished months and years**: Wrapped used to show the listening card only for the current month or year, even after **Recover history**. A finished period now gets its card from your saved Last.fm history: the plays are the all-time total at the end of the period minus the total just before it, with the top artists and estimated hours. July 2026 has no sample before it (history starts on July 14), so it uses the rolling 1-month count and says so on the card. Top tracks are not available for finished periods, because the history keeps counts per artist only. The result is saved with the month's Wrapped result.


# Kpop Stan Vault v7.1.0-261014
 
V7.1.0 makes Home lighter when you have lots of photos, brings your missing Last.fm history back, saves your Wrapped results, tidies up old photo files, and fixes the calendar button on Android, slow popups and a cloud sync problem that could skip your latest change.


## Tracking Links

- [Issue #76 - Last FM statistics](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/76)
- [Issue #77 - Add to calendar doesnt do anything and understanding its functionality](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/77)
- [Issue #78 - Every popup is laggy](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/78)
- [Issue #79 - Improve the performance of the cloud sync](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/79)
- [Issue #80 - Consider remove old pictures in Database](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/80)

### Added
- **Small photo copies for avatars**: every photo gets an extra small copy (shorter side 256 px, WebP, usually around 10 KB) that is used only where the photo is drawn small: the Home group cards and their quick look, the right-click menus, Notifications, the calendar previews and the Stan board. It is only used where it looks exactly the same as the full photo on your screen (it is skipped on slots that would look softer, and on photos you zoomed in on). The group page, member profiles, covers, large previews, Snapshots, exports and backups always use the original photo.
- **Your photos are never changed**: the small copy is a separate extra file. The original is never edited, re-compressed or replaced, and your vault data, JSON backups and Supabase rows get no new fields, so nothing about saving, importing, merging or syncing is different.
- **Shared through Cloud Sync**: for photos stored in your cloud photo storage, the small copy is also saved as a tiny file right next to the photo. Another device that signs in downloads that file instead of making its own. Saving it happens quietly in the background after the photo is uploaded, never delays or blocks a sync, and if it cannot be saved nothing happens and the full photo is shown as before. Photos you already have get their small copy gradually while you use the app.
- **Built gradually and kept on each device**: small copies are made in the background while the app is idle, one at a time, and remembered on that device. Until a photo's small copy exists, the full photo is shown exactly like before. Copies that have not been used for 90 days are cleaned up automatically.
- **Recover missing Last.fm history (issue #76)**: in **Settings, Last.fm** there is a new **Recover history** button. Last.fm still has the time of every scrobble, so it rebuilds the statistics days that went missing since Last.fm launched in Stan Vault (July 14): each day's plays, all-time total, rank and listening score are worked out from your scrobble times and saved. Days you already have are never changed, nothing is saved if Last.fm does not answer for some days, and it takes a few minutes because it reads about a year of scrobbles (you can close Settings while it runs). The recovered days sync to your other devices and are included in backups.
- **Wrapped results are saved (synced and in JSON backups)**: the headline numbers of each Wrapped month and year (top bias, top group, climbers, new groups and members, and the Last.fm listening card) are saved as a small result. This month's and this year's results are saved quietly once a day, so a finished period keeps its listening card, which Last.fm can never give back later. Results sync through Cloud Sync, are included in every JSON backup, and are merged (never overwritten) when you import a backup or use another device.
- **Last fetched time in Home status (issue #79)**: the Home status pill now shows how many minutes ago your vault was last fetched from the cloud.

### Changed
- **Redesigned Cloud Sync window**: once you are signed in, the window is split into four tabs so nothing needs a long scroll. **Overview** has the sync status card (account, Last fetched, group and member counts), **Sync Now** and **Restore from cloud**, and Recent Changes. **Backups** lists your cloud snapshots with **Save backup to cloud** (the window now stays open after saving). **Data** has Download backup, Import & Merge, Import & Replace, the Excel and CSV exports, a list of what a backup file contains and **Free up photo space**. **Account** has Change password and Sign out. Signing in and the JSON File tab look as before. Sync, backups and imports work exactly as before.
- **Free up photo space moved out of Settings (issue #80)**: it is no longer in Settings, Cross-device sync. It now lives in Cloud Sync, Data and opens in a separate window, with the same rules as before: only unused files over a week old, deleted only after you confirm (tap the button twice), and your current photos, their small copies and any group you deleted are never touched.
- **Old photos are removed automatically (issue #80)**: when you replace a photo, the old file is now removed from your cloud storage a week later, once nothing in your vault or its cloud copy uses it. The week keeps an undo, a device that has not synced yet and a recent cloud backup safe.
- **Popups no longer re-draw while the page updates (issue #78)**: every popup was re-rendered each time anything on the page changed (a Last.fm refresh, a sync status change, a toast), which made Settings, Quick Tour, Cloud Sync, Stats, Wrapped and the others stutter while open. Their buttons now keep one fixed identity, so an open popup only updates when its own data changes.
- **Lighter sync settings (issue #79)**: your settings are saved to the cloud about a second after the last change instead of a fraction of a second, so a burst of edits is sent once, and the cloud copy of the Last.fm history keeps one point per day for anything older than three days, which keeps the synced settings small. Your own device keeps every point.

### Fixed
- **Last.fm history could be overwritten in the cloud**: a device that had lost part of its history used to send its smaller copy over the complete one. The cloud copy of the Last.fm history and the Wrapped results are now merged with what is already stored before saving, so nothing is lost from either side.
- **Your latest change could be skipped by Cloud Sync (issue #79)**: when an update from the cloud arrived at the same moment as one of your edits, the edit could be left unsaved until your next change. It is now always saved.
- **Add to calendar did nothing on Android (issue #77)**: the button only opened a link that iPhone and Mac understand. It now opens Google Calendar's add-by-link page on Android and Windows, and the Calendar app on iPhone and Mac, with extra **Google Calendar** and **Apple / Outlook** buttons, Android steps, and a plain explanation: the feed only adds all-day events and carries no reminders, so any alert comes from your calendar app's own notification settings. **Turn off feed** stops the link so subscribed calendars can no longer update; events they already added stay until you remove the calendar in your calendar app. Stan Vault's own push notifications are separate and are not affected.


# Kpop Stan Vault v7.0.3-261012
 
V7.0.3 brings your Last.fm history back to a place where it can no longer disappear, and keeps it forever from now on. AI auto-fill no longer asks you to pick a model: it uses one default model and quietly switches to other free ones when Google retires or limits it. The site also asks much less of your graphics card, the Notifications window has a Tomorrow tab, and the Last.fm Scrobbles tab is simpler.


## Tracking Links

- [Issue #76 - Last FM statistics](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/76)

### Added
- **Lighter graphics switch**: new in **Settings, General**. Turn it on for weaker graphics cards: it removes the glow behind the page, every background blur and the looping decorations. It looks a little flatter and uses far less GPU. It is saved on the device you turn it on.
- **Tomorrow tab in Notifications**: the Notifications window now has **Today, Tomorrow, 7 Days and 30 Days**. **Tomorrow** shows only what happens the next day, and works together with the category filters (Releases, Birthdays, Stan Anniv and so on).
- **Last.fm history is in your backups**: every backup (download, linked file) now also contains your saved Last.fm history. Restoring or importing a backup merges that history into what you already have, so nothing is replaced or removed. If you made a backup before the history went missing, import it and the old points come back (and sync to your other devices).

### Changed
- **AI auto-fill picks its own model**: the **Model** list is gone from Settings, AI. Stan Vault always starts with **gemini-3.7-flash** and, if Google has retired it, it is out of quota or it is briefly down, tries other free-tier Flash models one after another (3.6 Flash, 3.5 Flash, 3.5 Flash-Lite, 3.1 Flash-Lite) before showing an error. A model you picked in an older version is ignored, so a retired choice can never get stuck again. Your API key is unchanged.
- **Popups open and close like the Calendar**: Settings, Quick Tour, Cloud Sync, Share Full Vault, What's New and the other popups now behave like the Calendar, which was always the fast one. They used to freeze the whole page behind them in a way that made the browser re-lay out everything when they opened and again when they closed, and they made the page redraw itself several extra times around the animation. They now use a light scroll lock (as light as the Calendar's), the page redraws once less on open and once less on close, and their code is downloaded in the background before you first open them so the first open is not delayed either. The animation itself (same slide and fade, same timing) is unchanged.
- **Scrobbles tab is only about scrobbles**: the **Listening score** card, its graph and its Current / Peak / Lowest / Average cards were removed from the Last.fm **Scrobbles** tab (in the Last.fm window and on public Snapshots). The score is still on the **Statistics** and **Compare** tabs.
- **Smoother and lighter, with nothing visual changed**: no animation, color or transparency was touched. The Last.fm history is now cleaned once and remembered instead of being re-read for every group on every update, and the rank history in Compare and Scrobbles is worked out in one pass instead of one search per point, which matters now that history is never deleted. Backups no longer re-clean the history each time they are saved. The group page and the Last.fm windows are no longer part of the first download: they load in the background once Home is ready, so the first screen appears sooner and they still open instantly. The soft glow behind the page stops while any popup is open, and the small looping animations (Last.fm now-playing bars and ring, the cloud dot, the status dots) pause when the window is idle, not focused, or in a hidden tab.

### Fixed
- **Last.fm history was disappearing (issue #76)**: only the newest 365 saved points per group were kept, and every refresh (opening the Last.fm window, pull to refresh, coming back to the tab) added a point, so the limit was reached within days and everything older was thrown away, on this device and in the cloud copy. **Nothing is deleted any more.** The last 30 days keep every point, older days keep their last point of the day, and after a year each week keeps its last point, so no day ever drops out of the graph and the saved size stays small. Merging history between devices, the cloud and backups is always a union by time, and a full browser storage can no longer wipe the saved copy.
- **Direct AI calls used a retired model**: when the vault could not reach its own server and called Gemini directly, it still used the retired 2.5 model name. It now uses the same default and fallback models.


# Kpop Stan Vault v7.0.0-261010
 
V7.0.0 lets you sign in with a username and password instead of an email link, and share your whole list of stans as one public Full Vault snapshot. Saves now go to your cloud database straight away, and your public snapshot links keep themselves up to date. It also adds a cookie notice, a nicer loading screen for shared links, and fixes pill hints hiding behind Quick Peek. The Compare window can now compare two whole groups, with Last.fm listening side by side. The Smart Upcoming Board has a cleaner look and no longer blocks scrolling, the Calendar window gives its event list more room, and Auto Extract no longer adds a release you already have a second time. Home search now forgives typos and understands Korean and English spellings of the same name.


## Tracking Links

- [Issue #75 - Hover tooltip need improvements](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/75)
 
### Added
- **Search that forgives typos and speaks Korean and English**: the one search box on Home still looks across groups, members, releases, dates and notes (the scope picker is unchanged), and it now finds what you meant. A small typo is fine (**Jeongsaebe** finds Jeong Saebi, **newjeanz** finds NewJeans, **hani** finds Hanni), spaces never matter (**Jeongsaebi** finds Jeong Saebi and the other way round), and Korean and English names match each other (**정새비** finds Jeong Saebi, **jeongsaebi** finds 정새비). Short words and numbers stay exact, so searching **2024** or **IVE** does not pull in unrelated groups, and anything that matched before still matches the same way. Typo matching only kicks in when nothing matches exactly.
- **Sign in with a username and password**: the Cloud Sync window now has two tabs, **Email link** and **Username**. Pick a username and password, tap **Create account**, and you are signed in right away. No email is needed and nothing has to be confirmed. Next time just tap **Sign in**. Your vault syncs across devices exactly like it does with the email link. Tick **Remember me on this device** to stay signed in. While signed in, you can use **Change password** in the same window. Because there is no email, a forgotten password cannot be reset, so keep it somewhere safe. Your username is also what shows in the name of your share links.
- **Full Vault snapshot**: share your whole list of stans as one public, read-only link. Open **Settings, Cloud, Full Vault snapshot** and tap **Share Full Vault**. The public page looks and moves like your Home screen: the same group cards with their ranks, tiers, member faces and release chips, the same Active, Planned, Disbanded and Unstanned tabs, search (by group, member or release), sort, and a Grid or List switch. Tap any group to open it with the same view as a normal group Snapshot (members, discography, statistics and Last.fm), then go back to the list right where you left off.
- **Choose what the Full Vault shows**: pick which kinds of stans to include (Active, Planned, Disbanded, Unstanned) and which sections to show (cover photos, logos, group info, dates, members, member photos, discography, stats and Last.fm).
- **One link that stays the same**: **Update link** refreshes the snapshot but keeps the same link, **New link** replaces it (the old one stops working), and **Disable link** turns it off. A progress bar shows while a big vault is being saved, and the link is copied for you when it is ready.
- **Saves go to the cloud right away**: when you save a group, a member, a release, a rating or a tier, the change is now sent to your cloud database immediately instead of waiting in the background for several seconds. A refresh, a closed tab or another device opening the vault a moment later now sees your latest edit. Settings (like bias management and Recent Changes) are sent right away too. If two saves happen back to back, they are sent one after the other so the newest edit always wins, and if you are offline or the connection drops, the change is kept and retried on its own.
- **Smoother saving**: after a save reached the cloud, the app used to swap every saved group for its cloud copy and redraw the whole vault, which could make the page stutter, and could even undo an edit you made while the save was still uploading. It now only touches a group when a photo was just uploaded or another device's newer changes were merged in, so saving no longer makes the page lag. The snapshot refresh also waits for a quiet moment and only re-checks groups that actually changed.
- **Snapshots update themselves**: once you have a Full Vault link (or a link for a single group), it now refreshes by itself a few seconds after your changes reach the cloud. The link stays the same, it uses the same choices as your last **Update Link** (which stans and which sections are shown), and there are no extra popups. Open **Share Full Vault** to see when it last refreshed. There is a new **Auto-update snapshot** switch in that window if you would rather keep updating by hand. The public page now shows the date and time of the last update.
- **Cookie notice**: the first time you open Stan Vault (or a shared Snapshot link) a small notice explains that the app saves your vault, settings and sign-in in your browser. Choose **Accept** or **Essential only**. Both keep every feature working, and it only asks once per device.
- **Smoother saving**: Added lastfm scrobbles stats to both Main and Snapshot that displays your no. of scrobbles and score.
- **Calendar feed you can subscribe to**: tap the new **Subscribe** button at the top of the Calendar window to create your feed. Tap **Add to calendar** on a phone or Mac, or **Copy feed link** and paste it into Google Calendar (**Other calendars, From URL**). You get one calendar with every comeback, birthday, anniversary and milestone, and it keeps itself up to date on its own, with no more saving events one by one. It has its own link, separate from your Full Vault snapshot, and only holds names and dates (no photos or stats). You can refresh it, make a new link, or turn it off from the same place.
- **Compare two groups, with Last.fm**: the Compare window now has a **Members | Groups** switch. In **Groups** mode pick any two groups and see them side by side: average member affinity, vault rank, tier, releases saved, active members, years since debut, and average age at debut (with the youngest to oldest range). Each metric is a pair of bars and the leader is marked with a small arrow. Groups on the Manual Bias System keep their affinity % hidden, as everywhere else, and are compared by rank and tier instead.
- **Last.fm stats in Compare**: a new **Last.fm stats** card compares total scrobbles, the last 30 days, listening score and Last.fm rank for the two groups, with a trend graph of the listening score over time. It also shows in **Members** mode, using each member's group, so two members from different groups can be compared by how much their groups are being listened to.
- **More to compare for members**: the member table now also shows **Group debut** and **Age at debut**.
- **Album covers in the Discography list**: every release in a group's Discography now shows its album cover on the left. Releases without a cover show a small disc icon instead.
- **Speed limit check for developers**: a new automatic test now fails if the first screen's code, the main page file, the stylesheet or the built bundle grows past a set limit, so the speed work cannot quietly slip back. It also fails if a heavy window (Settings, Stats, Wrapped, Cloud Sync, the chart code and others) is accidentally made to load up front, if an animation library is added, or if a text box is wired to run its handler twice per keystroke. Nothing changes on screen.

### Changed
- **Faster to build, safer to change (behind the scenes)**: more of the big Home screen was moved out into its own files: the search index and matching, the idle-time vault repairs, the Back button and Escape key handling, the Vault Doctor scan, and the Pinned Stans and Vault Doctor right-click menus. Nothing looks or moves differently; it just makes the app quicker to build and edit, and lowers the chance of a start-up crash caused by something being used before it exists. New automatic tests cover the search.
- **Nicer loading screen for shared links**: opening a shared Snapshot now shows a clear loading card with a spinner, a short step-by-step status and soft placeholder cards, instead of a plain line of text.
- **No more "queued" messages**: the save popup used to say "saved locally" and "Cloud sync queued", which sounded like your change was still waiting. It now simply says the item was saved and that it is syncing to the cloud, and it disappears faster. In Cloud Sync, recent changes that are on their way show **Syncing** instead of **Queued**, and the Home status shows **Syncing to cloud** or **Pushing changes** while a save is being sent.
- **More of the group page follows the group's color**: the soft glow behind the page, the page scrollbar, the borders of the info cards, and the top bar of your phone or browser now pick up the group's color, and go back to normal when you leave the group.
- **"Saving…" then "Saved"**: saving a group, a member, a member list or a release now shows **Saving <name>…** right away, sends the change to the cloud without waiting for the editor to close, and then turns into **<name> saved · Synced to cloud** in the same notification. If you are offline it says it was saved on this device and will sync later.

- **Cleaner Smart Upcoming Board**: every card now has a colored side edge, a clear label for what it is (Birthday, Release, Stan anniversary, Debut anniversary and so on), a larger photo, and a small date block with the countdown under it. The cards are tidier rectangles instead of long pills, the arrows moved up next to a count of how many events are showing, and the edge of the row fades when there are more cards to scroll to.
- **Compare timeframe**: the Compare graphs use the same **12H, 1D, 3D, 7D, 1M, 3M, ALL** buttons as the group Member Compare window, instead of being fixed at 30 days.
- **Tomorrow filter**: the Smart Upcoming Board has a **Tomorrow** button between Today and This Week, and the Calendar window has the same quick filter (**All, Today, Tomorrow, This week**, each with a count) above its Upcoming list, so you can see only what is happening the next day.
- **Softer One UI 8.5 corners**: the event cards on the Smart Upcoming Board and the entries in the Calendar window now use larger, smoother rounded corners in the One UI 8.5 style, and the colored edge on the cards sits neatly inside the card instead of being cut by the corner.
- **More room for the list in the Calendar window**: on a computer the Calendar window is wider, with the month on the left and the event list on the right at full height, so you see many more events at once. On a phone the list keeps a comfortable height under a slightly tighter month grid. A thin line separates them, the heading (for example "On October 8" or "Upcoming · next 30 days") stays pinned while you scroll, and picking another day starts the list back at the top.
- **Safer syncing and name matching**: the rules that decide what happens when two devices changed the same thing (which side wins, deleted members, tier and rating history) and the rules that decide whether two names are the same group or member are now covered by automatic tests, so a future change cannot quietly break them and corrupt your vault. Nothing looks different; this is extra protection behind the scenes.
- **Fewer double renders**: the cover and logo buttons in the group editor were redrawn on every keystroke even though nothing about them changed, and eight text boxes (search, compare pickers, the label field) ran their handler twice for each key you typed. Both now happen once. Animations and visuals are untouched.
- **Duplicate code removed (behind the scenes)**: helpers that were copy-pasted into several files (text input reading, member status, the stats mobile check, Gemini text helpers, cloud table names, compare timeframes, Last.fm track roll-ups, the member photo opener and the in-group rank builder) now live in one place each. In the group editor, soloists now see "Soloist Logo" in the logo editor title in every path.

### Fixed
- **Home would not scroll while the pointer was over the Upcoming Board**: a normal mouse wheel over the board was being turned into sideways scrolling, so the page stopped moving. Scrolling up and down now always scrolls the page. To move the row sideways use the arrows, drag it, hold **Shift** while scrolling, or swipe sideways on a trackpad or touch screen.
- **Auto Extract no longer adds a release twice**: when Auto Extract (or **Save Manual**) finds a release that is already in the Discography, it now updates that release instead of adding a second copy. A release counts as the same one when the Apple Music link, the Apple release id, or the date and title match, including titles that only differ by Apple's " - Single" or " - EP" ending. The message afterwards says whether a release was added or updated.
- **Pill hints hidden by Quick Peek**: when the Quick Peek card was open, the little hint that appears when you hover a group pill (for example "Stanned since April 2025") could slide behind it. The hint now always shows on top.
- **Hover hints in Group and Member Statistics**: since the statistics windows were made a different size, the little hints that appear when you hover a card could get cut off at the edge of the window or be partly hidden. They now float above everything, wrap when they are long, and always stay fully on screen.
- **Cleaner hover cards on the statistics graphs**: the card that shows the date and value when you hover or touch the Statistics, Rank and Compare graphs is now one tidy card with normal-sized text. It stays inside the graph, moves to whichever side of the line has room, and no longer covers the dates along the bottom. In Compare it lists each member with their color, rank and percentage.
- **Holding an entry no longer starts text editing on phones**: when you hold a group, member, release, calendar entry or other row to open its quick menu, the phone no longer highlights the text or shows its Copy and Select all bar over the menu.
- **Stretched chart hover cards**: in the Rank, Statistics and Compare graphs, the hover card and the dot on the line were stretched sideways on wide windows. The graphs now draw at their real size, and the Rank hover card is a tidier, compact card showing the date, the tier, and your rank as "#3 / 6".

### Good to know
- A Full Vault snapshot is a saved copy of your vault. With **Auto-update snapshot** on it refreshes itself after your changes are saved to the cloud; you can still press **Update link** any time to refresh it right away. Someone who already has the page open sees the newest copy the next time they open or reload the link.
- Anyone with the link can see it, so only share it with people you trust. You can turn it off at any time.
- Your data format is unchanged, so older backups and other devices keep working.


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
