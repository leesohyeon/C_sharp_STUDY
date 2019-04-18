## 조건문
* if /  if, else / if, else if
 
```C#
int x = 3, y = 7;

if(x < y)
   Console.WriteLine("if문이 참이면 실행");
 Console.WriteLine("이곳은 출력이 될까요??");  //if문과 상관없이 실행됨 
//{ }로 묶으면 그 안에 있는 내용은 모두 출력이 된다.


if(x < y)
   Console.WriteLine("if문이 참이면 실행");
else
   Console.WriteLine("거짓일 때 실행");
Console.WriteLine("이곳은 출력이 될까요??");  //if문과 상관없이 실행됨 



if(x > y)
   Console.WriteLine("if문이 참이면 실행");
else if(x != y)
   Console.WriteLine("첫번째 if문이 false일때, 2번째 if문이 조건이 true이면 실행");
else
   Console.WriteLine("if문 모두 false일때 실행");

```
* switch    
  하나의 값이 정해져있을때 사용하면 좋다.
```C#
int z = 10;

switch(z)   //z값에 따라 case문을 찾음
{
    case 1:
	Console.WriteLine("숫자 1입니다.");	
	break;
    case 10:
	Console.WriteLine("숫자 10입니다.");
	break;
    default:  //case에 없으면 default문으로 감
	Console.WriteLine("case에 없는 값일 때 실행");

}

```
if문을 switch로 바꿀 수도, switch문을 if문으로 바꿀 수 있다.




## 반복문
* for   
  for(초기 값 ; 조건식 ; 증감식)
```C#
int x=10, i =1;

// i=1, 1<=10, 2=1+1;
// i=2, 2<=10, 3=2+1;
//....
// i=10, 10<=10, 11=10+1;
// i=11, 11<=10  ---->거짓, 반복문이 종료
for(i=1; i<=x; i++) 
{
    Console.WriteLine(i);	
}

```
for : 초기값에 이미 선언한 변수를 써도 되고 그 안에서 선언해도 된다.  
 ==> i가 1부터 x까지 하나씩 증가한다.


### 구구단
 ==> 입력받은 수의 단을 출력한다.  
 +) Console.ReadLIne()은 사용자로부터 값을 입력받을 때 사용, 문자열로 입력받는다.
```C#
int x;
string y;

y = Console.ReadLine(); //산술연산을 하기 위해 파싱해야 함
x = int.Parse(y); //문자 y를 int로 바꿔 x에 넣어줌

for(int i=1; i<10; i++)
{
  Console.WriteLine("{0} * {1} = {2}", x, i, x*i);  //5입력 시 : 5*1=5, 5*2=10....5*9=45
}
```

* While  
 while(조건식){}
```C#
int x;
string y;
int i;

y = Console.ReadLine();
x = int.Parse(y); 
i=1;
while(i<10)
{
  Console.WriteLine("{0} * {1} = {2}", x, i, x*i);
  i++;  //i++ 안 해주면 i는 계속 1이기 때문에 무한반복된다.
}
```
