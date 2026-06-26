# CI Windows Build Fix

**Commit:** 974fbae298dd82f31b6a5e3df6f61ffd3241fd23

## Issue
Windows CI build was failing due to stale simplexmq submodule artifacts.

## Solution
Added cleanup step to remove simplexmq source directory before build.

## Implementation
- Clean source directory between builds
- Ensure reproducible builds
- Prevent state pollution

## Impact
- More reliable Windows builds
- Faster build diagnostics
