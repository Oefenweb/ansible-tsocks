## tsocks

[![Build Status](https://travis-ci.org/Oefenweb/ansible-tsocks.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-tsocks)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-tsocks-blue.svg)](https://galaxy.ansible.com/Oefenweb/tsocks)

Set up tsocks in Debian-like systems.

#### Requirements

None

#### Variables

* `tsocks_install`: [default: `[]`]: Additional packages to install

* `tsocks_local`: [default: `[]`]: Local networks
* `tsocks_path`: [default: `[]`]: Paths declaration
* `tsocks_path.{n}.directives`: [default: `[]`]: Directives (e.g. `['reaches 150.0.0.0/255.255.0.0']`)
* `tsocks_server`: [default: `127.0.0.1`]: Default server
* `tsocks_server_type`: [default: `5`]: SOCKS version used by the server
* `tsocks_server_port`: [default: `1080`]: The port on which the SOCKS server receives request

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - tsocks
  vars:
    tsocks_local:
      - 192.168.0.0/255.255.255.0
      - 10.0.0.0/255.0.0.0

    tsocks_path:
      - directives:
        - reaches 150.0.0.0/255.255.0.0
        - reaches 150.1.0.0:80/255.255.0.0
        - server 10.1.7.25
        - server_type 5
        - default_user delius
        - default_pass hello

    tsocks_server: 192.168.0.1
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-tsocks/issues)!
