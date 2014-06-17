Heroku buildpack: unzip
======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks)
for adding unzip to your application.

Multipacks
----------

More likely, you'll want to use it as part of a larger project, which needs to use zip. The easiest way to do this is with a [multipack](https://github.com/ddollar/heroku-buildpack-multi),
where this is just one of the buildpacks you'll be working with.

    $ cat .buildpacks
    git://github.com/heroku/heroku-buildpack-ruby.git
    git://github.com/davidlibrera/heroku-buildpack-unzip.git
    git://github.com/vidpresso/heroku-buildpack-zip.git

    $ heroku config:add BUILDPACK_URL=git://github.com/ddollar/heroku-buildpack-multi.git

This will bundle unzip into your instance without impacting your existing
system.
