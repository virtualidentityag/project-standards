# NPM
NPM is our standard package manager. We switched from yarn, back to NPM. So some projects might still have yarn in them.

## Package.json
The package.json should always be kept up to date. Especially concerning:
- License
- Name
- Repository
- Metadata

Because of our legacy CI/CD process, we have to use absolute versions in our package.json. So do not use `~` or `^` in package versions.

## start script
All projects should be able to be run in dev mode via the `npm start`command.
This will run all the services that are needed for development.  
>☝️ IF you cannot follow this rule, write it in the readme.

## build script
All projects should be able to be built via the `npm build`command.
This will run all the services that are needed for production build.  
>☝️ IF you cannot follow this rule, write it in the readme.

## Package serving
⚠️ NO package should be permanently served directly from github
NPM packages should be served from npm or the vi artifactory.

>☝️ It is temporally allowed to serve a package from the github virtualidentity organization, if you are waiting for a PR to be merged

All temporally github includes have to be resolved as soon as merged.
