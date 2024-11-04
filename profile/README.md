# SKNUPS GitHub Actions

## [sknups/github-action-template](https://github.com/sknups/github-action-template)

This is a template we use at SKNUPS for creating public GitHub Actions.

## [sknups/authenticate-google-artifact-registry-action](https://github.com/sknups/authenticate-google-artifact-registry-action)

This is a GitHub Action which authenticates Google Artifact Registry.

This allows you download packages from your organisation's private npm repository in Google Cloud.

## [sknups/sknups-build-javascript-action](https://github.com/sknups/sknups-build-javascript-action)

This is a GitHub Action we use to build JavaScript projects at SKNUPS.

- invokes `sknups/authenticate-google-artifact-registry-action` if needed
- executes `npm ci`
- executes `npm run lint`
- executes `npm run compile`
- executes `npm test`

## [sknups/npm-publish-action](https://github.com/sknups/npm-publish-action)

This is a GitHub Action for publishing npm packages.

It overwrites the version property in `package.json`, then runs `npm publish`.

If you push to `main` you get a version like `0.0.1-snapshot.1709644075`, including the epoch time (in seconds) of the Git commit.

If you push a tag you get a version derived from the tag, e.g. `1.2.3`.


## [sknups/sknups-npm-publish-action](https://github.com/sknups/sknups-npm-publish-action)

This is a GitHub Action we use to publish npm packages at SKNUPS.

- determines which npm repository the package should be published to
- invokes `sknups/authenticate-google-artifact-registry-action`
- invokes `sknups/npm-publish-action`

---

# SKNUPS Template Projects

## [sknups/eslint-config](https://github.com/sknups/eslint-config)

This is the eslint configuration used for JavaScript development at SKNUPS.

The configuration is strongly influenced by StandardJS, but more relaxed.

## [sknups/configure-javascript-template](https://github.com/sknups/configure-javascript-template)

This publishes the npm package `@sknups/configure-javascript-template` into our organisation's repository.

When a new GitHub repository is created from the `sknups/javascript-template` template, the user can then do this:

```
npx @sknups/configure-javascript-template
```

---

# SKNUPS JSON Schema

The [sknups/schema](https://github.com/sknups/schema) project holds all our JSON schema files.

It makes them available on the public internet using GitHub Pages.

---

# SKNUPS Digital Collectibles Platform

Certain repositories related to the wholesale (i.e. backend) part of SKNUPS Digital Collectibles platform are made public:

- [sknups/item-cloudfunctions](https://github.com/sknups/item-cloudfunctions)
- [sknups/stock-cloudfunctions](https://github.com/sknups/stock-cloudfunctions)
- [sknups/giveaway-cloudfunctions](https://github.com/sknups/giveaway-cloudfunctions)
- [sknups/flex](https://github.com/sknups/flex)
