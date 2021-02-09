# Install

## Installing on MacOS

### Install Ruby 

Ensure you install Ruby, not the ruby from the Apple default install. It will give you this error:

```
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /Library/Ruby/Gems/2.6.0 directory.
```
Use Homebrew to install latest Ruby. If you haven't had Homebrew installed:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Then install Ruby

```
brew install ruby
```
Add Ruby path on your terminal:

```
# If you're using Zsh
echo 'export PATH="/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/X.X.X/bin:$PATH"' >> ~/.zshrc
# If you're using Bash
echo 'export PATH="/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/X.X.X/bin:$PATH"' >> ~/.bash_profile
# Unsure which shell you are using? Type
echo $SHELL
```
Refresh your shell

```
source ~/.zshrc
# or
source ~/.bash_profile
```
check the path and you shoud see anything other than: `/usr/local/bin/ruby` 
and check the version and it should be the latest:
```
which ruby
'''
Mine would be:
```
/usr/local/opt/ruby/bin/ruby
```
Check ruby version

```
ruby -v
```

### Install Jekyll

Install the Bundler:

```gem install --user-install bundler jekyll
```

### Create a new Jekyll site

Once the Jekyll is installed, you can start creating the site e.g in `/blog` folder:

```
jekyll new blog
```

