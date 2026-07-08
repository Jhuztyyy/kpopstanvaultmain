# Kpop Stan Vault

Kpop Stan Vault is a private personal K-pop vault project for organizing groups, members, bias tiers, affinity, statistics, discography, upcoming events, public snapshots, Spotify listening context, and vault backups in one clean dashboard.

The project focuses on a polished One UI-inspired interface, stable data preservation, smooth popups, reliable stats history, source-backed profile and release data, safe AI review, and safer multi-device sync behavior.

## Features

### Group And Member Vault

- Manage K-pop groups and members in one organized vault.
- Track member roles, status, birthdays, photos, notes, nationality, familiarity, and custom information.
- View group profiles with clean cards, pills, badges, media, descriptions, source links, and member lists.
- Search and filter members while preserving saved order, rank, and personal organization.
- Keep group/member data readable across desktop and mobile layouts.
- Save trusted group profile source links from KProfiles or KPopping for cleaner Group Info references.

### Bias And Affinity System

- Use the Manual Bias System for full control over tiers and personal order.
- Keep manual tier/order as user-controlled data.
- Use optional Affinity Assist for suggestions only.
- Track tiers such as Main Bias, Bias, Main Wrecker, Wrecker, Member, Former Bias, and Bias Candidate.
- Preserve bias choices, tier history, affinity history, and manual rankings during normal app updates.
- Keep affinity suggestions separate from manual tier control.

### Stan Statistics

- Track bias, tier, rank, and affinity history over time.
- Display visual stat changes for members and groups.
- Compare members and groups with chart-based statistics.
- Use cleaner timeframe chips and compact hover tooltips across group, member, compare-series, and compare-all chart surfaces.
- Preserve real saved stats history instead of creating fake samples or guessed tier movement.
- Keep Stats views read-only unless the user explicitly edits data elsewhere.

### Spotify Top Music And Listening Trends

- Connect Spotify to add read-only listening context for saved groups.
- Match saved groups using Spotify artist IDs, direct Spotify artist links, group names, aliases, Korean names, discography names, album names, and trusted profile source hints.
- Use Group Edit AI Mode to include an exact Spotify artist-link check when Spotify is connected.
- Save confirmed Spotify artist IDs per group for safer future refreshes.
- Review uncertain matches instead of silently linking the wrong artist.
- View Home Top Music for matched top tracks and derived top albums across saved groups.
- Search Top Music by track, album, group, artist, or saved album-track text.
- Use LM, 4W, 6M, and ALL ranges with clearer labels so Spotify recent-play windows and Spotify top-item windows are not confused.
- View per-group Spotify Statistics, Ranges, Top Music, and Source tabs.
- Use compact chart hover tooltips in Spotify Ranges so range points behave closer to the normal Spotify Statistics and Affinity Stats chart style.
- Save read-only Spotify listening snapshots for trend graphs without touching affinity, bias tier, manual order, ranking history, or Stats history.

#### Spotify Range Meaning

- LM uses Spotify recent-play data from the latest refresh and summarizes matched plays from the last month.
- 4W uses Spotify's short-term top-item window.
- 6M uses Spotify's medium-term top-item window.
- ALL uses Spotify's long-term top-item window.
- Top Music tracks come from matched Spotify top tracks, while Top Music albums are derived only from matched top tracks so albums are not guessed from unrelated artists.
- Spotify listening data is context-only and should never write into affinity, bias tiers, manual member order, ranking history, or vault Stats history.

### Discography 2.0 And Release Tracking

- Manage group discography and release information with Apple Music/iTunes-backed data.
- Track latest, previous, and upcoming releases.
- Open releases in an in-modal detail view with cover art, release metadata, source link, and tracklist details.
- Scan Apple Music/iTunes to enrich saved releases with exact collection IDs, track counts, artwork, tracklists, and release type.
- Use Manual Load Tracks as a fallback for older saved entries or one-off fixes.
- Compare track title/order signatures so same-count but wrong tracklists can be replaced safely.
- Save personal release ratings without changing source-backed release metadata.
- Show source-confirmed audio badges only for DOLBY ATMOS, HI-RES LOSSLESS, and LOSSLESS.
- Exclude Apple Digital Master from the visible audio badge path and avoid showing false audio flags.
- Use safety warnings for destructive release actions.

### Upcoming Board And Notifications

- View birthdays, releases, anniversaries, planned stan dates, status dates, and pre-debut events.
- Filter events by Today, This Week, and This Month.
- Group related notifications for a cleaner event view.
- Handle pre-debut groups separately from normal group anniversaries.
- Keep unstanned groups hidden from event surfaces where they should not appear.

### Public Share Snapshot

- Generate public read-only snapshots of selected group data.
- Keep snapshot pages visually consistent with the main vault.
- Show group profile, members, stats, compare views, and discography sections in view-only mode.
- Preserve visible profile source links and release source links where allowed.
- Hide editing tools, private controls, and unsafe actions from public pages.

### Vault Doctor And Health Tools

- Detect missing or incomplete group/member information.
- Find possible vault data issues and duplicate-looking fields.
- Help keep the vault clean without rewriting important history.
- Show warning-style checks instead of silently repairing personal data.

### Sync And Backup

- Support optional Cloud Sync and local JSON backup workflows in one unified Sync & Backup popup.
- Keep local changes protected until sync succeeds.
- Delay risky cloud pushes when the latest cloud copy cannot be compared safely.
- Clearly show when JSON mode is paused while Cloud Sync is active.
- Keep JSON restore disabled while Cloud Sync is signed in so local JSON restore does not fight cloud data.
- Support JSON link/reconnect/create/save/export/import/copy actions for browser-supported local file workflows.
- Track recent changes for multi-device visibility.

### Quick Tour

- Provide a searchable in-app Quick Tour for common workflows.
- Cover Home, group editing, AI review, members, Top Members, Spotify Top Music, Discography 2.0, affinity charts, Vault Statistics, Calendar, Media, Sync & Backup, Cloud Sync, Share Snapshots, Settings, and workflow tips.
- Keep the tour as user-facing guidance only, not as a private setup or implementation manual.

## Design Direction

Kpop Stan Vault follows a polished One UI-inspired design direction.

The interface focuses on rounded cards and popups, smooth modal animations, clean member and group layouts, color-adaptive UI elements, mobile-friendly scrolling, consistent styling across the vault and public snapshots, and clear visual hierarchy for stats, releases, Spotify listening context, sync tools, and events.

The design goal is to feel personal, organized, and expressive without turning the vault into a generic dashboard.

## AI Review Direction

AI features are used as review assistance, not as automatic ownership of saved data.

- AI Fill previews suggested fields before applying changes.
- Saved fields stay protected unless the user chooses to apply a reviewed correction.
- Profile facts should come from reliable profile sources.
- Unknown or weakly sourced fields should stay empty instead of being guessed.
- Generic source statements should not replace meaningful saved notes or descriptions.
- AI should help clean names, status, profile facts, profile source links, exact Spotify artist links, and source-backed release details without inventing private vault data.

## Privacy And Data Safety

Kpop Stan Vault stores important user-created data such as groups, members, bias tiers, affinity values, statistics history, snapshots, Spotify link context, and backups.

Development changes should avoid:

- Resetting stats history.
- Rewriting tier history.
- Deleting affinity data.
- Changing manual bias order unexpectedly.
- Overwriting local changes before sync succeeds.
- Modifying backups without user confirmation.
- Creating fake stats samples or fake tier history.
- Letting Spotify listening context change affinity, bias tiers, ranking history, or manual order.
- Exposing private implementation details.

Safe updates should be isolated, reversible, and tested carefully.

## Public Information Notice

This README intentionally does not include installation steps, setup commands, environment variables, database setup, API details, source code explanations, folder structure, private configuration, internal implementation logic, or deployment instructions.

The project source, setup process, database structure, and private configuration are intended to remain private.

## Project Status

Kpop Stan Vault v2.0-260709 is an actively improved personal vault project with ongoing focus on performance, mobile polish, snapshot stability, statistics reliability, sync safety, UI consistency, discography accuracy, Spotify listening-context clarity, AI review quality, and data preservation.

## Tech Stack

- Next.js
- React
- Supabase
- Vercel
- Google Gemini API
- Apple Music / iTunes release data
- Spotify Web API
- KProfiles and KPopping profile sources
- Lucide icons
- Custom One UI-inspired CSS

## Acknowledgements

Special thanks to [KProfiles.com](https://kprofiles.com/) for being a helpful public K-pop profile reference for group and member information.

Kpop Stan Vault is an independent personal vault project and is not affiliated with KProfiles, KPopping, Apple, Spotify, or any K-pop company.

## License

No public license has been specified.

All rights are reserved unless a license is added later.

## About

Kpop Stan Vault is built for fans who want a personal, visual, and organized way to track their K-pop groups, members, biases, releases, listening context, statistics, and stan journey.
