javascript 문법
=======

- 변수와 자료형

  a. 자료형 
  
    내부적으로는 Primitive(기본형)과 Object(객체형)이 있으며 각각 다음과 같다.
    
    #Primitive
    
      Boolean: true, false
      null: 빈 값을 표현
      undefined: 값을 할당하지 않은 변수가 가지는 값
      Number: 숫자형으로 정수와 부동 소수점, 무한대 및 NaN(숫자가 아님) 등
      String: 문자열
      
    #Object
    
      Reference 타입
      클래스 뿐만 아니라 배열과 함수, 사용자 정의 클래스도 모두 Object
      JSON(Java Script Object Notation)의 기본 구조
      
  b. 변수 선언
    
     변수이름은 대소문자를 구별
     여러 변수를 한번에 선언할 수 있음
     지역변수와 전역변수가 있다.
     기본적으로 소문자로 시작되는 Camel Case를 사용
     
     #var, let, const
     
      var는 지역변수 개념으로 함수 범위에서 유효함
      var를 선언하지 않으면 자동으로 전역변수가 됨
      let과 const는 ES6 에서 등장한 block-scoped 변수 선언
      let은 값의 재할당이 가능하고 const는 불가능(immutable)
      const로 선언된 배열이나 객체의 경우 새로운 객체로 재할당하는 것은 안되고, 배열값의 변경/추가, 객체의 필드 변경등은 가능하다
     
      var
      
     ![image](https://user-images.githubusercontent.com/80931911/112603276-21301e80-8e58-11eb-8789-f64b148a7b9d.png)

      let, const
      
     ![image](https://user-images.githubusercontent.com/80931911/112603314-2db47700-8e58-11eb-8e07-b71c0ee6389e.png)
      
     #hoisting
      
      호이스팅은 끌어올리기라는 사전적 의미를 가지고 있다. 자바스크립트에서 모든 변수 선언은 호이스트 되고 함수의 경우 선언형식은 호이스팅 되며 변수에 할당된 형태는 호이스팅 되지 않는다.
    
      자바스크립트 변수에 있어 변수의 선언이 위치와 상관없이 최상위 레벨로 끌어올려진다고 이해할 수 있다.
      
     ![image](https://user-images.githubusercontent.com/80931911/112604766-dfa07300-8e59-11eb-8076-19f898137950.png)
      
      일반적인 언어인 경우 foo 변수는 첫번째 출력문에서 선언되기 전 상태로 에러가 발생해야 함
      자바스크립트는 var foo가 호이스트 되어 변수는 선언되고 값이 할당되지 않은 상태가 됨
      
     ![image](https://user-images.githubusercontent.com/80931911/112605142-52115300-8e5a-11eb-92c2-2701cfd5576b.png)
      
      
      위 예제에서는 myVar라는 변수를 먼저 선언한 상태에서 동일 이름의 함수를 정의 
      함수 선언이 호이스팅 되어 myVar변수에 할당
      
      경우에 따라 호이스팅은 사소한 문제를 일으키지 않아 유용할 수 있으나 복잡한 코드에서는 오류가능성이 높으므로 변수선언시에는 var, let, const등을 명확히 구분해 사용해야 한다.
      
   
     #String 변수
     일반적인 프로그램언어들은 문자열을 표현할때 큰따옴표를 사용하는데 반해 자바스크립트는 "", ''를 모두 사용할 수 있다.
     
     ![image](https://user-images.githubusercontent.com/80931911/112606229-791c5480-8e5b-11eb-8ca6-e0b524b6383c.png)
     
  c. 출력문
    
    자바스크립트는 HTML 문서를 통해 웹브라우저에서 출력되므로 따로 출력문이 존재한다기 보다는 HTML문서의 구성요소에 동적으로 출력하거나 웹브라우저의 경고창을
    이용해 출력하는 형태가 출력문으로 볼 수 있다. 물론 웹 브라우저의 콘솔창을 통해 특정 메시지를 출력할 수 있다.
    
    #HTML 문서에 출력
      
      HTML문서에 출력하는 형태로 페이지가 모두 로딩된 다음에 실행하면 원래 있던 HTML화면내용은 지워지게 된다.
     
![image](https://user-images.githubusercontent.com/80931911/112607277-5f2f4180-8e5c-11eb-9b99-a469e90bfb7b.png)

    

     #HTML문서의 특정부분에 출력
      
      HTML문서의 특정요소를 찾아 해당 콘텐츠를 대체해 출력한다. 자바스크립트에서 가장 보편적으로 HTML 문서를 동적으로 핸들링 하는 방법이다.
      
   ![image](https://user-images.githubusercontent.com/80931911/112607566-b2a18f80-8e5c-11eb-8b34-f244cde2e1b7.png)
   
    #Alert창을 이용한 출력
    
      웹브라우저에서 오픈되는 조그만 경고창(alert)을 이용한 출력이다. 보통 프로그램에서 에러, 경고, 사용자 입력을 위해 많이 사용한다.
      
   ![image](https://user-images.githubusercontent.com/80931911/112607857-02805680-8e5d-11eb-8d5b-cc7aca767f0b.png)


    #브라우저 콘솔창을 이용한 출력
      
      자바스크립트 코드에서 진행상황을 출력하거나 개발을 위해 참고하기 위한 값들을 출력하기 위한 용도로 사용한다.
      
   ![image](https://user-images.githubusercontent.com/80931911/112608040-3491b880-8e5d-11eb-8232-09bbffb939b9.png)
   
   
  d. 연산자와 제어문
    
    일반적인 프로그램 언어와 같이 자바스크립트도 다양한 연산자와 if, for와 같은 제어문을 가지고 있다.
    
  #연산자
    
    기본적으로 다른 프로그램 언어들과 유사하다.
    
    *비교 연산자
      
      비교연산자의 결과는 기본적으로 true/false 이다
      
   ![image](https://user-images.githubusercontent.com/80931911/112608583-d6b1a080-8e5d-11eb-949c-c8adedefc24c.png)
   
   *논리 연산자
   
   
   ![image](https://user-images.githubusercontent.com/80931911/112608653-e9c47080-8e5d-11eb-9b6b-ac152a2688ed.png)

  #조건문
  
    C, JAVA와 매우 유사하다. if, else, switch 등이 있다.
    
  ![image](https://user-images.githubusercontent.com/80931911/112608960-4de73480-8e5e-11eb-8664-9d21097b7fb4.png)
  
  #반복문
  
    반복문 역시 C, JAVA와 유사하다. for, while, forEach, for-in, for-of-for 등이 있다.
    
  ![image](https://user-images.githubusercontent.com/80931911/112609242-aa4a5400-8e5e-11eb-9707-a630d75ee2ba.png)
  
  ![image](https://user-images.githubusercontent.com/80931911/112609314-bfbf7e00-8e5e-11eb-892f-5a8814f6ce56.png)
  
  ![image](https://user-images.githubusercontent.com/80931911/112609351-ca7a1300-8e5e-11eb-9b5e-693d0f95283d.png)

  
  e. 배열과 자료구조
  
    #배열
      
      배열의 선언은 []나 new Array()로 생성하고 크기의 제약이 없으며 하나의 배열에 서로 다른 타입의 변수가 들어갈 수 있다.
      
   ![image](https://user-images.githubusercontent.com/80931911/112609607-12993580-8e5f-11eb-9fda-7530ff070a50.png)
   
   
      배열에 자바스크립트 객체를 넣을 수 있다. 이를 이용하면 JSON 데이터의 집합을 만들 수 있으며 서버와의 데이터 교환에 사용할 수 있는 구조가 된다.
      
   ![image](https://user-images.githubusercontent.com/80931911/112609751-42483d80-8e5f-11eb-9cf9-5022872f343e.png)

   ![image](https://user-images.githubusercontent.com/80931911/112609817-5a1fc180-8e5f-11eb-94a9-1ae7bd87b7da.png)

    #Map, Set
    
      ES6에서 새롤게 추가된 자료구조이다. 기존 자바스크립트는 배열 이외의 자료구조가 따로 없었으나 이제 다른 언어들 처럼 다양한 자료구조를 사용할 수 있다.
      
      *Map
        
        Map은 new Map()으로 선언 하고 map.set()을 이용해 키와 값을 추가한다.
        
        자바스크립트의 Map은 Key.Value 쌍으로 구성된 Object와 비슷한 구조로 볼 수 있지만 다음과 같은 차이가 있다
          
            - Object의 키는 문자열이며, Map의 키는 모든 값을 가질 수 있다.
            - Object는 크기를 수동으로 추적해야하지만, Map은 크기를 쉽게 얻을 수 있다.
            - Map은 삽입도니 순서대로 반복된다.
            - 객체(Object)에는 prototype이 있어 Map에 기본 키들이 있다.

![image](https://user-images.githubusercontent.com/80931911/112610465-14172d80-8e60-11eb-8b1e-9e6a8babb46a.png)

  
    #Set
      
      Set은 중복된 값을 허용하지 않고 입력된 순서에 따라 데이터를 저장하는 자료구조이다. set.add()를 이용해 데이터를 추가할 수 있고 데이터 관리를 위한 메서드가 제공된다.
      
      배열과 유사하지만 다음과 같은 차이가 있다.
        
        - indexOf()를 사용하여 배열내에 특정 요소가 존재하는지 확인하는 것은 느리다.
        - 배열에선 해당 요소를 배열에서 잘라내야 하는 반면 Set은 삭제 기능을 제공한다.
        - NaN은 배열에서 indexOf 메서드로 찾을 수 없다
        - Set객체는 값의 유일성을 보장하기 때문에 직접 요소의 중복성을 필요가 없다.

![image](https://user-images.githubusercontent.com/80931911/112611184-d961c500-8e60-11eb-8655-35582cc65634.png)


  f. 함수(Function)
  
    함수의 개념은 대부분의 프로그램 언어에서 존재하지만 특히 자바스크립트는 함수를 변수에 할당할 수 있으며 인자로 함수를 전달하거나 콜백함수를 구현하는 형태 등 
    
    다양한 함수 활용을 보여주고 있다. 이러한 특징들과 함께 최근의 함수형 프로그래밍(FP: Functional Programming) 개념도 자바스크립트에서 지원되고 있다.


![image](https://user-images.githubusercontent.com/80931911/112611627-6c9afa80-8e61-11eb-9598-2e108c07fa88.png)

![image](https://user-images.githubusercontent.com/80931911/112611688-7e7c9d80-8e61-11eb-8d9f-8f9b60792398.png)

![image](https://user-images.githubusercontent.com/80931911/112611713-86d4d880-8e61-11eb-94e2-cbe649806a5e.png)



  g. 객체와 클래스 
  
    
![image](https://user-images.githubusercontent.com/80931911/112611900-b1bf2c80-8e61-11eb-890f-21d2c9c75049.png)


![image](https://user-images.githubusercontent.com/80931911/112612067-d915f980-8e61-11eb-915b-87242a1a1970.png)

![image](https://user-images.githubusercontent.com/80931911/112612100-e4692500-8e61-11eb-8a5b-25f0b4d21681.png)

![image](https://user-images.githubusercontent.com/80931911/112612144-edf28d00-8e61-11eb-8729-3361cf17efee.png)

![image](https://user-images.githubusercontent.com/80931911/112612180-f6e35e80-8e61-11eb-935b-01fe4e4f8e2b.png)






     
      
