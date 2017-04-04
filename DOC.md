## System Preparation

To use this starter project, you'll need the following things installed on your machine.


### Required

- [Git](https://git-scm.com)
- Install [Ruby](https://www.ruby-lang.org/en/downloads/) with either rbenv, or with a operating system's package manager.
	- **Ways of Installing Ruby**
		- On Linux/UNIX, you can either use the package management system of your distribution or third-party tools (rbenv and RVM).
		- On OS X machines, you can use third-party tools (rbenv and RVM).
		- On Windows machines, you can use RubyInstaller.
	- **Use [rbenv](https://github.com/rbenv/rbenv#readme) to manage multiple Ruby versions.**
		- After installing `rbenv`, you also need [ruby-build](https://github.com/rbenv/ruby-build#readme) plugin for compiling Ruby.
	- If you are using OS X, you probably already have some version of Ruby installed.
		- It might still make sense to install latest version with rbenv.
- After you have installed Ruby, install:
	- [Jekyll](http://jekyllrb.com/)
		- `gem install jekyll`
	- [Bundler](http://bundler.io/)
		- `gem install bundler`
			- (OS X users might also need `sudo` in the beginning, if you use system-wide Ruby installation.)
- [NodeJS](http://nodejs.org)
	- Good way to install Node.js is to use [nvm](https://github.com/creationix/nvm) (_Node Version Manager_)
		- [Installing Node.js for Ubuntu with nvm](https://gist.github.com/d2s/372b5943bce17b964a79)
- After you have installed Node.js, install:
	- [GulpJS](https://github.com/gulpjs/gulp) - `npm install -g gulp` (mac users may need sudo)
	- [Bower](http://bower.io/) - `npm install -g bower`


### Optional tools
- [Composer](https://getcomposer.org) (installs PHPMailer)
- [Make](https://www.gnu.org/software/make) (used with rsync for deploying)


## Local Installation

Git clone this repository, or download it into a directory of your choice.  
Inside the directory run:

1. `bower install` (reference: .bowerrc and bower.json)
2. `npm install` (reference: package.json)
3. `bundle install` (reference: Gemfile and Gemfile.lock)
4. _Disabled: `composer install` (optional, reference: composer.json and composer.lock))_

**Do all that in one step:** `make install`


## Usage

### Tasks
- `npm start`
	- This will build your Jekyll site, give you file watching, browser synchronization, auto-rebuild, CSS injecting, Sass sourcemaps etc.

- `npm run build`  
	- This builds your site for production, with minified CSS and JavaScript. Run this before you deploy your site!


#### How to view the site

- `http://127.0.0.1:3000`  
	- Here you can access your site. If you want to access it with your phone or tablet, use the external access address which is showing up in the terminal window.

- `http://127.0.0.1:3001`  
	- Access the Browsersync UI.



##### If you enable xip.io support, you can also use:

- `http://127.0.0.1.xip.io:3000`
	- Here you can access your site. If you want to access it with your phone or tablet, use the external access address which is showing up in the terminal window.

- `http://127.0.0.1.xip.io:3001`
	- Access the Browsersync UI.


## Foundation for Sites Components

We don't want to include unused CSS or JavaScript.

	Uncomment the components you want to use
	1. Sass in `/assets/scss/foundation/_foundation.scss`
	2. JavaScript in `/gulp/config.yml` in javascript.src (you need to restart gulp)

Customize the variables used by Foundation in the settings file located in `/assets/scss/foundation/`.  

Place your custom sass in the subfolders of `/assets/scss/`. These folders follow the [SMACSS](https://smacss.com/) architecture. This should be the most scalable solution - from small to very large sites.  

### Deploy your site
Rsync is used here to sync our local `_site` with the remote host. Adjust the SSH-USER, SSH-HOST and REMOTE-PATH in the Makefile.

Be careful with these settings since rsync is set to **delete** the files on the remote path!

Deploy with `make deploy`.

## Restrictions

### compress.html layout

Inline JavaScript can become broken where // comments used. Please remove the comments or change to /**/ style.
[compress.html Docs](http://jch.penibelst.de/)
