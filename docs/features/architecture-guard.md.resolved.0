---
layout: page
title: Architecture Guard
nav_order: 3
parent: Features
---

# Architecture Guard
{: .label .label-purple }

> **Planned Feature:** This feature is part of the upcoming v2.0 roadmap.

Architecture Guard helps you enforce strict dependency rules based on your project structure.

## The Problem
In a well-structured project, your **UI** layer shouldn't reference **Gameplay** logic directly, or your **Core** systems shouldn't depend on specific **Level** assets.

## The Solution
Define rules in a `ArchitectureRules.json` file (coming soon):

```json
{
  "rules": [
    {
      "from": "Assets/Core",
      "cannot_reference": "Assets/Gameplay"
    }
  ]
}
```

The scanner will flag any usage that violates these rules, keeping your architecture clean and loosely coupled.
