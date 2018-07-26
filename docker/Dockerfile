FROM ubuntu 

RUN apt-get update && apt-get install -y curl git ca-certificates

RUN mkdir -p /usr/local/share/ca-certificates/pixart
COPY pixart.pem /usr/local/share/ca-certificates/pixart/
RUN update-ca-certificates

RUN curl https://dl.google.com/go/go1.10.3.linux-amd64.tar.gz | \
        tar tvz --transform=s/go/go.10/g

RUN git clone https://go.googlesource.com/go go.tip -b master 
RUN cd go.tip/src
ENV GOROOT_BOOTSTRAP=$HOME/go1.10 
RUN ./make.bash 
RUN echo $HOME/go.tip/bin >> ~/.bashrc 
