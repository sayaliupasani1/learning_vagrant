Vagrant synced folder

- To share a specific folder on host machine within the guest VM:

`` config.vm.synced_folder "./", "/vagrant"``

The first parameter: which folder on host machine should be available on the guest VM
2nd parameter: where should this folder be available within the VM

By default, the current directory is shared in the location /vagrant on the guest machine.

You can improve performance by using NFS for file sharing. To do so, you need to specify type as:

`` config.vm.synced_folder ".", "/vagrant", type: "nfs"``

Note: NFS requires nfsd to be installed on your host. Its present by default on MAC.
With virtualbox, you need to use private network with static IP to use NFS.

NFS does not work with windows host.
