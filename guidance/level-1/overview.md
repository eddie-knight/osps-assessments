# Overview Content

> [!IMPORTANT]
> Remember, we are only using Markdown as an example format. You can craft these headers and other elements using whatever tools you like. The content outlined here _is_ recommended, though.

Your overview section has multiple components nested beneath it:

- Overview statement — Basically a summary of your project.
- Background — Context for why your project exists.

This information will help your stakeholders understand your project at a high level, removing the need for a variety of follow-up questions later on. This contextualization is especially important when working with a joint-reviewer or auditor.

Your overview statement is a very short explanation of what your project does. This should distinguish it from other potentially similar projects, and give an uninitiated stakeholder an easy path to understanding what they’re about to look at.

Note that this isn’t intended to sell your project, it doesn’t need to be flashy and shouldn’t contain industry jargon. Write this with your least familiar audience in mind—most likely, your third-party auditors will know little about your particular niche.

## Overview Statement

This statement is the first entry to the Overview section, and the rest will each get their own subheadings.

```md
## Overview

Privateer is a test harness that is specially designed to combine any number of validation test packs into a single runtime that will harmonize inputs, executions, and outputs. The Privateer SDK enables the creation of test plugins, nicknamed _raids_, which can be selected and executed by Privateer users one at a time or in groups.
```

## Background

We’ll use this section to provide information for reviewers who may not be familiar with your project's domain or problem area. This section can be more verbose, but try to keep it within reason! We want to communicate all of the key issues without giving the reader an excuse to skim over it.

This is a subheading, nested within the Overview section.

```md
### Background

Historically, runtime validation tests are notoriously specific to the resource they're validating. While the validators are powerful, they typically only address a single use case.

In situations where engineers need to validate a wide array of deployed resources, they must build a custom solution that incorporates the commands and configurations for each validation tool.

Privateer seeks to remediate this problem by allowing validation tests to be built as plugins which adhere to the Simplified Compliance Infrastructure model. Each plugin receive their configuration from the Privateer runtime, and subsequently pass their outputs back to Privateer for logging and writing. When multiple plugins are executed by a user, only a single config is required, all executions log together, and the output will always be provided together in a matching format.
```
