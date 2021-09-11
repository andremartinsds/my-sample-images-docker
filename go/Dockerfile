FROM golang:1.14-alpine AS build

WORKDIR /app/src
COPY main.go go.* /app/src/
RUN CGO_ENABLED=0 go build -o /bin/maingo

FROM scratch
COPY --from=build /bin/maingo /bin/maingo
ENTRYPOINT ["/bin/maingo"]
CMD ["app"]