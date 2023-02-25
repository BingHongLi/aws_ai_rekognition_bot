# 安裝虛擬環境
sudo apt-get install -y python3-venv

# 啟用虛擬環境
python3 -m venv venv
source venv/bin/activate

# 安裝套件
pip3 install -r requirements.txt

# 下載ngrok
wget https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-linux-amd64.tgz

sudo tar xvzf ./ngrok-v3-stable-linux-amd64.tgz -C /usr/local/bin

# 增添token
ngrok config add-authtoken YOUR-TOKEN

# 開發時，設定環境變數

```
export CHANNEL_ACCESS_TOKEN=

export CHANNEL_SECRET=

export AWS_ACCESS_KEY_ID=

export AWS_SECRET_ACCESS_KEY=

export AWS_SESSION_TOKEN=

export AWS_MODEL_ARN=

export CLIENT_BUCKET_NAME=

```

# 啟動對應Port，並將網址貼回Line Messaging api ，開始進行測試
ngrok http 8080

# 確認功能正常後，打包程式碼
gcloud builds submit --tag gcr.io/$GOOGLE_CLOUD_PROJECT/ncu-ai-bot:0.0.5 --region asia-east1

# 部屬到Cloud RUN
必須指定環境變數

CHANNEL_ACCESS_TOKEN=YOUR-LINE-ACCESS-TOKEN

CHANNEL_SECRET=YOUR-LINE-CHANNEL-SECRET

AWS_ACCESS_KEY_ID=STUDENT-ACCOUNT-AWS-ACCESS-KEY-ID

AWS_SECRET_ACCESS_KEY=

AWS_SESSION_TOKEN=

AWS_MODEL_ARN=

CLIENT_BUCKET_NAME=
