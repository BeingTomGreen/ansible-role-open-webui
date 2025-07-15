# beingtomgreen.open_webui

This Ansible role deploys Open WebUI a Docker container.

## Installation

Given that Galaxy seems to have abandoned roles, I suggest referencing this repository directly in your projects `requirements.yml`:

```yml
---

roles:
  - name: beingtomgreen.open_webui
    src: https://github.com/BeingTomGreen/ansible-role-open-webui.git

collections: []
```

You can then install the requirements as normal:

```bash
ansible-galaxy install -r requirements.yml
```

## Requirements

- Docker and Docker Compose installed on target hosts
- Community.docker collection

## Role Variables

See [`defaults/main.yml`](defaults/main.yml) and [`vars/main.yml`](vars/main.yml) more details.

## Dependencies

- community.docker

Example Playbook
----------------

```yaml
- hosts: target_host
  vars:
    open_webui_env:
      WEBUI_AUTH: "false"
      OLLAMA_BASE_URL: "http://ollama.mydomain.com"
  roles:
    - beingtomgreen.open_webui
```

## License

[MIT](LICENSE)

## Author Information

[Tom Green](https://github.com/BeingTomGreen)
