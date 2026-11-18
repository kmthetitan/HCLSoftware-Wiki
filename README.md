# SmartGov

SmartGov is a mobile-first government-services application prototype for discovering public services and completing citizen workflows such as document management, family profiles, notifications, user services, and payments.

> **Project status:** A Volt Iris / Volt MX project export. Some flows use mock data or simulated actions, and checked-in Fabric service metadata requires environment-specific configuration.

## Highlights

- Mobile-first government-service discovery and workflows
- JavaScript controllers organized with Volt MX MVC patterns
- Document, family, notification, profile, and payment areas
- Volt MX Fabric identity, integration, orchestration, and object-service assets
- MySQL Flyway migrations and Jasmine test scaffolding
- GitHub-wiki-compatible project documentation

## Technology

- **Platform:** HCL Volt Iris `10.0.5.0` / Volt MX `10.0.7.0`
- **Application:** JavaScript MVC controllers, forms, widgets, themes, and navigation
- **Backend:** Volt MX Fabric services and MySQL
- **Testing:** Jasmine plans for mobile, tablet, and desktop

## Repository guide

| Area | Location |
|---|---|
| Startup and dashboard | `controllers/mobile/grpStartup/` |
| Sign-in | `controllers/mobile/grpGovServ/`, `controllers/mobile/frmLoginController/` |
| Government services | `controllers/mobile/grpGovServ/` |
| Documents | `controllers/mobile/grpDocs/` |
| Family and permissions | `controllers/mobile/grpFam/` |
| Notifications | `controllers/mobile/grpNotifs/` |
| Profile and payments | `controllers/mobile/grpUserserv/` |
| Fabric assets | `Fabric/Apps/` |
| Tests | `testresources/Jasmine/` |
| Documentation | `wiki/Home.md` |

## Run locally

This repository is a Volt Iris project, not a conventional Node.js application.

1. Open HCL Volt Iris and import or open the `SmartGov` project directory.
2. Select a supported build target and configure platform settings.
3. Configure the Fabric environment before exercising backend-dependent flows.
4. Build and run on a suitable emulator or device.

The checked-in `HeadlessBuild.properties` contains default headless-build settings that may require adjustment for a local machine or CI environment.

## Backend setup

Fabric assets are under `Fabric/Apps/`. The object service includes entities for user profiles, service requests, notifications, and government-service categories. Review environment mappings before connecting live services.

## Testing

Jasmine test scaffolding is located in `testresources/Jasmine/`. Run and validate test plans using tooling supplied with the Volt Iris installation; this repository does not include a standalone command-line test runner.

## Documentation

See [`wiki/Home.md`](wiki/Home.md) for architecture, setup, feature notes, backend assets, data model, and development guidance.
