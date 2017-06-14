# Ansible Role: Message Of The Day [![Build Status](https://travis-ci.org/manala/ansible-role-motd.svg?branch=master)](https://travis-ci.org/manala/ansible-role-motd)

This role is far simple, functionally useless and because of this, essential. It will setup your Message Of The Day on your linux boxes.

It's part of the Manala <a href="http://www.manala.io" target="_blank">Ansible stack</a> but can be used as a stand alone component.

## Requirements

None.

## Dependencies

None.

## Installation

### Ansible 2+

Using ansible galaxy cli:

```bash
ansible-galaxy install manala.motd
```

Using ansible galaxy requirements file:

```yaml
- src: manala.motd
```

## Role Handlers

None

## Role Variables

|Name|Default|Type|Description|
|----|----|-----------|-------|
`manala_motd_template`|template/manala.j2|String (path)|Path to custom motd.
`manala_motd_message`|California 1993|String|A custom message

### Configuration example

Use predefined type (manala|cow|turkey|stegosaurus) with custom message:

```yaml
---

manala_motd_template: template/turkey.j2
manala_motd_message:  "My awesome message"
```

Use custom template:

```yaml
---

manala_motd_template:  "{{ playbook_dir ~ '/templates/motd.j2' }}"
```

## Example playbook

```yaml
- hosts: servers
  roles:
    - { role: manala.motd }
```

# Licence

MIT

# Author information

Manala [**(http://www.manala.io/)**](http://www.manala.io)