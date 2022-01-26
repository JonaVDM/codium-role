# Codium Role

A simple role setups vscodium just how I like it.

## Requirements

You need to have vscodium installed, you can get it through your package manager or by installing it from their [https://vscodium.com](website).

## Role Variables

```yml
codium_user_config_location: "{{ ansible_user_dir }}/Application Support/VSCodium/User"
```

The directory where the user data is stored, grabs the path which is relevant to the platform (MacOSX - Linux).

```yml
codium_install_packages:
  - angular.ng-template
  - redhat.ansible
  - hookyqr.beautify
  - ...
```

The packages that will be installed by default.

```yml
dotfiles_settings_location: ~/.dotfiles/codium/settings.json
```

The location of where the user's settings are stored.

```yml
dotfiles_snippets_location: ~/.dotfiles/codium/snippets
```

The location of where the user's snippets are stored.

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
    - role: jonavdm.codium
      codium_user_config_location: >
        "{{ ansible_user_dir }}/Application Support/VSCodium/User"
      dotfiles_settings_location: ~/.dotfiles/codium/settings.json
      dotfiles_snippets_location: ~/.dotfiles/codium/snippets
```

## License

MIT
