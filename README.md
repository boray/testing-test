# Mina zkApp: Testing Test

This template uses TypeScript.

## Usage Guide
## UPDATE PATHS
```sh
cd ~/o1js
git switch boray/o1js-testing
GIT_LFS_SKIP_SMUDGE=1 git submodule update --recursive
rm -rf node_modules
npm i
npm run prepublishOnly
npm run pack
cd src/testing
rm -rf node_modules
npm i
npm run prepublishOnly
npm run pack
cd ~/testing-test
npm i
npm run build
node build/src/main.js
```

