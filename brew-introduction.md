# Mengenal apa itu homebrew
homebrew adalah package manager yang biasa digunakan pada macos, package manager ini sangat mudah digunakan, 
saya sendiri menggunakan homebrew untuk melakukan instalasi aplikasi seperti netbeans dan juga banyak sdk mulai dari java hingga flutter.

## instalasi
installasi cukup mudah tinggal buka terminal dan jalankan command, jika sudah tinggal ikutin deh step yang di berikan oleh brewnya nanti di terminal.
``` 
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
``

## penggunaan

```
Example usage:
  brew search TEXT|/REGEX/
  brew info [FORMULA|CASK...]
  brew install FORMULA|CASK...
  brew update
  brew upgrade [FORMULA|CASK...]
  brew uninstall FORMULA|CASK...
  brew list [FORMULA|CASK...]

Troubleshooting:
  brew config
  brew doctor
  brew install --verbose --debug FORMULA|CASK

Contributing:
  brew create URL [--no-fetch]
  brew edit [FORMULA|CASK...]

Further help:
  brew commands
  brew help [COMMAND]
  man brew
  https://docs.brew.sh
 ```
