# 과제 04_grid를 이용하여 새소식 section 만들기

## 과제 조건
- grid를 활용하여 레이아웃을 구현한다.


---

## 과제 내용

- 마크업 순서

<img width="551" alt="스크린샷 2023-06-12 오후 5 07 12" src="https://github.com/Sirori/home-work/assets/116864776/f24aeb1b-75e5-4c79-b160-35663c516150">

newsContents__txt 이하에는 각각

```
h3.newsContents__title,
span.date,
p.newsContents__contents>a 
```
로 클래스명을 부여함

<br>

- 구분선을 주기 위하여 .news에 position:relative를 주고 ::after를 생성하여 배치함
  
```
.news::after {
  position: absolute;
  content: '';
  background: linear-gradient(to right, #A9A9A9, #FFFFFF);
  width: 70%;
  height: 1px;
  top: 15%;
  left: 0;
}
```

<br>

-grid를 사용하여 가로 세로를 각 6:3 비율로 나누고 해당 콘텐츠들을 배치하였음

```
.newsContents {
  display: grid;
  grid-template-areas:
  "img img title title title title"
  "img img cont cont cont cont"
  "img img cont cont cont cont"
  ;
}

.newsContents__fig {
  grid-area: img;
}

.newsContents__txt {
  grid-area: title;
}

.newsContents__contents {
  grid-area: cont;
}
```

- 더보기 버튼은 임의로 font-weight를 조정하여 a 태그임을 명시하였음.

<br>

---

## 완성 이미지



<img width="478" alt="스크린샷 2023-06-12 오후 5 31 17" src="https://github.com/Sirori/home-work/assets/116864776/2953746d-d814-4418-b1d9-9a5c0a994192">
