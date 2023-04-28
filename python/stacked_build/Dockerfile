# Pull from previous build image
FROM jessej2605/centos_special:latest

# Set working directory
WORKDIR /usr/src

# Download Python 3.11 source 
RUN wget https://www.python.org/ftp/python/3.11.2/Python-3.11.2.tgz

RUN tar xzf Python-3.11.2.tgz
RUN cd Python-3.11.3 && /
RUN LD_LIBRARY_PATH=/usr/local/lib ./configure --prefix=/usr/local/python3.11 --enable-optimizations --enable-shared &&/



    




