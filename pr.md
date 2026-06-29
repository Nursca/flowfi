## Description

This PR addresses multiple contract, infrastructure, and testing issues to improve protocol safety and automate code quality checks.

### Changes
- **Contracts**: Added `transfer_admin` functionality to allow rotating protocol ownership safely, emitting an `AdminTransferredEvent`. (Closes #459)
- **Contracts / Testing**: Introduced `paused` and `paused_at` state to streams. Implemented `pause_stream` and `resume_stream`. Fixed accrual calculation during paused periods so that `cancel_stream` correctly settles the recipient's accrued tokens up to the paused timestamp. Added comprehensive unit tests. (Closes #462)
- **Infrastructure**: Configured a contracts CI workflow with `cargo fmt --check` and `cargo clippy` gates. (Closes #460)
- **Infrastructure**: Added a Dependabot configuration to automate dependency updates for npm (root, frontend, backend), Cargo, and GitHub Actions. (Closes #461)

Closes #459
Closes #460
Closes #461
Closes #462
