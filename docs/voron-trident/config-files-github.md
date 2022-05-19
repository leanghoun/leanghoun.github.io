---
layout: default
title: GitHub & TailScale
parent: Voron Trident
permalink: /docs/collections/voron-trident/GitHub & TailScale
nav_order: 2
---

# GitHub & TailScale

## Creating the Initial Repository
I've created a [GitHub repository](https://github.com/leanghoun/klipper_config) for my config files. Here are the steps I took.
1. Go to [GitHub](https://github.com) and create the repository. I just used *klipper_config* to match the folder name on the Raspberry Pi.
1. In Terminal, SSH into the Raspberry Pi and navigate to the folder you want to turn into a repository `cd klipper_config`
1. Create the readme file `echo "# mainsail-trident" >> README.md`
1. Initiliaze the folder `git init`
1. Start tracking all files in the folder `git add *`
1. Initial commit `git commit -m "First commit"`
1. Set the branch to main `git branch -M main`
1. Add the origin `git remote add origin https://github.com/leanghoun/klipper_config.git`
1. Finally, push the files `git push -u origin main`

## Macro to Auto Commit Changes to GitHub
By adding one python file and one script, it's possible to create a Mainsail dashboard macro to autocommit all changes in *~/klipper_configs/* to the GitHub repository. [Full instructions here](https://github.com/th33xitus/kiauh/wiki/How-to-autocommit-config-changes-to-github%3F).

### Creating the Python File
1. In Terminal, SSH into the Raspberry Pi and navigate to `cd klipper/klippy/extras`
1. Create the python file `nano gcode_shell_command.py` then paste the contents from the original [KIAUH file](https://github.com/th33xitus/kiauh/blob/master/resources/gcode_shell_command.py), exit and save

### Creating the Script
1. Navigate to `cd ~/klipper_config` to create the script within the GitHub repository
1. Create the script file `nano autocommit.sh` then paste the contents from the original [script](https://github.com/th33xitus/kiauh/blob/master/resources/autocommit.sh), uncomment the folders to commit to GitHub, exit and save

### Storing GitHub Credentials
The script cannot respond to terminal password prompts, so we will store the credentials `git config --global credential.helper store`

### Creating the Macro
Finally, we need to create two parts; the shell command and the macro itself:

```yaml
[gcode_shell_command backup_cfg]
command: sh /home/pi/klipper_config/autocommit.sh
timeout: 30.
verbose: True

[gcode_macro GIT_BACKUP]
gcode:
  RUN_SHELL_COMMAND CMD=backup_cfg
```

Clicking the new GIT BACKUP macro on the Mainsail dashboard should commit all files/changes to the GitHub repository. I also added a line for "printer-" to the .gitignore file to prevent Klipper backup files from being committed to the repository.

## Git Reference for Terminal
- `git status` - Checks status of local repository.
- `git add filename.css` - Start tracking a new file.
- `git add *` - Start tracking all files in current folder.
- `git rm --cached filename.css` - Remove file from tracking. Also consider adding to .gitignore to prevent future tracking. The `--cached` flag is very important as it removes the file from tracking, but does not delete it from the filesystem.
- `git rm --cached -fr folder` - Force remove folder and subfiles.
- `git commit -m "Updated something"` - Commit with a message.
- `git commit -a` - Commit all changes in local repository.
- `git commit --amend` - Commits new changes as part of the previous commit.
- `git push` - Pushes all commits to the remote repository.
- `find . -name .DS_Store -print0 | xargs -0 git rm --ignore-unmatch` - Find and remove all .DS_Store files in repository.
- `ls -ldF .?*` - Show hidden files and folders.

## TailScale

The easiest way to remotely access Mainsail is by installing a VPN like [TailScale](https://tailscale.com). There are only two requirements; (1) it must be installed on every device within the private network, and (2) the new TailScale IP addresses of remote devices need to be added to moonraker.conf's trusted_clients list.

To view the list of devices and their IP addresses, visit the [TailScale Admin page](https://login.tailscale.com/admin/machines).

### On Raspberry Pi
1. Install TailScale to the Raspberry Pi with `curl -fsSL https://tailscale.com/install.sh | sh`.
1. Start the service with `sudo tailscale up`, and it will provide a link for you to authenticate.

### On Other Devices
Windows, Mac, iPhones, and Android Phones all have a dedicated TailScale app to install and login. Upon login, the IP addresses will be registered.

