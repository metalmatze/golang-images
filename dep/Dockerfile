FROM golang:1.9
RUN go get -v -u github.com/golang/dep/cmd/dep
RUN CGO_ENABLED=0 go install -v -ldflags '-w -extldflags '-static'' github.com/golang/dep/cmd/dep
ENTRYPOINT ["/go/bin/dep"]
