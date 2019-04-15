# 2일차 C# 공부

> 변수 : 값을 저장할 때 사용 하는 식별자

> 자료형 : 정수, 실수, 문자 및 문자열, 논리

> 값 형식 : 스택 메모리 공간 사용

> 참조 형식 : 힙 메모리 공간 

```c#
byte a = 100;
// byte 자료형의 size는 1바이트(8bit),
// 표현 범위는 0~255, 0부터 2의 8승 - 1
sbyte b = -55;
// sbyte 자료형의 size는 1바이트(8bit),
// 표현 범위는 -128 ~ 127, -2의 7승 부터 2의 7승 -1
short c = -5;
// short 자료형의 size는 2바이트(16bit),
// 표현 범위는 -32768 ~ 32767, -2의 15승 부터 2의 15승 -1
ushort d = 200;
// ushort 자료형의 size는 2바이트(16bit),
// 표현 범위는 0 ~ 65535, 0부터 2의 16승 - 1
a = 55;

Console.WriteLine(a);
Console.WriteLine(b);
Console.WriteLine(c);
Console.WriteLine(d);
```
sbyte와 byte의 차이점은 해당 범위!! 두 수의 차는 같다
ushort의 u는 *unsigned*
