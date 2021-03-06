RigUp Laptop
======

RigUp Laptop is a script to set up an macOS laptop for web and mobile development.

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

Contents
--------
- [Requirements](#requirements)
- [Install](#install)
- [What it sets up](#what-it-sets-up)
- [RigUp Stack & Versions](#rigup-stack--versions)
- [Debugging](#debugging)

Requirements
------------

Support for the following OS versions are confirmed:

* macOS High Sierra (10.13)

Older versions may work but aren't regularly tested.
Bug reports for older versions are welcome.

Install
-------

Download the script:

```sh
curl --remote-name https://raw.githubusercontent.com/rjny/rigup_laptop/master/mac
```

Review the script (avoid running scripts you haven't read!):

```sh
less mac
```

Execute the downloaded script:

```sh
sh mac 2>&1 | tee ~/laptop.log
```

Optionally, review the log:

```sh
less ~/laptop.log
```

What it sets up
---------------

The entire script typically takes less than 10 minutes to install (depends on your machine).

#### macOS tools:

* [Homebrew] for managing operating system libraries. 🍺

[Homebrew]: http://brew.sh/

#### Unix tools:

* [Git] for version control

[Git]: https://git-scm.com/

#### GitHub tools:

* [Hub] for interacting with the GitHub API

[Hub]: http://hub.github.com/

#### Heroku tools:

* [Heroku CLI] and [Parity] for interacting with the Heroku API

[Heroku CLI]: https://devcenter.heroku.com/articles/heroku-cli

#### Programming languages, package managers, and configuration:

* [Bundler] for managing Ruby libraries
* [Node.js] and [NPM], for running apps and installing JavaScript packages
* [n] for node version management
* [rbenv] for ruby version management
* [Ruby] stable for writing general-purpose code
* [Elasticsearch] for RESTful search and analytics
  * [Java8] dependency for Elasticsearch.

[Bundler]: http://bundler.io/
[Node.js]: http://nodejs.org/
[n]: https://github.com/tj/n
[rbenv]: https://github.com/rbenv/rbenv
[NPM]: https://www.npmjs.org/
[Ruby]: https://www.ruby-lang.org/en/
[Elasticsearch]: https://www.elastic.co/
[Java8]: https://www.oracle.com/technetwork/java/javase/overview/java8-2100321.html

#### Databases:

* [Postgres] for storing relational data

[Postgres]: http://www.postgresql.org/

RigUp Stack & Versions
---------------

- AngularJS `1.5.8`
- Ruby on Rails `4.2.5.1`
- Ruby `2.3.3`
- node `8.9`
- NPM `5.6`

Debugging
---------

Your last Laptop run will be saved to `~/laptop.log`.
Read through it to see if you can debug the issue yourself.
If not, copy the lines where the script failed into a
[new GitHub Issue](https://github.com/rjny/rigup_laptop/issues/new) for us.
Or, attach the whole log file as an attachment.
