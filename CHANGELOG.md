# Changelog

All notable Kpop Stan Vault changes are tracked here. The repository code remains private; issue and release links are included for project tracking.

# Kpop Stan Vault V3.0-260807

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

- AI Mode still detects disbanded Groups

## Fixed

- All Buttons, Loading Animation and Mobile UI inconistencies has been fixed
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
