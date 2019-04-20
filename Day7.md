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
괄호 안의 조건이 맞지 않으면 한 번도 실행이 안될 수 있다
```c#
  while(i < 10)
  {
    Console.WriteLine("{0} * {1} = {2}", x, i , x*i);
    i++; // i를 증가시키지 않는다면 무한루프 
  }
```
무한루프를 멈추려면 `ctrl + C`를 눌러 멈춘다!

> do while
조건이 맞지 않더라도 반드시 처음 한 번은 실행!
```c#
string x;

do
{
  Console.WriteLine("반복문 연습중...");
  x = Console.ReadLine();
} while(x != "q"); // 입력되는 문자열이 q가 아닌 동안 반복
// 대문자 Q를 넣는다 해도 종료가 되는 것은 X!

/*
대문자 Q도 실행되도록 하기 위해서는
while ((x != "q") && (x != "Q"));
*/

> foreach : 배열과 같은 컬렉션 개체를 다룰 때 사용되는 반복문
컬렉션에 대한 개념알기
컬렉션 : 
```c#
string[] x = {"짜장면", "짬뽕", "탕수육"};
int[] y = {55, 7, 31, -9};

foreach (string i in x)
{
  Console.WriteLine(i); // 짜장면 짬뽕 탕수육
}

foreach (int i in y)
{
  Console.WriteLine(i); // 55 7 31 -9
}
```
for문은 초기값을 설정, 초기값부터 시작하며 조건문을 설정해서 실행
foreach문은 초기값이나 조건문이 없이 간단하게 실행

> break
```c#
int[] y = {55, 7, 31, -9};

for (int j = 0; i < 4; j++)
{
  if (j == 2) break; // 반복문 탈출
  Console.WriteLine(y[j]); // 55 7
}
```

> continue
```c#
int[] y = {55, 7, 31, -9};

for (int j = 0; i < 4; j++)
{
  if (j == 2) continue; // 2인 부분 실행x, 패스하고 실행
  Console.WriteLine(y[j]); // 55 7 -9
}
```
