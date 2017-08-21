FROM ubuntu:17.04

RUN apt-get update && \  
	apt-get install -y ca-certificates wget unzip


RUN wget http://releases.hashicorp.com/vault/0.7.3/vault_0.7.3_linux_amd64.zip && \
	unzip vault_0.7.3_linux_amd64.zip && \
	mv vault /usr/local/bin/vault && \
	chmod +x /usr/local/bin/vault && \
	rm -rf vault_0.7.3_linux_amd64.zip

#ADD vault /usr/local/bin/vault
RUN mkdir /vault

WORKDIR "/vault"
VOLUME ["/vault"]

ENTRYPOINT ["vault"]
CMD ["-v"]
