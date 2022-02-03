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
      vars:
        l10n_timezone: Europe/Kaliningrad
        l10n_locale_lang: en_US.UTF-8
        l10n_locales:
          - en_US.UTF-8
          - ru_RU.UTF-8
        l10n_console_charmap: UTF-8
        l10n_console_codeset: guess
        l10n_console_fontface: guess
        l10n_console_fontsize: 8x16
        l10n_keyboard_backspace: guess
        l10n_keyboard_options: "grp:alt_shift_toggle,grp_led:scroll"
        l10n_keyboard_model: pc104
        l10n_keyboard_layout: "us,ru"
        l10n_keyboard_variant: ","
```

License
-------

MIT
