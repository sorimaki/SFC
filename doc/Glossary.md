# SFC — Story First Culture

# Glossary

**Document Version:** 0.1
**Status:** Draft
**Last Updated:** 2026-07-12

---

# 1. Purpose

This document defines terminology used throughout the SFC specification library.

The purpose is to establish a shared vocabulary for:

* product discussions,
* requirements,
* design decisions,
* development,
* testing,
* and future collaboration.

---

# 2. Core Concepts

---

# Account

## Definition

An authenticated identity registered with SFC.

An Account represents a person or entity authorized to create and manage content.

## Notes

An Account is not necessarily the public identity shown to viewers.

The Account exists primarily for:

* authentication,
* ownership,
* permissions,
* accountability.

---

# Creator

## Definition

The person or entity responsible for creating content on SFC.

## Notes

The Creator is associated with one or more Channels.

The Creator is a public identity, but is secondary to the Channel identity.

---

# Channel

## Definition

The primary public identity and publishing entity on SFC.

A Channel represents the publisher of content.

## Example

A creator may own:

```text
Creator:
John Smith

Channels:

- Backyard Woodworking
- Mediterranean Travel Stories
- Science Explained
```

## Notes

Viewers primarily discover and follow Channels rather than individual creators.

A Channel may represent:

* an individual creator,
* a brand,
* a project,
* an organization,
* or a future collaborative entity.

---

# Publisher

## Definition

The entity responsible for presenting content to the public.

## SFC Usage

The Channel acts as the publisher.

## Example

A viewer looking for news searches for:

```text
CNN
```

rather than:

```text
Warner Bros.
```

The publisher identity is what matters to the viewer.

---

# Series

## Definition

A collection of related Episodes organized around a common theme, topic, or story.

## Examples

```text
Series:
Building My Sailboat

Series:
My Trip Through Europe

Series:
Physics Explained
```

## Notes

A Series may initially exist without Episodes.

A Series cannot become publicly available until it contains valid published content.

---

# Season

## Definition

An optional organizational layer grouping Episodes within a Series.

## Example

```text
Series:
Building My Sailboat

Season 1:
Design

Season 2:
Construction

Season 3:
Testing
```

## Notes

Seasons are optional.

Episodes may exist directly under a Series.

---

# Episode

## Definition

A complete story segment within a Series.

An Episode consists of one or more Pages.

## Notes

An Episode requires:

* Page 1
* Page 1 published

before it can be published.

---

# Page

## Definition

A single storytelling scene within an Episode.

A Page combines:

* visual composition,
* media components,
* text,
* timing,
* playback behavior.

## Notes

A Page is not simply a document page.

It is a multimedia storytelling scene.

---

# Virtual Stage

## Definition

The visual composition area where Story Components are placed.

The Virtual Stage defines:

* canvas size,
* orientation,
* component positions,
* visual arrangement.

## Notes

The Virtual Stage preserves creator intent.

The viewer sees a scaled version of the stage adapted to their device.

---

# Story Component

## Definition

An individual element placed on a Page.

## Types

MVP components include:

### Media Components

* Photo
* GIF
* Video
* Audio

### Text Components

* Text boxes

## Notes

Each component has:

* position,
* size,
* timing,
* playback rules,
* effects.

---

# Media Component

## Definition

A Story Component containing a media asset.

Examples:

* image,
* video,
* GIF,
* audio.

---

# Text Component

## Definition

A Story Component containing editable text.

## Notes

Text Components may support:

* fonts,
* size,
* color,
* effects.

---

# Canvas

## Definition

The logical visual space used to design a Page.

## Notes

The Canvas is independent from the viewer's device.

It is scaled proportionally during viewing.

---

# Timeline

## Definition

The time-based definition controlling how Story Components behave during playback.

## Defines

* start time,
* duration,
* sequence,
* overlap,
* effects.

---

# Playback

## Definition

The process of presenting an Episode or Page automatically according to its defined timeline.

## Types

### Episode Playback

Plays all Pages sequentially.

### Page Playback

Plays the current Page.

### Component Playback

Plays an individual Story Component.

---

# Revision

## Definition

A temporary editable version of published content.

## Notes

Editing published content creates a Revision.

When published:

* the Revision replaces the current published version,
* previous history is not retained in MVP.

---

# Visibility

## Definition

The level of public accessibility assigned to content.

## Visibility Levels

Highest visibility:

```text
Public
```

↓

```text
Restricted
```

↓

```text
Private
```

## Rule

A child object may have the same visibility as its parent or a higher visibility level.

A child may never have lower visibility than its parent.

Example:

Valid:

```text
Series:
Restricted

Episode:
Public
```

Invalid:

```text
Series:
Public

Episode:
Restricted
```

---

# Lifecycle Status

## Definition

The current operational state of an object.

Examples:

Channel:

```text
Active
Archived
Deleted
```

Episode:

```text
Draft
Published
Deleted
```

Future possibilities:

```text
Scheduled
Archived
```

---

# Archived

## Definition

A state where content is no longer actively published but has not been permanently deleted.

## Notes

Archiving is intended to be a reversible action.

---

# Deleted

## Definition

A state where content has been removed from normal use.

## Notes

MVP deletion is logical deletion.

Deleted objects are retained separately and may be restored.

---

# Published

## Definition

Content that is available to viewers according to its visibility settings.

---

# Draft

## Definition

Content that exists but is not available to viewers.

Draft content may be edited.

---

# Restricted Content

## Definition

Content that is visible as existing but requires specific permissions to access.

Examples:

* paid content,
* group access,
* classroom access.

---

# Private Content

## Definition

Content accessible only to specifically authorized users.

Examples:

* family sharing,
* personal projects,
* private groups.

---

# Story-First

## Definition

The core SFC philosophy that storytelling purpose precedes media selection.

---

# Summary

The SFC vocabulary establishes the foundation for describing:

* creators,
* publishers,
* stories,
* content structures,
* editing,
* playback,
* and visibility.

Future documents should use these terms consistently.

---

**End of Document — Glossary v0.1**

---
