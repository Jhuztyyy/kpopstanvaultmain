# Changelog

All notable Kpop Stan Vault changes are tracked here. The repository code remains private; issue and release links are included for project tracking.

## V1.3-260629

Tracking links:

- [Issue #21 - Autocorrect Members and Group in AI mode](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/21)
- [Issue #22 - AI gathers wrong information](https://github.com/Jhuztyyy/kpopstanvaultmain/issues/22)
- [Repository](https://github.com/Jhuztyyy/kpopstanvaultmain)
- [Releases](https://github.com/Jhuztyyy/kpopstanvaultmain/releases)

### Added

- Added source-backed AI review support for member name corrections.
- Added AI member schema fields for official `name` and `stageName`.
- Added support for extracting member data from KProfiles group profile pages when individual member pages do not exist.
- Added direct source URL propagation into AI review suggestions.
- Added private-code-safe README and changelog documentation.
- Added installable app support through the Next.js app manifest and a no-cache service worker.
- Added pre-debut notification handling so future debut dates show as debuting events instead of anniversaries.

### Improved

- Strengthened AI Fill source policy for Member Info and Group Info.
- Preferred KProfiles first, then KPopping, for profile facts.
- Improved member matching so safe casing/spelling/stylization corrections can be reviewed instead of blocked.
- Improved newer/niche group support where KProfiles stores all members inside one group profile page.
- Improved AI prompts so official member names come from profile headers/member rows.
- Improved issue-linked release documentation for GitHub tracking.
- Improved cloud sync conflict protection so stale device saves reconcile with newer cloud rows before upload.

### Fixed

- Fixed `AI could not confidently match this member` for source-backed group-profile member rows.
- Fixed styled-name corrections such as `ME:U` resolving to the official KProfiles spelling `Meu` when the group page confirms the member.
- Fixed typo-like member lookups such as `Hyeren` resolving to official `Hyerin` when KProfiles confirms the group/member.
- Fixed profile-source handling so Kpop Fandom is not used as an automatic Member Info/Profile source.
- Fixed wrong-info risk for birthdays, roles, height, weight, blood type, MBTI, and nationality by keeping uncertain fields empty.
- Fixed notification board labeling for pre-debut groups with future debut dates.
- Fixed stale-device cloud pushes that could revert newer profile/member info after an affinity-only edit.

### Protected

- Existing saved fields still require review before being changed.
- Stats history was not touched.
- Tier history was not touched.
- Affinity history was not touched.
- Manual bias order was not touched.
- Route changes were limited to profile-source accuracy and matching.
- Existing stats/tier/affinity history was preserved.

### Validation

- Production build passed with `npm.cmd run build`.
- Verified KProfiles direct lookup for a member listed on a group profile page.
- Verified source-backed member-name correction path using the local API route.

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
