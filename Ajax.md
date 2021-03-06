Ajax(Asynchronous Javascript And XML)
====

  AJAX란, JavaScript의 라이브러리중 하나이며 Asynchronous Javascript And Xml(비동기식 자바스크립트와 xml)의 약자이다. 브라우저가 가지고있는 XMLHttpRequest 객체를 이용해서 전체 페이지를 새로 고치지 않고도 페이지의 일부만을 위한 데이터를 로드하는 기법 이며 JavaScript를 사용한 비동기 통신, 클라이언트와 서버간에 XML 데이터를 주고받는 기술이다.

  즉, 쉽게 말하자면 자바스크립트를 통해서 서버에 데이터를 요청하는 것이다.
  
  - 비동기 방식이란?

    비동기 방식은 웹페이지를 리로드하지 않고 데이터를 불러오는 방식이며 Ajax를 통해서 서버에 요청을 한 후 멈추어 있는 것이 아니라 그 프로그램은 계속 돌아간다는 의미를 내포하고 있다.
    
  - 비동기 방식의 장점

    페이지 리로드의 경우 전체 리소스를 다시 불러와야하는데 이미지, 스크립트 , 기타 코드등을 모두 재요청할 경우 불필요한 리소스 낭비가 발생하게 되지만 
    비동기식 방식을 이용할 경우 필요한 부분만 불러와 사용할 수 있으므로 매우 큰 장점이 있다.
    
  - AJAX로 할 수 있는 것

    AJAX라는 네트워크 기술을 이용하여 클라이언트에서 서버로 데이터를 요청하고 그에 대한 결과를 돌려받을 수 있다.

  - 클라이언트란?

    서버에서 정보를 가져와서 사용자에게 보여줄 수 있고 사용자와 상호작용할 수 있는 소프트웨어를 일컫는다.
    Ex) 웹브라우저, 핸드폰 어플리케이션 등...

  - 서버란?
  
    네트워크 상에서 접근할 수 있는 프로그램으로서 어떤 자료들에 대한 관리나 접근을 제어해주는 프로그램을 말한다. 서버는 일반적으로 사용자가 직접적으로 사용하지 않는다.

  - AJAX를 사용하는 이유
  
    단순하게 WEB화면에서 무언가 부르거나 데이터를 조회하고 싶을 경우, 페이지 전체를 새로고침하지 않기 위해 사용한다고 볼 수 있다.

    기본적으로 HTTP 프로토콜은 클라이언트쪽에서 Request를 보내고 서버쪽에서 Response를 받으면 이어졌던 연결이 끊기게 되어있다. 
    그래서 화면의 내용을 갱신하기 위해서는 다시 request를 하고 response를 하며 페이지 전체를 갱신하게 된다. 하지만 이렇게 할 경우, 엄청난 자원낭비와 시간낭비를 초래하고 말 것이다.
    AJAX는 HTML 페이지 전체가 아닌 일부분만 갱신할 수 있도록 XMLHttpRequest객체를 통해 서버에 request한다. 이 경우, JSON이나 XML형태로 필요한 데이터만 받아 갱신하기 때문에 그만큼의 자원과 시간을 아낄 수 있다.

  - AJAX의 장단점
  
    1. AJAX의 장점
    
      웹페이지의 속도향상
      서버의 처리가 완료될 때까지 기다리지 않고 처리가 가능하다.
      서버에서 Data만 전송하면 되므로 전체적인 코딩의 양이 줄어든다.
      기존 웹에서는 불가능했던 다양한 UI를 가능하게 해준다. ( Flickr의 경우, 사진의 제목이나 태그를 페이지의 리로드 없이 수정할 수 있다.)
      
    2. AJAX의 단점
    
      히스토리 관리가 되지 않는다.
      페이지 이동없는 통신으로 인한 보안상의 문제가 있다.
      연속으로 데이터를 요청하면 서버 부하가 증가할 수 있다.
      XMLHttpRequest를 통해 통신하는 경우, 사용자에게 아무런 진행 정보가 주어지지 않는다. (요청이 완료되지 않았는데 사용자가 페이지를 떠나거나 오작동할 우려가 발생하게 된다.)
      AJAX를 쓸 수 없는 브라우저에 대한 문제 이슈가 있다.
      HTTP 클라이언트의 기능이 한정되어 있다.
      지원하는 Charset이 한정되어 있다.
      Script로 작성되므로 디버깅이 용이하지 않다.
      동일-출처 정책으로 인하여 다른 도메인과는 통신이 불가능하다. (Cross-Domain문제)
      
      
  - AJAX의 진행과정
  
    1.XMLHttpRequest Object를 만든다.
      request를 보낼 준비를 브라우저에게 시키는 과정
      이것을 위해서 필요한 method를 갖춘 object가 필요함
    2.callback 함수를 만든다.
      서버에서 response가 왔을 때 실행시키는 함수
      HTML 페이지를 업데이트 함
    3.Open a request
    서버에서 response가 왔을 때 실행시키는 함수
    HTML 페이지를 업데이트 함
    4.send the request
    
  - AJAX가 쓰이는 방법
  
    XMLHttpRequest 객체를 얻은 뒤, url을 통해 요청하고 응답을 받으면 응답 결과에 맞는 함수를 실행하는 구조로 되어 있다. 
    Ajax가 효율적이라고는 해도 이렇게 하게 될 경우, 코드가 길어지기 때문에 jQuery에서 그 문제를 해결해주고 있다.
    
    예시로 보는 AJAX - 1
    ```{.javascript}
    
      // This function gets invoked when server sends the response
      function reqListener (e) {
          console.log(e.currentTarget.response);
      }

      var oReq = new XMLHttpRequest();
      var serverAddress = "https://hacker-news.firebaseio.com/v0/topstories.json";

      oReq.addEventListener("load", reqListener);
      oReq.open("GET", serverAddress);
      oReq.send();
      ```
      
      
위의 예제는 자바스크립트를 이용하여 특정 서버에 요청을 보내고 그에 대한 자료를 성공적으로 받아올 수 있음을 확인해볼 수 있다. 위 예제에서는 XMLHttpRequest를 이용하여 요청을 보냈지만 일반적으로는 아래와 같이 jQuery나 기타 AJAX 기능이 내장되어 있는 라이브러리를 이용하여 AJAX 요청을 처리한다.

```{.javascript}

      var serverAddress = 'https://hacker-news.firebaseio.com/v0/topstories.json';

      // jQuery의 .get 메소드 사용
      $.ajax({
          url: ,
          type: 'GET',
          success: function onData (data) {
              console.log(data);
          },
          error: function onError (error) {
              console.error(error);
          }
      });
```
    
    예시로 보는 AJAX - 2
    
    ```{.javascript} 
    
      var xhr= new XMLHttpRequest();

      xhr. onreadystatechange = function(){
	      if(xhr.readyState===4){
    	      document.getElementById(‘ajax’).innerHTML= xhr.responseText;
          }
      }

      xhr.open(‘GET’,”sidebar.html”);  // html메소드와 URL을 보낸다. (open함수는 준비를 시키는것이지 보내는 것은 아니다.)
      xhr.send(); 
      ```
      
      
위의 예제는 AJAX가 XHR객체를 형성하고 이 객체의 콜백을 만들고 HTML메소드와 URL을 결정한 뒤, XHR객체의 메소드로 정보를 보내는 방식이다.

var xhr= new XMLHttpRequest(); : browser response를 얻었을 때 작동하는 함수 (callback 함수)
xhr.onreadystatecjange : AJAX Request에 어떠한 변화라도 있으면 작동한다. (callback 함수를 포함하고 있다고 생각하면 된다.)
xhr.readyState : response가 돌아왔는지 아닌지를 추적하는 property

