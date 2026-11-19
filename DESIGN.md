---
version: alpha
colors:
  civic-ink: "#29163D"
  action-violet: "#A64DFF"
  action-violet-dark: "#5F1AA8"
  supporting-purple: "#7C3AED"
  urgency-orange: "#F59E0B"
  success-green: "#15803D"
  danger-red: "#DC2626"
  city-canvas: "#F8F3FF"
  surface: "#FFFFFF"
  body-text: "#342246"
  muted-text: "#756784"
  boundary: "#E4D4F5"
typography:
  display:
    fontFamily: "Space Grotesk, sans-serif"
  body:
    fontFamily: "Inter, sans-serif"
  data:
    fontFamily: "IBM Plex Mono, monospace"
rounded:
  control: "6px"
  card: "12px"
  pill: "999px"
spacing:
  compact: "8px"
  default: "16px"
  section: "32px"
components:
  button:
    radius: "6px"
  card:
    radius: "12px"
  focus:
    color: "#A64DFF"
---

## Overview

NagaraSetu is a civic operations product for residents, municipal officers, and city administrators. It should feel like an illuminated civic coordination map: calm, precise, approachable, and easy to scan. White service surfaces, a quiet lilac map grid, and a distinctive `#A64DFF` signal are the signature elements. Avoid generic neon dashboards, decorative purple clutter, glassmorphism, and ceremonial government ornament.

## Colors

Violet `#A64DFF` owns brand highlights and focus, while deeper purple provides accessible primary-action and navigation contrast. Amber marks hazards and priority but is not general decoration. Green remains reserved for confirmed resolution, while red is reserved for danger and destructive actions. White surfaces sit on a pale lilac city canvas with soft purple boundaries so dense civic information stays bright and readable.

## Typography

Space Grotesk carries concise headings and civic identity, Inter carries interface copy, and IBM Plex Mono carries issue IDs and operational data. Labels are direct and sentence case unless they are short operational eyebrows.

## Layout

The landing page uses a wide editorial hero paired with a live report ticket, followed by a three-step service path that explains the real handoff from resident to service team. A universal three-bar site menu groups exploration and role-based entry points, including distinct Super Admin access. Authenticated views use a stable, high-contrast sidebar and task-focused workspace panels. Cards remain scan-friendly and collapse to a single column on narrow screens. The map grid can appear only on large background surfaces.

## Elevation & Depth

Use one restrained violet-tinted shadow plus a faint purple edge for floating cards and dialogs. The landing report ticket may use a small pointer-driven 3D tilt as the signature interaction; touch and reduced-motion experiences stay stable and flat. Lists and dashboard panels rely on borders, white-to-lilac surface contrast, spacing, and type hierarchy rather than stacked shadows.

## Shapes

Controls use a 6px radius, panels use 12px, and status chips use pills. The mix echoes precise municipal signage without feeling severe.

## Components

Buttons keep their dimensions while busy and always show a visible keyboard focus ring. Native selects are intentional: platform-owned option popups are accepted. Toasts share one fixed live region. Issue category color is supplementary to text and icons.

## Do's and Don'ts

Do use exact location, service area, team, priority, and issue reference language. Do keep resident and officer actions explicit. Do not imply that AI decisions are final; officers review suggested routing and priority. Do not use color alone for status.
