VagrantFile

- This file defines your machine settings and how provisioning will happen.
- It is usually placed in the root of your project directory (From where you init the vagrant using box image)
- It uses Ruby language
- Elements it includes - Refer note 'Basics'
- Each vagrantfile has below line by default:

`vagrant.configure("2")`

This defines the configuration version. 2 is currently the latest one and hence we keep this line intact.
Each version has specific config options and changing this might lead to errors.

- post-up messages:

Recent version of vagrant can include this:

``config.vm.post_up_message``

This way you can create a message that will be displayed after vagrant up is performed.

eg: ``config.vm.post_up_message="Web app running on 10.10.10.10``


