Provisioners

*Shell Provisioner:*

2 ways: Inline, separate provisioning file.

Inline: Place the script content within Vagrantfile
Separate: Specify path to provision file within VagrantFile.

Define provision method in vagrant file as: ``config.vm.provision``

*Inline:*

``config.vm.provision "shell", inline: "ls -la /vagrant"``

This will run the specified command on to the VM shell and display the output on terminal running vagrant.

*Using separate file:*

``config.vm.provision "shell", path: "script.sh"``

Where script.sh is relative or absolute path pointing to the provisioning script.

**Note:**

By default, provisioner runs only once - when you run the vagrant up for first time and/or after machine was destroyed.

If the environment was already created and provisioning has happened once, you can re-run it by using below command:

``vagrant up --provision``

If the machine is already running and you need to execute provisioning:

`` vagrant provision``

or

`vagrant reload --provision` (This will reboot he VM before running the provisioning)

You can choose to always run the provisioning using below flag in vagrantfile:

`` vagrant.configure(2) do |config|``
    ``config.vm.provision "shell", run: "always" do |s|``
        ``s.inline = "echo Hello"``
    ``end``
``end``
