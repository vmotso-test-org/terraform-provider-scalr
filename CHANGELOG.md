# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- **New data source:** `scalr_endpoint` ([#10](https://github.com/Scalr/terraform-provider-scalr/pull/10))
- **New data source:** `scalr_webhook` ([#10](https://github.com/Scalr/terraform-provider-scalr/pull/10))
- **New resource:** `scalr_endpoint` ([#10](https://github.com/Scalr/terraform-provider-scalr/pull/10))
- **New resource:** `scalr_webhook` ([#10](https://github.com/Scalr/terraform-provider-scalr/pull/10))

### Required

- scalr server >= `8.0.1-beta.20200917`

## [1.0.0-rc6] - 2020-09-10

### Added

- `scalr_workspace`: new attribute `vcs_provider_id` (Scalr vcs provider ID, replaces `vcs_repo.oauth_token_id`)  ([#17](https://github.com/Scalr/terraform-provider-scalr/pull/17))

### Removed

- `scalr_workspace`: drop attribute `vcs_repo.oauth_token_id` ([#17](https://github.com/Scalr/terraform-provider-scalr/pull/17))

### Required

- scalr server >= `8.0.1-beta.20200903`

## [1.0.0-rc5] - 2020-09-03

### Added

- `scalr_workspace`: new attribute `environment_id` (Scalr environment ID, replaces `organization`) ([#11](https://github.com/Scalr/terraform-provider-scalr/pull/11))
- `provider`: new environment variable `SCALR_HOSTNAME` (Scalr hostname, replaces `TFE_HOSTNAME`) ([#12](https://github.com/Scalr/terraform-provider-scalr/pull/12))
- `provider`: new environment variable `SCALR_TOKEN` (Scalr token, replaces `SCALR_TOKEN`) ([#12](https://github.com/Scalr/terraform-provider-scalr/pull/12))

### Changed

- `scalr_workspace`: attribute `id` is now in the `ws-<RANDOM STRING>` format ([#11](https://github.com/Scalr/terraform-provider-scalr/pull/11))

### Removed

- `scalr_workspace`: drop attribute `organization` in favour of `environment_id` ([#11](https://github.com/Scalr/terraform-provider-scalr/pull/11))
- `scalr_workspace`: drop attribute `external_id` in favour of `id` ([#11](https://github.com/Scalr/terraform-provider-scalr/pull/11))
- `scalr_workspace`: drop attribute `vcs_repo.ingress_submodules` ([#11](https://github.com/Scalr/terraform-provider-scalr/pull/11))
- `provider`: drop environment variable `TFE_HOSTNAME` in favour of `SCALR_HOSTNAME` ([#12](https://github.com/Scalr/terraform-provider-scalr/pull/12))
- `provider`: drop environment variable `TFE_TOKEN` in favour of `SCALR_TOKEN` ([#12](https://github.com/Scalr/terraform-provider-scalr/pull/12))

### Required

- scalr server >= `8.0.1-beta.20200901`

## [1.0.0-rc3] - 2020-07-30

### Added

- `scalr_workspace`: new attribute `vcs_repo.path` ([#8](https://github.com/Scalr/terraform-provider-scalr/pull/8))
- `data.scalr_workspace`: new attribute `vcs_repo.path` ([#8](https://github.com/Scalr/terraform-provider-scalr/pull/8))

### Changed

- `data.scalr_current_run` will return empty values on the local operation backend instead of an error ([#9](https://github.com/Scalr/terraform-provider-scalr/pull/9))

### Required

- scalr server >= `8.0.1-beta.20200709`

## [1.0.0-rc2] - 2020-07-10

### Added

- `data.scalr_current_run`: new attribute `environment_id` ([#6](https://github.com/Scalr/terraform-provider-scalr/pull/6))
- `data.scalr_current_run`: new attribute `workspace_name` ([#6](https://github.com/Scalr/terraform-provider-scalr/pull/6))

### Removed

- `data.scalr_current_run`: drop attribute `workspace` ([#6](https://github.com/Scalr/terraform-provider-scalr/pull/6))

## [1.0.0-rc1] - 2020-07-01

Requires Scalr 8.0.1-beta.20200625 at least

### Added

- **New data source:** `scalr_current_run` ([#2](https://github.com/Scalr/terraform-provider-scalr/pull/2))
- `data.scalr_workspace`: new attribute `created_by` ([#5](https://github.com/Scalr/terraform-provider-scalr/pull/5))
- `scalr_workspace`: new attribute `created_by` ([#5](https://github.com/Scalr/terraform-provider-scalr/pull/5))

## [0.0.0-rc2] - 2020-03-30

### Added

- **New data source:** `scalr_workspace` ([#1](https://github.com/Scalr/terraform-provider-scalr/pull/1))
- **New data source:** `scalr_workspace_ids` ([#1](https://github.com/Scalr/terraform-provider-scalr/pull/1))
- **New resource:** `scalr_variable` ([#1](https://github.com/Scalr/terraform-provider-scalr/pull/1))
- **New resource:** `scalr_workspace` ([#1](https://github.com/Scalr/terraform-provider-scalr/pull/1))

## [0.0.0-rc1] - 2020-03-25

### Added

- Initial release.

[Unreleased]: https://github.com/Scalr/terraform-provider-scalr/compare/v1.0.0-rc6...HEAD
[0.0.0-rc2]: https://github.com/Scalr/terraform-provider-scalr/compare/v0.0.0-rc1...v0.0.0-rc2
[0.0.0-rc1]: https://github.com/Scalr/terraform-provider-scalr/releases/tag/v0.0.0-rc1
[1.0.0-rc1]: https://github.com/Scalr/terraform-provider-scalr/releases/tag/v1.0.0-rc1
[1.0.0-rc2]: https://github.com/Scalr/terraform-provider-scalr/releases/tag/v1.0.0-rc2
[1.0.0-rc3]: https://github.com/Scalr/terraform-provider-scalr/releases/tag/v1.0.0-rc3
[1.0.0-rc5]: https://github.com/Scalr/terraform-provider-scalr/releases/tag/v1.0.0-rc5
[1.0.0-rc6]: https://github.com/Scalr/terraform-provider-scalr/releases/tag/v1.0.0-rc6
