# AI Baby Gorilla v0.3.0 — Release Notes

**Release date:** 3 September 2026  
**Release status:** Production  
**Developer:** Sydney Business Web  
**Principal designer:** Keith Rowley

## Release summary

Version 0.3.0 is the first formally documented public production release of AI Baby Gorilla.

AI Baby Gorilla provides a free, bounded assessment of the JSON-LD entity connections found on one publicly accessible webpage.

## Principal capabilities

This release:

- extracts and analyses JSON-LD from one public webpage;
- identifies entities and named relationships;
- resolves compatible repeated definitions using canonical `@id` values;
- distinguishes connected, partly connected, fragmented and isolated structures;
- detects pages with no JSON-LD or invalid JSON-LD;
- identifies unresolved same-site entity references;
- identifies conflicting definitions attached to the same canonical identifier;
- separates graph connectivity from minimum homepage identity coverage;
- checks for connected Homepage → WebSite → Business identity anchors;
- presents a selectable visual relationship map;
- provides plain-English findings, probable effects and targeted next steps; and
- offers a real 10% assessment credit without requiring an email gate.

## Safety and operational controls

Version 0.3.0 includes:

- managed human verification;
- approved-origin enforcement;
- rate limiting;
- public-target network restrictions;
- rejection of private and unsafe network destinations;
- bounded redirects;
- bounded response size;
- bounded request duration; and
- controlled diagnostic output.

## Validation

The production build passed all 43 automated tests covering:

- JSON-LD extraction and parsing;
- entity connectivity;
- homepage minimum identity calibration;
- compatible and conflicting entity definitions;
- internal and external identifier handling;
- visual relationship preservation;
- assessment-code generation and validation;
- assessment-code expiry and redemption states;
- public-target network safety;
- human-verification handling;
- origin enforcement; and
- production request boundaries.

## Known boundaries

This release analyses one page at a time. It does not prove whole-site identity consistency, external crawler retrieval, indexing, AI-platform use, citation or recommendation.

Whole-site entity analysis remains the role of Schema Gorilla.

## Public system

https://sydneybusinessweb.com.au/ai-baby-gorilla/

## Public repository scope

The GitHub and Zenodo records contain system-level documentation, citation metadata, release history and authorship information only.

Production source code, infrastructure configuration, security implementation and proprietary assessment logic are not included.

## Copyright and rights

Copyright (c) 2026 Sydney Business Web.

These textual release notes are licensed under CC BY-NC-ND 4.0. The underlying software, proprietary assessment logic, implementation methods, trademarks and visual assets remain proprietary.