<!-- 작성자 소개 -->
### 🎁 작성자 Profile
> - [작성자의 Velog Blog](https://velog.io/@kim-src/series)
> - [작성자의 LinkedIn Profile](https://www.linkedin.com/in/chang-seong-kim-7826142a0/)

<!-- 글 시작 -->
<!-- Update Date -->
<!-- Title -->
<!-- Contents -->

<!-- Update Date -->
#### <p align="right">Date : January 17, 2024</p>

<!-- Title -->
# 🚀 Book Rental Service (BRS) PJT

<br/>

<!-- Contents -->
### 📌 웹 개발 프로젝트

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 16, 2024</p>

<!-- Title -->
# ✅ Spring

<br/>

<!-- Contents -->

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 15, 2024</p>

<!-- Title -->
# ✅ Spring

<br/>

<!-- Contents -->
### 🔔 STS 3 (Spring Tool Suite 3) 구동 테스트
### 📌 STS 환경에서 Tomcat 활용 과정(오류의 연속)
> ☠️ "No mapping found for HTTP"는 무엇을 의미할지..
>> - 메인 메서드 관련 ```@RequestMapping("/hello")``` 모듈 import 문장 미기입
>> - ```import org.springframework.web.bind.annotation.RequestMapping;``` 으로 해결
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/6e798369-4d5b-4931-87de-eb9a10183dec" width="500px"></p>

<br/>

> ☠️ 이번에는 500 코드를 리턴하는 Tomcat..
>> - 문제를 찾지 못했기에 java class 삭제 후 다시 생성
>> - 그럼에도 문제 발생 시 STS 등 초기화 후 재시도까지 사료
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/f096f516-bb09-4d77-bf30-b7a7496bd6b4" width="500px"></p>

<br/>

> 🚀 드디어 STS 환경에서 Tomcat 실행 성공
>> - Search 버튼 클릭 및 JDK 버전 검색 후 JDK 11로 변경
>> - Preferences → Java → Installed JREs → Add C:\jdk11
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/41fc47ca-0f38-4286-a751-6c693d295668" width="500px"></p>

<br/>

> ☠️ 영문 모를 이유로 404 코드만 리턴하는 Tomcat..
>> - Tomcat은 정상적으로 실행되었지만 System.out으로 인한 404 코드 반환
>> - STS 콘솔창에 "Hello" 출력된 것 확인
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/630eda1d-631b-4baf-8686-8799128810e6" width="500px"></p>

<br/>

> 🚀 STS 콘솔창에 "Hello" 출력 성공
>> - Tomcat 내부에서 객체 생성
>> - Instance Method임에도 Method 호출
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/27917b95-44b5-4b1a-bbdf-a144d50e9d43" width="500px"></p>

<br/>

### 🎁 References
> - FastCampus의 남궁성 강사님 강의

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 14, 2024</p>

<!-- Title -->
# ✅ Spring

<br/>

<!-- Contents -->
### 🔔 HTTP 특징
### 📌 ㅇㅇ

<br/>

### 🎁 References
> - FastCampus 남궁성 강사님 강의

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 13, 2024</p>

<!-- Title -->
# ✅ Spring

<br/>

<!-- Contents -->
### 🔔 Spring Legacy Project 생성 오류
> - STS 3에서 새로운 Spring MVC Project 생성을 시도하였음
> - 프로젝트명 입력 후 Next 버튼을 클릭
> - 그런데 아래와 같은 오류가 발생하였음
``` 
An error has occurred. See error log for more details.
java.lang.ExceptionInInitializerError
```
> - 오류를 무시하고 넘어갈 수 없으며 다른 오류도 발생됨

<br/>

### 🎯 Spring Legacy Project 생성 오류 해결 과정 (1/3)
### 🔑 Java JDK 호환 문제 해결
> - 오류의 원인은 STS 3와 Java JDK 버전의 호환 문제로 예상됨
> - 최신 java.lang package 관련 오류 내용으로 해석되었기 때문임
> - STS3와 호환성이 좋은 Java JDK는 JDK 11 버전임
> - [JDK 11 다운로드 사이트는 이 문장을 클릭하면 로드됨](https://jdk.java.net/java-se-ri/11-MR2)
> - 이곳 또는 비슷한 사이트에서 JDK 11을 다운로드 해야됨
> - 참고로 작성자의 개발 환경은 Window 11 x64임

<br/>

### 🎯 Spring Legacy Project 생성 오류 해결 과정 (2/3)
### 🔑 시스템 환경 변수 편집
> - 다운로드 받은 JDK 11 zip 파일을 압축 해제
> - 압축 해제된 폴더를 C 드라이브로 이동
> - 이동시킨 후 (제어판 → 시스템 속성 → ) 환경 변수 버튼 클릭
>> 1. 새로 만들기 → 이름에 JAVA_HOME 입력 → 값에 C:\jdk11 입력
>>> - "C:\jdk11"은 C 드라이브의 JDK 폴더 주소임
>> 2. 기존의 Path 클릭 → 편집 클릭 → 새로 만들기 클릭 → C:\jdk11\bin 입력
>>> - "C:\jdk11\bin"은 JDK 11 폴더의 bin 폴더 주소임
>>> - 기존 시스템 변수 중 Path 변수를 편집하는 과정임
>>> - 입력한 JDK Path의 위치는 최상단으로 위치시켜야 됨
>> 3. 모든 환경 변수 설정을 완료 후 확인 클릭
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/e7551df5-4a94-4323-b763-8120670489aa" width="500px"></p>

<br/>

### 🎯 Spring Legacy Project 생성 오류 해결 과정 (3/3)
### 🔑 오류 해결 결과 검토
> - STS 3 실행
> - File → New → Spring Legacy Project 클릭
> - Spring MVC Project → Next
> - Package 구조 입력 페이지로 넘어가면 오류 해결 완료
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/7052a5ab-3a9b-499c-8c26-dba67bc10f45" width="500px"></p>

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 12, 2024</p>

<!-- Title -->
# ✅ Spring

<br/>

<!-- Contents -->
### 🔔 Tomcat 페이지 로드 오류
> - Tomcat 페이지 로드를 위해 Chrome 주소창에 localhost:8080을 입력함
> - 그런데 "사이트에 연결할 수 없음"이라는 오류 페이지만 로드됨
> - 오류의 원인은 Tomcat 관련 cmd 명령어 창을 종료시켰기 때문임
> - Tomcat 종료 방법 중 하나가 cmd 명령어 창을 종료시키는 것임

<br/>

### 🎯 Tomcat 페이지 로드 오류 해결
> - Tomcat 9 페이지를 로드시키기 위해서 cmd 명령어 창 실행
> - 실행창 실행(Win + R) → 명령어 창 실행(cmd 입력)
> - cmd에 아래와 같이 "cd + Tomcat 설치 위치" 입력 후 Enter
``` cmd
cd C:\apache-tomcat-9.0.85\bin
```
> - 이후 cmd에 Tomcat 실행 명령어 입력 후 Enter
``` cmd
startup
```
> - Tomcat 관련 cmd 명령어 창 최소화 버튼 클릭
> - Chrome 주소창에 https://localhost:8080 입력
> - 아래와 같 정상적인 Tomcat 페이지 로드 확인
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/163ce9cd-34cf-4231-a0fd-6fcdbc966dec" width="500px"></p>

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 11, 2024</p>

<!-- Title -->
# ✅ Spring

<br/>

<!-- Contents -->
### 🔔 Spring으로 개발하기 위해 필요한 도구들
> - 통합 개발 환경(IDE; Integrated Development Environment)
>> - STS : Spring Tool Suite
>> - IntelliJ : Java, Spring, Spring Boot 등 개발 가능
> - Java 개발 도구 : JDK (Java Development Kit)
> - Web Server : Tomcat
> - Web Browser : Chrome
> - DBMS (DataBase Management System)
>> - MySQL (Structured Query Language)
> - VS Code : Visual Studio Code
> - Git : 버전 관리용 툴
> - AWS : Amazon Web Services
> - Apache Maven : HTTP Server 관련 툴
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/fbfec5ba-5e5b-4545-987a-361fd2808619" width="500px"></p>

<br/>

### 🎁 References
> - FastCampus 남궁성 강사님 강의

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 10, 2024</p>

<!-- Title -->
# ✅ Java

<br/>

<!-- Contents -->
### 🔔 잘 설계된 VO 클래스
### 📌 IntelliJ에서의 Java class 설계 순서
> 1. class에 상태 정보(권한 : private) 입력
> 2. class에 생성자 메서드(constructor method) 입력
> 3. 마우스 우클릭 후 Generate 클릭
> 4. Generate 메뉴에서 Constructor 선택 후 오버로딩
> 5. Generate 메뉴에서 Getter and Setter 선택 후 OK 클릭
> 6. Generate 메뉴에서 toString() 선택 후 OK 클릭
> 7. main class 설계 및 인스턴스 변수 생성 후 검토

<br/>

### 🚀 잘 설계된 MovieVO 클래스 설계(1 ~ 6단계)
``` Java

package kim.java.model;

public class MovieVO {

    private String title;
    private int date;
    private String starring;
    private String type;
    private int running_time;
    private int level;

    public MovieVO() {}

    public MovieVO(String title, int date, String starring, String type, int running_time, int level) {
        this.title = title;
        this.date = date;
        this.starring = starring;
        this.type = type;
        this.running_time = running_time;
        this.level = level;
    }

    public String getTitle() {
        return title;
    }

    public void setTitle(String title) {
        this.title = title;
    }

    public int getDate() {
        return date;
    }

    public void setDate(int date) {
        this.date = date;
    }

    public String getHero() {
        return starring;
    }

    public void setHero(String hero) {
        this.starring = hero;
    }

    public String getType() {
        return type;
    }

    public void setType(String type) {
        this.type = type;
    }

    public int getRunning_time() {
        return running_time;
    }

    public void setRunning_time(int running_time) {
        this.running_time = running_time;
    }

    public int getLevel() {
        return level;
    }

    public void setLevel(int level) {
        this.level = level;
    }

    @Override
    public String toString() {
        return "MovieVO{" +
                "title='" + title + '\'' +
                ", date=" + date +
                ", starring='" + starring + '\'' +
                ", type='" + type + '\'' +
                ", running_time=" + running_time +
                ", level=" + level +
                '}';
    }
}

```

<br/>

### 🚀 잘 설계된 MovieVO 클래스 검토(7단계)
``` Java

package kim.java.part3;
import kim.java.model.MovieVO;

public class BestVOModeling {
    public static void main(String[] args) {

        MovieVO vo = new MovieVO("Avatar: The Way of Water", 20221214, "Sam Worthington", "Action", 192, 12);
        System.out.print(vo);

    }
}

```

<br/>

### 📌 JVM 이해
> - JVM : Java Virtual Machine
> - 4가지의 메모리 공간
>> 1. Method Area
>> 2. Heap Area
>> 3. Stack Area
>> 4. Literal Pool

<br/>

### 📌 Static 이해
> - static 있으면 class method
> - static 없으면 instance method
> - static 있으면 기울임체로 자동 표기
> - 어느 class로부터 사용할 메서드에는 전부 static 입력
> - class에 static 있으면 생성자 메서드 권한을 private으로 설정

<br/>

### 📌 생성자 메서드 권한 : private
> - Java에 기본적으로 설계된 System, Math 메서드 등이 예시임
> - 별도의 new 생성자 메서드 없이 바로 사용할 수 있는 메서드이기 때문임
> - System, Math 변수 등에 .(연결)을 입력하면 설계된 변수들이 표시됨

<br/>

### 📌 강의 내용 요약 : 배열과 클래스의 관계
#### Q1. 동일한 기억공간을 메모리에 연속적인 구조로 만들어서 사용하는 자료 구조를 무엇이라고 합니까?
> - Array

#### Q2. 현실 세계의 객체는 이질적인 구조로 표현되는데 객체지향 프로그래밍에서의 이질적인 구조를 설계하는 도구는 무엇입니까?
> - Class

#### Q3. 배열과 클래스의 공통점으로 Java에서 배열과 클래스를 무엇이라고 취급합니까?
> - Object

#### Q4. 배열과 클래스로 객체를 생성할 때 공통적으로 사용되는 연산자는 무엇입니까?
> - new

#### Q5. 영화 데이터 5편을 저장할 수 있는 객체 배열은 무엇입니까?
> - MovieVO[ ] mv = new MovieVO[5];

<br/>

### 📌 강의 내용 요약 : Static 및 JVM 메모리 모델 이해
#### Q1. 클래스를 사용하는 시점에서 단 한 번 메모리에 로딩하기 위해 사용하는 키워드는 무엇입니까?
> - Static

#### Q2. 아래 설명하는 메모리가 어떤 JVM 메모리입니까?
> 1. 메서드가 호출되면 호출된 기계어 코드가 push 되고 실행되는 메모리 공간
> 2. 현재 프로그램이 실행되고 있는 상태를 파악할 수 있는 메모리 공간
> 3. LIFO (Last-In-First-Out) 구조의 메모리 공간
>> - Call Stack Frame Area / Stack Area / Stack Memory

#### Q3. 객체 생성을 막는 방법은 무엇입니까?
> - 생성자 메서드의 권한을 private으로 변경

#### Q4. JVM의 메모리 공간 4가지는 무엇입니까?
> 1. Method Area
> 2. Heap Area
> 3. Stack Area
> 4. Literal Pool

<br/>

### 🎁 References
> - FastCampus 박매일 강사님 강의

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 9, 2024</p>

<!-- Title -->
# ✅ Java

<br/>

<!-- Contents -->
### 🔔 Setter & Getter Methods
> - Java에서 class의 상태정보 권한은 일반적으로 private 상태로 설계됨
> - 따라서 데이터를 저장할 때 public 상태의 setter method를 사용해야 class가 활용됨
> - 저장된 데이터는 public 상태의 getter method를 사용해야 추출 또는 출력됨
> - 한편 생성자 method를 이용하여 해당 class의 초기 상태 정보를 설계할 수 있음

<br/>

### 🔔 Differences between Class & Array
### 📌 Difference 1
> - class는 여러 종류의 데이터 자료형으로 구성된 이질적인 구조의 데이터 객체(object)임
> - array는 한 종류의 데이터 자료형으로 구성된 동일한 구조의 데이터 객체(object)임
### 📌 Difference 2
> - class의 경우 설계(모델링)로 데이터를 구조화 함
> - array의 경우 java에서 제공하는 기본 문법인 대괄호 [ ]를 사용하여 데이터를 구조화 함
### 📌 Difference 3
> - class가 여러개 모이면 "객체 배열"이라고 표현할 수 있음
> - array는 같은 종류의 자료형 데이터가 여러개 모인 "기본 배열"이라고 표현할 수 있음

<br/>

### 🔔 잘 설계된 VO 클래스
### 📌 Java의 데이터 모델은 크게 세 가지로 구분된다.
1. VO : Value Object, DTO : Data Transfer Object
2. DAO : Data Access Object
3. Utility : VO, DTO, DAO가 아닌 모델이며 정식 명칭은 없음
### 📌 각 데이터 모델에 대한 한 줄 설명은 아래와 같다.
1. VO 및 DTO : 데이터를 일괄적으로 이동시킬 때 사용됨
2. DAO : 데이터를 DB와 연결시킬 때 사용됨
3. Utility : 한국어 사용을 위한 UTF-8 등을 설정하는 등 보조 역할임
### 📌 이때 잘 설계된 VO 및 DTO 모델을 설계하는 방법은 아래와 같다.
### 1. 입력
> - 기본 생성자 메서드에 오버로딩하면 각 데이터의 자료형이 자동으로 입력됨
> - public 변수명() 괄호 안에 자료형 및 변수명을 순서대로 입력하여 설계하면 됨
### 2. 출력
> - toString() 메서드를 사용하면 모든 데이터를 가장 간편하게 출력할 수 있음
> - 심지어 System.out.println(변수명);에서 toString()을 생략해도 정상 출력됨

<br/>

### 🚀 잘 설계된 Java VO 클래스 예시
``` Java

package kim.java.model;

public class PersonVO {

    private String name;
    private int age;
    private String phone;


    // Constructor Method : 기본 생성자 메서드
    // 오버로딩 하려면 기본 생성자 메서드가 있어야 될듯함
    public PersonVO() {
        this.name = "Hong";
        this.age = 30;
        this.phone = "010-1234-1234";
    }


    // 생성자 메서드의 오버로딩 예시
    // PsersonVO() 괄호 안에 값 입력하면 자료형이 자동으로 기입됨
    public PersonVO(String name, int age, String phone) {
        this.name = name;
        this.age = age;
        this.phone = phone;
    }


    // Setter Method
    public void setName(String name) {
        this.name = name;
    }
    public void setAge(int age) {
        this.age = age;
    }
    public void setPhone(String phone) {
        this.phone = phone;
    }


    // Getter Method
    public String getName() {
        return this.name;
    }
    public int getAge() {
        return this.age;
    }
    public String getPhone() {
        return this.phone;
    }


    // 간편 출력용 toString Method
    public String toString(){
        return name + "\t" + age + "\t" + phone;
    }
}

```

<br/>

### 🎁 잘 설계된 Java VO 클래스 설명
<p align="center"><img src="https://github.com/Kim-src/Diary/assets/150884526/c89d036e-885e-4b77-b161-2d838bd656e4" width="500px"></p>

<br/>

### 📌 강의 내용 요약 : 잘 설계된 VO 클래스(객체)
#### Q1. 다른 객체에서 자신의 정보를 숨기고 클래스 외부에서 특정 정보에 대한 접근을 막는다는 것을 무엇이라고 합니까?
> - Information Hiding

#### Q2. 은닉된 정보에 접근하는 방법 중 값을 저장하는 메서드를 무엇이라고 합니까?
> - Setter Method

#### Q3. 은닉된 정보에 접근하는 방법 중 값을 얻어오는 메서드를 무엇이라고 합니까?
> - Getter Method

#### Q4. 은닉된 정보에 접근하는 ㅂ아법 중 객체 초기화를 통해 접근하는 메서드를 무엇이라고 합니까?
> - Constructor Method

#### Q5. 객체가 가지고 있는 값 전체를 문자열 형태로 넘겨주기 위한 메서드를 무엇이라고 합니까?
> - toString()

<br/>

### 🎁 References
> - FastCampus 박매일 강사님 강의

<br/>

***

<br/>
<br/>
<br/>

<!-- Title -->
# ✅ Python

<br/>

### 📌 Parsing
> - 파싱(parsing)은 구문 분석이라는 의미로 토큰으로 분석할 수 있음
> - 토큰(token)은 구문의 최소 단위인 단어를 의미함
> - 토큰으로 분석한 문법 구조로 파스트리(parse tree)를 생성할 수 있음
> - Parsing 관련 추가적인 학습 필요

<br/>

***

<br/>
<br/>
<br/>

<!-- Title -->
# 🚀 CDM Project

<br/>

<!-- Contents -->
### 🔔 Project Progress
> - 2023-12-15 Cavity Detection Model (CDM) PJT 시작
> - 2024-01-09 CDM에 첫 이미지 학습 완료
> - 추후 이미지 학습 과정에 대한 검토 진행 예정

<br/>

### 🎁 References
> - [GitHub URL on Cavity Detection Model](https://github.com/Kim-src/Cavity-Detection-Model)

<br/>

***

<br/>
<br/>
<br/>

<!-- Title -->
# 🚀 Toy Project

<br/>

<!-- Contents -->
### 📌 Velog and LinkedIn
> - 2024-01-08 작업했던 데이터 분석 toy project 결과 내용을 벨로그 및 링크드인에 업로드 함
> - References란에 관련 링크를 작성함

<br/>

### 📌 Kaggle DataSets
> - 캐글 사이트에서 데이터셋을 발췌하는 방법을 학습함
> - 넷플릭스, 디즈니 데이터를 활용하여 Word Cloud 등을 제작함

<br/>

### 📌 TTA
> - 한국정보통신기술협회(TTA)에서 제작한 정보통신용어 사전의 존재를 인지함
> - 정보통신 관련 용어 학습 시 요긴하게 사용될 가능성이 있음

<br/>

### 🎁 References
> - [GitHub URL on Toy-PJT](https://github.com/Kim-src/Stock-Information)
> - [Velog URL on Toy-PJT](https://velog.io/@kim-src/stock-information)
> - [LinkedIn URL on Toy-PJT](https://www.linkedin.com/feed/update/urn:li:activity:7150347795420336128/)
> - [Kaggle DataSets](https://www.kaggle.com/datasets?topic=trendingDataset)
> - [TTA Dictionary](http://word.tta.or.kr/main.do)

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 8, 2024</p>

<!-- Title -->
# ✅ Python

<br/>

<!-- Contents -->
### 🔔 데이터 분석 : 라이브러리 활용
> #### 1. 웹 데이터 분석 시 활용되는 BeautifulSoup 및 Pandas 라이브러리의 장단점 비교  
> #### 2. 라이브러리 비교 테스트 한 결과를 깃허브에 연동 시도  

<br/>

### 📌 BeautifulSoup
> #### ⭕ 장점 : Parsing 기능으로 DB 내에서 추출하는 데이터를 세부적으로 선택할 수 있음  
> #### ❌ 단점 : 데이터 시각화가 어려우며 추출하려는 데이터를 print 구문에 일일이 입력해야 된다는 번거로움이 있음  

<br/>

### 📌 Pandas
> #### ⭕ 장점 : DB 내 모든 column에 대한 내용을 간편하게 발췌하여 데이터를 table로 시각화 할 수 있음  
> #### ❌ 단점 : Parsing 기능이 없기(?) 때문에 HTML 코드가 잘 구분되어 있지 않은 웹 페이지의 경우 데이터 추출이 온전하게 되지 않음  

<br/>

### 🚀 GitHub 연동
> - "Google Colab 내 Python code" 및 "GitHub repository" 연동 실패  
> - GitHub repository 연동을 위한 코드 입력을 다양하게 시도해봤지만 일반적인 터미널에 입력하는 방식과는 상이한 느낌이었음  
> - 결국 Google Colab 파일 탭에서 "GitHub에 사본 저장" 기능을 사용하여 GitHub "Stock" repository에 내용을 업로드하였음  
> - 추후 Python toy-project 시 GitHub 연동에 재도전할 예정임  

<br/>

### 🎁 References
> - [Python을 활용한 데이터 분석 Toy-PJT](https://github.com/Kim-src/Stock-Information)  
> - FastCampus Selena 강사님 강의  

<br/>

***

<br/>
<br/>
<br/>

<!-- Update Date -->
#### <p align="right">Date : January 7, 2024</p>

<!-- Title -->
# ✅ Java

<br/>

<!-- Contents -->
### 📌 강의 내용 요약 : 객체에 접근하는 권한 이해하기  
#### Q1. 자바에서 객체에 접근할 때 사용하는 접근제한자(Access Modifier) 4가지는 무엇입니까?
> - public, private, protected, default  

#### Q2. 자바에서 기능이 서로 비슷한 클래스들끼리 모아서 관리를 쉽게 하기 위한 것은 무엇입니까?
> - package → 보안 설정이 중요하다는 것이 일반 폴더와의 차이

#### Q3. 자바에서 제공하는 package 중 default package는 무엇입니까?
> - java.lang  

#### Q4. Class에 접근하는 방법 2자기는 무엇입니까?
> - main class 상단에 import package의 위치 입력  
> - class 이름 앞에 매번 full name 입력  

#### Q5. 자바에서 제공하는 API 중에서 String class와 Scanner class의 full name은 무엇입니까?
> - String class : java.lang.String  
> - Scanner class : java.util.Scanner  

#### Q6. Package를 현재 클래스에 포함시킬 때 필요한 명령어는 무엇입니까?
> - import  

<br/>

### 🎁 References
> - FastCampus 박매일 강사님 강의  

<br/>

***
<br/>
<br/>
<br/>
