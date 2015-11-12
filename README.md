
<!-- THIS IS A GENERATED FILE, DO NOT EDIT -->

All things Build & Release. This role manages the provisioning of various B&R tools and services, including build environments, continuous integration services and package repositories.


* * *


## Supported Platforms

  * Ubuntu
  * Debian

## Variables

| Name | Value | Description |
|------|-------|-------------|
| relkit_aptly_api_address | _(default:)_ 0.0.0.0 | API service address to bind |
| relkit_aptly_api_port | _(default:)_ 8081 | API service port to bind |
| relkit_aptly_dl_address | _(default:)_ 0.0.0.0 | Download service address to bind |
| relkit_aptly_dl_port | _(default:)_ 8080 | Download service port to bind |
| relkit_aptly_repositories | _(default:)_ [{'distribution': 'latest', 'name': 'default'}] | List of dict {'name', 'distribution'} |
| relkit_environment | _(default:)_ {} | Common environment variables, such as http_proxy |
| relkit_jenkins_groups | _(default:)_ [] | List of groupnames to which the jenkins user belongs |
| relkit_jenkins_http_address | _(default:)_ 127.0.0.1 | HTTP service address to bind |
| relkit_jenkins_http_port | _(default:)_ 8080 | HTTP service port to bind |
| relkit_jenkins_memory | _(default:)_ 512m | How much memory the JVM can use |
| relkit_jenkins_sshkeys | _(default:)_ [] | List of dicts {'keyval', 'pubval', 'filename'} |
| relkit_jenkins_stable | _(default:)_ True | Boolean. If set, use Long Term Support (LTS) release |
| relkit_jenkins_state | _(default:)_ ignored | One of present, absent, ignored |



## Usage

To use this role from a **playbook**, 
register its ID in the project `requirements.{txt,yml}` file.
To add this role as another **role dependency**,
register its ID in the `dependencies` list of the role manifest `meta/main.yml`.
For further details,
please refer to the Ansible documentation at https://docs.ansible.com/playbooks_roles.html.

By default, this role does nothing as all `*_state` variables are set to `ignored`. For the components you're interested in, set the `*_state` variables to `present` or `absent`.
The following components are available:
  * `relkit_jenkins_state` — Jenkins, CI Service
  * `relkit_aptly_state` — Aptly, Debian Repository
  * …

**NOTICE!** Integration issues (firewalling, proxying…) are not managed here, use a support role.



## Maintenance

Install [ansible-universe](https://github.com/fclaerho/ansible-universe)
and run `ansible-universe check` to re-generate this distribution.

The following files are generated or updated based on various role assets:
  * tasks/main.yml
  * README.md


