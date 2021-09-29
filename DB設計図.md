# データベース設計図

## d_purchase

|項目名|型|PK|NN|FK|
|-----|--|--|--|--|
|order-id|bigint(20)|○|○||
|customer-code|varchar(50)||○|○|
|purchase-date|date||○||
|total-price|int(11)||○||

## d_purchase_detail

|項目名|型|PK|NN|FK|
|-----|--|--|--|--|
|detail-id|bigint(20)|○|○||
|order-id|bigint(20) |○|○|○|
|item-code|int(11)||○||
|price|int(11)||○||
|num|int(11)||○||

## m_customers

|項目名|型|PK|NN|FK|
|-----|--|--|--|--|
|customer-code|varchar(50)|○|○||
|pass|varchar(50)||○||
|name|varchar(20)||○||
|address|varchar(100)||○||
|tel|varchar(20)||○||
|mail|varchar(100)||○||
|del-flag|int(1)||||
|reg-date|date||○||

## m_category

|項目名|型|PK|NN|FK|
|-----|--|--|--|--|
|category-id|int(11)|○|○||
|name|varchar(20)||○||
|reg-date|date||○||

## m_items

|項目名|型|PK|NN|FK|
|-----|--|--|--|--|
|item-code|int(11)|○|○||
|item-name|varchar(50)||○||
|price|int(11)||○||
|category-id|int(11)||○|○|
|image|varchar(200)||○||
|detail|varchar(500)||||
|del-flag|int(11)||||
|reg-date|date||○||
