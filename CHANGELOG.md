# Changelog

## [v1.5.0] - 2025-05-28

### Added

- Added support for custom task IDs.
- Added support for multiple IDs.
- Added the option to use the full commit message.
- Added parsing of Conventional Commit types.

### Changed

- Fixed minor syntax bug.

## [v1.4.2] - 2025-05-28

### Added

- Added support for running the workflow on macOS.

### Changed

- Changed commit message keyword for task ID detection from "task-id:" to "task:".

## [v1.4.0] - 2025-05-13

### Added

- Added automatic ClickUp task link creation from commit messages
- Added support for detecting task IDs in format `task-id: \`TASK_ID\`` in commit messages
- Added conversion of task IDs to clickable links in notification messages
- Support for alphanumeric task IDs (like "86eqv0y92")
- Enhanced message formatting to show task ID as clickable link with pipe separator format

## [v1.3.0] - 2025-05-13

### Improved

- Added sanitization for author names to handle special characters and symbols.
- Replaced problematic characters in commit author names with spaces.
- Added fallback to "Unknown Contributor" when author name becomes empty after sanitization.
- Cleaned up unnecessary comments and debug statements from all steps:
  - Removed redundant logging from "Fetch Duration" step
  - Removed unnecessary debug output from "Fetch Commits" step
  - Streamlined "Send ClickUp Notification" step
- Optimized overall workflow execution by reducing verbose output.

## [v1.2.0] - 2025-05-05

### Added

- Initial release of **ClickUpNotification** GitHub Action.
- Fetches commits between the last successful CI/CD run and the current run.
- Sends a formatted notification to ClickUp with commit messages and authors.
- Duration of the CI/CD process included in the notification.
