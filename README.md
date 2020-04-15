# Longhorn Website

[![Netlify Status](https://api.netlify.com/api/v1/badges/a7c1b4ef-e90e-477c-b9c4-f515d0dd7c7f/deploy-status)](https://app.netlify.com/sites/longhornio/deploys)

This repo houses the assets used to build the website for Longhorn, available at https://longhorn.io.

## Running the site locally

To run the website locally, you need to have the [Hugo](https://gohugo.io) static site generator installed (installation instructions [here](https://gohugo.io/getting-started/installing/)). Once Hugo is installed:

```bash
hugo server --buildDrafts --buildFuture
```

This starts Hugo in local mode. You can see access the site at http://localhost:1313.

## Publishing the site

The Longhorn site is automatically built and published by [Netlify](https://netlify.com) when changes are pushed to the `master` branch.

## New versions of the docs

To create a new version of the documentation:

1. Copy the most recent version of the documentation to create a new version. If the most recent version is 1.2.4 and you'd like to create 1.2.5:

    ```sh
    cp -rf content/docs/1.2.4 content/docs/1.2.5
    ```

1. Add the version to the `params.versions` list in [`config.toml`](./config.toml). Make sure that the list has the latest versions first.
