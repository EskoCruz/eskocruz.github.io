## A New Post

`$ brew install postgresql`

    ==> Installing dependencies for postgresql: readline
    ==> Installing postgresql dependency: readline
    ==> Downloading https://homebrew.bintray.com/bottles/readline-7.0.1.sierra.bottle.tar.gz
    ######################################################################## 100.0%
    ==> Pouring readline-7.0.1.sierra.bottle.tar.gz
    ==> Caveats
    This formula is keg-only, which means it was not symlinked into /usr/local.
    
    macOS provides the BSD libedit library, which shadows libreadline.
    In order to prevent conflicts when programs look for libreadline we are
    defaulting this GNU Readline installation to keg-only.
    
    
    Generally there are no consequences of this for you. If you build your
    own software and it requires this formula, you'll need to add to your
    build variables:
    
        LDFLAGS:  -L/usr/local/opt/readline/lib
        CPPFLAGS: -I/usr/local/opt/readline/include
    
    ==> Summary
    🍺  /usr/local/Cellar/readline/7.0.1: 46 files, 2M
    ==> Installing postgresql
    ==> Downloading https://homebrew.bintray.com/bottles/postgresql-9.6.1.sierra.bottle.tar.gz
    ######################################################################## 100.0%
    ==> Pouring postgresql-9.6.1.sierra.bottle.tar.gz
    ==> Using the sandbox
    ==> /usr/local/Cellar/postgresql/9.6.1/bin/initdb /usr/local/var/postgres
    ==> Caveats
    If builds of PostgreSQL 9 are failing and you have version 8.x installed,
    you may need to remove the previous version first. See:
      https://github.com/Homebrew/homebrew/issues/2510
    
    To migrate existing data from a previous major version (pre-9.0) of PostgreSQL, see:
      https://www.postgresql.org/docs/9.6/static/upgrading.html
    
    To migrate existing data from a previous minor version (9.0-9.5) of PostgreSQL, see:
      https://www.postgresql.org/docs/9.6/static/pgupgrade.html

      You will need your previous PostgreSQL installation from brew to perform `pg_upgrade`.
      Do not run `brew cleanup postgresql` until you have performed the migration.
    
    To have launchd start postgresql now and restart at login:
      brew services start postgresql
    Or, if you don't want/need a background service you can just run:
      pg_ctl -D /usr/local/var/postgres start
    ==> Summary
    🍺  /usr/local/Cellar/postgresql/9.6.1: 3,242 files, 36.4M
    
    Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above,     or click the **?** button for formatting help.
