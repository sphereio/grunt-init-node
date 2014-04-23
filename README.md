sphere-grunt-init
=================

[![Build Status](https://travis-ci.org/sphereio/sphere-grunt-init.png?branch=master)](https://travis-ci.org/sphereio/sphere-grunt-init)

This is a project template used for creating sphere node modules using [grunt-init](http://gruntjs.com/project-scaffolding) (scaffolding tool used to automate project creation).

[grunt-init]: http://gruntjs.com/project-scaffolding

## Installation
If you haven't already done so, install `grunt-init`
```bash
npm install -g grunt-init
```

Once `grunt-init` is installed, place this template in your `~/.grunt-init/` directory. It's recommended that you use git to clone this template into that directory, as follows:

```
git clone git@github.com:sphereio/sphere-grunt-init.git ~/.grunt-init/sphere-node
```

## Usage

At the command-line, create a new directory for the project you want to setup and change to that directory. Now run `grunt-init` command and follow the prompts.

```bash
# create dir and change into it
mkdir sphere-node-xyz
cd sphere-node-xyz/

grunt-init sphere-node
# or use the path to the template
grunt-init ~/dev/src/sphere-grunt-init
```

_Note that this template will generate files in the current directory, so be sure to change to a new directory first if you don't want to overwrite existing files._


## Project Setup

* run `chmod +x create_config.sh` (make script executable)
* create `config.js` by running `./create_config.sh`
  * add credentials (used only in local development)
* configure github/hipchat integration (see project *settings* in github)
* install travis gem `gem install travis`
* add encrpyted keys to `.travis.yml`
  * sphere project credentials

    ```bash
    travis encrypt SPHERE_PROJECT_KEY=your_key --add
    travis encrypt SPHERE_CLIENT_ID=your_id --add
    travis encrypt SPHERE_CLIENT_SECRET=your_secret --add
    ```
  * hipchat notifications

    ```bash
    travis encrypt your_token@Sphere --add notifications.hipchat.rooms
    ```
