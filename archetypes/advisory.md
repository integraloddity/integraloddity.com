---
title: "My 1st post"
date: 2020-09-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["notes", "learning"]
author: "integraloddity"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
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

> **Disclosure Policy:** Coordinated disclosure with vendor; see timeline below.

## Overview
- **Identifier:** CVE-YYYY-XXXX (pending/assigned), internal ID  
- **Severity:** Critical/High/… (CVSS v3.1/4.0 base score X.Y)  
- **Attack Vector:** Network/Local/Adjacent  
- **Impact:** RCE/Privilege escalation/Info disclosure/DoS

## Affected Products / Versions
- Vendor Product ≤ vX.Y.Z on OS/arch

## Technical Details
- **Root Cause:** (e.g., unsafe deserialization, auth bypass)
- **Prerequisites:** (auth required? user interaction?)
- **Exploitability:** ease, reliability
```text
Minimal vulnerable code path or config snippet (no secrets).
```

## Mitigations
- Immediate config change / feature disable
- Network controls / WAF signature

## Fix / Patch
- Patched version(s) and links to vendor advisory

## Detection & Indicators
- Log signatures, telemetry, YARA/Sigma (if applicable)

## Risk Assessment
- Environments at highest risk and why
- Business impact

## Timeline
YYYY-MM-DD: Discovery
YYYY-MM-DD: Vendor notified
YYYY-MM-DD: Patch released
YYYY-MM-DD: Public disclosure

## Credits
Researcher(s), acknowledgements

## References
CWE(s), related advisories, commits