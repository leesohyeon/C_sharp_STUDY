# 3일차 C# 공부

> 정수 표현 방식
```c#
int e = 70000;
// int는 4바이트! 
// 표현 범위가 약 21억이기 때문에 많은 수를 표현할 수 있다
// int 자료형의 size는 4바이트(32bit)
// 표현 범위는 -2의 31승 부터 2의 31승

uint f = 250000000;
// unsigned int는 0부터 약 42억까지 정수표현을 할 수 있기 때문에 
// int 보다 더 많은 수를 표현할 수 있다!
// uint 자료형의 size는 4바이트(32bit)
// 표현 범위는 0부터 3의 32승 - 1

long l
// long, ulong 각각 8바이트
// long의 표현 범위는 -2의 64승부터 2의 64승 -1
// ulong의 표현 범위는 0부터 2의 64승 -1
```

---

> 실수 표현 방식
```C#
// 부동 소수점 float 4byte, double 8byte
float f = 3.14f; // float 자료형은 뒤에 f를 붙여줘야 함, 붙이지 않으면 double로 인식
double d = 3.14; // 그렇다고 double 값 뒤에 d를 붙이지는 않는다. 구분 방법임!

Console.WriteLine(f / 3);
Console.WriteLine(d / 3);
// 결과 
// 1.046667
// 1.04666666666667 double 같은 경우, 자료형의 표현 범위가 더 넓기 때문에 float보다 자세한 값이 나온다!
```

---

> 문자(열) 표현 방식
```c#
// 문자, 문자열
char c = '이';
string s = "채원";

Console.WriteLine(c); // 이
Console.WriteLine(s); // 채원
```

---

> 논리 자료형
```c#
bool b1 = true;
bool b2 = false;

Console.WriteLine(b1); // True
Console.WriteLine(b2); // False
Console.WriteLine(b1 && b2); // False (곱하는 느낌)
```
