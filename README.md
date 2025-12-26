# pipe experiments

## private llm inference p2p-share example

### setup

```shell
npm ci
npm run init:keyfile
# for the client - get the public key - should be added to a server "firewall" whitelist
```

### server

```shell
# start listen
npm run start:server
# obtain public key - use later for client "known_peers"
```

### client

* add server public key to `~/.hypershell/known_peers`
> note: first time, there would be no folder, hence can
> `npm run start:client` which would end with an error but create the folder

```txt
# <name> <public key>
llm-provider 1234..key..6789
```
> note: "llm-provider" name is required to connect to the server

```shell
npm run start:client
```

> opencode: checkout opencode.json config example to setup
