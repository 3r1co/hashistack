FROM ubuntu:17.04

RUN apt-get update && \  
	apt-get install -y ca-certificates wget unzip


RUN wget -q https://releases.hashicorp.com/packer/1.0.3/packer_1.0.3_linux_amd64.zip && \
	unzip packer_1.0.3_linux_amd64.zip && \
	mv packer /usr/local/bin/packer && \
	chmod +x /usr/local/bin/packer && \
	rm -rf packer_1.0.3_linux_amd64.zip

RUN mkdir /packer

WORKDIR "/packer"
VOLUME ["/packer"]

ENTRYPOINT ["packer"]
CMD ["-v"]
