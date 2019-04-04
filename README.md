# gcloud-docker-python
dockerでpythonアプリをgaeに上げるための環境

## 概要
docker コンテナのappディレクトリに

ローカルのカレント(docker-compose.ymlのあるディレクトリ)がマウントされます。

### Docker起動
docker-compose.ymlのあるディレクトリをカレントとする

```
docker-compose up -d
```

### gcloud設定
- docker内へ
```
docker-composer exec gcloud bash
```

- gcloud sdk の利用
```
gcloud auth login
gcloud config set project PROJECT_ID
gcloud config list
gcloud app deploy app/app.yaml
```