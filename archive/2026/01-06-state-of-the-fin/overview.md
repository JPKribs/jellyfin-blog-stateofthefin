## Introduction

Happy New Year and welcome to the State of the Fin!
This new blog series will regularly basis highlight the ongoing development of Jellyfin and our official clients.
We aim to keep our community informed and engaged, so feel free to share your feedback or thoughts on our progress!

## Project Updates

### Jellyfin Turns 7

December marked Jellyfin's 7th anniversary!
A lot has changed in 7 years, but we remain steadfast in our commitment to Open Source and to being the best personal media server out there.
Special thanks to our developers, testers, moderators, and supporters for your invaluable contributions!
Here's to many more years of collaboration and streaming!

### Versioning

We received a substantial amount of feedback regarding our versioning scheme following the 10.11 release, particularly concerning the stability of what are perceived as 'minor' version updates.
This has prompted internal discussions about potentially revising our versioning scheme in the next major release.
While nothing has been finalized yet, we are considering 'dropping' the major version 10, which would make the next release 12.0.
Stay tuned for further updates as we navigate this feedback!

## Development Updates

### 10.11 Release Status

Jellyfin 10.11 introduced a major [EF Core refactor](https://jellyfin.org/posts/efcore-refactoring-incoming/), consolidating the legacy `library.db` into a single unified `jellyfin.db`.
Following more than six months of development and an additional six months of release candidate testing, version [10.11.0](https://jellyfin.org/posts/jellyfin-release-10.11.0/) was released last year.
This extended testing period allowed us to mitigate most [refactoring](https://github.com/jellyfin/jellyfin/issues/13047) and [RC](https://github.com/jellyfin/jellyfin/issues/14350)-related issues prior to release.

Even with this level of testing, issues were expected given the scale of the database change and the limited number of users reporting bugs.
These issues are currently being tracked on GitHub across three categories:

1. [General bugs](https://github.com/jellyfin/jellyfin/issues/15045)
2. [Performance bugs](https://github.com/jellyfin/jellyfin/issues/15685)
3. [Migration and database bugs](https://github.com/jellyfin/jellyfin/issues/15686)

We have been moving quickly to address these issues, delivering four additional point releases with over [100 changes](https://github.com/jellyfin/jellyfin/compare/v10.11.0...v10.11.5) since the initial 10.11.0 release.
To date, most point releases have focused on resolving general and migration-related issues.
The remaining migration issues are largely isolated, one-off cases and are unlikely to be resolved.
Most general issues have already been fixed, and the next bug-fix release is expected to include additional fixes for music metadata display issues and for watched status not being preserved when media is replaced or renamed.

We are continuing to investigate ways to mitigate performance issues caused by client-side enumeration and filtering of large datasets.

### Jellyfin Web vNext (aka 10.12 / 12.0)

- **Default 'Experimental' Layout**: The 'Experimental' layout is now enabled by default for all non-TV devices, introducing a new navigation layout and updated UI components.
- **Theming Support Overhaul**: We are improving theming support by enabling easier runtime customization of default themes through CSS variables and simplifying the process for creating new bundled themes.
- **Community Acknowledgment**: Huge thanks to those reviewing, testing, and providing feedback on web pull requests. Your contributions are immensely helpful, as the review burden largely falls on me alone!

\- [thornbill](https://github.com/thornbill)

## Sign Off

Wishing you all happy streaming in 2026 and beyond!
We look forward to another year filled with exciting updates and features for Jellyfin.

\- thornbill and the Jellyfin Team
