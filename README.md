# ComputerLanguageAndExperience
컴퓨터언어및실습 수업정리


## 1강(20180911) ##
1. 프로그램 작성시 가장 중요한 것은 if, for와 같은 조건 반복문이다. 어떠한 문제의 조건과 반복을 파악하면 만들기 쉽다.<br>

2. 프로그램 언어의 역할 <br>
  기술적 언어:컴퓨터가 작동하도록 지시함 <br>
  개념적 언어:프레임워크(의사코드) <br>
  
3. 프로그래밍하면서 다루어야 하는 두 가지의 것 <br>
  정보 : 우리가 조종(manipulate)하고자 하는 '것'을 의미 <br>
  절차 : 정보를 조종하기 위한 기술 <br>
  
4. Formal Language : 컴퓨터와 대화하기 위한 수단 <br>

5. 프로그래밍 언어는 컴퓨터가 어떠한 동작을 수행하도록 하는 '지시사항'을 담고 있다. <br>
  print("asdf") <br>
  
6. 기계언어 <br>
  처리장치가 유일하게 이해할 수 있는 언어. <br>
  0과 1로 이루어짐 <br>
  ~~~
  00010101 
  11010001 
  01001100 
  ~~~
  각 줄은 processor에 의해 처리됨 <br>
  기계언어로 프로그래밍 하는 것은 모든 명령어를 외우기 힘들기 때문에 어렵고 느리다. <br>
  
7. 어셈블리어 <br>
  기계언어를 단어와 숫자로 표현되도록 한 것 <br>
  ~~~
  LOAD A, 9999
  LOAD B, 8282 
  SUB B
  MOV C, A
  LOAD C, #0002
  DIV A, C
  STORE A, 7002
  ~~~
  기계어보다 쉽지만 여전히 어렵다. 메모리의 변경이 가능하지 않다. (공간 A의 주소는 여전히 공간 A의 주소여야 한다)(BIG PROBLEM)<br>
  각각의 컴퓨터는 저마다의 어셈이 있다-->소프트웨어보다 하드웨어에 더 의존이 큼<br>
  근데 아두이노로 개발할때 어셈을 쓰나...?<br>
  
8. 고급언어
  더 많은 단어를 사용하고, 문장이 영문장과 비숫하도록 만든다.<br>
  프로그래밍 구조는 problem-oriented ==> 컴퓨터가 어떻게 그것것을 실행하는지는 알 필요가 없다.<br>
  Basic, fortran, pascal, cobol, c, c++, java<br>
  고급 언어는 컴파일러에 의해 분석되어져야 하고, 기계언어로 컴파일되어야 프로세서가 그것을 실행할 수 있다.<br>
  
### 9. C언어 ###
  명명이유는 Bell 연구소에서 개발돤 B언어를 기반으로 만들어졌기 때문이다.<br>
  데니스 리치에 의해 개발<br>
  켄 톰슨과의 협업을 통해 이것은 유닉스 체제에 사용되었다.<br>
  C언어는 모호하게 정의되었고, 표준화되지 않았기때문에 거의 대부분의 사람들이 스스로의 ㄱ관점을 가지고 있었다<br>
  표준 언어의 출현이 긴박하게 요구됨.<br>
  ANSI에서 표준을 개개발함<br>

10. Imperative Language C
  highly imperative language<br>
  -어떻게 무엇을 하길 원하는지 명백하게 표현해야함<br>
  -의미와 기능을 명백하게 표현해야함<br>
  -어떠떤 라입이블브러리를 사용하는지 명확하게 해야함<br>
  -모든 것완벽하게 표현해야함<br>
 
 11. simple code in c
 ~~~
 #include <stdio.h> // header
 
 int main() // beginning of program
 { // start of segment
  printf("hello world")// function for printning text ;// end of statement
  return 0;
 } // end of segment
 ~~~
 12. 전처리기
  '#' 문자를 이용해 전처리기를 지시한다.<br>
  컴파일 과정 직전에 시행된다.<br>
  ~~~
  #include <...>
  #defind A B
  ~~~
  #incllude <stdio.h>는 stdio.h 라는 헤더 파일을 식별한다.<br>
<br>

13. main 함수
~~~
int main()
{
  return 0;
}
~~~
모든 c언어 프로그램의 시작. 모든 c 프로그램은 main 함수를 가져야 한다.

14. 중괄호 {}
  소스코드의 segment와 body를 식별하게 한다.<br>
  이것이 start와 end를 의미하기 때문에, {의 개수는 }와 같아야 한다. 즉, 열었으면 닫아주어야 한다.<br>

15. Statement
  프로그램에서 실행되어야 할 action을 기술 <br>
  세미콜론(;)을 무조건 찍어야 함

16. 식별자(identifier)
  특정한 프로그램 요소(변수, 함수 이름 등)을 표현하는데 사용되는 단어들
  ~~~
  int myName; // myName은 변수의 이름을 나타내는 식별자이다.
  public static void myFunction(int myName) // myFunction은 함수 이름을 나타내는 식별자이다.
  ~~~
17. 예약어(keywords)
auto, do, goto, signed, unsigned, break, double, if, sizeof, void, case, else, int, static, volatile, <br>
char, enum, long, struct, while, const, extern, register, switch, continue, float, return, typedef, default, for, short, union 등<br>
기본적으로 컴파일러가 점유한 단어들로, 특정한 기능, 역할을 수행할 때 사용된다. 이 단어들은 변수나 함수 등의 이름으로 사용이 불가능하다.<br>

18. 변수(variables)
변수 : 값이 변경경될 수 있는 메모리 공간과 관련된 이름.<br>
변수 선언 : int thisIsVariable; // 사용자가 지정한 이름의 변수를 만들 수 있다.<br>
변수 정의 : thisIsVariable = 5; // 어떠한 변수에 값을 할당할 수 있다. 이때 '='기호가 하나 사용된다.<br>
흔히 수학에서 사용되는 '='의 역할을 프로그래밍 언어에서는 '=='이 담당한다.<br>
'->'는 결코 대입이 아님에 주의하라.<br>

~~~
int integerValue; // 정수형 변수
float floatValue; // 실수형 변수
double doubleValue; // 실수형 변수, float와 다른 점이 존재함
char charValue; // 문자형 변수
~~~
이외에도, long long ('__int64'), string 등의 변수형도 언어에 따라 존재할 수 있다.<br>

19. 변수 명명 규칙
  영문, '_'로 시작 (int iLove5) <br>
  숫자로 시작 불가 (int 5iLove) <br>
  예약어 사용 불가 (int return) <br>

20. 상수
  constants, 프록로그램 수행 중 절대 변경되지 않는 data <br>
  변수 선언시 const 식별자를 사용하거나, #define 전처리기를 사용해 선언할 수 있다.
  ~~~
  #define PI 3.14
  ...
  const double DOUBLE_PI = 3.14;
  ...
  ~~~
  이미 선언되고 정의된 상수형 변수( const 식별자를 이용해 선언된 변수)를 변경하고자 하는 일체의 행위는 오류를 발생시킨다.<br>

21. enum
  list처럼 주어진 값들<br>
  ~~~
  enum Language {
    CLanguage,
    Java,
    Python
  }
  ~~~
  python의 dictionary와 유사<br>
 
22. 기본적인 자료형
  int범위가 -32768 ~ 32767로 설명된 책은 도대체 언제적 책인가, 그리고 우리 교수님께선 왜 이 책으로 설명을 하시는가
  
  -2147483648 ~ 2147483647임에 주의하자
  unsinged는 양수만 나타내는 변수를 선언할 때 사용한다.
  
  int : 4byte : –2,147,483,648 ~ 2,147,483,647<br>
  unsigned int : 4byte : 0 ~ 4,294,967,295 <br>
  char : 1byte : –128~127 <br>
  float : 4byte : 3.4E+/-38(7개의 자릿수) <br>
  double : 8byte : 1.7E+/-308(15개의 자릿수) <br>
  
