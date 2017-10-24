# Kolibri UI

**User interface component library**

---

[![Build Status](https://travis-ci.org/dossiersolutions/kolibri-ui.svg?branch=master)](https://travis-ci.org/dossiersolutions/kolibri-ui)

<!--
**[Component Documentation](https://dossiersolutions.github.io/kolibri-ui/)**
-->

Kolibri UI contains presentational React components that we use to make Dossier ProFile. It also contains a documentation app, a test suite, and a hot-reloading server for developers.

The development environment is provided through [create-react-app](https://github.com/facebookincubator/create-react-app). This means we don't have to maintain a build configuration, which saves a lot of work for us, will still providing an awesome development environment.

The actual library distribution is built by Babel, and does not even know about create-react-app.


## Usage

Add as dependency: `yarn add kolibri-ui` or `npm install kolibri-ui`

Import component: `import {SmallSpinner} from "kolibri-ui/components/SmallSpinner";`

Import less for component: `@import "~kolibri-ui/styles/components/SmallSpinner";`

Import less for all components: `@import "~kolibri-ui/styles/main";`

#### Variables supported by less:

TODO


## Developing

### Getting started

- Clone this repo using git
- Install [yarn](https://yarnpkg.com) if you don't have it
- Run `yarn install` inside the kolibri-ui folder

### Commands

- `yarn run` shows a list of the available commands
- `yarn run start` runs the hot reloading server
- `yarn run watch-css` live-rebuilds the less-files
- `yarn run test` runs the test suite
- `yarn run build-app` builds the documentation app
- `yarn run build-lib` builds the component library
- `yarn deploy` deploys the documentation app to Github Pages

Whatever you do, DO NOT RUN `yarn run eject` . The whole point of using create-react-app is to not deal with configuration. At least ask me (jbe) first!

### Testing

Testing is provided by create-react-app, and uses [Jest](https://facebook.github.io/jest/). See this link for documentation on how to write tests, expectations, mocks and so on.

### Documentation

Because this project uses create-react-app to provide its features, [almost everything is documented there](https://github.com/facebookincubator/create-react-app). They also have instructions for how to migrate to newer versions
.

### Important information

Keep in mind that the test and development environments provided here are different from the enviroment that imports and uses the components in the end. The library distribution is transpiled by Babel alone, without even knowing about create-react-app. This means that if you depend on any polyfills or build environment features provided by create-react-app, you will have to include these manually in your own build. Currently, the library transpiler only transpiles a subset of the create-react-app syntax. We are only using create-react-app to provide testing and development features.

### Editor and IDE integration

Create-react app already provides lint configuration (and optionally flow), which will integrate with many editors.

#### IntelliJ

If you want to add this repository as a project subfolder within a larger project, [IntelliJ supports multiple VCS roots natively](https://intellij-support.jetbrains.com/hc/en-us/community/posts/207052265-Multiple-git-repositories). Just check out the project in a subfolder, then go to *Settings*, and then *Version Control*, and add the folder to the list. If you do this, you will still have to make sure that commits get meaningful messages, end up in the correct branch, and push them to Github. It is might be easier to use git directly.

### How to submit changes and have them reviewed

If you are new to git, [this is a very quick intro](http://rogerdudler.github.io/git-guide/).

We use pull requests to review changes before pulling them into the master branch. Therefore, all work should happen within *feature branches* that can be reviewed on git. Github has a [quick overview of this process](https://guides.github.com/introduction/flow/). Atlassian also has a [nice guide that goes more in-depth with actual command line examples](https://www.atlassian.com/git/tutorials/comparing-workflows#feature-branch-workflow).

Packages must not be published to npm/yarn before they have been reviewed.

#### Some useful Git commands

- `git branch ..` create a branch, list branches, delete branches
- `git checkout --track ..` create a branch tracking an existing remote branch
- `git checkout ..` switch to a branch
- `git add ..` add files to the staging area
- `git commit ..` commit the staging area to HEAD (the current branch)
- `git pull` pull remote changes into the current branch
- `git merge master` merge changes from the master branch into the current branch
- `git rebase master ..` re-base the current branch on top of new changes from the master branch. [Explained here](https://www.atlassian.com/git/tutorials/merging-vs-rebasing#the-golden-rule-of-rebasing).
- `git push` push the current branch to the remote tracking branch (Github).
