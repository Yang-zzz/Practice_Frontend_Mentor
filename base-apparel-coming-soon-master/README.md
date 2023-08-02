# 학습일지

## white-space

```
// 수정 전
          <h2 class="notice-title">
            we're
            <strong>commingsoon</strong>
          </h2>

```

- .notice-title 의 strong 태그의 text value가 viewport withd 값이 줄어들 때, 줄바꿈이 일어나지 않고 고정되어 있었음.

```
// 수정 후
          <h2 class="notice-title">
            we're
            <strong>comming soon</strong>
          </h2>

```
- 단어단위로 띄어쓰기를 하였더니 줄바꿈되었음.
- white-space 프로퍼티의 defualt 값은 normal로 요소안에서는 연속된 띄어쓰기, 들여쓰기, 줄바꿈 문자가 모두 무시된다.
- 해당 요소의 텍스트가 너무 길어서 부모요소의 withd 값이 넘어 갈 때, 자동으로 줄바꿈이 일어나지만, 수동으로 바꿀 수 없다.
