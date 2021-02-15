---
layout: about
title: Install Jekyll
parent: Jekyll
has_children: true
has_toc: true

---

# Install

## Installing on MacOS

### Install Ruby 

Ensure you install Ruby, not the ruby from the Apple default install. It will give you this error:

```bash
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /Library/Ruby/Gems/2.6.0 directory.
```
Use Homebrew to install latest Ruby. If you haven't had Homebrew installed:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Then install Ruby

```bash
brew install ruby
```
Add Ruby path on your terminal:

```bash
# If you're using Zsh
echo 'export PATH="/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/X.X.X/bin:$PATH"' >> ~/.zshrc
# If you're using Bash
echo 'export PATH="/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/X.X.X/bin:$PATH"' >> ~/.bash_profile
# Unsure which shell you are using? Type
echo $SHELL
```
Refresh your shell

```bash
source ~/.zshrc
# or
source ~/.bash_profile
```
check the path and you shoud see anything other than: `/usr/local/bin/ruby` 
and check the version and it should be the latest:
```bash
which ruby
```

Mine would be:
```bash
/usr/local/opt/ruby/bin/ruby
```
Check ruby version

```bash
ruby -v
```

### Install Jekyll

Install the Bundler:

```bash
gem install --user-install bundler jekyll

```

### Create a new Jekyll site

Once the Jekyll is installed, you can start creating the site e.g in `/blog` folder:

```bash
jekyll new blog
```
+ In an indeal world you can just run `bundle exec jekyll serve` and will show you all details of configuration including the server you can go to in local, but since the following libraries are no longer bundled gems or standard libraries including `webrick`, this message will appear:

```bash
/usr/local/lib/ruby/gems/3.0.0/gems/jekyll-4.2.0/lib/jekyll/commands/serve/servlet.rb:3:in `require': cannot load such file -- webrick (LoadError)
```
Then you need to run `bundle add webrick` providing you have `bundle` installed.
This should let you run the `bundle exec jekyll serve` and the following message will appear:

```bash
Configuration file: /Users/irawan/dev/others/bloog/_config.yml
            Source: /Users/irawan/dev/others/bloog
       Destination: /Users/irawan/dev/others/bloog/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
       Jekyll Feed: Generating feed for posts
                    done in 0.465 seconds.
 Auto-regeneration: enabled for '/Users/irawan/dev/others/bloog'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

Where `Server address: http://127.0.0.1:4000/` is your localhost address of your Jeckyll site
