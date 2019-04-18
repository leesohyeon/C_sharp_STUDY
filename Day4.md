# 4일차 C# 공부
갑자기 작성하려는데 oh no 떠서 재부팅했다... 

## 주석문, 형변환, 열거식, 기타 형식
* 주석문 : /*  */ 여러줄 주석 처리, // 해당 라인 주석처리
* 형변환 : 
* 열거식 : (보통 클래스 안 쪽, 메인 함수 바깥 쪽에 선언 / element들로 작성하며 ,로 구분함)

```c#
class Program 
{
  enum Human { Warrior, Wizard, Thief }
  static void Main(string[] args)
  {
    Console.WriteLine(Human.Wizard); // 내부적으로 Wizard가 1로 세팅
    Console.WriteLine((int)Human.Warrior); // int형으로 형 변환을 하면 0으로 출력
    Console.WriteLine(Human.Thief);
  }
}
```

```c#
// 여기서 enum 내에 값을 바꿔 출력할 수 있다!
enum Human { Warrior, Wizard = 55, Thief }
...
  {
    Console.WriteLine(Human.Wizard); 
    Console.WriteLine((int)Human.Warrior); // 56
    Console.WriteLine(Human.Thief);
  }
  ```
  
---

```c#
var x = 55; // 알아서 컴파일 내에서 int로 인식
// var x = -55.7; // 알아서 컴파일 내에서 double로 인식
var y = "MIRIM LEE";
var z = 19;

Console.WriteLine(x);
/* 반드시 var 키워드의 변수를 선언할 때 초기화가 같이 이루어져야 한다 !!! */

Console.WriteLin("{0} {1} {2}",x ,y ,z); // 55 MIRIM LEE 19
// 한 번에 출력

Console.WriteLin("{0} {1} {2}",x.GetType() ,y.GetType() ,z.GetType());
// System.String System.Double System.String System.Int32
```

---
매우매우 졸립고 자고 싶은 마음이 1등이지만 그래도 참아본다


