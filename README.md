# Solana Relayer

## Setup

See https://jito-foundation.gitbook.io/mev/jito-relayer/running-a-relayer until Section "RPC Server" for setup instructions.

--> Create a new folder (e.g. "explorer-relayer") and add your jito-relayer authentication files: public.pem, private.pem, keypair.json

## Run

The easiest way to run the Explorer Relayer is to run our public docker image.

Example run command with a explorer-relayer at /home/ubuntu/explorer-relayer authentication folder and a local RPC running:

```shell
sudo docker run -d -v /home/ubuntu/explorer-relayer/:/home/ubuntu/explorer-relayer \
    --name=explorer-relayer \
    --restart=always \
    --network=host \
    --entrypoint=./jito-transaction-relayer explorerlabs/explorer-relayer:latest \
    --rpc-servers="http://127.0.0.1:8899" \
    --websocket-servers="ws://127.0.0.1:8900" \
    --keypair-path=/home/ubuntu/explorer-relayer/keypair.json \
    --signing-key-pem-path=/home/ubuntu/explorer-relayer/private.pem \
    --verifying-key-pem-path=/home/ubuntu/explorer-relayer/public.pem \
    --block-engine-url=https://amsterdam.mainnet.block-engine.jito.wtf \
    --explorer-engine-url=<redacted> \
    --packet-delay-ms=200 \
    --public-ip 178.0.0.0
```
# 👋 Contact Me

### 
Telegram: https://t.me/earthzeta
###
<div style={{display:flex; justify-content:space-evenly}}> 
    <a href="https://discordapp.com/users/339619501081362432" target="_blank"><img alt="Discord"
        src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white"/></a>
    <a href="https://t.me/earthzeta" target="_blank"><img alt="Telegram"
        src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/></a>
</div>


#### Feel free to contact me if you need any help.

