# react-navigation-v5-expo44

React Navigation 5
THIS REPO IS ARCHIVED AND CODE HAS BEEN MOVED TO THE MAIN REPOSIORY

Build Status Code Coverage MIT License

Routing and navigation for your React Native apps with a component-first API.

Documentation can be found at next.reactnavigation.org.

Contributing
The project uses a monorepo structure for the packages managed by yarn workspaces and lerna. To get started with the project, run yarn in the root directory to install the required dependencies for each package:

yarn
While developing, you can run the example app with Expo to test your changes:

yarn example start
Make sure your code passes TypeScript and ESLint. Run the following to verify:

yarn typescript
yarn lint
To fix formatting errors, run the following:

yarn lint --fix
Remember to add tests for your change if possible. Run the unit tests by:

yarn test
Running the e2e tests with Detox (on iOS) requires the following:

Mac with macOS (at least macOS High Sierra 10.13.6)
Xcode 10.1+ with Xcode command line tools
First you need to install applesimutils and detox-cli:

brew tap wix/brew
brew install applesimutils
yarn global add detox-cli
Then you can build and run the tests:

detox build -c ios.sim.debug
detox test -c ios.sim.debug
Publishing
To publish a new version, first we need to export a GH_TOKEN environment variable as mentioned here. Then run:

yarn lerna publish
This will automatically bump the version and publish the packages. It'll also publish the changelogs on GitHub for each package.

Installing from a fork on GitHub
Since we use a monorepo, it's not possible to install a package from the repository URL. If you need to install a forked version from Git, you can use gitpkg.

First install gitpkg:

yarn global add gitpkg
Then follow these steps to publish and install a forked package:

Fork this repo to your account and clone the forked repo to your local machine
Open a Terminal and cd to the location of the cloned repo
Run yarn to install any dependencies
If you want to make any changes, make them and commit
Now cd to the package directory that you want to use (e.g. cd packages/stack for @react-navigation/stack)
Run gitpkg publish to publish the package to your repo
After publishing, you should see something like this:

Package uploaded to git@github.com:<user>/<repo>.git with the name <name>
You can now install the dependency in your project:

yarn add <user>/<repo>.git#<name>
Remember to replace <user>, <repo> and <name> with right values.
