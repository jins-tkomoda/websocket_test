# Websocket samples

JINS MEME のデータをWebsocket serverで受け取るサンプル。

## Node.js

clientの場合はhost/portの個別指定（デフォルトlocalhost:5001）、serverの場合はportの個別指定（デフォルト5001）がコマンドラインで可能

1. `npm i`
2a. `node svr_rec.js --port=5001`
2a. `node svr_rec.js --port=5001`
2b. `node cli_send.js --host=localhost --port=5001`
2c. `node cli_send2.js --host=localhost --port=5001 --csv=csv/run_unit1.csv` CSVを繰り返し送信

## Python

1. https://github.com/Pithikos/python-websocket-server をインストール
2. `python svr_rec.py`

## バリエーション詳細

- cli_send.js: clientから20HzでRTデータ相当（乱数）を送信
- cli_send2.js: clientから20HzでRTデータ相当（CSVから）を送信
- svr_rec.js: serverで受信したデータをそのまま表示
- svr_rec.py: serverで受信したデータをそのまま表示(python)
- svr_rec2.js: 1秒毎に受信数のstatsを表示
- svr_rec3.js: serverで受信したblinkStrength/blinkSpeedを表示
- svr_send.js: clientから20Hzでカウントを送信