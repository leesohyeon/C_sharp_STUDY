# 7일차 C# 공부
반복문에 대해 !

> for (가장 많이 쓰이는 반복문이라고 할 수 있음)
```c#
int x = 10, i = 1;

// for (초기값; 조건식; 증감식)
// i == 1 ~ i == 10 -> 참, 반복문 실행
// i == 11, 11 <= 10 -> 거짓, 반복문 종료
for (i = 1; i <= x; i++) 
{
  Console.WirteLine(i);
}
```

```c#
string y;

y = Console.ReadLine(); // 안녕하세용 (입력)
Console.WirteLine(y); // 안녕하세용 (출력)
```
Console.ReadLine()에 숫자를 입력해도 y는 string형이기 때문에 숫자가 아닌 문자열로 인식된 채로 입력이 된다!
따라서 +를 넣어도 연산이 되는 것이 아닌, 문자끼리 합쳐진 상태로 출력 된다.

```c#
int x;
string y;

y = Console.ReadLine(); // 50 (입력)
x = int.Parse(y);
Console.WirteLine(x+7); // 57 (출력)
```

```c#
int x;
string y;

y = Console.ReadLine(); // 50 (입력)
x = int.Parse(y);

for (int i = 1; i < 10; i++)
  Console.WriteLine("{0} * {1} = {2}", x, i , x*i); // 구구단 형식
```

> while
```c#
  while(i < 10)
  {
    Console.WriteLine("{0} * {1} = {2}", x, i , x*i);
    i++; // i를 증가시키지 않는다면 무한루프 
  }
```
무한루프를 멈추려면 `ctrl + C`를 눌러 멈춘다!
> do while

> for each

> break

> continue
