# 과제02_Login창 만들기

## 과제 조건
- 마크업 순서
  1. 로그인(제목)
  2. 아이디 레이블과 입력서식
  3. 비밀번호 레이블과 입력서식
  4. 로그인 버튼
  5. 회원가입 및 아이디/비밀번호 찾기 링크<br>
<br>
- 이미지 assets 없이 모든 디자인을 CSS로 구현.

- 일부 요소의 배치를 position 속성을 활용하여 구현.

- 회원가입, 아이디/비밀번호 찾기 영역은 float을 활용하여 구현.

<br>
<br>

---
## 과제 내용
<br>

- form 태그를 활용하여 아이디, 비밀번호 입력창과 button을 생성.


- 아이디와 비밀번호를 입력하는 창은 position: absolute를 주어 오른쪽 정렬이 맞을 수 있도록 하였음.
  
  
```
.idInput__input,
.passwordInput__input {
  position: absolute;
  right: 30%;
}
```

-회원가입, 아이디/비밀번호 찾기는 각각 float:left, float:right를 주어 각 자리에 배치될 수 있도록 하였음.

 (또한 이미지를 대신하여 list-style을 변경하였음)

```
.signIn {
  list-style: circle;
  float: left;
}

.finder {
  list-style: circle;
  float: right;
}
```







<img width="271" alt="image" src="https://github.com/Sirori/home-work/assets/116864776/a5ecdd83-0000-468f-acac-42a910a516ae">
