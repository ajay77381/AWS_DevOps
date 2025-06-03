To install:

Install [Bison](https://www.gnu.org/software/bison/):

sudo apt-get install bison
Install gvm:

bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
> gvm version
 gvm listall

### now install the required version form the given version.
gvm install go1.4 -B

gvm use go1.4


![Image](https://github.com/users/agileguru/projects/24/assets/130822600/f37f2e2c-62eb-4d12-8e4e-b919fc5b5276)



go version

test@DESKTOP-M8NEQM2:~$ gvm use go1.4 --default

![Image](https://github.com/users/agileguru/projects/24/assets/130822600/d5a1bcd9-68c5-4df7-925f-d9a8a2545ba4)

Now using version go1.4

test@DESKTOP-M8NEQM2:~$ cd .gvm/gos

test@DESKTOP-M8NEQM2:~/.gvm/gos$ ls

go1.4
test@DESKTOP-M8NEQM2:~/.gvm/gos$



### Additional options can be specified when installing Go:
Usage: gvm install [version] [options]
    -s,  --source=SOURCE      Install Go from specified source.
    -n,  --name=NAME          Override the default name for this version.
    -pb, --with-protobuf      Install Go protocol buffers.
    -b,  --with-build-tools   Install package build tools.
    -B,  --binary             Only install from binary.
         --prefer-binary      Attempt a binary install, falling back to source.
    -h,  --help               Display this message.

A Note on Compiling Go 1.5+
Go 1.5+ removed the C compilers from the toolchain and [replaced](https://docs.google.com/document/d/1OaatvGhEAq7VseQ9kkavxKNAfepWy2yhPUBs96FGV28/edit) them with one written in Go. Obviously, this creates a bootstrapping problem if you don't already have a working Go install. In order to compile Go 1.5+, make sure Go 1.4 is installed first. If Go 1.4 won't install try a later version (e.g. go1.5), just make sure you have the -B option after the version number.

gvm install go1.4 -B
gvm use go1.4
export GOROOT_BOOTSTRAP=$GOROOT
gvm install go1.7



A Note on ARMv6 and ARMv7 architectures (32 bit)
Binary versions for ARMv6 architecture are available [starting from Go 1.6](https://go.dev/dl/#go1.6). So, it is necessary to bootstrap with an existing binary version, then it will be possible compiling other versions. For instance, to bootstrap a setup, version 1.21.0 may be used:

gvm install go1.21.0 -B
gvm use go1.21.0

And then, compile any other version:

gvm install go1.20.7

Go 1.20+ requires go1.17.3+. Use the below:

gvm install go1.4 -B
gvm use go1.4
export GOROOT_BOOTSTRAP=$GOROOT
gvm install go1.17.13
gvm use go1.17.13
export GOROOT_BOOTSTRAP=$GOROOT
gvm install go1.20
gvm use go1.20

# List Go Versions

To list all installed Go versions (The current version is prefixed with "=>"):

gvm list

To list all Go versions available for download:

gvm listall

## Uninstalling

To completely remove gvm and all installed Go versions and packages:

gvm implode

