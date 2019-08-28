# SQS scripts

[![Build Status](https://travis-ci.org/neo9/sqsmv.svg?branch=master)](https://travis-ci.org/neo9/sqsmv)


Fork of https://github.com/mercury2269/sqsmover

Move messages from queue A to queue B.
Useful to manage dead letter queues

## Requirements

- Go 1.12.x

## Features

- Reliable delivery. Messages are only deleted from the original queue if they were successfully un-queued to the destination.
- Messages are sent and received in batches for faster processing.
- Progress indicator.
- Queue name resolution. For ease of use, you only need to provide a queue name and not the full arn address.

## Installation

Binaries are available in the releases section

## Usage

```
usage: main --source=SOURCE --destination=DESTINATION [<flags>]

Flags:
      --help                     Show context-sensitive help (also try --help-long and --help-man).
  -s, --source=SOURCE            Source queue to move messages from
  -d, --destination=DESTINATION  Destination queue to move messages to
  -r, --region="us-west-2"       AWS Region for source and destination queues

```

Environment variables:

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`

## Dev usage

```
go mod vendor
go run main.go -s [source_queue_name] -d [destination_queue_name] -r [aws_region]
```
