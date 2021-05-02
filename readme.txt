# built on ubuntu 20.04 focal

apt-get install autoconf automake pkg-config libavahi-client-dev
git clone https://github.com/ravelox/pimidi.git
cd pimidi/raveloxmidi
git checkout v0.10.3
./autogen.sh
./configure --prefix /opt/raveloxmidi
make
make install

tar czf /tmp/opt-raveloxmidi-0.10.3-focal-armv7l.tar.gz /opt/raveloxmidi
tar czf /tmp/opt-raveloxmidi-0.10.3-focal-aarch64.tar.gz /opt/raveloxmidi
tar czf /tmp/opt-raveloxmidi-0.10.3-focal-x86_64.tar.gz /opt/raveloxmidi
