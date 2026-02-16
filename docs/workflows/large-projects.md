---
layout: page
title: Large Projects
nav_order: 2
parent: Workflows
---

# Workflow: Large Scale Projects

For projects with 1000+ prefabs (MMOs, Open World), scanning everything can be slow.

## Optimization Tips

1. **Use Scope**:
   - Don't scan `Project` scope unless necessary.
   - Use `Current Scene` scope to quickly check the scene you are working on.

2. **Smart Caching**:
   - The tool caches results. The first scan is slow; subsequent scans are instant.
   - **Do not clear cache** unless you've done a major git pull.

3. **Batching**:
   - Don't select 500 prefabs at once.
   - Select folder-by-folder to keep the results readable.

4. **CI/CD Integration** (Advanced):
   - You can call the API `DependencyScanner.ScanMultipleAsync` from a build script to generate a report artifact during your nightly builds.
