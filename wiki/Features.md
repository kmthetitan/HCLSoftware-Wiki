# Features

This page maps the main user-facing areas to their controller locations. The project contains a mix of implemented UI logic, mock data, and backend placeholders; inspect the relevant controller and Fabric configuration to determine the runtime behavior of a specific path.

| Feature area | Controller location | Notes |
|---|---|---|
| Startup and dashboard | `controllers/mobile/grpStartup/` | Startup/dashboard screen controllers |
| Sign-in | `controllers/mobile/FormSignInController/`, `controllers/mobile/frmLoginController/` | Sign-in related controller assets |
| Government services | `controllers/mobile/grpGovServ/` | Separate service-category screen controllers, including health, education, transport, business, tax, immigration, legal, utilities, and social services |
| Documents | `controllers/mobile/grpDocs/` | Document list, upload, and viewer flows; document list includes mock data |
| Family | `controllers/mobile/grpFam/` | Family members, adding a member, and permissions |
| Notifications | `controllers/mobile/grpNotifs/` | Notification list and detail screens |
| Profile and payments | `controllers/mobile/grpUserserv/` | Profile, payment, and payment history controllers |

## Document flow

Document controller assets cover browsing, upload, and viewing. The upload controller contains a simulated upload path as well as an HTTP-request implementation path. File selection, camera access, and upload behavior depend on the target platform and runtime configuration.

## Family flow

Family controllers cover the family view, adding members, and member permissions. Some controllers contain HTTP request code; confirm the configured service endpoint and identity token handling in the environment where the app is run.

## Payments

Payment and payment-history controllers are present in `grpUserserv`. Validate any payment behavior against the actual target environment; a UI flow or simulated response should not be treated as a live payment integration.

