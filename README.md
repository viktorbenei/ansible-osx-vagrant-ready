ansible-osx-vagrant-ready
=========================

Ansible playbook to prepare a bare OS X VM for vagrant


# Manual Steps


## Required

* install OS X updates (these scripts are written for 10.9 Mavericks, 10.10 Yosemite is not yet tested)
* when you create the OS X user the username should be "vagrant" and the password should be "vagrant" too
* enable SSH : System Preferences / Sharing / Remote Login: enable
* make sure auto login to user" is enabled for the "vagrant" user


## Not required but advised

* allow 2 CPUs and at least 2GB of RAM (3-4 is the optimal) -> this can help to speed up the setup (you can downscale it after the setup if you like).
* turn off the App Store automatic update
	* System Preferences -> App Store -> Automatically check for updates
* turn off sleep
	* System Preferences -> Energy Saver -> Change all options to 'never' and disable Hard disk sleep
* turn off screen saver
* turn off every sharing between the VM and the Guest
	* in Parallels:
		* Virtual Machine -> Configure -> Security
			* Isolate Mac from virtual machine
			* Time Machine: do not backup
		* Virtual Machine -> Configure -> Options -> Advanced
			* Time: Do not sync
			* Copy & Paste: disable


## Optional, depends on what you want to do with the VM

* Install the 'Guest Additions' of your VM system for better speed and other integration.


# Run the playbook

* create a 'hosts' file in this folder and add a single line containing the VM's IP address
	* example: $ echo '10.211.55.20' > hosts
* run the playbook
	* you can use the 'run_playbook.sh' script: $ bash ./run_playbook.sh

