# Ganache-CLI
Note that all these features are now available in `Ganache GUI`
## Programmatic use

### As a web3.js provider:
To use ganache as a Web3 provider:
```
const {Web3} = require('web3');
const ganache = require('ganache');
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
`npm install -g ganache` (For global installation)

Now write `ganache-cli` or `ganache` in terminal.

Now how to customize blockchain :-
- `ganache-cli -h 172.23.0.64` : to start it on '172.23.0.64'
- `ganache-cli -p 7000` : to start it on port:7000
- `ganache-cli -k berlin` : to change hardfork rules for the EVM. Valid options are: constantinople, byzantium, petersburg, istanbul, muirGlacier, berlin, london, arrowGlacier, and grayGlacier. (Default - london)
- `ganache-cli -g` : Sets the default gas price in WEI for transactions
- `ganache-cli -i 700` : The id of the network set to 700. For example - goerli (5) || sepolia (11155111) || ethereum (1) 
- `ganache-cli -l` : Sets the block gas limit in WEI.
- `ganache-cli -b` : Sets the time taken for mining in seconds for automatic mining. Default is 0. A blockTime of 0 enables "instamine mode", where new transactions mined instantly.
- `ganache-cli -t` : Date that the first block should start.
- `ganache-cli -a` : Number of accounts generated
- `ganache-cli -e` : The default account balance, specified in ether.
- `ganache-cli -d` : Use pre-defined, deterministic seed. Default case is everytime you run ganache-cli random addresses are generated
- `ganache-cli -m` : Use a specific mnemonic to generate initial addresses.
- `ganache-cli -s` : Uses seed string to use to generate a mnemonic and hence for addresses. [default: Random value, unless wallet.deterministic is specified]
- `ganache-cli --wallet.accounts="0xd0fcf...4b483,100000000000000000000"` : Account data in the form "<private_key>,<initial_balance>", can be specified multiple times. Note that private keys are 64 characters long and must be entered as an 0x-prefixed hex string. Balance can either be input as an integer, or as a 0x-prefixed hex string with either form specifying the initial balance in wei.
- `ganache-cli -n` : Locks available accounts.
- `ganache-cli -u` : Array of addresses or address indexes specifying which accounts should be unlocked. Examples are : `ganache-cli -n -u 0 1 2` (0th, 1st & 2nd indexed address unlocked) **OR** `ganache-cli -n -u 0x6Ee9...9477` (this address unlocked only)
- `ganache-cli --accountKeysPath` : Specifies a file to save accounts and private keys to, for later reuse.
- `ganache-cli --database.dbPath` : Specify a path to a directory to save the chain database. Examples are : `ganache-cli --database.dbPath .` **OR** `ganache-cli --database.dbPath .\newFolder\`
- `ganache-cli -v` : Set to true to log detailed RPC requests.
- `ganache-cli -q` : Set to true to disable logging.
- `ganache-cli -?` : Shows help (alias : `ganache-cli --help`)

## How to fork the Ethereum Mainnet

[**Reference #1**](https://www.youtube.com/watch?v=9X78nFqJwCM) || [**Reference #2**](https://www.youtube.com/watch?v=oBqS37ffNjE)