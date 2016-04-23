# ansible-role-rsyslog

This role configures rsyslog rules.

## Requirements

None.

## Role Variables

variable | required | default | choice | comment
-------- | -------- | ------- | ------ | -------------------
facility | yes      |         |        | facility type
priority | yes      |         |        | priority level
path     | yes      |         |        | file path

## Dependencies

None.

## Example Playbook

```yml
- hosts: servers
  roles:
    - rsyslog
```

*Inside `vars/main.yml`*:  
```yml
rsyslog:
  # iptables
  - facility: kernel
    priority: debug
    path: /var/log/iptables.log
```

## License

MIT

## Author Information
