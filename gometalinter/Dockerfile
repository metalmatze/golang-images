FROM golang:1.9 as builder
RUN go get -u github.com/alecthomas/gometalinter && gometalinter --install

FROM golang:1.9
COPY --from=builder /go/bin/* /usr/bin/
ENTRYPOINT ["/usr/bin/gometalinter"]
