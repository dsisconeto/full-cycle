FROM golang:1.8 as builder

WORKDIR /usr/src/app
COPY . .
RUN go build  -o ./code_education


FROM scratch
COPY --from=builder /usr/src/app/code_education  /usr/local/bin/code_education
CMD ["code_education"]