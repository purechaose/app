**this is a hobby project we hack on every now and then when we have the time and motivation to do so.
do not expect any timeframe or release date**

# R6DB Desktop [![Build Status](https://travis-ci.org/r6db/app.svg?branch=master)](https://travis-ci.org/r6db/app)

a rainbow six stat tracker app.

## feature ideas:

-   [ ] per-match tracking (as far as possible)
-   [ ] timeline view of own profile
-   [ ] personal stats (all-time and/or timeframe)

### goals:

-   tracking your own stats often and accurately
-   host _everything_ locally
-   allow for management of local data

### non-goals:

-   leaderboard
-   tracking everyone you ever came across
-   plugins

## How to run

-   install node & yarn
-   install all build tools needed for node-gyp (windows users can use [this](https://www.npmjs.com/package/windows-build-tools))
-   run `yarn global add lerna` to install the [lerna monorepo tool](https://lernajs.io/)
-   run `lerna bootstrap` to install all dependencies and crosslink packages
-   run `lerna run build-deps` to rebuild native deps for electron (needed for sqlite)
-   run `lerna run build` to build all packages. You might want to ignore the desktop app for that though: `lerna run build --ignore @r6db/desktop`

alternatively (for dev mostly), you can start it in watch mode:

### in root directory:

-   `yarn dev` build and watch packages `desktop` and `core`. this uses typescript references to re-build the other packages as needed
-   `yarn run-app` starts the app

### other

Don't forget that you can still use any of the npm scripts in the package folders. Only managing dependencies needs lerna
