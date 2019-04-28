# 8일차 C# 공부
마저 못한거 다시 시작합니당

> 메소드 (Method)
* 객체 지향 언어(OOP)에서 사용되는 용어
* return (메소드가 끝남과 동시에 메소드가 호출된 위치에 값 전달)
* Recursive call

```c#
class Dog
{
  public static void Eat()
  {
    Console.WriteLine("냠냠");
  }
  
  public static void sleep() 
  {
    Console.WriteLine("쿨쿨");
  }
}


class Chap0428
{
  public static void Nice()  // 캡슐화와 관련된 접근지시어
  {
    Console.WriteLine("C# 재밌다!");
  }
  static void Main(string[] args) 
  {
    Chap0428.Nice(); // C# 재밌다!
    Dog.sleep(); // 쿨쿨
  }
}
```

### 매개변수 값 전달하기
```c#
class Dog
{
  public static void Eat(string food)
  {
    Console.WriteLine(food + " 냠냠");
  }
  
  static void Main(string[] args) 
  {
    Dog.Eat("사료"); // 사료 냠냠
    Dog.Eat("간식"); // 간식 냠냠
  }
}
```

### return 문 사용하기
```c#
class Dog
{
  public static string sleep() 
  {
    return "쿨쿨";
  }
  
  static void Main(string[] args) 
  {
    Console.WriteLine(Dog.Sleep()); // 쿨쿨
  }
}
```





