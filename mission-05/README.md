# 과제05_sprite 이미지를 이용한 랭킹 section

## 과제 조건
- rank.png(sprite) 이미지를 활용하여 스프라이트 기법으로 스타일링.
  
- 각 인기 사이트의 순위를 나타내는 영역은 기존 ol 요소에서 제공하는 기본 숫자를 보이지 않도록 한 후 CSS로 구현.


## 과제 내용

- 마크업 순서는 이미지 파일 첨부


단, a.more 태그는 가장 마지막에 마크업 하였음.

- 더보기 태그는 왼쪽 위로 올리기 위하여 section에 position: relative를 주고 더보기 a 태그에 position: absolute를 주어 위치를 조정함.

- 인기 사이트 중 '사이트' 부분은 색상을 달리하기 위하여 span으로 묶어주었음.

- ol 태그에서의 기본 list-style은 none을 주었음. 그리고 listItem에 가상 요소 ::before를 넣어 스타일링을 하였음.

```
.site__ListItem {
  counter-increment: number;
}

.site__ListItem::before {
  content: counter(number);
  padding: 3px 6px;
  background: #A3A3A3;
  border-radius: 5px;
  color: #fff;
}
```

- 오른쪽 순위 변동 아이콘은 sprite 이미지를 이용하여 listItem에 background로 설정하였음. 이후 background-position을 주어 특정 이미지들이 위치에 알맞게 갈 수 있도록 하였음.

```
.site__ListItem {
  background: url(./rank.png) no-repeat;
  background-position: 100%;
}

.site__ListItem:first-child, .site__ListItem:last-child {
  background-position: 100% -11%;
}

.site__ListItem:nth-child(3) {
  background-position: 100% 101%;
}
```



## 완성 이미지

