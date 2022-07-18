DB is **nosql** or **coreData(Sqlite)**

## Room
- index (primary key)
- ruid
- name
- game_type
- reg_date


## Raid schedule
- index (primary key)
- ruid (foreign key)
- game_type (foreign key)
- rsuid
- name
- weekdays
- raid_type
- reg_date
- noti_date


## Raid schedule users
- index (primary key)
- rsuid (foreign key)
- noti_date (foreign key)
- uuid (foreign key)
- room_reg_date


## User
- uuid (primary key)
- nickname
- social_type
- reg_date


## User games
- index (primary key)
- uuid (foreign key)
- game_type
- name
- level
- classes



*추후 다른 게임이 추가된다고 가정하에 nosql을 사용하여 class별로 값을 가져오는것이 현명하긴 함.*
*만약에 nosql로 간다면 index를 빼도 됨 (document 방식으로)*
