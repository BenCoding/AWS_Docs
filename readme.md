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

## MKDocs Reference

### Custom Domains

https://www.mkdocs.org/user-guide/deploying-your-docs/

GitHub Pages includes support for using a Custom Domain for your site. In addition to the steps documented by GitHub, you need to take one additional step so that MkDocs will work with your custom domain. You need to add a CNAME file to the root of your docs_dir. The file must contain a single bare domain or subdomain on a single line (see MkDocs' own CNAME file as an example). You may create the file manually, or use GitHub's web interface to set up the custom domain (under Settings / Custom Domain). If you use the web interface, GitHub will create the CNAME file for you and save it to the root of your "pages" branch. So that the file does not get removed the next time you deploy, you need to copy the file to your docs_dir. With the file properly included in your docs_dir, MkDocs will include the file in your built site and push it to your "pages" branch each time you run the gh-deploy command.

If you are having problems getting a custom domain to work, see GitHub's documentation on Troubleshooting custom domains.