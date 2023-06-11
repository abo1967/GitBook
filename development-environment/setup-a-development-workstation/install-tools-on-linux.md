# Install Tools on Linux

### Transfer and run the Install Script

* Login on the Ubuntu VM
* Find out the IP address of the virtual machine.
  * It is shown when you log in.
  * You can also use ‘`ip addr show’`.
* On the Mac, open a terminal window (using Terminal, iTerm2, …).
* If the same IP address was previously used by another VM (or if you have reinstalled the VM), you will first need to delete the SSH key with:\
  **ssh-keygen -R \<ip\_address>**
* Copy the install script to the Ubuntu VM with:\
  **scp install-tools.sh \<username>@\<ip\_address>:/home/\<username>**
* Log on to the VM with:\
  **ssh \<ip\_address>**
* On the Ubuntu VM, run the script with root privileges with\
  **sudo ./install-tools.sh**
* When prompted to link the shared directory, before answering follow these steps:
  * On the VMware Fusion application, make sure to select the menu item Virtual Machine -> Sharing -> Sharing Settings…
  * Click on the ‘+’
  * Select the development directory to be shared.
  * Now you can go back on the terminal window and answer by typing ‘**y\<enter>**’
  * Select the proper directory.
