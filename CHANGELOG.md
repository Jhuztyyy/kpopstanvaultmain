# Changelog

All notable Kpop Stan Vault changes are tracked here. The repository code remains private; issue and release links are included for project tracking.

# Kpop Stan Vault V5.2.1-260919
 
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
