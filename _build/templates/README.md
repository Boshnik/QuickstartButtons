What you need
--------------------------------------

In order to build QuickstartButtons front end assets, you need to have Ruby, Node.js/npm latest and git 1.7 or later.
(Earlier versions might work OK, but are not tested.)

For Windows you have to download and install [git](http://git-scm.com/downloads) and [Node.js](http://nodejs.org/download/).

Mac OS users should install [Homebrew](http://mxcl.github.com/homebrew/). Once Homebrew is installed, run `brew install git` to install git,
and `brew install node` to install Node.js.

Linux/BSD users should use their appropriate package managers to install git and Node.js, or build from source
if you swing that way. Easy-peasy.

Installing Ruby and Ruby Gems
----------------------------
You'll need ruby and sass gems installed. If you're on OS X or Linux you probably already have Ruby installed; test with ruby -v in your terminal. When you've confirmed you have Ruby installed, run gem install sass to install Sass.

```bash
gem install sass
```

Make sure you have `sass` installed by testing:

```bash
sass --version
```
_Note: Depending on your ruby setup you may need to install gems using `sudo gem install sass`._

Installing Grunt & Grunt Packages
----------------------------

First, clone a copy of this git repo by running:

```bash
git clone git://github.com/modmore/QuickstartButtons.git
```

Install the [grunt-cli](http://gruntjs.com/getting-started#installing-the-cli) package if you haven't before. This should be done as global install:

```bash
npm install -g grunt-cli
```

Make sure you have `grunt`installed by testing:

```bash
grunt --version
```

If grunt comes back as command not found on OS X, you may need to update your PATH. [See this page for more details](http://www.hongkiat.com/blog/grunt-command-not-found/)

Enter the default template directory and install the Node dependencies, this time *without* specifying a global(-g) install:

```bash
cd revolution/_build/templates/default
npm install
```
_Note: `npm install` updates dependencies and should be run whenever you pull from git._

Optionally enable Growl notifications install [terminal-notifier](https://github.com/alextucker/grunt-growl#getting-started) with RubyGems:
```bash
gem install terminal-notifier
```
_Note: Depending on your ruby setup you may need to install gems using `sudo gem install terminal-notifier`._

Grunt Commands
----------------------------

__Build__<br>
Build Sass files by running:

```bash
grunt build
```

__Watch__<br>
Compile the Sass and watch files for changes type the following:

```bash
grunt
```
_Note: grunt is now watching files for changes. When Sass files are changed CSS will automatically be generated.<br>Install the LiveReload [browser extension](http://feedback.livereload.com/knowledgebase/articles/86242-how-do-i-install-and-use-the-browser-extensions-) to inject CSS changes without a page refresh._
