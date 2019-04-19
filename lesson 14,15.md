## do while 
 while문(조건이 맞지 않으면 한 번도 실행되지 않음)  
 do while문(조건이 맞지 않아도 한 번은 무조건 실행됨)  
 
```C#
string x;

do
{
  Console.WriteLine("반복문 연습중... ");
  x = Console.ReadLine();

}while((x != "q") && (x != "Q")); //입력받은 x가 q가 아니면 계속 반복
```

## foreach
 foreach문은 배열과 같은 컬렉션 개체를 다룰 때 사용되는 반복문  
 배열 : 번호가 붙어있는 락카와 같은 개념/같은 이름을 가진 변수가 여러개가 있고 인덱스번호로 구분   
   맨 앞은 0번부터 시작
```C#
string[] x ={"짜장면", "짬뽕", "탕수육'};
int[] y ={55, 7, 31, -9};

foreach(string i in x) //x 배열에 있는 값을 i에 하나씩 넣는다.
{
  Console.WriteLine(i);  //x 배열 0번째 값부터 하나씩 출력됨
}

//배열과 받는 변수의 타입은 같아야 한다.
foreach(int j in y) 
{
  Console.WriteLine(j);  
}

//foreach문으로 작성한 것을 for문으로 바꿀 수 있다.
for(int j=0; j<4; j++)
{
  Console.WriteLine(y[j]);
}
```


## break
 반복문 중간에 탈출하는 것
```C#
string[] x ={"짜장면", "짬뽕", "탕수육'};
int[] y ={55, 7, 31, -9};

for(int j=0; j<4; j++)
{
  if(j == 2) break;   //break 이후의 문장은 실행하지 않고 for문을 빠져나온다.
  Console.WriteLine(y[j]);
}
//result : 55, 7


for(int j=0; j<4; j++)
{
  if(j == 2) continue;   //이후의 라인을 실행하지 않고 증감식으로 이동한다.
  Console.WriteLine(y[j]);
}
//reault : 55, 7, -9

```


# 메소드(Method)
* 객체 지향 언어(OOP)에서 사용되는 용어 - 메소드는 클래스 안에 만들어지는 것, 함수와는 비슷한 개념  
   2가지 형태(클래스메소드 / 객체 생성 후 사용하는 메소드)
* return - 메소드가 끝남과 동시에 메소드를 호출한 곳에 값을 전달해주는 역할
* Recursive call

```C#
class Dog
{  //강아지가 하는 기능 - 메소드
   public static void Eat(string food)  //parameter
   {
      Console.WriteLine(food+"를 맛있게 먹습니다. 냠~냠~");   
   }
   public static string Sleep()
   {
      //Console.WriteLine("쿨쿨");  //return이 void
      return "쿨쿨";
   }

}//Dog

class Chap15
{
   public static void Nice()
   {
     Console.WriteLine("C# 꿀잼");
   }
   static void Main(string[] args)
   {
     Chap15.Nice();  //result : C# 꿀잼
     Dog.Seelp();  //return이 void였을 때 result : 쿨쿨
     Dog.Eat("사료");
     Dog.Eat("개껌");  //인수, 파라미터, 매개변수
     Console.WriteLine(Dog.Sleep());   //return이 string
   }
}//Chap15
```

void : return 값이 없을 때 사용  
parameter : '사료'의 주소가 string food로 넘어가 메모리 주소를 기억한다. 메소드 호출에서 어떤 값이 들어오느냐에 따라 출력되는 문장이 달라짐  
return : void 자리에 자료형이 오고 메소드 안에서 return 문을 적어 그 값을 메소드를 호출한 곳으로 반환한다.  
+) static이 붙는 이유는 다른 calss에서도 접근이 가능하도록 만들기 위해  

