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
