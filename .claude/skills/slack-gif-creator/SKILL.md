---
name: slack-gif-creator
description: Create animated GIFs optimized for Slack messaging and emoji use cases. Provides validators, animation primitives, and helper utilities for generating GIFs within Slack's technical constraints.
---

# Slack GIF Creator

This skill provides a comprehensive toolkit for creating animated GIFs optimized for Slack messaging and emoji use cases.

## Key Constraints

**Message GIFs:**
- Max size: ~2MB
- Optimal dimensions: 480x480
- Typical FPS: 15-20

**Emoji GIFs:**
- Max size: 64KB (strict limit)
- Optimal dimensions: 128x128
- Typical FPS: 10-12

## Core Components

The toolkit offers three primary tool categories:

1. **Validators** - Functions to verify GIFs meet Slack's technical requirements

2. **Animation Primitives** - Composable motion building blocks:
   - shake, bounce, spin, pulse, fade, zoom
   - explode, wiggle, slide, flip, morph
   - and movement effects

3. **Helper Utilities** - Optional assistance with:
   - GIF assembly
   - Text rendering
   - Color management
   - Visual effects
   - Easing functions

## Design Approach

Complete creative freedom is available in how these tools are applied. Use, modify, or replace utilities as needed rather than following rigid patterns.

## Optimization for Emoji GIFs

For the strict 64KB emoji limit:
- Limit to 10-15 frames total
- Use 32-48 colors maximum
- Aggressive palette reduction
- Minimize frame differences

## Dependencies

- PIL (Pillow)
- ImageIO
- NumPy
