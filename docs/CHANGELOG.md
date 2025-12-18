# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.0] - 2025-12-18

### Added
- Initial release of Alembic Converger
- Core convergence algorithm for merging multiple Alembic heads
- Graph analysis utilities for DAG traversal
- Merge migration creation and validation
- Upgrade path validation with database testing
- CLI interface with click
- Python API for programmatic usage
- Comprehensive error handling and rollback
- Dry-run mode for preview
- Verbose logging support
- Unit tests for core functionality
- Complete documentation (README, CONTRIBUTING)
- PyPI packaging configuration

### Features
- Automatic detection of heads from base revision
- Iterative pairwise merging
- Validation that merges contain no schema operations
- Safety guarantees:
  - Never modifies existing migrations
  - Never auto-resolves schema conflicts
  - Deterministic behavior
  - Automatic rollback on failure
- Exit codes for CI/CD integration
- Colorized CLI output

[0.1.0]: https://github.com/rishav00a/alembic_converger/releases/tag/v0.1.0
