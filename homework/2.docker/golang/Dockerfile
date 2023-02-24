FROM golang:alpine3.17 as builder
WORKDIR /app_go_less2
COPY . ./
RUN go build -o app .

FROM scratch
WORKDIR /app_go_less2
COPY --from=builder /app_go_less2/app /app_go_less2/
EXPOSE 8080
ENTRYPOINT ["/app_go_less2/app"]
