---
layout: ballerina-inner-page
title: How to generate Ballerina code for Protocol Buffer Definition
---

# How to generate Ballerina code for Protocol Buffer Definition

The `Protocol Buffers` to Ballerina tool provides capabilities to generate Ballerina source code for the Protocol
 Buffer definition. The code generation tool can produce `ballerina stub` and `ballerina service/client template
 ` files.
 
> In Ballerina, Protocol Buffers serialization is only supported in the gRPC module. Therefore, you can only use
> this tool to generate Ballerina source code for gRPC service definitions.

## CLI Command

You can generate Ballerina source code using the following command:

```
./ballerina grpc --input <proto-file-path> [--output <path>] [--mode client | server]
```

____**Options**____

`--input`  - Path of the input .proto file. This is a mandatory field. You need to provide the path of the definition
 file.

`--output` - Location of the generated Ballerina source files. This is an optional field. 
If output path is not specified, output will be written to a directory corresponding to the package in the Protocol
 Buffers definition. 
If package is not specified, output will be written to a 'temp' directory in the current location.

`--mode`   - Set the mode (client or server) to generate code samples. If not specified, only the stub file is
 generated.


## Sample

The below example shows how you can generate Ballerina source code from the following Protocol Buffers definition (in the `helloworld_service.proto` file).

```proto
syntax = "proto3";

service helloWorld {
    rpc sayHello(HelloRequest) returns (HelloResponse);
}

message HelloRequest {
	string name = 1;
}
message HelloResponse {
	string message = 1;
}
```

* You can run the following command to generate the client/service stub and service template.
```
$ ballerina grpc --input helloworld_service.proto --mode service --output service
```
Once you execute the command, the stub file(`helloworld_service_pb.bal`) and the service template file (`helloWorld_sample_service.bal`) are generated inside the service directory.

* You can run the following command to generate the client/service stub and client template.
```
$ ballerina grpc --input helloworld_service.proto --mode client --output client
```
Once you execute the command, the stub file(`helloworld_service_pb.bal`) and the service template file (`helloWorld_sample_client.bal`) are generated inside the client directory.

* You can run the following command to generate only the client/service stub.
```
$ ballerina grpc --input helloworld_service.proto --output stubs
```
Once you execute the command, only the stub file (`helloworld_service_pb.bal`) is generated inside the `stubs` directory.
