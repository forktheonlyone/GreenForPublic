![1](./Pasted%20image%2020230922161357.png)

![2](./Pasted%20image%2020230922161332.png)

여기에 해당하는 내용들 중

dependencies 디펜던시 제외하고 하지 않음 보지도 말것

```java
dependencies {
    testImplementation platform('org.junit:junit-bom:5.9.1')
    testImplementation 'org.junit.jupiter:junit-jupiter'
}
```

외부에서 불러오는 라이브러리 = 디펜던시
외부라이브러리를 들고온다는게 귀찮고 복잡고 어렵고 짜증남

디펜던시에서 쉽게 불러올 수 있음 = **( 의존성 추가 )**

## 의존성

휴대폰 자바라 거치대와 비슷함
만약 휴대폰 프로젝트라면 자바라 거치대를 의존성으로 추가할 수 있음

SQL할꺼니 DB도 의존성 추가해야됨.
타임리프, JPA JDBC, Security 등 자바 웹개발을 하면서 필요한 애들을 다 디펜던시에 추가할것임.
의존성 추가한다 라는 말과 같음

디펜던시 아래쪽을 많이 쓰고 위쪽으로는 거의 많이 안씀

### 필수사항

**어떤 의존성을 추가하던간에**
뭘 추가 하던지간에 **우측에서 (코끼리모양)Gradle 을 누르고 새로고침**을 해줘야됨

### 롬복

어떤 PC로 가던지 .. ( 생략됨 )

롬복 설치할때는 이렇게 해야됨

```java
dependencies {
    compileOnly 'org.projectlombok:lombok:1.18.22'
    annotationProcessor 'org.projectlombok:lombok:1.18.22'
```

둘 다 써야됨

###### 만약 롬복( Lombok )이 없다면

파일 -> 설정 -> 플러그인 -> 'lom' 만 쳐도 나옴, Install 이 뜨면 설치해야됨

---

# 다시 인텔리제이로

메인을 만들고 Test용으로 Test.class 하나를 만듬.

Test.java

```java
// @Getter 하면 lombok 으로 하나 나올껀데 그거 하면 이렇게 만들어짐
import lombok.Getter;
import lombok.Setter;

public class Test {
    int A;
    int B;
    int C;
    int D;
}
```

자매품으로 Data도 됨, 그럼 다 기능이 됬었던가?

Main.java

```java
Test test = new Test();
test. // .을 하게 되면 get A get B 등등 나오고 Set도 마찬가지로 나온다.
```

---

Test.java

```java
import lombok.Getter;
import lombok.Setter;

@Getter
@Setter
public class Test {
    private int A;
    private int B;
    private int C;
    private int D;
}
```

Main.java

```java
public class Main {
    public static void main(String[] args) {

        Test test = new Test();
        test.
    }
}
```

![4](./Pasted%20image%20230922164422.png)

interface 앞에 @가 찍혀있으면 쓸 수 있는 어노테이션

위와 같은 형태는 기본적인 게터 세터만 만들수 있음.

만약 탐색을 해서 넣는 과정이 필요하다면 우리가 아는 게터 세터 방식으로 만들고 수정해줘야됨.

게터는 안쓸수있다, 반환만 하는 애라.
세터는 요구사항에 따라서 다르게 작성될 수 있으므로 꼭 안쓰기는 어렵다.

> 강사님은..
> @Setter 같은 경우에는 제일 빨리 지워질것같아서 클래스에 제일 멀리두고
> 제일 삭제 안될것같은건 클래스 위에둠.
> 그냥 개인적인 편의적으로 둠

오늘할것은 어노테이션을 익히는 과정 (익숙해지는 과정)

### SQL

H2 DB 라는게 있는데
SQL에서는 좀 신세계임
쉬움

다만 대중적으로 쓰지 않는게 문제
저장소가 안좋아서 잘 안씀

---

# 추후 계획

- DB도 H2DB를 이용한 SQL을 사용할꺼임
- 롬복 사용할꺼임
- 구조적인 부분을 많이 바꿀것임
