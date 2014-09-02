ansible-osx-vagrant-ready
=========================

Ansible playbook to prepare a bare OS X VM for vagrant


# Manual Steps

## Not required but advised

* turn off the App Store automatic update
	* System Preferences -> App Store -> Automatically check for updates
* turn off sleep
	* System Preferences -> Energy Saver -> Change all options to 'never' and disable Hard disk sleep
* turn off every sharing between the VM and the Guest
	* in Parallels:
		* Virtual Machine -> Configure
		* Isolate Mac from virtual machine

## Optional, depends on what you want to do with the VM

* Install the 'Guest Additions' of your VM system for better speed and other integration.


# Run the playbook