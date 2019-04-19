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

