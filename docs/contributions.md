---
title: Contributions
---

# Contribute documentation

To contribute, use the Github [repo](https://github.com/economic/research_docs) and submit changes with pull requests.

## Install MkDocs

We build the documentation from markdown files using [MkDocs](https://www.mkdocs.org/) and some related python modules. If you haven't already installed MkDocs, use `pip` to install

* `mkdocs`
* `mkdocs-material`
* `pymdown-extensions`
* `mkdocs-awesome-pages-plugin`

For example, on our server maynard open a terminal and type 

```bash
pip3 install mkdocs mkdocs-material pymdown-extensions mkdocs-awesome-pages-plugin --user
```

## Build the docs locally
Clone the repo and use `mkdocs serve` on the raw files to build and view the website locally:

```bash
git clone git@github.com:Economic/research_docs.git
cd research_docs
mkdocs serve
```

Then open up `http://127.0.0.1:8000/` in your browser to view your local version of the website.


## File structure
The repo has the following general structure:
```bash
docs/
  - index.md
  - otherfile.md
  subdirectory1/
    - file.md
mkdocs.yml
```

All of the site's pages are built from markdown files in `docs/` directory. This is where you will edit or add content.

`mkdocs.yml` is the MkDocs configuration file that specifies the theme and other site-wide options. If you are just editing or adding pages, you likely don't need to worry about this file.

## Editing content
1. Create a separate branch.
2. Edit or add .md files in the `docs/` directory.
3. Confirm the site looks the way you want locally.
4. Commit changes and push them to github.
5. Submit a pull request.
