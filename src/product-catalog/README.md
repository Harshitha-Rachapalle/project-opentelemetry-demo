# Product Catalog Service

When this service is run the output should be similar to the following

```export PRODUCT_CATALOG_PORT=8088```
```./product-catalog```

output:

 Loading Product Catalog...
 Loaded 10 products
 Product Catalog reload interval: 10
 Product Catalog gRPC server started on port: 8088

for json format:

```json
{"message":"successfully parsed product catalog json","severity":"info","timestamp":"2022-06-02T23:54:10.191283363Z"}
{"message":"starting grpc server at :3550","severity":"info","timestamp":"2022-06-02T23:54:10.191849078Z"}
```

## Local Build

To build the service binary, run:

```sh
go build -o product-catalog .
```

## Docker Build

From the root directory, run:

```sh
docker compose build product-catalog
```

## Regenerate protos

To build the protos, run from the root directory:

```sh
make docker-generate-protobuf
```

## Bump dependencies

To bump all dependencies run:

```sh
go get -u -t ./...
go mod tidy
```
