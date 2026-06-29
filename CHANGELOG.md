# Changelog

All notable Kpop Stan Vault changes are tracked here. The repository code remains private; issue and release links are included for project tracking.

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
