# monorepo-changesets-template
Monorepo template using changesets as a versioning tool.

## How to make new release
1. Create branch `releases` base on `main`
2. Maintainer run `changeset add` and `changeset version` on branch `releases`
3. Create PR/MR from `releases` to `main`
4. After PR/MR is approved, merge to `main`
5. Maintainer checkout `main`, run `changeset tag` to create release tags
6. Maintainer run `git push --tags` to push new release tags
7. Create new releases on relevant locations based on new tags (github/gitlab/npm/pypi/etc.)

## Pros and cons
### Pros
- Changesets is the only mature versioning tool that natively support monorepo
- Changesets support updating changelogs by default
- Changesets does not couple commit messages and versioning
- Changesets does not enforce conventional commits

### Cons
- More things to do compared to semantic-release tool which create releases based on conventional commit format
- Changesets is not as stable and extensible as semantic-release
- Changesets is designed specifically for using with github and npm, commands like `changeset publish` works with npm but not others

