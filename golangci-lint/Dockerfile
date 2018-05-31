FROM alpine:3.7

#RUN curl -L https://github.com/alecthomas/gometalinter/releases/download/v2.0.5/gometalinter-2.0.5-linux-amd64.tar.gz > /tmp/gometalinter.tar.gz && \
#	tar -zxvf /tmp/gometalinter.tar.gz -C /tmp && \
#	mv /tmp/gometalinter-2.0.5-linux-amd64/* /usr/bin/
RUN apk add -U --no-cache curl

RUN curl -L https://github.com/golangci/golangci-lint/releases/download/v1.3.7/golangci-lint-1.3.7-linux-amd64.tar.gz > /tmp/golangci-lint.tar.gz && \
	tar -zxvf /tmp/golangci-lint.tar.gz -C /tmp && \
	mv /tmp/golangci-lint-1.3.7-linux-amd64/golangci-lint /usr/bin/ && \
	rm -rf /tmp/*

ENTRYPOINT ["/usr/bin/golangci-lint"]
