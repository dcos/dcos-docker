#
# THIS FILE IS AUTOGENERATED; SEE "build/base/generate.sh"!
#

FROM ubuntu:xenial

RUN apt-get update \
	&& apt-get install -y \
		aufs-tools \
		bash-completion \
		btrfs-tools \
		ca-certificates \
		curl \
		debianutils \
		gawk \
		git \
		iproute \
		ipset \
		iptables \
		iputils-ping \
		libcgroup-dev \
		libpopt0 \
		nano \
		net-tools \
		openssh-client \
		openssh-server \
		sudo \
		systemd \
		tar \
		tree \
		unzip \
		vim-nox \
		xz-utils \
	&& rm -rf /var/lib/apt/lists/* \
&& ( \
cd /lib/systemd/system/sysinit.target.wants/; \
for i in *; do \
if [ "$i" != "systemd-tmpfiles-setup.service" ]; then \
rm -f $i; \
fi \
done \
) \
&& rm -f /lib/systemd/system/multi-user.target.wants/* \
&& rm -f /etc/systemd/system/*.wants/* \
&& rm -f /lib/systemd/system/local-fs.target.wants/* \
&& rm -f /lib/systemd/system/sockets.target.wants/*udev* \
&& rm -f /lib/systemd/system/sockets.target.wants/*initctl* \
&& rm -f /lib/systemd/system/anaconda.target.wants/* \
&& rm -f /lib/systemd/system/basic.target.wants/* \
&& rm -f /lib/systemd/system/graphical.target.wants/* \
&& ln -vf /lib/systemd/system/multi-user.target /lib/systemd/system/default.target

# systemd needs a different stop signal
STOPSIGNAL SIGRTMIN+3
CMD ["/sbin/init"]