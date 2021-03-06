# Todo

[<img src="https://dply.me/6fwyh1/button/large" alt="Try it on your device via DeployGate">](https://dply.me/6fwyh1#install)


## 機能要件
### Phase 1
- Todoを一覧で表示する
  - 作成日順で表示する(Ormaだとデフォルトで追加順なので特にきにする必要はない)
- Todoの詳細を表示する
- Todoを作成し保存する

### Phase 2
- Todoを削除する
- Todoを更新する

### Phase 3
- Todoの並び順を変更する
  - 作成日の昇順/降順
- お気に入り機能を実装する

## モデル
### Todo
| 項目 | 変数名 | 型 |補足|
|---|---|---|---|
|id|id|long|識別子|
|タイトル|title|String||
|詳細|description|String||
|作成日|createAt|long||
|更新日|updateAt|long||
|お気に入り|isFavorite|boolean|*chapter 3で追加|

### 画面
|一覧|新規作成|照会|
|---|---|---|
|![](Img/list.png)|![](Img/create.png)|![](Img/show.png)|

### 備忘録
#### 実装順（例
- プロジェクト作成
- build.gradleを記載
- packageを作成
    - model
    - presentation
        - list
        - create
        - edit
- model > Todo作成
- list 作成
    - layout
    - adapter
    - activity
          - 画面遷移の処理は作成後に実装
- create
    - layout
    - activity
- show
    - layout
    - activity

#### OSS ライブラリ
- Orma 
    - http://gfx.hatenablog.com/entry/2016/01/25/215003
    - https://github.com/gfx/Android-Orma
```
Copyright (c) 2015 FUJI Goro (gfx).

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
```
