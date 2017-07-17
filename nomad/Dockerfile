FROM ubuntu:17.04

RUN apt-get update && \  
	apt-get install -y ca-certificates wget unzip


RUN wget -q https://releases.hashicorp.com/nomad/0.5.6/nomad_0.5.6_linux_amd64.zip && \
	unzip nomad_0.5.6_linux_amd64.zip && \
	mv nomad /usr/local/bin/nomad && \
	chmod +x /usr/local/bin/nomad && \
	rm -rf nomad_0.5.6_linux_amd64.zip

RUN mkdir /nomad

WORKDIR "/nomad"
VOLUME ["/nomad"]

ENTRYPOINT ["nomad"]
CMD ["-v"]
