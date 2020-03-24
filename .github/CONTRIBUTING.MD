# Contributing to GSRI repositories

This documentation provides guidelines and standard procedures to contribute to our project. It is a generic documentation which may be overriden on a per-project basis. Please check the `.guithub\CONTRIBUTING.md` file of projects for additional instructions.

## Ways to contribute to GSRI projects

There are two ways of contributing to our projects :

1. Suggest ideas and feedback
1. Contribute to the source code

**Note:** in order to contribute to the source code you need to own a github.com account.

## How to suggest ideas and feedback

*We are in the process of writing this documentation*

## Occasional contribution to the source code

**Note:** *this procedure is for non-GSRI occasional contributors. As such you are not granted write access to our repository, but you still may provide pull request from forked repositories.*

### Fork the repository

The first step in order to contribute is to fork our repository. This basically means you will create your own copy of our repository. In order to do so, just click on the `Fork` button in the top right of your screen.

That's all.

### Clone the repository

You need to use a git client in order to download and synchronize your work with the repository. If you don't know how to use git, we suggest you use [Github Desktop](https://desktop.github.com/).

Once git client installed, go to your forked project repository on github.com, and click the green `Clone or download` button on the right side of the webpage, then click `Open in Desktop` in the tooltip. Github Desktop will open and ask you where to download the source code. Select a directory of choice, and once selected, click `Clone` ; Github Desktop will download the sources on your computer.

### Modify the sources

You can now work on the source code with your favorite editor. If you don't have one, we suggest you use [Microsoft Visual Studio Code](https://code.visualstudio.com/), which integrates well with Github Dekstop. If you are modifying a mission, please follow guidelines below on *How to contribute to Arma 3 missions*.

Git has three different features regarding changes tracking :

* `git stage` means you want to consider the current version of a given file *ready to commit*. It is a convenient way to add or remove changes from your current commit.

* `git commit` means your *staged* modifications are stored **locally**. Every commit is associated to your identity and you can add a small description of what you changed, and why. If you did not stage anything, git will stage all changes and commit them.

* `git push` will send your *committed* modifications to github. All modification stay local until you git push. Other users can then access you modifications from their repository. You can also obtain code *pushed* by other people by `fetch`ing from github.

### Keeping repositories synced

You should frequently ensure you're not working on an outdated version of the code base. Please ensure your branch has no *behind* commits relative to our master branch. If your branch is not up-to-date with upstream/master, opening a pull request will be denied by our staff.

If you need to update, you should sync changes from our repository to yours. this operation is called *integration*. When integrating, conficts may happen, for instance if you modified an entity but it was deleted from upstream by another developper.

Conflict resolutions should preferably be done on your currently working branch, as it makes it easier to test wether the integration process did not break anything. Once you're satisfied with the merge, check your version of the code still works OK before opening the pull request. This technique is called *ping-pong merging*.

### Open a pull request to upstream

Once you're satisfied with your work, and you want it to go to the official version, you can open a pull request to merge your changes *upstream*. 

Open the pull request by selecting `Branch` / `Create pull request` in Github Dekstop. This will open your browser with a form to fill in. Ensure the source branch is the one you have been working on, and the destination is the master branch of our repository. Once completed, click `Open pull request`.

 **Note: All PR to other branches will be denied by our staff.**

GSRI project administrators will the review your code before merging to production. Depending on the project type, tests and other operations may happen to ensure your code does not break anything. If anything goes wrong or we spot somthing that must be modified, you can commit fixes to your current working branch, this will add changes to the pull request automatically.

## Regular contribution to the source code

**Note:** This procedure is for GSRI members or well known regular contributors. Such people are allowed to contribute directly on the repository to prevent fork proliferation. If you are not allowed to contribute directly to the repository, see instructions in the *occasional contribution to the source code* section below.

### Obtain write access to the repository

Your first step in order to contribute directly is to obtain write access to the repository. Ask on Discord and we will consider adding you write access.

### Clone the repository

If you are a regular contributor, you may contribute directly on our repository. you do not need to fork the repository and you can clone the gsri directory directly.

### Create a new branch

**Note: This step is mandatory.** Failing to do so will make your modifications on the master branch. You will be allowed to commit locally, but you will be denied pushing to github.

In order to create a new branch, select `Branch` / `New branch ...` in the menu. Github Desktop will ask a branch name. Enter anything you want, such as your nickname or the feature you're planning to implement. If in doubt, ask us. Ensure the source branch is `master`. Once created, publish the branch to github by clicking on the button in the top bar of Github Desktop.

Other operations are similar to above procedure

### Keeping your branch up-to-date with master

You should frequently ensure you're not working on an outdated version of the code base. Please ensure your branch has no *behind* commits relative to our master branch. If your branches are not up-to-date with upstream/master, opening a pull request will be denied by our staff. If changes happened on the master branch, you may use `Branch` / `Update from master` from Github Desktop menu to upgrade. Conflict resolution must be done on your currently working branch as well.

### Open a pull request to master

The procedure is also the same as above. Your repository must be up-to-date with master, or your pull request will be denied. The operation is easier because Github will help you more. Like with forked repository, commits may run tests and operations to ensure your code is correct before allowing merges. Merges are done by GSRI staff. You can commit again to your current working branch to add changes to the PR automatically.

## Specific information about Arma 3 mission contributions

If you want to contribute to an arma 3 mission, you must also follow these guidelines :

### Clone location

You **MUST** download the repository in your `mpmissions` directory in order to be able to modify the mission using Eden editor. This directory is located in different paths depending on how you setup your game :

* If you never used any command line options nor created any new profile, the directory is `%USERPROFILE%\Documents\Arma 3\mpmissions`

* If you created a custom profile, the directory is `%USERPROFILE%\Documents\Arma 3 - Other Profiles\<profile_name>\mpmissions`

* If you use the `-profiles` switch when playing the game, your directory is `<profiles_path>\Users\<profile_name>\mpmissions`

### Do not use optional mods

Ensure you're *not* using the optionals mods from our modpack, or any other mod than core pack. Editing the mission with other mods tend to create dependencies, which means other players will be kicked from the mission if they do not have them when playing.

### No binary/rapified content

**Ensure files are *not* binarized.**

This concerns `mission.sqm` files, but also `config.cpp`. Git is good at versionning text files, not binaries. It also helps with changes history. Do not worry, we will setup a procedure to rapify it before packing the pbo.

Also, do not add your own generated pbo/binary content, we will be build, rapify, binarize and pack automatically from sources.

If your changes include large binary content (images, audio, video), contact staff so we can decide wether it shall be versionned or hosted on our private cloud for integration.

## A few words of advice

* Always `Fetch from github` and `Update from master` **before** you work
* Always work on your own branches and then pull request to master
* Commit small changes and add meaningfull descriptions
* Commit changes frequently, this is a near equivalent of a `Ctrl + S`
* Push at least daily, even if your code is broken (better broken than lost)
* Borderless mode makes it easier to switch between game and desktop
