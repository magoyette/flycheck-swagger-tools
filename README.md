# flycheck-swagger-tools

An Emacs Flycheck checker for Swagger YAML and JSON files that uses [swagger-tools](https://github.com/apigee-127/swagger-tools).

flycheck-swagger-tools is still under initial development and might not be stable.

## Configuration

[swagger-tools](https://github.com/apigee-127/swagger-tools) must be installed.

``` shell
npm install -g swagger-tools
```

The checker can be activating by requiring this package.

``` emacs-lisp
(require 'flycheck-swagger-tools)
```

By default, only the first 4000 characters of a file are scanned to find the swagger 2.0 element. To avoid stack overflow in Emacs multi-line regex, this limit is necessary. The defcustom swagger-tools-predicate-regexp-match-limit can be used to change the limit. That could be necessary for YAML files with long initial comments.
