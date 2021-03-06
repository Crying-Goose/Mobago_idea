## 생각하는 화면 정의

### View Screen (전체화면으로 보여줄 친구들)

1. 초기앱 실행화면 (Splash)
2. 초기가이드 (First guide)
3. 로그인 (Login)
4. 회원가입 (Create account)
5. 메인 방 리스트, 캘린더 버튼, 알림 버튼, 프로필 버튼 (Main)
6. 방 - 레이드 그룹 리스트, 위에 공지바, 캘린더 버튼, 방찾기 돋보기 버튼 (Room)
7. 방 찾기 (Room search)
8. 레이드 그룹방, 레이드 날짜 및 클리어 여부 등 정보 (Raid group)
9. 레이드 그룹 생성 / 수정 (Raid group settings)
10. 레이드 그룹 / 전체 캘린더 (raid calendar)
11. 주간 캘린더 (weekly calendar)
12. 알림 (Notifications)
13. 프로필 (User profile)
14. 유저 정보 수정 (User info modify)
15. 설정 (Setting)

*10번과 11번은 전체적으로 보여주는 MainCalendarView 를 만들고, 각각 상세 View를 보여주게끔*


### Modal (작은 알림창 혹은 시스템 얼럿들)

1. 앱 공지
2. 기본적인 추가, 삭제, 수정에 대한 시스템 얼럿
3. 레이드 그룹방장(이하 공대장)의 클리어 여부 체크
4. 공대장의 주간 공지 알림 입력창 (노티의 최대 길이로)
5. 레이드 불참 확인 얼럿


### Screen flow chart

![screen_flow_chart](screen_flow_chart.drawio.png)


### 화면 플로우 Ex

- 앱 실행 -> 로그인(자동로그인) -> 메인 -> 리스트 중 원하는 방 선택 -> 레이드 그룹방 -> 그룹방에 레이드 공지 입력 (그 방에 사람들한테 푸시 알림)
- 앱 실행 -> 초기가이드 -> 회원가입 -> 로그인 -> 메인 -> 방 찾기 -> 방 참여하기
- 앱 실행 -> 로그인(자동로그인) -> 메인 -> 프로필버튼 클릭 -> 프로필 -> 설정버튼 클릭 -> 회원탈퇴 ㅠ
