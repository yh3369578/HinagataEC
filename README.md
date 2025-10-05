# README

## 初回 環境構築コマンド

### 所有者権限の設定

```
chown -R <your_user>:<your_group> ./
```

### Expo Go のネットワーク指定

1. `./storefront/.env.sample`をコピー。(`./storefront/.env`)
2. `REACT_NATIVE_PACKAGER_HOSTNAME`の値を、ホストマシンの ip アドレスに設定。

### Docker イメージ作成 & 起動

```
docker compose up -d
```

### モジュールのインストール

storefront でインストール。

```
./docker/storefront/login
npm i
```

vendure でインストール。

```
./docker/vendure/login
npm i
```

## 実機接続 (ios,android)

1. 実機で **Expo Go** アプリをインストール、起動
2. **Enter URL manually** に、`exp://<your_host_machine_ip>:8081`を入力 -> **Connect**
