# Standout Homebrew Tap

If you would like to use formulas in this repository, start by tapping it.

```bash
brew tap standout/homebrew-tap
```

## Setup x86_64 Homebrew on your Apple Silicon Mac

Some software that we use may only support AMD64 architecture. Therefore if
you use a Mac with Apple Silicon you must also install one version of Homebrew
for x86_64 if you need to use any software here that does not have support for
ARM64.

```bash
softwareupdate --install-rosetta --agree-to-license
arch -x86_64 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
#BREW=arch -x86_64 /usr/local/homebrew/bin/brew
```
Then to use the x86_64 version of brew you should add an alias to ~/.zshrc. Use this command for that.

*If you use bash, change ~/.zshrc to ~/.bashrc*

```bash
echo 'alias axbrew="arch -x86_64 /usr/local/homebrew/bin/brew"' >> ~/.zshrc
```

## Formulas

### Elasticsearch@5.6

Will install Elasticsearch version 5.6 and the plugins analysis-icu and analysis-phonetic.

#### Using AMD64

```bash
brew install elasticsearch@5.6
brew services start elasticsearch@5.6
```

#### Using ARM64 (Apple Silicon)

```bash
axbrew install elasticsearch@5.6
axbrew services start elasticsearch@5.6
```
