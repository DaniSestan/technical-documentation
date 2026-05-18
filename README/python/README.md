# README template

> If you need more information about how to fill in this template, read the accompanying [guide](./guide_readme.md).
>
> This template includes writing instructions and boilerplate text that you can customize, use as-is, or completely replace with your own text. This text is indicated in {curly brackets}. Make sure you replace the placeholders with your own text.

## {Project} logo and badges

{This section is optional. Embed an image of the project logo and include links to relevant badges in the README.}

## {Project Name}

{Include the project URL and project owner name underneath the project name if applicable.}

## Table of contents

1. Project description
2. Project setup
3. Contributing guidelines
4. Project documentation
5. Links to support resources
6. Terms of use

## Project description

### What kind of software is this?

[...]

__________________

### Who can use this app?

[...]

__________________

### How is the project is organized?

#### Naming conventions

###### What is the official 'source of truth' for 'standardization'?

###### E.g., PEP defines the naming convention guidelines for Python.

[...]

#### Project structure

[...]

#### File types

###### Not all files types are necessary according to the 'latest' recommendations.
###### Understand the context of the software app as an end-product.
###### What's the difference between project recommendations versus requirements?

[...]

## Project setup

### Pre-requisites

Before using {Project name}, install necessary pkgs:

* [<LINK>](<URL>): <LINK_DESC>

### Requirements

GitHub will automatically not push any tokens.

However, to commit any changes the .gitignore file must include any files that contain credentials.

If the Markdown Changelog Generator is used, it needs to include  'changelog_generator.toml' because it lists your GitHub repo's PAT (Personal Access Token). 

#### Install {Project Name}

1. {Write the step here.}

   {Explanatory text here}

   {Optional: Include a code sample or screenshot that helps your users complete this step}

2. {Write the step here.}

   a. {Substep 1}

   b. {Substep 2}

#### Configure {Project Name}

1. {Write the step here.}
2. {Write the step here.}

#### Run {Project Name}

1. {Write the step here.}
2. {Write the step here.}

#### Troubleshoot {Project Name}

1. {Write the step here.}
2. {Write the step here.}

<table>
  <tr>
   <td>
    Issue
   </td>
   <td>
    Solution
   </td>
  </tr>
  <tr>
   <td>
    {Describe the issue here}
   </td>
   <td>
    {Write solution here}
   </td>
  </tr>
  <tr>
   <td>
    {Describe the issue here}
   </td>
   <td>
    {Write solution here}
   </td>
  </tr>
  <tr>
   <td>
    {Describe the issue here}
   </td>
   <td>
    {Write solution here}
   </td>
  </tr>
</table>

Other troubleshooting supports:

* {Link to FAQs}
* {Link to runbooks}
* {Link to other relevant support information}

### Recommendations

* [Markdown Changelog Generator](https://changelog.seapagan.net)

  `github-changelog-md`

  _For additional options and advanced usage, refer to the documentation._

  _Note: Dont commit the config file to your project repository!_

  The config file contains your GitHub PAT. GitHub always prevents committing credentials, so to push any commit, it's necessary to include the changelog_generator.toml file in the .gitignore.

  The CHANGELOG generator creates CHANGELOG entries based on the repository PRs. For instance, the PR label, is used to define CHANGELOG entry section. Note that options are available to customize the output of the tool, as per the documentation.

  | Title               | Label           | Notes                       |
  |----------------------|-----------------|------------------------------|
  | Breaking Changes     | breaking        |                              |
  | Merged Pull Requests |                 | Any PR with NO labels        |
  | Enhancements         | enhancement     |                              |
  | Bug Fixes            | bug             |                              |
  | Refactoring          | refactor        |                              |
  | Documentation        | documentation   |                              |
  | Dependency Updates   | dependencies    |                              |

  To make merge requests from the command line:

  Step 1: Clone the repository or update your local repository with the latest changes.

  git pull origin main

  Step 2: Switch to the base branch of the pull request.

  git checkout main

  Step 3: Merge the head branch into the base branch.

  git merge dev

  Step 4: Push the changes.

  git push -u origin main

### Version Control Process
I. **Create a Feature Branch**
Any code updates for a version change -- [Major].[Minor].[Patch] -- should be on a separate branch, referred to as a 'feature' branch.

Once work on the branch is completed, a pull-request can be created to merge the branch into `dev`, a staging/pre-release branch, where those changes are tested.

Once the staging branch is tested, stable code can be merged into `main` a production/release branch.

________________
##### Maintaining repos

Maintaining the permissions, the branching strategy, and a consistent timeline between each repo lessens the probability of a bottleneck when releasing any new changes.

Permissions

| Repository | Visibility |
|-------------|-------------|
| Staging     | Private     |
| Production  | Public      |

Timeline

| Version | Change    |
|---------|---------|
| Major   | 1 month |
| Minor   | 2 weeks |
| Patch   | 1 week  |


_Once changes are pushed to `main` in the staging repo, allow some time for those changes to 'soak' in the 'dev' in each repository._

| Feature | Timeline |
|---------|-----------|
| Major   | 1 month   |
| Minor   | 2 weeks   |
| Patch   | 1 week    |

__________________

###### Branch Naming Conventions

`<VERSION-RELEASE-#>/<FEATURE_NAME>/<CONTRIBUTOR>`

- `<VERSION-RELEASE-#>`: Refer to [SemVer](https://semver.org/) for details

- `<FEATURE_NAME>`: Descriptive title for the feature

- `<CONTRIBUTOR>`: GitHub account name, e.g., https://github.com/<NAME>

______________

###### Tagging Conventions

Please use standard tagging conventions to define each branch with its version release number, feature name, and the contributor.

`git tag -a <TAG_VAL> -m "<TAG_TYPE>"`

- `git tag -a v<VERSION_#> -m 'version #'`
- `git tag -a <FEATURE_NAME> -m 'feature name'`
- `git tag -a <CONTRIBUTOR> -m 'contributor'`

To check tagging info:
`git tag -n9`

II. **Pull-request**

Instead of merging on local, please remember to create a pull-request.

`bash ./<REPO-NAME>/version-control/pull-request.sh`

To do this manually:
`git request-pull [-p] <VERSION-RELEASE-#> https://github.com/DaniSestan/<REPO_NAME> dev `

III. **Merge-request**

Once a pull-request is reviewed, accepted and merged, the merge request data can then be used to document those changes through the Markdown Changelog Generator.

`bash ./<REPO-NAME>/version-control/merge-request.sh`

To do this manually:
`git push -o mr.<END> origin <START>`

IV. **Documenting changes**

Maintaining a CHANGELOG file is always recommended for a quick overview of how the project is progressing.
1. Checkout main locally.
2. From a terminal session, run the commands to use the GitHub ChangeLog Generator.
3. Commit the CHANGELOG file to the remote branch.

`changelog-generator-md`

## Contributing guidelines

{Include a link to your contributing guide here. If you do not have a contributing guide, incorporate the information in the README.}

## Project documentation

### Standard project docs are located in the `{PROJECT_ROOT}` folder.

- README
- LICENSE
- CHANGELOG
    - Refer to the Project dependencies section of the README for more information on generating a CHANGELOG file

### Please upload any other supporting documentation in the `{PROJECT_ROOT}/docs` folder.

* Reference link 1: Description
* Reference link 2: Description
* Reference link 3: Description...

## Links

### Support resources

* Reference link 1: Description
* Reference link 2
* Reference link 3...

### Additional links

* [The Good Docs Project](https://thegooddocsproject.dev/): A site dedicated to software documentation templates

## Terms of use

{Project Name} is licensed under [MIT](https://commons.wikimedia.org/wiki/Template:X11)
