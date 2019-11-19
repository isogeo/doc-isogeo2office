# Isogeo To Office documentation

[![Build Status](https://dev.azure.com/isogeo/Documentations/_apis/build/status/isogeo.doc-isogeo2office?branchName=master)](https://dev.azure.com/isogeo/Documentations/_build/latest?definitionId=25&branchName=master)

Content, structure and media of the website documentation. It's part of the Isogeo online documentations ([see Github repositories](https://github.com/search?q=topic%3Adocumentation+org%3Aisogeo&type=Repositories)).

## Edit this documentation

It's based on Gitbook v3.2.* which is:

- [a book format](https://github.com/GitbookIO/gitbook)
- [a toolchain](https://toolchain.gitbook.com/)

## Deployment

It's deployed on Isogeo Azure (Storage v2 Static website) using CircleCI ([see config](https://github.com/isogeo/doc-isogeo2office/blob/master/.circleci/config.yml)):

- each commit triggers a deploy on QA :

  - <http://help.qa.isogeo.com/isogeo2office>
  - <https://qaisogeohelp.z28.web.core.windows.net/isogeo2office>

- each tagged commit triggers a deploy on PROD:

  - <http://help.isogeo.com/isogeo2office>
  - <https://prodisogeohelp.z28.web.core.windows.net/isogeo2office>

## Build

Git clone this repository then:

```powershell
yarn
yarn dev
yarn gitbook install
yarn gitbook serve
```
