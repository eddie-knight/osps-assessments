# Self-assessment

Maintainers: John Smith

Security reviewers: Arthur Williams

This self-assessment is created by the [project] team to perform an internal analysis of the
project's security.  It is not intended to provide a security audit of [project], or
function as an independent assessment or attestation of [project]'s security health.

This document serves to provide [project] users with an initial understanding of
[project]'s security, where to find existing security documentation, [project] plans for
security, and general overview of [project] security practices, both for development of
[project] as well as security of [project].

This document provides the CNCF TAG-Security with an initial understanding of [project]
to assist in a joint-assessment, necessary for projects under incubation.  Taken
together, this document and the joint-assessment serve as a cornerstone for if and when
[project] seeks graduation and is preparing for a security audit.

## Table of Contents

- [Metadata](#metadata)
- [Project Overview](#project-overview)
  - [Background](#background)
  - [Security Goals](#security-goals)
  - [Security Non-goals](#security-non-goals)
- [System Design](#system-design)
  - [Actors](#actors)
  - [Actions](#actions)
  - [Security functions and features](#security-functions-and-features)
- [Development & Support](#development--support)
- [Appendix](#appendix)

## Metadata

- **Assessment Stage:** Incomplete, Complete, or Obsolete. Status of this file may change over time.
- **Software:** A link to the software’s repository.
- **Security Provider:** Yes or No. Is the primary function of the project to support the security of an integrating system?
- **Languages:** Language(s) the project is written in.
- **SBOM:** Software bill of materials.  Link to the libraries, packages, versions used by the project, may also include direct dependencies.
- **Compliance:**  List of any security standards or sub-sections the project is already documented as meeting (PCI-DSS, COBIT, ISO, GDPR, etc.).
- **Security links:** List of links to existing security documentation for the project. At minimum, include a link to the project security-insights.yaml.

## Project Overview

One or two sentences describing the project -- something memorable and clear
that distinguishes your project to quickly orient readers who may be assessing
multiple projects.

### Background

Provide information for reviewers who may not be familiar with your project's
domain or problem area. This should include what pain point you are solving,
how you are solving it, and who a typical user might be.

### Security Goals

The intended goals of the projects including the security guarantees the project
is meant to provide (e.g., Flibble only allows parties with an authorization
key to change data it stores).

### Security Non-goals

Non-goals that a reasonable reader of the project’s literature could believe may
be in scope (e.g., Flibble does not intend to stop a party with a key from storing
an arbitrarily large amount of data, possibly incurring financial cost or overwhelming
the servers)

## System Design

This section provides an overview of the system and it's distinct parts.

### Actors

These are the individual parts of your system that interact to provide the
desired functionality.  Actors only need to be separate, if they are isolated
in some way.  For example, if a service has a database and a front-end API, but
if a vulnerability in either one would compromise the other, then the distinction
between the database and front-end is not relevant.

The means by which actors are isolated should also be described, as this is often
what prevents an attacker from moving laterally after a compromise.

### Actions

These are the steps that a project performs in order to provide some service
or functionality.  These steps are performed by different actors in the system.
Note, that an action need not be overly descriptive at the function call level.
It is sufficient to focus on the security checks performed, use of sensitive
data, and interactions between actors to perform an action.

For example, the access server receives the client request, checks the format,
validates that the request corresponds to a file the client is authorized to
access, and then returns a token to the client.  The client then transmits that
token to the file server, which, after confirming its validity, returns the file.

### Security functions and features

- Critical.  A listing critical security components of the project with a brief
description of their importance.  It is recommended these be used for threat modeling.
These are considered critical design elements that make the product itself secure and
are not configurable.  Projects are encouraged to track these as primary impact items
for changes to the project.
- Security Relevant.  A listing of security relevant components of the project with
  brief description.  These are considered important to enhance the overall security of
the project, such as deployment configurations, settings, etc.  These should also be
included in threat modeling.

## Development & Support

- **Development Pipeline:**  A description of the testing and assessment processes that
  the software undergoes as it is developed and built. Be sure to include specific
information such as if contributors are required to sign commits, if any container
images immutable and signed, how many reviewers before merging, any automated checks for
vulnerabilities, etc.
- **Communication Channels:** Reference where you document how to reach your team or
  describe in corresponding section.
  - Internal. How do team members communicate with each other?
  - Inbound. How do users or prospective users communicate with the team?
  - Outbound. How do you communicate with your users? (e.g. flibble-announce@
    mailing list)
- **Ecosystem:** How does your software fit into the cloud native ecosystem?  (e.g.
  Flibber is integrated with both Flocker and Noodles which covers
virtualization for 80% of cloud users. So, our small number of "users" actually
represents very wide usage across the ecosystem since every virtual instance uses
Flibber encryption by default.)
- **Responsible Disclosures Process:** A outline of the project's responsible
  disclosures process should suspected security issues, incidents, or
vulnerabilities be discovered both external and internal to the project. The
outline should discuss communication methods/strategies.
  - Vulnerability Response Process. Who is responsible for responding to a
    report. What is the reporting process? How would you respond?
- **Incident Response:** A description of the defined procedures for triage,
  confirmation, notification of vulnerability or security incident, and
patching/update availability.

## Appendix

Provide links to helpful external references.

Here are some recommended items to include in the appendix:

- Known Issues Over Time. List or summarize statistics of past vulnerabilities
  with links. If none have been reported, provide data, if any, about your track
record in catching issues in code review or automated testing.
- [Open SSF Best Practices](https://www.bestpractices.dev/en).
  Best Practices. A brief discussion of where the project is at
  with respect to CII best practices and what it would need to
  achieve the badge.
- Case Studies. Provide context for reviewers by detailing 2-3 scenarios of
  real-world use cases.
- Related Projects / Vendors. Reflect on times prospective users have asked
  about the differences between your project and projectX. Reviewers will have
the same question.
