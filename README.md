# Dotfiles Manager

A robust, feature-rich dotfiles management system written in bash. Manage your dotfiles with git integration, automatic backups, and easy installation.

## Installation

```bash
# clone and cd into project
git clone git@github.com:oatbiscuit/dotfile-manager.git
cd dotfile-manager

# make file executable
chmod +x dotfiles

# make local bin directory, if it doesn't exist
mkdir -p ~/.local/bin

# create a symlink of dotfiles in local bin
ln -s "$(pwd)/dotfiles" ~/.local/bin/dotfiles

# verify installation
dotfiles --version
```

## Help

```bash
Dotfiles Manager

Usage: dotfiles <command> [arguments]

Environment Variables:
    DOTFILES_DIR                - Override dotfiles location (default: ~/.dotfiles)
    BACKUP_DIR                  - Override backup location
    GIT_REMOTE                  - Default git remote for push/pull
    XDG_CONFIG_HOME             - XDG config home (default: ~/.config)
    XDG_STATE_HOME              - XDG state home (default: ~/.local/state)

Commands:
    install                     - Create symlinks for all dotfiles.
    uninstall                   - Remove symlinks from home directory.
    list                        - List all managed dotfiles.
    status                      - Show installation status of dotfiles.
    add <file>                  - Add a new file to dotfiles management.
    remove <file>               - Remove a file from dotfiles management.
    restore                     - Restore backed up files.
    sync                        - Sync changes between home and dotfiles repo.
    save                        - Commit changes to git.

Git Commands:
    git-init                    - Initialise git repository.
    git-status                  - Show git status.
    git-commit [message]        - Commit changes.
    git-log [options]           - Show commit history.
    git-push [remote]           - Push to remote.
    git-pull [remote]           - Pull from remote.
    git-diff [options]          - Show differences.

Options:
    [--help] [-h]               - Show this help.
    [--version] [-v]            - Show version information.
```

## License
MIT License - feel free to use and modify
