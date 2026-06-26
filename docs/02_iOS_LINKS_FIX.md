# iOS SimpleX Links In-App Routing

**Commit:** 547595041eb661b9038245c082f65e5fb19a6f73

## Problem
Tapping an inline SimpleX connection link in message text was ignored by iOS when the app is in foreground.

## Root Cause
iOS drops `UIApplication.shared.open()` of a URL owned by the same app while in foreground. Both `simplex:` scheme and `simplex.chat` universal links belong to SimpleX Chat app.

## Solution
Route SimpleX links to `ChatModel.appOpenUrl` instead - the same sink that `onOpenURL` feeds, leading to `connectViaUrl/planAndConnect`.

## Benefits
- Matches connection-link card behavior
- Consistent with multiplatform clients
- Implements in-process connection instead of OS round-trip
- Also fixes "Send questions" and "connect to developers" buttons
