# Payment Gateway - Checksums

Automatically updated checksum containing file hashes for each published version of the JS SDK for Payment Gateway v2.

## Description

This repository stores a version.json file, this file is used as a source of truth for the Checksum Lambda.

For each new version of the Eoneo JS SDK that is published, a branch and pull-request will be created against this repo.

- Branches and pull-requests are using the following naming; `RELEASE/{VERSION}` e.g. `RELEASE/1.12.0`

This pull request will contain the updated versions.json file, containing the file hashes for the new version.

***Here is an example of what the version.json file should look like.***

```json
{
  "1.11.0": {
    "eoneo-pay.common.js": "eesei7Jaehoh9chu9Kooroo0chaid1ohpu4zuC0pheth1oa1yeeGi5oothaZiecai",
    "eoneo-pay.common.min.js": "AiNgeenei2poCaap6eeng1pohjailai3yieque9eingoo3pohweingahgh9onai7S",
    "eoneo-pay.iife.js": "eikilaovae1laeSeighaisoomoc0eibeeFeed8Kae1eexah7dumiey6fonuCaehoo"
  },
  "1.12.0": {
    "eoneo-pay.common.js": "ze2xaexaip7ehithoo6faop2bie3Biep2Chah0Ozeiqu8aiPh0roepa8eaT6egh7i",
    "eoneo-pay.common.min.js": "fohngu3wee0oukae8ie9cai4Ekohz1ieGh1mahWooroGhikohwie1OoCh4eehe7ei",
    "eoneo-pay.iife.js": "xohsh2aem8etheNag0sei4jox0ievie3EiceegeiSeiboh9eiH5leifuphoov2Bee"
  }
}

```

- Each version in the JSON file has to be unique.
- Hashes may appear more than once, as we cannot ensure that all the files will change.


it is automatically kept updated by the Github Action running in [Eoneo JS SDK v2](https://github.com/eonx-com/eoneo-js-sdk-v2/)
## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

