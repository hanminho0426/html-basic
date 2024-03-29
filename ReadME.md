# HTML 기본문법

## 요소(Element)

```html
<!--시작(열린)태그, 요소의 내용(Contents), 종료(닫힌)태그로 이루어진다.-->
 <태그>내용</태그>
```

## 부모와 자식

```html
<!--<태그(부모)>
      <부모요소(윗태그의 자식)>자식요소</부모요소>
    </태그>-->
 <태그>
    <태그>내용</태그>
  </태그>
```

- 들여쓰기: tap
- 내어쓰기: shift + tap

## 상위(조상) 요소

- 부모요소를 포함한 내부(자식)요소를 기준으로 감싸는 모든 상위요소

```html
  <상위>
    <상위>
      <자식>자식</자식><!--기준-->
    </상위>
  </상위>
```

## 하위(후손) 요소

- 나를 기준으로 내가 감싸고 있는 아래의 모든 하위요소

```html
  <상위><!--기준-->
    <하위>
      <하위>자식</하위>
    </상위>
  </상위>
```

## 빈(Empty)태그

- 종료(닫힌)태그가 없어 내용이 없고 빈 태그
- 방식 2가지가 있다.

1. <태그> 열린 태그처럼 보이는 방식 HTML1/2/3/4/5 편리함
2. <태그/> 끝에 /(슬러쉬)를 붙여주는 방식 XHTML/HTML5 안전함

## 기능의 확장

열린(시작) 태그에는 속성(Attribute))과 값(Value)(기능의 확장)을 넣을 수 있다.

```html
<태그 속성='값'>내용</태그>
<img src(속성)='./위치'(값) alt(속성)='이미지'(값)/>
<input type(속성)="text"(값)>
```

### input

- 사용자가 데이터를 입력하는 요소(태그)! 어떤 데이터 타입을 입력 받을 것인지 명확해야한다.
- 쉽게 말해 type에 "text"를 넣으면 검색창, "checkbox"를 넣으면 체크박스 형태가 만들어진다.

## 글자와 상자

- 요소가 화면에 출력되는 특성, 크게 2가지로 구분
- 인라인(Inline)요소: 글자를 만들기 위한 요소들 /글자에 해당
- 블록(Block)요소: 상자(레이아웃)를 만들기 위한 요소들 / 상자에 해당

## 인라인(Inline)요소

- 인라인 요소는 자식요소로 블록요소를 넣을 수 없다.(글자 안에는 상자를 넣을 수 없다.)
- 인라인과 인라인 사이는 부모 자식이 가능하다.
- 수평으로 쌓인다.(왼쪽에서 오른쪽으로)

### span

- 대표적인 인라인 요소! 본질적으로 아무것도 나타내지 않는 콘텐츠 영역을 설정하는 용도
- 포함한 콘텐츠 크기만큼 가로,세로의 크기가 자동으로 줄어든다.

```html
<span>Hello</span>
<span>World</span>
<span>Content</span>

Hello World Content(요소가 수평으로 쌓임 / 왼쪽에서 오른쪽으로)
```

```html
요소의 가로너비를 지정하는 CSS속성

<span style="width:100px;">Hello</span>
<span style="height:100px;">World</span>

글자는 가로,세로 사이즈를 가질 수 없기 때문에<br />
CSS 가로세로 크기 속성을 넣어도 변하지 않는다.
```

```html
요소의 외부 내부 여백 지정하는 CSS속성

<span style="margin(외부):20px(위아래) 20px(좌우);">Hello</span>
<span style="padding(내부):20px(위아래) 20px(좌우);">World</span>

인라인은 내부 외부 상관없이 위아래 여백은 적용이 되지 않고<br />
좌우만 적용된다. -->
```

## 인라인(Inline)종류

1. img태그: 이미지를 삽입하는 요소(image)

```html
<img src="삽입할 이미지의 경로" alt="삽입할 이미지의 이름" />
```

2. a태그: 다른/같은 페이지로 이동하는 하이퍼링크를 지정하는 요소.(Anchor)

```html
<a href="주소" target="_blank(새 탭) / 링크 URL의 표시(브라우저 탭)위치"
  >내용</a
>
```

3. span태그: 특별한 의미가 없는 구분을 위한 요소
4. br태그: 인위적으로 줄바꿈을 하는 요소(Break)

## 블록(Block)요소

- 블록요소 안에는 인라인요소를 자식요소로 사용 가능하다.
- 인라인과 다르게 수직으로 쌓인다(위에서 아래로)
- 가로너비는 최대한 늘어나려고 하고 세로너비는 포함한 컨텐츠 크기만큼 자동으로 줄어든다.

### div태그: 대표적인 블록요소! 본질적으로 아무것도 나타내지 않는, 콘텐츠 영역을 설정하는 용도

```html
요소의 가로너비를 지정하는 CSS속성

<div style="width:100px;">Hello</div>
<div style="height:40px;">World</div>

div는 Block 상자이기 때문에 가로, 세로너비의 CSS속성을 적용하면 변한다.
```

```html
요소의 외부 내부 여백 지정하는 CSS속성

<div style="margin(외부):20px(위아래) 20px(좌우);">Hello</div>
<div style="padding(내부):20px(위아래) 20px(좌우);">World</div>

블록은 위아래 좌우 모두 외부, 내부 상관없이 CSS속성이 적용된다.
```

## 블록(Block)종류

1. div태그 특별한 의미가 없는 구분을 위한 요소(Division)
2. h1태그 제목을 의미하는 요소(Heading) h1~h6까지있고, 숫자가 작을수록 제묵의 크기가 작아진다.
3. p태그 문장을 의미하는 요소(Paragraph)
4. ul태그 순서가 필요없는 목록의 집합을 의미.(Unordered List) ul태그의 자식으로는 반드시 li가 하나라도 있어야 한다.
5. li태그 목록 내 각 항목 (List item)
6. input태그

```html
<input type="text" value="Hello" />
미리 입력된 값(데이터) 화면에 미리 출력 될 값

<input type="text" placeholeder="이름을 입력하세요" />
사용자가입력할 값(데이터)의 힌트 희미하게 보여지는 값

<input type="text" disabled />
입력요소 비활성화 사용자가 입력창에 입력을 할 수 없어짐

<input type="checkbox" />
사용자에게 체크 여부를 입력 받음!

<input type="checkbox" checked />
체크박스 입력 요소가 미리 체크됨

<input type="radio" name="그룹이름" />
radio: 사용자에게 체크여부를 그룹에서 1개만 입력 받음! --> name: 그룹 지어주는
그룹명 사용자가 데이터를 입력하는 요소, \*인라인인 동시에 블록의 성질을
가진다(inline-block).
```

```html
<ul>
  <li>사과</li>
  <li>배</li>
  <li>홍시</li>
</ul>
```

## 테이블 요소 = table

- 표 요소 행(Row)과 열(Column)의 집합.

```html
<table>
  <tr>
    <!--행(Row)을 지정하는 요소 (Table Row)-->
    <td>A</td>
    <!--열(Column)을 지정하는 요소 (Table Data)-->
    <td>B</td>
  </tr>
  <tr>
    <td>C</td>
    <td>D</td>
  </tr>
  <table></table>
</table>
```

## 주석

- Ctrl + /
- <!--Commit--> 수정사항이나 설명등을 작성(주석)
- 브라우저는 이 태그를 해석하지 않기 때문에 화면에 내용이 표시되지 않음

## 전역속성

- 전체영역에서 사용할 수 있는 속성

1. <태그 title="설명"></태그> 요소의 정보나 설명을 지정
2. <태그 style="스타일"></태그> 요소의 적용할 스타일(CSS)을 지정
3. <태그 class="이름"></태그> 요소를 지칭하는 중복가능한 이름 class를 적용할 때는 ".이름" 사용
4. <태그 id="이름"></태그> 요소를 지칭하는 고유한 이름 id를 적용할 때는 "#이름" 사용
5. <태그 data-이름="데이터"></태그> 요소에 데이터를 지정

```html
<div data-fruit-name="apple">사과</div>
<div data-fruit-name="banana">바나나</div>
```

```js
const
els = document.querySelectAll('div') els.forEach(el => {
console.log(el.dataset.fruitName) })

```
