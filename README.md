## Build Your Own Boxes

First, install [Packer](http://packer.io) and then clone this project.

Inside the `packer` directory, a JSON file describes each box that can be built. You can use `packer build` to build the
boxes.

    $ packer build debian-7.4-i386.json

If you want to use a another mirror site, use mirror variable.

    $ packer build -var 'mirror=http://ftp.jaist.ac.jp/pub/Linux/debian-cdimage/release' debian-7.4-i386.json

If you only have VMware or VirtualBox available, you may also tell Packer to build only that box.

    $ packer build -only=virtualbox-iso debian-7.4-i386.json

