FROM    ruby:latest
RUN     curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN     echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN     apt update -y && apt upgrade -y && apt install ruby sqlite3 nodejs yarn -y
RUN gem install rails
