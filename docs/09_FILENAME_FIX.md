# Filename Trailing Dot Fix

**Commit:** f144bf45607e8838c250bae424660658844457f4

## Issue
Files saved without extension had trailing dot (e.g., "document." instead of "document").

## Root Cause
File naming logic didn't handle no-extension case properly.

## Solution
Strip trailing dot when no extension present.

## Platforms
- Android
- Desktop
- iOS

## Impact
- Cleaner saved files
- Better compatibility
- Improved file management
