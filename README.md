# heroku-buildpack-couchdb
just merge, push, sit and relax

If you are at the step of creating an app you can do the following:

`heroku create --buildpack https://github.com/AlexYates/heroku-buildpack-couchdb.git`

and thereby create the app. with the couchdb buildpack installed.

However, if you already have the app. you'll need to:

`heroku config:add BUILDPACK_URL="https://github.com/AlexYates/heroku-buildpack-couchdb.git" -a YOUR_APP`

The `-a YOUR_APP` is optional, you probably don't need it considering you're probably in a directory you've initialised as a Heroku app. when you added the buildpack.

Or, the easier:

`heroku buildpacks:set https://github.com/AlexYates/heroku-buildpack-couchdb.git`

after which you have to run:

`git push heroku master`

to deploy your buildpack.
