# ENS.BID Truffle Box

This box comes with everything you need to start using smart contracts on Ethereum blockchain and interact with MetaMask to send transactions.  

## Technical stack

#### Frontend
- React
- Redux
- Saga
- Web3(MetaMask)

#### UI
- Sass
- Material-UI

#### Smart contract/Solidity
- Truffle

## Prerequisites
In order to run the Truffle box, you will need [Node.js](https://nodejs.org) (tested with version 8.x.x). This will include npm, needed to install dependencies. You will also need the [MetaMask](https://metamask.io/) plugin for Chrome.

## Installation and Building

1. Install truffle and an ethereum client. For local development, try Ethereum TestRPC.
    ```javascript
    npm install -g truffle
    npm install -g ethereumjs-testrpc
    ```

2. Install yarn.

    ```javascript
    ## MacOS
    brew install yarn

    ## Windows
    https://yarnpkg.com/en/docs/install#windows-tab
    ```

3. Download box.
    ```javascript
    truffle unbox ens-bid/ens-bid-truffle-box
    ```

4. Install the node dependencies.
    ```javascript
    yarn install
    ```

5. Run Ethereum RPC.
    ```javascript
    testrpc
    ```

6. Compile and migrate the contracts.
    ```javascript
    truffle compile
    truffle migrate
    ```

7. Run the webpack server for front-end hot reloading. For now, smart contract changes must be manually recompiled and migrated.
    ```javascript
    yarn start
    ```

8. Jest is included for testing React components and Truffle's own suite is included for smart contracts. Be sure you've compile your contracts before running jest, or you'll receive some file not found errors.
    ```javascript
    // Runs Jest for component tests.
    yarn test

    // Runs Truffle's test suite for smart contract tests.
    truffle test
    ```

9. To build the application for production, use the build command. A production build will be in the build_webpack folder.
    ```javascript
    yarn build
## FAQ

* __Why is there both a truffle.js file and a truffle-config.js file?__

    Truffle requires the truffle.js file be named truffle-config on Windows machines. Feel free to delete the file that doesn't correspond to your platform.

* __Where is my production build?__

    The production build will be in the build_webpack folder. This is because Truffle outputs contract compilations to the build folder.

* __Where can I find more documentation?__

    All truffle boxes are a marriage of [Truffle](http://truffleframework.com/) and a React setup created with [create-react-app](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md). Either one would be a great place to start!
    