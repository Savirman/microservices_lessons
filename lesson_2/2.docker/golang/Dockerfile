FROM golang:latest as builder
RUN mkdir /app
COPY . /app
WORKDIR /app
RUN CGO_ENABLED=0 GOOS=linux GOArCH=amd64 go build -o server .
FROM scratch
COPY --from=builder /app/server /
EXPOSE 9000
CMD ["/server"]

