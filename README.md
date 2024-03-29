# AndroidMemoApp

## 개발 순서
1. 필요한 Activity 및 레이아웃 파악
2. 기능 정리 
3. 제공된 디자인에 맞게 레이아웃 구성
4. 기능 구현

---
### 1. 필요 Activity 및 layout 파악    

---

### Actvitiy

#### MainActivity
- 메인 화면으로 데이터를 받아와 RecyclerView에 띄우는 역할

#### MakeMemoActivity
- 메모 작성 액티비티

#### ShowMemoActivity
- RecyclerView에서 선택한 메모를 상세하게 보여주는 액티비티

#### ModifyMemoActivity
- 입력된 메모에 대해 수정하는 액티비티

---
### Layout

#### 각 Activity에 대한 레이아웃    
- 각 Acitivty에 맞게 레이아웃 구성

#### row_main.xml
- MainActivity의 RecyclerView에 대한 한 칸 xml

#### menu_main.xml
- MainActivity의 툴바 메뉴

#### menu_make_memo
- MakeMemoActivity에 대한 툴바 메뉴

#### menu_show_memo
- ShowMemoActivity에 대한 툴바 메뉴

#### menu_modify_memo
- ModifyMemoActivity에 대한 툴바 메뉴

---

### 추가 Class
#### Memo (Data Class)
- 메모에 필요한 내용을 담을 클래스
---

### 2. 기능 정리 

---
### Actvitiy

---

#### MainActivity

- RecyclerView 기능
  - 데이터 띄우기
  - 클릭 시 ShowMemoActivity로 전환 및 데이터 전달
- Toolbar 기능
  - 툴바의 상단 기능 클릭 시 MakeMemoActivity로 전환
  - MakeMemoActivity에서 데이터 가져오기


#### MakeMemoActivity
- 사용자로부터 제목, 내용 입력 받고 날짜는 시스템 날짜 받기
  - 내용은 여러줄 입력 가능하게 설정한다.
- 툴바 기능
  - 체크 표시 클릭 시 제목, 내용, 날짜 데이터를 MainActivity로 전달
    - 입력에 대한 예외 처리 주의
  - 백버튼 구현

#### ShowMemoActivity
- MainActivity로부터 받은 제목, 작성 날짜, 내용 데이터를 출력하기
- 툴바 기능
  - 수정 (아이콘 o)
    - ModifyMemoActivity로 제목, 작성 날짜, 내용 데이터를 전달
  - 삭제 (아이콘 o)
    - 데이터를 삭제하고 MainActivity로 전환
  - 백버튼 구현

#### ModifyMemoActivity
- 수정 전의 내용을 TextField에 띄운다.
- 툴바 기능
  - 체크 버튼 클릭 시 ShowMemoActivity로 전환하고 수정된 데이터를 전달한다.
  - 백버튼 구현

---

### 3. 제공된 디자인에 맞게 레이아웃 구성

---

- [x] MainActivity

- [x] MakeMemoActivity

- [x] ShowMemoActivity

- [x] ModifyMemoActivity

- [x] row_main.xml

- [x] menu_main.xml

- [x] menu_make_memo

- [x] menu_show_memo

- [x] menu_modify_memo

---

### 4. 기능 구현

---

- [x] MainActivity
  - [x] RecyclerView 기능
    - [x] 데이터 띄우기
    - [x] 클릭 시 ShowMemoActivity로 전환 및 데이터 전달
  - [x] Toolbar 기능
    - [x] 툴바의 상단 기능 클릭 시 MakeMemoActivity로 전환
    - [x] MakeMemoActivity에서 데이터 가져오기


- [x] MakeMemoActivity
  - [x] 사용자로부터 제목, 내용 입력 받고 날짜는 시스템 날짜 받기
    - [x] 내용은 여러줄 입력 가능하게 설정한다.
  - [x] 툴바 기능
    - [x] 체크 표시 클릭 시 제목, 내용, 날짜 데이터를 MainActivity로 전달
      - [x] 입력에 대한 예외 처리 주의
    - [x] 백버튼 구현

- [x] ShowMemoActivity
  - [x] MainActivity로부터 받은 제목, 작성 날짜, 내용 데이터를 출력하기
  - [x] 툴바 기능
    - [x] 수정 (아이콘 o)
      - [x] ModifyMemoActivity로 제목, 작성 날짜, 내용 데이터를 전달
    - [x] 삭제 (아이콘 o)
      - [x] 데이터를 삭제하고 MainActivity로 전환
    - [x] 백버튼 구현

- [x] ModifyMemoActivity
  - [x] 수정 전의 내용을 TextField에 띄운다.
  - [x] 툴바 기능
    - [x] 체크 버튼 클릭 시 ShowMemoActivity로 전환하고 수정된 데이터를 전달한다.
    - [x] 백버튼 구현

- [x] Memo (data class)
  - [x] 제목, 내용, 날짜


---
### 감점 요인
---

- [x] 오류 발생 때문에 실행이 안되거나 중간에 튕기는 경우 : -70점
- [x] 구현되지 않는 기능이 있을 경우 : 기능 하나당 -10점. 최대 감점 -70점
- [x] 슬라이드 3번의 화면의 툴바에 아이콘을 적용하지 않는 경우 : 아이콘 하나당 -5점
- [x] 입력 요소에 대해 입력된 것이 없을 경우에 대한 처리를 하지 않는 경우 : 입력요소 하나당 -5점
- [x] 화면 네비게이션이 정상적이지 않을 경우 : 하나당 -5점
- [x] 현재 날짜를 구해서 적용하지 않았을 경우 : -5점
- [x] 기타 사유 : -5점