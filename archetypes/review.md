---
title: "My 1st post"
date: 2020-09-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["design","architecture","code-review","business-logic"]
author: "iO"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: true
hidemeta: false
comments: false
description: "Desc Text."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: false # to disable highlightjs
disableShare: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: false
ShowPostNavLinks: false
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/<path_to_repo>/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

## Executive Summary
- What the system does, key risks, and recommended actions.

## Context & Goals
- Problem statement, constraints, SLAs/SLOs, compliance

## Architecture Overview
- Diagram and component responsibilities  
  `{{</* figure src="architecture.png" alt="Architecture" */>}}`

## Business Logic Decomposition (Top-Down)
- **Use-cases → Policies → Rules → Code paths**  
- Decision table (inputs → rules → outcomes)

## Code Review (Representative Paths)
- File/Function: rationale, complexity notes
```lang
# short snippet emphasizing the reviewed concern
```

## Findings: defect/maintainability/security
- Test coverage gaps

## Data & Control Flows
- Sequence diagrams for critical transactions

## Quality Attributes
- Performance, reliability, security, privacy, cost

## Threat Model (High-Level)
- Assets, trust boundaries, STRIDE notes, key mitigations

## Alternatives & Trade-offs
- Option A vs B vs C (pros/cons)

## Recommendations
- Refactors, tests, observability, rollout plan

## Acceptance Criteria
- What “done” looks like; measurable outcomes

## Open Questions
- Unknowns, dependencies, spikes needed