git-pbuilder
============

This a fork of Russ Allberys git-pbuilder script which makes
building Debian packages (for Debian and Ubuntu)
with [git-buildpackage]
(https://honk.sigxcpu.org/piki/projects/git-buildpackage/)
a lot easier.

git-buildpackage actually includes a copy of git-pbuilder, but
that version have some deficencies when building "cross-distributor"
packages.

* The ```source.changes``` file is removed form the build-area.
This makes building packages for upload to a PPA uneccessary complex.

* The BASE files are named base-$DIST, whereas Ubuntu tools like 
backportpackage use $DIST-base.

* Support for the appropriate keyring (Debian or Ubuntu) in debootstrapopts
