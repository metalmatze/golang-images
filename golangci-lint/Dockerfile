FROM golang:1.10-alpine

RUN apk add -U --no-cache curl

RUN curl -L https://github.com/golangci/golangci-lint/releases/download/v1.3.7/golangci-lint-1.3.7-linux-amd64.tar.gz > /tmp/golangci-lint.tar.gz && \
	tar -zxvf /tmp/golangci-lint.tar.gz -C /tmp && \
	mv /tmp/golangci-lint-1.3.7-linux-amd64/golangci-lint /usr/bin/ && \
	rm -rf /tmp/*

ENTRYPOINT ["/usr/bin/golangci-lint"]
