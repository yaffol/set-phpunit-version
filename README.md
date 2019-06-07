# Symfony PHPUnit Version

This repo demonstrates how it's possible to set the PHPUnit version installed by Symfony's PHPUnit Bridge by editing `phpunit.xml.dist`.

## Running
1. `docker run -u  $(id -u ${USER}):$(id -g ${USER}) -it --rm --volume $PWD:/app  prooph/composer:7.2  install`
2. Set `<server name="SYMFONY_PHPUNIT_VERSION" value="6.5" />` to the required version in `phpunit.xml.dist`.
3. `rm -rf bin/.phpunit`
4. `docker run -u  $(id -u ${USER}):$(id -g ${USER}) -it --rm --volume $PWD:/app --entrypoint /app/bin/phpunit prooph/composer:7.2
`

You can change the php version by adjusting the tag of the prooph/composer docker image eg `prooph/composer:7.1`
