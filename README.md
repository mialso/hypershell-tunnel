# pipe experiments

## setup

```shell
npm run init:keyfile
```

## server

```shell
# obtain public key - use later for client "known_peers"
cat ./keyfile
# start listen
npm run start:server
```

## client

* add server public key to `~/.hypershell/known_peers`

```txt
# <name> <public key>
llm-provider 1234..key..6789
```
> note: "llm-provider" name is required to connect to the server

```shell
npm run start:client
```

> opencode: checkout opencode.json config example to setup
