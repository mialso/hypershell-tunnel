# pipe experiments

## private llm inference p2p-share example

### setup

```shell
npm ci
npm run init:keyfile:lm
npm run init:keyfile:mx
# for the client - get the public key - should be added to a server "firewall" whitelist
```

> note: "ssh" suffix for a complete ssh-like shell

### server

```shell
# start listen
npm run start:server:mx
npm run start:server:lm
# obtain public key - use later for client "known_peers"
```

### client

* add server public key to `~/.hypershell/known_peers`
> note: first time, there would be no folder, hence can
> `npm run start:client:mx` which would end with an error but create the folder

```txt
# <name> <public key>
lm-provider 1234..<key>..6789
mx-provider 9876..<key>..4321
```
> note: "llm-provider" name is required to connect to the server

```shell
npm run start:client:lm
npm run start:client:mx
```

> opencode: checkout opencode.json config example to setup
