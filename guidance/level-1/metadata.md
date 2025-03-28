# Metadata Content

The first required entry to your self-assessment will be the metadata values, quick-view information about your project:

- Software — A link to the software’s repository.
- Security provider — `Yes` or `No`? Is the primary function of the project to support the security of an integrating system? 
  - Example: Your project is an authentication provider.
- Languages — Languages the project is written in.
- Software Bill of Materials (SBOM) — Link to the libraries, packages, and the versions of each that are used by the project.
  - Where practical, it is recommended to provide this in SPDX or CycloneDX format. If attached to a release, provide an example path, using `{version}` to indicate that a version should be supplied to get a specific SBOM.
- Security links — List of links to existing security documentation for the project.

As usual, formatting is less important than clear communication with your stakeholders. Below is an example showing how you can organize your metadata via subheadings.

```md
## Metadata

### Software
- https://privateerproj/privateer
- https://privateerproj/privateer-sdk
- https://privateerproj/privateer-raid-wireframe

### Security Provider?

No. Privateer is designed to facilitate security or compliance validation, but it should not be considered a security provider.

### Languages

Go

### Software Bill of Materials

Known Weakness. Automated generation of each repo's SBOM is not yet complete, and should be added to the roadmap.

### Security Links

Known Weakness. Creation of a security-insights.yml should be added to the roadmap.
```

Alternate: Some projects choose to present this in a table to occupy less space at the top of the page.

The downside to this is that longer or multi-line entries will push the limits of markdown, as seen with `<br>` HTML added to the Software row in the following table. This could complicate maintainability, though likely only in a small way.

```md
## Metadata

| | |
|-----------|------|
| Software | https://privateerproj/privateer<‌br‌>https://privateerproj/privateer-sdk<‌br‌>https://privateerproj/privateer-raid-wireframe |
| Security Provider? | No. Privateer is designed to facilitate security or compliance validation, but it should not be considered a security provider. |
| Languages | Go |
| Software Bill of Materials | Known Weakness. Automated generation of each repo's SBOM is not yet complete, and should be added to the roadmap. |
| Security Links | Known Weakness. Creation of a security-insights.yml should be added to the roadmap. |
```

> [!IMPORTANT]
> Remember, we are only using Markdown as an example format. You can craft these headers and other elements using whatever tools you like. The content outlined here _is_ recommended, though.

**[> Next Up: Overview](./overview.md)**