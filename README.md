Description
This Vagrant box is used for starting a CI environment. It contains essential CI tools such as Java JDK, Maven, Selenium, Jenkins, Xvfb and Firefox. With this, a fully functional environement for testing and integration jobs can be easily created.

CI Vagrant Box uses Puppet for provisioning required services and components and is configurable. There are two ways of using this box:

Using already provisioned and packed Vagrant Box
Provisioning a new box
Requirements
Vagrant 1.8.1 or later
Latest Vagrant version can be found on: https://www.vagrantup.com/downloads.html.

Start a preconfigured, ready to use VM
Provisioning a new Box
First approach is easier and faster, it will get the already configured CI running with just two commands. The second approach is better if additional configuration is needed for your CI environment, but requires provisioning a new Vagrant environment.

Plug & Play
To start a preconfigured VM, following command should be executed:
vagrant init ubuntu/trusty64 && vagrant up

This will start a VM with following configuration:

Ubuntu/Trusty64 is running on port 8080 inside the started VM. To access it from your host machine, you'll have to add port forwarding to the generated Vagrantfile (ie. config.vm.network "forwarded_port", guest: 80, host: 8080)

Generated Vagrantfile can be further configured (for port forwarding, folder sharing etc).
