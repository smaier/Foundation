# Respect\Foundation

[![Build Status](https://travis-ci.org/Respect/Foundation.png?branch=master)](https://travis-ci.org/Respect/Foundation)

A conventional project tool for PHP and git.

**This is a work in progress! Several features are missing. [Get in touch...](https://github.com/Respect/Foundation/issues)**

Works out of the box with:

  * PEAR
  * Onion
  * Composer
  * Pirum
  * PHPUnit
  * New and pre-existing projects

## Installation

Make sure you have curl, git PHP and PEAR installed. On your project
folder, run:

    curl -LO https://raw.githubusercontent.com/Respect/Foundation/master/Makefile && make foundation

This command line will install and/or update your Foundation
installation.

## Usage

Type `make help` to see all available targets.

To see what Foundation has discovered about your project, run `make project-info`.

You can modify the package.ini file only. Changes in that file will
propagate to other package files when you run `make package`.


### Using your own Makefile

If you want to tweak your own `Makefile` and use it instead of the *defuault* one:

    export FOUNDATION_URL=http://my.domain.com/raw/Makefile/url; make foundation

This will only use a different `Makefile`, Foundation has a PHP library included to
discover some information about the project itself. For that, this repository is cloned,
but the URL is also exposed through the `FOUNDATION_REPO` environment variable which
can be overriden as shown above.
