### 값 형식 : 스택(stack) 메모리 공간 사용
  { 로 시작해 }로 끝나는 공간안에서 사용 -> 바로 메모리에서 제거
  
### 참조 형식 : 힙(heap) 메모리 공간 사용
  GC(Garbage Collector)에 의해 -> 더이상 사용하지 않는 변수 공간을 제거
  
  ```C#
  int a = 55;  //값 형식 변수, 중괄호가 끝나는 시점에 메모리에서 제거
  object b ="ITGO";  //참조 형식 변수, GC 메모리에서 제거
  object c = 100;   //참조 형식 변수, GC 메모리에서 제거
  Console.WriteLine("{0} {1} {2}",a,b,c);  //a에 들어있는 값을 {0}에 찍고...
  Console.WriteLine("{1} {0} {2}",a,b,c);  //ITGO 55 100 ->순서를 바꿀 수 
  ```
   object는 모든 자료형의 조상
  
  # 주석문, 형변환, 열거식, 기타 형식
   * 주석문 : /*  */ 여러줄 주석 처리, // 해당 라인 주석처리
   * 형변환 : 자료형의 변경
   * 열거식 : enum
   * 기타형식 : var, ...
   
   
``` C#
//3개 모두 정수형, 음수도 가능
//같은 물통이지만 공간이 다름
int a = 55; 
short d = 30000;   //0111 0101 0011 0000(2)
sbyte e = 127;
//작은 수를 큰 수로 형 변환
int f;
f = e;  //result:127
//e = 30000;  //Error(암시적으로 변환 불가)
e = (sbyte)d;  //2바이트 자료형인 short을 sbyte형으로 강제 형변환, Overflow 발생
```
0111 0101 0011 0000(2)이 강제 형변환되면서 e에는 0011 0000(2)만 들어가게 됨
```C#
//공간은 같지만 물통이 다름
int f;
float g = 3.141592f;
f = (int)g;  //float형 -> int형으로 강제 형변환, 소수점 부분이 잘려나감
//f - result : 3
```
  
# lesson7
## 열거식
```C#
class Program
{  enum Human { Warrior, Wizard=55, Thief}  //열거식 - 이름은 Human임
  //값이 첫번째부터 0으로 시작함, 중복 X
  static void Main(string[] args)
  {
    Console.WriteLine(Human.Wizard);  //Human.Wizard = 1
    Console.WriteLine((int)Human.Thief);  //result : 2
    Console.WriteLine(Human.Warrior);  //result : Warrior
  }
}```
Wizard = 55이면 그 다음 부터는 숫자가 하나씩 증가하기 때문에 (int)Human.Thief에는 56이 나온다.
## 기타형식
```C#
class Program
{  static void Main(string[] args)
  {
      //값에 따라 타입이 자동적으로 지정됨. 값이 할당되는 시점에 x는 double로 결정됨
      //주의점 : 할당되는 시점에서 타입이 결정되기 때문에 선언과 동시에 초기화를 해야 한다.
      var x = -55.7;
      var y ="CHOI";  //string
      var z = 9;      //int
      object a = 3.7;
      a = 5;    //가능
      z = 11;   //가능
      // z = 11.7;   //자료형이 다르면 Error -> 캐스트 연산자를 써주어야 함
      z = (int)11.7;  //명시적으로 해줌 소수점이 잘려나감
         
      Console.WriteLine("{0} {1} {2} {3}",x.GetType(),y.GetType, z.GetType, a.GetType); //x의 타입을 가져옴
      //result : System.Double  System.String  System.Int32 System.String 
  }
}```
Object와 var의 차이점 
- object : 중간에 다른 타입의 값도 받을 수 있음
- var : 타입이 다르면 명시적으로 해주어야 함
_.GetType : 변수의 자료 타입을 알려주는 메소드
