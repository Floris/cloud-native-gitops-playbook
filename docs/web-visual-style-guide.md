# Shared Web Visual Style Guide

## Goal

This document defines the default visual system that Floris-managed websites should follow so the portfolio feels recognizably related across domains.

The current reference implementation is `json.droppert.dev`. New websites and redesign work should inherit this direction unless there is a clear product reason to diverge.

## Scope

This is a house style, not a universal design rule.

Apply it by default to:

- `florisdroppert.com`
- `treppord.com`
- `json.droppert.dev`
- future portfolio or product sites in the same ecosystem

## Source of visual truth

Use `droppert-platform/apps/json` as the primary implementation reference for:

- color mood
- typography pairing
- panel styling
- spacing density
- button treatment
- code or data presentation

When a design decision is ambiguous, prefer matching the JSON project over inventing a new visual language.

## Design intent

The visual identity should feel:

- technical but polished
- premium without feeling corporate
- calm, focused, and slightly futuristic
- clear enough for utility tools and strong enough for portfolio storytelling

Avoid generic startup UI patterns that make each site feel unrelated.

## Core visual language

### Color model

The baseline palette uses:

- deep navy and blue backgrounds
- cooler mid-tones for structure
- soft mint green as the primary accent
- pale, high-contrast text
- translucent white layers for glass surfaces

This palette creates a night-shift, studio-like atmosphere. Bright white backgrounds should not become the default.

### Surfaces

Prefer layered translucent panels over flat cards.

Base treatment:

- soft gradient page background
- radial glow accents in the canvas
- glass-like panels with blur and subtle border definition
- large radii with generous breathing room
- elevated shadows that feel atmospheric rather than heavy

### Typography

Default type pairing:

- primary display and interface font: `Space Grotesk`
- technical or structured data font: `IBM Plex Mono`

Rules:

- use strong, compact headlines
- keep body copy readable and relaxed
- use mono type for code, metrics, payloads, or machine-readable values
- do not switch font families per site without a deliberate brand exception

### Shape and spacing

The system should feel rounded, spacious, and intentional.

Defaults:

- large panel radius
- medium-to-large control radius
- clear vertical rhythm
- dense information grouped inside spacious containers

Avoid cramped layouts, tiny border radii, or overly sharp enterprise styling.

## Standard components

### Hero sections

Use a hero block with:

- a small uppercase eyebrow
- a short, decisive headline
- one supporting paragraph
- optional metadata pills or quick facts

Hero copy should be concise and high signal. Do not overload the top of the page.

### Panels and cards

Use two levels of surfaces:

- primary glass panel for major page regions
- secondary glass card for nested content blocks

This creates continuity across landing pages, tools, and content pages.

### Buttons

Button hierarchy:

- primary actions use the mint accent gradient
- secondary actions use translucent neutral surfaces
- ghost or subtle actions are quiet but still belong to the same system

Buttons should feel tactile through hover lift, border emphasis, and small motion.

### Data and code blocks

Whenever a site contains technical output, structured content, examples, or config:

- use `IBM Plex Mono`
- place content inside dark translucent containers
- preserve syntax-aware accent colors when helpful
- keep line height generous enough for scanning

## Layout principles

- Use one dominant content shell per page.
- Constrain width so pages feel authored rather than stretched.
- Combine editorial hierarchy with product utility patterns.
- Use asymmetry carefully, but keep alignment disciplined.
- Collapse to a simple single-column layout on smaller screens.

## Interaction principles

- Motion should be subtle and meaningful.
- Hover states may lift or brighten slightly.
- Do not use playful motion that conflicts with the calm technical tone.
- Feedback states should be immediate and readable.
- Accessibility wins over visual novelty.

## Responsive behavior

Every site should remain coherent on mobile.

Minimum expectations:

- hero stacks vertically on narrower screens
- utility bars wrap cleanly
- textareas, code areas, and cards reduce height responsibly
- spacing tightens without losing the design language

## AI implementation rules

When an AI system is asked to build or restyle a site in this ecosystem, it should:

1. Start from the `json.droppert.dev` visual language.
2. Reuse the shared tokens from `templates/web-style-system/base/tokens.css` when possible.
3. Preserve the `Space Grotesk` plus `IBM Plex Mono` pairing unless instructed otherwise.
4. Prefer deep gradient backgrounds and glass surfaces over plain white sections.
5. Keep mint green as the default accent family.
6. Use rounded geometry and atmospheric shadowing.
7. Keep interactions understated and professional.
8. Treat this style guide as the default for new pages, components, and redesign work.

## Allowed variation

Variation is encouraged in content and composition, but not in core identity.

Safe areas to vary:

- hero messaging
- page-specific illustrations or diagrams
- information architecture
- component density depending on the product

Areas that should stay consistent:

- overall color mood
- primary typography pairing
- glass-panel treatment
- button hierarchy
- spacing philosophy

## When to create a separate brand direction

A separate design direction is justified only when:

- the site serves a meaningfully different audience
- the product needs a different trust signal
- there is a business or brand reason to separate it from the portfolio family

If that happens, document the exception explicitly instead of drifting away from the baseline over time.
