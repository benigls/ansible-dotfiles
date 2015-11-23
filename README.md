ansible-dotfiles
=========

A ansible role for installing dotfiles. All you need is a `install.sh` or any script that installs your dotfiles.

Requirements
------------

The only requirement is that you need a `install.sh` file or any shell script that install your dotfiles.

Role Variables
--------------

`dotfiles_repo` url of your dotfiles repository.

`dotfiles_name` name of the repository folder. `dotfiles` is the default.

`dotfiles_dest` destination of your dotfiles when it's cloned. `/tmp/` is default

`dotfiles_install_script` dotfiles installer file.

Example Playbook
----------------

    - hosts: ben
      vars:
        dotfiles_repo: "https://github.com/benigls/dotfiles.git"
        dotfiles_name: "dotfiles"
        dotfiles_install_script: "install.sh"
      roles:
        - ansible-dotfiles

License
-------

BSD/MIT
