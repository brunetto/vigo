FROM ubuntu 

RUN apt-get update && apt-get install -y curl git gcc
#ca-certificates

# RUN mkdir -p /usr/local/share/ca-certificates/pixart
# COPY pixart.pem /usr/local/share/ca-certificates/pixart/
# RUN update-ca-certificates

RUN curl -SLO https://dl.google.com/go/go1.10.3.linux-amd64.tar.gz 

RUN tar -xzvf go1.10.3.linux-amd64.tar.gz 
RUN mv go go1.10

RUN git clone https://go.googlesource.com/go go.tip -b master 

ENV GOROOT_BOOTSTRAP=/go1.10

RUN cd go.tip/src && ./make.bash 
ENV PATH=$PATH:/go.tip/bin