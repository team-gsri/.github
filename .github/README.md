# GSRI Documentation Project

## What is this project

This project serves as a document versioning management for general purpose documents that apply to multiple GSRI github repositories.

## Rules and standards

The following documents provide additional information on rules and standards applying to this project :

   * [MIT License](../LICENSE)
   * [GSRI Code of Conduct](../content/CODE_OF_CONDUCT.md)
   * [Contributing to this repository](./CONTRIBUTING.md)

## Content

The [`content/` directory](../content/) contains applicable versions of the following documents:
   * [GSRI Code of Conduct](../content/CODE_OF_CONDUCT.md)
      * [French version](../content/CODE_OF_CONDUCT_FR.md)
   * [GSRI Standard Contribution Guide](../content/CONTRIBUTING.md)
      * [French version](../content/CONTRIBUTING.md)

## How to use

The [`template/` directory](../template/) contains files that link to the applicable documents. You shall copy the template files to repositories that will use the standard documents. It will link to the currently applicable versions of the documents.

Some documents, such as the GSRI Code of Conduct is applicable to all repositories, but other can be opted out. For instance, this project contains a generic contribution guide, but some projects may use different contribution standards. In that case, do not copy the template file and provide your own version of the document in the repository. You can also adopt an hybryd approach by modifying the template document, linking to the standard document and including additional elements.

New versions of the standard documents are applicable as soon as they are pushed on `master` branch. Changes will be handled as through git branches, pull requests, history, etc ...

## How to get help

You can ask for support on [our discord server](https://discord.gg/bhMn4jd)
