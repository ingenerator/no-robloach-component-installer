This very simple empty package replaces robloach/component-installer with a stub that
does nothing and has no dependencies.

This allows us to consume front-end and similar resource packages that require 
robloach/component-installer, but skip the extra PHP dependencies and automatic 
resource packaging scripts that extension defines, because they're not relevant
to our preferred asset build and distribution process.

Use it like `composer require ingenerator/no-robloach-component-installer` and 
then run `composer update` to remove any orphaned dependencies.
  
Note that the .gitattributes excludes absolutely everything apart from 
composer.json from exported git archive files by default, because literally all
this package needs is the json.
