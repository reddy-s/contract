[![Build Status](https://dev.azure.com/reddyhorcrux/iot-computing/_apis/build/status/reddy-s.contract?branchName=master)](https://dev.azure.com/reddyhorcrux/iot-computing/_build/latest?definitionId=13&branchName=master)
# Contract artifact for all gRPC communication

## Generating code for Java 
```bash
./gradlew generateProto
```

## Generating files for Python
```bash
for file in $(ls ./src/main/proto); do
    python3 -m grpc_tools.protoc -I./src/main/proto --python_out=.python --grpc_python_out=.python ./src/main/proto/${file};
done
```