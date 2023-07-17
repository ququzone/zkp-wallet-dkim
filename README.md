ZKP Wallet DKIM service
=======================

## Startup

```
docker build -t iotex-zkp-dkim .
docker run -d -v "$(realpath .)/key:/key" -name zkp-dkim \
  -e IMAP_SERVER=imap.larksuite.com:993 \
  -e IMAP_USERNAME= \
  -e IMAP_PASSWORD= \
  -e KEY_FILE=key \
  -e KEY_PASSPHRASE= \
  -e RPC=https://babel-api.testnet.iotex.io \
  iotex-zkp-dkim
```
