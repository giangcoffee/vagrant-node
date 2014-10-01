# vagrant-node

vagrant-node is the virtual machine used for Node.js development.

## Installation

First of all you need to set up SSH agent forwarding for the key you use to authenticate with GitHub. Run

    $ ssh-add -l

and verify whether that key is listed. If so, everything is fine, if not, run the following command.

    $ ssh-add ~/.ssh/id_rsa

Next, you need to have [Vagrant](http://www.vagrantup.com/) and either VMware or VirtualBox installed. Once you have done this, you are ready to setup the virtual machine.

For that, first clone this repository. As the virtual machine will automatically provide all directories that share the same parent, you probably want to put it into a directory next to your projects' directories.

## Quick Start

To run the virtual machine, change to the directory you cloned into and run the following command.

    $ vagrant up

If you want to ssh into the virtual machine run the following command. Please note that insie of the virtual machine you will automatically be taken to the `~/projects` folder that contains all your projects.

    $ vagrant ssh

Apart from that, any other Vagrant command will work as well, such as `vagrant status`, `vagrant halt` or `vagrant destroy`.

### Trying GitHub access

To verify that SSH agent forwarding was setup successfully, ssh into the virtual machine and run the following command.

    $ ssh -T git@github.com

If the output is

> Hi <username>! You've successfully authenticated, but GitHub does not provide shell access.

everything is fine. If not, please consider the documentation for SSH.

## License

The MIT License (MIT)
Copyright (c) 2014 the native web.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.