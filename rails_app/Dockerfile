# イメージの指定
FROM ruby:2.6.5

# rails環境を構築するのに必要なパッケージのインストール
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

# 作成するイメージ内に/var/www/rails_appというディレクトリを作成
RUN mkdir -p /var/www/rails_app
# 作業ディレクトリ（working directory）を/var/www/rails_appに指定
WORKDIR /var/www/rails_app

# ホスト側にあるGemfileを/var/www/rails_app内にコピー
COPY Gemfile Gemfile
# ホスト側にあるGemfile.lockを/var/www/rails_app内にコピー
COPY Gemfile.lock Gemfile.lock

# bundlerというgem(ruby用のライブラリ)をインストール
RUN gem install bundler
# Gemfile(Gemfile.lock)に記述されているgemを一括でインストール
RUN bundle install
