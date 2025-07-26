# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.0.1] - 2025-07-26

### Added
- Podman role for installing container runtime with DNS support
  - Installs podman, dnsmasq, containernetworking-plugins, and podman-compose
  - Includes dnsname and aardvark-dns plugins for container DNS resolution
  - Daemonless operation (no systemd service management)
- Comprehensive project documentation
  - Enhanced README.md with collection overview and usage examples
  - CHANGELOG.md following Keep a Changelog format
  - CODING.md with development guidelines
  - CLAUDE.md for AI assistant context
  - RELEASE.md with release process documentation
- GitHub Actions release workflow
  - Automatic collection build on version tags
  - Ansible Galaxy publishing support
- Existing roles from initial collection structure:
  - **ansible** role for Ansible configuration and tools setup
  - **common** role for base system configuration (packages, repos, locales, timezone, etc.)
  - **updates** role for system update management
  - **users** role for user account management with home directory configuration

[0.0.1]: https://github.com/mkbrechtel/sys/releases/tag/v0.0.1