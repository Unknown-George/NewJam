# NewJams

**A Cross-Platform Music Application Inspired by NewJeans**

An independently developed music platform combining a contemporary listening experience, personalized media management, and a distinctive Y2K-inspired interface.

**[Launch Application](https://newjams.pages.dev/)** · **[Download for Desktop](https://newjams.pages.dev/)** · **[Developer Profile](https://github.com/Unknown-George)**

| Project Information | Details |
|---|---|
| **Application** | NewJams |
| **Latest Confirmed Release** | v1.0.5 |
| **Supported Platforms** | Web, Windows x64, macOS ARM64, macOS x64 |
| **Application Type** | Cross-platform music and media player |
| **Development** | Independent software project |
| **Source Availability** | Proprietary — private repositories |
| **Official Website** | [newjams.pages.dev](https://newjams.pages.dev/) |
| **Developer** | [George Paraskevopoulos](https://github.com/Unknown-George) |

---

## 01. Project Overview

**NewJams** is an independently developed, cross-platform music application inspired by NewJeans and the visual characteristics of early-2000s digital design.

Initially conceived as a browser-based music player, the project evolved into a desktop-capable application supporting modern web browsers, Windows, and macOS.

The application brings together supported music playback, YouTube media integration, personal music libraries, playlist management, user authentication, and account-based preferences within a consistent interface.

NewJams is built using **React, Vite, Electron, Supabase, PostgreSQL, and Cloudflare infrastructure**. Its development encompasses frontend engineering, managed backend integration, desktop application packaging, release automation, update verification, and production security hardening.

The project demonstrates the process of developing and maintaining a complete user-facing software product, from interface implementation through deployment and distribution.

**Project status:** v1.0.5 is the latest confirmed publicly released version. A subsequent playlist-focused improvement has been discussed but is not represented here as released.

---

## 02. Application Features

### 2.1 Music Playback

NewJams provides a custom playback interface integrated with supported YouTube media.

Core capabilities include:

- Media selection and playback.
- Play, pause, and track navigation.
- Music information and available artwork.
- Integrated video playback controls.
- Playback-state management.
- Handling of unavailable or restricted embedded content.
- External playback through YouTube when required.

The desktop application includes specific handling for YouTube's embedded-player client identity and referrer requirements.

Playback availability remains subject to the original content provider's restrictions.

### 2.2 Personal Music Library

The personal library provides a centralized location for organizing saved music and supported media.

The interface integrates saved content with the broader application experience, allowing users to navigate between their library, media playback, and playlists.

Account-associated content is supported by the application's Supabase data architecture.

### 2.3 Playlist Management

NewJams includes functionality for building and maintaining personal music collections.

Supported operations include:

- Creating personal playlists.
- Naming and organizing collections.
- Adding supported music and video entries.
- Removing entries from playlists.
- Accessing saved playlists across supported authenticated sessions.
- Persisting account-associated playlist information.

The playlist system is designed to provide accessible, organized media management while maintaining the application's established visual identity.

### 2.4 Music Videos and Dance Practice

NewJams provides dedicated navigation for supported video categories.

**Music Videos**

Allows users to browse and watch supported music videos through YouTube's embedded playback functionality.

**Dance Practice**

Provides a separate destination for supported dance-related video content.

Both sections use external media integration rather than independently hosting copyrighted recordings.

### 2.5 Search and Discovery

Search and discovery features support navigation through available music-related content.

The interface allows users to locate supported media and access relevant content within the application.

### 2.6 User Authentication and Profiles

NewJams uses **Supabase Authentication** to support account-based functionality.

Capabilities include:

- Email and password authentication.
- User registration and sign-in.
- Account profile management.
- Avatar and profile customization.
- Account-specific preferences.
- Persistent saved content where supported.
- Authentication-session management.

The authentication architecture separates identity management from the React frontend.

### 2.7 Listening Activity

The application includes listening-related functionality intended to provide users with information about their activity.

Features developed for the project include accumulated listening time, frequently played music, and account-associated listening information.

### 2.8 Interface and Personalization

NewJams combines modern application conventions with a restrained Y2K-inspired visual language.

The interface incorporates:

- Dark mode as the default theme.
- Optional light-mode preferences.
- Persistent theme settings.
- Component-based layouts.
- Consistent typography and spacing.
- Responsive browser layouts.
- Shared visual components across platforms.
- Platform-specific desktop navigation adjustments.

The objective is to provide a recognizable interface without sacrificing clarity or usability.

---

## 03. Supported Platforms and Distribution

NewJams is available through a hosted web application and separately packaged desktop installations.

### 3.1 Web Application

**Production URL:** https://newjams.pages.dev/

The web version is hosted on Cloudflare Pages and is accessible through a compatible browser.

No local development tools or application installation are required.

### 3.2 Desktop Applications

The desktop versions are packaged with Electron and distributed as platform-specific installers.

| Platform | Architecture | Package Format | Release |
|---|---|---|---|
| Windows | x64 | `.exe` | v1.0.5 |
| macOS | Apple Silicon / ARM64 | `.dmg` | v1.0.5 |
| macOS | Intel / x64 | `.dmg` | v1.0.5 |

**Official Downloads**

| Platform | Installer |
|---|---|
| Windows x64 | [Download NewJams for Windows](https://pub-f37b1abf363249fc941a05f7c78de0d7.r2.dev/v1.0.5/NewJams-Setup-1.0.5-x64.exe) |
| macOS Apple Silicon | [Download NewJams for Apple Silicon](https://pub-f37b1abf363249fc941a05f7c78de0d7.r2.dev/v1.0.5/NewJams-1.0.5-mac-arm64.dmg) |
| macOS Intel | [Download NewJams for Intel Mac](https://pub-f37b1abf363249fc941a05f7c78de0d7.r2.dev/v1.0.5/NewJams-1.0.5-mac-x64.dmg) |

The website and desktop installers are distributed independently of the original development repositories.

**Installation notice:** The current desktop builds are unsigned and not notarized. Operating-system security warnings may appear during installation.

---

## 04. Technology Stack

The application integrates frontend technologies, managed backend infrastructure, desktop tooling, and cloud-based distribution services.

| Layer | Technology | Responsibility |
|---|---|---|
| Frontend Framework | React | Component-based application interface |
| Programming Language | JavaScript | Client-side application behavior |
| Styling | CSS | Layouts, themes, and responsive design |
| Build System | Vite | Development tooling and optimized production bundles |
| Desktop Runtime | Electron | Standalone Windows and macOS applications |
| Desktop Packaging | Electron Builder | Installer generation and platform packaging |
| Authentication | Supabase Auth | Account registration, login, and sessions |
| Backend Services | Supabase | Managed application backend |
| Database | PostgreSQL | Persistent application and user data |
| Media Integration | YouTube Embedded Player | Supported music and video playback |
| Web Deployment | Cloudflare Pages | Production website hosting |
| Installer Hosting | Cloudflare R2 | Public release artifact distribution |
| Source Control | Git | Version management |
| Repository Hosting | GitHub | Private source and release repositories |
| Automation | GitHub Actions | Build, test, and release workflows |
| Policy Verification | Ed25519 | Cryptographic update-policy authentication |
| Artifact Verification | SHA-256 | Installer integrity verification |

---

## 05. System Architecture

NewJams uses a shared React frontend with platform-specific Electron integration and managed backend services.

### 5.1 Frontend Layer

The application interface is implemented using React and JavaScript.

Reusable components support navigation, media playback, music organization, profiles, account settings, and personalization.

Vite provides development tooling and production compilation.

Sharing frontend components between browser and desktop builds reduces duplicated implementation while maintaining a consistent user experience.

### 5.2 Backend and Data Layer

Supabase provides account authentication and managed backend services.

PostgreSQL supports persistence for application-related user data.

The frontend communicates with Supabase services to support authenticated operations and account-specific functionality.

This architecture separates user-facing presentation from persistent data management.

### 5.3 Media Integration Layer

NewJams uses supported YouTube embeds to display externally hosted media.

Playback controls and error handling are integrated into the application interface.

The system accounts for embedding restrictions and provides access to external playback when supported content cannot be embedded.

The desktop integration includes appropriate referrer handling for Electron's application environment.

### 5.4 Desktop Application Layer

Electron provides the desktop runtime and operating-system integration.

The desktop layer supports:

- Standalone application windows.
- Secure renderer configuration.
- Platform-specific application startup.
- Controlled external navigation.
- Desktop-specific interface behavior.
- Application version checking.
- Installer download and verification.
- Windows and macOS packaging.

### 5.5 Cloud Infrastructure

NewJams separates web hosting from installer distribution.

**Cloudflare Pages** hosts the public browser application.

**Cloudflare R2** stores publicly downloadable desktop installation packages and update-related artifacts.

Private GitHub repositories hold the original development resources and support the build and release process.

This separation allows the application to remain publicly accessible while preserving the privacy of its source repositories.

---

## 06. Desktop Version Management

NewJams introduced its desktop update architecture in v1.0.4.

The system checks a remotely hosted update policy and determines whether an installed desktop version is currently supported.

### 6.1 Update Policy

The update policy contains information used to determine:

- Latest available application version.
- Minimum supported application version.
- Optional or mandatory update status.
- Platform-specific installer selection.
- Installer verification requirements.

### 6.2 Mandatory and Optional Updates

When a newer version is available, the application can display an update prompt.

Updates become mandatory when the installed version falls below the configured minimum supported version.

For mandatory updates, the interface requires the user to update or quit before entering the main application.

If the policy service becomes temporarily unavailable, the application can continue without indefinitely locking users out.

### 6.3 Cryptographic Verification

The update architecture uses two separate protections.

| Mechanism | Purpose |
|---|---|
| Ed25519 signatures | Verify the authenticity of update policy data |
| SHA-256 checksums | Verify the integrity of downloaded installer packages |

The current unsigned distribution uses installer-based updates.

NewJams can download, verify, and open the installer, but users must complete the installation themselves.

Fully automatic in-place replacement is not currently enabled.

---

## 07. Security and Proprietary Source Code

**NewJams is proprietary software. The original development source code and private GitHub repositories are not publicly distributed.**

The project follows a separation between internal development resources and the files necessary for public application use.

### 7.1 Private Development Repositories

Both the primary source repository and the release repository are privately maintained.

The original repository structure, development history, internal resources, and privileged deployment credentials are not made publicly available as open-source distributions.

### 7.2 Production Code Hardening

Version 1.0.5 introduced additional protections designed to reduce unnecessary source exposure and increase the difficulty of analyzing distributed application code.

Implemented measures include:

- Optimized production JavaScript minification.
- Selective first-party JavaScript obfuscation.
- Minified Electron main and preload modules.
- Production-only Electron packaging.
- Exclusion of original Electron development source files.
- Disabled production source maps.
- Exclusion of unnecessary development resources.
- Reduced packaged runtime dependencies.
- Electron ASAR packaging and supported integrity checks.
- Hardened Electron security configuration.

These measures improve production hygiene and raise the effort required to interpret bundled code.

### 7.3 Packaging Optimization

The v1.0.5 security-hardening effort also reduced unnecessary files in the Electron application archive.

| Packaging Metric | v1.0.4 | v1.0.5 |
|---|---:|---:|
| Packaged ASAR files | 2,202 | 212 |
| ASAR archive size | 13.80 MB | 1.87 MB |
| Original Electron source tree | Included as readable modules | Excluded |
| First-party Electron modules | Readable | Minified and selectively obfuscated |

The resulting ASAR archive was approximately **86% smaller**.

Archive-size reduction reflects packaging optimization and should not be interpreted as a quantitative security guarantee.

### 7.4 Electron Security Controls

The application retains Electron security protections, including:

- Context isolation.
- Renderer sandboxing where supported.
- Disabled renderer Node.js integration.
- Restricted navigation.
- Controlled external-link handling.
- Reduced exposure of native functionality.
- Compatible ASAR integrity features and Electron fuses.

### 7.5 Secret Management

Privileged release and deployment credentials are maintained separately from public application artifacts.

The v1.0.5 release audit reported that no privileged credentials were identified in the packaged application.

Public client configuration is distinguished from secret backend or release credentials.

### 7.6 Source Availability and Limitations

NewJams is not released as an open-source project.

Public access is limited to the hosted web application, desktop installers, and required public distribution assets.

**The original source repository is not provided to users.**

As with other browser-based and Electron applications, the distributed software contains client-side code that can be inspected or reverse-engineered.

Minification, obfuscation, and packaging do not provide absolute protection against code extraction.

They are used to reduce exposure of unnecessary resources and make remaining distributed code harder to interpret.

---

## 08. Testing and Quality Assurance

NewJams development includes automated tests, packaged application checks, and release-artifact validation.

### 8.1 Testing Coverage

Project verification has included:

- Automated application tests.
- Frontend production builds.
- Desktop application startup checks.
- Navigation validation.
- Music playback controls.
- YouTube integration checks.
- Update-policy behavior.
- Installer integrity verification.
- Electron security configuration.
- Production packaging inspection.
- Source exposure audits.

### 8.2 Platform Validation

Desktop releases have been evaluated across Windows x64, macOS ARM64, and macOS x64 environments.

Testing has included packaged application launch checks and relevant workflow verification.

Some functionality, such as authentication with real accounts and complete update-installation scenarios, has not been comprehensively exercised in every production environment.

### 8.3 v1.0.5 Release Verification

The v1.0.5 release validation included:

- 20 passing automated tests.
- Successful production frontend compilation.
- Windows x64 packaged application verification.
- macOS Apple Silicon packaged application checks.
- macOS Intel packaged application checks.
- Installer checksum verification.
- Electron ASAR and fuse inspection.
- Signed update-policy verification.
- Cloudflare Pages deployment verification.
- Cloudflare R2 installer-integrity validation.

These checks provide release confidence but do not constitute a guarantee that every operation has been tested across all devices and accounts.

---

## 09. Build and Release Engineering

NewJams was developed with a structured release process rather than relying exclusively on manually uploaded application files.

The release architecture supports:

1. Application compilation.
2. Automated test execution.
3. Production asset generation.
4. Desktop application packaging.
5. Platform startup validation.
6. Installer creation.
7. Cryptographic integrity verification.
8. Artifact distribution through Cloudflare R2.
9. Website deployment through Cloudflare Pages.
10. Application version and update-policy management.

GitHub Actions has been used for cross-platform build and release automation.

The existing infrastructure also supports direct website deployment when GitHub Actions execution is unavailable.

The release process keeps the public application distribution separate from the private development repositories.

---

## 10. Release History

| Version | Milestone |
|---|---|
| **v1.0.2** | Desktop packaging and initial distribution improvements |
| **v1.0.3** | Desktop playback handling, default dark theme, and navigation refinements |
| **v1.0.4** | Signed update policies, version management, and installer verification |
| **v1.0.5** | Production code hardening, optimized packaging, and application security improvements |

**Current confirmed production release:** v1.0.5.

The project was restored to the original v1.0.5 interface after subsequent experimental changes. The public website and desktop download links correspond to the stable v1.0.5 release.

---

## 11. Engineering Objectives and Outcomes

NewJams was developed to apply software engineering principles to a complete application rather than an isolated programming exercise.

### Frontend Engineering

Implemented a component-based interface using React, JavaScript, and CSS.

Developed consistent navigation, application views, playback controls, and theme behavior.

### Backend Integration

Integrated managed authentication and persistent data through Supabase and PostgreSQL.

Supported account-specific application functionality without maintaining a custom password authentication service.

### Cross-Platform Engineering

Adapted a shared frontend for browser-based use and packaged desktop applications.

Supported Windows x64, macOS Apple Silicon, and macOS Intel.

### Cloud Deployment

Established public website hosting through Cloudflare Pages and installer distribution through Cloudflare R2.

Separated public distribution assets from private project repositories.

### Release Engineering

Developed automated build, packaging, testing, and verification workflows.

Introduced application version management and cryptographically verified update metadata.

### Application Security

Implemented secure Electron configuration, production-only packaging, JavaScript hardening, secret-management separation, and release-integrity verification.

Together, these areas demonstrate practical experience across frontend development, backend integration, infrastructure, desktop distribution, and application maintenance.

---

## 12. Maintenance and Project Scope

NewJams is independently maintained.

Development has focused on application stability, interface consistency, playlist management, media playback compatibility, release reliability, and protection of original development resources.

The application may receive targeted maintenance or improvements where necessary.

Its features and third-party media availability remain subject to technical compatibility and external platform requirements.

---

## 13. Developer

**George Paraskevopoulos**  
*Independent Software Developer*

**GitHub:** [github.com/Unknown-George](https://github.com/Unknown-George)  
**Application:** [newjams.pages.dev](https://newjams.pages.dev/)

NewJams was independently developed as a personal software engineering project.

The project reflects hands-on experience in designing, developing, securing, packaging, deploying, and maintaining a cross-platform application.

It represents a combination of software engineering practice and a music-focused, user-oriented product concept.

---

## 14. Intellectual Property and Licensing

**Copyright © 2026 George Paraskevopoulos. All rights reserved.**

NewJams is a privately maintained, proprietary software project.

The original development source code is not publicly distributed, and no general open-source license is granted for proprietary project materials.

Public access to the website or desktop application does not grant permission to reproduce, redistribute, or commercially exploit proprietary NewJams code and original assets beyond what applicable law or relevant third-party licenses permit.

Third-party libraries and dependencies remain subject to their respective licenses.

All third-party music, videos, trademarks, logos, artwork, and other protected materials remain the property of their respective rights holders.

---

## 15. Disclaimer

NewJams is an **independent, unofficial fan-developed application**.

The project is not affiliated with, authorized by, sponsored by, or endorsed by NewJeans, ADOR, HYBE, YouTube, or their respective subsidiaries or affiliates.

References to NewJeans and associated media are used for identification and descriptive purposes.

Third-party media is accessed through supported external services and remains subject to applicable copyright laws, platform terms, embedding permissions, and content availability.

NewJams does not claim ownership of third-party intellectual property.

---

**NewJams**

*A Cross-Platform Music Application*

Developed and maintained by **[George Paraskevopoulos](https://github.com/Unknown-George)**

[Official Website](https://newjams.pages.dev/) · [Desktop Downloads](https://newjams.pages.dev/) · [Developer GitHub](https://github.com/Unknown-George)

**© 2026 George Paraskevopoulos. All rights reserved.**
