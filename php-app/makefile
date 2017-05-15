# Building an application
# + Update Source From Repository
# + Installing The dependencies
# + Running PHPUnit Tests
# + Installing Front End Dependencies
# + File permissions
# + Generate
# Reference: http://codesamplez.com/management/build-php-web-application-makefile

.PHONY: all update-repo dependency-install unit-tests file-permission
 
all: update-repo dependency-install unit-tests file-permission
 
update-repo:
	git reset --hard
	git pull origin master
 
dependency-install:
	bower install
 
unit-tests:
	vendor/bin/phpunit
 
file-permission:
	chmod 765 application/logs
	chmod 765 application/cache
	chmod 765 application/models/proxies
