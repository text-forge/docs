# Text Forge Online Documentation
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/text-forge/docs/mkdocs.yml?label=build%20%26%20deploy)

This repository is build and deploy place for main project docs. It means all docs (everything in `docs/` directory) copied from [here](https://github.com/text-forge/text-forge/tree/Main/docs)
(by GitHub Actions), and then built and deployed. This repository was created solely for the purpose of using the link `text-forge.github.io/docs` instead of `text-forge.github.io/text-forge`, and 
also includes configuration files. With this in mind, please use the `docs/` folder in the main project repository ([here](https://github.com/text-forge/text-forge/tree/Main/docs)) to make changes 
to the documentation.

> [!Important]
> `mkdocs.yml` and `docs/` directory will be sync by [`github-actions[bot]`](https://github.com/apps/github-actions), don't change them directly.
