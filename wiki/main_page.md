---
redirect_from: /
published: true
---

# Welcome to my wiki page!

通过我的wiki，记录我完整的知识体系！

## kubernetes

## Docker

## Linux

[List of git-wiki installations](examples.md)

[List of forked repository](https://github.com/Drassil/git-wiki-theme/network/members)


### [Share your wiki with us!](examples) and keep the "Powered by Git-Wiki" footer link please. It will help both of us!


## Installation instructions

### Remote theme method

1. Fork, Clone [the skeleton repository](https://github.com/Drassil/git-wiki-skeleton) or click on "Use this template" button to create your copy.

2. Edit _config.yml and other pages as you need and then deploy it on github/gitlab pages.

**Description**: This method will allow you to create a wiki based on our skeleton repository and that extends git-wiki-theme. 

**Direct installation comparison**:

 + **pros**: This will allow you to avoid upgrading process pulling files from git-wiki-theme and eventually merge them.

 - **cons**: To edit/fix git-wiki-theme core files you need to configure a second repository forked by git-wiki-theme repo. However, [YAGNI](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)

**GITLAB SUPPORT**: if you want to fork the skeleton from gitlab, you can use [this repo](https://gitlab.com/drassil/git-wiki-skeleton)

**Without skeleton**: you can avoid to use the skeleton repository if you want start from scratch, however it's important to use at leaset the configuration variables needed by the theme: [_config.yml](https://github.com/Drassil/git-wiki-skeleton/blob/master/_config.yml)

### Direct installation method

1. Fork, Clone [git-wiki-theme repository](https://github.com/drassil/git-wiki-theme) or click on "Use this template"

2. Edit _config.yml and push your changes in your repository, then configure the github/gitlab pages in your repository settings

**Description**: This method will allow you to create a wiki using git-wiki-theme directly. You can create your theme from scratch. It's for advanced users and people who want directly collaborate to git-wiki-theme project.

**Remote installation comparison**:

 + **pros**: You can build your wiki and collaborate with git-wiki-theme project by PR at the same time.

 - **cons**: Upgrading your wiki to the latest version need a merge with git-wiki-theme repo.


### Notes:
In both cases please is preferred to use **Fork** instead of **Template** and **Template** instead of **Clone** (Fork > Template > Clone).
Fork will allow you to make pull request to/from original repository to keep your files updated (for skeleton too). Please, keep everything open and collaborative!


### Local development

If you need to work on git-wiki locally before publish, then clone your wiki repo and follow this instructions 
from official github article: <https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/>
Git wiki already contains the Gemfile for local installations.

You can also use our **docker files** to run git-wiki under **docker**, 
the easiest method is to run `docker-compose up` command in this folder

## Configuration and customization

Read documentation about [Customization HERE](customize.md)


## Current known limitations

* You can't use the wiki internal link format: [[example]]. Please, use gh-pages links instead: \[example\](example) . It's a known jekyll limitation: <https://jekyllrb.com/docs/templates/>


## Support & Collaboration

You can open a public issue on [github](https://github.com/Drassil/git-wiki/issues) , 
send a private <a href="mailto:staff-drassil@googlegroups.com">email</a>  or create a PR to improve it.

Thank you!

## Components used

- [jekyll-toc](https://github.com/allejo/jekyll-toc)

- [jQuery](https://jquery.com/) for DOM manipulation

[MIT LICENSE](LICENSE)
