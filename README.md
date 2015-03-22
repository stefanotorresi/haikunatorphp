# HaikunatorPHP

[![Build Status](https://img.shields.io/travis/Atrox/haikunatorphp.svg?style=flat-square)](https://travis-ci.org/Atrox/haikunatorphp)

Generate Heroku-like random names to use in your PHP applications.

## Installation

```
composer require atrox/haikunator
```

## Usage

Haikunator is pretty simple.

```php
use Atrox\Haikunator\Haikunator;

// default usage
Haikunator::haikunate() // => "wispy-dust-1337"

// custom length (default=4)
haikunate(["tokenLength" => 6]) // => "patient-king-887265"

// use hex instead of numbers
haikunate(["tokenHex" => true]) // => "purple-breeze-98e1"

// use custom chars instead of numbers/hex
haikunate(["tokenChars" => "HAIKUNATE"]) // => "summer-atom-IHEA"

// don't include a token
haikunate(["tokenLength" => 0]) // => "cold-wildflower"

// use a different delimiter
haikunate(["delimiter" => "."]) // => "restless.sea.7976"

// no token, space delimiter
haikunate(["tokenLength" => 0, "delimiter" => " "]) // => "delicate haze"

// no token, empty delimiter
haikunate(["tokenLength" => 0, "delimiter" => ""]) // => "billowingleaf"
```

## Options

The following options are available:

```javascript
haikunate([
  "delimiter" => "-",
  "tokenLength" => 4,
  "tokenHex" => false,
  "tokenChars" => "0123456789"
]);
```
*If ```tokenHex``` is true, it overrides any tokens specified in ```tokenChars```*

## Contributing

Everyone is encouraged to help improve this project. Here are a few ways you can help:

- [Report bugs](https://github.com/atroxdev/haikunatorphp/issues)
- Fix bugs and [submit pull requests](https://github.com/atroxdev/haikunatorphp/pulls)
- Write, clarify, or fix documentation
- Suggest or add new features

## Other Languages

Haikunator is also available in other languages. Check them out:

- Python: https://github.com/Atrox/haikunatorpy
- Node: https://github.com/Atrox/haikunatorjs
- Ruby: https://github.com/usmanbashir/haikunator
- Go: https://github.com/yelinaung/go-haikunator