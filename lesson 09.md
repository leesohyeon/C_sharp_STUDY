* 삼항 : (조건식) ? (조건식이 true일 때) : (조건식이 false일 때)
 세가지의 피연산자를 가짐
 ```C#
 int x = 5;
 int y = 7;
 int z;
 z = (x>y) ? x : y;
 Console.WriteLine(z);  //7
  string a;
 a = (x>y) ? "x가 큰 수" : "y가 큰 수";
 ```
  * 논리 : !, &&, ||
  참, 거짓으로 리턴
 ```C#
 bool b;
  Console.WriteLine("{0} {1}", !false, !true);   //True False
  b = (x != y && x < y);  //&&는 양쪽 다 true일 때 true 반환
 Console.WriteLine("{0} {1} {2}", (x != y), (x < y), b);  //true true true
  b = (x != y || x > y); 
 Console.WriteLine("{0} {1} {2}", (x != y), (x > y), b);  //true false true
  ```
  - && 논리 AND연산 : 양쪽 모두의 값이 true이면 true 반환, 하나라도 false면 false반환
  - || 논리 OR연산 : 양쪽 중 한쪽 값만 true면 true 반환(양쪽 다 true이면 전체가 true), 둘 다 false면 false반환
