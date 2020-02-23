# Avoiding Conflicting Dependancies, macOS Python Development with pyenv


By default, macOS includes python 2.7. This version of Python reached EOL January 2020, and is not recommended for use. When working on multiple projects, you may stat to notice that your projects may (probably will) have conflicting dependancies. One of those could be python itself, particularly the default installation.

A great solution to this problem is `pyenv`, from the support documentation


> pyenv lets you easily switch between multiple versions of Python. It’s simple, unobtrusive, and follows the UNIX tradition of single-purpose tools that do one thing well.

For more information on `pyenv` see (https://github.com/pyenv/pyenv)


It's quite easy to get `pyenv` set up on your Mac.


### Install Homebrew if it isn't already available
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
### Update Homebrew
```
brew update && brew upgrade
```
### Install pyenv
```
brew install pyenv
```

### Add pyenv to your shell config, your's may be ~/.zshrc
```
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bashrc
```
### Add pyenv initializer to shell startup script
```
echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
```
### Reload your profile
```
"source ~/.bash_profile"
```
### Reset the current shell
```
Exec $O
```
### Check which version of python
```
which python
```
### You should get
```
/Users/<user>/.pyenv/shims/python
```
### If you need to install a specific version of python
```
pyenv install <version>
```
 Ex.

```
pyenv install 3.8.1
```
### set specific version as global default version for pyenv environments
```
pyenv global <version>
```
Ex.

```
pyenv global 3.8.1
```
