# Changelog

All notable Kpop Stan Vault changes are tracked here. The repository code remains private; issue and release links are included for project tracking.

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
- Improved active/former/hiatus member status accuracy by requiring member-section or target-group evidence.

## Fixed

- Fixed source-backed AI lookup missing members that are present inside their group profile page.
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
