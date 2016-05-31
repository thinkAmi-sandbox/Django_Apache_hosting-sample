# Django_Apache_hosting-sample

## セットアップ
### Djangoアプリ
```
# 任意のGit用ディレクトリへ移動
>cd path\to\dir

# GitHubからカレントディレクトリへclone
path\to\dir>git clone https://github.com/thinkAmi-sandbox/Django_Apache_hosting-sample.git

# virtualenv環境の作成とactivate
# *Python3.5は、`c:\python35-32\`の下にインストール
path\to\dir>virtualenv -p c:\python35-32\python.exe env
path\to\dir>env\Scripts\activate

# requirements.txtよりインストール
(env)path\to\dir>pip install -r requirements.txt
```

　  
### Apache

- `mod_wsgi`をApache2.4のmodulesに入れる
- `httpd.conf`を上書き (もしくは、末尾の2行を既存のものに追記)
- `httpd-vhosts.conf`を上書き

　  
### DNS

- CNAMEレコード`django`を、任意の端末のAレコードに対するものとして、登録

　  
あとは、Apacheを再起動して、`http://django/mysite/` にアクセスし、動作確認

　  
## テスト環境

- Windows7 x64
- Apache 2.4.20 32bit版 (Apache Lounge バイナリ)
- mod_wsgi 4.5.2
- Python 3.5.1 32bit版
- Microsoft Visual C++ 2015 再頒布可能パッケージ 32bit版
- Django 1.9.6


　  
## 関係するブログ

[Windows + Apache2.4 + mod_wsgiにて、virtualenvのDjangoをバーチャルホストで動かす - メモ的な思考的な](http://thinkami.hatenablog.com/entry/2016/06/01/055522)