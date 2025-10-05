# SAS Packages Archive policy and rules of contribution

[**Document version: 2025-10-05**]

[**SAS Packages Archive**](https://github.com/SASPAC) (SASPAC) is location dedicated to store and provide publicly available **SAS packages** generated with the [SAS Packages Framework](https://github.com/yabwon/SAS_PACKAGES).

This document provides a list of rules and practices (*R&P*) designed to maintain quality standards for shared packages. Those *R&P* describe requirements for repositories, packages, and developers.

Some legal and formal considerations are also presented.

The SASPAC team is a group of volunteers, their time is SASPAC the most precious resource, please keep that in mind when contacting the team.

---

## Rules and Practices

The following rules and practices apply to repositories, packages, and developers. They are not sorted in any particular order, consider them all equally important.

- Repository is designed to store the "final" package, i.e. the `packagename.zip` file. This is not the development zone! Of course, the source code can be presented too but *it is not required nor recommended*. Developers have to have their own repos for the development stage. 

- Repository has to have a `README.md` file with at least package name and link to the documentation.

- Repository should contain documentation. The `packagename.md` file is preferred, but not necessary. The file can be replaced by a clearly presented link to the documentation located someplace else (e.g., a dedicated webpage).

- Package should provide *full* backward compatibility, i.e., the new version should not break/alter behavior of older versions. If the developer needs to introduce altered behavior, consider the following alternatives:
  - if changes are "small" then create new name for the modified version of the object, e.g., you are modifying behavior of macro `%abc()`, then create macro `%abc2()` with introduced changes and keep `%abc()` as it was,
  - if changes are "big" create a new package.

- Package content should be prepared with the best quality and properly tested (e.g., think globally, write *high* quality documentation, run tests, check parameters, provide accurate log messages, etc.) Before publication a code review is strongly suggested. Before introduction to SASPAC a package can be subjected to a code review process by the SASPAC team. If minimal code standards are not satisfied, the package will not be published (unless the criteria are met).

- Package should introduce additional and non-trivial value to the community.

- To introduce a package to SASPAC, the developer is required to provide tests documentation. In particular a log file from the loading test (the default test executed by the SPF during package generation) is a "must".

- A package is *assumed* to work on SAS under Windows, Linux, and UNIX environment, *if it is not the case* a clear information about the fact has to be provided in package documentation! Preferably in the `description` file.

- Data of the first maintainer on the maintainer's list provided in the metadata **has** to have *name and active contact email*! The email provided will be used for every communication with developers, so it's essential for the email to be correct and active one. Lack of contact may be a reason to orphan a package.

- Packages should be of the *minimum necessary size*. As a general rule, neither data nor documentation, nor additional content should exceed 5MB. Overall, a SAS package `zip` file should not exceed 10MB in size. If you have extensive data or big documentation consider a separate location for them.

- The package code and examples provided in a package should *never* do anything that might be regarded as malicious or "dangerous for the user". If a package is reported to "misbehave" it will be removed without warning!

- Packages should be named in a way that does not conflict with any current or past SAS package presented in SASPAC or [PharmaForest](https://github.com/PharmaForest) current packages. Ask the SASPAC team if you are not sure.

## Legal and formal considerations.

- For clarity, the `developer` is the first `maintainer` on the maintainer's list provided in the metadata.

- SAS Packages Archive *only* hosts packages files! SASPAC *does not* take any responsibility for packages content. It is the developer who takes full responsibility for the content of a package. **Publishing a package on SASPAC is equivalent to accepting the fact and this responsibility.** Especially, the additional content (if provided) is the developer responsibility!

- By publishing a package on SASPAC, the developer acknowledges that the right for SASPAC to distribute the package is granted in perpetuity. 

- Copyright and intellectual property rights of the package components must be clear and unambiguous. The ownership has to be clearly presented. The developer is *responsible* for providing all required information in proper form and format, so that all rights are preserved correctly.

- The developer is responsible for providing the proper license file for the package. *Remember!* If `license.sas` file is not provided during the package generation process the default one is the MIT license.

- If a license type presented in the package metadata is not aligned with the text provided in the license file, the license file takes precedence.

- Maintainers of a package hosted in SASPAC are assigned with the "maintain" role in GitHub's "Collaborators and teams" section. The "administrator" role will *not be granted* under any circumstances.

- Package maintainers give the right to use that package name to SASPAC when they publish it. The SASPAC team may orphan a package and allow another maintainer to take it over. Orphaning of a package can be done on direct request from the current developer or when there is no contact with members of the developers team over a longer period of time (that's why providing active email is so important).

- Names of SAS packages hosted on SASPAC are persistent and in general it is not permitted to change a package’s name.

- When a new maintainer wishes to take over a package, this should be accompanied by the written agreement of the previous maintainer (unless the package has been formally orphaned).

- The SASPAC team reserves the right to remove packages from SAS Packages Archive without notice or explanation (usually we notify and explain).

---

### Acknowledgment 

The SASPAC team would like to acknowledge the [CRAN](https://cran.r-project.org/ "CRAN") project team. Their work was an inspiration and this document is highly influenced by the following document: "[CRAN Repository Policy](https://cran.r-project.org/web/packages/policies.html)"


---
