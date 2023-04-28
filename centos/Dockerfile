# Use the latest CentOS 7 image as the base
FROM centos:7

# Set the user to root
USER root

# Install the required packages
RUN yum -y update 

# Add repo for MS Code
RUN rpm --import https://packages.microsoft.com/keys/microsoft.asc && \
    sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

# Add rpm for GIT LFS
RUN curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.rpm.sh | bash

# # Add NI Driver Repo
# ENV START_PATH=$(pwd)

# RUN mkdir -p /etc/yum.repos.d/ni
# RUN rpm -i ni-software2019> /etc/yum.repos.d/ni/ni.repo

# Install the required packages
RUN yum -y install \
    autoconf\
    binutils \
    blas-devel \
    cmake \
    code \
    cpio \
    curl-devel \
    dos2unix \
    expat-devel \
    epel-release \
    gcc \
    gcc-c++ \
    gdbm-devel \
    git \
    git-gui \  
    git-lfs \
    git-svn \
    glibc-devel \
    glibc-devel.i686 \
    gmp-devel \
    lapack-devel \
    libffi-devel \
    libmpc-devel \
    libtool \
    libusb \
    libxml2-devel \
    libxslt-devel \
    make \ 
    minicom \
    mpfr-devel \
    ni-daqmx \
    ni-dmm \
    ni-iotrace \
    ni-pxiplatformservices \
    ni-switch \
    ni-switch-daqmx \
    ni-visa \
    openssh-clients \
    openssl-devel \
    perl-ExtUtils-MakeMaker \
    phonon-devel \
    python \   
    python-devel \
    python-pip \
    qt5-qtbase \
    qt5-qtbase-devel \
    qt5-qtbase-examples \
    qt5-qtbase-doc \  
    qt-creater \
    qt-devel \  
    readline-devel \
    rpmdevtools \
    rsh \
    rsh-server \
    sqlite-devel \
    tcl \
    tcsh \
    tk-devel \
    wget \
    which \
    xz-devel \
    xz-libs \
    zlib-devel* \

# Install the required python packages
RUN yum -y groupinstall "Development Tools" --setopt=group_package_types=mandatory,default,optional
RUN yum -y groupinstall "MATE Desktop"