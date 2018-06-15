# Ansible Role: cfs

[![Build Status](https://api.travis-ci.org/JeremyVV/ansible-role-csf.svg?branch=master)](https://travis-ci.org/JeremyVV/ansible-role-csf)

Installs [role template](https://www.configserver.com/cp/csf.html). CSF is a Stateful Packet Inspection (SPI) firewall, Login/Intrusion Detection and Security application for Linux servers.

## Requirements

Ansible 2+


## Operating Systems
- RHEL 5+
- CentOS 5+
- CloudLinux 5+
- Fedora 26+

## Virtual Servers
- VMware
- Xen
- VirtualBox
- OpenVZ
- KVM


## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
csf_restrict_ui: 2
csf_tcp_in:          "20,21,22,25,53,80,110,143,443,465,587,993,995"
csf_tcp_out:         "20,21,22,25,53,80,110,113,443,587,993,995"
csf_udp_in:          "20,21,53"
csf_udp_out:         "20,21,53,113,123"
csf_icmp_in:         "1"
csf_ignore_allow:    "1"
csf_eth_device_skip: ""
csf_ct_limit:        "100"
csf_ct_permanent:    "1"
csf_lf_alert_to:     ""
csf_cc_deny:         ""
csf_ignore_allow:    "0"
```

## Dependencies

  - none

## Example Playbook

    - hosts: servers
      roles:
        - csf 

## License

MIT

## Author Information

This role was created in 2018 by [Jeremy Van Veelen](https://www.techgooroo.net/).

