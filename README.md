GNU Parallel for Heroku
=======================

[Parallel](https://www.gnu.org/software/parallel/) is a shell tool for executing jobs in parallel.

This buildpack will make & install the executable to `/app/.heroku/gnu-parallel/bin/parallel`, and it is automatically put on the `$PATH` via [.profile.d script](.profile.d/000-gnu-parallel.sh).

Usage
-----

Add this buildpack to your app before other buildpacks:

```bash
heroku buildpacks:add -i 1 https://github.com/mars/heroku-buildpack-gnu-parallel
```

Then, redeploy your app.

Specify the version
-------------------

Commit the file `.gnu_parallel_version` to you app containing the version part of the [distribution file name](https://ftp.gnu.org/gnu/parallel/), such as `20171022` or `latest`.

Default version: `latest`
