WDIO Sauce Labs Service [![Build Status](https://travis-ci.org/webdriverio/wdio-sauce-service.svg?branch=master)](https://travis-ci.org/webdriverio/wdio-sauce-service) [![Code Climate](https://codeclimate.com/github/webdriverio/wdio-sauce-service/badges/gpa.svg)](https://codeclimate.com/github/webdriverio/wdio-sauce-service) [![Test Coverage](https://codeclimate.com/github/webdriverio/wdio-sauce-service/badges/coverage.svg)](https://codeclimate.com/github/webdriverio/wdio-sauce-service/coverage)
==========

> A WebdriverIO service. It updates the job metadata ('name', 'passed', 'tags', 'public', 'build', 'custom-data') and runs Sauce Connect if desired.

## Installation

The easiest way is to keep `wdio-sauce-service` as a devDependency in your `package.json`.

```json
{
  "devDependencies": {
    "wdio-sauce-service": "~0.1"
  }
}
```

You can simple do it by:

```bash
npm install wdio-sauce-service --save-dev
```

Instructions on how to install `WebdriverIO` can be found [here.](http://webdriver.io/guide/getstarted/install.html)

## Configuration

In order to use the service you need to set `user` and `key` in your `wdio.conf.js` file. It will automatically
use Sauce Labs to run your integration tests. If you want to use [Sauce Connect](https://wiki.saucelabs.com/display/DOCS/Using+Sauce+Connect+for+Testing+Behind+the+Firewall+or+on+Localhost)
you just need to set `sauceConnect: true`.

```js
// wdio.conf.js
module.exports = {
  // ...
  user: process.env.SAUCE_USERNAME,
  key: process.env.SAUCE_ACCESS_KEY,
  sauceConnect: true,
  // ...
};
```

## Options

### user
Your Sauce Labs username.

Type: `String`

### key
Your Sauce Labs access key.

Type: `String`

### sauceConnect
If true it runs Sauce Connect and opens a secure connection between a Sauce Labs virtual machine running your browser tests.

Type: `Boolean`<br>
Default: `false`

----

For more information on WebdriverIO see the [homepage](http://webdriver.io).
