heroku-buildpack-tesseract
===========================

This buildpack is built to be used through [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi).
In your app you need to:
```
heroku config:set BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi
```

Then, create a `.buildpacks` file inside your app:
```
https://github.com/heroku/_YOUR_MAIN_BUILDPACK
https://github.com/Papiel/Heroku-multi-deploy-buildpack
```
See the documentation of heroku-build-multi for a detailed explanation
how to use it.

# Variables
You need to define some variable into your heroku app:

```bash
heroku config:set NAME=_HEROKU_APP_NAME
heroku config:set GIT_REPO=_GIT_URL_REPOSITORY
heroku config:set NUM_INSTANCES=_NUMBER_OF_HEROKU_INSTANCES
heroku config:set NETRC=_YOUR_.NETRC_FILE
```
Example:
```bash
heroku config:set NAME=anyfetch-hydrater-plaintext
heroku config:set GIT_REPO=git@github.com:Papiel/plaintext.hydrater.anyfetch.com.git
heroku config:set NUM_INSTANCES=4
netrc=$(<~/.netrc)
heroku config:set NETRC=$netrc
```


