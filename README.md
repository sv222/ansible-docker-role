# Ansible Docker Role

This role installs Docker on a Linux system.

## Requirements

- Ansible 2.7 or later

## Supported Distributions

This role has been tested on the following distributions:

<!-- - Ubuntu 20.04
- Amazon Linux 2
- Debian 10 -->
- CentOS 7, 8, 9

## Role Variables

The following variables are defined in the `defaults/main.yml` file:

```yaml
# Docker version to install
docker_version: "23.0.1"
```

## Dependencies

None.

## Example Playbook

Here's an example playbook that uses this role:

```yaml
- name: Install Docker and Docker Compose
  hosts: all
  roles:
  - ansible-docker
```

## Using Ansible Galaxy

To use this role from Ansible Galaxy, add the following to your requirements.yml file:

```yaml
- src: /roles
  name: ansible-docker
```

Then run the following command to install the role from the local path:

```yaml
ansible-galaxy install -r requirements.yml --roles-path /path/to/roles
```

The --roles-path option specifies the directory where the roles will be installed. If the directory doesn't exist, it will be created.

## Contributing

Feel free to contribute to this project by submitting pull requests or reporting issues.

## License

MIT
