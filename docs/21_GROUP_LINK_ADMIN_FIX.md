# Group Link Fix After Admin Demotion

**Commit:** 6cde614e51e92fde0ea6068a7242fbfa897ec8dd

## Issue
Group links were lost when admin was demoted to regular member.

## Root Cause
Role change logic was removing links inappropriately.

## Solution
- Fix group role change handling
- Allow link use for non-admins
- Proper size limit enforcement
- Improved delete logic
- Better query planning

## Testing
- Relay test suite
- Role transition scenarios
- Link persistence verification

## Impact
- Better member experience
- Preserved group links
- Improved role flexibility
