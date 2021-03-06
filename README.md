# singularity-score-client
[![Hosted](https://img.shields.io/badge/hosted-sylabs.io-green.svg)](https://cloud.sylabs.io/library/icaoberg/default/score-client)
![Release](https://img.shields.io/badge/release-v2.29.2-green.svg)
[![Build Status](https://travis-ci.org/icaoberg/singularity-score-client.svg?branch=master)](https://travis-ci.org/icaoberg/singularity-score-client)
[![GitHub issues](https://img.shields.io/github/issues/icaoberg/singularity-score-client.svg)](https://github.com/icaoberg/singularity-score-client/issues)
[![GitHub forks](https://img.shields.io/github/forks/icaoberg/singularity-score-client.svg)](https://github.com/icaoberg/singularity-score-client/network)
[![GitHub stars](https://img.shields.io/github/stars/icaoberg/singularity-score-client.svg)](https://github.com/icaoberg/singularity-score-client/stargazers)
[![GitHub license](https://img.shields.io/badge/license-GPLv3-blue.svg)](https://www.gnu.org/licenses/quick-guide-gplv3.en.html)

For more information about the `score-client` please visit the [ICGC DCC Docs page](https://docs.icgc.org/download/guide/).

## Pre-requisites

* [Singularity v3.5.+](https://sylabs.io/docs/).

## Building the image using the recipe

### To build the image locally
Run the script `build.sh` to build image locally.

```
bash ./build.sh
```

### To build the image remotely remotely
Run the script `rbuild.sh` to build image remotely.

```
bash ./rbuild.sh
```

You will need to edit the script above to match your account on [SyLabs.io](https://sylabs.io/).

### Pulling from the repository
If you have the client installed and cannot build the image locally nor remotely, simply run

```
singularity pull library://icaoberg/default/score-client:3.0.1
```

The command above will download the image from the SyLabs.io image repository.

## Example
If you read the documentation you will find the following basic example

```
bin/score-client url --object-id ddcdd044-adda-5f09-8849-27d6038f8ccd
```

When using the container the command above turns into

```
singularity run --app score /path/to/score-client_3.0.1.sif url --object-id ddcdd044-adda-5f09-8849-27d6038f8ccd
```

Use the comand above as a emplate when working with your scripts.

## Disclaimer

I am nothing but a humble programmer creating the container for this wonderful app.

---
[![CBD](http://www.cbd.cmu.edu/wp-content/uploads/2017/07/wordpress-default.png)](http://www.cbd.cmu.edu)

Copyleft © 2019-2020 [icaoberg](http://www.andrew.cmu.edu/~icaoberg) at the [Computational Biology Department](http://www.cbd.cmu.edu) in [Carnegie Mellon University](http://www.cmu.edu)
