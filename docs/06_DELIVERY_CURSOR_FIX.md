# Delivery Cursor Fix

**Commit:** 09e9235c86866cb167231e4d95aa45ad95687659

## Issue
PostgreSQL delivery cursor was not advancing to maximum group member ID.

## Impact
- Messages could be re-delivered
- Inefficient cursor tracking
- Potential duplicate notifications

## Solution
Ensure cursor advances to highest member ID seen.

## Testing
- Verified with large group scenarios
- PostgreSQL specific fix
