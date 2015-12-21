## tsocks

[![Build Status](https://travis-ci.org/Oefenweb/ansible-tsocks.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-tsocks) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-tsocks-blue.svg)](https://galaxy.ansible.com/list#/roles/1417)

Set up tsocks in Debian-like systems.

#### Requirements

None

#### Variables

* `tsocks_install`: [default: `[]`]: Additional packages to install

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - tsocks
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-tsocks/issues)!
