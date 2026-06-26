# amu.css
> "아무나, 아무렇게나 사용하는 태그 기반 디자인 시스템"


## 🚀 서비스 소개 (Service Introduction)
**"복잡한 클래스명은 잊으세요, 태그만 적으면 디자인이 완성됩니다."**

**amu.css**는 이름 그대로 **'아무나'** 쉽고 빠르게, **'아무렇게나'** 태그를 작성해도 조화로운 디자인이 유지되도록 설계된 초경량 디자인 시스템입니다.   
클래스명을 외워야하던 방식에서 벗어나, 표준 HTML 태그 기반의 시맨틱 구조를 통해 개발 생산성을 극대화합니다.


## 🖼️ 디자인 미리보기 (Visual Showcase)
<img width="1710" height="880" alt="image" src="https://github.com/user-attachments/assets/29c0a075-b85b-437b-bbdd-cb2c123e9541" />

```html
<body>
    <main>
        <article>
            <header>
                <h2>문제: 가장 긴 증가하는 부분 수열(LIS)</h2>
                <p>난이도: <mark>Gold II</mark></p>
            </header>
            
            <section>
                <h3>문제 설명</h3>
                <p>어떤 수열의 부분 수열 중 증가하는 순서대로 나열된 가장 긴 수열을 찾으세요.</p>
                <pre>입력: [10, 9, 2, 5, 3, 7, 101, 18]
출력: 4 (수열: [2, 3, 7, 18])</pre>
            </section>

            <hr>

            <section>
                <h3>제출 및 풀이</h3>
                <form>
                    <label for="solution-code">작성한 소스 코드</label>
                    <textarea id="solution-code" rows="10" placeholder="여기에 풀이를 작성하세요..."></textarea>
                    
                    <button type="submit">제출하기</button>
                </form>
            </section>
        </article>
    </main>
</body>
```


## 🔗 Quick Start
amu.css를 시작하는 방법은 사용자의 목적에 따라 두 가지가 있습니다.

* **빠르게 적용하기 (CDN)**: 별도의 설치 과정 없이 CDN 링크 하나만으로 즉시 시스템을 적용할 수 있습니다.
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Arma75/amu-css/amu.css">
```

* **나만의 디자인으로 완성하기 (Fork & Customize)**: amu.css는 단순히 제공되는 스타일을 사용하는 것을 넘어, **사용자가 직접 프로젝트를 Fork하여 `_origin.scss`의 변수값들을 수정하는 것을 더욱 권장합니다.**   
  브랜드 아이덴티티에 맞춰 시스템의 기초 스케일과 색상을 직접 제어함으로써, 본인만의 고유한 디자인 시스템을 구축하는 최상의 경험을 누려보세요.


## 💡 프로젝트 배경 및 필요성 (Project Background)
* **개발 배경:** 매번 프로젝트를 시작할 때마다 클래스명을 고민하고, 동일한 컴포넌트 스타일을 반복해서 작성하는 비효율성을 해소하고자 기획되었습니다.
* **필요성:** 디자이너가 없어도, 복잡한 디자인 지식이 없어도 HTML 태그 구조만 올바르게 작성하면 수준 높은 레이아웃과 디자인이 자동으로 적용되는 시스템이 필요했습니다.


## 🛠️ 주요 기능 (Main Features)
* **태그 기반 스타일링:** 특정 클래스 호출 없이 표준 태그(`h1~h6`, `section`, `input` 등)만으로 스타일 자동 적용
* **자동 스케일 시스템:** `generate-scale` 믹스인을 통한 비율 기반의 간격 및 크기 자동 생성
* **다크 모드 지원:** `data-theme="dark"` 속성 하나로 전체 컬러 시스템 자동 전환
* **반응형 최적화:** 브라우저 뷰포트에 따른 여백 및 간격(Gap) 자동 변환
* **유연한 커스터마이징:** 단 하나의 `_origin.scss` 수정으로 전체 시스템의 톤앤매너 변경 가능


## 🎯 타겟 고객 (Target Audience)
* 빠르게 프로토타입을 제작해야 하는 1인 개발자 및 스타트업
* 디자인 시스템 구축의 복잡함에 지친 프론트엔드 개발자
* 클래스 명명 규칙에 얽매이지 않고 표준 HTML 구조를 선호하는 사용자


## 📂 시스템 구조 (System Architecture)
본 시스템은 디자인의 변경이 유연하고 유지보수가 간편한 3단계 레이어 구조를 채택하고 있습니다.
```
└── amu-css
    ├── README.md
    ├── LICENSE
    ├── amu.scss
    ├── amu.css
    ├── amu.css.map
    ├── _origin.scss
    └── modules
        ├── _raws.scss
        ├── _semantics.scss
        ├── _reset.scss
        ├── _layouts.scss
        ├── _typography.scss
        ├── _tables.scss
        ├── _lists.scss
        ├── _interactives.scss
        ├── _forms.scss
        └── _media.scss
```


## 🏗️ 변수 레이어 (Variable Layers)
본 시스템은 디자인의 변경이 유연하고 유지보수가 간편한 3단계 레이어 구조를 채택하고 있습니다.

| 레이어 | 역할 | 설명 |
| --- | --- | --- |
| **_origin.scss** | 근본 값 | 시스템의 가장 기초가 되는 기본 스케일 값(색상, 간격, 크기 등)을 정의합니다. |
| **_raws.scss** | 원시 토큰 | Origin 값을 시스템 전반에서 활용하기 쉬운 형태로 규격화합니다. |
| **_semantics.scss** | 시맨틱 토큰 | 실제 HTML 태그와 매핑되는 의미론적 변수를 정의합니다. |


## 🏷️ 모듈별 디자인 대상 태그 (Module & Tag Mapping)
amu.css 시스템은 각 모듈별로 명확한 태그 디자인을 담당합니다.

* **_layouts.scss**
```html
body
header
nav
main
aside
section
article
footer
dialog
```
* **_typography.scss**
```html
h1
h2
h3
h4
h5
h6
p
span
hr
b
i
u
s
sub
sup
strong
em
mark
small
time
abbr
dfn
q
blockquote
cite
del
ins
a
summary
address
details
```
* **_tables.scss**
```html
table
caption
thead
tbody
tfoot
tr
th
td
```
* **_lists.scss**
```html
ul
ol
li
dl
dt
dd
```
* **_interactives.scss**
```html
input
textarea
select
button
```
* **_forms.scss**
```html
fieldset
legend
progress
meter
output
```
* **_media.scss**
```html
figure
figcaption 
img
video
iframe
audio
svg
```