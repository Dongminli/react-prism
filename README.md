# react-prism
> React.js + Prism.js syntax highlight component

[![Version][npm-image]][npm-url] [![Travis CI][travis-image]][travis-url] [![Quality][codeclimate-image]][codeclimate-url] [![Coverage][codeclimate-coverage-image]][codeclimate-coverage-url] [![Dependencies][gemnasium-image]][gemnasium-url] [![Gitter][gitter-image]][gitter-url]


## Installation

```sh
npm i --save react-prism
```


## Demo

Static hosted [demo site][demo] on GitHub.


## Example

Please refer to the [client][client] folder for an example.


## Usage

This module is intended to be bundled with [webpack][webpack]/browserify.


First, you have to include [prismjs][prismjs] in your `index.html`:

```html
<script src="path/to/your/prism.js"></script>
```

**Why not require Prism by CommonJS?**
It's because prism.js will try to run itself as a Web Worker. It won't take affect if we require it into the source.

Then:

```javascript
import {PrismCode} from "react-prism";

  // In a react component:
  render () {
    return (
      <PrismCode className="language-javascript">
        {require("raw-loader!./PrismCode")}
      </PrismCode>
    );
  }
```


## Development

```shell
git clone ...
npm install
cd examples/gh-pages
npm install
npm start
```

Then open [http://localhost:8080](http://localhost:8080).


## Contributing

[![devDependency Status][david-dm-image]][david-dm-url]

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new pull request


## Credits

* [`prismjs`][prismjs]


[npm-image]: https://img.shields.io/npm/v/react-prism.svg?style=flat-square
[npm-url]: https://www.npmjs.org/package/react-prism

[travis-image]: https://img.shields.io/travis/tomchentw/react-prism.svg?style=flat-square
[travis-url]: https://travis-ci.org/tomchentw/react-prism
[codeclimate-image]: https://img.shields.io/codeclimate/github/tomchentw/react-prism.svg?style=flat-square
[codeclimate-url]: https://codeclimate.com/github/tomchentw/react-prism
[codeclimate-coverage-image]: https://img.shields.io/codeclimate/coverage/github/tomchentw/react-prism.svg?style=flat-square
[codeclimate-coverage-url]: https://codeclimate.com/github/tomchentw/react-prism
[gemnasium-image]: https://img.shields.io/gemnasium/tomchentw/react-prism.svg?style=flat-square
[gemnasium-url]: https://gemnasium.com/tomchentw/react-prism
[gitter-image]: https://badges.gitter.im/Join%20Chat.svg
[gitter-url]: https://gitter.im/tomchentw/react-prism?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge
[david-dm-image]: https://img.shields.io/david/dev/tomchentw/react-prism.svg?style=flat-square
[david-dm-url]: https://david-dm.org/tomchentw/react-prism#info=devDependencies


[demo]: http://tomchentw.github.io/react-prism/
[client]: https://github.com/tomchentw/react-prism/tree/master/client
[webpack]: http://webpack.github.io/docs/tutorials/getting-started/
[prismjs]: http://prismjs.com/
