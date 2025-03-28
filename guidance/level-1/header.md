# Header Content

Let's kick things off by putting in some basic information about the project and the assessment itself.

> [!IMPORTANT]
> Remember, we are only using Markdown as an example format. You can craft these headers and other elements using whatever tools you like. The content outlined here _is_ recommended, though.

## Header

Let's open up the document with some very basic details.

### Introdcution

Your document title will simply be your project’s name followed by “Self-Assessment”.

We used `#` to make this a top level header (H1).

Use plaintext below the title to specify who did this assessment and who the project maintainers are. In the example below, we are using a project which the security reviewer is a maintainer on.

You may want to add a single sentence here explaining the motivation behind this self-assessment, but don’t bother adding anything if you don’t have something valuable for readers—this section should be very light.

In this example, we are leaving a note for readers to warn readers that we may not keep the document up to date over time.

Markdown:

```md
# Privateer Self-Assessment

Security reviewers: Eddie Knight

Project Maintainers: Eddie Knight, Jason Meridth

This document is intended to aid in roadmapping, and the onboarding of new maintainers. This document is used for planning purposes, and may quickly go out of date due to ongoing development. Please contact a maintainer to verify the accuracy prior to making decisions using this self-assessment.
```

### Table of Contents

If you’re using something like Google Docs or Microsoft Word, you can auto-generate a table of contents.

In Markdown, we can add self-referencing links to our document—these will be functional once we actually create the associated entries.

We may also need to come back and modify this after we’ve added our content. If you decide to create subsections for a complex topic, be sure to add those to the table of contents here.

```md
## Table of Contents

* [Metadata](#metadata)
  * [Security links](#security-links)
* [Overview](#overview)
  * [Actors](#actors)
  * [Actions](#actions)
  * [Background](#background)
  * [Goals](#goals)
  * [Non-goals](#non-goals)
* [Self-assessment use](#self-assessment-use)
* [Security functions and features](#security-functions-and-features)
* [Project compliance](#project-compliance)
* [Secure development practices](#secure-development-practices)
* [Security issue resolution](#security-issue-resolution)
* [Appendix](#appendix)
```

## Self-Assessment Use

The "Self-Assessment Use" section helps readers understand what your intent was when you created the document. Try to give as much detail as possible about the background and motivation behind the effort, and what you expect readers to use it for.

In the example below, we only slightly adjusted the CNCF boiler-plate text to create content for this section.

Markdown:

```md
### Self-assessment Use

This self-assessment is created by the Privateer team to perform an internal analysis of the project's security. It is not intended to provide a security audit of Privateer, or function as an independent assessment or attestation of Privateer's security health.

This document serves to provide Privateer users with an initial understanding of Privateer's security, where to find existing security documentation, Privateer plans for security, and general overview of Privateer security practices, both for development of Privateer as well as security of Privateer.

This document provides Privateer maintainers and stakeholders with additional context to help inform the roadmap creation process, so that security and feature improvements can be prioritized accordingly.
```

**[> Next Up: Metadata](./metadata.md)**
