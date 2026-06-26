# Group Link Policy - Obfuscated Links

**Commit:** 8c4580ee00b1239d6781dccb278534a1284eca47

## Feature
Groups can now configure whether obfuscated SimpleX links are allowed.

## Implementation
- Added obfuscated link parser
- Enforces group policy at message level
- More efficient than previous implementation

## Configuration
Groups can set policies to:
- Allow all SimpleX links
- Block obfuscated SimpleX links
- Allow standard links only

## Security Implications
- Prevents accidental exposure through obfuscated links
- Group admins maintain control over link usage
- Protects privacy-sensitive groups
