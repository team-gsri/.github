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

*We are in the process of writing this documentation*
