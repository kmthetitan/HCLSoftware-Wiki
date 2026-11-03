# Development and Testing

## Editing

- Use Volt Iris / Volt MX tooling for forms, project resources, and app builds.
- Keep screen logic in the matching controller group under `controllers/`.
- Check both the form definition and controller when changing a screen; the form defines the UI while its controller handles event behavior.
- Keep platform-specific code in the appropriate platform folder where required.
- Avoid editing bundled SDK or vendor files under `resources/customlibs/` unless the change specifically requires it.
- If changing backend-dependent behavior, review the corresponding assets under `Fabric/Apps/` and test with the intended Fabric environment.

## Tests

The repository includes Jasmine scaffolding at `testresources/Jasmine/`, with test plans for Mobile, Tablet, and Desktop and a shared reporter in `Common/`. Review the test plan and configure it in the Volt Iris test runner for your target platform.

No conventional package-based test command is defined in this project export. The presence of test plans does not guarantee that all feature flows have automated coverage.

## Headless builds

`HeadlessBuild.properties` documents the Volt MX headless build settings. Its defaults use build mode `0` and have platform targets disabled. Before running a headless build, use the build tooling documented for your Volt MX installation and configure the required platform flags and environment-specific values. Do not store Fabric passwords, tokens, signing credentials, or other secrets in committed project files.

## GitHub Wiki publishing

GitHub Wikis are stored separately from the main source repository. These Markdown files are formatted as wiki pages (`Home.md`, page files, and `_Sidebar.md`). To publish them, clone the wiki repository for the project, copy these page files into it, and push using an authorized GitHub account. The project checkout available while these pages were prepared did not include a Git remote or GitHub authentication.

