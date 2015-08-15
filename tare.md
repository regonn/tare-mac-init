# App Storeでインストールするソフト
+ xcode
+ karabiner
+ BetterSnapTool
+ sunrise
+ kobito
+ dash

#Appleの command line toolインストール
Xcode起動⇒メニュー⇒Open Developer tool⇒More Developer Tools

#Homebrew(macのライブラリ管理ツール) インストールコマンド

```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

```
$ brew doctor # => Your system is ready to brew. # => これが出れば成功
```

# homebrew cask  

```
$ brew install caskroom/cask/brew-cask
```
```
$ brew cask install google-chrome atom dropbox gimp android-studio cakebrew coteditor libreoffice google-japanese-ime iterm2 karabiner skitch virtualbox visual-studio-code gitter obs postgres gyazo
```

# atomのパッケージ

```
$ apm login
```

```
$ apm stars --install
```

#zshを標準で使う

```
$ chsh -s /bin/zsh
```

#必要なライブラリをbrewでインストール

```
$ brew install rbenv ruby-build rbenv-gemset rbenv-gem-rehash readline imagemagick lua ag pow nvm zsh heroku
```

```
$ brew install vim --with-lua
```

```
$ mkdir -p ~/Library/Application\ Support/Pow/Hosts
```

```
$ ln -s ~/Library/Application\ Support/Pow/Hosts ~/.pow
```

# Githubやheroku用にssh-keygenで公開鍵を作成して、サイトに登録しておく

```
$ ssh-keygen
```

自分用メモなので他の人は無視して可
自分のgithubからdotfileをクローンしてシェルスクリプトを実行すると.zshなどが引き継げる
ただし、Neobundle vimにインストールしないといけないので、dotfiles/.vim/bundleフォルダを作りbundleフォルダ上で

```
$ git clone https://github.com/Shougo/neobundle.vim
```

```
$ git clone https://github.com/Shougo/vimproc.vim.git ~/.vim/bundle/vimproc
```

```
$ cd ~/.vim/bundle/vimproc
```

```
$ make
```

をしてからvim上で:NeoBundleInstallをする

# nvm(Node.js)のバージョン管理ツール

```
$ cd ~
```

```
$ mkdir ~/.nvm
```

```
$ cp $(brew --prefix nvm)/nvm-exec ~/.nvm/
```

```
$ nvm install stable
```

# rbenv（Rubyのバージョン管理ツール）

```
$ rbenv install --list (ここで欲しいrubyのバージョンをメモしておく)
```

```
$ rbenv install <ruby-version>
```

```
$ rbenv global <ruby-version>
```

```
$ rbenv exec gem install bundler powder jekyll jekyll-sitemap cocoapods
```

```
$ rbenv rehash
```

# pg gemのインストールで失敗する場合

```
$ gem install pg -- --with-pg-config=/Applications/Postgres.app/Contents/Versions/9.4/bin/pg_config
```

http://stackoverflow.com/questions/20224483/cannot-install-pg-gem-in-mavericks-with-postgres-app

# 以下参考リンク

[iTerm2 + zsh + tmux + vim で快適な256色ターミナル環境を構築する - ( ꒪⌓꒪) ゆるよろ日記](http://yuroyoro.hatenablog.com/entry/20120211/1328930819)

[mac homebrew と rbenvをインストール](http://qiita.com/issobero/items/e0443b79da117ed48294)
↑ruby-buildを自分でgit clone しちゃうのはマズイかもしれない

[homebrewとrbenv ruby-buildで ruby2.0.0をインストール](http://qiita.com/s-yamaz@github/items/b38b330b44f517f3c77c)

[ruby - Installing libv8 and therubyracer gems on Mavericks (with system v8 installation) - Stack Overflow](http://stackoverflow.com/questions/23536893/installing-libv8-and-therubyracer-gems-on-mavericks-with-system-v8-installation)

[libv8を入れているのに、therubyracerがエラーになる](http://banker0507.blogspot.jp/2012/06/libv8therubyracer.html)

[therubyraver のVer0.10.2だったらこの記事ruby on rails - "gem install therubyracer -v '0.10.2'" on osx mavericks not installing - Stack Overflow](http://stackoverflow.com/questions/19630154/gem-install-therubyracer-v-0-10-2-on-osx-mavericks-not-installing)

[Installing Qt and compiling capybara webkit · thoughtbot/capybara-webkit Wiki](https://github.com/thoughtbot/capybara-webkit/wiki/Installing-Qt-and-compiling-capybara-webkit)

[Homebrewを使ったPostgreSQLのインストール(Mac OS Lion) - Qiita](http://qiita.com/tstomoki/items/0f1a930bd42a8e1fdaac)

[Rails - gem install libv8 に失敗する。 - Qiita](http://qiita.com/s_osa/items/6e563304fcdcf86afcfa)
