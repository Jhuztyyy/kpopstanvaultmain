# Kpop Stan Vault

Kpop Stan Vault is a private personal K-pop vault project for organizing groups, members, bias tiers, affinity, statistics, discography, upcoming events, public snapshots, and vault backups in one clean dashboard.

The project focuses on a polished One UI-inspired interface, stable data preservation, smooth popups, reliable stats history, safe AI review, and safer multi-device sync behavior.

## Features

### Group And Member Vault

- Manage K-pop groups and members in one organized vault.
- Track member roles, status, birthdays, photos, notes, nationality, and custom information.
- View group profiles with clean cards, pills, badges, media, descriptions, and member lists.
- Search and filter members while preserving saved order, rank, and personal organization.
- Keep group/member data readable across desktop and mobile layouts.

### Bias And Affinity System

- Use the Manual Bias System for full control over tiers and personal order.
- Keep manual tier/order as user-controlled data.
- Use optional Affinity Assist for suggestions only.
- Track tiers such as Main Bias, Bias, Main Wrecker, Wrecker, Member, Former Bias, and Bias Candidate.
- Preserve bias choices, tier history, affinity history, and manual rankings during normal app updates.

### Vault Statistics

- Track bias, tier, rank, and affinity history over time.
- Display visual stat changes for members and groups.
- Compare members and groups with chart-based statistics.
- Preserve real saved stats history instead of creating fake samples or guessed tier movement.
- Keep Stats views read-only unless the user explicitly edits data elsewhere.

### Discography And Release Tracking

- Manage group discography and release information.
- Track latest and upcoming releases.
- Save manual release entries and verified source links.
- Review release details before applying updates.
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
- Hide editing tools, private controls, and unsafe actions from public pages.

### Vault Doctor And Health Tools

- Detect missing or incomplete group/member information.
- Find possible vault data issues and duplicate-looking fields.
- Help keep the vault clean without rewriting important history.
- Show warning-style checks instead of silently repairing personal data.

### Cloud Sync And Backups

- Support optional cloud sync and local backup workflows.
- Keep local changes protected until sync succeeds.
- Delay risky cloud pushes when the latest cloud copy cannot be compared safely.
- Support safer backup and restore flows.
- Track recent changes for multi-device visibility.

## Design Direction

Kpop Stan Vault follows a polished One UI-inspired design direction.

The interface focuses on rounded cards and popups, smooth modal animations, clean member and group layouts, color-adaptive UI elements, mobile-friendly scrolling, consistent styling across the vault and public snapshots, and clear visual hierarchy for stats, releases, and events.

The design goal is to feel personal, organized, and expressive without turning the vault into a generic dashboard.

## AI Review Direction

AI features are used as review assistance, not as automatic ownership of saved data.

- AI Fill previews suggested fields before applying changes.
- Saved fields stay protected unless the user chooses to apply a reviewed correction.
- Profile facts should come from reliable profile sources.
- Unknown or weakly sourced fields should stay empty instead of being guessed.
- Generic source statements should not replace meaningful saved notes or descriptions.
- AI should help clean names, status, profile facts, and source-backed details without inventing private vault data.

## Privacy And Data Safety

Kpop Stan Vault stores important user-created data such as groups, members, bias tiers, affinity values, statistics history, snapshots, and backups.

Development changes should avoid:

- Resetting stats history.
- Rewriting tier history.
- Deleting affinity data.
- Changing manual bias order unexpectedly.
- Overwriting local changes before sync succeeds.
- Modifying backups without user confirmation.
- Creating fake stats samples or fake tier history.
- Exposing private implementation details.

Safe updates should be isolated, reversible, and tested carefully.

## Public Information Notice

This README intentionally does not include installation steps, setup commands, environment variables, database setup, API details, source code explanations, folder structure, private configuration, internal implementation logic, or deployment instructions.

The project source, setup process, database structure, and private configuration are intended to remain private.

## Project Status

Kpop Stan Vault is an actively improved personal vault project with ongoing focus on performance, mobile polish, snapshot stability, statistics reliability, sync safety, UI consistency, discography accuracy, AI review quality, and data preservation.

## Sourcing

K-pop Members and Group infomation are sourced from KProfiles.com. 

## Tech Stack

- Next.js
- React
- Supabase
- Vercel
- Google Gemini API
- Apple Music / iTunes release data
- KProfiles profile sources
- Lucide icons
- Custom One UI-inspired CSS

## License

No public license has been specified.

All rights are reserved unless a license is added later.

## About

Kpop Stan Vault is built for fans who want a personal, visual, and organized way to track their K-pop groups, members, biases, releases, statistics, and stan journey.
