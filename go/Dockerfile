FROM golang:1.10

WORKDIR /go/src/app
COPY . .
RUN go get -u github.com/golang/dep/cmd/dep
RUN dep ensure
RUN go build

FROM gcr.io/distroless/base
COPY --from=build /go/bin/app /
CMD ["/app"]