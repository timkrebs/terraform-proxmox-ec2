# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2026-03-13

### Changed

- **BREAKING:** Removed provider configuration from module. Callers must now configure the `bpg/proxmox` provider in their root module.
- **BREAKING:** Removed `proxmox_api_url`, `proxmox_api_token`, `proxmox_api_token_secret`, and `proxmox_insecure` variables.

### Added

- `cpu_type` variable to configure VM CPU type (default: `x86-64-v2-AES`)
- Input validation for `ip_address` (CIDR format) and `gateway` (IPv4 format)
- `.pre-commit-config.yaml` for local development hooks
- TFLint recommended preset

### Fixed

- Dependabot referencing non-existent `/examples/complete/` directory
- README inputs table showing incorrect `instance_type` default

## [1.0.0] - 2026-03-09

### Added

- Initial release
- Proxmox VM provisioning with EC2-like instance types (t3.small - t3.2xlarge)
- Custom instance sizing support
- Cloud-init user data support
- Static IP and network configuration
- SSH key authentication
- Tag support
