## JVM이란 무엇인가



Java로 작성한 코드를 운영체제가 바뀌어도 코드 그대로 실행해주는 것



## JDK버전 유의사항



상위버전에서 컴파일한 class파일은, 하위버전에서 실행할 수 없다.

하위버전에서 컴파일한 class파일은, 상위버전에서 실행할 수 있다.

(예컨대, 자바14버전과 자바8버전)



**## 다만, javac 옵션을 주면 cross compile이 가능하다**

[How to fix java.lang.UnsupportedClassVersionError: Unsupported major.minor version]: https://stackoverflow.com/questions/10382929/how-to-fix-java-lang-unsupportedclassversionerror-unsupported-major-minor-versi



> For example, in order to generate class files compatible with Java 1.4, use the following command line:

```java
javac -target 1.4 HelloWorld.java
```





## 바이트코드

![](C:\Users\rlgus\Downloads\1.PNG)



- 바이트코드 O    바이트 코드 X  : 붙인 게 맞다
- OP코드(operation code) 들은 1byte로 구성. 위 그림에서는 javap -c 옵션을 줘서 텍스트로 보이는 것임
- class파일 안에 생성되는 코드
  - JVM이 이해할 수 있는 형태의 코드
  - java파일은 사람이 이해할 수 있는 언어로 작성되며, JVM은 이를 컴퓨터가 이해할 수 있는 언어로 번역해서 전달
  - 이때 JVM이 이해할 수 있는 형태의 코드가 class파일 내부의 바이트코드
- aload, return 등의 operation code
  - 명령어
  - 1byte로 이루어짐 : 최대 256 (2^8, 8bit) 개까지 가능하며, 약 200개의 명령어가 있음



## JIT 컴파일러

계속...

https://youtu.be/T7NyR5UvyYo?list=PLfI752FpVCS96fSsQe2E3HzYTgdmbz6LU&t=5294