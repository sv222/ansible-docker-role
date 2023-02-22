# Ansible Docker Role

This role installs Docker on a Linux system.

## Install Requirements

1. Ansible 2.5+
2. Python 2.7+

  ```sh
apt update \ 
&& export DEBIAN_FRONTEND=noninteractive \ 
&& apt install -y python3 ansible git 
  ```

## Supported Distributions (More in progress)

This role has been tested on the following distributions:

- Ubuntu 18.04, 20.04, 22.04

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
  name: ansible-docker
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
