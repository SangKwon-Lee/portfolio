부모에 상관없이 조절 ->vh
//////
\*display: flex : 자동으로 왼쪽~오른쪽으로 정렬
flex-direction : 기본값은 row // 왼쪽~오른쪽 방향
reverse : 가능

\*flex-wrap
nowrap :한 줄에 아이템이 꽉 차도 다음 줄로 넘어가지 않음 // 기본값
wrap : width가 줄어들면 자동으로 다음 줄로 넘어감

\*flex-folw : wrap과 directio을 한 번에 설정
column nowrap 이렇게

\*justify-contnet : 중심축에서 아이템들을 어떻게 배치할지 결정해줌
flex-start : 기본값 왼쪽~오른쪽으로 정렬
flex-end : 순서는 그대로, 하지만 오른쪽에 붙어서 정렬
center : 가운데
space-around : 박스를 둘러싸게 spacing을 넣어줌
space-evenly : spacing을 모두 똑같은 간격
space-between : 제일 왼쪽 오른쪽만 맞추고 중간에 spacing을 넣음

\*align-items : 반대축에서 아이템들을 배치하는 속성
center : 수직적으로 중간에 둠
baseline : item 요소에서 중간으로 맞춤

\*align-content : 반대축의 아이템들을 지정해둠
space-between : 위 와 아래는 각 변에 딱 붙은 상태에서 동등한 space를 줌
center : 모두 중간 배치

*flex-grow : 컨테이너를 꽉 채우려고 아이템들이 늘어남 기본값은 0
*flex-shrink : 컨테니너가 점점 작아졌을 떄 어떻게 행동하는지 정해줌 기본값은 0
\*flex-basis : 아이템들이 공간을 얼마나 차지해야 하는지 도와줌. 기본값은 auto로, grow와 shrink에 맞춰짐 %로 값을 주면 됨. 굉장히 유용

\*align-self : 아이템 별로 아이템들을 정렬할 수 있음 하나만 center로 주거나 다른 값을 줄 때

font-family: 'Open Sans', sans-serif;


//////
position: relative
-> 얘는 원래 있던 위치에서 우리가 지정해준 만큼 움직이는 녀석이다.
ex) top:30px; left:30px;
이렇게 하면 같은 컨테이너에 있던 다른 아이템은 자리는 그대로지만,
우리가 지정해준 녀석만 바뀌게 된다.
원래 자기 자리를 찜해두고 이동하는 것과 같음

position: absolute
얘는 자신의 부모를 기준으로 가게 된다.
만약 부모가 기본 값인 static이라면 무시하고 다시 부모를 찾는다.
그래서 모든 부모가 static이면 body에 맞춰지게 된다.

만약 얘를 쓰려면 container를 relative로 하게 되면 이녀석을 중심으로 움직이게 된다.
그리고, 자기 자리를 벗어나 위치가 재조정되기 때문에 다른 아이템들의 위치가 변하게 된다.


//////
position: fixed
-> 바디에서 항상 고정

position: sticky
본인의 자리를 유지하면서 스크롤 내릴 때만 부모 컨테이너 안에서 고정


//////
flexbox가 아닐 때 정렬하는 것
1. margin : auto
   div는 블록이라 한 줄을 다 차지한다.
   div의 길이를 제외한 나머지 공간은 자동으로 margin을 넣어준다. 보통은 오른쪽에 있다.
   그래서 auto를 하면 자동으로 가운데 맞춤이 된다. 많이 쓰는 방법.
   다만, 한 줄에 하나만 들어가기 위한 아이여서 수평적으로만 중간 정렬이 가능하다.
   수직은 x

2. text-align : center
   텍스트 말고 다른 애들도 정렬이 가능.
   텍스트가 아니더라도 다른 요소들을 중간에 정렬이 가능하지만 블록개념으로 1개만 있으면 마진 때문에 안된다.
   그래서 margin auto를 다시 줘야 한다.
   button같은 하나만 있어도 얘로 정렬이 가능

3.transform: translate(50%, 50%);
x에서 50%, y에서 50%주는 것

4. text-align:ceter
   text를 수평에서 가운데 주는 녀석
   line-height:를 부모상자의 높이만큼 주면 수직 정렬도 가능하다.
