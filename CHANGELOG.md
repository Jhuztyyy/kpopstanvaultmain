# Changelog

All notable Kpop Stan Vault changes are tracked here. The repository code remains private; issue and release links are included for project tracking.


## V1.4-260701

Tracking links:

- [Issue #6 - Add overall member familiarity on group cards](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/6)
- [Issue #31 - Improve AI recognition for group and member info](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/31)
- [Repository](https://github.com/Jhuztyyy/kpopstanvaultmain)
- [Releases](https://github.com/Jhuztyyy/kpopstanvaultmain/releases)

### Added

- Added compact member familiarity summaries on home group cards using saved member familiarity values.
- Added group-card familiarity tooltips showing the average percentage and mastered-member count.
- Added updated Quick Tour guidance for AI Fill review, source-backed group/member matching, member Familiarity, discography filters, personal release ratings, Date Dashboard, Recent Changes, Cloud Sync, and app install support.

### Improved

- Improved the home group-card familiarity meter width so it lines up with the logo/content lane and affinity area instead of stretching across the whole card.
- Improved the home group-card familiarity placement so it stays near the release pill lane without crowding the affinity percentage or footer controls.
- Improved Discography type filters so Mini Album, EP, and Album releases use separate buckets and no longer inflate each other's counts.
- Improved release type badges so saved album-title fields display as Mini Album, EP, Single, or Album based on the actual release category.
- Improved member-list readability so long member names and tier labels wrap cleanly instead of cutting off with ellipses.
- Improved AI Fill review readability so long reviewed field values and source labels wrap instead of truncating.
- Improved Quick Tour search text so help topics are easier to find by Familiarity, discography rating, AI mode, backup, sync, PWA, and safety keywords.
- Improved KProfiles group-page parsing so member sections that are stored as headings/rows inside one group profile page can be recognized.
- Improved AI profile lookup for newer or niche groups where members do not have separate individual KProfiles pages.
- Improved group-page member merging so active lineup names from a verified group profile page are not missed when only some detailed member blocks are available.
- Improved direct KProfiles matching for popular/stylized group names such as BTS and IZ*ONE.
- Improved group entertainment detection from profile intro text such as "under MODHAUS" when no explicit agency field is present.
- Improved active/former/hiatus member-status parsing so former text must belong to the target group/member section before it can change a saved status.

### Fixed

- Fixed source-backed member lookup failing when the member exists inside the group profile page but not as a separate profile page.
- Fixed home group cards not showing the overall familiarity progress for their saved members.
- Fixed large KProfiles pages leaking sidebar/navigation names into group member counts.
- Fixed tripleS parsing returning too many members; the verified lineup now resolves to 24 current members.
- Fixed fact bullets being mistaken for member names on group profile pages.
- Fixed debut-date extraction using unrelated anniversary/reveal dates instead of a real debut sentence.
- Fixed active/former member-list names being clipped in compact two-column member cards.


## V1.3-260629

Tracking links:

- [Issue #21 - Autocorrect Members and Group in AI mode](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/21)
- [Issue #22 - AI gathers wrong information](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/22)
- [Issue #23 - Cloud Sync Improvements](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/23)
- [Issue #24 - Installable app support](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/24)
- [Issue #25 - Pre-debut handling in notifications board](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/25)
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
