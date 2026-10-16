<h1 align="center">Android-Skills</h1>
<p align="center">
  <a href="README.md">简体中文</a>
</p>

<p align="center">
  <a href="https://developer.android.com"><img src="https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white" alt="Android"></a>
  <a href="https://kotlinlang.org"><img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white" alt="Kotlin"></a>
  <a href="https://developer.android.com/jetpack/compose"><img src="https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white" alt="Jetpack Compose"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache%202.0-2C6BED?style=flat-square&logo=apache&logoColor=white" alt="License"></a>
</p>

## Introduction

**Android-Skills** is a curated Skills integration package for Android developers, bringing together three high-quality sources:

| Source | Focus | Usage Strategy |
|------|------|----------|
| [android/skills](https://github.com/android/skills) | Google's official Android Skills library | **Prioritized**, covering platform standards, migration guides, compliance checks, CLI tools, etc. |
| [chrisbanes/skills](https://github.com/chrisbanes/skills) | Chris Banes' deep Kotlin / Compose practices | **Used as a supplement**, including only coding practices, architecture, and performance Skills not covered or differently emphasized by the official library |
| [ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | General UI/UX design Skills library | **Selectively retained**, keeping only design systems, branding, and UI/UX Skills useful for Android development |

The integration package follows these principles:

1. **Official first**: If a Skill already exists in the official library, the `android/skills` version is preferred.
2. **Supplemental support**: `chrisbanes/skills` only provides Kotlin / Compose coding expertise missing from the official library.
3. **Selective retention**: `ui-ux-pro-max-skill` removes unrelated content such as Web / Tailwind / shadcn.

## Skills List

### Official Skills (android/skills)

The following Skills all come from `android/skills` and are the preferred reference for Android development:

| Skill | Purpose |
|------|------|
| `adaptive` | Adapt to phones, tablets, foldables, desktop, TV, Auto, XR |
| `edge-to-edge` | Edge-to-edge display, Insets handling, IME adaptation |
| `jetpack-compose-performance` | Compose performance diagnosis and optimization |
| `navigation-3` | Jetpack Navigation 3 migration and usage |
| `navigation-event` | Predictive back gestures and back interception |
| `migrate-xml-views-to-jetpack-compose` | Migrate XML Views to Compose |
| `testing-setup` | Unit test, UI test, screenshot test infrastructure |
| `agp-9-upgrade` | Upgrade to Android Gradle Plugin 9 |
| `android-cli` | Use the `android` command-line tool |
| `camerax` | CameraX camera development |
| `restore-credentials` | Passwordless sign-in and silent sign-in after device restore |
| `verified-email` | OTP-less email verification |
| `appfunctions` | Expose App functions to the Android system for AI Agent invocation |
| `android-permissions-security` | Permission and IPC component security audit |
| `android-intent-security` | Intent security and redirection protection |
| `play-policy-insights` | Google Play policy compliance check |
| `r8-analyzer` | R8 / ProGuard keep rule optimization |
| `play-billing-library-version-upgrade` | Google Play Billing Library upgrade |
| `android-profiler` | System Trace, ANR, memory leak, battery usage analysis |
| `leanback-to-compose-tv-migration` | Migrate Leanback to Compose for TV |
| `android-for-cars-parked-apps` | Car parked app adaptation |
| `glance-canonical-layouts` | Jetpack Glance home screen widgets |

> The complete list is subject to the official `android/skills` repository.

### Supplemental Skills (chrisbanes/skills)

The following Skills do not exist in the official repository or have a different focus, and are included as supplements:

| Skill | Purpose |
|------|------|
| `using-chrisbanes-skills` | Routing entry point for the Chris Banes Skills package |
| `compose-state-and-effects` | Compose state management and side effects |
| `compose-component-design` | Reusable Compose component API design |
| `compose-animations` | Compose animations and transitions |
| `compose-performance` | Recomposition cost, compiler stability, skippability analysis |
| `compose-ui-testing-patterns` | Compose UI testing and screenshot testing patterns |
| `kotlin-api-design` | Kotlin function, class, extension, value class design |
| `kotlin-concurrency-and-flow` | Coroutine scope, Flow, StateFlow modeling |
| `kotlin-control-flow` | Kotlin control flow, sealed types, smart casts |
| `gradle-run` | Gradle build diagnosis and execution |
| `grounded-writing` | Technical documentation, blog posts, review comments writing |
| `compose-focus-navigation` | TV, keyboard, D-pad focus navigation |

### UI/UX Design Skills (selectively retained from ui-ux-pro-max-skill)

Only Skills useful for Android development are retained:

| Skill | Purpose |
|------|------|
| `ui-ux-pro-max` | UI/UX design intelligence, covering components, layout, color, typography, accessibility |
| `design-system` | Design tokens, component specifications, spacing and typography scales |
| `brand` | Brand voice, visual identity, brand consistency |
| `banner-design` | Google Play promotional graphics, social media assets (optional) |

> Removed: `ui-styling` (Web / shadcn / Tailwind), `slides` (presentations), and other Skills unrelated to native Android development.

## Installation

### Method 1: Batch install using `npx skills`

```bash
# Install official Skills (preferred)
npx skills add https://github.com/android/skills \
  --skill adaptive \
  --skill edge-to-edge \
  --skill jetpack-compose-performance \
  --skill navigation-3 \
  --skill navigation-event \
  --skill migrate-xml-views-to-jetpack-compose \
  --skill testing-setup \
  --skill agp-9-upgrade \
  --skill android-cli \
  --skill camerax \
  --skill restore-credentials \
  --skill verified-email \
  --skill appfunctions \
  --skill android-permissions-security \
  --skill android-intent-security \
  --skill play-policy-insights \
  --skill r8-analyzer \
  --skill play-billing-library-version-upgrade \
  --skill android-profiler \
  --skill leanback-to-compose-tv-migration \
  --skill android-for-cars-parked-apps \
  --skill glance-canonical-layouts

# Install Chris Banes supplemental Skills
npx skills add chrisbanes/skills  \
  --skill using-chrisbanes-skills \
  --skill compose-state-and-effects \
  --skill compose-component-design \
  --skill compose-animations \
  --skill compose-performance \
  --skill compose-ui-testing-patterns \
  --skill kotlin-api-design \
  --skill kotlin-concurrency-and-flow \
  --skill kotlin-control-flow \
  --skill gradle-run \
  --skill grounded-writing \
  --skill compose-focus-navigation

# Install selectively retained UI/UX Skills
npx skills add nextlevelbuilder/ui-ux-pro-max-skill --global --yes \
  --skill ui-ux-pro-max \
  --skill design-system \
  --skill brand \
  --skill banner-design
```

### Method 2: Manual copy

Copy each Skills folder to the corresponding Agent's skills directory, for example:

- Claude Code: `~/.claude/skills/`
- Cursor: `~/.cursor/skills/`
- Other Agents: refer to their official documentation

## Acknowledgements

- [android/skills](https://github.com/android/skills) — Google's official Android Skills library
- [chrisbanes/skills](https://github.com/chrisbanes/skills) — Chris Banes' Kotlin / Compose practices
- [ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) — UI/UX design Skills library
