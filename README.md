# Docker Alpine PHP with Composer

A very small Docker image to bootstrap your PHP development.

This Docker image is based on [petehouston/docker-alpine-php](https://github.com/petehouston/docker-alpine-php) but with [Composer](getcomposer.org) supported.

### Support Versions

Following PHP versions are supported,

* [tag:7.0](src/7.0/Dockerfile) - latest (7.0.6)
* [tag:5.6](src/5.6/Dockerfile) (5.6.21)
* [tag:5.5](src/5.5/Dockerfile) (5.5.35)

### How to use?

First, pull to your local development machine,

```
$ docker pull petehouston/docker-alpine-php-composer
```

Then run the `composer` command in the mount directory

```
$ docker run --rm -v $(pwd):/home -w /home petehouston/docker-alpine-php-composer:5.6 composer require phpunit/phpunit
```

### Build

The repo uses `make` to execute the command, so you can either use `make` to build or manually issue the commands.

The build commands are listed below:

* `make php-5.5`: to build image for PHP 5.5.
* `make php-5.6`: to build image for PHP 5.6.
* `make php-7.0`: to build image for PHP 7.0.
* `make build`:to build images for all PHP versions.
* `make test`: to execute image tests.
* `make all` or `make`: to execute build and test
* `make clean`: to remove all images.

### Testing

The test suite is located in [tests/index.sh](tests/index.sh).

### Notes

Please share your words if any. Always welcome :)