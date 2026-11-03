# Data Model

The Volt MX Fabric object-service assets under `Fabric/Apps/_ObjectServices/SmartGov/1.0/` define the application's server-side entities. Each object directory contains some combination of field metadata, CRUD mappings, relationships, and migration assets.

## Object definitions

The checked-in object-service directories include:

- `Business`
- `Education`
- `govDocs`
- `GovServiceCategory`
- `Health`
- `Immigration`
- `Legal`
- `Notifications`
- `PendingActions`
- `ServiceRequests`
- `SocialServices`
- `Tax`
- `transportLicense`
- `transportVehicle`
- `UserProfile`
- `Utility`

## Examples

- `UserProfile/Fields.json` includes a `userID` key and profile fields such as `displayName`, `email`, `phone`, `profileimageURL`, and `role`.
- `ServiceRequests/Fields.json` includes `requestID`, `userID`, `serviceName`, `serviceCategory`, `status`, `submittedDate`, and `amount`.
- The metadata includes common audit and soft-delete fields on some entities.
- MySQL migration scripts are under `Fabric/Apps/_ObjectServices/SmartGov/1.0/_Flyway/MYSQL/` and are versioned `V1` through `V21`.

These are Fabric model definitions and migration files; validate their compatibility and intended relationships against the target database before applying migrations. Do not use mock client data as authoritative schema documentation.

