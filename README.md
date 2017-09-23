# i3-qubes
Qubes OS rpm for i3 4.12

You'll find the full installation instructions and more information on https://sietse.no/i3-wm-in-qubes-os

## To install, follow these steps:

First, clone the repository in a vm (if needed, install git first):

```
user@vm$ git clone https://github.com/QubesOS/qubes-desktop-linux-i3.git
```

Then make sure all dependencies are installed:

```
user@vm$ sudo dnf install -y $(cat build-deps.list)
```

Build the srpms (this is required to download the source tarball):

```
user@vm$ make srpms

```

After that, build the rpm:

```
user@vm$ make rpms
```

Then, copy the rpm to your Dom0:
```
user@Dom0$ qvm-run --pass-io <vmname> 'cat /path/to/rpm/x86_64/i3-4.12-3.f23.x86_64.rpm' > i3-4.12-3.f23.x86_64.rpm
```

...and the same for the i3-settings-qubes rpm. 

And finally install it:

```
user@Dom0$ sudo yum localinstall i3-4.12-3.f23.x86_64.rpm
```

*NOTE* The above command doesn't work if dom0 is fedora 25 (as is the case in 4.0), and the equivalent `sudo qubes-dom0-update` won't work on your local rpm as it cannot be verified.



Log out, log in again and configure to your needs!

## Contributors
https://github.com/SietsevanderMolen
https://github.com/o-
https://github.com/minad
