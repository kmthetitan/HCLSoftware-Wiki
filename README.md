# SmartGov

SmartGov is a mobile-first government services application prototype built with HCL Volt Iris / Volt MX. It brings service discovery and common citizen workflows—documents, family profiles, payments, notifications, and account information—into a single app.

> **Project status:** This repository contains a Volt Iris project export. Some flows use mock data or simulated actions, and the checked-in Fabric service metadata requires environment configuration. The presence of a screen, model, or service asset does not mean that a production backend integration is complete.

## Technology

- **Platform:** Volt Iris / Volt MX
- **Application:** JavaScript controllers with Volt MX forms and widgets
- **Navigation and device APIs:** Volt MX MVC navigation, local storage, and networking APIs
- **Backend assets:** Volt MX Fabric identity, integration, orchestration, object services, and MySQL Flyway migrations
- **Test scaffolding:** Jasmine plans for mobile, tablet, and desktop

Project properties identify Volt Iris `10.0.5.0` and Volt MX `10.0.7.0`. Use tooling compatible with this project version.

## Features and code locations

| Area | Location |
|---|---|
| Startup and dashboard | `controllers/mobile/grpStartup/` |
| Sign-in | `controllers/mobile/FormSignInController/` and `controllers/mobile/frmLoginController/` |
| Government service categories | `controllers/mobile/grpGovServ/` |
| Document list, upload, and viewer | `controllers/mobile/grpDocs/` |
| Family members and permissions | `controllers/mobile/grpFam/` |
| Notifications | `controllers/mobile/grpNotifs/` |
| Profile and payments | `controllers/mobile/grpUserserv/` |

These are feature entry points; inspect the corresponding form and controller to understand the behavior of a particular screen.

## Project layout

| Path | Contents |
|---|---|
| `forms/` | Screen and widget definitions |
| `controllers/` | Screen logic, organized by platform and feature |
| `navigation/` | Platform-specific navigation-controller assets |
| `themes/` | Themes and styling resources |
| `resources/` | Images, fonts, libraries, and other application assets |
| `Fabric/Apps/` | Fabric app, identity, integration, orchestration, object-service, and migration assets |
| `testresources/Jasmine/` | Jasmine test plans and shared reporter |
| `wiki/` | GitHub-Wiki-compatible project documentation |

## Open and run

This is a Volt Iris project, not a standalone Node.js project; no `npm install` or `npm start` workflow is provided.

1. Open Volt Iris and import or open the `SmartGov` project directory.
2. Select a supported build target and configure the required platform settings.
3. Configure the intended Fabric environment before testing flows that depend on backend services.
4. Build and run the app from Volt Iris on a suitable emulator or device.

The project also includes `HeadlessBuild.properties` for Volt MX headless builds. Its checked-in defaults use build mode `0` and disable the listed platform targets. Configure local or CI environment values and the required targets before building. Do not commit credentials, tokens, or signing secrets.

## Fabric and data

Fabric assets are under `Fabric/Apps/`. The SmartGov object service includes entities such as `UserProfile`, `ServiceRequests`, `Notifications`, and government-service categories. MySQL Flyway migration scripts are in `Fabric/Apps/_ObjectServices/SmartGov/1.0/_Flyway/MYSQL/`.

The project metadata includes identity, integration, and orchestration assets, but some service metadata is marked empty or needs environment-specific setup. Review and validate service mappings, endpoints, authentication, and migrations in the target Fabric environment before relying on backend behavior.

## Testing

Jasmine test scaffolding and platform test plans are located in `testresources/Jasmine/`. Configure and run them using the test tooling available in your Volt Iris installation. There is no conventional package-based test command in this project export, and the test plans may not cover every feature flow.

## Documentation

See [`wiki/Home.md`](wiki/Home.md) for the project documentation index, including getting started, architecture, feature notes, backend assets, data model, and development/testing guidance.
