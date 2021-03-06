# {%= name %}

{% if (travis) { %}[![Build Status](https://secure.travis-ci.org/{%= git_user %}/{%= git_repo %}.png?branch=master)](http://travis-ci.org/{%= git_user %}/{%= git_repo %}){% } %}{% if (coveralls) { %} [![Coverage Status](https://coveralls.io/repos/{%= git_user %}/{%= git_repo %}/badge.png)](https://coveralls.io/r/{%= git_user %}/{%= git_repo %}){% } %} [![Dependency Status](https://david-dm.org/{%= git_user %}/{%= git_repo %}.png?theme=shields.io)](https://david-dm.org/{%= git_user %}/{%= git_repo %}) [![devDependency Status](https://david-dm.org/{%= git_user %}/{%= git_repo %}/dev-status.png?theme=shields.io)](https://david-dm.org/{%= git_user %}/{%= git_repo %}#info=devDependencies)


{%= description %}

## Getting Started
Install the module with: `npm install {%= name %}`


## Documentation
_(Coming soon)_

## Tests
Tests are written using [jasmine](http://pivotal.github.io/jasmine/) (Behavior-Driven Development framework for testing javascript code). Thanks to [jasmine-node](https://github.com/mhevery/jasmine-node), this test framework is also available for Node.js.

To run tests, simple execute the *test* task using `grunt`.

```bash
$ grunt test
```

## Examples
_(Coming soon)_

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).
More info [here](CONTRIBUTING.md)

## Releasing
Releasing a new version is completely automated using the Grunt task `grunt release`.

```javascript
grunt release // patch release
grunt release:minor // minor release
grunt release:major // major release
```

## Styleguide
We <3 CoffeeScript here at commercetools! So please have a look at this referenced [coffeescript styleguide](https://github.com/polarmobile/coffeescript-style-guide) when doing changes to the code.

## License
Copyright (c) {%= grunt.template.today('yyyy') %} {%= author_name %}
Licensed under the {%= licenses.join(', ') %} license{%= licenses.length === 1 ? '' : 's' %}.
