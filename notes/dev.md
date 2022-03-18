

```sh
sudo apt update
sudo apt install curl git-core zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev software-properties-common libffi-dev

sudo apt install zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

git clone https://github.com/asdf-vm/asdf.git ~/.asdf
cd ~/.asdf
git checkout "$(git describe --abbrev=0 --tags)"

asdf plugin-add ruby https://github.com/asdf-vm/asdf-ruby.git


. $HOME/.asdf/asdf.sh

gem install bundler
git config --global color.ui true
git config --global user.name "YOUR NAME"
git config --global user.email "YOUR@EMAIL.com"
ssh-keygen -t rsa -b 4096 -C "YOUR@EMAIL.com"

cat ~/.ssh/id_rsa.pub

ssh -T git@github.com

gem install rails 


# Setting Up A Database
sudo apt install mysql-client libmysqlclient-dev libpq-dev

sudo apt install mysql-server

sudo apt install postgresql-11

sudo -u postgres createuser khairi -s

# If you would like to set a password for the user, you can do the following
sudo -u postgres psql
postgres=# \password khairi

sudo apt install dirmngr gpg gawk unzip locate autoconf bison re2c libxml2 pkg-config libgd-dev libonig-dev libzip-dev

# https://asdf-vm.com/#/plugins-all?id=plugin-list

asdf plugin add ruby
asdf list-all ruby

asdf plugin add nodejs 
asdf list-all nodejs
asdf install nodejs lts

asdf plugin add erlang
asdf install erlang latest

asdf install elixir
asdf install elixir latest

asdf plugin add crystal
asdf install crystal latest

asdf plugin add redis

asdf plugin add php
asdf install php latest
```
