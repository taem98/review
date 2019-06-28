# 1. HTML 기초

html은 마크업 언어의 기초이다 <br>
- 마크업 언어 : 구조 정의 언어
- **태그**

`<!DOCTYPE html>` : html5으로 작성된 다는 것을 브라우저에게 알려줌
`<html lang="kr">` :시작태그, lang은 사용하는 주 언어, html 밖에 다른 태그 있으면 안 됨.
`<meta charset="utf-8">`: 한글 깨지지 않게 해줌
`title`: 페이지 제목
`body` : 실질적 출력 내용

  

## 시맨틱 태그

- html 태그 중 하나
- 레이아웃에 직접 관여
[참고](https://www.w3schools.com/html/html_layout.asp)
<br>
- header : 제목, 소개
- nav : 페이지 이동을 위한 메뉴가 들어옴
- section : 기준에 따라 구획을 구분ㅂ하기 위함
- article : 주 내용을 담기 위함
- aside : 광고나 사이트 주변 부분
- footer : 회사 정보, 사이트 정보 등 추가 정보


## 텍스트와 관련된 태그

<h3> 제목 태그 </h3>
- `h1` ~ `h6`
- heading의 약자
<h3> 내용 태그 </h3>
- `p` : 단락, 문단의 토막을 나타내고 싶을 때
- `br` : 줄바꿈, 종료태그 x(빈요소), break
- `pre` : 줄바꿈, 들여쓰기 모두 포함 출력 preformatted

<h3> 택스트 관련 태그 </h3>
- `strong` : 굵게 ( 강조 )
- `em` : emphasized , 이탤릭체 ( 강조 )
- `sub` : subscripted, 다른 텍스트보다 아래쪽에 출력  ( 작게 )
- `sup` : superscripted, 다른 텍스트보다 위쪽에 출력 ( 작게 )
- `int` : insert,  밑줄
- `del` : deleted, 취소선

## 링크 태그

`a` : anthor

```html
<a href = " www.naver.com"> 네이버 바로가기 </a>
```
`href` :  hypertext reference, 웹사이트의 URL을 가지고 있다.

# 멀티 미디어와 관련된 태그

## 이미지 삽입하기

`img` : 이미지 출력
```html
<img scr = "삽입하고 싶은 이미지의 URL">
```
- `src` : source, 삽입하고 싶은 이미지를 속성에 넣어야 이미지 출력 가능

```html
<img src="이미지URL" alt="불러올 이미지 실패 시 표시 문구">
```

## youtube 삽입하기

```html
<iframe width="" height="" src="퍼가기 버튼의 유튜브 주소"></iframe>
```

# target

- 새 창을 열 때 속성 추가

## 새탭에서 링크 열기
```html
target="_blank"
```

## 기존탭에서 링크 열기
```html
target="_self"
```

# table과 list

## table
- `<table>` : 테이블 태그
- `<th>` : 제목셀
- `<td>` : 데이터셀
- `<tr>` : 행

<img src="https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F50c389db-5e11-46ce-a91a-f8f6a954a00c%2F_2019-04-01__11.06.23.png?table=block&id=ea13e7e7-f1be-43c0-a2ee-d87efd196fc3&width=4660&cache=v2">

### 병합하기 ( 셀합치기 )

- `rowspan = "숫자"` : 숫자만큼 셀이 행을 점유
- `colspan = "숫자"` : 숫자만큼 셀이 열을 점유
## LIST

### LIST생성하기

#### 순서가 없는 목록
- `<ul>` : unordered list<br>
    - `<li>` : 리스트 표현

#### 순서가 있는 목록
- `<ol>` : ordered list
    - `<li>` : 리스트 표현
- 관련 속성
    - `start = "숫자"`: 리스트가 시작하는 숫자 지정
    - `type = "문자"` : 리스트가 시작하는 문자 지정
    - `reversed` : 순서를 반대로 시작
        - `<ol <ol reversed></ol>`
    - `value="숫자"`: `li`태그에 기재하는 속성, 해당 리스트 아이템 번호를 지정
    
[리스트 태그 속성 참고](https://www.w3schools.com/html/html_lists.asp)


# form 태그

`form` <br>
데이터를 입력하는 신청서 종이
- 속성
    1. `action` : 데이터를 보낼 url을 지정
    2. `method` : 데이터 전송 방식 지정 ( GET or POST)
- 관련태그 
    1. `input` :  사용자에게 입력을 받기 위해 사용
    ```html 
    <input type ="text" id = "userid" name="id" value="html">
    ```
    - `type` : (필수) 입력받는 데이터 타입
    - `id` : 모두 고유하게 갖고 있는 이름
    - `name`, `value` : 데이터를 보낼 때 Key, Value
    - `placeholder` : 입력 하기 전에 연한 글씨로 폼 설명
    2. `label` : input과 같이 씀. for 속성에 원하는 input 태그의 id 속성을 넣어주면 두 태그가 같이 묶여서 나오게 된다.
    3. `select` : 선택 박스
        - `option` : `select`태그 안에 선택지로 삽입해서 사용
    4. `textarea` : 한번에 많은 글을 입력 받기 위해 사용
        - `cols`, `rows` : 행과 열, 글자 수와 줄 수 (속성)
    5. `button` : 전송, 초기화

[input 태그의 type들 + form 관련 태그들](https://www.w3schools.com/html/html_form_input_types.asp)
