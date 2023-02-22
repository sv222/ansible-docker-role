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

## Using

1. Create playbook that uses this role:

main.yml:

```yaml
- name: Install Docker
  hosts: localhost
  roles:
  - ansible-docker
```

2. Create file with requirements:

requirements.yml:

```yaml
- src: https://github.com/sv222/ansible-docker-role
  name: ansible-docker
```

3. Then run the following command to install the role from the requirements.yml:

```yaml
ansible-galaxy install -r requirements.yml --force
```

4. And after run playbook:

```shell
ansible-playbook main.yml
```

## Contributing

Feel free to contribute to this project by submitting pull requests or reporting issues.

## License

MIT
