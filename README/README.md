# README template

> If you need more information about how to fill in this template, read the accompanying [guide](./guide_readme.md).
>
> This template includes writing instructions and boilerplate text that you can customize, use as-is, or completely replace with your own text. This text is indicated in {curly brackets}. Make sure you replace the placeholders with your own text.

## {Project} logo and badges

{This section is optional. Embed an image of the project logo and include links to relevant badges in the README.}

## {Project Name}

{Include the project URL and project owner name underneath the project name if applicable.}

## Table of contents

{This section is optional.}

1. Heading 1

2. Heading 2

3. Heading 3...

## Project description

{The README template guide includes information on how to write a project description and a project description. Here are some examples of effective phrases for describing a project.}

With _{Project Name}_ you can _{verb}_ _{noun}_...

_{Project Name}_ helps you _{verb}_ _{noun}_...

Unlike _{alternative}_, _{Project Name}_ _{verb}_ _{noun}_...

{Include screenshots and/or demo videos if applicable}

## Project structure

_Use PEP's naming conventions when modifying the src packages and modules._

Naming conventions within the project source folder:
- Name of project package: `{PROJECT_NAME}`
- Name of frontend app package: `{PROJECT_NAME}_APP`
- Name of Jinja template packages: `{TEMPLATE_FRAMEWORK_OR_DESCRIPTION}`
  - Folders & subfolders using the Flask extension of SemanticUI retain their names, including packages and modules: `{PROJECT_ROOT}/src/{PROJECT_NAME}/flask_semanticui`; `{PROJECT_ROOT}/src/{PROJECT_NAME}/{PROJECT_NAME_APP}/semantic`

## Who this project is for

This project is intended for {target user} who wants to {user objective}.

## Project dependencies

Before using {Project Name}, ensure you have:

### Required
GitHub will automatically not push any tokens.

However, to commit any changes the .gitignore file must include any files that contain credentials.

If the Markdown Changelog Generator is used, it needs to include  'changelog_generator.toml' because it lists your GitHub repo's PAT (Personal Access Token). 

### Recommended

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


* TOML files
    
  _Note that this file type is recommended for scalable Python projects._
  
  _The pyproject.toml file is the standard configuration file for modern Python projects, defined by PEP 518. It serves as a central place to specify project metadata, dependencies, build requirements, and tool configurations._


* RestructuredText Files
  
    _reStructuredText is a file format for textual data used primarily in the Python programming language community for technical documentation._



## Instructions for using {Project Name}

Get started with {Project Name} by {write the first step a user needs to start using the project. Use a verb to start.}.

### Install {Project Name}

1. {Write the step here.}

   {Explanatory text here}

   {Optional: Include a code sample or screenshot that helps your users complete this step}

2. {Write the step here.}

   a. {Substep 1}

   b. {Substep 2}

### Configure {Project Name}

1. {Write the step here.}
2. {Write the step here.}

### Run {Project Name}

1. {Write the step here.}
2. {Write the step here.}

### Troubleshoot {Project Name}

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

## Contributing guidelines

{Include a link to your contributing guide here. If you do not have a contributing guide, incorporate the information in the README.}

## Project documentation

#### Standard project documentation is stored in the `{PROJECT_ROOT}` folder.

- README
- LICENSE
- CHANGELOG
  - Refer to the Project dependencies section of the README for more information on generating a CHANGELOG file

#### Any other project-specific documentation is stored in the `{PROJECT_ROOT}/docs` folder.

{Include links and brief descriptions to other documentation.}

#### For more information:

* Reference link 1
* Reference link 2
* Reference link 3...

## Links to support resources

{Include links and brief descriptions for support resources. Examples provided in README template guide.}

* Reference link 1
* Reference link 2
* Reference link 3...

## Terms of use

{Project Name} is licensed under {link to license file}.

---

> Explore other templates from [The Good Docs Project](https://thegooddocsproject.dev/). Use our [feedback form](https://thegooddocsproject.dev/feedback/?template=Readme%20template) to give feedback on this template.
