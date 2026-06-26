# SimplexNameDomain Refactoring

**Commit:** 68fc1b5d227941677afa534b5453a9d9ec8dbe72

## Change
Split `SimplexNameDomain` out of `SimplexNameInfo` for better code organization.

## Benefits
- Cleaner architecture
- Reduced coupling
- Better type safety
- Easier maintenance

## Implementation
- New SimplexNameDomain type
- Updated SimplexNameInfo
- Refactored UI components
- SimplexMQ library alignment

## Migration
- Backward compatible
- Updated schema
- Type migration helpers

## Testing
- Full regression suite
- Cross-platform validation
