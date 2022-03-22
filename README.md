# CES Goerli MCD

MCD system deployed on Goerli as a staging environment for the Collateral Engineering Services core unit.

## Installation

Clone this repo:
  ```bash
  git clone --recurse-submodules git@github.com:clio-finance/ces-goerli-mcd.git
  # or using HTTPS:
  git clone --recurse-submodules https://github.com/clio-finance/ces-goerli-mcd
  ```

If you forget the `--recurse-submodules` option above, you can always run:

```bash
git submodule update --init --recursive
```

## Usage

All contracts and their respective names can be found in the [contracts.json](./contracts.json) file.

Notice that those contracts might be out of sync with the on-chain changelog. To make sure everything is up-to-date,
there is a utility script `lib/shell-utils/bin/changelog-to-json` that will fetch the latest values on-chain and output it as JSON:

```bash
lib/shell-utils/bin/changelog-to-json $(jq -r '.CHANGELOG' contracts.json) > contracts.json
```
