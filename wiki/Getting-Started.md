# Getting Started

## Requirements

- HCL Volt Iris / Volt MX Studio compatible with this project export. Project properties identify Volt Iris `10.0.5.0` and Volt MX `10.0.7.0`.
- Access to any required Volt MX Fabric environment and credentials if you intend to publish or exercise backend-dependent flows.
- A configured mobile build target/device for running the application.

This project does not include a conventional Node package manifest or a generic `npm install` / `npm start` workflow. Use Volt Iris to import and build the project.

## Open the project

1. Open Volt Iris and use its project import/open workflow to load the `SmartGov` project directory.
2. Review the project configuration and select the target platform(s) supported by your Volt Iris installation.
3. Configure the Fabric environment and services before testing backend-dependent operations.
4. Build and run the app from Volt Iris on an emulator or device.

The project also includes `HeadlessBuild.properties` for the Volt MX headless build process. Its checked-in defaults select build mode `0` and disable all listed platform targets. Set up the environment-specific build properties in your local environment before attempting a headless build or publish. Do not commit credentials or tokens.

## First screens to explore

- Startup and sign-in controllers: `controllers/mobile/grpStartup/` and `controllers/mobile/FormSignInController/`
- Document flows: `controllers/mobile/grpDocs/`
- Family flows: `controllers/mobile/grpFam/`
- Government service navigation: `controllers/mobile/grpGovServ/`
- Notifications: `controllers/mobile/grpNotifs/`
- Payments, history, and profile: `controllers/mobile/grpUserserv/`

See [[Architecture]] for how these assets fit together and [[Development-and-Testing|Development and Testing]] for test scaffolding.
