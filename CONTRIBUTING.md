# GSRI Standard Contribution Guide

👉 [French version / version française](./CONTRIBUTING_FR.md)

This documentation provides guidelines and standard procedures to contribute to our project. It is a generic documentation which may be overriden on a per-project basis. Please check the `.github\CONTRIBUTING.md` file of projects for additional instructions.

**Note:** the usage of git is beyond the scope of this guide. If you need help in using git, see [our support policy](./SUPPORT.md) on how to get help.

## Ways to contribute to GSRI projects

There are two ways of contributing to our projects :

1. Suggest ideas and feedback
1. Contribute to the source code

**Note:** in order to contribute to the source code you need to own a github.com account.

## How to suggest ideas and feedback

The best way to provide feedback or suggest ideas is by opening an issue on a github repository.
In order to do so, go to the repository and click on the `issues` tab just below the repository name.
Then click on the green `New issue` button, which will open an issue submit form.

Before submitting the issues ensure you have filled in :
* a meaningfull title
* a description with details
* add either a `bug` or `enhancement` label

If you need help in opening an issue, see [our support policy](./SUPPORT.md) on how to get help.

## Occasional contribution to the source code

This procedure is for non-GSRI occasional contributors. As such you are not granted write access to our repository, but you still may provide pull request from forked repositories.

1. Fork the repository
1. Make change in your own repository
1. Ensure your repository is not behind ours
1. Open a pull request to upstream

There are a few rules for pull request to be deemed valid :
* Your repository must not be behind ours
* Your pull request must target our master/main branch, unless explicit request to do otherwise
* You must provide a meaningfull title to the pull request
* You must provide an exhaustive description on changes

GSRI project administrators will the review your code before merging to production. Depending on the project type, tests and other operations may happen to ensure your code does not break anything. If anything goes wrong or we spot somthing that must be modified, you can commit fixes to your current working branch, this will add changes to the pull request automatically.

## Regular contribution to the source code

This procedure is for GSRI members or well known regular contributors. Such people are allowed to contribute directly on the repository to prevent fork proliferation. If you are not allowed to contribute directly to the repository, see instructions in the *occasional contribution to the source code* section above.

1. Clone repository
1. Create a work branch
1. Ensure your branch is not behind master/main
1. Open a pull request to master/main

## Specific information about ArmA 3 mission contributions

If you want to contribute to an ArmA 3 mission, you must also follow these guidelines :

### Clone location

You **MUST** download the repository in your `mpmissions` directory in order to be able to modify the mission using Eden editor. This directory is located in different paths depending on how you setup your game :

* If you never used any command line options nor created any new profile, the directory is `%USERPROFILE%\Documents\Arma 3\mpmissions`

* If you created a custom profile, the directory is `%USERPROFILE%\Documents\Arma 3 - Other Profiles\<profile_name>\mpmissions`

* If you use the `-profiles` switch when playing the game, your directory is `<profiles_path>\Users\<profile_name>\mpmissions`

### Do not use optional mods

Ensure you're *not* using the optionals mods from our modpack, or any other mod than the core pack. Editing the mission with other mods tend to create unwanted dependencies, which means other players will be kicked from the mission if they do not have them when playing.

### No binary/rapified content

**Ensure files are *not* binarized.**

This concerns `mission.sqm` files, but also `config.cpp`. Git is good at versionning text files, not binaries. It also helps with changes history. Do not worry, we will setup a procedure to rapify it before packing the pbo.

Also, do not add your own generated pbo/binary content, we will be build, rapify, binarize and pack automatically from sources.

If your changes include large binary content (images, audio, video), contact staff so we can decide wether it shall be versionned or hosted on our private cloud for integration.