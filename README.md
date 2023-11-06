# Ganache-CLI
Note that all these features are now available in `Ganache GUI`
## Programmatic use

### As a web3.js provider:
To use ganache as a Web3 provider:
```
const Web3 = require("web3");
const ganache = require("ganache");

const web3 = new Web3(ganache.provider());
```
NOTE: depending on your web3 version, you may need to set a number of confirmation blocks
```
const web3 = new Web3(ganache.provider(), null, { transactionConfirmationBlocks: 1 });
```

### As an ethers.js provider:
```
const ganache = require("ganache");

const provider = new ethers.providers.Web3Provider(ganache.provider());
```

### Browser Use
You can also use Ganache in the browser by adding the following script to your HTML:

`<script src="https://cdn.jsdelivr.net/npm/ganache@{VERSION}/dist/web/ganache.min.js"></script>`

NOTE: the `{VERSION}` in the above path needs to be replaced with a version number or tag that is listed in npm.

From there, Ganache is available in your browser for use:

```
const options = {};
const provider = Ganache.provider(options);
```

### Command Line Use 
`npm install -g ganache-cli`

Now write `ganache-cli` in terminal.

Now how to customize blockchain :-
- `ganache-cli -h 172.23.0.64` : to start it on '172.23.0.64'
- `ganache-cli -p 7000` : to start it on port:7000
- `ganache-cli -k berlin` : to change hardfork rules for the EVM. Valid options are: constantinople, byzantium, petersburg, istanbul, muirGlacier, berlin, london, arrowGlacier, and grayGlacier. (Default - london)
- `ganache-cli -g 
- `ganache-cli -l
- `ganache-cli -b
- `ganache-cli -t
- `ganache-cli -a
- `ganache-cli -e
- `ganache-cli -d 
- `ganache-cli -m
- `ganache-cli -s
- `ganache-cli --account
- `ganache-cli -n
- `ganache-cli -u 
- `ganache-cli --accountKeysPath
- `ganache-cli --dbPath
- `ganache-cli -v 
- `ganache-cli -q
- `ganache-cli -?

## How to fork the Ethereum Mainnet

[1](https://www.youtube.com/watch?v=9X78nFqJwCM)

[2](https://www.youtube.com/watch?v=oBqS37ffNjE)
