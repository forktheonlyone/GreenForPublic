[H2 다운로드 링크](http://www.h2database.com/html/download.html)

![Alt text](<Pasted image 20230922165556-1.png>)

설치되면

![Alt text](<Pasted image 20230922170829-1.png>)
이걸 누르면 아래와 같은 사진이 뜸

or

localhost 포트주소 8082 << 주소창에 입력하면 이렇게 나옴

![Alt text](<Pasted image 20230922170836-1.png>)
( 가장 기본 형태 )
이렇게 뜸

**연결 시험 버튼 누르지 말것**
완벽하지 않아서 누르게 되면 DB를 생성해버림
연결할려고 할때 이미 어디에 연결되어있다고 나와서 접속이 안되는 경우도 있음

![Alt text](<Pasted image 20230922171152-1.png>)
연결 누르면 이런 화면이 뜸

> 만약 안되면 ..
> 바탕화면 -> 메모장 새로 생성 -> 파일명을 **test.mv.db** 로 생성 .txt 삭제

![Alt text](<Pasted image 20230922171935-1.png>)
그리고 여기 있는 주소를 변경해줘야함.

test 파일이 있는 위치를 입력해줘야하는데

> C:\Users\(사용자명)\Desktop

이렇게 경로 설정 해주면 연결 가능할것임

![Alt text](<Pasted image 20230922173512-1.png>)

여기 SQL문 안에는 이제 SQL 영역이다.
잠깐 제껴둘꺼임

---

# 다시 인텔리제이로

![Alt text](<Pasted image 20230922173729-1.png>)

build.gradle 로 가서 `implementation 'com.hedatabase:h2:` 를 치고 뒤에 이렇게 무엇인가 데이터를 쓸 수 있음.

![Alt text](<Pasted image 20230922173833-1.png>)
우선 이렇게 주석 처리 할꺼임.
( 사용하지 않을꺼면 주석 처리 하는게 맞다, 아니면 추후 문제 생길 수 있다. )
`1.4.200` 나오는 메뉴에서 엔터를 치면 **mvstore** 가 나온다 ... 이건 또 뭘까?

![Alt text](<Pasted image 20230922173848-1.png>)
강사님 ver

![Alt text](<Pasted image 20230922174809-1.png>)
그 다음 패키지 만들들것임
패키지의 이름은 **controller**

![Alt text](<Pasted image 20230922175000-1.png>)

그 안에 **UserController** 클래스 생성
![Alt text](<Pasted image 20230922175836-1.png>)
보여지는곳에서 반응하는 창이라고 생각하면됨

![Alt text](<Pasted image 20230922175451-1.png>)

그리고 domain 패키지를 생성하고 User 클래스 생성

![Alt text](<Pasted image 20230922175732-1.png>)
보통 여기선 세터를 사용하지 않고 좀 순수한 상태로 만들어 둬야함.

다음 서비스 패키지 만들고 UserService 클래스 생성

![Alt text](<Pasted image 20230922175847-1.png>)

> 게임을 예시로 ..
> 컨트롤러는 싸울지 말지 슬롯을 했는지를 파악해주는곳
>
> 서비스객층에선 사냥터를 갔으면 사냥터에서 발생할 수 있는 요소들이 여기서 실행
> 이와 같은 경우는 사냥터에서 발생하는 일이니 사냥터 서비스가 있어야됨
>
> 유저는 다른곳에서 사용됨
> 유저 정보.. 등
> 유저에대한 정보를 변경하는 일들만 수행됨

리포지토리의 갯수는 테이블 갯수와 동일하다.
무조건 적이진 않으나 지금 배우는 입장에선 무조건적이라고 생각하자.

![Alt text](<Pasted image 20230922182737-1.png>)

![Alt text](<Pasted image 20230922182745-1.png>)

![Alt text](<Pasted image 20230922182751-1.png>)
