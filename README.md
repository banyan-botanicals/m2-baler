#Overview

## **It's non-official module yet. Just for alpha testing!**

Magento_Baler module introduces functionality to preload JS bundles configuration generated by https://github.com/DrewML/baler/ - tool for static analysis of Javascript dependencies.
This functionality is disabled by default and it can be enabled on the configuration page (Stores -> Configuration -> Advanced -> Developer -> Javascript Settings).
Developer settings is not displayed in production mode. To enable this feature in production mode, CLI command `bin/magento config:set dev/js/enable_baler_js_bundling 1` can be used.

### Installing with composer
Add the following to your magento project's composer.json file:
```json
{
    "require": {
        ...
        "magento/module-baler": "^0.1.0"
    },
    ...
    "repositories": {
        ...
        "adifucan": {
            "type": "vcs",
            "url": "git@github.com:adifucan/m2-baler.git",
            "no-api": true
        }
    }
}
```


### What is not implemented in this module yet:
1. The following features should be disabled when Magento_Baler is enabled:
   - JS Bundling
   - JS Minification
