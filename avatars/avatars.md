# 20240504 과제 - avatar

### [ 과제 요구사항 ]
- 아바타 이미지는 배경 방식이 아닌 콘텐츠 이미지(<img> 요소)로 마크업한다.

- 아바타의 상태 정보를 알 수 있도록 정보를 제공한다.

- 아바타 이미지의 크기 - 64px X 64px

- 아바타 이미지 간의 간격 - 20px

- 회색 원 배경색 - #DBDBDB

- 초록색 원 배경색- #4CFE88

- **float**를 사용하여 레이아웃을 구현한다.

- **flex**를 지원하는 환경에서의 레이아웃 또한 구현한다.
(float 레이아웃과는 아이템 순서가 다르다.)


***
### [ 과제 해결 방법 ]

> #### HTML 마크업 
>> 1. 8개의 img 요소와 접속 여부를 나타내는 span 요소를 감싸는 용도로 &lt;div&gt; 요소를 활용, 'avatars-container'라는 class 이름을 지정하였다.
>> 2. span 요소의 경우, online/offline 상태를 파악해야 하므로 class 이름을 따로 부여했다. 
>> 3. 접근성을 고려하여 span 요소에 'aria-label' 속성을 부여하였다.
<br><br>

<br>

> #### CSS 스타일링 
>> 1. 과제 이미지에 있는 배경 색상은 개발자 도구의 스포이트 기능을 활용해 색을 추출했다. 
>> 2. 'position', 'transform' 속성을 활용하여 avatars-container를 화면 중앙에 배치하였다. (중앙 정렬에 대해서 더 학습해야 할 것 같다.)
>> 3. float를 활용하면 레이아웃이 무너질 수 있으므로 부모 요소인 avatars-container에 가상 요소 'after'를 사용해서 문제를 해결하려 했다.
>> 4. img 요소를 부모 요소에 딱 맞게 위치시키기 위해 'width' 속성을 100%로 설정하였다.
>> 5. flex를 지원하는 웹 브라우저를 위해 @supports CSS 조건부 규칙을 사용했다. 
>> 6. nth-child() 선택자를 사용하여 img 순서를 조정했다.
<br><br>

<br>

***

### [ 느낀 점 ]

HTML, CSS 선행학습을 했지만, 실습을 많이 해보지 않아서 머리로만 아는 상태이다. 특히나 float의 경우, 사용 방법이 아직 어색해서 float 레이아웃 구현 연습이 많이 필요할 것 같다. 그래도 position으로 요소를 배치하는 건 어느 정도 이해가 되어서 흥미롭게 느껴진다. 처음엔 과제 요구사항에 나와있는 결과 화면만 보고 간단한 과제라고 생각했지만 아니었다^^ 요구사항에 맞게 구현을 잘 한 건지는 모르겠지만 화면에 결과가 나온 것에 만족한다. 이번 과제를 하면서 HTML/CSS에 대해 너무 애매하게 알고 있다는 것을 깨달았다. 실습 많이 해야겠다.  