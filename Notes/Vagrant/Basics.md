Basics

1] When you initialize vagrant, it creates a vagrant file that consist of following basic stuff:

- Box settings:

It includes all the settings related to the box.

#config.vm.box --> Defines the box operating system

- Provider settings:

This includes settings related to the VM provider. (Default: Virtualbox). 
Includes: CPU, memory, processors, etc

#config.vm.provider

- Network settings:

This defines network configuration for guest machine - IP private network, port forwarding, etc

#config.vm.network

- Folder settings:

Define any shared folders between host and guest machine.

#config.vm.synced_folder

- Provision settings:

Defines what we want to setup with this box.

#config.vm.provision

If you don't make any edits to the created vagrant file (on vagrant init) - it brings up default virtualbox guest machine running image you specified while init vagrant
