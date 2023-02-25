# 此為學生體驗用教材

在rekognition建立模型

在rekognition啟用模型

啟動SageMaker Notebook，選用Jupyter notebook


指定教材github

https://github.com/BingHongLi/aws_ai_rekognition_bot


將自己的對話機器人稿件excel上傳至 jupyter


打開aws_temp_app.ipynb，切換到第三個儲存格，將Line的安全參數貼入，並運行


搜尋ngrok 網站，並註冊，取得ngrok憑證


回到Jupyter的管理介面，右上角打開terminal
```
wget https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-linux-amd64.tgz

sudo tar xvzf ./ngrok-v3-stable-linux-amd64.tgz -C /usr/local/bin

ngrok config add-authtoken YOUR-AUTH-TOKEN

ngrok http 5000

```

將得到的網址，貼回Line WebHook



