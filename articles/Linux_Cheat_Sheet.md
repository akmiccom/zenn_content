---
title: Linux のチートシートを作成してみた
emoji: 
type: tech
topics: [python, Linux]
published: False
---

<!-- https://qiita.com/miyamasaru/items/238f6e469982fa76c2e8 -->

# Linux Cheat Sheet
とりあえず簡単なものだけメモとしてまとめてみました。
ヘビーユーザーではないのでこれくらいで十分そうです。

## ファイル操作
| Command |       Despriction        |  Optins  |       Examples        |
| :-----: | :----------------------: | :------: | :-------------------: |
|   ls    | ファイルディレクトリ表示 | -l -a -h |         ls -l         |
|   cd    |   チェンジディレクトリ   |          | cd /path/to/directory |
|   pwd   |  ワークディレクトリ表示  |          |          pwd          |
|  mkdir  |     ディレクトリ作成     |          |     mkdir newdir      |
|   rm    |           削除           |  -r -f   |        rm.txt         |
|   cp    |          コピー          |    -r    |      cp file.txt      |
|   mv    |           移動           |          |  mv file.txt new.txt  |
|  touch  |      新規作成、更新      |          |    touch file.txt     |
|   cat   |         内容表示         |          |     cat file.txt      |
|  head   |      最初の数行表示      |    -n    |  head -n 5 file.txt   |
|  tail   |      最後の数行表示      |    -n    |  tail -n 5 file.txt   |
|  clear  |       履歴のクリア       |          |       Ctrl + l        |


## 使いそうなコマンド

| Command |    Despriction     |          Optins          | Examples |
| :-----: | :----------------: | :----------------------: | :------: |
| histry  |    コマンド履歴    |
|  date   |        日付        |
|   cal   |     カレンダー     |
|  kill   |   プログラム停止   |
| apt-get | アプリインストール | apt-get install app_name |