# i3-qubes
Qubes OS rpm for i3 4.16

Full installation and building instructions can be found on:
https://www.qubes-os.org/doc/i3/

## Building from source

### Install the build dependencies

```
sudo dnf install -y $(cat build-deps.list)
```

### Build the rpm

```
make rpms
```

## Contributors

- https://github.com/SietsevanderMolen
- https://github.com/o-
- https://github.com/minad
