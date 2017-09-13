FROM golang:1.9-alpine
RUN apk add --no-cache -U ca-certificates git
RUN go get -u github.com/alecthomas/gometalinter && gometalinter --install

# TODO: Copy only installed binaries
