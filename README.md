# sys Ansible Collection

**sys** provides base system configuration and management roles for Debian/Ubuntu systems. This collection focuses on common system administration tasks, user management, and container runtime setup.

> **⚠️ Development Phase Notice**  
> This collection is currently in development (version 0.x.x). Breaking changes may occur in any release until we reach version 1.0.0. APIs, role interfaces, and variable names are subject to change.

## Installation

```bash
ansible-galaxy collection install mkbrechtel.sys
```

## Requirements

- Ansible >= 2.14.3
- Debian (bookworm, bullseye) or Ubuntu (jammy, focal)

## Included Roles

- **ansible**: Ansible configuration and tools setup
- **common**: Base system configuration (packages, repos, locales, timezone, etc.)
- **updates**: System updates management
- **users**: User account management with home directory configuration
- **podman**: Podman container runtime with DNS support

## Global Variables

This collection uses global variables that are shared across roles where applicable:

- `domain_name`: The primary domain name used for system configuration (optional)

## Usage

### Base System Setup

```yaml
- hosts: servers
  become: yes
  roles:
    - mkbrechtel.sys.common
    - mkbrechtel.sys.users
    - mkbrechtel.sys.podman
```

### User Management

```yaml
- hosts: servers
  become: yes
  roles:
    - role: mkbrechtel.sys.users
      vars:
        users:
          - name: alice
            groups: ['sudo', 'docker']
            shell: /bin/bash
```

## License

Apache-2.0