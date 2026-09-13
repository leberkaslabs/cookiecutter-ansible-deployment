# Ansible Deployment: {{ cookiecutter.deployment_name.lower() }}

[![Ansible Lint](https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/actions/workflows/ansible-lint.yml)

{{ cookiecutter.description }}

## Prerequisites

- Ensure you have Ansible installed (e.g. `pip3 install ansible`)
- **Development**: Install the pip packages listed in [requirements.txt](requirements.txt)

## Usage

> [!NOTE]
> Before running the playbooks, prepare the inventory and configuration files.

1. Copy the example inventory file to `hosts.yml`:

    ```bash
    cp inventories/hosts.example.yml inventories/hosts.yml
    ```

2. Run the Ansible playbook:

    ```bash
    ansible-playbook main.yml
    ```

## Development

This project includes [Ansible Molecule](https://github.com/ansible/molecule) to streamline testing and development.

```bash
molecule test
```

Molecule will automatically create, converge, verify and destroy the test instances.

## License

Copyright (c) {% now 'local', '%Y' %} {{ cookiecutter.full_name }}
