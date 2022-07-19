DB is **nosql** or **coreData(Sqlite)**

## Room
>레이드 그룹을 포함하는 집단의 방(이하 길드)

|필드명|데이터 타입|설명|
|---|:---:|---|
|index|Int (primary key)|방 인덱스|
|ruid|String|방의 범용 고유 식별자|
|name|String|방 제목|
|game_type|String|방의 게임 타입 (프로토 타입에선 사용되지 않음)|
|reg_date|Date|방 생성날짜|

## Room user
>길드 안의 유저

|필드명|데이터 타입|설명|
|---|:---:|---|
|index|Int (primary key)|길드안에 유저 인덱스(삭제할 수 있으면 그냥 삭제)|
|ruid|String (foreign key)|Room 테이블의 ruid|
|uuid|String (foreign key)|User 테이블의 uuid|
|room_reg_date|Date|길드에 들어온 날짜|


## Raid group
>길드 안에 레이드 그룹

|필드명|데이터 타입|설명|
|---|:---:|---|
|index|Int (primary key)|레이드 그룹 인덱스|
|ruid|String (foreign key)|Room 테이블의 ruid|
|game_type|String (foreign key)|방의 게임 타입 (프로토 타입에선 사용되지 않음)|
|guid|String|레이드 그룹의 범용 고유 식별자|
|name|String|레이드 그룹의 이름|
|weekdays|String|레이드 요일(수정가능성 있음)|
|raid_type|String|그룹의 레이드 종류|
|reg_date|Date|그룹 생성날짜|
|noti_date|Date|그룹 알림일정(수정가능성 있음)|


## Raid group user
>레이드 그룹 안에 유저

|필드명|데이터 타입|설명|
|---|:---:|---|
|index|Int (primary key)|그륩안에 유저 인덱스(삭제할 수 있으면 그냥 삭제)|
|guid|String (foreign key)|Raid group 테이블의 guid|
|uuid|String (foreign key)|User 테이블의 uui)|
|group_reg_date|Date|레이드 그룹에 들어온 날짜|


## User
>유저

|필드명|데이터 타입|설명|
|---|:---:|---|
|uuid|String (primary key)|유저의 범용 고유 식별자|
|nickname|String|유저 닉네임|
|social_type|Int|가입한 소셜 타입|
|reg_date|Date|회원가입한 날짜|


## ~~User games~~
>유저의 게임 (지금은 로스트아크만 하기때문에 클래스만 추가)

- index (primary key)
- uuid (foreign key)
- game_type
- name
- level
- classes



*추후 다른 게임이 추가된다고 가정하에 nosql을 사용하여 class별로 값을 가져오는것이 현명하긴 함.*
*만약에 nosql로 간다면 index를 빼도 됨 (document 방식으로)*
