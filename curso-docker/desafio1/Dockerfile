FROM golang AS builder

WORKDIR /fullcycle

COPY hello.go go.mod /fullcycle

RUN go build hello.go

FROM scratch 

COPY --from=builder /fullcycle .

CMD ["./hello"]
