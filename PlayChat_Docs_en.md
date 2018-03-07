# Playchat Docs
---
## 목차
* 시작하기
	* 10분 안에 챗봇 만들기
	*  기본 개념
* 개요
	* 챗봇
		* 만들기
		* 정보 수정
		* 복제 하기
		* 공유 하기
		* 삭제 하기
	* 대화 시나리오
		* 개발
			1. 카드
			2. 사용자 입력
			3. 답변 전 실행 함수
			4. 챗봇 답변
		* 관리
	* 대화셋
		* 개발
			1. 기본 대화셋
			2. 추가 대화셋
		* 관리
	* 채널
		* 카카오
		* 페이스북
		* 네이버 톡톡
		* 라인
		* 위챗
	* 운영
		* 사용자
		* 대화
	* 분석
		* 사용자
		* 대화
	* 테스트
		* 대화창
		* 실시간 대화 분석

* 모범 사례
	* 대화 시나리오 작성 가이드
	* 답변 전 실행 함수 가이드


----------

## 시작하기
### 챗봇 만들기

### 챗봇 이해하기



## 개요

### 챗봇
챗봇 관리 페이지에서 챗봇을 생성, 편집 및 삭제할 수 있습니다.

#### 만들기

다음 단계에 따라 챗봇을 생성합니다.

1. "챗봇 관리" 화면이 아직 열려 있지 않으면 플레이챗에 접속하여 홈버튼을 클릭하세요.
2. "챗봇 관리" 화면에서 새 봇 만들기 버튼을 클릭합니다. 
3. 빈 봇, 기능 안내 봇, 업종별 샘플 봇 중 하나를 선택하여 챗봇을 만들 수 있습니다.
4. "챗봇 생성" 화면에서 이름, 설명, 프로필 이미지, 언어를 입력하면 새로운 챗봇이 생성됩니다.
	- 이름 : 플레이챗 상에서 고유한 값으로 중복입력이 불가능합니다. 해당 챗봇에 대한 식별자 역할을 하며, 실제로 다른 사람들에게 보이는 값입니다. 글자 수 제한(30자)이 있습니다.
	- 설명 : 챗봇에 대한 간략한 설명을 입력해주세요. 글자 수 제한(100자)이 있습니다.
	- 프로필 사진 : 챗봇의 프로필 이미지를 등록해주세요. Playchat의 다른 사용자에게 보여지는 이미지입니다.
	- 언어 : 챗봇이 이용될 언어 환경을 선택합니다. 영어, 중국어, 한국어를 지원하고 있습니다. 

챗봇이 생성되면 챗봇 관리 화면에 카드 형태로 나타납니다.

* 종류
빈 봇, 기능 안내 봇, 샘플 봇 등 3가지 종류 중 하나로 챗봇을 만들 수 있습니다. 

	* 빈 봇 
빈 봇은 말 그대로 시작 카드만 있는 백지 상태의 챗봇을 말합니다.

	* 기능 안내 봇
챗봇을 구축함에 있어 필요한 기능들(엔터티, 인텐트 등)을 쉽게 설명하기 위해 제공되는 챗봇입니다. '챗봇 만들기' 안내 문서를 참고해 이용할 수 있습니다. 

	* 샘플 봇
업종별 챗봇 구축을 쉽게하기 위해 각 업종별로 필요한 기능들을 구현해 놓은 맞춤형 샘플 챗봇입니다. 챗봇을 구축하고 싶으나 어떻게 시작해야될지 몰라 막막할 때 미리 생성된 업종별 샘플 봇을 수정해 챗봇을 구축할 수 있습니다. 

* 갯수 제한
플레이챗에서 만들 수 있는 챗봇의 갯수는 제한이 없습니다. 최대한 많이 챗봇을 만들어보세요.

#### 정보 수정
이름, 설명, 프로필 사진, 언어 설정을 변경하려는 챗봇 카드 우상단의 메뉴버튼을 눌러 챗봇의 정보를 수정할 수 있습니다.

#### 복제하기
복제하려는 챗봇 카드 우상단의 메뉴버튼을 눌러 챗봇을 복제할 수 있습니다. 

#### 공유하기
공유하려는 챗봇 카드 우상단의 메뉴버튼을 눌러 챗봇을 공유할 수 있습니다.

#### 삭제하기
삭제하려는 챗봇 카드 우상단의 메뉴버튼을 눌러 챗봇을 삭제할 수 있습니다.

### 대화 시나리오
트리 형식의 시나리오 그래프로, 사용자가 쉽게 챗봇을 개발하고 편집할 수 있는 도구입니다. 대화 시나리오는 *.graph.js 형태의 파일로 저장되고, Task는 *.js의 파일 형태로 저장됩니다. 대화 시나리오를 사용하기 위해서는 왼쪽 네비게이션 바의 "개발" -> "대화 시나리오"를 클릭하세요.
#### 개발


1. 카드

대화 시나리오 화면을 보면 네모난 박스들이 연결되어 있는 것을 확인할 수 있습니다. 이 네모 박스 하나를 **카드**라고 지칭합니다. 하나의 **카드**는 기본적으로 카드 이름, 사용자 입력, 챗봇 답변, 답변 전 실행함수로 이루어져 있습니다. **카드**를 더블 클릭하면 오른쪽에 카드 수정창이 등장합니다.

 * 카드이름
**카드이름**은 해당 카드를 지칭하는 이름으로써 카드들에 대한 식별자 역할을 하기에 중복된 이름을 사용할 수 없습니다. 카드 이름은 대화흐름조절 기능에서 이용됩니다. 

 * 사용자 입력
**사용자 입력**은 해당 카드를 실행시키기 위한 조건 정보(예상되는 챗봇 사용자의 입력값)를 지정하는 부분 입니다. 예를 들어 **사용자 입력**에 '안녕'이라고 입력했다면, 챗봇 사용자가 '안녕'이라고 입력하는 순간 해당 카드가 실행됩니다. 즉, 챗봇 답변을 내놓습니다. 

* 답변 전 실행 함수 

* 챗봇 답변
**챗봇 답변**은 해당 카드가 실행됐을 때 챗봇이 내놓을 답변을 지정하는 부분입니다. 예를 들어 **챗봇 답변**에 '반가워'라고 입력했다면, 해당 카드가 실행됐을 때 챗봇은 '반가워'라고 답변합니다.

* 부모카드와, 자식카드 그리고 형제카드
부모카드와 자식카드는 직접적으로 연결된 카드 사이의 관계를 지칭하는 용어입니다. 카드는 하나의 부모 카드와 복수의 자식 카드를 가질 수 있습니다. 예를 들어, 시작 카드의 오른편에 직접적으로 연결된 카드들은 모두 시작 카드의 자식 카드이며, 시작카드를 부모카드로 가지고 있다고 말할 수 있습니다. 또한 동일한 부모를 갖고 있는 카드들을 형제 카드라고 말합니다. 

* 뎁스
**뎁스**는 카드의 세대를 의미합니다. 예를 들어 시작 카드의 경우, 세대 즉 뎁스는 0이며 시작 카드의 자식들은 뎁스가 1입니다.  
자식 카드로 내려갈수록 뎁스는 1씩 증가합니다. 

* 커서
 **커서**는 챗봇 사용자의 입력을 기다리는 카드(혹은 마지막으로 실행된 카드)를 지칭하는 용어입니다. 예를 들어 시작  카드가 실행된 후, 사용자의 입력을 기다리고 있다면 커서는 시작 카드에 놓여 있습니다.
커서는 챗봇 사용자의 입력값이 있을 경우에 이동합니다.
커서의 이동을 대화흐름이라고 말할 수 있습니다.
대화 흐름(커서의 이동)은 기본적으로  부모 카드에서 자식 카드로 이동합니다. 하지만 챗봇 답변의 대화흐름 조절 기능을 이용할 경우 임의의 다른 카드로 이동할 수 있습니다.

* 검색, 매칭 그리고 실행
	* **검색**은 챗봇 사용자의 입력값이 어떤 자식 카드의 '사용자 입력'과 일치하는지  찾는 행위를 말합니다.예를 들어 챗봇 사용자가 '안녕'이라고 입력했을 경우, '사용자 입력'에 '안녕'이라고 입력된 자식 카드를 찾는 것을 **검색한다**라고 말합니다. 
		* 검색은 순서를 가집니다. 상위의 자식 카드부터 하위의 자식 카드 순으로 검색이 진행됩니다. 다시 말해, 챗봇 사용자의 입력값에 대해 첫 번째 자식카드(자식들 중 가장 상위에 있는 카드)부터 매칭 여부를 판단하고, 매칭이 되지 않았을 경우 두 번째 자식카드와 매칭여부를 판단합니다.  따라서 동일한 **사용자 입력** 을 갖고 있는 자식 카드들이 있다면 가장 상위에 있는 카드가 매칭됨을 기억해야 합니다.
		* 공통 카드는 일반 카드보다 먼저 검색됩니다. 커서의 위치에 상관없이, 공통 카드를 검색한 후 일반 카드를 검색합니다.
	* **매칭**은 챗봇 사용자의 입력값과 부합하는 자식 카드를 발견한 것을 말합니다. 
	예를 들어 챗봇 사용자가 '안녕'이라고 입력했을 경우, '사용자 입력'에 '안녕'이라고 입력된 자식 카드를 찾았다면 해당 카드와 **매칭되었다**고 말합니다. 
	* **실행**은 챗봇 사용자의 입력값이 특정 카드의 사용자 입력과 매칭되어, 챗봇 답변을 출력하는 것을 말합니다.
	예를 들어 챗봇 사용자가 '안녕'이라고 입력하고 '사용자 입력'에 '안녕'이라고 입력된 카드와 매칭되었을 경우 해당 카드의 '챗봇 답변'을 출력하는데 ,이를 해당 카드가 **실행되었다**고 말합니다.
	카드가 실행되고 나면 커서는 해당 카드로 이동하고 챗봇 사용자의 입력을 다시 기다립니다.

* 대화 흐름
대화 흐름은 "챗봇 사용자의 입력" -> "검색" -> "실행"의 주기로 커서가 이동하는 것을 지칭합니다.
	* 챗봇 사용자의 입력
	챗봇 답변이 출력되면 챗봇 사용자의 입력을 기다립니다.
	* 검색
	챗봇 사용자의 입력값이 어느 자식 카드의 사용자 입력과 일치하는지 검색합니다.
	* 실행
	챗봇 사용자의 입력값이 자식 카드의 **사용자 입력**과 부합할 때(매칭) 자식 카드가 실행되고 커서가 해당 카드로 이동합니다.
	(만약 챗봇 사용자의 입력값이 모든 자식 카드의 **사용자 입력**과도 매칭되지 않는다면 챗봇은 '알아듣지 못했습니다'라고 답변하고 커서는 시작카드로 이동합니다. 챗봇 사용자의 입력값에 부합하는 자식 카드가 없기 때문입니다.)
	* 챗봇 사용자의 입력
	챗봇 답변이 출력되면 챗봇 사용자의 입력을 기다립니다.
	> 챗봇 사용자의 입력 -> 검색(자식카드와의 매칭 여부) -> 실행(챗봇 답변 및 커서 이동) -> 챗봇 사용자의 입력-> ....

* 공통 카드
	공통 카드는 모든 카드에 앞서 검색되는 카드들을 의미합니다. 대화 시나리오 화면의 공통 카드 버튼을 눌러 확인 할 수 있습니다. 예를 들어, 시작카드와 이전 카드의 경우 커서의 위치에 상관없이 챗봇 사용자의 입력값에 대해 제 1순위로 검색됩니다. 
	* 시작카드
	사용자가 처음 챗봇과 대화를 시작할 때 실행되는 카드이자, 대화 시나리오의 처음으로 돌아가고자 할 때 실행되는 카드입니다.
	* 답변없음 카드
	매칭된 카드가 존재하지 않을 때 실행되는 카드입니다. 챗봇 답변은 "알아듣지 못했습니다." 입니다.

* 메뉴
카드의 우상단에 해당 카드를 조작하는 메뉴가 있습니다.
	* 자식카드 생성
	해당 카드를 부모로 하는 자식 카드를 생성합니다. 생성된 자식 카드는 최하위 자식 카드로 추가됩니다. 또한 카드의 오른쪽에 추가하기 버튼을 클릭하면 자식카드를 생성할 수 있습니다.
	* 위로 가기 및 아래로 가기
	형제 카드들 사이의 순서를 변경합니다. 
	* 잘라내기
	해당 카드를 삭제하고 삭제된 카드를 복사해 메모리에 저장해 둡니다.
	* 복사하기
	해당 카드를 복사해 메모리에 저장해 둡니다.
	* 붙여넣기
	메모리에 저장된 카드를 해당 카드의 자식카드로 생성합니다.
	* 복제하기
	해당 카드와 동일한 카드를 형제 카드로 생성합니다.
	* 삭제하기
	해당 카드를 삭제합니다. 

2. 사용자 입력
* 사용자 입력의 구성
사용자 입력의 기본 모드는 키워드입니다. 사용자 입력을 키워드, 인텐트, 엔터티, 정규식, 타입, 조건문을 조합하여 다양하게 구성할 수 있습니다. 

	* 키워드(Keyword)
		* 사용자 입력의 기본 모드는 *키워드 방식*입니다. 
		* 키워드 방식이란 **사용자 입력**에 저장된 *키워드*를 챗봇 사용자가 입력했을 경우에 해당 카드가 실행되는 방식을 뜻합니다. 예를 들어, **사용자 입력**에 "여름 상의 면"과 같은 키워드가 입력되었을 경우 사용자가 해당 키워드가 모두 포함된 문장(면으로 된 여름 상의 좀 찾아줄 수 있어? 등)을 입력했을 시에 해당 카드가 실행됩니다. 다른 예시로 **사용자 입력**에 "여름", "상의", "면"과 같은 키워드가 입력되었을 경우, 사용자가 해당 키워드 중 어느 하나라도 포함된 문장(면으로된 옷 좀 보여줘, 여름에 입을만한 옷좀 찾아줘, 상의 보여줘 등)을 입력하면 해당 카드가 실행됩니다. 
		* 키워드 방식은 버튼형 챗봇과 같은 간단한 챗봇에는 적합할 수 있으나, 대화형 챗봇이나 고도화된 챗봇에는 적합하지 않을 수 있습니다. 예를 들어, 챗봇 사용자가 "면으로 된 여름 상의 찾아줘"라고 입력했을 경우 키워드 방식이 적합할 수 있으나,  "더울 때 입는 윗도리 찾아줘"와 같이 같은 의미의 다른 문장을 입력했을 경우 해당 카드는 실행되지 않습니다. 같은 의미지만 다른 키워드를 사용했기 때문에 해당 카드가 실행되지 않은 것입니다. 따라서 다양하게 표현되는 동일한 의미의 문장들을 함께 처리하고 싶을 경우에는 키워드 대신 인텐트를 이용해야 합니다.

	> 버튼형 챗봇은 키워드! 대화형 챗봇은 인텐트!

	* 인텐트(#Intent)
		*	인텐트는 의도를 뜻합니다. 
		* "상의 찾아줘"와 "상의 검색해줘"는 같은 뜻 혹은 의도를 가졌다고 볼 수 있습니다. 이럴 경우, 두 문장을 하나의 인텐트로 처리할 수 있습니다. 따라서 **사용자 입력**을 인텐트로 입력하면 하나의 의도를 가진 여러가지 표현의 문장을 함께 처리할 수 있습니다. 예를 들어, *검색 인텐트*를 만들어 위의 두 문장을 포함시키면 두 가지 문장을 하나의 인텐트로 처리할 수 있습니다.
		* 화면 왼쪽 네비게이션 바의 관리 -> 인텐트에 들어가면 인텐트를 만들 수 있습니다. 혹은 카드의 사용자 입력에 포커스하고 '#'키를 누르면 인텐트를 선택하거나 새로 만들 수 있는 입력 가이드가 나타납니다.
		* 문장과 인텐트가 1:1대응이 아니라는 점을 기억하세요. 즉, 하나의 문장이 여러 인텐트에 속할 수도 있습니다. 예를 들어,  "점퍼 갖고 싶어"의 경우 맥락에 따라 검색 인텐트일 수 있고, 구매 인텐트일 수도 있습니다. 이렇듯 어떤 문장이 어느 인텐트에 속하는지는 대화의 맥락에 따라 변할 수 있습니다. 챗봇 개발자는 이 점을 염두해 일관성있게 인텐트 사용해야합니다.

	> 여러 문장을 하나의 인텐트로 처리하자!

	* 엔터티(@Entity) 
		* 엔터티는 개체명을 뜻합니다.
		* 반팔, 긴팔, 외투, 점퍼 등을 하나의 개체명(상의)으로 인식하고 싶을 때는 엔터티를 사용할 수 있습니다. 반팔, 긴팔, 외투 등을 '상의'라는 엔터티로 묶는다고 말할 수 있습니다. 다른 예시로, 말, 고양이, 호랑이 등을 '동물'이라는 엔터티로 묶을 수도 있습니다. 즉, 다양한 각각의 개체들(말, 고양이, 호랑이)을 '개체명(동물)'으로 묶을 수 있습니다. 
		* 화면 왼쪽 네비게이션 바의 관리 -> 엔터티에 들어가면 엔터티를 만들 수 있습니다. 혹은 카드의 사용자 입력에 포커스하고 '@'키를 누르면 엔터티를 선택하거나 새로 만들 수 있는 입력 가이드가 나타납니다.
		* 명사와 엔터티가 1:1 대응이 아니라는 점을 기억하세요. 즉, 하나의 명사가 여러 엔터티에 속할 수도 있습니다. 예를 들어, 말은 '동물'이라는 엔터티에 속할 수도 있고, '십이지신'이라는 엔터티에 속할 수도 있습니다. 또한 고양이 자체가 엔터티가 되어 그 개체에 샴고양이, 뱅골 고양이 등이 속할 수 있습니다. 따라서 쓰임새에 따라 어떤 개체명으로 어떤 개체를 묶을지, 즉 어떤 엔터티를 사용할지 결정해야 합니다. 
	예시)
		* 만약 **사용자 입력**에는 @상의 엔터티와 #검색 인텐트가 AND 조건으로 입력되어 있다면, 상의 엔터티에 포함된 개체들과 검색 인텐트의 문장을 동시에 입력했을 때 해당 카드가 실행됩니다. 그 결과, "반팔티 찾아줘", "긴팔 찾아줘", "긴팔 검색해줘" 등 다양한 표현을 하나의 카드에서 처리할 수 있습니다. 

	> 여러 명사를 하나의 엔터티로 처리하자!

	* 정규식(/RegExr/) - 기능 가이드 챗봇 샘플(사용자입력_정규식)
	정규식은 특정한 규칙을 가진 문자열을 표현하는 데 사용하는 형식을 뜻합니다. 
	만약 사용자로부터 핸드폰 번호를 입력받고 싶을 땐 어떻게 해야할까요? **사용자 입력**에 '010-1234-1234'이라고 넣는다면 특정 핸드폰 번호만 부합합니다. 그렇다고 모든 핸드폰 번호를 사용자 입력에 저장할 수도 없습니다. 따라서 특정한 패턴의 숫자를 입력 받는 방법이 필요한데요, 이 때 사용할 수 있는 방법이 정규식(Regular Expression)으로 입력 받는 것입니다.  
	010-1234-1234와 같은 특정한 패턴을 가리키는 정규식을 **사용자 입력**에 저장하면 사용자가 해당 패턴을 입력할 때에만 대화 카드가 실행됩니다. 즉, **사용자 입력**이 /^\d{3}-\d{3,4}-\d{4}$/로 되어있기 때문에 해당 대화 카드가 실행되기 위해서는 사용자가 핸드폰 번호 형식을 입력해야만 합니다.
	**사용자 입력**에서 정규식을 입력하고 싶다면 '/'를 입력하면 됩니다. 정규식에 익숙하지 않은 분들은 <a href= "regexr.com">regexr.com</a>을 참고하세요.

	> 핸드폰 번호, 주소 등 특정 패턴을 받으려면 정규식이나 타입으로!

	* 타입($Type) - 기능 가이드 챗봇 샘플(사용자입력_타입)
	타입은 특정한 규칙을 가진 문자열을 표현하는 데 사용하는 형식을 뜻합니다. 
	타입은 특정한 패턴을 읽는 정규식과 같은 기능을 제공합니다. 예를 들어 **사용자 입력**에서 '$'을 입력하면 미리 생성되어 있던 여러가지 타입들이 보입니다. 그 중 mobile을 선택하면 핸드폰 번호에 맞는 입력값만 받아들이게 됩니다. 이처럼 타입은 기본적으로 특정 패턴의 입력값을 받아들이는 기능을 합니다(즉, 정규식과 같은 기능을 합니다.).
	하지만 타입은 코드 레벨에서 조작이 가능하기 때문에 정규식보다 더 많은 일을 할 수 있습니다. 예를 들어, 핸드폰으로 전송된 인증번호와 챗봇 사용자가 입력한 번호가 일치하는지 여부는 정규식만으로는 할 수 없습니다. 왜냐하면 정규식은 사용자 입력이 4자리라는 패턴은 읽을 수 있지만, 그 번호가 전송된 번호와 일치하는지는 알 수 없기 때문입니다. 따라서 전송된 번호와 사용자가 입력한 값이 일치하는지는 코드 차원에서 접근해야 합니다. 이럴 때 타입을 이용할 수 있습니다.
	인증번호 확인 대화카드에서 $checkCode라는 타입을 만들어 보겠습니다. 그러면 default.js 파일 에서 사용자가 입력한 값과 전송된 인증번호가 같은지 코드 레벨에서 처리 가능합니다. 
	자세한 내용은 답변 전 실행함수 파트에서 살펴볼 수 있습니다. 

	* 조건문(IF) - 기능 가이드 챗봇 샘플(사용자입력_조건문)
	조건문은 챗봇 사용자의 입력값 이외의 기준으로 카드를 실행시키는 기능입니다.
	대부분의 경우, 키워드, 엔터티, 인텐트, 정규식, 타입으로 **사용자 입력**을 원하는 방식으로 구성할 수 있습니다. 그러나 챗봇 사용자의 입력값과 무관하게 해당 카드가 실행되어야 하는 경우도 있습니다. 예를 들어, 사용자 이름을 **사용자 입력**으로 입력 받아야 하는 경우, 특정한 값이나 특정한 패턴으로 입력 받을 순 없습니다. 값이 정해져 있지 않을 뿐더러, 이름의 패턴은 전 세계적으로 다양하기 때문입니다(물론, 한국식 이름은 특정 패턴이 있으므로 정규식이나 타입을 이용할 수 있습니다). 따라서 사용자가 입력한 값에 상관없이 카드가 실행되어야 합니다. 이럴 때는 **사용자 입력**에 IF를 이용할 수 있습니다. 
	**사용자 입력**에서 조건문을 입력하고 싶다면 Advanced 모드에서 if를 입력하고 () 안에 조건식을 입력하면 됩니다.
	if(조건식)
	조건식은 코드레벨로 작성해야 합니다. 조건식의 결과값은 true나 false 둘 중 하나입니다. 사용자 입력을 if(true)라고 설정하면 해당 카드는 검색시 항상 매칭 된다고 볼 수 있습니다.
	조건문은 if(true)처럼 단순한 방식으로 사용할 수도 있지만, 사용 의도에 따라 충분히 다양한 응용이 가능합니다. 예를 들어, 남자 사용자와 여자 사용자에 따라 매칭 여부를 다르게 하고 싶을 때에도 if(gender == 'male')과 같은 형식을 입력할 수 있습니다. 물론, gender와 같은 변수는 미리 설정되어 있어야 합니다(조건식은 코드레벨입니다). 


* 사용자 입력의 추가/삭제
+버튼을 눌러 사용자 입력을 추가하고, 휴지통 버튼을 눌러 사용자 입력을 삭제할 수 있습니다.

* 복수의 사용자 입력(OR 조건)
시작 카드의 **사용자 입력**에는 3개의 사용자 입력(시작, 처음, start)이 지정되어 있습니다. 사용자 입력이 복수일 경우, 챗봇 사용자가 복수의 사용자 입력 중 어느 하나의 값만 입력해도 **시작 카드**가 실행됩니다. 예를 들어, '시작', '처음' 또는 'start'  중 어느 하나를 사용자가 입력했을 경우 **시작 카드**가 실행됩니다(오른쪽 대화창에서 확인해보세요).

* 사용자 입력의 AND 조건
하나의 사용자 입력에 복수의 값을 입력했을 경우, 챗봇 사용자가 복수의 값을 모두 입력했을 경우에만 해당 카드가 실행됩니다. 예를들어, '시작', '처음', 'start'가 하나의 사용자 입력에 함께 입력되어 있을 경우 챗봇 사용자가 '시작 처음 start'라고 입력해야 해당 카드가 실행됩니다. 

* 사용자 입력의 NLU
	사용자 입력에 새로운 값을 입력할 때 입력창 아래 작은 글씨로 nlu라는 안내글이 보입니다. nlu는 Natural Language Understanding(자연어 이해)의 약자로, 사용자 입력값을 실시간으로 챗봇이 이해할 수 있는 언어로 변환(자연어 처리)한 결과입니다. 예를 들어, 사용자 입력에 '처음으로 돌아가'라고 입력했을 경우, nlu 엔진에 의해 해당 값은 '처음 돌아가다'로 변환됩니다.


3. 답변 전 실행 함수 

*답변 전 실행 함수*는 카드가 실행됐을 때, 챗봇 답변이 출력되기 전에 필요한 기능들을 처리하는 함수를 뜻합니다. 
챗봇이 문자를 보내주거나, 음악을 틀어주거나, 집안의 조명기기를 조절하거나, 다른 기기와 소통하거나 데이터 베이스의 정보에 접근할 때 그 기능들을 수행하는 부분이 답변 전 실행 함수입니다. 따라서 답변 전 실행 함수는 코드레벨에서 할 수 있는 다양한 일들을 설정하는 자바스크립트 코드가 들어갑니다. 
```javascript
bot.setTask("myTask",
{
    action: function(dialog, context, callback)
      {
       //기능 구현 영역
          callback();
      }
});
```
위의 자바스크립트 코드는 답변 전 실행 함수를 이루는 기본 구조를 보여줍니다. 
```
* 기본적으로 bot.setTask(arg1, arg2); 와 같은 형태로 setTask 함수를 실행해 챗봇에 해당 함수를 등록합니다.
* 첫번째 파라미터(arg1)로 해당 함수의 이름("myTask")을 문자열 형태로 넣습니다.
* 두번째 파라미터(arg2)로 JSON 형태의 객체(Object)를 넣습니다. 기본 형태는 { action : function(dialog, context, callback){} }와 같습니다.
*  기능 구현 영역에 원하는 기능을 자바스크립트 코드로 구현합니다. 따라서 Node.js library를 이용할 수 있습니다. 
```

* action 함수
action 함수는 dialog, context, callback 3개의 매개 변수를 받습니다.

	* dialog
dialog는 해당 카드의 실행과 관련된 정보들(카드 정보, 챗봇 사용자의 입력값, 출력될 챗봇 답변)을 JSON 형태로 담고 있습니다. 즉, dialog 파라미터(JSON 객체)는  4가지 key(card, userInput, output, data)를 갖고 있습니다. 
		```javascript
		    dialog = {
			    card : ... ,
			    userInput : ... ,
			    output: ... ,
			    data: ... 
		    }
		```
			* dialog.card
		```javascript
		    dialog = {
			    card : {
						    "name": "카드 이름",
						    "id": "default95",
						    "input": [
						        {
						            "text": {
						                "raw": "1",
						                "nlp": "1"
						            }
						        }
						    ],
						    "task": {
						        "name": "defaultTask"
						    },
						    "output": [
						        {
						            "kind": "Content",
						            "text": "챗봇 답변 텍스트입니다.",
						            "buttons": [
						                {
						                    "url": "",
						                    "text": "챗봇 답변 버튼입니다."
						                }
						            ]
						        }
						    ]
					   },
			    userInput : ... ,
			    output: ... ,
			    data: ... 
		    }
		```
		```
		* card는 해당 카드와 관련된 정보가 들어 있습니다.
		* name은 해당 카드의 이름입니다.
		* id는 해당 카드에 대한 식별자 값입니다.
		* input은 해당 카드의 "사용자 입력"란에 저장된 값들(배열)입니다.
		* task는 해당 카드에 등록된 답변 전 실행함수(객체)입니다.
		* output은 해당 카드의 챗봇 답변에 저장된 값들(배열)입니다.
		```
		 * dialog.userInput
		```json
		    dialog = {
			    card : ... ,
			    userInput : {
						        "text": "1",
						        "nlp": [
						            {
						                "text": "1",
						                "pos": "Number",
						                "length": 1
						            }
						        ],
						        "nlpText": "1",
						        "types": {},
						        "entities": {},
						        "intents": []
						   },
			    output: ... ,
			    data: ... 
		    }
		```
		```
		* userInput에는 챗봇 사용자의 입력값과 관련된 정보가 들어있습니다. 
		* text는 챗봇 사용자의 입력값 그 자체입니다.
		* nlp는 챗봇 사용자의 입력값을 자연어처리한 결과값(배열)입니다.
		* nlpText는 챗봇 사용자의 입력값을 자연어처리한 결과를 텍스트화한 값(문자열)입니다.
		* types는 챗봇 사용자의 입력값과 매칭된 타입들이 담겨 있습니다.
		* entities는 챗봇 사용자의 입력값과 관련된 엔터티들이 담겨 있습니다.
		* intents는 챗봇 사용자의 입력값과 관련된 인텐트들이 담겨 있습니다.
		```
		 * dialog.output
		```json
		    dialog = {
			    card : ... ,
			    userInput : ... ,
			    output: [
					        {
					            "kind": "Content",
					            "text": "챗봇 답변 텍스트입니다.",
					            "buttons": [
					                {
					                    "url": "",
					                    "text": "챗봇 답변 버튼입니다."
					                }
					            ]
					        }
					   ],
			    data: ... 
		    }
		```
		```
		* output은 출력될 챗봇 답변들이 들어있습니다.
		* 따라서 output을 수정하면 챗봇 답변을 코드레벨에서 수정할 수 있습니다.
		* kind는 해당 답변의 종류(Content와 Action)를 말합니다. Content는 일반적인 챗봇 답변(text, image, button)을 말하고, Action은 대화흐름조절을 사용한 챗봇 답변을 말합니다. 
		* text는 챗봇의 문자 답변을 말합니다.
		* buttons는 챗봇 답변의 버튼을 말합니다. 
		```
		 * data
		```json
		    dialog = {
			    card : ... ,
			    userInput : ... ,
			    output: ... ,
			    data: {}
		    }
		```
		```
		* data는 비어있는 객체입니다.
		* 챗봇 개발자가 데이터를 저장하고 출력할 때 이용할 수 있는 키(Key)입니다.
		* 한 가지 주의할 점은 `dialog.data['key'] = 'value';`에 저장되는 값은 챗봇을 업데이트할 때 자동으로 사라진다는 점입니다. 따라서 챗봇을 업데이트해도 사라져서 안되는 정보는 `context.session['key'] = 'value';`에 저장해야 됩니다. 또한 	`context.session`에 있는 정보라 할지라도 서버를 재시작하거나 상호작용이 일정 시간동안 없을 경우(세션 만료) 사라집니다. 따라서 사라져서 안되는 정보는 데이터 베이스에 저장해 연동해야 됩니다.
		```
		다음은 dialog 파라미터의 전체적인 모습입니다.
		```json
		    dialog = {
					    "card" : {
								    "name": "카드 이름",
								    "id": "default95",
								    "input": [
										        {
										            "text": {
										                "raw": "1",
										                "nlp": "1"
										            }
										        }
										    ],
								    "task": {
										        "name": "defaultTask"
										    },
								    "output": [
										        {
										            "kind": "Content",
										            "text": "챗봇 답변 텍스트입니다.",
										            "buttons": [
										                {
										                    "url": "",
										                    "text": "챗봇 답변 버튼입니다."
										                }
										            ]
										        }
										     ]
							     },
					    "userInput": {
								        "text": "1",
								        "nlp": [
										            {
										                "text": "1",
										                "pos": "Number",
										                "length": 1
										            }
										       ],
								        "nlpText": "1",
								        "types": {},
								        "entities": {},
								        "intents": []
								     },
				        "output": [
							        {
							            "kind": "Content",
							            "text": "챗봇 답변 텍스트입니다.",
							            "buttons": [
										                {
										                    "url": "",
										                    "text": "챗봇 답변 버튼입니다."
										                }
										           ]
							        }
							     ],
					    "data": {}
				    }
		```

	* context
	context는 해당 카드의 실행과 관련된 정보(dialog)를 넘어선, 챗봇과 사용자 간의 상호작용에 관한 맥락 정보를 JSON 형태로 담고 있습니다. 

		context 파라미터(JSON 객체)는  3가지 key(bot, user, session)를 갖고 있습니다. 
		```json
		    context = {
					    bot : ... ,
					    user : ... ,
					    session: ... 
					  }
		```
		* context.bot
		```json
		    context = {
					    bot :	{
							        name: 'test_sample',
							        description: 'test_sample',
							        created: '2018-02-20T08:34:41.854Z',
							        language: 'ko',
							        options: {
										          use: true,
										          kakao: {},
										          globalSearch: [Object],
										          hybrid: [Object],
										          dialogsetMinMatchRate: 0.5,
										          intentMinMatchRate: 0.5,
										          useQuibble: false 
									         },
							       dialogs: [ [Object], [Object], [Object], [Object] ],
							       commonDialogs: [ [Object], [Object], [Object], [Object] ],
							       tasks: { defaultTask: [Object]},
							       types: { email: [Object] },
				     			   intents: [],
				     			   entities: [],
							       entityContents: [],
							       dialogsets: []
						        },
					    user : ... ,
					    session: ... 
					 }
		```
		```
		* bot은 해당 챗봇에 관한 정보를 담고 있습니다. 
		* name은 해당 챗봇의 이름입니다.
		* description은 해당 챗봇에 관한 설명입니다.
		* created는 해당 챗봇이 생성된 일자입니다.
		* language는 해당 챗봇이 사용하는 언어입니다.
		* options은 해당 챗봇에 관한 설정입니다.
		* dialogs는 해당 챗봇의 대화 시나리오를 JSON 객체의 형태로 담고 있습니다.
		* commonDialogs는 해당 챗봇의 공통 대화 시나리오를 JSON 객체의 형태로 담고 있습니다.
		* tasks는 해당 챗봇에 등록된 모든 답변 전 실행함수들이 담겨 있습니다.
		* types는 해당 챗봇에 등록된 모든 타입들이 담겨 있습니다.
		* intents는 해당 챗봇에 등록된 모든 인텐트들이 담겨 있습니다. 
		* entities는 해당 챗봇에 등록된 모든 엔터티들이 담겨 있습니다.
		* entityContents는 해당 챗봇에 등록된 모든 엔터티 내용들이 담겨 있습니다.
		* dialogsets는 해당 챗봇에 등록된 대화셋들이 담겨 있습니다.
		```
		* context.user
		```json
		    context = {
					    bot : ... ,
					    user : { 
							      userKey: '5a4d91842b7a1e41079c0d9a', 
							      channel: { name: 'socket' }
							   },
					    session: ... 
				      }
		```
		```
		* user는 해당 챗봇 사용자에 관한 정보를 담고 있습니다.
		* userKey는 해당 챗봇 사용자에 대한 식별값입니다.
		* channel은 해당 챗봇 사용자가 챗봇과 대화하고 있는 채널에 관한 정보를 담고 있습니다.
		```
		* context.session
		```json
		    context = {
					    bot : ... ,
					    user : ... ,
					    session:  { 
								     history: [ [Object], [Object] ],
								     dialogCursor: 'default95',
								     previousDialogCursor: 'startDialog'
								  }
				      }
		```
		```
		* session은 챗봇과 사용자간의 상호작용에 관한 데이터를 담고 있으며, 일정 기간(세션) 동안 유지될 데이터를 저장하는 영역입니다. 세션 기간은 5분으로, 5분동안 사용자와 챗봇 간의 상호작용이 없을 경우 세션이 만료됩니다.
		* history는 실행됐던 카드의 목록을 순서대로 담고 있습니다.
		* dialogCursor는 현재 커서가 있는 카드의 id값입니다.
		* previousDialogCursor는 현재 커서 이전에 커서가 놓여있던 카드의 id값입니다.

		* 일정 기간 동안 유지될 데이터를 저장하기 위해서는 context.session['key'] = value; 와 같이 사용합니다.
		```
		다음은 context 파라미터의 전체적인 모습입니다.
		```json
		    context = {
					    bot :	{
							        name: 'test_sample',
							        description: 'test_sample',
							        created: '2018-02-20T08:34:41.854Z',
							        language: 'ko',
							        options: {
										          use: true,
										          kakao: {},
										          globalSearch: [Object],
										          hybrid: [Object],
										          dialogsetMinMatchRate: 0.5,
										          intentMinMatchRate: 0.5,
										          useQuibble: false 
									         },
							       dialogs: [ [Object], [Object], [Object], [Object] ],
							       commonDialogs: [ [Object], [Object], [Object], [Object] ],
							       tasks: { defaultTask: [Object]},
							       types: { email: [Object] },
				     			   intents: [],
				     			   entities: [],
							       entityContents: [],
							       dialogsets: []
						        },
					    user : { 
							      userKey: '5a4d91842b7a1e41079c0d9a', 
							      channel: { name: 'socket' }
							   },
					    session: { 
								     history: [ [Object], [Object] ],
								     dialogCursor: 'default95',
								     previousDialogCursor: 'startDialog'
								  }
					 }
		```
	* callback
	답변 전 실행함수는 비동기(Async)방식으로 구현되기에 반드시 기능 구현이 끝나면 callback을 호출해야 합니다. callback은 기능 구현이 끝났음을 선언하고 결과를 return하는 함수입니다. 따라서 기능 구현이 끝난 부분에 `callback()`을 실행시킵니다.
		* callback(arg1, arg2)
		`callback()` 함수는 두 개의 파라미터를 받을 수 있습니다. 첫번째 파라미터(arg1)는 재질의 여부를 결정하는 값입니다. true 혹은 false를 받습니다. 두 번째 파라미터(arg2)는 첫번째 파라미터가 true일 경우, 재질의 문장을 입력받는 파라미터입니다. 예를 들어 `callback(true, '다시 말씀해주세요.');`라고 입력했을 경우, 답변 전 실행함수가 실행되면 커서는 이동하지 않고 챗봇은 '다시 말씀해주세요.'라고 출력합니다. 더 자세한 예시는 대화 시나리오 가이드를 참고하세요. 

* 복수의 action 함수
	기존에 등록된 함수를 이용함과 동시에 추가적인 기능을 구현한 함수를 등록하고 싶을 경우, action함수에 복수의 함수를 설정할 수 있습니다. 
	```javascript
	var preTask =
	{
		action: function (dialog, context, callback)
		{
			dialog.output[0].text += '\n하하하2';
			callback();
	  	}
	};

	var postAction = function(dialog, context, callback)
	{
		callback();
	}

	bot.setTask('newTask',
	{
		action: [
	           		preTask,	//답변 전 실행 함수 형태
	           		'myTask',   //기존에 등록된 답변 전 실행 함수. 즉, bot.setTask()된 함수.
	           		postAction	//action 함수 형태
	           	]
	});
	```
	* newTask의 경우, action함수로 배열을 받고 있습니다. 배열의 요소는 Task 객체(preTask)이거나 기존에 등록된 함수('myTask')이거나 action 함수(postAction)입니다. 
	* 위와 같이 action함수를 배열로 지정할 경우에, 배열의 순서대로 각 함수가 실행됩니다. 즉, preTask의 action함수가 실행되고, 기존에 등록된 'myTask'의 action함수가 실행된 뒤 postAction가 실행됩니다. 
	* action함수를 배열로 지정하는 경우는 기존에 등록된 함수('myTask')를 이용함과 동시에 등록된 함수 이전에 실행될 함수(preTask) 혹은 등록된 함수가 이후에 실행할 함수(postAction)가 필요할 때 사용함을 기억하세요. 

> **예시 1 - 이름 저장하기**

saveCustomerName 이라는 답변 전 실행 함수(task)를 만듭니다. 

    bot.setTask('saveCustomerName', {
	    action: function (dialog,context,callback) {
	    
		    context.session.customerName = dialog.userInput.text; 
		
		    callback();
		}
	});

* 기능 구현 영역을 보면 자바스크립트 코드를 볼 수 있는데요. `context.session.customerName`에`dialog.userInput.text` 값을 저장합니다. 챗봇 사용자의 입력값(`dialog.userInput.text`)을 일정 기간 유지될 세션(`context.session.customerName`)에 저장합니다.

* 해당 값(`context.session.customerName`)을 챗봇 답변에서 출력하기 위해서는 +변수이름+로 표현해줍니다. 예를 들어, +context.session.customerName+이라고 입력하면 해당 값을 챗봇 답변에서 출력합니다. 

> **예시 2 - 외부 서버에 요청하기 1(크롤링)**

챗봇이 다양한 기능을 수행하기 위해서는 외부 서버의 정보를 이용해야 합니다. 외부 서버의 정보를 이용하기 위해  crawling이라는 이름의 함수를 만들겠습니다. 그 다음 외부 서버에 요청하기 위해서 request.js 와 cheerio(Node.js Module)을 이용하겠습니다. `default.js`파일의 상단에 다음 문구를 추가합니다.

    var request = require('request');
    var cheerio = require('cheerio');

그리고 crawling 실행 함수의 기능 구현 영역에 다음 코드를 추가 합니다.


    var url = 'http://finance.naver.com/item/main.nhn?code=035720';
    request(url, function (err, response, body) 
			     {
				      if(err)
				      {
					      console.log(err);
				      }
		              var $ = cheerio.load(body);
		              var selector = '#content > div.section.invest_trend > div:nth-child(2) > table > tbody > tr:nth-child(2) > td:nth-child(2) > em';
		              var result = $(selector).text();

		              context.session.crawlingResult = result;
		              callback();
				 }
	);

* 챗봇 답변에 +context.session.crawlingResult+ 를 입력하면 해당 값을 출력하게 됩니다. 

> 미션 1 : 대화 형태의 크롤링 구현하기. URL, Selector 사용자 입력을 받아 크롤링하기.

> **예시 3 - 외부 서버에 요청하기 2 (API)**

`var request = require('request')`가 필요 합니다. naverMovieSearch라는 실행 함수를 만들겠습니다. 그리고 기능 구현 영역에 다음 코드를 입력합니다. 
```javascript
   var client_id = 'tXRaAWut2_2R5OkcLpLQ';
   var client_secret = 'TaU4yqU4fI';
   var api_url = 'https://openapi.naver.com/v1/search/movie.json';
   var options = {
       method: "GET",
       url: api_url,
       headers: {'X-Naver-Client-Id':client_id, 'X-Naver-Client-Secret': client_secret},
       qs:{ query: '사건'}
   };
   request(options, function (err, response, body) 
				    {
			           if(err)
			           {
			               console.log(err);
			           }
			     	   body = JSON.parse(body);
			     	   
			           context.session.movieData = body;
			           callback();
			        }
   );
```
* 네이버에서 영화 검색 하는 함수입니다. https://developers.naver.com에 접속해 어플리케이션을 등록하고 client_id와 client_secret 값을 받습니다. 그리고 API 설정에서 '검색'을 추가합니다. 그리고 Documents -> 서비스 API -> 검색 -> 영화로 들어와 API 호출에 대한 정보를 참고 합니다. 
* 네이버에서 전달받은 정보의 형태는 JSON형태입니다. 10개 이상의 영화가 전달 받은 데이터에 배열 형태로 담겨 있습니다. 챗봇 답변에서 배열 형태를 표현하기 위해서는 ###과 같은 문법을 사용합니다. 더 자세한 이야기는 챗봇 답변 파트에서 설명하겠습니다. 

> 미션 2 : 대화 형태의 Naver API 연동 구현하기. 

4. 챗봇 답변

* 챗봇 답변의 구성
시작 카드의 **챗봇 답변**에는 챗봇의 인사말과 함께 자기소개가 입력되어 있습니다. 챗봇이 텍스트로 답변하길 원할 경우, **텍스트**만 입력하고, 좀 더 생생한 브랜드 이미지를 전달하기 위해서는 **이미지**를 사용할 수 있습니다. 또한 챗봇 사용자들의 답변 입력을 편리화하기 위해 카드에 **버튼**을 달 수도 있습니다. 버튼의 경우, 단순한 답변을 위한 버튼일 수도 있지만 URL값을 입력하면 특정 URL로 연결되는 **링크 버튼**을 만들 수도 있습니다. **대화 흐름 조절**은 커서의 이동을 설정하는 기능입니다. 기본적으로 커서는 부모 카드에서 자식 카드로 이동합니다. 커서를 임의의 다른 카드로 이동하고 싶을 때 **대화 흐름 조절**을 이용할 수 있습니다. (더 자세한 설명은 구체적인 예시와 함께 살펴보겠습니다.)

* 챗봇 답변의 추가/삭제
+버튼을 눌러 챗봇 답변을 추가하고, 휴지통 버튼을 눌러 챗봇 답변을 삭제할 수 있습니다.

* 복수의 챗봇 답변(OR 조건)
복수의 챗봇 답변이 지정되어 있을 경우, 복수의 챗봇 답변 중 하나가 랜덤하게 답변됩니다. 예를 들어, 챗봇 답변에 '반가워'와 '반갑습니다.'가 입력되어 있을 경우, 해당 카드가 실행되었을 때 '반가워', '반갑습니다.' 중 하나가 랜덤으로 답변됩니다.

* 변수 접근 - 기능 가이드 챗봇 샘플(챗봇답변_변수)
**챗봇 답변**은 고정된 답변을 해줄 수도 있지만, 많은 경우 고객이 누구냐에 따라 다양한 답변을 할 필요가 있습니다. 예를 들어, 사용자 이름을 입력 받았을 경우에도 해당 사용자의 이름을 언급할 필요가 있습니다. 이를 위해서 사용자이름 대화카드에서 사용자의 입력값을 `context.session.customerName`이라는 변수에 저장했습니다. 이렇게 저장된 변수값을 챗봇 답변에서 사용하고 싶을 경우 `+변수명+`이라고 입력하면 됩니다.  예를 들어, 사용자이름 카드의 챗봇 답변에 "안녕하세요. 반가워요. `+context.session.customerName+`님" 이라고 입력하겠습니다. 그리고 사용자이름 대화카드까지 대화를 이어나가 봅니다.

	* 객체(Object)
변수가 객체일 경우, 자바스크립트와 동일하게 .key 의 형태로 해당 키(key)에 해당하는 값에 접근할 수 있습니다.
예를 들어, +context.session.movieDataObject.date+

	* 배열(Array)
변수가 배열일 경우, ###와 같은 문법을 통해 배열을 for문처럼 접근할 수 있습니다.
예를 들어, context.session.movieDataArray는 배열입니다. 이럴경우, #movieDataArray#와 같이 표현하면 movieDataArray 배열의 각 아이템에 접근합니다. #movieDataArray# 뒤부터는 각 아이템의 key를 통해 해당하는 값에 접근할 수 있습니다. 그리고 하나의 아이템에 대한 접근이 끝났을 경우 #을 붙여줘 끝을 명시해줍니다. 결론적으로 #배열#각 아이템# 형태의 문법입니다. 이 때, 각 아이템 내에서는 +key값+와 같은 형태로 각 아이템의 key와 해당하는 값에 접근할 수 있습니다. 또한 +index+는 각 아이템별로 해당 인덱스 값을 자동으로 반환해줍니다.


* IF (조건에 따른 챗봇답변) - 사랑해 대화카드
**사용자 입력**에서 if의 사용법을 알아봤습니다. **챗봇 답변**에도 동일한 if 기능을 이용할 수 있습니다. 하나의 대화카드에서 조건에 따라 다른 답변을 내놓을 수 있는 기능입니다. 초급 강의에서 챗봇 답변을 여러개 등록 했을 시에 무작위로 챗봇 답변이 선택된다고 말씀드렸습니다. 만약 복수의 챗봇 답변을 등록하고 IF에 조건을 집어 넣으면 조건에 해당되는 챗봇 답변이 실행됩니다. 
이러한 구조는 차후 설명한 배포 채널과 관련 깊습니다. 카카오, 페이스북, 네이버 톡톡 등과 같이 다양한 채널을 하나의 챗봇으로 배포하기 위해서는 각각의 채널에 맞는 형식으로 배포해야 합니다. 따라서 `IF(context.user.channel.name == 'kakao')`일 때, <br/>
`IF(context.user.channel.name == 'facebook')`일 때, <br/>
`IF(context.user.channel.name == 'navertalk')`일 때, <br/>
등과 같이 해당 채널에 따라 챗봇 답변을 다르게 해야 합니다. 


* 대화흐름조절(대화이동)
대화 시나리오의 커서 이동은 기본적으로 부모 카드에서 자식 카드로 진행됩니다. 대화흐름조절은 특정 카드로 커서를 이동시키는 기능입니다.

	* 대화이동
먼저 초급에서 살펴보았던 **대화이동**이 있습니다. 대화 이동의 경우,  이동 후 대화 카드의 실행함수가 실행되고  이동 전 대화 카드의 텍스트가 출력됩니다. 그리고 커서는 이동 후 대화카드를 가리킵니다.

	* 다시 질문하기
**다시 질문하기**는 챗봇 사용자의 입력값에 부합하는 자식 카드가 없을 경우, 커서가 이동하지 않고 챗봇 답변을  재실행하는 기능입니다. 예를 들어, 다시 질문하기 실행 카드에서 챗봇 답변으로 '번호를 입력하세요'라고 했습니다. 이 때 사용자가 핸드폰 번호 형식이 아닌 엉뚱한 답변을 할 경우, 사용자의 입력값에 부합하는 자식 대화 카드가 없습니다. 따라서 챗봇은 '알아듣지 못했습니다'를 출력합니다. 하지만 핸드폰 대화 카드의 막내 대화카드로 **사용자 입력**에는 if(true)를, **챗봇 답변**에는 **다시 질문하기**를 설정하면 사용자의 입력값에 부합하는 자식 대화 카드가 없을 때, 핸드폰 재질의 카드가 실행되면서 커서는 핸드폰 대화카드에 남아있습니다. 그리고 핸드폰 재질의 카드의 텍스트를 출력합니다. 핸드폰 재질의 카드의 챗봇 답변에 '핸드폰 번호 형식에 맞게 다시 한 번 입력해주세요.'라고 입력하면 결과적으로 재질의하는 효과를 가져옵니다. 이처럼 재질의 기능은 주로 사용자 입력에 if(true)와 같이 사용되어 막내 대화카드에 위치합니다. 결국 부모로 대화이동하는 기능이 재질의 기능입니다.

	* 이전 대화이동
**이전 대화이동**은 주로 대화상에서 '이전'이라고 입력했을 때 이전에 실행된 카드로 커서가 이동하는 기능을 말합니다. '이전'이라고 말했을 때 기본적으로 이전 카드로 이동하는 것은 *공통 대화 시나리오* 기능으로 구현된 것입니다. 여기서 주의할 점은 '이전 대화이동' 기능이 있는 카드가 실행됐을 경우, 해당 카드를 기준으로 2단계 부모(조부모) 카드로 커서가 이동한다는 것입니다.

	* 대화이동 후 검색
**대화이동 후 검색**은 대화이동 후 이동한 카드의 자식들을 대상으로 검색하는 기능입니다. 부합하는 사용자 입력이 있을 시 해당 자식 카드가 실행되고 없을 경우, '답변을 알아들을 수 없습니다'로 답변합니다. 

	* 돌아가기용 대화이동 / 돌아가기
**돌아가기용 대화이동**은 대화이동과 동일하게 작동합니다. 다만 대화이동한 후 특정 카드에서 돌아가기 기능을 실행했을 시, 돌아가기용 대화이동을 실행했던 카드의 부모 카드로 커서가 이동합니다. 

> 미션3 : 핸드폰 인증 챗봇 만들기.

5. 단축키 (Shortcuts)
* 대화 시나리오
	- ← ↓ ↑ → : Navigate Dialog  
	- Ctrl + ↑ → : Move Dialog Up/Down  
	- Enter : Open Edit Dialog  
	- Esc : Cancel Edit  
	- Insert : Add child dialog  
	- Del : Delete Dialog  
	- Space : Expand/Collapse Child Dialog  

* 카드 수정창
	- Tab : Next (Input, Task, Output 전환, Input 등 여러 개 인경우 한줄씩 이동)  
	- Ctrl+Enter : Save Dialog Modal  

* js Code Editor
	- Alt+← : Back (Dialog Graph에서 Code Editor로 온 후에 복귀)  

* 공통
	- / : Search Box  
	- Ctrl+S : Save File  
	- Ctrl+Z : Undo  
	- ? : keyboard shortcut help  

#### 관리
1. 대화 시나리오
대화 시나리오 관련 파일은 기본적으로 3가지(*.bot.js 파일, *.graph.js 파일, *.js파일)입니다.

* *.bot.js 파일 - 봇에 관한 옵션을 설정하는 파일입니다. 해당 파일은 복수로 만들 수 없습니다.
* *.graph.js 파일 - 대화 시나리오 그래프를 JSON 객체형태로 저장하고 있는 파일입니다. 대화 시나리오 관리 메뉴에서 복수의 대화 시나리오 그래프 파일을 만들 수 있습니다. 복수의 대화 시나리오 그래프 파일이 있을 경우, 각각의 대화 시나리오는 시작 카드의 자식 카드로 합쳐지고, 시나리오 사이의 우선순위를 설정할 수 있습니다. 
* *.js 파일  - 답변 전 실행 함수를 설정하는 파일입니다. 대화 시나리오 관리 메뉴에서 복수의 답변 전 실행함수 파일을 만들 수 있습니다. 

2. 엔터티
엔터티를 생성, 수정, 삭제할 수 있는 메뉴입니다.
* 불러오기를 클릭했을시 엑셀파일로 엔터티를 등록할 수 있습니다. 
* 엑셀파일로 엔터티 등록시 관련 양식을 주의하세요. 엔터티 등록 엑셀 양식은 "불러오기"버튼을 눌러 다운로드 할 수 있습니다.

3. 인텐트
인텐트를 생성, 수정, 삭제할 수 있는 메뉴입니다.
* 불러오기를 클릭했을시 엑셀파일로 인텐트를 등록할 수 있습니다. 
* 엑셀파일로 인텐트 등록시 관련 양식을 주의하세요. 인텐트 등록 엑셀 양식은 "불러오기"버튼을 눌러 다운로드 할 수 있습니다.

4. 테스크
테스크를 생성, 수정, 삭제할 수 있는 메뉴입니다.

### 대화셋(DialogSet)
챗봇은 대화 시나리오와 대화 셋 두가지 방법으로 구성될 수 있으며, 함께 사용하는 것도 가능합니다. 대화 셋은 질문과 답변으로 이루어진 데이터 쌍을 통해 챗봇을 학습시키는 방법입니다. 대화셋을 통해 챗봇을 구성할 경우, 챗봇 사용자가 특정 문장을 입력했을 때, 가장 유사도가 높은 질문을 찾아 답변을 출력합니다(Retreival 방식).

* 대화 시나리오와 대화셋을 같이 사용하였을 경우에는, 대화 시나리오가 답변에서 우선순위를 가집니다.  
* 대화셋은 기본대화셋과 추가대화셋으로 나뉘어져있고, 기본대화셋은 작성 즉시 적용되며, 추가 대화셋은 추가적으로 연결/해제가 가능합니다.
* FAQ 위주의 챗봇을 구축할 경우, 이용할 수 있는 방법입니다.

#### 개발
1. 기본 대화셋
기본 대화셋을 작성하기 위해서는 왼쪽 네비게이션 바의 "개발" -> "대화 셋"을 클릭하세요. 질문과 그에 대한 답변을 입력하고, 질문의 카테고리를 입력해주세요. 

* 대화셋의 질문과 답변 각각을 복수로 입력할 수 있습니다. 질문을 복수로 입력할 경우, 복수의 질문들은 OR조건으로써 복수의 질문 중 어느 값을 사용자가 입력해도 해당 질문의 답변이 출력됩니다. 또한 복수의 답변을 입력할 경우, 챗봇 사용자가 해당 질문을 입력했을 때 복수의 답변들 중 하나가 랜덤하게 출력됩니다. 

2. 추가 대화셋
추가 대화셋을 작성하기 위해서는 기본 대화셋 오른쪽 "+"탭을 클릭하세요. 대화셋 선택의 "새로 만들기" 버튼을 클릭하여 추가대화셋을 등록합니다. 추가 대화셋은 왼쪽 네비게이션 바의 "관리" -> "대화 셋"에서 "새로 만들기" 버튼을 클릭하여 등록할 수도 있습니다. 

* 추가 대화셋을 관리하기 위해서는 왼쪽 네비게이션 바의 "개발" -> "대화 셋"에서 +버튼을 눌러 추가 대화셋을 열고 그 내용을 수정합니다.

#### 관리

1.  대화셋 파일 가져오기
질문과 답변을 일일이 입력하는 것이 아니라, 엑셀파일(xlsx)이나 csv파일로 불러오기(import)할 수 있습니다. 다만 엑셀파일이나 csv 파일로 불러올 시에는 데이터 양식을 주의하세요.

* 데이터 양식은 불러오기 버튼을 클릭하고 양식 다운로드 버튼을 클릭하면 내려받을 수 있습니다.
* 엑셀파일의 데이터 양식은 다음과 같습니다. 1열부터 3열까지는 각 질문 답변의 카테고리를 적습니다. 1열은 대분류, 2열은 중분류, 3열은 소분류로 이용할 수 있습니다. 카테고리 값은 필수 입력값은 아닙니다. 4열은 질문을, 5열은 그에 대한 답변을 입력합니다. 질문과 답변은 필수 입력값으로 둘 중 하나라도 비어있을 시에 해당 질문과 답변은 학습하지 않습니다. 
* 제목 : 대화셋 제목을 입력해주세요. 해당 대화셋에 대한 식별자 값입니다.
* File : 불러오기 할 파일을 업로드해주세요.
* 컨텐츠 : 대화셋에 대해 설명해주세요.

2.  추가 대화셋 설정
추가 대화셋을 등록하면 대화셋 관리 화면에서 대화셋 리스트에 표시되지만 챗봇에 연결된 것은 아닙니다. 추가 대화셋을 사용하기 위해서는 사용하고자 하는 대화셋 오른쪽 "사용하기"버튼을 클릭하세요. 이후 연결을 끊고 싶으면 다시 버튼을 누르면 연결이 끊어집니다.
추가 대화셋의 제목, 컨텐츠는 대화셋 관리화면의 설정 아이콘을 클릭해 수정할 수 있고, 휴지통 버튼을 눌러 삭제할 수 있습니다. 

### 채널
현재 플레이챗은 카카오톡, 페이스북, 네이버톡톡, 라인, 위챗 등의 채널을 지원합니다. 사용자는 원하는 채널들에 개발한 챗봇을 연결하여 직접 서비스 할 수 있습니다.

#### 카카오
카카오톡에 챗봇을 배포하기 위해서는 다음 단계를 수행하세요.

1.  카카오 옐로아이디를 만듭니다.([https://yellowid.kakao.com/login](https://yellowid.kakao.com/login))
2.  옐로아이디 프로필을 만들고 심사를 기다립니다.(5일 이내 소요)
3.  심사된 프로필로 옐로아이디 페이지 자동응답 탭으로 들어갑니다.
4.  API 자동응답 설정하기로 들어갑니다.
5.  앱 이름, URL, 설명, 전화번호를 설정합니다.

자세한 설명 및 앱 URL은 "배포"메뉴의 카카오톡 로고 아래의 "메신져봇 생성" 버튼을 클릭하면 확인할 수 있습니다.
#### 페이스북
플레이챗에서는 페이스북 자동 연결을 제공합니다. 페이스북 로고 아래의 "연결하기" 버튼을 클릭하고 연결하고 싶은 자신의 페이지를 연결하세요. (페이지가 없으면 새로 페이지를 만들어야 합니다.)

#### 네이버 톡톡
-   네이버톡톡 파트너센터 접속 (partner.talk.naver.com)
-   회사 단체아이디 또는 대표성있는 개인아이디로 로그인
-   내 계정관리 \> 새로운 톡톡 계정 만들기 클릭
-   서비스 선택하기에서 서비스 선택없이 서비스 연결 나중에 하기 클릭!
-   테스트 계정생성시 개인을 선택, 서비스 계정생성시 사업자 또는 기관/단체을 선택 후 다음 대표이미지, 프로필명, 휴대폰 번호 등 정보를 입력 후 사용신청하세요.
-   생성된 계정은 검수중 상태이며, 검수가 완료되면 사용중상태로 변경되고 SMS로 알림 전송됩니다.
-   내 계정관리의 등록된 계정 리스트에서 계정관리로 계정 홈을 클릭하세요.
-   좌측 메뉴 챗봇 API 하위 API 설정 메뉴를 통해 이용약관동의 및 챗봇을 설정하세요. (beta기간에는 등록신청 필요)
-   네이버의 API사용 승인이 된 후 playchat에서 제공하는 URL을 입력하여 연결하세요.

#### 라인
라인에 챗봇을 배포하기 위해서는 다음 단계를 수행하세요.

1.  LINE회원이어야해요 LINE 앱 또는 웹으로 회원가입해요
2.  가입이 됐다면 LINE Business Center에서 사용할 이메일을 등록해요
3.  서비스 탭에서 Messaging API 시작하기 버튼을 누르고 정보를 입력해요
4.  LINE Manager에서 API 켜기 버튼을 누르고 Webhook 사용을 허용하고 저장해요
5.  LINE Business Center에서 계정 목록 탭으로 이동해요
6.  Messaging API에 있는 LINE Developers 버튼을 눌러요
7.  ISSUE 버튼을 눌러 Channel access token을 발급받아요
8.  EDIT 버튼을 눌러 Webhook URL을 아래의 Webhook URL을 복사해 넣고 저장 및 확인해요

자세한 설명 및 Webhook URL은 "배포"메뉴의 라인 로고 아래의 "메신져봇 생성" 버튼을 클릭하면 확인할 수 있습니다.

#### 위챗
-   Wechat 개인 계정번호가 있어야 합니다. 없으면 휴대폰에서 wechat app 다운로드 후 신청해주세요.
-   https://mp.weixin.qq.com/ 에 가서 상단의 “WeChat Official Accounts“을 신청하세요.
-   신청 후 "Basic configuration“라는 버튼 클릭하세요. 그 다음 오른 쪽에 있는 "I agree” 앞에 체크를 하시고, “Become a developer“라는 버튼 클릭하세요.
-   “Change Configuration” 라는 버튼 클릭하세요. 입력칸에는 Playchat 페이지 왼쪽 메뉴 중 Channel를 클릭하고 wechat의 연결버튼을 눌렀을 때 안내되는 URL을 입력하시면 됩니다. 그후, Token에는 moneybrain_token 이라고 입력하세요.
-   그리고 Encoding AESKey는 Encoding AESKey 뒤에 있는 “Random Generation“라는 버튼을 클릭하면 자동적으로 생성됩니다. 그 후, “Change Configuration” 라는 버튼 옆에 있는 “Enable“라는 버튼을 클릭하세요.
-   휴대폰 WeChat 어플리케이션을 실행한 후, "Add Contact" 에 있는 “Official Accounts “버튼을 클릭하세요. 검색창에 Wechat에서 주어진 나의 “WeChat Official Accounts “를 찾으면 완료!

### 운영
PlayChat은 실패한 대화를 확인하고, 실패한 대화를 학습하여 챗봇이 말을 더 잘 할 수 있게 하는 운영 관리 기능을 제공합니다. 운영 -> 사용자 메뉴에서는 해당 챗봇과 대화한 사용자들에 관한 정보를 열람할 수 있는 기능을 제공하며, 운영 -> 실패대화 메뉴에서는 챗봇이 실패한 대화를 열람하고, 이를 학습시키는 기능을 제공합니다.

#### 사용자
* 챗봇을 이용한 사용자에 대한 정보를 채널, 식별값, 마지막 대화, 첫 대화, 대화수, 상세보기 목록으로 보여줍니다. 

* 오른쪽 상위에 고급검색 기능을 이용하면 채널, 식별값, 마지막 대화, 첫 대화, 대화수를 이용하여 특정 사용자를 검색할 수 있습니다.

* 목록의 상세보기를 클릭하면 오른쪽 대화창에서 해당 사용자가 챗봇과 대화한 내역을 대화형태로 볼 수 있습니다.

* 해당 사용자에 대한 메모를 입력할 수 있습니다.

#### 실패대화 학습
실패한 대화를 학습할 때에는 대화 셋, 대화 시나리오, 인텐트 세 가지 방식으로 학습할 수 있습니다. 
1. 대화 셋
* 실패 대화를 빈도 순으로 보여줍니다.
* 실패 대화의 질문(챗봇 사용자의 입력값)과 기존 대화 셋에 학습되어 있는 유사한 질문을 추천해줍니다.
* 실패 대화의 답변을 입력하면 기존 대화 셋에 학습되어 있는 답변 중 유사한 답변을 추천해줍니다.
* 무시하기 버튼을 누르면 해당 실패대화를 실패대화 목록에서 삭제합니다.

2. 대화 시나리오
* 실패 대화를 빈도 순으로 보여줍니다.
* 실패 대화가 발생한 위치의 카드(이전 대화)와 실패한 사용자의 입력값, 빈도를 목록으로 보여줍니다.
* 대화 시나리오 바로가기 버튼을 누르면 실패 대화가 발생한 위치의 카드의 자식 카드를 생성할 수 있도록 도와줍니다. 
* 무시하기 버튼을 누르면 해당 실패대화를 실패대화 목록에서 삭제합니다.

3. 인텐트
의도분석 대화학습에서는, 대화가 실패했을 때, 인텐트를 모아 보여줍니다. (대화 실패 : 기본 Dialog 발생)  
표의 실패 인텐트는 "추천 인텐트"를 뜻합니다. 오른쪽의 대화 수정 버튼을 누르면, 실패한 인텐트 들이 나옵니다. 실패한 인텐트들 중 추천 인텐트와 같은 의미를 가진다고 판단되는 것들을 체크하여 추가하면, 인텐트가 업데이트 됩니다.

### 분석
PlayChat에서는 봇에 대한 기본적인 분석을 제공하고 있으며, 웹 상으로 쉽게 확인할 수 있습니다. 분석은 크게 사용자에 대한 분석과 대화에 관한 분석이 있습니다. 

* 사용자에 관한 분석은 일별 사용자, 채널별 사용자가 있으며, 사용자 단위를 세션으로 설정해 분석한 자료도 제공합니다.
* 사용자에 관한 분석은 또한 사용자의 입력에 관한 자료를 대화셋, 대화 시나리오, 인텐트 기준으로 제공합니다.
* 대화에 관한 분석은 대화량과 대화의 구체적 내용을 대화셋, 대화 시나리오 별로 제공합니다. 
* 대화에 관한 분석은 또한 대화의 흐름을 통계로 보여주며, 실패 대화에 관한 통계를 제공합니다. 
* 사용자와 대화에 관한 통계는 모두 기간을 설정하여 엑셀파일로 다운로드할 수 있습니다.

#### 요약
요약에서는 챗봇 사용에 관한 통계에 핵심이 되는 자료를 핵심적으로 보여줍니다.

* **실시간 이용자**는 최근 5분 이내에 해당 챗봇과 대화한 사용자 수를 보여줍니다. 
*  **이용자 (30일)**은 최근 30일 동안의 해당 챗봇과 대화한 사용자의 총 수를 의미합니다.
* **대화량 (30일)**은 최근 30일 동안의 해당 챗봇의  총 대화 횟수를 의미합니다. 
* **누적 이용자**는 해당 챗봇과 대화한 사용자의 총 수를 의미합니다.
* **누적 대화량**은 해당 챗봇의 총 대화 횟수를 의미합니다. 대화 횟수는 사용자 입력과 그에 대한 챗봇 답변을 1회로 계산합니다.
* **일자별 대화량**은 최근 30일 동안의 일자별 대화 횟수를 보여줍니다. 대화 횟수는 사용자 입력과 그에 대한 챗봇 답변을 1회로 계산합니다.
* **채널별 이용자 분포**는 최근 30일 동안의 채널별 이용자 분포를 보여줍니다.
* **대화 성공률**은 최근 30일 동안의 대화성공(챗봇이 준비된 답변을 한 경우)과 대화실패(답변 없음 카드의 챗봇 답변을 출력한 경우)의 비율을 보여줍니다.
* **사용자 입력 TOP 10**은 최근 30일 동안의 챗봇 사용자의 입력값을 빈도순으로 보여줍니다. 챗봇 사용자들이 어떤 입력을 주로 사용하는지 확인할 수 있습니다.
* **대화 실패 TOP 10**은 최근 30일 동안의 실패한 대화(답변 없음 카드의 챗봇 답변을 출력한 경우)를 빈도순으로 보여줍니다. 챗봇과의 대화가 어떤 사용자 입력에 대해 대화 실패를 많이 하는지 확인할 수 있습니다.
* **시나리오 사용량TOP 10**은 최근 30일 동안의 대화 시나리오 사용량을 보여줍니다. 챗봇 사용자들이 주로 어떤 대화 시나리오를 많이 이용하는지 확인할 수 있습니다. 

#### 사용자
사용자에서는 챗봇 사용자에 대한 일별 통계, 채널별 사용자 분포를 보여줍니다.
* 일별 사용자 통계는 각 채널별로 일별 사용자 통계를 나타냅니다. 막대 그래프의 채널 이름을 클릭하면 해당 채널이 제외된 통계를 볼 수 있습니다.
* 채널별 사용자 통계는 각 채널별 사용자 분포를 보여줍니다. 도넛 그래프의 채널 이름을 클릭하면 해당 채널이 제외된 분포를 볼 수 있습니다.

#### 세션
세션에서는 챗봇 사용자에 대한 일자별 통계를 세션단위로 보여줍니다.
* 세션은 5분으로 설정되어 있습니다. 5분동안 챗봇과 대화하지 않을 경우, 해당 사용자는 새로운 세션으로 분석됩니다. 
* 일별 세션은 각 채널별로 일별 세션 통계를 나타냅니다. 막대 그래프의 채널 이름을 클릭하면 해당 채널이 제외된 통계를 볼 수 있습니다.
* 세션당 평균 대화량은 한 세션당 챗봇과의 대화량을 의미합니다. 챗봇 사용자가 챗봇과 한 번 대화할 때 평균적으로 몇 번의 대화를 나누는지 알 수 있습니다. 

#### 사용자 입력 - 대화셋
대화셋의 답변이 출력된 경우에 한해 사용자들의 입력값 빈도를 보여줍니다. 어느 질문과 답변이 많이 이용돼었는지 그리고 해당 답변이 출력되게 한 사용자들의 입력값은 어떤 것들이 있었는지 확인할 수 있습니다. 

#### 사용자 입력 - 대화 시나리오
대화 시나리오의 카드가 실행된 경우에 한해 사용자들의 입력값 빈도를 보여줍니다. 어느 카드가 많이 이용되었는지 그리고 해당 카드가 실행되게 한 사용자들의 입력값은 어떤 것들이 있었는지 확인할 수 있습니다.

#### 사용자 입력 - 인텐트


#### 대화량
대화량에서는 챗봇과의 대화량과 대화의 성공, 실패를 기간별로 보여줍니다. 또한 대화의 채널별 분포도 함께 보여줍니다.

* **일별 대화량** 통계는 각 채널별로 대화 통계를 나타냅니다. 막대 그래프의 채널 이름을 클릭하면 해당 채널이 제외된 통계를 볼 수 있습니다.
* **일별 대화 성공/실패** 통계는 각 채널별로 대화 성공, 실패 통계를 나타냅니다. 막대 그래프의 채널 이름을 클릭하면 해당 채널이 제외된 통계를 볼 수 있습니다.
* **채널별 대화** 통계는 각 채널별 대화 분포를 보여줍니다. 도넛 그래프의 채널 이름을 클릭하면 해당 채널이 제외된 분포를 볼 수 있습니다.

#### 대화량 - 대화셋
대화셋의 답변이 출력된 경우에 한해 챗봇 답변의 빈도를 보여줍니다. 사용자에게 어떤 챗봇 답변이 많이 출력됐는지 확인할 수 있습니다.

#### 대화량 - 대화 시나리오
대화 시나리오의 카드가 실행된 경우에 한해 카드 이용 빈도를 보여줍니다. 사용자에게 어떤 카드의 챗봇 답변이 많이 출력됐는지 확인할 수 있습니다. 

#### 대화 경로
대화 시나리오의 어떤 대화흐름(커서의 이동)이 많이 이용되었는지 보여줍니다. 

#### 실패 대화
실패 대화의 사용자 입력값을 빈도 순으로 보여줍니다. 

### 테스트
개발한 챗봇을 PlayChat 페이지에서 실시간으로 테스트할 수 있습니다. 테스트를 통해 챗봇이 구상대로 작동하는지 확인하고 수정하세요. 챗봇 테스트는 대화창을 통해 대화하는 동시에 로그창을 확인하며 진행할 수 있습니다.

#### 대화창
화면 오른쪽에 대화창이 준비되어있습니다. 대화창에서 챗봇과 실제로 대화하며 원하는 답변을 출력하는지 확인 할 수 있습니다. 대화 시나리오 화면을 열어놓고 대화를 진행하면, 현재 활성화되어있는 카드가 하이라이트 표시됩니다.

* 대화창 왼쪽 상단의 동그란 화살표를 클릭하면 봇이 업데이트 됩니다. 대화 시나리오의 변동사항이 봇에 반영됩니다.
* 대화창 오른쪽 상단의 X를 클릭하면 대화창을 안 보이게 할 수 있습니다.

#### 실시간 대화 분석
화면 아래쪽에 실시간 대화 분석창이 준비되어 있습니다. 대화창에서 챗봇과 대화하며 실시간으로 챗봇 사용자의 입력값과 그에 해당되는 인텐트와 엔터티, 그리고 실행 함수와 챗봇 답변에 대한 분석을 확인할 수 있습니다.
1. 사용자 입력 분석
* 사용자 입력 : 챗봇 사용자가 입력한 원문 그대로의 값
* 자연어 처리 : 챗봇 사용자의 입력을 자연어 처리한 결과를 보여줍니다.
* 자연어 분석 : 챗봇 사용자의 입력을 자연어 처리한 결과의 구체적 내용(품사)을 보여줍니다.

2. 인텐트 분석
매칭된 인텐트의 이름과 일치율을 보여줍니다. 일치율은 0에서 1값입니다.

3. 엔터티 분석
챗봇 사용자의 입력값에서 등록된 엔터티가 있을 경우, 해당 엔터티를 보여줍니다. 

5. 답변 전 실행 함수

6. 챗봇 답변 분석
챗봇 답변 분석에서는 대화 셋이 실행되었을 경우에는 어떤 대화셋이 실행됐는지에 관한 정보를 보여주며, 대화 시나리오가 실행되었을 경우에는 어떤 카드가 실행됐는지에 관한 정보를 보여줍니다.









