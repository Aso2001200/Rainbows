## DBテーブルカラム詳細一覧
### 購入テーブル(d_purchase)
|和名|属性名|型|PK|NN|FK|
|----|-----|--|--|--|--|
|オーダーID|order_id|bigint(20)|○|○||
|顧客コード|custom_code|varchar(50)||○||
|購入日|today|date||○||
|総額|total_price|int(11)||○||

### 購入テーブル詳細(d_purchase_detail)
|和名|属性名|型|PK|NN|FK|
|----|-----|--|--|--|--|
|オーダー詳細ID|detail_id|bigint(20)|○|○||
|オーダーID|ourder_id|bigint(20)|○|○|○|
|商品コード|item_code|int(11)||○||
|価格|price|int(11)||○||
|巻数|volumenum|int(11)||○||
|数量|num|int(11)||○||


### 顧客テーブル(m_customers)
|和名|属性名|型|PK|NN|FK|
|----|-----|--|--|--|--|
|顧客コード|costom_code|varchar(50)|○|○||
|パスワード|pass|varchar(50)|○|○|○|
|氏名|name|varchar(20)||○||
|生年月日|birthday|date||○||
|住所|address|varchar(100)||○||
|電話番号|tel|varchar(20)||○||
|メールアドレス|mail|varchar(100)||○||
|削除フラグ|del_flag|int(1)||||
|登録日|registerday|date||○||


### カテゴリテーブル(m_category)
|和名|属性名|型|PK|NN|FK|
|----|-----|--|--|--|--|
|カテゴリID|category_id|int(11)|○|○||
|氏名|name|varchar(20)||○||
|登録日|registerday|date||○||


### 商品テーブル(m_items)
|和名|属性名|型|PK|NN|FK|
|----|-----|--|--|--|--|
|商品コード|item_code|int(11)|○|○||
|商品名|item_name|varchar(50)||○||
|価格|price|int(11)||○||
|カテゴリID|category_id|int(11)||○|○|
|画像ファイル名|image|varchar(200)||○||
|商品詳細説明|detail|varchar(500)||||
|削除フラグ|del_flag|int(11)||||
|登録日|registerdate|date||○||

