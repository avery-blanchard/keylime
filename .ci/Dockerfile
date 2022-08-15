FROM fedora:latest
RUN dnf update -y 
RUN dnf install -y git 
RUN git clone https://github.com/keylime/keylime.git && cd keylime && cp keylime.conf /etc/keylime.conf 
RUN git clone -b ci https://github.com/avery-blanchard/rust-keylime.git
RUN dnf install -y vim automake clang clang-devel czmq-devel dbus dbus-daemon dbus-devel dnf-plugins-core efivar-devel gcc git glib2-devel glib2-static gnulib iproute kmod libarchive-devel libselinux-python3 libtool libtpms llvm llvm-devel make openssl-devel pkg-config procps python3-cryptography python3-dbus python3-devel python3-m2crypto python3-pip python3-requests python3-setuptools python3-sqlalchemy python3-tornado python3-virtualenv python3-yaml python3-zmq redhat-rpm-config rust clippy cargo swtpm swtpm-tools tpm2-abrmd tpm2-tools tpm2-tss tpm2-tss-devel uthash-devel wget which
RUN dnf groupinstall -y "Development Tools"
#RUN cargo install cargo-tarpaulin
ENV TPM_HOME=/root/swtpm2
ENV KEYLIME_HOME=/root/keylime
ENV HOME=/root
ENV KEYLIME_DIR=/var/lib/keylime
