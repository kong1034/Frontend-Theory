## 옵저버 패턴<br/>
<br/>
 
하나의 인스턴스에서 이벤트를 감지하고 해당 이벤트에 대한 알림을 해당 인스턴스에 추가된 객체한테만 알려주는 기법이다.<br/>
조금 더 쉽게 이해하기 위해서 하나의 그림을 가져왔다.<br/>
<br/>
![7F52FC9F-4F1C-46FE-823E-088912C3831C](https://github.com/kong1034/Frontend-Theory/assets/19910034/c0b0940f-1073-4d2a-b016-dfc15675d544)<br/>


유명 빵집을 구독한 사람들에게만 유명빵집의 이벤트를 알려주고 구독하지 않은 사람들에게는 이벤트를 알려주지 않는 이 시스템이 옵저버 패턴과 동일하다.<br/>
<br/>
<br/>
- 장점<br/>
1. 결합으로 인해 시스템이 유연해진다.<br/>
2. 실시간으로 변경사항을 공유할수있다.<br/>
<br/>
<br/>

- 단점<br/>
1. 남발하게되면 관리가 힘들어진다.<br/>
2. 순서를 제어할수없다.<br/>
3. 객체를 만든 이후에 없애지 않는다면 메모리 누수가 발생한다.<br/>

- 코드<br/>

<img width="480" alt="스크린샷 2023-06-27 오후 6 14 25" src="https://github.com/kong1034/Frontend-Theory/assets/19910034/670b2a04-1149-4135-976c-c71610fb5a56"><br/>
빵집에 대해서 이벤트들과 구독자들을 어떻게 등록시키고 해제 시킬건지에 대해서 정의한다.<br/>
<br/>

<img width="461" alt="스크린샷 2023-06-27 오후 6 17 13" src="https://github.com/kong1034/Frontend-Theory/assets/19910034/ee77df93-a55e-4660-a6e0-2faf04568ec1"><br/>
어떤 알림을 줄건지 정의한다.<br/>
<br/>

<img width="850" alt="스크린샷 2023-06-27 오후 6 22 52" src="https://github.com/kong1034/Frontend-Theory/assets/19910034/e7de8ce3-21c4-43e5-ba3d-d6ddbb7b5287"><br/>
정의 해놓은 빵집을 이제 변수에 담고 실제 정의해놓은 이벤트들을 구독자들에게 보낸다.<br/>
<br/>
<br/>
<br/>
<br/>


## 퍼사드 패턴<br/>
연계되어 실행되는 기능들을 인터페이스를 통해 하나로 만드는 기법이다.<br/>
<br/>

- 징잠<br/>
1. 하나의 인터페이스에 연계되어 실행되는 기능들을 모아두기 때문에 작업하기 편해진다.<br/>
2. 밀접한 관계일때만 공유하므로 단순화 되어 좋다.<br/>
<br/>
<br/>

- 단점<br/>
1. 유지보수 측면에서 힘이 더 들어간다.<br/>

- 코드<br/>
<br/>
<img width="382" alt="스크린샷 2023-06-28 오후 11 28 55" src="https://github.com/kong1034/Frontend-Theory/assets/19910034/03e14816-7670-42ea-90ba-c9a948ecc262">

<br/>
주문 클래스와 주문완료, 주문취소에 대한 함수를 정의해놓는다.<br/>
<br/>
<img width="493" alt="스크린샷 2023-06-28 오후 11 29 15" src="https://github.com/kong1034/Frontend-Theory/assets/19910034/2c979625-1b8a-44a4-88c5-e36371d554c3">

<br/>
인스턴스를 만들어두고 함수도 만들어둔다.<br/>
그리고 주문완료와 주문취소를 실행하게되면 위에서 정의해놓은 여러가지 기능들이 같이 실행된다.<br/>
