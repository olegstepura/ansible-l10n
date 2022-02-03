Role Name
=========

Configure localisation on debian-based distributions. Configures `locale`, `console-setup`, `keyboard` and `timezone`.

Requirements
------------

Runs on Debian and Ubuntu.

Role Variables
--------------

see [defaults](./defaults/main.yml)

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: olegstepura.l10n
      timezone: Europe/Kaliningrad
      locales:
        - en_US.UTF-8
        - ru_RU.UTF-8
      locale: en_US.UTF-8
      console:
        charmap: UTF-8
        codeset: guess
        fontface: guess
        fontsize: 8x16
      keyboard:
        backspace: guess
        options: "grp:alt_shift_toggle,grp_led:scroll"
        model: pc104
        layout: "us,ru"
        variant: ","

```

License
-------

MIT
