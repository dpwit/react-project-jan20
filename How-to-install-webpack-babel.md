# Webpack: Babel

## ES6 (ECMAScript 6)

Modern JavaScript code can be written in the ES6 (ECMAScript 6) syntax. This brings new syntax and features to make your code more modern and more readable it also allows you to write less code and do more. ES6 however, is not supported by all browsers. We therefore need to transpile the code to turn your ES6 syntax into ES5 for use in browsers that don't provide native support for ES6.

We can use Babel to transpile our ES6 code into ES5.

## Install Babel

NPM (Node Package Manager) will be used to install the packages requires to setup Babel. Here is the list of packages to be installed:

* @babel/core - The main dependency that includes the Babel transform script
* @babel/preset-env  - The default Babel preset used to transfrom ES6+ into valid ES5 code and to optionally configure browser polyfills
* babel-loader - A Webpack loader that hooks Babel into Webpack allowing Babel to run when using Webpack

Open the terminal and install the packages listed above as devDependencies:

```

		$ npm install @babel/core @babel/preset-env babel-loader --save-dev

```

The $ symbol at the start of a code line is used to identify that this is a terminal command. When entering the command, the $ symbol is not needed.

## Updating the Webpack Config

The Webpack config file, named webpack.config.js, is placed within the root of your project folder/directory. Although Webpack is referred to as 'zero-configuration', it mostly applies to general defaults such as entry and output. The Webpack config file will need to be updated to apply Babel.

Open the webpack.config.js file and add the following code:

```

		module.exports = {
			module: {
				rules: [
					{
						test: /\.js$/,
						exclude: /node_modules/,
						use: {
							loader: 'babel-loader'
						}
					}
				]
			}
		}

```

## Babel config file

To allow Babel to work, a Babel config file needs to be created. This config file is named .babelrc and should be placed within the root of your project directory.

Begin by creating the .babelrc config file:

```

		$ touch .babelrc

```

The .babelrc file once created maybe hidden in your project folder. Use CTRL + SHIFT + . (dot) to see the hidden file(s).

This will create an empty config file. Open the .babelrc config file and add the following code:

```

		{
			"presets": [ "@babel/preset-env" ]
		}

```

## Running Babel

Now that Babel has been setup within your Webpack configuration, you can now write JavaScript in the latest ES6 syntax and have it transpiled into ES5 syntax for use across all browsers. Begin by opening the index.js file within the src directory of your project and add the following ES6 code example:

```

		const sayHello = () => {
			console.log("Hello World")
		}

		sayHello()

```

As an example of ES6 we are using the ES6 Arrow function syntax to demonstrate Babel in action.

To run Webpack, simply use the build script within the package.json file:

```

		$ npm run build

```

When the build runs the code written in ES6 within the index.js file will be transpiled by Babel using Webpack and will be added to the main.js bundle in the distribution (dist) directory as ES5 syntax.
