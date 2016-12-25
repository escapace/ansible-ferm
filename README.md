<p align="right">
    <a href="https://travis-ci.org/epiloque/ansible-ferm">
        <img src="https://travis-ci.org/epiloque/ansible-ferm.svg?branch=master"
             alt="build status">
    </a>
        <a href="https://galaxy.ansible.com/epiloque/ferm">
        <img src="https://img.shields.io/badge/ansible--galaxy-ferm-blue.svg"
             alt="ansible galaxy">
    </a>
</p>

ferm role

## Role Variables

Available variables are listed below, along with default values:

```yaml
ferm_ipv4_forwarding: 1
ferm_ipv6_forwarding: 1
ferm_ipv6_accept_ra: 0
```

Be aware that IPv6 forwarding may interfere with your existing IPv6
configuration: If you are using Router Advertisements to get IPv6 settings for
your hosts interfaces you should set accept_ra to 2. Otherwise IPv6 enabled
forwarding will result in rejecting Router Advertisements.

## Example Playbook

```yaml
- hosts: servers
  roles:
    - epiloque.ferm
```

## License

BSD
