# SQS scripts

Fork of https://github.com/mercury2269/sqsmover

Project can be opensource on GitHub

## Requirements

- Go 1.12.x

## Usage

```
go mod vendor
go run main.go -s [source_queue_name] -d [destination_queue_name] -r [aws_region]
```
