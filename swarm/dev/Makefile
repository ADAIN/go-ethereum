.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/ADAIN/go-ethereum-genesis-test/cmd/swarm
	go build -o bin/geth     github.com/ADAIN/go-ethereum-genesis-test/cmd/geth
	go build -o bin/bootnode github.com/ADAIN/go-ethereum-genesis-test/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/ADAIN/go-ethereum-genesis-test/swarm/...
