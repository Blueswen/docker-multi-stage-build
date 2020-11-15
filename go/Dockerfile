FROM golang:alpine3.12 AS builder
WORKDIR /workspace
COPY . /workspace/
RUN go build -o hello-world

FROM busybox:1.32.0
WORKDIR /workspace
COPY  --from=builder /workspace/hello-world .
CMD ./hello-world
