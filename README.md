# Tribler           [![Build Status](http://jenkins.tribler.org/job/Test_tribler_devel/badge/icon)](http://jenkins.tribler.org/job/Test_tribler_devel/)

_Making Bittorrent anonymous and impossible to shutdown._

We use our own dedicated Tor-like network for anonymous torrent downloading. We implemented and enhanced the _Tor protocol specifications_ plus merged them with Bittorrent streaming. More info: https://github.com/Tribler/tribler/wiki
Tribler includes our own Tor-like onion routing network with hidden services based seeding and end-to-end encryption, detailed specs: https://github.com/Tribler/tribler/wiki/Anonymous-Downloading-and-Streaming-specifications

The aim of Tribler is giving anonymous access to online (streaming) videos. We are trying to make privacy, strong cryptography and authentication the Internet norm.

Tribler currently offers a Youtube-style service. For instance, Bittorrent-compatible streaming, fast search, thumbnail previews and comments. For the past 9 years we have been building a very robust Peer-to-Peer system. Today Tribler is robust: "the only way to take Tribler down is to take The Internet down" (but a single software bug could end everything).

## Build dependencies

We make use of submodules, so remember using the --recursive argument when cloning this repo.

### Debian/Ubuntu/Mint

```bash
sudo apt-get install libav-tools libjs-excanvas libjs-mootools libx11-6 python-apsw \
python-cherrypy3 python-feedparser python-gmpy python-libtorrent python-m2crypto \
python-netifaces python-pyasn1 python-requests python-twisted python-wxgtk2.8 vlc
```

### Windows and OSX
TODO

## Running Tribler from this repository
### Unix
First clone the repository:

```bash
git clone --recursive  git@github.com:Tribler/tribler.git
```

or, if you don't have added your ssh key to your github account:

```bash
git clone --recursive  https://github.com/Tribler/tribler.git
```

Done!
Now you can run tribler by executing the tribler.sh script on the root of the tree:

```bash
./tribler.sh
```
### Windows
TODO

# Submodule notes
 - As updated submodules are in detached head state, remember to check out a branch before commiting changes on them.
 - If you forgot to check out a branch before doing a commit, you should get a warning telling you about it. To get the commit to a branch just check out the branch and do a git cherry-pick of the commit.
 - Take care of not accidentally commiting a submodule change with git commit -a
 - Do not commit a submodule update without running all the tests first and making sure the new code is not breaking Tribler.
