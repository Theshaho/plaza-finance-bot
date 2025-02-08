
# Auto Daily Plaza Finance Bot

Register : https://testnet.plaza.finance/rewards/mR7nGgrFA4Jh

This script automates interactions with Plaza Finance's faucet, ensuring unlimited spending for the wstETH token, creating Bond and Leverage tokens, and redeeming a portion of those tokens. It processes multiple wallets in a cycle, with a delay of 6 hours after all wallets are processed.

## Features
- Claims faucet tokens.
- Sets unlimited allowance for wstETH token.
- Creates Bond and Leverage tokens.
- Redeems 50% of Bond and Leverage tokens' balance.
- Repeats the entire cycle every 6 hours.

## Requirements
- Node.js
- `web3`, `axios`, `chalk`, `fs`

Install the required Node.js modules:

```bash
npm install web3@1.8.0 axios chalk@2 fs https-proxy-agent
```

## Setup

```bash
git clone https://github.com/Theshaho/plaza-finance-bot
```
```bash
cd plaza-finance-bot
```

Add your private keys to the `private_keys.txt` file, with one private key per line. Ensure each key is exactly 64 characters (without 0x).

```bash
nano private_keys.txt
```
put your private keys and then Ctl + X and then Y and then Enter.

### Proxy Format
if you want to use proxy,create a file named `proxies.txt` and each line in the `proxies.txt` file should contain a proxy in the following format:

```
<IP_ADDRESS>:<PORT>
```

For example:

```
192.168.1.100:8080
123.456.789.101:3128
```   

so use these commands to save your proxies:

```bash
nano proxies.txt
```

put your proxies and then Ctl + X and then Y and then Enter.

## Usage

Run the script with Node.js:

create a screen
```bash
screen -S plaza
```


if you prefer using proxies, run:

```bash
node index-proxy.js
```

otherwise run:

```bash
node index.js
```

The script will run once immediately and will repeat every 6 hours.

Ctl + A + D


[source: forked from main Repo](https://github.com/ganjsmoke/plaza-finance-bot)
