Command Vagrant commands

Below are some commonly used vagrant commands:

1] ``vagrant init <name of the box>``

This initializes vagrant and creates a vagrant file that will be used to bring up vagrant box.
The vagrant file consist of all required metadata in 'Basic' note.

2] `` vagrant up ``

This reads the vagrant file and brings up the box as per specified settings.

If you keep your virtualbox open, you will see a new VM machine created and running.

3] `` vagrant suspend ``

This saves the state of the box and suspends the guest machine.

4] `` vagrant resume ``

Resumes the box from suspended state

5] ``vagrant destroy``

Kills the guest machine.

6] ``vagrant reload ``

If you make any changes to the vagrant file, you need to reboot the guest box for changes to take effect. Reload simply reboots the OS.

In your virtualbox, you will actually see the box going down and powering on.

7] ``vagrant ssh``

You can use this command to SSH into your VM box. Once you ssh, you can do any of the OS stuff - installing application, performing updates, etc.

However, this is not standard method to do so and usually we use vagrant file's provision settings for achieving this.

8] ``vagrant global-status``

Lists all the vagrant environments that are currently running.
Each environment will have a specific ID that will be displayed in the output of above command.

You can use that ID with specific commands, for eg-- to suspend a specific vagrant environment:
``vagrant suspend <id>``

Note: A suspended VM will also be listed under global-status. You can halt a VM to remove the session.


