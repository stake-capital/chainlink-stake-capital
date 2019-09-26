# chainlink-stake-capital
All materials related to Chainlink

Chainlink documentation: https://docs.chain.link/docs/running-a-chainlink-node

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

## Run Cargo 

`cd ~/.chainlink && docker run -p 6688:6688 -v ~/.chainlink:/chainlink -it --env-file=.env smartcontract/chainlink local n -p /chainlink/.password -a /chainlink/.api`

Run in deamon mode: 

`cd ~/.chainlink && docker run -p 6688:6688 -d -v ~/.chainlink:/chainlink -it --env-file=.env smartcontract/chainlink local n -p /chainlink/.password -a /chainlink/.api`
