# NewJams ♡

### A Modern Music Experience Inspired by NewJeans

**An independently developed, cross-platform music application combining modern web technologies, personalized listening features, and a nostalgic Y2K-inspired interface.**

**[Launch NewJams](https://newjams.pages.dev/)** · **[Download Desktop App](https://newjams.pages.dev/)** · **[Developer GitHub](https://github.com/Unknown-George)**

🌐 **Website:** https://newjams.pages.dev/  
💻 **Platforms:** Web · Windows · macOS  
🎀 **Current Release:** v1.0.4  
🔒 **Source Code:** Privately maintained

---

## Overview

**NewJams** is an independently developed music application inspired by the music and visual identity of NewJeans.

Originally conceived as a web-based music player, the project has evolved into a cross-platform application supporting modern web browsers, Windows computers, and macOS devices.

NewJams brings together music discovery, official music videos, dance practice content, personalized playlists, account management, and listening-related features within a unified interface.

The application combines a React-based frontend, Supabase backend services, Electron desktop integration, and Cloudflare infrastructure to provide a consistent experience across supported platforms.

Beyond its visual design, NewJams represents a practical software engineering project involving frontend development, authentication, cloud infrastructure, desktop application packaging, release automation, software distribution, and secure version management.

**NewJams is an independent, unofficial fan-developed application and is not affiliated with NewJeans or its associated organizations.**

---

## 🌐 Access NewJams

### Web Application

**Official Website:** https://newjams.pages.dev/

**[Launch NewJams in Your Browser](https://newjams.pages.dev/)**

The web application runs directly in a compatible browser without requiring installation or development software.

Users can access the music player, browse available media, manage playlists, and use supported account features through the hosted application.

### Desktop Application

NewJams is also available as a standalone desktop application.

| Platform | Supported Architecture | Distribution |
|---|---|---|
| Windows | x64 | `.exe` installer |
| macOS | Apple Silicon (ARM64) | `.dmg` installer |
| macOS | Intel (x64) | `.dmg` installer |

**[Download NewJams for Windows or macOS](https://newjams.pages.dev/)**

The desktop applications are packaged using Electron, allowing the React-based interface to run as an installed application.

Desktop-specific functionality includes application startup handling, platform-aware navigation, update checks, and installer-based software updates.

**Installation note:** Current desktop releases are unsigned and not notarized. Windows SmartScreen or macOS Gatekeeper may display a security warning during installation.

---

## ✨ Features

### Music Library and Discovery

NewJams provides a centralized interface for exploring music associated with NewJeans.

- Browse an organized collection of music releases.
- Discover available songs and related media.
- Navigate between music content and playback interfaces.
- Access supported tracks through integrated media services.
- Use search functionality to locate available music content.

The music library is designed to make navigation straightforward while maintaining a consistent visual presentation.

### Integrated Music Player

The application includes a custom listening interface designed around the NewJams visual identity.

Supported functionality includes:

- Track selection and playback controls.
- Play and pause functionality.
- Navigation between available songs.
- Media playback state management.
- Integration with supported YouTube playback functionality.
- Playback-related error handling.

The desktop player includes platform-specific handling for YouTube's embedded player requirements.

When a video cannot be embedded because of restrictions established by its owner, NewJams can provide an option to open that content directly on YouTube.

Media availability and playback permissions remain controlled by the respective content providers.

### Official Music Videos and Dance Practice

NewJams organizes supported video content into dedicated areas.

**Music Videos**
- Access official music video content through supported YouTube embeds.
- Browse available videos within the application.
- Open restricted content on YouTube when necessary.

**Dance Practice**
- Explore available dance practice videos.
- Navigate dance-related content separately from the primary music library.
- Use the integrated video player where embedding is permitted.

NewJams does not independently host or redistribute copyrighted music recordings or video files.

### Personalized Playlists

Users can organize their listening experience through personal playlists.

- Create custom playlists.
- Add songs to saved collections.
- Remove songs from playlists.
- Organize personal music selections.
- Access supported saved content through their account.

Playlist functionality is integrated with the application's account and data-management architecture.

### User Accounts and Profiles

NewJams uses **Supabase Authentication** to support account-based functionality.

Features include:

- Email and password authentication.
- Personalized user profiles.
- Profile information management.
- Avatar customization.
- Account-specific settings.
- Persistent preferences and supported saved content.

The application integrates frontend account interfaces with managed backend services, allowing users to maintain a more personalized experience.

### Listening Activity and Analytics

NewJams includes listening-related functionality intended to provide insight into individual music activity.

Supported features include:

- Accumulated listening time.
- Frequently played songs.
- Individual listening activity.
- Personalized listening information.

These features are part of the application's evolving account and music experience.

### Interface and Personalization

The NewJams interface combines contemporary music application design with visual influences from Y2K aesthetics.

Design priorities include:

- A consistent visual identity across platforms.
- Dark mode enabled by default.
- An optional light theme.
- Saved theme preferences.
- Responsive web layouts.
- Reusable interface components.
- Clear navigation and playback controls.
- Desktop-specific interface adjustments.

Theme preferences can be retained through account settings, providing a consistent personalized experience.

---

## 🛠 Technology Stack

NewJams uses a combination of frontend technologies, desktop application tooling, managed backend services, and cloud infrastructure.

| Category | Technology | Purpose |
|---|---|---|
| Frontend | React | Component-based user interface |
| Programming | JavaScript | Application logic and interactivity |
| Styling | CSS | Layout, themes, and visual presentation |
| Build Tool | Vite | Frontend development and production builds |
| Desktop Framework | Electron | Windows and macOS desktop applications |
| Desktop Packaging | Electron Builder | Installer creation and release packaging |
| Authentication | Supabase Auth | Account registration and sign-in |
| Backend Services | Supabase | Account-related services and application data |
| Database | PostgreSQL | Persistent data through Supabase |
| Media Integration | YouTube Embedded Player | Supported music and video playback |
| Web Hosting | Cloudflare Pages | Production website deployment |
| File Distribution | Cloudflare R2 | Public desktop installer hosting |
| Source Control | Git and GitHub | Private repositories and version history |
| CI/CD | GitHub Actions | Automated builds, validation, and releases |
| Update Security | Ed25519 and SHA-256 | Signed update policies and file integrity verification |

---

## 🏗 Application Architecture

NewJams is structured around a shared frontend, managed backend services, platform-specific desktop functionality, and independently hosted release infrastructure.

### 1. React Frontend

The primary application interface is developed with React and JavaScript.

The frontend manages the interactive user experience, including navigation, music browsing, playback controls, playlists, profiles, settings, and media presentation.

Reusable components help maintain a consistent interface between the browser application and desktop versions.

Vite supports local development and optimized production builds.

### 2. Authentication and Data Persistence

Supabase provides the application's authentication and managed backend infrastructure.

The frontend communicates with Supabase services to support user authentication, profile information, account preferences, and supported saved content.

PostgreSQL provides the underlying relational database platform.

This separation allows the user interface and persistent account data to be maintained independently.

### 3. Media Playback Integration

NewJams integrates supported third-party media using YouTube's embedded player.

The application manages playback-related interactions while respecting the availability and embedding permissions of the original content.

Desktop integration required additional handling because Electron applications can use a custom application origin rather than a conventional website origin.

The desktop implementation was updated to provide the appropriate client identity and referrer information required for supported YouTube embedding.

NewJams also includes playback error handling for content that cannot be embedded.

### 4. Electron Desktop Applications

The desktop versions use Electron to package the web application into installable software.

The desktop architecture includes:

- Application window management.
- Secure application-origin handling.
- Platform-specific startup behavior.
- Desktop-specific navigation.
- Windows and macOS packaging.
- Application version detection.
- Update policy verification.
- Installer download and verification.

The application is distributed separately for Windows x64, macOS Apple Silicon, and macOS Intel.

### 5. Cloudflare Hosting and Distribution

NewJams separates website hosting from downloadable software distribution.

**Cloudflare Pages** hosts the production web application at:

https://newjams.pages.dev/

**Cloudflare R2** stores publicly downloadable desktop installers and update-related release files.

This arrangement allows users to access the website and download installation packages without accessing the private source repositories.

The public website provides platform-specific download options while the underlying development repositories remain private.

### 6. GitHub Actions and Release Automation

NewJams uses GitHub Actions to automate important build and release processes.

The workflow supports:

- Production frontend builds.
- Automated test execution.
- Windows application packaging.
- Apple Silicon macOS packaging.
- Intel macOS packaging.
- Packaged application launch checks.
- Update-interface validation.
- Installer artifact generation.
- Release publishing and distribution.
- Installer integrity verification.
- Website download-link updates.

Release validation helps reduce the risk of publishing incomplete or broken installation packages.

---

## 🔄 Software Version Management and Updates

Beginning with **NewJams v1.0.4**, the desktop application includes a version-management system designed to support reliable future updates.

### Startup Version Checks

When a supported desktop application launches, it checks a remotely hosted update policy.

The policy can identify:

- The latest available application version.
- The minimum supported version.
- Whether an update is optional or mandatory.
- The appropriate installer for the user's platform.
- Information needed to verify downloaded installation packages.

### Optional Updates

When a newer version is available but the installed version remains supported, the application can offer an update without preventing continued use.

### Mandatory Updates

When the installed version is below the minimum supported version, NewJams displays a required-update interface before allowing access to the main application.

Users are given two primary choices:

- **Update NewJams**
- **Quit Application**

This helps prevent outdated application versions from continuing to operate when a newer release is required.

### Secure Update Verification

The update system includes multiple integrity protections.

- **Ed25519 digital signatures** are used to verify the update policy.
- **SHA-256 hashes** are used to verify downloaded installer files.
- Installer selection is based on the supported operating system and architecture.
- Invalid update information is rejected rather than trusted automatically.

For the current unsigned desktop distribution, NewJams downloads and verifies the appropriate installer before opening it for installation.

Fully automatic in-place application replacement is not enabled in v1.0.4.

### Update Reliability

The update experience also accounts for operational failures.

If the update policy service is temporarily unavailable, the application can allow continued access rather than permanently blocking the user.

Failed downloads can be retried.

**Compatibility note:** Versions earlier than v1.0.4 do not include this startup update system. Users of those versions must manually install an update-enabled release before receiving future in-app update notifications.

---

## 🔐 Security and Source Code Management

NewJams is developed using privately maintained GitHub repositories.

The project separates its development resources from publicly accessible application files.

### Private Development Repositories

The original source code, internal development files, and release automation configurations are not publicly distributed through an open-source repository.

### Public Distribution

Users can access:

- The hosted web application.
- Windows and macOS installers.
- Public files necessary for software distribution and update checks.

Public access to the application does not provide access to the private GitHub repositories.

However, distributed browser and Electron applications necessarily contain client-side code that can be inspected. Private repositories protect the original development environment and non-distributed resources, not every aspect of compiled or bundled client-side software.

### Release Security

The release process uses private GitHub Actions secrets for sensitive publishing and signing credentials.

The update system uses signed policy information and file-integrity verification to help prevent unauthorized or corrupted update packages from being accepted.

---

## 🧪 Testing and Quality Assurance

NewJams development includes automated testing and packaged-application verification.

For **v1.0.4**, the release process reported:

- 20 passing automated tests.
- A successful production frontend build.
- Successful Windows x64 build and installation checks.
- Successful macOS Apple Silicon build and launch checks.
- Successful macOS Intel build and launch checks.
- Verification of mandatory and optional update screens.
- Successful full-file SHA-256 verification of the three published installers.
- Successful release and website deployment workflows.

These checks validate important parts of the release process.

They do not establish that every feature has been tested under every real-world account, device, or network condition. In particular, a complete upgrade using an existing signed-in user's data was not verified during the v1.0.4 release.

---

## 📦 Releases and Distribution

### Current Release — v1.0.4

**[Download the Latest Version](https://newjams.pages.dev/)**

The official website provides the latest supported installers.

| Platform | Installer |
|---|---|
| Windows x64 | [Download `.exe`](https://pub-f37b1abf363249fc941a05f7c78de0d7.r2.dev/v1.0.4/NewJams-Setup-1.0.4-x64.exe) |
| macOS Apple Silicon | [Download `.dmg`](https://pub-f37b1abf363249fc941a05f7c78de0d7.r2.dev/v1.0.4/NewJams-1.0.4-mac-arm64.dmg) |
| macOS Intel | [Download `.dmg`](https://pub-f37b1abf363249fc941a05f7c78de0d7.r2.dev/v1.0.4/NewJams-1.0.4-mac-x64.dmg) |

Desktop releases are distributed through Cloudflare R2 rather than public source-code repositories.

### Release History

| Version | Development Milestone |
|---|---|
| v1.0.2 | Earlier desktop distribution and packaging improvements |
| v1.0.3 | Desktop playback integration fixes, default dark mode, and platform-specific interface changes |
| v1.0.4 | Signed update policies, version checks, mandatory and optional update interfaces, and verified installer-based updates |

---

## 🎯 Project Objectives

NewJams was developed to explore and apply practical software engineering concepts through a complete user-facing application.

The project's main objectives include:

1. **Frontend Engineering** — Build a responsive, component-based application with reusable UI elements and consistent navigation.
2. **Full-Stack Integration** — Connect frontend functionality to authentication, persistent data, and managed backend services.
3. **Cross-Platform Development** — Adapt a shared web application into native desktop installation packages for Windows and macOS.
4. **Cloud Infrastructure** — Deploy the website and distribute downloadable software using independent cloud services.
5. **Software Release Engineering** — Automate builds, testing, packaging, verification, and release publication.
6. **Application Security** — Protect development resources and verify software update information and installer integrity.
7. **User Experience** — Create an accessible, visually distinctive application with personalization and intuitive media controls.

The project demonstrates experience extending beyond interface development into application architecture, distribution, and maintenance.

---

## 🚀 Future Development

NewJams remains an actively maintained personal project.

Potential improvements include:

- Expanded listening analytics and user statistics.
- Additional playlist organization features.
- Improved music discovery and search.
- More profile customization options.
- Accessibility and performance improvements.
- Continued refinement of desktop media playback.
- Improved update installation workflows.
- Platform signing and notarization for smoother desktop installation.
- Additional automated integration and end-to-end testing.

Future functionality is subject to development priorities and technical feasibility.

---

## 👨‍💻 Developer

**George Paraskevopoulos**  
Independent Software Developer

**GitHub:** https://github.com/Unknown-George  
**Project:** https://newjams.pages.dev/

NewJams was independently developed as a personal software engineering project.

The project demonstrates practical work across React frontend development, backend integration, authentication, desktop application packaging, cloud deployment, CI/CD automation, software distribution, and secure update management.

It reflects an interest in building software that combines technical functionality with a distinctive, user-focused design.

---

## Copyright and Intellectual Property

**Copyright © 2026 George Paraskevopoulos. All rights reserved.**

Original project code, independently created interface designs, and proprietary project assets remain the intellectual property of their respective owners.

No general permission to reproduce, modify, redistribute, or commercially exploit proprietary NewJams materials is granted through public access to the application.

Third-party libraries and dependencies remain subject to their respective licenses.

Music, video content, trademarks, logos, artwork, and other third-party materials remain the property of their respective rights holders.

---

## Disclaimer

NewJams is an **independent, unofficial fan-developed application**.

The project is not affiliated with, authorized by, sponsored by, or endorsed by NewJeans, ADOR, HYBE, YouTube, or their respective subsidiaries or affiliates.

References to NewJeans and associated media are used for descriptive and identification purposes.

Third-party media is accessed through supported external services and remains subject to applicable platform terms, copyright restrictions, embedding permissions, and content availability.

NewJams does not claim ownership of third-party music, videos, trademarks, or other protected materials.

---

### NewJams ♡

**Music, technology, and a little Y2K nostalgia.**

Developed and maintained by **[George Paraskevopoulos](https://github.com/Unknown-George)**.

**[Launch NewJams](https://newjams.pages.dev/)** · **[Download NewJams](https://newjams.pages.dev/)** · **[GitHub Profile](https://github.com/Unknown-George)**

© 2026 George Paraskevopoulos. All rights reserved.
