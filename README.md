# Java Package

Java 의 패키지는 클래스, 하위 패키지 및 인터페이스 그룹을 캡슐화하기 위한 메커니즘이다.  

#### 패키지의 용도

- 서로 다른 패키지에 동일한 이름의 클래스, 인터페이스, enum 등을 정의할 수 있다.
- 클래스, 인터페이스, enum 등의 검색 및 사용을 더 쉽게 할 수 있다.  
- default 및 protected 접근자 제어를 통해 패키지 수준에서의 접근 제어를 제공한다.  
- 패키지는 데이터 캡슐화(또는 데이터 은닉)로 간주할 수 있다.  

#### 패키지의 작동

패키지의 이름과 구조는 밀접한 관계가 있다.  
만약 패키지 이름이 com.oh29oh29.study01 이면 3개의 디렉토리 com, oh29oh29, study 가 있으며 study 는 oh29oh29 에 있고, oh29oh29 는 com 에 있다.  
또한 디렉토리 com 은 CLASSPATH 변수를 통해 접근할 수 있다.  
즉, com 의 부모 디렉토리 경로가 CLASSPATH 에 있는 것이다. 그렇게 함으로써 com 의 경로를 쉽게 찾을 수 있는 것이다.  

## import 키워드

import 는 현재 패키지에 접근할 수 있는 다른 패키지의 클래스, 인터페이스 및 기타 멤버들을 만들기 위해 필요한 키워드이다.  

#### Import a single member from a package

다른 패키지의 특정 클래스 또는 인터페이스를 현재 패키지에서 만들기 위해서 package 문 뒤에 정의한다.

```java
package com.oh29oh29.study01.sample01;      // Problem 클래스의 패키지 

import com.oh29oh29.study01.sample02.Java;  // import statement 

public class Problem {
    Java java = new Java();
}
```

#### Import all the members from a package

패키지 이름 뒤에 asterisk(*) 와일드 카드 문자와 함께 import 키워드를 사용하면 해당 패키지의 모든 타입(클래스, 인터페이스, enum 등등)에 접근할 수 있다.  

```java
package com.oh29oh29.study02.sample01;

import com.oh29oh29.study02.sample02.*;     // import statement with (*) wild card

public class Problem {
    Java java = new Java();
    Database database = new Database();
}
```

<hr>

#### References

> 웹 문서
> - [geeksforgeeks | Packages In Java](https://www.geeksforgeeks.org/packages-in-java/)
> - [javacodegeeks | Java Import Keyword Example](https://www.geeksforgeeks.org/packages-in-java/)
