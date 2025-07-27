# Common Role

This role provides base system configuration for Debian/Ubuntu systems.

## Requirements

- Ansible >= 2.14
- Debian (bookworm, bullseye) or Ubuntu (jammy, focal)
- Root/sudo privileges for system configuration

## Role Variables

See `defaults/main.yaml` for all available variables and their default values.

Key variables include:
- `common_debian_packages`: List of packages to install
- `common_locales`: List of locales to generate
- `common_default_locale`: Default system locale
- `common_timezone`: System timezone
- `common_hostname`: System hostname configuration

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  become: yes
  roles:
    - mkbrechtel.sys.common
```

## Features

- Debian/Ubuntu repository configuration
- Package installation and management
- Locale generation and configuration
- Timezone configuration
- Hostname configuration
- Keyboard layout configuration
- Network configuration
- Security settings and tweaks
- Shell configuration (fish, xonsh)
- SSH agent systemd service
- Root user configuration

## License

Apache-2.0