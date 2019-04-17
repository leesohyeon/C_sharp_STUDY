* 변수 : 값을 저장할 때 사용하는 식별자(값이 변할 수 있음)
* 자료형 : 정수(int..), 실수, 문자 및 문자열, 논리
* 값 형식 : 스택(stack) 메모리
- byte(1바이트(8bit), 표현 범위 : 0~255, 0부터 2의 8승 -1) 
    ex) byte a = 100;
- sbyte(1바이트, 음수까지 저장 가능, 표현 범위 : -2의 7승 ~ 2의 7승-1 => -128~127)
    ex) sbyte b = -128;
- short(2바이트, 표현 범위 : -32768 ~ 32767, -2의 15승 부터 2의 7승 -1) 
   ex) short c = -32768;
- ushort(2바이트, 표현 범위 : 0 ~ 65535, 0부터 2의 16승 -1 )
   ex) ushort d = 32768;
'='는 우측의 값을 좌측에 넣어줌 

* 자료형 : 정수(int..), 실수, 문자 및 문자열, 논리
- int(4바이트(32bit), -2의 31승 부터 2의 31승 -1)  
    ex) int e = 70000;
- uint(4바이트, 음수는 안됨, 표현 범위 : 0부터 2의 32승 -1)
    ex) uint = 2500000000;
- long, ulong 각각 8바이트
* 실수(부동 소수점)
  IEEE 754 부동 소수점 표현방식 -> 더 자세하게 알아볼 수 있음
- float(4바이트)
   ex) float f = 3.14;(Error-double로 인식함) -> float f = 3.14f;
- double(8바이트)
    ex) double d = 3.14;
	``` C#
	Console.WriteLine(f / 3);  //결과는 float
  Console.WriteLine(d / 3);  //결과는 double
	```
* 문자 및 문자열
- char (문자)
    ex) char c = '김';
- String (문자열)
    ex) string s = "C# 공부";
* 논리 자료형(boolean)
- bool(true/false)
    ex) bool b1 = true;  
          bool b2 = false;
          Console.WriteLine(b1&&b2); //양쪽 다 true일 경우 true, 하나라도 false일 경우 false



