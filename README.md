bashlinux_motd
===============

This role creates a banner with a warning message for visitors and show it as Message Of The Day (motd)

Role Variables
--------------

The settable variables for this role are:
```yaml
motd_app:               # Name of the application to show in motd. Optional
                        # (default empty)
motd_env:               # Environment to show in motd. Optional
                        # (default empty)
motd_logo_src:          # File name with logo or banner in ascii art. Optional
                        # (default bashlinux)
motd_info_src:          # Template file with warning message and application info variables. Optional
                        # (default "No privacy expected")
motd_file_empty:	# Flag enabling system's motd to be appended to our custom motd
                        # (default false)
```

Example Playbook
----------------

Deploy motd along with Linux distrubution motd

```yaml
- hosts: servers
  roles:
    - bashlinux_motd
```

Deploy motd with custom banner on sandbox environment and no OS info appended to motd. Assuming the file `custom_banner` exists on the search path.
```yaml
- hosts: servers
  vars:
    motd_env: sandbox
    motd_logo_src: custom_banner
    motd_file_empty: true
  roles:
    - bashlinux_motd
```

License
-------

LGPL-3.0-or-later
