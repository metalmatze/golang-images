FROM golang:1.9 as builder
RUN go get -u github.com/golang/dep/cmd/dep
RUN CGO_ENABLED=0 go install -v -ldflags '-w -extldflags '-static'' github.com/golang/dep/cmd/dep
RUN ls -lah $GOPATH/bin/dep

FROM alpine:latest
RUN apk --no-cache add ca-certificates
COPY --from=builder /go/bin/dep /usr/bin/
ENTRYPOINT ["/usr/bin/dep"]
