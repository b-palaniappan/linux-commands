## Add User to Sudoer list
* Switch to Super user - `su -`
* Upgrade - `apt update && apt -y install && apt -y autoremove`
* Install Sudo - `apt install sudo`
* Add user to sudo group - `usermod -aG sudo <username>`
* Reboot system - `reboot`
* After restart check - `sudo whoami`.. will return `root`
