Stouts.source
=============

[![Build Status](https://travis-ci.org/Stouts/Stouts.source.png)](https://travis-ci.org/Stouts/Stouts.source)

Ansible role wich manage source code from git or mercurial repositoires

#### Variables
```yaml
source_enabled: yes           # Enable role
source_known_hosts: []        # Ensure the hosts in known_hosts
source_sources: []            # Repositories to clone
source_sources_type: git      # Set repository type (git, hg)
source_default_dest:          # Default destination

source_known_hosts_file: /home/{{ansible_ssh_user}}/.ssh/known_hosts
```

#### Usage

Add `Stouts.source` to your roles and set vars in your playbook file.

Example:

```yaml

- hosts: all

  roles:
    - st.source

  vars:
    source_known_hosts: [github.com]
    source_sources:
      - repo: https://github.com/Dipsomaniac/dj-simple.git
      - dest: /usr/lib/simple/source

```

See [git-module](http://docs.ansible.com/git_module.html) and [hg-module](http://docs.ansible.com/hg_module.html) for source params.

#### License

Licensed under the MIT License. See the LICENSE file for details.

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Stouts/Stouts.source/issues)!

