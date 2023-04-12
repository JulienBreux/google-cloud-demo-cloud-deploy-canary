ARG GO_VERSION=1.20

FROM golang:${GO_VERSION}-alpine AS build

WORKDIR /go/src/app

COPY . .

RUN go mod download
RUN CGO_ENABLED=0 go build -o /go/bin/app

FROM gcr.io/distroless/static

LABEL maintainer="Julien BREUX <julienbreux@google.com>"
USER nonroot:nonroot

COPY --from=build --chown=nonroot:nonroot /go/bin/app /

ENTRYPOINT ["/app"]