# Amazon 2023 GSA Benchmark

This role configures Amazon Linux 2023 optimized for EKS to be GSA compliant. Level 1 and 2 profiles will be applied by default based on [Amazon 2023 GSA Benchmarks](https://docs.google.com/spreadsheets/d/1Bf0QBKHbEOLA8tHfqQy7REO90CMnOPVPpZZlE7Ijy8g/edit#gid=884169645)

## Role Variables

There are many role variables defined in ``./defaults/main.yml``.

**Hardening will be applied to the following configurations by default**:

- General Configurations
- Services Configurations
- Network Configurations
- Logging and Auditing Configurations
- Access, Authentication and Authorization Configurations
- System Maintenance Configurations

Above high level configurations and other fine-grained configurations can be enabled/disabled using variabled defined in in defaults/main.yml.

**The configuration will not**:

- Install and configure AIDE
- Install and configure NTP

SELinux Configuration:
- SELinux is enabled to run in permissive mode

Other settings and services are listed. Please review to ensure they meet your organizational requirements.

## Dependencies

Python  >= 3.7
Ansible >= 2.11

## Example Playbook

```
---
- name: Harden Server
  hosts: 10.0.1.18
  become: yes

  roles:
  - ansible-os-amazon-linux-2023
```

## License

MIT.
