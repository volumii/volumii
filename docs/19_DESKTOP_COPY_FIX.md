# Desktop Text Copy Fix

**Commit:** 553f98adf4d28f2e3f4aab4e065f61e8842509f2

## Issue
Selecting text across messages also copied text of event/info items (e.g., "connected").

## Root Cause
`getSelectedCopiedText` emitted text for every merged item between selection bounds. Event/info items have no msgContent but non-empty text, so they were included.

## Solution
Skip items without msgContent - only real messages are copyable.

## Result
- Clean text copying
- No system messages in copy
- Better user experience

## Implementation
- Enhanced content filtering
- Message detection logic
- UI feedback improvement
