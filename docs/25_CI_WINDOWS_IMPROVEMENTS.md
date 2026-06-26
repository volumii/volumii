# CI/CD Windows Build Improvements

**Commit:** 602f17ecfa36056cbdbfb381710291a3ada44013

## Fix Windows Build
Clean simplexmq submodule source directory on Windows build.

## Benefits
- Remove stale artifacts
- Ensure clean builds
- Improve CI reliability
- Faster diagnostics

## Details
- Directory cleanup script
- Build pre-flight checks
- Automated cleanup
