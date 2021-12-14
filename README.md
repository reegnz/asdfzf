# asdfzf

[asdf](https://github.com/asdf-vm/asdf) + [fzf](https://github.com/junegunn/fzf) = asdfzf!

## Installation

Put the script on your path, eg.:

```sh
mkdir -p ~/bin
cd ~/bin
wget https://raw.githubusercontent.com/reegnz/asdfzf/master/asdfzf
chmod +x asdfzf
```

## Usage

The asdfzf command hides asdf commands behind an fzf interactive selection interface.

There are no arguments. Just run `asdfzf` and that's it!

### Custom version filters per tool

You can influence versions that display during install.

Precedence of environment variables is:
* ASDFZF_VERSION_FILTER_COMMAND_pluginname
* ASDFZF_VERSION_KEEP_pluginname
* ASDFZF_VERSION_FILTER_COMMAND
* ASDFZF_VERSION_KEEP

#### ASDFZF_VERSION_KEEP

`ASDFZF_VERSION_KEEP=semver-no-prerelease` will keep versions that are
not semver prerelease versions.

`ASDFZF_VERSION_KEEP_kubectl=semver-only-prerelease` will only show semver
prerelease versions

#### ASDFZF_VERSION_KEEP_pluginname

Same as `ASDFZF_VERSION_KEEP` but limited to a given plugin only.

#### ASDFZF_VERSION_FILTER_COMMAND

Allows for providing a custom shell command to filter the version strings.

#### ASDFZF_VERSION_FILTER_COMMAND_pluginname

Same as `ASDFZF_VERSION_FILTER_COMMAND` but limited to a given plugin only.
