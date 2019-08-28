# SQS scripts

[![Build Status](https://travis-ci.org/neo9/sqsmv.svg?branch=master)](https://travis-ci.org/neo9/sqsmv)


Fork of https://github.com/mercury2269/sqsmover

## Requirements

- Go 1.12.x

## Usage

- `--source / -s`: Source queue name
- `--destination / -d`: Destination queue name
- `--region / -r`: AWS region


Environment variables:

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`

## Dev usage

```
go mod vendor
go run main.go -s [source_queue_name] -d [destination_queue_name] -r [aws_region]
```
