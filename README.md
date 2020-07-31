## :two_men_holding_hands: ​부캠나우(나우누리) (20200731 - v1.0.0)

### :pushpin: 나우누리 소개

- 나우누리는 1994년 서비스를 개시했으며 **2013년 1월 31일 서비스**가 종료되었다. 천리안과 하이텔에 이은 대형 BBS로 인터넷이 지금과 같이 발전하지 못했던 시절, 몇 안되는 정보 **교류의 장** 역할을 수행함으로써 한 때 수백만에 이르는 많은 회원을 거느렸으며 **다양한 게시판 및 동호회가 운영**되었다.

  ![나우누리2](https://user-images.githubusercontent.com/33643752/89039259-b1c36700-d37c-11ea-927e-0b650ebf6969.gif)

- 당시는 예절이 지켜지는 아름다운 시절로 요즘처럼 초딩들이 날뛰는 모습은 볼 수 없었다. **나우지기**들이 열심히 모니터링을 하였기 때문이다. 또한 여러 대학들과 제휴하여 <u>사이버캠퍼스</u>를 운영하여서 **대학생**들도 많이 이용하였다.

- 웹으로 넘어와서 나우누리의 가장 강력한 세일즈 포인트는 **동호회 자료실**이었다. 당시 나우누리의 자료실 소스는 어느 인터넷 서비스도 쫓아올 수 없는 서비스량을 자랑하고 있었고, 내심 유료 서비스로도 사용자들의 충성도를 유지할 수 있으리라 생각했나 보지만 결과는 시궁창이었다.

  

  ![나우누리](https://user-images.githubusercontent.com/33643752/89039227-a40de180-d37c-11ea-889d-6ab1dab66a1b.jpg)

  

### :closed_book: 만들 서비스 소개

- 기존의 클린 했던 나우누리의 상황을 재현 하기 위한 **A: 욕설 필터링 기능**과 현재 존재하는 다른 커뮤니티와의 차이를 만들기 위해서 **B: 둘 중 하나, C: 유저 추천** 기능을 추가하였다.

- 여기서 **둘 중 하나** 기능은 유저의 유치를 위한 재미 요소로 추가하였다.

  

### :man: 서비스 대상

- 부스트 캠퍼와 스태프, 마스터님



### :book: 일반 서비스 제공 요구사항 명세

| 구분  | 요구사항                                                     | 산출물                                                     |
| ----- | ------------------------------------------------------------ | ---------------------------------------------------------- |
| 2주차 | - 댓글 기능이 구현된 게시판(코딩, 아재개그, 운동, 음악, 역사, 맛집, 음주 등)<br />- 관심사(코딩, 운동, 음악, 역사, 맛집탐방, 음주 등) | 게시판 페이지                                              |
| 3주차 | 회원가입 - 받을 데이터(아이디, 패스워드, 닉네임, 관심사)<br />로그인 - 예시) Session, Cookie<br />프로필수정 | 회원가입 페이지<br />로그인 페이지<br />프로필 수정 페이지 |
| 4주차 | 메인화면 구현(전체적인 디자인 수정), 게시글의 좋아요(하트) 기능 | 메인화면 페이지                                            |



### :book: 인공지능 서비스 제공 기능 명세

| 구분   | 기능명      | 설명                                                         |
| :------: | :-----------: | ------------------------------------------------------------ |
| 기능 A<br/>(주) | 욕설 필터링 | **욕설, 비방을 걸러주는 기능** [[참조](https://github.com/hjh010501/appropriate-filetering)]<br />게시판과 댓글에 올라오는 스팸이나 욕설/비방을 필터링 해주는 것입니다.<br />욕설에 해당하는 문자는 *로 표기합니다. |
| 기능 A<br/>(서브) | 읽음이      | **CSS 서비스를 통해 글 읽어주는 서비스** [[참조](https://www.ncloud.com/product/aiService/css)]<br />다중 작업을 하는 동안 글을 귀로 들을 수 있다. |
| 기능 B<br/>(주) | 둘 중 하나  | **teachable machine을 통한 1:1 비교** [[참조](https://teachablemachine.withgoogle.com/train)]<br /><br />자신의 이미지나 웹캠을 통한 얼굴을 업로드하고 그에 대한 결과값을 출력해주는 것입니다.<br />teachable machine을 통해 여러 장의 이미지를 학습합니다.<br />예제) 사자와 토끼를 학습시키고 사용자가 얼굴을 등록하면 웹 페이지에 "당신은 사자와 더 닮았습니다(73%)"<br />이런식으로 출력해줍니다. (사자, 토끼), (아이유, 아이린) 등 누구와 내가 더 닮았는지 다양한 경우를 제공합니다. |
| 기능 B<br/>(서브) | 감정 이모지 | **얼굴인식을 통한 이모지 만들기** [[참조](https://www.ncloud.com/product/aiService/cfr)]<br />셀카를 올리면 얼굴을 가려지기 원하는 사람은 얼굴이 이모지로 대체가 된다.<br />쉽게 프로필 사진이라고 생각하면 됩니다.<br />제공해드린 링크를 보시면 표정에 대한 결과값이 제공되고 그에 맞는 이모지를 프로필로<br />설정해주시면 됩니다. |
| 기능 C<br/>(주) | 유저 추천   | **활동이나 관심사기반으로 그룹이나 유저를 추천해주는 기능**<br />Recommendation 기본 알고리즘에 대해서 검색<br />유저를 추천해주는 것에서 친구 추가나 쪽지에 대해서는 고려하지 않는다. |
| 기능 C<br/>(서브) | 게시글 추천 | **예상 조회수나 추천수를 예측하는 기능**<br />게시글의 메타데이터들을 모아서 글의 길이, 이미지 개수를 고려해 조회수와 추천수를 예측한다. <br />실제 있는 게시판에서 정보를 긁어와 학습하는 것도 좋을 것 같다. |

- 각 주차별 팀은 주 기능이 힘들 시 서브 기능을 구현할 수 있다.

### UI 설계
- [UI 설계도](https://docs.google.com/presentation/d/10_LDhi5gE6HRMyb9G11cD4XZKgyufq62Za5Njs0RkBU/edit#slide=id.g86ac92521f_0_10)
