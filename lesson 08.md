## 연산자(Operator)
* 산술 : +, -, *, /, %
```C#
int a = 55;
in b = 3;
Console.WriteLine(a + b);
Console.WriteLine(a - b);  //-52
Console.WriteLine(a * b);  //165
Console.WriteLine(a / b);  //0
Console.WriteLine(a % b);  //3  몫을 구하고 난 나머지 
```
* 증감 (후위/전위)
```C#
int a = 55;
int b=2;
++b; //b = b+1;  -> 3이 나옴
a++; //a = a+1;  -> 56
/////////////////
int x = 55;
Console.WriteLine(x++);  //x값 출력 후 x =x+1을 함
//result : 55
Console.WriteLine(++x);  //x = x+1을 한 후 x값 출력
//result : 57
Console.WriteLine(++x);  //58
Console.WriteLine(x++);  //58
Console.WriteLine(x);    //59
```
* 대입(할당) : =, +=, -=, *=, /=, %=
```C#
int x = 55;
Console.WriteLine(x);  //55
//x = x+1;
x += 1;
Console.WriteLine(x);  //56
```
* 비교 : >, <, ==, !=, <=, >=
```C#
int x = 55;
int y = 44;
bool z;
z = (x != y);  //변수를 만들어 명제의 결과를 z에 넣음 
Console.WriteLine(x<y);  //비교연산자의 결과는 bool 타입으로 나옴(true, false)
```
```
