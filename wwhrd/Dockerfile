FROM golang:1.9 as builder
RUN go get -v -u github.com/frapposelli/wwhrd
RUN CGO_ENABLED=0 go install -v -ldflags '-w -extldflags '-static'' github.com/frapposelli/wwhrd

FROM alpine
COPY --from=builder /go/bin/wwhrd /usr/bin/
ENTRYPOINT ["/usr/bin/wwhrd"]
