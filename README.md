# Payment Gateway - Checksums

Registry of file hashes taken for each published version of the JS SDK.


## Description

This repository is a registry for file hashes, generated for each version of the JS SDK. a version.json file, this file is used as a source of truth for the Checksum Lambda.

For each new version of [Eoneo JS SDK v2](https://github.com/eonx-com/eoneo-js-sdk-v2/) that is published, a branch and pull-request will be created against this repo.

- Branches and pull-requests are using the following naming; `RELEASE/{VERSION}` e.g. `RELEASE/1.12.0`

This pull request will contain the updated versions.json file, containing the file hashes for the new version.

## version.json
The version.json file will list the sem version, and hashes for each file found in the `/dist` folder in [Eoneo JS SDK v2](https://github.com/eonx-com/eoneo-js-sdk-v2/)

***Here is an example of what the version.json file should look like.***

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

- Each version in the JSON file has to be unique.
- Hashes may appear more than once, as we cannot ensure that all the files will change. In the example above you can see the hash is the same for the first file `eoneo-pay.common.js` across both versions.

## Pull Request workflow

Pull requests made against this repo are only created automatically, they will need a senior staff member to merge the pull request into the master branch.

Once the pull request is merged into the master branch, the version.json file will become available for the Payment Gateway Checksum Lambda to verify against.  

**Note:** ***False positives may occur for about 10 minutes after merging as the the GitHub supplied [RAW](https://raw.githubusercontent.com/eonx-com/payment-gateway-frontend-checksums/master/versions.json) URL is cached.***

## Built With

* [eonx-com/actions-pull-request](https://github.com/eonx-com/actions-pull-request) - Github Action to create pull requests 

## Authors

* **Jy Kingston** - *Initial work* - [EonX](https://eonx.com/)
