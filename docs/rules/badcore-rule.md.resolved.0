---
layout: page
title: Bad Core Dependencies
nav_order: 2
parent: Rules
---

# Bad Core Dependencies

A common architectural anti-pattern is having "Core" prefabs (like a Game Manager or Player) reference specific "Level" assets.

## Example

Imagine a `GameManager` prefab that holds an array of every `LevelPrefab` in the game.
- **Result**: To load the Menu, you load GameManager. GameManager loads references to Level 1, Level 2... Level 50.
- **Memory**: You effectively load the entire game into memory at start.

## Detection

Use the **Architecture Guard** (conceptually) or manual scanning to find these:
1. Scan your `GameManager`.
2. Look for references to `Assets/Levels/...`.
3. If found, **Refactor**:
   - Change the reference to `AssetReference` (Addressables).
   - Or use a `Resources.Load` path string.
