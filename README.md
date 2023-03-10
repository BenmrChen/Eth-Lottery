# ETH Lottery ð²
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/49083753/161920881-b00a8854-e9b8-48fc-8cc3-64d6e3c72f4a.png">

Using blockchain to provide highly transparent digital services & competitive lottery platform solutions


====

## ðª Quick Start

Prerequisites: [Node (v16)](https://nodejs.org/en/download/) plus [npm](https://www.npmjs.com/) and [Git](https://git-scm.com/downloads)

> clone/fork:

```bash
git clone https://github.com/Krypto-Camp/batch2-final-project-team-4
```

> setup:

```bash
npm install
copy .env.example file and rename it to .env
npm i hardhat -g
npm run clean # reset the env
npm run chain # run localhost chain by hardhat, keep this process, don't close it
npm run deploy:localhost # compile and deploy contracts to localhost chain
npm run dev
```
> env:
```bash
INFURA_PROJECT_ID = 'add_the_infura_project_id_here'
ACCOUNT_PRIVATE_KEY = 'add_ur_own_metamask_develop_account_private_key_here'
VITE_INFURA_ID = 'add_the_infura_project_id_here'
```


> deploy/test:

```bash
npm run clean
npm run deploy:rinkeby
npm run dev
```
## ð Reference
[Hardhat](https://hardhat.org/getting-started/)
\
[React Ethers Hook - Wagmi](https://wagmi-xyz.vercel.app/)
\
[Vite](https://cn.vitejs.dev/guide/#scaffolding-your-first-vite-project)
\
[RentRent](https://rentrent.xyz/)

## Others
#### Connect Frontend to Contracts
`src/components/GetContract.tsx`
\
`src/main.tsx`

#### Create Contract
```
1. æ¼ contract/ æ°å¢åç´
2. æ¼ scripts/deploy.js æ°å¢é¨å±¬æ¹æ³ `deployContract()`
3. npm run deploy:localhost or npm run deploy:rinkeby
4. config/contracts.ts å¼å¥åç´ address ä»¥å abi json file
5. ä»¿é  getContract.tsx ä¸²æ¥
```

#### Folder Strcuture
```bash
- address/ # generate contract address file by deploy.jsï¼å®¢è£½å¯«æ³ï¼é¿ååç«¯è¦å¨é¨å±¬åç´å¾ä¸ç´æ´æ°åç´å°å
- artifacts/ # compiled contract here, use npm run clean to delete it.
- cache/ # hardhat deploy contract log, use npm run clean to remove the content in it and re-deploy ur contract.
- contracts/ # write ur smart contract here!
  - testing/ # example contract here
- external/ # å¤é¨åç´ abi
- scripts/ # scripts
  - deploy.js # script ur compiled contracts
  - mint.js # mintApe demo js
- test/ # testing contract by using ethers
- hardhat.config.js # config 
- .env # INFURA_PROJECT_ID, ACCOUNT_PRIVATE_KEY
# åç«¯
- src/
  - components/
    - GetContract.tsx # å¦ä½æä½åç´åè
  - configs/contract.ts # éè£¡å¼å¥åç´
  - App.tsx
  - main.tsx # éè£¡å¼å¥ provider
```

#### scripts
```bash
npm run chain # run localhost chain by hardhat, keep this process, don't close it
npm run compile # compiled contract in contracts/
npm run clean # reset env
npm run console:local # run hardhat console on localhost
npm run console:rinkeby # run hardhat console on rinkeby (if need testnet, pls add a .env file)
npm run deploy:hardhat # deploy contracts on localhost chain
npm run deploy:rinkeby # deploy contracts on rinkeby
npm run deploy # deploy contracts on mainnet
```

## ð¤ Collaboration Guide

* Create new branches for new features: naming convention `<member name>-<branch feature>`, e.g., `XXX-contract`
* Before `PR` to main branch: `pull from main` -> `local testing` -> `pull request`

## ð Sketch
![image](https://user-images.githubusercontent.com/88078588/161436894-7b21ab27-ee5a-405e-b848-93a93b49051f.png)



