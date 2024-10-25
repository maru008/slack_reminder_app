# slackリマインダーコマンド生成アプリ

Slackの締切の日時を基準に，リマインドコマンドを生成するアプリを作りました．

### 動機
何かの締め切りがあった時にSlackのリマンダーを作るかと思うのですが，日時が決まっているものに対して1週間前，2日前など設定したい時があった．
ただ，日時を個別に指定するのが大変なのでそこを自動化してくれるアプリをつくりました．

## 起動
ローカルアプリに変更しました．Dockerを起動して以下のコマンドを実行．

```
docker compose up --build
```

これで，http://127.0.0.1:5002/ にアクセスすると表示されるかと思います．

## 使い方
1. メッセージを入力    
    - slackのリマインダーに送りたいメッセージを書きます．（〇〇の締切など）
    - このとき，channelをメンションするかどうかも決めれます（チェックを入れると冒頭に@channelが入力されます）
2. 締切を入力
    - その締切の日時を入力，時刻も入力します．
3. いつリマインドするかを生成
    - そのリマインダーをいつリマインドさせたいのかを選択します．
4. 生成&コピー
    - 生成ボタンを作るとコマンドが作成されるのでコピーボタンを押してSlackへ投稿します．

## 実際の動作例
順序に従って入力すると以下のように複数のコマンドが生成されます．

<img src="fig/output_ex.png" width="50%">

## 備考
- 環境: Python(Flusk)，html，CSS，Docker
- 何かあればgithub issueでお願いします🙏
