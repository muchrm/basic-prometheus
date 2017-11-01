FROM golang:1.9

WORKDIR /go/src/app
COPY . .
RUN go get -u github.com/golang/dep/cmd/dep
RUN dep ensure
ENTRYPOINT go run main.go
EXPOSE 8080