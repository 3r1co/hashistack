FROM ubuntu:17.04

RUN apt-get update && \  
	apt-get install -y ca-certificates wget unzip


RUN wget -q https://releases.hashicorp.com/consul/0.8.5/consul_0.8.5_linux_amd64.zip && \
	unzip consul_0.8.5_linux_amd64.zip && \
	mv consul /usr/local/bin/consul && \
	chmod +x /usr/local/bin/consul && \
	rm -rf consul_0.8.5_linux_amd64.zip

RUN mkdir /consul

WORKDIR "/consul"
VOLUME ["/consul"]

ENTRYPOINT ["consul"]
CMD ["-v"]
