# puppeteer-heroku-buildback-fonts

Heroku buildpack adding missing fonts for [jontewks/puppeteer-heroku-buildpack](https://elements.heroku.com/buildpacks/jontewks/puppeteer-heroku-buildpack)

This buildpack add 22MBs of fonts to the built Heroku slug size so it is not added by default.

It aims to support (Chinese, Japanese, Arabic, Hebrew, Thai, Hindi and a few others). It will support all the language that [puppeteer/puppeteer](https://github.com/puppeteer/puppeteer) docker image supports
If you are facing missing character sets, feel free to open a PR.

## Usage

```sh-session
# clear cache and current buildpacks
heroku builds:cache:purge
heroku buildpacks:clear

# puppeteer
heroku buildpacks:add -i 1 jontewks/puppeteer

# fonts
heroku buildpacks:add -i 2 https://github.com/anandtripathi5/puppeteer-heroku-buildpack-fonts

# other buildpack
heroku buildpacks:add -i 3 heroku/nodejs
```

# Credits

Thanks to [@jonknapp](https://github.com/jonknapp) for its initial fork (see https://github.com/CoffeeAndCode/puppeteer-heroku-buildpack/pull/3)
