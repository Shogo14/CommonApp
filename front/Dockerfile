FROM node:latest

# 作業ディレクトリの作成、設定
RUN mkdir /front
# 作業ディレクトリ名をAPP_ROOTに割り当てて、以下$APP_ROOTで参照
ENV APP_ROOT /front
WORKDIR $APP_ROOT

# ホスト側（ローカル）のGemfileを追加する（ローカルのGemfileは【３】で作成）
COPY ./package.json $APP_ROOT/package.json
COPY ./package-lock.json $APP_ROOT/package-lock.json

# npm install
RUN npm install

COPY . $APP_ROOT

EXPOSE 3000
# CMD ["npm", "run", "dev"]