# 6일차 C# 공부

**조건문을 공부하는 날 !!!**

> if
```c#
int x = 3, y = 7;
if(x > y) 
  Console.WriteLine("if문이 참이면 실행"); 
Console.WriteLine("이곳은 출력이 될까용?"); // 출력, if문의 참 거짓 유무와 상관없이 출력!  
```
---

> if else
```c#
if(x > y) 
  Console.WriteLine("if문이 참이면 실행!!"); 
else 
  Console.WriteLine("if문이 거짓이면 실행!!"); // 출력
Console.WriteLine("이곳은 출력이 될까용?"); // 출력
```
---

> if, else if
```c#
if(x > y) 
  Console.WriteLine("if문이 참이면 실행!!");
else if(x != y)
  Console.WriteLine("첫 번째 if문이 false, 두 번째 if문이 true일 때 실행"); // 출력
else
  Console.WriteLine("이곳은 출력이 될까용?"); // 출력
```
---

> switch case (고정된 값을 비교할 때 많이 사용함)
```c#
int z = 10;

switch(z)
{
  case 1:
    Console.WriteLine("숫자 1입니다");
    break;
  case 10:
    Console.WriteLine("숫자 10입니다"); // 
    break;
  default:
    Console.WirteLine("case에 없는 값일 때 실행");
    break;
}    
```

---
if문과 switch문 비교 !!

```c#
  case 1:
    Console.WriteLine("숫자 1입니다");
    break;
  // if(z == 1) Console.WriteLine("숫자 1입니다");
  case 10:
    Console.WriteLine("숫자 10입니다"); // 
    break;
  // else if(z == 1) Console.WriteLine("숫자 10입니다");
  default:
    Console.WirteLine("case에 없는 값일 때 실행");
    break;
  // else Console.WriteLine("case에 없는 값일 때 실행");
```
