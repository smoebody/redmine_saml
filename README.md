# Redmine OmniAuth SAML plugin

This plugins adds SAML authentication support for [Redmine](https://www.redmine.org) based on [OmniAuth authentication framework](https://github.com/omniauth/omniauth) with [omniauth-saml](https://github.com/omniauth/omniauth-saml).

[![Run Linters](../../workflows/Run%20Linters/badge.svg)](../../actions?query=workflow%3A%22Run+Linters%22) [![Run Brakeman](../../workflows/Run%20Brakeman/badge.svg)](../../actions?query=workflow%3A%22Run+Brakeman%22) [![Run Tests](../../workflows/Tests/badge.svg)](../../actions?query=workflow%3ATests)

## Install

You can first take a look at general instructions for plugins [here](https://www.redmine.org/wiki/redmine/Plugins).

Note that the plugin is now *only compatible with Redmine 4.1.x or higher.

Then :

* clone this repository in your plugins/ directory ; if you have a doubt you put it at the good level, you can go to your redmine root directoryand check you have a @plugins/redmine_saml/init.rb@ file
* install the dependencies with bundler: @bundle install@
* run migration: @bundle exec rake redmine:plugins:migrate RAILS_ENV=production@
* restart your Redmine instance (depends on how you host it)

Finally you *must* configure your SAML settings adding a file in @<redmine_folder>/config/initializers@ for example named @saml.rb@ (the name is not important, but it must be a ruby file). A sample file is given in the plugin root folder named @sample-saml-initializers.rb@
For more information about configuration options, see <https://github.com/omniauth/omniauth-saml#options>

Finaly you need to configure some minor options for the plugin to work, in "Administration" > "Plugins" > "Configure" on the OmniAuth SAML plugin line.

## Support & contribution

If you have any wishes or improvements, PRs are welcome!

## Credits

Its a fork of

* <https://github.com/chrodriguez/redmine_omniauth_saml>
* <https://github.com/jbbarth/redmine_omniauth_cas>

Many thanks to them!
