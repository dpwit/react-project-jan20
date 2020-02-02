[Home](index.html)

# How to set up Webpack

## What is Webpack?

Webpack is an open-source JavaScript module bundler. Its main purpose is to bundle JavaScript files for use in the browser to reduce requests and improve page load speeds. Therefore there is no more individual script tags which increases requests and page load speeds. Webpack, Out of the box is pure Javascript. Alternative JavaScript module bundlers include [rollup.js](https://rollupjs.org/guide/en/) and [Parcel.js](https://parceljs.org/).

### Setup

### Install Node and NPM (Node Package Manager)

Webpack will be installed using NPM (Node Package Manager). Installing Node.js on your machine will also install NPM.

* [Download Node.js](https://nodejs.org/en/)

The terminal can be used to confirm the versions of Node and NPM once installed:

```

		$ node --version
		$ npm --version

```

### Create a new directory

Begin by opening your terminal and creating a new directory. In this example the directory created will be named js-project.

```

		$ mkdir react-project-jan20

```

Next, change directory (cd) to the newly created directory:

```

		$ cd react-project-jan20

```

Create a package.json file. This will be required to allow NPM (Node Package Manager) packages/modules to be installed:

```

		$ npm init -y

```

## Install Webpack

NPM (Node Package Manager) will be used to install Webpack within the project. The webpack and webpack-cli packages will be installed as devDependencies. Within the terminal, enter the following command:

```

		$ npm install webpack webpack-cli --save-dev

```

Both packages will be listed within the package.json file as devDependencies. A package-lock.json file and node_modules directory will now be generated within the project folder.

Once installed we can run webpack

## Setup Webpack

Begin by opening the package.json file and adding a build script. This will allow Webpack to be run from within the terminal. In this example the build script is named 'build':

```

		scripts {
			"build": "webpack"
		}

```

Webpack requires a src directory to be created. Begin by creating a src directory within the project folder:

```

		$ mkdir src

```

Within this newly created src directory, create an empty JavaScript file. This needs to be named index.js as this is the default file Webpack will look for. For Mac's ONLY, you can use 'touch'.

```

		$ cd src
		$ touch index.js //Mac only

```

Open the index.js file and add a single line of JavaScript code:

```

		console.log("Hello World");

```

### Run Webpack

To run Webpack, enter the following command in your terminal:

```

		$ npm run build

```

This will run the build script inside the package.json file. Once executed, this command will create a distribution directory inside the project folder named 'dist'. Within this directory, a bundled JavaScript file will be created named main.js.
