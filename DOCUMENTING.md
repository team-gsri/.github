# GSRI Documentation Guide

👉 [French version / version française](./DOCUMENTING_FR.md)

This documentation provides guidelines on how to document projects with GSRI standards.

👷 ***We are in the process of writing this documentation***

## How to and why document

The first entrypoint to project documentation is the `README` file. This file is displayed on the homepage of any project. It gives information to users as to how the software is useful to them, links to other documentation, and explains how to interact with the project in general. This file has a standard structure for consistency. Although you could store this file in the repository root, it is better to move this file with them in the `.github` directory with other mandatory documentation.

Other useful files are `USAGE` and `LICENSE`, they are **mandatory** in every project. The `USAGE` file explains how to use the software. It should take all profiles of users into account. If too large, the file can be split across multiple subfiles. The `USAGE` file must sit in the `.github` directory. The `LICENSE` file specifies which right you grant to other people. Without a license file, other people get no right over the software and need to ask you for permission for anything. The `LICENSE` file stays in the root directory.

Additional documentation can be added to projects if that is of use.

## Readme file content

Readme files are structured in 3 parts :
* Description
* Rules and standards
* Disclaimer

### Description
This section contains a small paragraph describing what the project is about.

### Rules and standards
This section contains links to documents in 3 subsections :
* Links to project specific documents ; license and usage are mandatory
* Links to standard GSRI documents
* Links to BI EULA

You can copypaste the rules and standards paragraph from the [organization profile](https://github.com/team-gsri/.github/edit/master/profile/README.md).

### Disclaimer
> This application or website is not affiliated or authorized by Bohemia Interactive a.s. Bohemia Interactive, ARMA, DAYZ and all associated logos and designs are trademarks or registered trademarks of Bohemia Interactive a.s.
> 
> The GSRI logo is a trademark of GSRI.
