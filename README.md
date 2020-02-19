# Payment Gateway - Checksums

Registry of file hashes taken for each published version of the [Eoneo JS SDK v2](https://github.com/eonx-com/eoneo-js-sdk-v2/).

**Note:** ***Payment Gateway is the new name for Eoneo***

## Description

This repository is a registry of file hashes that are generated for each version of [Eoneo JS SDK v2](https://github.com/eonx-com/eoneo-js-sdk-v2/) 

For each version of [Eoneo JS SDK v2](https://github.com/eonx-com/eoneo-js-sdk-v2/) that is published, a branch and pull-request will be created against this repo.

- Branches and pull-requests are using the following naming; `RELEASE/{VERSION}` e.g. `RELEASE/1.12.0`

This pull request will contain the updated versions.json file, containing the file hashes for the new version.

### Checksum file - version.json
The version.json file will list the semantic version, and hashes for each file found in the `/dist` folder in [Eoneo JS SDK v2](https://github.com/eonx-com/eoneo-js-sdk-v2/)

***Here is an example of what the version.json file***

```json
{
  "1.11.0": {
    "eoneo-pay.common.js": "eesei7Jaehoh9chu9Kooroo0chaid1ohpu4zuC0pheth1oa1yeeGi5oothaZiecai",
    "eoneo-pay.common.min.js": "AiNgeenei2poCaap6eeng1pohjailai3yieque9eingoo3pohweingahgh9onai7S",
    "eoneo-pay.iife.js": "eikilaovae1laeSeighaisoomoc0eibeeFeed8Kae1eexah7dumiey6fonuCaehoo"
  },
  "1.12.0": {
    "eoneo-pay.common.js": "eesei7Jaehoh9chu9Kooroo0chaid1ohpu4zuC0pheth1oa1yeeGi5oothaZiecai",
    "eoneo-pay.common.min.js": "fohngu3wee0oukae8ie9cai4Ekohz1ieGh1mahWooroGhikohwie1OoCh4eehe7ei",
    "eoneo-pay.iife.js": "xohsh2aem8etheNag0sei4jox0ievie3EiceegeiSeiboh9eiH5leifuphoov2Bee"
  }
}

```

- Each version in the versions.json file has to be unique.
- Hashes are not unique and may appear more than once, as the files may not change. As an example, above you can see the hash is the same for the first file `eoneo-pay.common.js` across both versions.

***We are using `sha256` hashes, these are based on the file content, any updates to the JS files should cause a new hash to be generated***

If for whatever reason the hash appears to be incorrect, you can verify it from the command line by running the following in your checked out copy of the [Eoneo JS SDK v2](https://github.com/eonx-com/eoneo-js-sdk-v2/) repo;
```shell script
$ cd eoneo-js-sdk-v2
$ sha256sum dist/*
 
Piogh3Hiqu6ieCoh7aif6TeingahxieB5oaH2jae7eudeiz1eiSh8eoquuasah2ze  dist/eoneo-pay.common.js
etahch6xaifu1aulemeethoo6fae9iereejeiquaitooho6Ahlooth6Fob0ootahj  dist/eoneo-pay.common.min.js
Rievaeh7eigiodoo6seec0if5Vootai9ooWaiY5ohgiesh7eiraiH4eipoo0hohFi  dist/eoneo-pay.iife.js

```
### Pull Requests

Pull requests are automatically made when a branch matching the `RELEASE/*` pattern is pushed to, each pull request will need a senior staff member to review and merge into the master branch.

The branch will be generated, have the updated version.json file committed, and pushed by the Github Action running on the [Eoneo JS SDK v2](https://github.com/eonx-com/eoneo-js-sdk-v2/) repo.
 
Once the pull request is merged into the master branch, the version.json file will become available for the [Payment Gateway - Serverless Checksum Lambda](https://github.com/eonx-com/payment-gateway-checksums-serverless) to verify against.  

**Note:** ***False positives may occur for about 10 minutes after merging as the the GitHub supplied [RAW](https://raw.githubusercontent.com/eonx-com/payment-gateway-frontend-checksums/master/versions.json) URL is cached.***

## Built With

* [eonx-com/actions-pull-request](https://github.com/eonx-com/actions-pull-request) - Github Action to create pull requests 

## Authors

* **Jy Kingston** - *Initial work* - [EonX](https://eonx.com/)
