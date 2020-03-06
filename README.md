# i3lock-color
A fork of [i3lock](https://github.com/i3/i3lock): "improved screen locker".  

## Usage
Simply invoke the 'i3lock' command. To unlock, enter your password and press enter.  

There are a number of undocumented options in i3lock.c: `struct option longopts[]`.  

A [sample script](https://github.com/PandorasFox/i3lock-color/blob/master/lock.sh) is included in this repository. [Here](https://streamable.com/fpl46) is a short clip of that script in action!  

## Building
### Build and Install
```bash
# [optional] git tag -f "git-$(git rev-parse --short HEAD)"
autoreconf -i
./configure --disable-sanitizers
make
sudo make install
```
### Required Packages

#### openSUSE Tumbleweed
```bash
sudo zypper in -y \
	autoconf \
	automake \
	cairo-devel \
	libev-devel \
	libjpeg8-devel \
	libxcb-devel \
	libxkbcommon-devel \
	libxkbcommon-x11-devel \
	pam-devel \
	pkgconf-pkg-config \
	xcb-util-devel \
	xcb-util-image-devel \
	xcb-util-xrm-devel
```
