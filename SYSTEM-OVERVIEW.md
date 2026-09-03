# AI Baby Gorilla — System Overview

## Document status

**System version:** 0.3.0  
**Document date:** 3 September 2026  
**Developer:** Sydney Business Web  
**Principal designer:** Keith Rowley

## Purpose

AI Baby Gorilla is a bounded one-page diagnostic system that examines whether the JSON-LD entities described on a public webpage form a coherent machine-readable identity graph.

The system was created to address a limitation of conventional structured-data testing:

> JSON-LD can be syntactically valid while the entities it describes remain incomplete, fragmented, duplicated or disconnected.

AI Baby Gorilla therefore evaluates entity relationships and identity structure rather than awarding a generic schema score.

## Core diagnostic question

The system asks:

> Do the structured entities on this public webpage connect into a coherent identity graph?

For a homepage, it asks an additional question:

> Does the graph contain the minimum connected Homepage → WebSite → Business identity route?

Graph connectivity and identity completeness are reported separately. A connected graph may still lack the minimum identity anchors expected from a business homepage.

## Conceptual processing model

AI Baby Gorilla performs the following high-level stages:

1. **Public-page retrieval**  
   Retrieves one publicly accessible HTTP or HTTPS webpage within defined operational limits.

2. **JSON-LD extraction**  
   Locates structured-data scripts and parses valid JSON-LD without exposing malformed source content in diagnostic responses.

3. **Entity normalisation**  
   Identifies described entities, canonical identifiers, embedded objects and repeated definitions.

4. **Relationship construction**  
   Converts named references and embedded relationships into a navigable entity graph.

5. **Identity resolution**  
   Resolves compatible definitions that share a canonical `@id` while retaining evidence of conflicting definitions.

6. **Topology analysis**  
   Examines connected components, isolated entities, relationship paths and unresolved same-site references.

7. **Minimum identity assessment**  
   For homepages, checks for stable business, website and homepage entities and a connected route between them.

8. **Human-readable reporting**  
   Produces a bounded explanation of what is present, what may be missing and the probable machine-readable effect.

## Diagnostic outputs

A completed assessment may report:

- the number of JSON-LD blocks detected;
- the number of identifiable entities;
- the number of named relationships;
- connected and isolated graph components;
- principal entity types;
- canonical identifier advisories;
- conflicting entity definitions;
- unresolved internal references;
- minimum homepage identity coverage;
- signals requiring human review; and
- targeted next steps.

The visual graph is explanatory. It preserves relevant relationship paths around findings instead of displaying disconnected warnings without context.

## Result classifications

### Connected

The principal structured entities form one coherent on-page graph. This indicates useful entity connectivity but does not, by itself, prove that the identities are complete or reused consistently elsewhere on the website.

### Partly connected

Meaningful relationships exist, but one or more important entities remain outside the principal graph or lack adequate identity connections.

### Fragmented

Multiple disconnected or competing identity groups are present. Individually valid schema blocks may therefore fail to resolve into one coherent representation.

### Isolated

A key entity is described without sufficient relationships to connect it meaningfully to the page, website, business or other relevant entities.

### No JSON-LD

No JSON-LD structured data was detected on the retrieved page.

### Invalid JSON-LD

One or more structured-data blocks could not be parsed safely. Invalid source content is not reproduced in the public diagnostic result.

## Homepage minimum identity model

For a business homepage, AI Baby Gorilla looks for three stable identity anchors:

1. a business entity with a stable canonical identifier;
2. a `WebSite` entity with a stable canonical identifier; and
3. a homepage `WebPage` entity with a stable canonical identifier.

It then examines whether a coherent relationship route connects:

**Homepage → WebSite → Business**

This is a minimum structural model, not a complete prescription for every organisation or website.

## Operational safeguards

The public service incorporates bounded retrieval and abuse controls, including:

- public HTTP and HTTPS targets only;
- rejection of private, loopback, link-local and otherwise unsuitable network targets;
- controlled redirects, response size and processing duration;
- human-verification controls;
- approved browser-origin controls;
- rate limiting; and
- bounded diagnostic responses.

Detailed production implementation and security configuration remain proprietary.

## Interpretation boundaries

AI Baby Gorilla does not claim to measure every component of AI visibility.

It does not prove that:

- a search engine has indexed the page;
- an AI crawler has retrieved the page;
- an external platform has parsed or retained the structured data;
- the business will be mentioned, cited or recommended;
- the same identities are used coherently across the entire website; or
- a particular rich result will be awarded.

These are separate questions requiring different evidence.

## Relationship to other testing tools

Schema.org validators answer whether structured data follows the relevant vocabulary and syntax.

Rich-result testing examines whether a page may qualify for supported search features.

AI Baby Gorilla examines whether the entities on one page form a connected and minimally coherent identity structure.

These functions are complementary rather than interchangeable.

## Relationship to Schema Gorilla

AI Baby Gorilla is the junior one-page companion to Schema Gorilla.

AI Baby Gorilla examines the entity topology of one public page. Schema Gorilla performs a comprehensive whole-site analysis to determine whether identities, relationships and references across many pages resolve into one coherent business system.

## Public access

https://sydneybusinessweb.com.au/ai-baby-gorilla/

## Ownership and documentation licence

AI Baby Gorilla was designed by Keith Rowley and developed by Sydney Business Web.

Copyright © 2026 Sydney Business Web.

This textual system overview is licensed under CC BY-NC-ND 4.0. The underlying software, source code, assessment logic, implementation methods, trademarks and visual assets remain proprietary and are not licensed by this document.