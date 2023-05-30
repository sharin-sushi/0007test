#Dockerのメリット
#誰でも同じ開発環境をすぐに利用することができる
#フレームワークなどのパッケージをローカルにインストールする必要がないF
#↓起動した人皆を同じ開発環境にしてくれる？

FROM golang:1.17.7-alpine
 #alpine Linuxの機能を制限？→ものによってはcdも使えなくなる可能性

RUN apk update && apk add git
RUN go get github.com/cosmtrek/air@v1.29.0
RUN mkdir -p /go/app
 #runで実行するコマンドを記述

WORKDIR /go/app
 #操作するディレクトリの絶対パスを指定
 #以降はこのディレクトリを基準にDockerfileに書いた操作が実行される
 #......go/appってどこ？　　　？　　？　　？

CMD ["air", "-c", ".air.toml"]
 ## CMD ["実行コマンド", "オプション1", "オプション2"...]

#docker cmdとかで調べると分かるかも
#Airは転職で加点にならないかも。かといって、RUN go get...airだけ消したらエラーなる
#CMD丸っと消す？