# blogApp

## B/S フレームワーク

# 利用技術

* JSP
* Servlet
* Jquery
* log4j
* Junit

# dataBase

## tb_user

| column        | type    | option       |
|---------------|---------|--------------|
| user_id       | int     | primary key  |
| user_name     | varchar | null: false  |
| user_password |varchar| null: false  |
| nick          |varchar| null: false,UNIQUE  |
| head          |varchar| null: false |
| mood          |varchar| null: false |

### association

* has_many :tb_note_type

## tb_note
| column   | type    | option       |
|----------|---------|--------------|
| note_id  | int     | primary key  |
| title    | varchar | null: false  |
| content  | varchar | null: false  |
| type_id  | references | foreign_key: true  |
| pub_time | varchar | null: false |
| lon      | float   | null: false |
| lat      | float   | null: false |


## tb_note_type
| column    | type    | option            |
|-----------|---------|-------------------|
| type_id   | int     | primary key       |
| type_name | varchar | null: false       |
| user_id   | references     | foreign_key: true |
### association

* has_many :tb_note
