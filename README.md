# Ansible Role: `aisbergg.docker`

This Ansible role installs and configures [Docker](https://docs.docker.com/engine/) and [Docker Compose](https://docs.docker.com/compose/) on Debian, CentOS and Arch Linux systems.

## Requirements

None.

## Role Variables

| Variable | Default | Comments |
|----------|---------|----------|
| `docker_centos_repo_url` | `https://download.docker.com/linux`<br>`/centos/$releasever/$basearch/stable` | RPM repository URL to be used for installation |
| `docker_debian_repo_url` | `https://download.docker.com/linux/`<br>`{{ ansible_distribution \| lower }}` | APT repository URL to be used for installation |
| `docker_install_docker_compose` | `true` | Whether or not to install Docker Compose |
| `docker_centos_compose_url` | `https://github.com/docker/compose`<br>`/releases/download/v{{ docker_centos_compose_version }}/docker-compose-Linux-x86_64` | URL for downloading Docker Compose on CentOS systems. |
| `docker_centos_compose_sha256_checksum` | `xxxx` | SHA256 checksum to validate the download of Docker Compose. |
| `docker_centos_compose_version` | `1.29.1` | Docker Compose version to be installed on CentOS systems |
| `docker_install_python_docker` | `true` | Whether or not to install Docker Python library |
| `docker_service_enabled` | `true` | Service enabled on boot |
| `docker_service_state` | `started` | Service run state (`started`, `stopped`, `restarted`) |
| `docker_service_restart_on_change` | `true` | Restart Docker daemon service on configuration changes. |
| `docker_config` | `{}` | Configuration of the Docker daemon (key-value pairs). See https://docs.docker.com/engine/reference/commandline/dockerd/#daemon-configuration-file |
| `docker_users` | `[]` | List of users to be added to the Docker group (allow users to control Docker) |

## Example Playbook

```yaml
- hosts: all
  vars:
    docker_service_enabled: true
    docker_service_state: started
    docker_service_restart_on_change: true
    docker_users:
      - foo
    docker_config:
      data-root: /var/lib/docker
      icc: false
      iptables: true
      ipv6: false
      live-restore: false
      log-driver: json-file
      log-opts:
        max-file: 2
        max-size: 10m
      storage-driver: overlay2
  roles:
    - aisbergg.docker
```

## License

MIT

## Author Information

Andre Lehmann (aisberg@posteo.de)
