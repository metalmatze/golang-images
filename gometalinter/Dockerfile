FROM golang:1.10

RUN curl -L https://github.com/alecthomas/gometalinter/releases/download/v2.0.5/gometalinter-2.0.5-linux-amd64.tar.gz > /tmp/gometalinter.tar.gz && \
	tar -zxvf /tmp/gometalinter.tar.gz -C /tmp && \
	mv /tmp/gometalinter-2.0.5-linux-amd64/* /usr/bin/

ENTRYPOINT ["/usr/bin/gometalinter"]
