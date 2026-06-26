# /start Remote Host Parser Fix

**Commit:** 5aace8401ce69bce497cdd1be993d50716d453a7

## Issue
Parser failed when interface name contained spaces (e.g., "Ethernet 2").

## Root Cause
`iface=` field used `jsonP` which strict-decoded entire remaining input. When `port=` followed `iface=`, strict decode failed on trailing data and fallback `text1P` stopped at first space.

## Solution
Replace `jsonP` with bounded `quotedP` that consumes only up to closing quote, leaving `port=` for next parser.

## Impact
- Support for spaced interface names
- Better parser robustness
- Improved error handling
- Better remote host support

## Testing
- Verified with various interface names
- Edge cases handled
