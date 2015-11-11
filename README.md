
<!-- THIS IS A GENERATED FILE, DO NOT EDIT -->

All things Build & Release. This role manages the provisioning of build and release tools and services: [Jenkins](http://jenkins-ci.org), [Aptly](http://www.aptly.info), … By default, this role does nothing as all `*_state` variables are set to `ignored`. For the components you're interested in, set the `*_state` variables to `present` or `absent`. Integration issues (firewalling, proxying…) are not handled here.


* * *


## Supported Platforms

  * Ubuntu

  * Debian


## Variables

| Name | Value | Description |
|------|-------|-------------|
| relkit_aptly_api_bind_address | default 0.0.0.0 | None |
| relkit_aptly_api_bind_port | default 8081 | None |
| relkit_aptly_dl_bind_address | default 0.0.0.0 | None |
| relkit_aptly_dl_bind_port | default 8080 | None |
| relkit_aptly_repositories | default [{'distribution': 'latest', 'name': 'default'}] | None |
| relkit_environment | default {} | Environment variables, such as http_proxy |
| relkit_jenkins_groups | default [] | List of groupnames to which the jenkins user belongs |
| relkit_jenkins_http_bind_address | default 127.0.0.1 | None |
| relkit_jenkins_http_bind_port | default 8080 | None |
| relkit_jenkins_memory | default 512m | How much memory the JVM can use |
| relkit_jenkins_sshkeys | default [] | List of dicts {'keyval', 'pubval', 'filename'} |
| relkit_jenkins_stable | default True | Boolean. If set, use Long Term Support (LTS) release |
| relkit_jenkins_state | default ignored | One of present, absent, ignored |



## Usage

To use this role from a **playbook**, 
register its ID in the project `requirements.{txt,yml}` file.
To add this role as another **role dependency**,
register its ID in the `dependencies` list of the role manifest `meta/main.yml`.
For further details,
please refer to the Ansible documentation at https://docs.ansible.com/playbooks_roles.html.


## Maintenance

Install [ansible-universe](https://github.com/fclaerho/ansible-universe)
and run `ansible-universe check` to re-generate this distribution.

The following files are generated or updated based on the role manifest `meta/main.yml`:
  * tasks/main.yml
  * README.md