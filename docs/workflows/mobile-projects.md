---
layout: page
title: Mobile Projects
nav_order: 1
parent: Workflows
---

# Workflow: Mobile Optimization

Mobile projects have strict memory budgets. Unwanted dependencies are the #1 cause of crashes on low-end devices.

## Strategy

1. **The "Zero-Ref" Rule**:
   - Ensure your **Boot Scene** has 0 references to heavy assets.
   - Scan your `BootLauncher` prefab. It should only reference lightweight managers.

2. **UI Audit**:
   - UI Prefabs often accidentally reference 4K textures or 3D models.
   - Scan all UI Panels.
   - If a simple "Pause Menu" references the "Player Character" (for a portrait), check if it's dragging in the whole character rig + animations.

3. **Resources Folder**:
   - Anything in `Resources` is always packaged.
   - Use the Tracker to ensure prefabs in `Resources` don't pull in other massive chains of assets.
