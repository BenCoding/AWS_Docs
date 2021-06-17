# AWS Docs

This project is a compilation of my learnings as a Cloud Solution Architect & Analyst
This guide is intended to help anyone in their journey to the cloud on AWS. 

---
 
# Setting up Domain

## Checking DNS Configuration for site

[Domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

`dig aws.bencassani.com +nostats +nocomments +nocmd`

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.