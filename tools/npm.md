---
layout: default
title: NPM
parent: Tools
nav_order: 1
has_child: false
has_toc: false

---

# NPM
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-de#lta }
1. TOC
{:toc}
</details>

# What is NPM?
`npm` is the world's largest software registry. Open source developers from every continent use npm to share and borrow packages, and many organizations use npm to manage private development as well.

See more details on [About NPM](https://docs.npmjs.com/about-npm)

# Installation
Install the `npm` with NodeJS by downloading it on [the download page](https://nodejs.org/en/download/). It is strongly recommended to install Nodejs and npm with version manager like [`nvm`](https://github.com/nvm-sh/nvm)

# Check version
Once the `npm` is installed, check the version by running:
```bash
npm -v (or --version)
```

# Check for hints of usage
```
npm help
```

# Starting the package
Run `npm init` to start the use and it will create folder `node_module` and file called `package.json`. It will ask question in steps about the details.
If you wish to use all defauylt options, add `-y` or `--yes`

```
npm init -y (or --yes)
```
The default `package.json` will look lik this:
```json

  "name": "package-name",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": "",
  }
}
```

# Then you can change the config details
Example
```bash
npm config set init-author-name "Irawan"
npm set init-license "MIT"
```

Then it will look like this:

```json
  "name": "package-name",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "Irawan",
  "license": "MIT",
  "description": "",
  "dependencies": {
    "gulp": "^4.0.2",
    "lodash": "^4.17.3"
  }
}
```

# check and remove default configuration
To check the configuration details, run the following:
```bash
npm config get init-author-name
npm get init-license
```

to remove details;
```bash
npm config delete init-author-name
npm delete init-license
```

# Install package
## Locally
E.g installing gulp-sass
```bash
npm install gulp gulp-sass --save-dev
```
Always use `--save-dev` to ensure that the changes is saved in the package.json file.

## Install globally (in the machine and not only in current folder)
```bash
npm install -g nodemon
npm install -g live-server

```

# Remove or uninstall module
```bash
npm uninstall gulp-sass --save-dev
# or
npm remove gulp --save-dev
#or
npm rm gulp-sass --save-dev
```

# Install module with version and upate
```bash
npm install gulp-sas@5.5.5 --save

# to update
# UPDATE
npm update lodash --sav
```

# To check the root folder of global install
```
npm root -g
```

# Remove global package
```bash
npm remove -g gulp-sass
```

# To show the installed packages

```bash
#Main modules only:
npm list

#result:

╰─ npm list                        
user@1.0.0 /Users/project-name
├── gulp-cli@2.3.0
├── gulp-sass@5.1.0
├── gulp@4.0.2
└── lodash@4.17.21

# Main modules with the direct dependencies:
npm list --depth 0

#Main modules with the dependencies next level 
npm list --depth 1

# etc...
```

