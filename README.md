# create-github-release-simply

This action creates github release.
Not required tag name.

## Inputs

## `token`

**Required** Github Token

##repository

**Required** The owner and repository name. For example, Codertocat/Hello-World.

## name

**Required** release name

## body-path

**Required** path of release body text

## tag-name:

release tag name. Defautl "".

## draft

draft or not. Default false.

## prelesease:

prerelease or not. Default false.

## target-commitish:

Specifies the commitish value that determines where the Git tag is created from. Can be any branch or commit SHA. Unused if the Git tag already exists. Default: the repository's default branch (usually master). Default "".

## discussion-category-name

If specified, a discussion of the specified category is created and linked to the release. The value must be a category that already exists in the repository. Default "".

## generate-release-notes

generate release_notes or not. Default false.


## Example

uses: cgetc/create-github-relrease-simply@v0.1.0
with:
    token: ${{ secrets.GITHUB_TOKEN }}
    repository: ${{ github.repository }}
    name: v0.1.0
    body-path: release_body.txt
    draft: true
