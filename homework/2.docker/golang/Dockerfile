FROM golang:alpine3.17 as builder
WORKDIR /app
COPY . /app/
RUN go build -o app .

FROM scratch
WORKDIR /app
COPY --from=builder /app/app /app/
EXPOSE 8080
ENTRYPOINT ["/app/app"]
