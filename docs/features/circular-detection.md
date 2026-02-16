---
layout: page
title: Circular Detection
nav_order: 2
parent: Features
---

# Circular Dependency Detection
{: .label .label-yellow }

> **Note:** This feature is currently in **Beta**.

Circular dependencies occur when **Prefab A** references **Prefab B**, and **Prefab B** references **Prefab A**. This can cause infinite loops during instantiation or serialization errors.

## How to Detect

1. Select multiple prefabs in the Left Panel.
2. Run a **Project Scope** scan.
3. Look for the **Circular Dependency Warning** in the results panel.

## Fixing Circles

To break a circular dependency:
1. Identify the "weakest link" (usually a script reference).
2. Change the reference to load dynamically (e.g., using `Resources.Load` or Addressables) instead of a hard link.
3. Re-scan to verify the cycle is broken.
