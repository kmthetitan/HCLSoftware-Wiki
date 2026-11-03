# SmartGov

SmartGov is a Volt Iris / Volt MX mobile application prototype that brings common citizen-facing government services into one mobile experience. The project includes screens and controller code for service discovery, documents, family profiles, payments, notifications, and account information.

> **Project status:** This repository is a Volt Iris project export, not a standalone Node.js application. Some flows use mock data or simulated actions, and the included Fabric service metadata is not fully configured. Treat feature descriptions as a guide to the project structure, not as a claim that every service is production-ready.

## Wiki

- [[Getting-Started|Getting Started]]
- [[Architecture]]
- [[Features]]
- [[Fabric-and-Backend-Services|Fabric and Backend Services]]
- [[Data-Model|Data Model]]
- [[Development-and-Testing|Development and Testing]]

## At a glance

| Area | Project evidence |
|---|---|
| App platform | Volt Iris / Volt MX |
| App identifier | `SmartGov` |
| Project version | `1.0.0` in the headless build properties |
| Main client language | JavaScript controllers |
| Backend assets | Volt MX Fabric identity, integration, orchestration, and object-service project files |
| Test scaffolding | Jasmine plans for mobile, tablet, and desktop |

## Source layout

The application project is in the repository root. Start with `controllers/mobile/` for screen behavior, `forms/` for UI definitions, `resources/` for app assets, and `Fabric/Apps/` for Fabric configuration and database migration assets.
