# Architecture

SmartGov follows the Volt MX project structure: declarative screen definitions, JavaScript controllers, reusable resources, and a separate Fabric project configuration.

## Application layers

| Path | Responsibility |
|---|---|
| `forms/` | Form and widget UI definitions |
| `controllers/mobile/` | Mobile screen behavior, event handlers, and navigation |
| `controllers/desktop/`, `controllers/tablet/` | Platform-specific controller assets |
| `navigation/` | Navigation-controller assets by platform |
| `themes/` | Application styling and skins |
| `resources/` | Images, fonts, libraries, and other app resources |
| `Fabric/Apps/` | Volt MX Fabric identity, integration, orchestration, and object-service assets |
| `testresources/Jasmine/` | Jasmine test plans and shared test reporter |

## Mobile controller groups

Mobile controller folders are grouped by feature:

- `grpStartup/` — startup/dashboard screens
- `grpGovServ/` — government-service categories and related screens
- `grpDocs/` — document list, upload, and viewer screens
- `grpFam/` — family, member, and permission screens
- `grpNotifs/` — notifications and notification details
- `grpUserserv/` — profile, payment, and payment history

Volt MX APIs appear in the client code for screen navigation (`voltmx.mvc.Navigation`), local key/value storage (`voltmx.store`), and HTTP requests (`voltmx.net.HttpRequest`). Consult the specific controller before assuming a flow is backed by a live service: parts of the application use mock data or simulated processing.

## Fabric layout

- `Fabric/Apps/_Identity/SmartGovAuth/` contains the `SmartGovAuth` user-store identity configuration.
- `Fabric/Apps/_Integration/OpenLibraryService/1.0/` contains an integration service with `searchBooks` and `getBookByISBN` operation assets.
- `Fabric/Apps/_Orchestration/smartGovServ/1.0/` contains orchestration metadata.
- `Fabric/Apps/_ObjectServices/SmartGov/1.0/` contains object definitions, fields, mappings, relationships, and MySQL Flyway migrations.
- `Fabric/Apps/SmartGov/Meta.json` declares the app's linked services.

Metadata files in several of these service directories are marked `empty`. Treat them as project assets requiring environment setup and validation, not proof of a deployed or operational backend.

