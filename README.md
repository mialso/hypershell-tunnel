# pipe experiments

## private llm inference p2p-share example

### setup
* lm: lm-studio runtime (runs multiple models, slow, need exact model-id)
* mx: mlx-openai-server main model
* mx-sm: mlx-openai-server small model

```shell
npm ci
npm run init:keyfile:lm
npm run init:keyfile:mx
npm run init:keyfile:mx-sm
# for the client - get the public key - should be added to a server "firewall" whitelist
```

> note: "ssh" suffix for a complete ssh-like shell

### server

```shell
# start listen
npm run start:server:mx
npm run start:server:mx-sm
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
mx-sm-provider 9876..<key>..4321
```
> note: "llm-provider" name is required to connect to the server

```shell
npm run start:client:lm
npm run start:client:mx
npm run start:client:mx-sm
```

### copy files
```shell
# start server on a peer (llm-host) machine
npm run start:server:ssh
# target machine
npm run copy:llm-host @llm-host:/Users/me/.cache/huggingface/hub/models--mlx-community--MiniMax-M2.5-8bit-gs32 /media/me/llm-storage/llm-hub/models--mlx-community--MiniMax-M2.5-8bit-gs32
```
> ensure "llm-host" is set correct at `~/.hypershell/known_peers`

### opencode: checkout opencode.json config example to setup
```bash
ipconfig getifaddr en1
rsync -ahP user@192.168.68.108:/Users/user/.cache/huggingface/hub/models--mlx-community--Qwen3.5-4B-8bit ~/.cache/huggingface/hub/
```

### Git server
```bash
git daemon --reuseaddr --verbose --base-path=/Users/user/storage/git --export-all --listen=127.0.0.1 --port=9094 --enable=receive-pack /Users/user/storage/git
```
