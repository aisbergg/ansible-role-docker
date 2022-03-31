# Changelog

All notable changes to this project will be documented in this file.

- [1.4.0 (2022-03-31)](#140-2022-03-31)
- [1.3.0 (2022-01-28)](#130-2022-01-28)
- [1.2.1 (2021-10-11)](#121-2021-10-11)
- [1.2.0 (2021-10-10)](#120-2021-10-10)
- [1.1.0 (2021-10-10)](#110-2021-10-10)
- [1.0.0 (2021-10-10)](#100-2021-10-10)

---

<a name="1.4.0"></a>
## [1.4.0](https://github.com/aisbergg/ansible-role-docker/compare/v1.3.0...v1.4.0) (2022-03-31)

### CI Configuration

- add branch explicitly to make Ansible import action happy
- bump Ansible Galaxy action version

### Chores

- don't use bump2version to include the CHANGELOG in the bump commit, it doesn't do a good job

### Features

- bump Docker Compose version to 2.3.4


<a name="1.3.0"></a>
## [1.3.0](https://github.com/aisbergg/ansible-role-docker/compare/v1.2.1...v1.3.0) (2022-01-28)

### Bug Fixes

- don't run python-docker installation in check mode (fails, if repository is not installed)
- install Python 3 Docker package on Debian systems

### CI Configuration

- fix automatic release and publish process

### Chores

- include changelog in bump commits
- update changelog template


<a name="1.2.1"></a>
## [1.2.1](https://github.com/aisbergg/ansible-role-docker/compare/v1.2.0...v1.2.1) (2021-10-11)

### Chores

- update author information
- **.ansible-lint:** update linter config
- **.pre-commit-config.yaml:** bump pre-commit hook versions
- **CHANGELOG.md:** update changelog
- **requirements.yml:** add role requirements


<a name="1.2.0"></a>
## [1.2.0](https://github.com/aisbergg/ansible-role-docker/compare/v1.1.0...v1.2.0) (2021-10-10)

### Chores

- **CHANGELOG.md:** update changelog

### Features

- add option to install Docker Python library


<a name="1.1.0"></a>
## [1.1.0](https://github.com/aisbergg/ansible-role-docker/compare/v1.0.0...v1.1.0) (2021-10-10)

### Chores

- **CHANGELOG.md:** update changelog

### Documentation

- **README.md:** update usage information

### Features

- bump Docker Compose version and add checksum verification


<a name="1.0.0"></a>
## [1.0.0]() (2021-10-10)

Initial Release
