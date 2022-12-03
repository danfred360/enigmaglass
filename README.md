## Project Status
| Branch | Live Site | Test Status | CICD Status |
| - | - | - | - |
| `main` | [Production Site](https://enigmaglass-docs.github.io/enigmaglass/) | [![Run Tests - CodeQL](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/codeql.yml/badge.svg?branch=main)](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/codeql.yml) | [![pages-build-deployment](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/pages/pages-build-deployment/badge.svg?branch=main)](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/pages/pages-build-deployment) |
| `development` | [Development Site](https://enigmaglass-docs.github.io/enigmaglass-dev/) | [![Run Tests - CodeQL](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/codeql.yml/badge.svg?branch=development)](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/codeql.yml) | [![Development Build and Deploy](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/deploy-dev.yml/badge.svg?branch=development)](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/deploy-dev.yml) [![pages-build-deployment](https://github.com/enigmaglass-docs/enigmaglass-dev/actions/workflows/pages/pages-build-deployment/badge.svg?branch=main)](https://github.com/enigmaglass-docs/enigmaglass-dev/actions/workflows/pages/pages-build-deployment)|

## Project Overview
Welcome to the Enigma Glass training resource. This site has been designed to provide a framework that Enigma Glass or other students can continue to build on.

The major factor that informed our design decisions was ease of development and integration. This project has been setup in a way that attempts to make it as easy as possible to contribute to. The site content development work is done mostly in markdown, but the site can be customized with HTML, CSS, and JS. Due to the include / override nature of Ruby on Rails and Gems, the site will run well and look good without anything other than markdown. 

This project deploys to three distinct environments and features automated build and deploy workflows, in addition to automated testing and dependency scanning.

The site is intended to be served by Jekyll; it was built using a gem theme called `just-the-docs`. When the site is built Jekyll parses all of the markdown files in the directory looking for templating tags and markdown. It then outputs the `_site` directory which contains the static HTML / CSS / JS for the site.

When the site is built a search index is created to be used by Lunr.js to support the site's full-text search functionality. The search runs as clientside javascript, but as this is a small static site the search is still lightning fast.

## Development Flow
1. Create feature branch off of develop

```bash
git checkout -b feature/my-cool-feature develop
```

2. Make you changes and test them locally.

```bash
# run site locally (you must have Ruby and Jekyll installed)

`bundle install`

`bundle exec jekyll serve --livereload`
```

3. Create a pull request to merge your branch with `develop`.

This pr will trigger [the Pheonix deploy](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/deploy-pr.yml) which creates a shortlived repository that is ownded by the enigmaglass-docs organization before deploying a build of your branch to that repo. Your version of the site will then be served at it's own external ip address.

This stage is usefull for getting an idea of what your changes will look like if you can't run the site locally, or if you want to verify that the site behaves as it should when deployed on github pages. These workflow runs are aggregated in [the pr-staging environment](https://github.com/enigmaglass-docs/enigmaglass/deployments/activity_log?environment=pr-staging).

The Pheonix deploy is entireley optional.

[![Pheonix Build and Deploy](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/deploy-pr.yml/badge.svg)](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/deploy-pr.yml)

4. Once you've tested what you want to in the Pheonix stage and your pull request has at least 1 approval you can complete the pr into `develop`.

A push to `develop` will trigger [the Development Build and Deploy workflow](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/deploy-dev.yml) which will build the site and deploy it to [the enigmaglass-dev repository](https://github.com/enigmaglass-docs/enigmaglass-dev). The dev site can be accessed [here](https://enigmaglass-docs.github.io/enigmaglass-dev/).

5. To complete the contribution and update the production site, create a pull request merging `develop` into `master`. In order to merge into `master` you will need 1 pr approval, [the development environment](https://github.com/enigmaglass-docs/enigmaglass/deployments/activity_log?environment=development) must be successfuly deployed to.

Your push into `master` will trigger [the Github pages build and deploy workflow](https://github.com/enigmaglass-docs/enigmaglass/actions/workflows/pages/pages-build-deployment) that deploys to [the github pages environment](https://github.com/enigmaglass-docs/enigmaglass/deployments/activity_log?environment=github-pages).