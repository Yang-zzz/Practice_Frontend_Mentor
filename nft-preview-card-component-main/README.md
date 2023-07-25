# 학습일지

## preview 는 어떤 태그로 마크업을해야 하나?
- product의 자세히 보기기능으로 해당 product의 자세한 설명을 볼 수 있는 modal로 인식하여 시맨틱한 마크업을 하고자 고민하였음.
- 독립적인 콘텐츠 vs 연관있는 콘텐츠로서 구분하려고함.
- product가 여러개 나열되어 있는 page에서 product를 클릭하고 해당 product의 preview가 나타난다면 해당 서비스 또는 page에서는 연관성이 높은 component 라고 판단하였음.
- article vs section -> section 태그를 사용하여 맥락에 맞는 component로 생성될 수 있도록 하고자 함.