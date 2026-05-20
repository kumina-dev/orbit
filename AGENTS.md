# AGENTS.md

## Project

This is a fresh React Native CLI + TypeScript mobile app.

The old Expo project is reference material only. Do not migrate it 1:1.

## Goal

Build a maintainable mobile app with a pragmatic OOP-style architecture.

The foundation matters:

- app identity
- assets
- navigation
- native configuration
- permissions
- notifications
- storage
- architecture boundaries
- build verification

## Project structure

Use a practical React Native folder structure with familiar names:

```txt
src/
  app/
  assets/
  config/
  features/
  services/
  screens/
  components/
  hooks/
  utils/
  types/
```

Prefer folder names commonly used in real React Native projects.

Do not force clean architecture naming such as domain/application/infrastructure/presentation unless explicitly requested.

## OOP style

Use pragmatic OOP inside services, repositories, adapters, schedulers, and clients.

Good:

- services/storage/StorageService.ts
- services/notifications/NotificationService.ts
- features/routines/services/RoutineService.ts
- features/settings/services/SettingsRepository.ts

Avoid:

- class-based React components
- abstract factory/provider/manager chains
- unnecessary interfaces for every class
- architecture folders that make the app harder to navigate

## Rules

- No Expo packages.
- No Expo Router.
- No 1:1 migration from the old project.
- Keep React components functional.
- Use classes for services, use cases, repositories, gateways, adapters, and schedulers.
- Keep native-facing code behind infrastructure adapters.
- Do not touch Android/iOS native code unless the task requires it.
- Do not edit Markdown files unless explicitly asked.

## Foundation checklist

Before feature implementation, verify:

- package name / bundle id
- app name
- app icon
- splash screen
- Android adaptive icon
- permissions
- notification channel strategy
- storage strategy
- navigation setup
- TypeScript path aliases
- lint/typecheck scripts
- Android build works

## Reference project rule

The old Expo project may be inspected for:

- feature behavior
- copy
- data shapes
- user flows
- domain concepts

Do not copy:

- Expo-specific dependencies
- Expo Router structure
- old documentation
- old AGENTS.md
- old folder structure blindly

## Working mode

For broad tasks:

1. inspect
2. report findings
3. propose plan
4. wait before editing

For implementation tasks:

- make the smallest useful patch
- keep changes reviewable
- explain verification commands
