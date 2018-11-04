# HomeSafeButton
A client/server application for families to know who is currently home safe.

## Setup Instructions

### Developers

The client and communicate via grpc. In order to compile the proto files, install the grpc tools:

`python3 -m pip install grpc grpcio-tools googleapis-common-protos`.

Then, the proto messages can be compiled from the root of the git directory with:

`python3 -m grpc_tools.protoc -I=src/server/ --python_out=src/server src/server/homesafe.proto`.

This results in a generated `src/server/homesafe_pb2.py` file.