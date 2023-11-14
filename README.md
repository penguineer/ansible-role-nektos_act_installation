# Ansible Role: nektos_act_installation

> Install [Act](https://github.com/nektos/act)

This Ansible role installs [Act](https://github.com/nektos/act), a tool for running GitHub Actions locally

## Usage


### Configuration

The defaults are usually suitable for installation. Feel free to change them if they do not fit your needs.


Controlling the files on the target system:

* `nektos_act_path_prefix`: Prefix to the installation target

For automatic download:

* `nektos_act_version`: Fix the release version. Leave empty to retrieve the latest version.

To fix the release, set:

* `nektos_act_url`: URL to the act archive. Leave empty for the devault URL


### Requirements

Add to your `requirements.yml`:
```yml
- src: https://github.com/penguineer/ansible-role-nektos_act_installation
  version: …
```
Ansible Galaxy is currently not accessible, so the role must be downloaded from GitHub directly.


### Include

as role:

```yaml
vars:
  nektos_act_path_prefix: …
  nektos_act_version: …
  nektos_act_url: …

roles:
  - role: ansible-role-nektos_act_installation
```


as task:

```yaml
tasks:
  - name: Set up Act
    include_role:
      name: ansible-role-nektos_act_installation
    vars:
      nektos_act_path_prefix: …
      nektos_act_version: …
      nektos_act_url: …
```


## Maintainers

* Stefan Haun ([@penguineer](https://github.com/penguineer))


## Contributing

PRs are welcome!

If possible, please stick to the following guidelines:

* Keep PRs reasonably small and their scope limited to a feature or module within the code.
* If a large change is planned, it is best to open a feature request issue first, then link subsequent PRs to this issue, so that the PRs move the code towards the intended feature.


## License

[MIT](LICENSE.txt) © 2023 Stefan Haun and contributors
