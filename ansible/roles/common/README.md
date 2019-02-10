# Common Role

A base role used to install some `git`, `htop`, `tmux`, `vim` and
`oh-my-zsh` on a server.

A few Vim plugins are installed. Look at the `vim_plugins` variable in
`vars/main.yml` to see which ones.

## Role Variables

Here are the variables used for this role:

- `additionnal_users`: list of the user names whose home directory is not in
  `/home` and you want to configure shells and `vim` (eg. `root`).
- `vim_bundle_folder`: path to the folder where Vundle and Vim plugins will be
  installed and copied to user's `.vim` folders.
- `vimrc_path`: location where the `vimrc` template file will be generated.
  This file is then copied to users' `.vimrc`.
- `vim_plugins`: list of the Vim plugins you want to install.
- `zsh_installation_folder`: location where `oh-my-zsh` will be installed.
- `zsh_theme`: `oh-my-zsh` theme name (see [here](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes)
  to have a look on available themes).


## Example Playbook

Use this role by doing the following in your `playbook.yml`:

```
- hosts: common_servers
  roles:
     - common
```
