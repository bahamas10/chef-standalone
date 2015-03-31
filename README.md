chef-standalone
===============

Build a standalone Chef installation on SmartOS - useful while omnibus is broken for this OS

Pre-built binaries are available at http://us-east.manta.joyent.com/bahamas10/public/chef-standalone/index.html

Example
-------

Build a standalone chef tarball on version `v12.2.1` of chef

    $ ./build-chef-tarball -v 12.2.1 smartos-chef-12.2.1-x64.tar.gz

This will install Ruby and Chef to `/opt/chef`, as well as create the tarball
specified as the first argument.

Usage
-----

    $ ./build-chef-tarball -h
    usage: build-chef-tarball [-v chef_version] [-r ruby_url] [-d cache_dir] [-h] <tarball_name.tar.gz>

    build a standalone chef tarball on SmartOS

    options
      -c <chef_dir>         the dir to use for install chef, defaults to /opt/chef
      -d <cache_dir>        the dir to use for caching ruby tarballs, defaults to ~/.standalone-chef
      -h                    print this message and exit
      -j <jobs>             number of jobs, will be passed as make -j <jobs>, defaults to 4
      -r <ruby_url>         the url of the ruby tarball to use, defaults to http://cache.ruby-lang.org/pub/ruby/2.2/ruby-2.2.1.tar.gz
      -v <chef_versio>      the chef version to install, defaults to 12.2.1

License
-------

MIT License
