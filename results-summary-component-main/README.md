# 23.07.07 학습일지

## 1. layout - flexBox

### 🧐 고민상황
- 전체 wrapper, result content 가 담긴 wrapper, summary content가 담긴 wrapper를 생성하고 flex를 사용하여 가로정렬을 적용하였음.

- 예제에서는 result content가 공중에 띄어진 것 처럼 보이기 때문에, 레이아웃 배치가 고민되는 상황임.



## 2. em or rem

### ✏️  상속과 크기에 대한 개념부족
- em ,rem 과 같이 단위에 대한 개념이 부족하여 px단위로 작업하고 있음.
- 상속 개념을 학습 후에 리팩토링을 해볼 예정

## 3. 작업현황
<img width="512" alt="image" src="https://github.com/TEAM-HI25/nonamarket/assets/89332492/7714df7a-fa94-41be-bb05-8208df4b237d">

<br>

# 23.07. 12 학습일지

## 1. align-items

- list container 내부에 있는 contents를 세로축으로 가운데 정렬를 하고자 한다.
<img width="271" alt="image" src="https://github.com/mixnuts211/Practice-basic-everyday/assets/89332492/9c74b891-6dd9-48c1-a697-d75a6662e60f"> <br>
위 img 처럼 상단에 쏠려 있는 contents를 가운데로 정렬하고자 함.
- list container 에 [**display:flex**] 를 적용하고 align-item 프로퍼티를 적용하여 내부 콘텐츠들을 세로축으로 중앙정렬을 적용하기 위해 center 속성을 적용.
<img width="273" alt="image" src="https://github.com/mixnuts211/Practice-basic-everyday/assets/89332492/8d2fa751-a01f-48fb-8d56-91f1902cd4d3"> <br>
- align-items의 default 속성은 stratch 로 컨테이너에 맞게 크기가 늘어남. center 을 적용하여 세로축 중앙정렬 하였음.
- 이외 적용 가능한 속성은 flex-start, flex-end, baseline 이 있다.

## 2. div 용도
- 시맨틱한 태그, 웹접근성을 고려한 마크업, 웹 표준을 위한 마크업 에 대한 마크업을 작성할 때, div 태그 사용에 대한 막연한 거부감이 있었으나, 새로운 방법론에 대해 논의하게 되었음.

- 콘텐츠에 특별한 의미가 있거나, 용도가 명확한 콘텐츠의 경우 div를 사용하게 된다면 의미 없는 마크업이 될 수 있으나, 레이아웃(또는 디자인을 위한)을 위해 사용될 경우, 웹 표준에 부정적인 영향을 끼치지 않는다고 볼 수 있음. 단순한 레이아웃과 구도를 위해 사용(wrapper or container 성질을 띄는 것)된다면 거부감을 갖지 않고 써도 된다라는 의견을 들을 수 있었음.  

- 웹표준을 준수하기 위해 또는 웹접근성을 위해 시멘틱한 태그업을 고려하는 경우에도 왜 해당 방법론을 유지하고 작성하려 하는지 생각해볼 필요성을 느낄 수 있었음.
 

 ## 3. nth-child, nth-of-type
 - 가상 선택자를 활용하여 반복되는 list에 별도의 아이콘을 넣어주기 위하여 가상선택자를 활용하였음.
 - span:nth-child(N) == span태그 내부 자식요소 중 N번째 태그
 - span:nth-of-type(N) == N 번째 있는 span요소 선택 <br>
    ```css
    .summary-list-text::before {
    content: "";
    position: absolute;
    display: inline-block;
    background: no-repeat center left / contain;
    left: -20px;
    top: 1px;
    width: 15px;
    height: 15px;
    }
    .summary-list:nth-child(1) .summary-list-text::before {
    background-image: url(./assets/images/icon-reaction.svg);
    }

    .summary-list:nth-child(2) .summary-list-text::before {
    background-image: url(./assets/images/icon-memory.svg);
    }

    .summary-list:nth-child(3) .summary-list-text::before {
    background-image: url(./assets/images/icon-verbal.svg);
    }

    .summary-list:nth-child(4) .summary-list-text::before {
    background-image: url(./assets/images/icon-visual.svg);
    }
    ```
    공통으로 적용될 프로퍼티를 작성 하고 nth-child 를 활용하여 별도의 아이콘을 삽입 하였음.