# gRPC -- As easy as func()

Tejas Manohar
Software Engineer at Segment

## How do Apps Communicate?

## Where do REST/HTTP/JSON shine?
- Human Readable Protocol
- Not SOAP
- Popular

## Where do REST/HTTP/JSON fall short?
- Leading machines in a sane direction
- Extremely basic
- Lots undefined
  - How does a REST API handle login?
  - Streaming
  - Bidirectional communication

>REST isn't really a standard. REST APIs are a suggestion/guideline/design principle.

## What is gRPC
> Calls another systems function over the network without considering the implementation details

- Is an open-source project based on "stubby"
- 'g' is for Google
- RPC stands for Remote Procedure Call

PB - Protocol Buffers (PB)
IDL - Interface Definition Language (IDL)

## Protobuf is binary
- Much smaller
- Must know location of fields to parse it
- Binary protocol so not human-readable
- Robust type system and data structures

## gRPC supports Go

## gRPC supports many paradigms
- Unary RPC
- Bidirectional Streaming
  - Client-side Streaming
  - Server-side Streaming

## gRPC supports streaming data both ways (a la websockets)

## gRPC has middleware (interceptors in gRPC)

## What's wrong wit gRPC
- Load balancing has a long way to go
- Go implementation is meh
- gRPC web is still a WIP
- Unstable api
- Relatively small community
