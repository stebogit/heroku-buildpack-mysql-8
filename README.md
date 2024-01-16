# Heroku Buildpack MySQL 8

This is a [Heroku buildpack](https://devcenter.heroku.com/articles/buildpacks) that installs and adds the `mysql` 
and `mysqldump` binaries (v8.0) from the `mysql-client-core` deb package, which will be available in `$PATH` on 
your Dyno.

```
$ mysql --version
mysql  Ver 8.0.22-0ubuntu0.20.04.3 for Linux on x86_64 ((Ubuntu))

$ mysqldump --version
mysqldump  Ver 8.0.22-0ubuntu0.20.04.3 for Linux on x86_64 ((Ubuntu))
```

## Versions

* MySQL: `8.0` for `heroku-20` stack

> **Note:** it might have issues with different Heroku stack versions

## Usage

- via Heroku CLI:
   ```
   $ heroku buildpacks:add https://github.com/stebogit/heroku-buildpack-mysql-8
   $ git push heroku master
   ```

- or from the dashboard of your project

  ![heroku-dashboard](https://github.com/Turfjs/turf/assets/12717225/ffc60f76-a359-4eb6-bd9e-6547f41cd541)


```
-----> MySQL Client app detected
-----> MySQL Install mysql-client-core-8.0_8.0.22-0ubuntu0.20.04.3_amd64.deb
-----> MySQL set PATH
-----> MySQL Done 🎉
```

## Credits

I just [registered](https://devcenter.heroku.com/articles/buildpack-registry#registering-a-buildpack) 
[`olaoluwa-98`'s buildpack](https://github.com/olaoluwa-98/heroku-buildpack-mysql)
to [Heroku](https://elements.heroku.com/buildpacks) and updated the docs :
