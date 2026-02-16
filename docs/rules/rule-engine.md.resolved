---
layout: page
title: Rule Engine & Risk
nav_order: 1
parent: Rules
---

# Rule Engine & Risk Assessment

The Prefab Dependency Tracker includes a built-in heuristic engine to assess the "Risk" of modifying or deleting a prefab.

## Risk Badges

In the **Dependency Tree View**, you will see colored badges next to grouped results. These indicate the **Dependency Count**:

| Badge | Color | Dependencies | Meaning |
|:---|:---|:---|:---|
| **Low** | Green | 0 - 2 | Safe to modify. Low impact. |
| **Med** | Yellow | 3 - 10 | Exercize caution. Used in several places. |
| **High** | Red | 10+ | **Critical Asset**. Changing this will affect many parts of your project. |

## Calculation Logic

The risk is calculated based on:
1. **Count**: Total number of unique assets referencing the target.
2. **Type**: Scene references are weighted higher than nested prefabs in some contexts (configurable in Settings).

> **Pro Tip:** Always prioritize refactoring "High Risk" assets to decouple your project.
