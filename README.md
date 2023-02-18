# Ansible Docker Role

This role installs Docker on a Linux system.

## Requirements

- Ansible 2.7 or later

## Supported Distributions

This role has been tested on the following distributions:

- Ubuntu 18.04, 20.04, 22.04
- Debian 9, 10
- CentOS 7, 8, 9

## Role Variables

The following variables are defined in the `defaults/main.yml` file:

```yaml
docker_version: "latest" # The version of Docker to install (default: latest)
docker_package_state: "present" # The state of the Docker package (default: present)
```

## Dependencies

None.

## Example Playbook

Here's an example playbook that uses this role:

```yaml
- name: Install Docker
  hosts: localhost
  roles:
  - ansible-docker
```

## Using Ansible Galaxy

To use this role from Ansible Galaxy, add the following to your requirements.yml file:

```yaml
- src: https://github.com/sv222/ansible-docker-role
  name: ansible-docker-role
```

Then run the following command to install the role from the local path:

```yaml
ansible-galaxy install -r requirements.yml
```

And after:

```shell
ansible-playbook main.yml
```

## Contributing

Feel free to contribute to this project by submitting pull requests or reporting issues.

## License

MIT
