# reproducer bug 3634

repro for https://github.com/phpstan/phpstan/issues/3634

# how to reproduce

- clone the repo
- run `composer install`
- run `vendor/bin/phpstan analyze -c app/phpstan.neon  --debug`
-> 'Call to an undefined method HttpResponse::deleteCookie()' error

expected result: no error, since the composer loadable HttpResponse should be preferred over the HttpResponse class from PHPStorm stubs.