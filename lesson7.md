## 열거식
```C#
class Program
{
  enum Human { Warrior, Wizard=55, Thief}  //열거식 - 이름은 Human임
  //값이 첫번째부터 0으로 시작함, 중복 X
  static void Main(string[] args)
  {
    Console.WriteLine(Human.Wizard);  //Human.Wizard = 1
    Console.WriteLine((int)Human.Thief);  //result : 2
    Console.WriteLine(Human.Warrior);  //result : Warrior
  }
}
```
Wizard = 55이면 그 다음 부터는 숫자가 하나씩 증가하기 때문에 (int)Human.Thief에는 56이 나온다.

## 기타형식
```C#
class Program
{
  static void Main(string[] args)
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
}
```
Object와 var의 차이점 
- object : 중간에 다른 타입의 값도 받을 수 있음
- var : 타입이 다르면 명시적으로 해주어야 함

_.GetType : 변수의 자료 타입을 알려주는 메소드

