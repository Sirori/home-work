# 과제03_hover 애니메이션을 활용한 목록 만들기

## 과제 조건
- 링크 목록은 5개이며 CSS를 사용하여 화면에 1개의 목록만 보이도록 구현
- 목록에 마우스를 올리면 5개의 목록이 펼쳐지도록 구현
- transition 속성을 활용하여 애니메이션 효과를 적용

<br>

---

## 과제 내용

- 마크업 순서는 이미지로 대체함.
  
<img width="318" alt="스크린샷 2023-06-11 오전 12 01 31" src="https://github.com/Sirori/home-work/assets/116864776/d90f43ec-fa5e-43df-acdd-2588a73b260a">

siteTitle 에서의 '사이트'는 색상이 다르기 때문에 span으로 묶어 해당 색상으로 설정하였음.

<br>

- padding값을 주면 overflow되는 것을 방지하기 위해 border-box, hover 전에는 first-child만 보일 수 있도록 height를 제한하고 overflow:hidden을 주었음.
  
```
  .siteBox {
    box-sizing: border-box;
    width: 100%;
    height: 40px;
    overflow: hidden;
    padding: 0 1.5rem;
    transition: all 1s;
  }
  ```

또한, hover를 했을 때 자연스럽게 애니메이션이 동작할 수 있도록 transition을 주었음.

- hover 애니메이션
  
```
.siteBox:hover {
  height: 190px;
  transition: all 500ms;
}

.siteBox:hover .siteList {
  padding-top: 5%;
  transition: all 500ms 500ms;
}

.siteBox:hover .siteList__item {
  padding: 0.5rem auto;
  transition: all 500ms;
}
```

  hover를 하였을 때 siteBox(하얀색 박스)는 높이가 길어져야하므로 height 값을 설정.

  siteBox에 hover 할 시, siteList는 아래로 내려가는 효과가 있기에 padding-top을 5%로 주며, 바로 실행되지 않도록 transition-delay를 주었음.


---

## 완성 이미지와 영상

<img width="345" alt="스크린샷 2023-06-11 오전 12 01 20" src="https://github.com/Sirori/home-work/assets/116864776/399d08cd-6d4d-4e40-83b6-62a547528cd3">

<img width="278" alt="image" src="https://github.com/Sirori/home-work/assets/116864776/46ab2813-bef8-49ea-b69c-862f6a4c4b1e">

hover 이전 화면과 hover 시 화면.


![화면_기록_2023-06-11_오전_12_00_48_AdobeExpress](https://github.com/Sirori/home-work/assets/116864776/43a79ba6-5c3f-44fc-8511-65a5532c42df)


gif 파일.


