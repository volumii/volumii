# Desktop Updater Fix

**Commit:** 9b76742c6e1c7f65f55d9b0ce409dcc18e3a2f25

## Issue
The in-app updater was deleting the download before the "Open file location" button worked.

## Root Cause
The updater downloads to a temp UUID file via `createTmpFileAndDelete`, then relies on `file.renameTo(newFile)` to move bytes to the asset name. If rename failed, bytes stayed at UUID path and finally block deleted the only copy.

## Solution
Replace `renameTo` with `Files.move` using `REPLACE_EXISTING`:
- Performs in-place rename when possible (inode preserved, no copy)
- Falls back to copy+delete when atomic rename isn't possible
- Throws on genuine failure instead of silently losing files

## Impact
- Fixed download preservation for "Open file location"
- Improved Whonix compatibility
- More robust file handling
