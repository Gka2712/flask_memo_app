# ベースイメージとしてPythonを使用
FROM python:3.12

# 作業ディレクトリを指定
WORKDIR /app

# 必要なパッケージをインストール
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# アプリケーションコードをコンテナ内にコピー
COPY . .

# アプリケーションを起動
CMD ["waitress-serve","--host=0.0.0.0","--port=5000","app:app"]
