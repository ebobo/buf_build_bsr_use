# use buf.build BSR demo

The purpose of this repository is to demonstrate how to use the services offered by [buf.build](https://buf.build/) for hosting protobuffer definitions and automatic code generation for protobuffers and gRPC services.

This means that the developer **does not have to**:

- install the `buf` tool
- does not have to deal directly with the `.proto` files
- does not have to do code generation

## Building

If you have Go and make installed you should be able to just execute

```shell
make
```

to build the project. The binaries will be in `bin`.

## How do you use it?

In this example we are using the [test](https://buf.build/ebobo/test) module hosted on [buf.build](https://buf.build/).

If you look in [cmd/server/main.go](cmd/server/main.go) you simply add `"go.buf.build/library/go-grpc/ebobo/test/userpb/v1"` to your imports, run `go mod tidy` and that's that. Now you can use all the generated types from the project.

The docs for the API are hosted here.

## Limited to Go (for now)

In this project, I will try to test more languages which buf.build remote code generation support in the future.
