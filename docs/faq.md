---
layout: page
title: FAQ
nav_order: 10
---

# Frequently Asked Questions

## General

**Q: Does this modify my assets?**
A: **No.** The scanning process is read-only. It only reads dependencies using `AssetDatabase`.

**Q: Can I delete prefabs directly from the tool?**
A: Currently, no. We prioritize safety. We verify it's unused, but you must delete it manually in the Project View.

**Q: Does it support Addressables?**
A: It detects direct references. Use of `AssetReference` class is detected as a script reference. String-based addressing is **not** detected (as it is runtime only).

## Troubleshooting

**Q: The scan says "Safe to delete" but my code uses `Resources.Load("MyPrefab")`.**
A: **Warning:** The tool cannot find dependencies referenced only by **String**. If you use `Resources.Load`, `AssetBundle.Load`, or Reflection to load assets, the tool will not know about it. Always verify code usage for "Magic Strings".

**Q: The window is blank.**
A: Try clicking "Refresh" in the top toolbar to reload the asset list.
