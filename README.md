<img src="https://venturebeat.com/wp-content/uploads/2015/12/oracle-java-e1450723340931.jpg?w=1200&strip=all" width="200" height="100">



# `Java`를 공부하면서 기록을 남기는 곳

참고 강의 : https://www.youtube.com/playlist?list=PLuHgQVnccGMAIluRRVsC1e79ri-dwnBmR

취준을 1년가까이 하면서 느꼈지만 Java를 쓰는 기업이 참 많은것 같다

Java자체나 프레임워크, 앱개발(kotlin 등)에도 쓰여서 범용성이 참 넓은언어라는 생각이 든다

뭔가 손이 안가서 끝까지 안하고 싶었지만 결국 자존심 굽히고 Java를 정복하기로 마음먹었다

<br>

>### 전에 Docker를 공부하면서 기록을 매우 디테일하게 남겼었는데 결론은... 너무 힘들었다..
>- 내용을 전부다 적으려고 하니까 지치고 피곤해서 중간에 포기한게 된것같다
>- 그날그날 느낀점이나 공부를 하면서 생긴 의문점을 적어두는 일기장 정도의 공간으로 바꾸려고 한다
>- 이제는 공부하다가 의문점이 생기면 여기다가 Question을 적고
>- 검색해서 찾은 좋은 답변(Answer)을 찾아서 날마다 ___Q&A를 올리는 식___ 으로 간소화 하려고한다

<hr><br>

## `2023-09-06` Java 1일차
- 노트북에 자바를 설치하고 환경설정까지 완료하기(문서 작성 및 자료검색은 데스크탑으로)
- Java IDE중 하나인 eclipse도 설치

.java 파일은 사람이 읽고 쓸수있는 소스파일

이 파일을 저장하면 자바가 컴파일을 거쳐서 class라는 새로운 파일을 만든다

.class 파일은 사람이 읽을수 없는 파일

HelloWorld를 띄우는것으로 우선 자바 환경설정은 마무리가 됐다 (과정 생략)

<br>

## `2023-09-07` Java 2일차
- Java가 컴퓨터에서 어떻게 동작하는지 이해
  - 자세한 설명 : https://youtu.be/9V0rdrm59X4?si=Pet0aTxUQNK88YKM&t=120
![image](https://github.com/sonkeehoon/Java/assets/81700507/f3dc0d98-eb11-4b63-a535-c8bc3c50a886)

1. 확장자가 .java인 소스코드를 작성
  - 사람만 이해할수 있는 언어이다
  - 기계(컴퓨터)는 .java 파일을 이해할수 없다
2. 기계가 알아듣게 만들기 위해 .java 파일을 compile 해서 .class 파일로 바꾼다
- 이클립스에서 소스코드(.java)파일을 작성하고 저장 버튼을 누르면 자동으로 class파일이 생성된다
- 개발자가 Java의 기술을 응용해서 만든 Application
- 확장자가 class인 이 파일을 Java Application 이라고 부른다
3. JVM(Java Virtual Machine)에게 .class파일을 실행하라고 시킨다
- 이클립스에서 run 버튼을 누르면 수행되는 일
- JVM이 확장자가 class인 파일을 읽어서 적힌대로 컴퓨터를 동작시킨다

Java로 할수있는 것들은 뭐가 있을까?
- 데스크탑 어플리케이션 : https://www.youtube.com/watch?v=bZuoyW26zW4&list=PLuHgQVnccGMAIluRRVsC1e79ri-dwnBmR&index=11
- 사물 제어 : https://www.youtube.com/watch?v=hbk1twmxzF4&list=PLuHgQVnccGMAIluRRVsC1e79ri-dwnBmR&index=12
- 안드로이드 어플리케이션 : https://www.youtube.com/watch?v=hbk1twmxzF4&list=PLuHgQVnccGMAIluRRVsC1e79ri-dwnBmR&index=13

<br>

## `2023-09-08` Java 3일차
공부할 내용
- 데이터와 연산
- 데이터 타입
- 숫자와 연산
- 문자열의 표현
- 문자열 다루기

다른 언어에서 수차례 공부했던 부분들이라 가볍게 들으면서 넘어가려고 한다

> vscode에서도 java가 실행 가능한 모양이다..! eclipse가 개인적으로 불편하기도 해서 내일 해보려고 한다

<br>

## `2023-09-09` Java 4일차
전날에 메모해둔 vscode에서 java실행을 성공했다

복잡할줄 알았는데 생각보다 별거 없었다.. 그냥 영상보고 따라하면 된다
- https://youtu.be/dulYAOildPw?si=pTt5ot4B4muRSQkg&t=125

공부할 내용
1. 변수의 정의
2. 변수의 효용
3. 데이터 타입의 변환(casting)

__Q. (casting 관련 질문) 다음 코드에서 b가 1.0으로 출력되는 이유가 뭘까?__

![image](https://github.com/sonkeehoon/Java/assets/81700507/81504c5f-2dfb-4b39-b651-ba5d2d1ff5dd)

분명히 b = 1을 넣었음에도 출력해보면 1.0이 나온다 왜그럴까?

>- A. b = 1 이지만 b의 데이터 타입은 double로 선언됐기 때문에 1이 아닌 1.0으로 자동 변환해준다
>- 그런데 거꾸로 int c = 1.1; 이렇게 선언하면 에러가 난다
>- 이걸 해결하려면 double c = 1.1; 하거나
>- int c = (int) 1.1; 이렇게 해야하는데
>- 여기서 형변환을 할때 __중요한 규칙__ 이 나온다
>- int형인 1을 double형인 1.0으로 바꾸는건 그냥 소수점을 붙히면 되기때문에 문제가 없다
>- 그런데 double형인 1.1을 int형으로 강제로 바꾸면
>- ![image](https://github.com/sonkeehoon/Java/assets/81700507/7aaff8f4-8f7c-4351-a834-6213dbce1eee)
>- 이런 데이터 손실이 발생할수 있기때문에 명시적으로(int)라고 하지 않으면 에러를 발생시키는 것이다

<br>

## `2023-09-13` Java 5일차

1. 프로그래밍
2. IOT 라이브러리
3. IOT 프로그램
   
강사님의 코드를 그대로 내 프로젝트에 불러와서 import하는 내용이었다

특별히 메모할 내용은 없다

<br>

## `2023-09-17` Java 6일차

1. 디버거

디버거의 유용함을 다시한번 느낀 강의였다

오늘도 특별히 메모할 내용은 없다

<br>

## `2023-09-20` Java 7일차

1. 입력과 출력

입력을 받을때 대화상자를 띄워서 입력받고 싶다면

```
import javax.swing.JOptionPane;

JOption.showInputDialog(message);
```

입력받은 String 데이터를 Double로 변환하려면
```
Double.parseDouble(variable);
```

<br>

## `2023-09-22` Java 8일차

1. 자바 직접 컴파일하고 실행하기
  - .java 파일을 컴파일해서 .class로 바꾼다
  - .class파일을 실행(Run)한다
  - 실행할때 입력값을 준다
2. 라이브러리를 이용할때 컴파일하고 실행하기

리눅스에서 환경변수 수정하는법
```
vi ~/.bash_profile
```
맨 아랫줄에 본인의 JAVA JDK가 설치된 곳의 bin 디렉토리를 적어준다(예시)
```
export PATH=$PATH:/Library/Java/JavaVirtualMachines/jdk-9.0.4.jdk/Contents/Home/bin
```
1.1 .java파일 컴파일

터미널에서 컴파일하기 원하는 .java파일이 있는곳으로 이동한 후 다음 명령어를 실행한다
```
javac {filename}.java
```
잘 안될수도 있다. 그냥 넘어가자

.class 파일 실행하기
```
java {filename}
```
주의할 점은 filename 뒤에 .class를 붙이지 않는다

<br>

## `2023-09-23` Java 9일차

1. 자바 문서 보는법
   - API vs UI
   - 패키지, 클래스, 변수, 메소드
   - 클래스
   - 인스턴스
   - 상속

1.5 상속

![image](https://github.com/sonkeehoon/Java/assets/81700507/e6ca6d00-418a-476c-a835-022231c2e1ed)
![image](https://github.com/sonkeehoon/Java/assets/81700507/2ec2829a-4730-4e7f-bfb6-e24f6fe8586d)


Object(=superclass)는 Writer의 부모클래스이고 Writer는 PrintWriter의 부모클래스이다

PrintWriter를 만들던 사람이 처음부터 짜기 귀찮아서(?) Writer를 상속받고

거기에 본인이 필요한 기능만 추가적으로 넣어서 새로운 PrintWriter를 만든것

당연히 PrintWriter 클래스는 모든 Writer의 기능을 사용할수 있다

<br>

## `2023-09-25` Java 10일차

1. 나의 앱 만들기

강의 내용을 그대로 따라하면 된다 특별히 어려운점은 없었다

사용자의 입력을 받을때 eclipse 에서는 args에 변수를 주는법이 있는데 

나는 vscode에서 작업중이라 그냥 java.util.Scanner 를 활용했다

예를들면
```
import java.util.Scanner;
Scanner sc = new Scanner(System.in);
System.out.print("가격을 입력하세요 : ");
double valueOfSupply = sc.nextDouble();
...
```
이런식으로 입력을 받았다. 끝!
























