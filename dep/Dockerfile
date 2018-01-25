FROM alpine as builder
RUN cd /tmp && wget https://github.com/golang/dep/releases/download/v0.4.1/dep-linux-amd64

FROM alpine
COPY --from=builder /tmp/dep-linux-amd64 /usr/bin/dep
RUN chmod +x /usr/bin/dep

ENV PATH=/go/bin:/usr/local/go/bin:$PATH
ENV GOPATH=/go

ENTRYPOINT ["/usr/bin/dep"]
