# Supporter Badges System

**Commit:** ad23da63d0f3c5388c08a5d7db8f4e3ddf2c6915

## Overview
Implements a privacy-preserving badge system for SimpleX supporters.

## Technology
- Blind Signature Scheme (BBS)
- Anonymous credentials
- No identity exposure

## Features
- Supporter verification
- Multiple badge types
- Configurable badge keys
- Badge images and positioning

## Components
1. Badge generation (CLI)
2. Badge signing (private)
3. Badge verification (public)
4. UI rendering (images)

## Privacy
- Supporters remain anonymous
- No tracking of badge holders
- Decentralized verification

## Implementation Details
- FFI exports for badge symbols
- Schema migrations for badge storage
- Bot API extensions
- Cross-platform UI support (iOS, Android, Desktop)
