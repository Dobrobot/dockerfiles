FROM ubuntu:14.04
RUN apt update
RUN apt-get install -y gawk git gnupg flex bison gperf build-essential \
	zip curl libc6-dev x11proto-core-dev \
	libgl1-mesa-dev g++-multilib tofrodos \
	python-markdown libxml2-utils xsltproc \
	lib32z1 bc busybox wget
RUN git clone https://github.com/friendlyarm/h5_lichee.git lichee --depth 1
WORKDIR /lichee/brandy/toolchain/
RUN wget http://bxd.snop.org/dev/gcc-linaro-arm-4.6.3.tar.xz
RUN wget http://bxd.snop.org/dev/gcc-linaro-aarch64.tar.xz 
WORKDIR /lichee/fa_tools
RUN ./build.sh -b nanopi-neo2 -p linux -t all; exit 0
CMD ["bash"]
