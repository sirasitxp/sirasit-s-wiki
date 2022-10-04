# What's the difference
## NVM
NVM is short for Node Version Manager, and its purpose is to allow you to check which version of Node.JS you have installed and even to let you install a fresh most up to date version of Node. It also allows you to install multiple instances of Node so you can test your app in multiple iterations of the program to see if it works with older versions.
## NPM
NPM is Node Package Manager, and it is the meat and potatoes package installer for Node.JS. It is a CLI (Command Line Interface) based installer for Node and works with simple commands like: node install and node init -y which allows you to create the package.json to store and list the dependencies of your Node.JS app. The website for NPM acts as the documentation for all your NPM needs and as well as a home for all of the many, many packages that you can install and utilize in your Javascript/Node applications.
## Yarn
Yarn is the latest and greatest version of NPM. It takes the same methods that NPM uses but stores all of the install information into the app so it’ll work across multiple machines. Yarn also tends to be more stable than NPM. The nice thing about Yarn is that all if not most packages on the NPM site are usable with Yarn. Another advantage to using Yarn is besides caching all installed packages, it installs simultaneously whereas NPM installs everything in order listed in the dependencies. To summon and install Yarn packages use yarn install or yarn i if they both do the same thing, it just depends on how lazy you are in typing.
## You can't use yarn and npm at the same time for same project(same folder)
Don't dare!

# Update packages to latest version
```bash
npm install [package_name]@latest --save-dev
-------
pnpm add [package_name]@latest --save-dev
-------
yarn add [package_name]@latest --dev
```
