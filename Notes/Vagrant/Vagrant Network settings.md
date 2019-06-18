Vagrant Network settings

- By default vagrant creates a guest with NAT masquerade network with host.
- Although you are able to access internet from guest with this network settings, outside world cannot access this VM.
- Private network: 

eg: ``config.vm.network: private, ip: "192.168.33.10"``

This creates a separate interface on your VM. Mostly used so that other devices in the same private network can access the VM for testing.

- You can port forward so that the traffic incoming on host machine's specific port can be forwarded to the guest machine listening on specified port.

eg" ``config.vm.network "forward_port", guest: 80, host: 8080``

Requests to localhost:8080 will be forwarded to VM's IP:80

Note: If you run multiple VMs with same settings, it will lead to collision and vagrant will throw an error.

