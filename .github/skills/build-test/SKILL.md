---
name: build-test
description: Build and test BonBazaar changes with evidence before marking work complete.
---

When code changes are made:
1. Identify the smallest relevant build target.
2. Restore dependencies if needed.
3. Build.
4. Run relevant tests.
5. Capture the exact result.
6. Do not mark GREEN when build or tests were skipped.
7. Report changed files and remaining warnings.
