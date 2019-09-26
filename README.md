# chainlink-stake-capital
All materials related to Chainlink

# Install a Chainlink validator 
## Install Docker
```
curl -sSL https://get.docker.com/ | sh
sudo usermod -aG docker $USER
exit
# log in again
```

## Create Chainlink folder
`mkdir ~/.chainlink`

## Create an Environment File
```
echo "ROOT=/chainlink
LOG_LEVEL=debug
ETH_CHAIN_ID=1
CHAINLINK_TLS_PORT=0
SECURE_COOKIES=false
ALLOW_ORIGINS=*" > ~/.chainlink/.env
```

## Set your Ethereum Client URL
echo "ETH_URL=LINK_to_ETHEREUM_CLIENT" >> ~/.chainlink-ropsten/.env

