**Update codes:**
```
sudo apt update && sudo apt upgrade -y \

sudo apt install curl git jq build-essential gcc unzip wget lz4 -y
```

**Run code:**
```
wget https://raw.githubusercontent.com/dxzenith/allora-worker-node/main/allora.sh && chmod +x allora.sh && ./allora.sh
```

**Error fix codes:**
```
sudo usermod -aG docker $USER
```
```
sudo reboot
```

**Check status code:**
```
  curl --location 'http://localhost:6000/api/v1/functions/execute' \
--header 'Content-Type: application/json' \
--data '{
    "function_id": "bafybeigpiwl3o73zvvl6dxdqu7zqcub5mhg65jiky2xqb4rdhfmikswzqm",
    "method": "allora-inference-function.wasm",
    "parameters": null,
    "topic": "1",
    "config": {
        "env_vars": [
            {
                "name": "BLS_REQUEST_PATH",
                "value": "/api"
            },
            {
                "name": "ALLORA_ARG_PARAMS",
                "value": "ETH"
            }
        ],
        "number_of_nodes": -1,
        "timeout": 2
    }
}'
```

**Migrate to V2**
```
wget -O testnetmigrator.sh https://raw.githubusercontent.com/casual1st/alloraworkersetup/main/testnetmigrator.sh && chmod +x testnetmigrator.sh && ./testnetmigrator.sh
```
