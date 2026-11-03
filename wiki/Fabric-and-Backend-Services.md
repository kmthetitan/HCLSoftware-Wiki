# Fabric and Backend Services

The Fabric project assets are stored under `Fabric/Apps/`. They describe the services and models associated with SmartGov, but checked-in metadata is not sufficient to establish that a backend is deployed or ready to use.

## Configured project assets

| Asset | Location | What is present |
|---|---|---|
| Fabric app | `Fabric/Apps/SmartGov/` | App metadata links `SmartGovAuth`, the `OpenLibraryService` integration, the `smartGovServ` orchestration, and the `SmartGov` object service |
| Identity | `Fabric/Apps/_Identity/SmartGovAuth/` | User-store identity metadata |
| Integration | `Fabric/Apps/_Integration/OpenLibraryService/1.0/` | Operation assets `searchBooks` and `getBookByISBN` |
| Orchestration | `Fabric/Apps/_Orchestration/smartGovServ/1.0/` | Orchestration metadata |
| Object service | `Fabric/Apps/_ObjectServices/SmartGov/1.0/` | Object definitions, field definitions, CRUD mappings, relationships, and MySQL Flyway scripts |

The integration, orchestration, object-service, and identity metadata include `empty` or configuration markers that require review in Volt Iris/Fabric. In particular, do not infer that the OpenLibrary integration is a live government-service backend.

## Before connecting an environment

1. Import or open the Fabric assets in the supported Volt Iris/Fabric tooling.
2. Configure the target Fabric environment, service endpoints, authentication, and any required identity provider.
3. Review object-service mappings and the database migrations for the target database.
4. Test each client flow against the configured environment; replace demo/mock behavior where production data is required.
5. Keep credentials, tokens, and environment-specific secrets outside source control.

`HeadlessBuild.properties` contains blank environment and credential fields. Populate these only through your approved local or CI secret-management process before a build or publish.

