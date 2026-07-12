# SFC — Story First Culture

# Decision Log

**Document Version:** 0.1
**Status:** Draft
**Last Updated:** 2026-07-12

---

# 1. Purpose

This document records significant product, business, and design decisions made during the development of SFC.

Each decision should include:

* Decision ID
* Date
* Status
* Decision
* Reasoning
* Impact
* Future considerations

---

# Decision Format

Example:

```
Decision ID:

DL-XXX

Decision:

Description of the decision.

Reason:

Why this decision was made.

Impact:

What areas of the project are affected.

Status:

Approved / Under Review / Deprecated
```

---

# DL-001 — Public Identity is the Channel

**Date:** 2026-07-12

**Status:** Approved

## Decision

The primary public identity on SFC is the Channel, not the creator.

Creators exist as identifiable owners and contributors, but viewers primarily discover and interact with Channels.

## Reason

SFC is intended to function more like a publishing platform than a traditional social network.

Viewers are generally interested in the content source, topic, and publisher identity.

Example:

A viewer searching for news looks for:

```
CNN
```

not:

```
Warner Bros.
```

## Impact

* Search should prioritize Channels.
* Channel branding is important.
* Creator profiles remain secondary.
* Ownership and identity are separate concepts.

---

# DL-002 — Story-First Content Structure

**Date:** 2026-07-12

**Status:** Approved

## Decision

All SFC content is organized around stories rather than individual media objects.

The fundamental structure is:

```
Channel

    Series

        Season

            Episode

                Page

                    Story Component
```

## Reason

Existing platforms are often media-first.

SFC is designed to encourage meaningful storytelling rather than disconnected uploads.

## Impact

The platform architecture must support:

* narrative structure,
* sequential presentation,
* multimedia storytelling.

---

# DL-003 — No Anonymous Content Creators

**Date:** 2026-07-12

**Status:** Approved

## Decision

Anonymous users cannot create public content.

Creators must establish an accountable identity relationship with SFC.

## Reason

SFC prioritizes creator responsibility.

The platform aims to avoid problems associated with anonymous publishing:

* misinformation,
* irresponsible claims,
* malicious content creation.

## Impact

* User verification requirements will exist.
* Creator identity information must be protected.
* Public identity and verified identity are separate concepts.

---

# DL-004 — Creator Identity Information is Private

**Date:** 2026-07-12

**Status:** Approved

## Decision

Creator identity information collected for accountability is not publicly displayed.

## Reason

SFC requires accountability without exposing unnecessary personal information.

## Impact

The system must separate:

```
Private Creator Identity

from

Public Channel Identity
```

---

# DL-005 — Initial Channel Limit

**Date:** 2026-07-12

**Status:** Approved

## Decision

A creator may initially own up to three Channels.

Additional Channels may become available through future monetization.

## Reason

Multiple identities may be valuable, but unlimited creation creates management and quality challenges.

## Impact

The user account system must support:

* multiple Channels,
* ownership rules,
* future expansion.

---

# DL-006 — Collaboration is Future Functionality

**Date:** 2026-07-12

**Status:** Approved

## Decision

Collaborative Channels are part of the long-term vision but are not included in MVP.

## Future Examples

* Classrooms
* Project teams
* Organizations
* Custom groups

## Reason

Collaboration introduces significant complexity:

* permissions,
* roles,
* ownership,
* access control.

## Impact

The initial design should avoid blocking future collaboration.

---

# DL-007 — Channel Transfer is Allowed

**Date:** 2026-07-12

**Status:** Approved

## Decision

Channel ownership transfer is allowed.

## Reason

The platform should support future publishing scenarios where ownership changes.

Examples:

* organizations,
* projects,
* acquired channels,
* team transitions.

## Impact

Ownership should be designed separately from creator identity.

---

# DL-008 — Channel Lifecycle States

**Date:** 2026-07-12

**Status:** Approved

## Decision

Channels have three lifecycle states:

```
Active

Archived

Deleted
```

## Reason

Deletion should not be an immediate irreversible action.

## Rules

A Channel must first be archived before deletion can occur.

Deletion requires a deliberate request.

## Impact

The system must support:

* archival,
* recovery,
* controlled deletion.

---

# DL-009 — Episode Lifecycle States

**Date:** 2026-07-12

**Status:** Approved

## Decision

Episodes use the following states:

```
Draft

Published

Deleted
```

Future states may include:

```
Archived

Scheduled
```

## Reason

The MVP requires simple publishing control while allowing future expansion.

---

# DL-010 — Logical Deletion

**Date:** 2026-07-12

**Status:** Approved

## Decision

Deleted content is not immediately destroyed.

Objects are marked deleted and moved to a separate recovery area.

## Reason

Creators need protection against accidental deletion.

## Impact

Deleted content can potentially be restored.

---

# DL-011 — Visibility Hierarchy

**Date:** 2026-07-12

**Status:** Approved

## Decision

Visibility levels are:

Highest visibility:

```
Public
```

↓

```
Restricted
```

↓

```
Private
```

## Rule

A child object may have the same visibility as its parent or a higher visibility level.

A child may never have lower visibility than its parent.

## Example

Valid:

```
Series:
Restricted

Episode:
Public
```

Invalid:

```
Series:
Public

Episode:
Restricted
```

---

# DL-012 — Seasons are Optional

**Date:** 2026-07-12

**Status:** Approved

## Decision

Series may contain Seasons, but Seasons are optional.

Episodes may exist directly under a Series.

## Reason

Different stories have different organizational needs.

---

# DL-013 — Published Content Requirements

**Date:** 2026-07-12

**Status:** Approved

## Decision

A Channel, Series, Season, or Episode must contain at least one published Page before becoming visible/searchable.

## Reason

Empty structures do not represent meaningful published content.

---

# DL-014 — Page-Based Storytelling

**Date:** 2026-07-12

**Status:** Approved

## Decision

Episodes are composed of Pages.

Pages are the primary storytelling units.

## Reason

The format combines:

* comics,
* presentations,
* multimedia storytelling.

---

# DL-015 — Maximum Pages Per Episode

**Date:** 2026-07-12

**Status:** Initial Decision

## Decision

Maximum Pages:

```
100
```

Configurable in future.

## Reason

Provides reasonable MVP limits while allowing flexibility.

---

# DL-016 — Maximum Media Components Per Page

**Date:** 2026-07-12

**Status:** Initial Decision

## Decision

Maximum Story Components per Page:

```
500
```

Configurable.

## Reason

Supports single-page complex experiences while allowing system protection.

---

# DL-017 — Responsive Canvas Design

**Date:** 2026-07-12

**Status:** Approved

## Decision

SFC uses a responsive canvas model.

Creators design within a defined canvas.

Viewers see the canvas scaled to their device while preserving proportions.

## Reason

This preserves creator intent across:

* desktop,
* tablet,
* mobile.

---

# DL-018 — Playback Uses Defined Timelines

**Date:** 2026-07-12

**Status:** Approved

## Decision

Playback behavior is defined by creator-controlled timing parameters.

Components may define:

* order,
* start time,
* duration,
* overlap,
* effects.

## Reason

SFC storytelling depends on controlled presentation.

---

# DL-019 — Published Editing Uses Revisions

**Date:** 2026-07-12

**Status:** Approved

## Decision

Editing published content creates a new revision.

Publishing the revision replaces the current published version.

MVP does not maintain full revision history.

## Reason

Provides editing flexibility without unnecessary MVP complexity.

---

# DL-020 — Deleted Pages in Published Episodes

**Date:** 2026-07-12

**Status:** Approved

## Decision

Deleted Pages in published Episodes are automatically skipped during playback.

## Reason

Avoids breaking published content flow.

---

# Summary

The initial SFC design decisions establish:

* a publishing-oriented identity,
* structured storytelling,
* creator accountability,
* flexible visibility,
* controlled publishing,
* multimedia storytelling,
* future scalability.

These decisions form the foundation for the Domain Model and MVP Functional Specification.

---

**End of Document — Decision Log v0.1**

---

