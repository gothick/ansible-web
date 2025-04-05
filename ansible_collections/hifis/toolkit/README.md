<!--
SPDX-FileCopyrightText: Helmholtz Centre for Environmental Research (UFZ)
SPDX-FileCopyrightText: Helmholtz-Zentrum Dresden-Rossendorf (HZDR)

SPDX-License-Identifier: Apache-2.0
-->

# Ansible Collection - hifis.toolkit

[![Latest release](https://img.shields.io/github/v/release/hifis-net/ansible-collection-toolkit)](https://github.com/hifis-net/ansible-collection-toolkit/releases)
[![hifis.gitlab_runner](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/gitlab_runner.yml/badge.svg)](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/gitlab_runner.yml)
[![hifis.gitlab](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/gitlab.yml/badge.svg)](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/gitlab.yml)
[![hifis.haproxy](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/haproxy.yml/badge.svg)](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/haproxy.yml)
[![hifis.keepalived](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/keepalived.yml/badge.svg)](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/keepalived.yml)
[![hifis.netplan](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/netplan.yml/badge.svg)](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/netplan.yml)
[![hifis.redis](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/redis.yml/badge.svg)](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/redis.yml)
[![hifis.ssh_keys](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/ssh_keys.yml/badge.svg)](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/ssh_keys.yml)
[![hifis.unattended_upgrades](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/unattended_upgrades.yml/badge.svg)](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/unattended_upgrades.yml)
[![hifis.zammad](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/zammad.yml/badge.svg)](https://github.com/hifis-net/ansible-collection-toolkit/actions/workflows/zammad.yml)
[![DOI](https://zenodo.org/badge/495697576.svg)](https://zenodo.org/doi/10.5281/zenodo.11147483)

This collection provides production-ready Ansible roles used for providing services used in research and by research
software engineers, but not exclusively. The following use cases are supported:

* **DevOps platform:**
    * [GitLab](roles/gitlab)
    * deploy [GitLab-Runner](roles/gitlab_runner) with a focus, but not limited, on Openstack autoscaling
    * [Redis](roles/redis)
* **Help desk:**
    * [Zammad](roles/zammad)
* **High Availability (HA) / Load Balancing:**
    * [HAProxy](roles/haproxy)
    * [Keepalived](roles/keepalived)
* **OS-related:**
    * [unattended-upgrades](roles/unattended_upgrades)
    * [netplan](roles/netplan)
    * distribute authorized [SSH keys](roles/ssh_keys) to users

## Looking for the unattended_upgrades role?

You can now find it under [roles/unattended_upgrades](roles/unattended_upgrades).

We moved our existing Ansible roles into a single collection to deduplicate code and have a common test suite for all roles.
We decided to reuse the unattended_upgrades repository as a collection repo as it is our most popular role.

## Minimum required Ansible-version

* Ansible >= 2.16

## Installation

Install the collection via ansible-galaxy:

```shell
ansible-galaxy collection install hifis.toolkit
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Apache-2.0

## Author

This collection is maintained by [HIFIS Software Services](https://hifis.net/).
