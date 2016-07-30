# bananacss.github.io

> The Banana CSS website.

## Run the project locally

**1 -** Clone the project and install the dependencies:

```sh
$ git clone https://github.com/bananacss/bananacss.github.io.git
$ cd bananacss.github.io
$ npm install
```

**2 -** Run the metalsmith:

```sh
$ metalsmith
```

Go to: [localhost:3000](http://localhost:3000/)
## Stack

Stack based in NodeJS:

- Static Generator: [Metalsmith](http://www.metalsmith.io/)
- HTML Template Engine: [Handlebars](http://handlebarsjs.com/)
- <s>CSS Superset: [Banana CSS](https://github.com/bananacss/bananacss.github.io)</s>
- <s>JS Traspiler: [BabelJS](https://babeljs.io/)</s>

Vendors:

- SPA: [SennaJS]()
- CSS Reset: [Normalize](https://necolas.github.io/normalize.css/)

Folders Structure:

	.
	├── README.md
	├── build/
	├── src/
	|   ├── assets/
	|   ├── partials/
	|   ├── layouts/
	|   ├── playground/
	|   ├── docs/
	|   └── index.jade
	├── metalsmith.js
	├── package.json
	├── .editorconfig
	├── .jshintrc
	└── .gitignore

## Versioning

To keep better organization of releases we follow the [Semantic Versioning 2.0.0](http://semver.org/) guidelines.

## Contributing

Find on our [roadmap](https://github.com/bananacss/bananacss.github.io/issues/1) the next steps of the project ;)
<br>
Want to contribute? [Follow these recommendations](https://github.com/bananacss/bananacss.github.io/blob/master/CONTRIBUTING.md).

## History

See [Releases](https://github.com/bananacss/bananacss.github.io/releases) for detailed changelog.

## License

[MIT License](https://github.com/bananacss/bananacss.github.io/blob/master/LICENSE.md) © [Afonso Pacifer](http://afonsopacifer.com/)
