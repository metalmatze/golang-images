FROM golang:1.9 as builder
RUN go get -v -u github.com/golang/dep/cmd/dep
RUN CGO_ENABLED=0 go install -v -ldflags '-w -extldflags '-static'' github.com/golang/dep/cmd/dep

FROM golang:1.9
COPY --from=builder /go/bin/dep /usr/bin/
ENTRYPOINT ["/usr/bin/dep"]
