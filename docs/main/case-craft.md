---
layout: default
title: CaseCraft
parent: OLOSIA Main
nav_order: 6
---

# CaseCraft
{: .fs-7 }

Snake case To Camel case Online Converter
{: .fs-5 .fw-300 }

DB 컬럼 (snake_case) 기준으로, camelCase 변수를 생성하는 서비스를 소개해드립니다.

프로그래밍 언어별 조각코드 생성에 활용해보세요.

입력하신 정보는 올로시아 서버에 전송하거나 저장하지 않습니다.

[CaseCraft 바로가기](https://olosia.com/case-craft){:target="_blank" .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

![case-craft-pc](/assets/images/main/case-craft_ko.png)




<br /><br /><br />
## 프로그래밍 언어별 조각코드 생성 예

![case-craft-excel](/assets/images/main/case-craft_excel.png)

Tab 으로 구분된 테이블 컬럼 정보를 복사해서 입력합니다.

### 입력 테이블 컬럼 정보
    seq	int(11)	N	Y	Sequence
    user_id	varchar(15)	N	N	User identification
    user_email	varchar(50)	Y	N	User E-mail
    del_fg	bit(1)	N	N	Delete flag
    create_date	timestamp	N	N	Date of creation

언어 / 기능별 메뉴와 옵션을 선택하시면, 다양한 조각코드를 생성하실 수 있습니다.


Java Variable
```java
public int seq = 0;	// Sequence
public String userId = null;	// User identification
public String userEmail = null;	// User E-mail
public boolean delFg = false;	// Delete flag
public LocalDateTime createDate = null;	// Date of creation
```

Java Entity
```java
public class OlosiaCom {
	private int seq;
	private String userId;
	private String userEmail;
	private boolean delFg;
	private LocalDateTime createDate;

	public OlosiaCom (int seq, String userId, String userEmail, boolean delFg, LocalDateTime createDate) {
		this.seq = seq;
		this.userId = userId;
		this.userEmail = userEmail;
		this.delFg = delFg;
		this.createDate = createDate;
	}
}
```

Javascript Variable
```javascript
let seq        = 0    ;	// Sequence
let userId     = ''   ;	// User identification
let userEmail  = ''   ;	// User E-mail
let delFg      = false;	// Delete flag
let createDate = ''   ;	// Date of creation
```

Javascript Class
```javascript
class OlosiaCom {
	constructor(seq, userId, userEmail, delFg, createDate) {
		this.seq = seq;
		this.userId = userId;
		this.userEmail = userEmail;
		this.delFg = delFg;
		this.createDate = createDate;
	}
	getSeq() {
		return this.seq;
	}
	getUserId() {
		return this.userId;
	}
    ...
```

Typescript Variable
```typescript
let seq       : number  = 0    ;	// Sequence
let userId    : string  = ''   ;	// User identification
let userEmail : string  = ''   ;	// User E-mail
let delFg     : boolean = false;	// Delete flag
let createDate: string  = ''   ;	// Date of creation
```

SQL Select
```sql
SELECT /*  */
       seq,
       user_id,
       user_email,
       del_fg,
       create_date
  FROM olosia_com
 WHERE 1 = 1
   AND seq = :seq
   AND user_id = :userId
   AND user_email = :userEmail
   AND del_fg = :delFg
   AND create_date = :createDate
```




<br /><br /><br />
## 유형별 문자열 변환 예제

### PascalCase
> 구분 기호 없이 각 단어의 첫 문자를 대문자로 변환합니다.

    "test string" => "TestString"

### camelCase
> 각 단어의 첫 문자를 대문자로 변환한 다음 첫 번째 문자를 소문자로 표시합니다.

    "test string" => "testString"

### snake_case
> 단어 사이에 밑줄이 있는 소문자 문자열로 변환합니다.

    "test string" => "test_string"

### CONSTANT_CASE
> 단어 사이에 밑줄이 있는 대문자 문자열로 변환합니다.

    "test string" => "TEST_STRING"

### param-case
> 단어 사이에 대시가 있는 소문자 문자열로 변환합니다.

    "test string" => "test-string"

### Header-Case
> 대시로 구분된 대문자 단어 문자열로 변환합니다.

    "test string" => "Test-String"

### dot.case
> 단어 사이에 마침표가 있는 소문자 문자열로 변환합니다.

    "test string" => "test.string"

### path/case
> 단어 사이에 슬래시가 있는 소문자 문자열로 변환합니다.

    "test string" => "test/string"

### no case
> 단어 사이에 공백이 있는 소문자 문자열로 변환합니다.

    "testString" => "test string"

### Capital Case
> 각 단어를 대문자로 하여 공백으로 구분된 문자열로 변환합니다.

    "test string" => "Test String"

### Sentence Case
> 단어 사이에 공백이 있는 소문자로 변환한 다음 첫 번째 문자를 대문자로 표시합니다.

    "testString" => "Test string"

### lower case
> 문자열을 소문자로 변환합니다.

    "TEST STRING" => "test string"

### UPPER CASE
> 문자열을 대문자로 변환합니다.

    "test string" => "TEST STRING"

### lOWER cASE fIRST
> 첫 번째 문자가 소문자인 문자열로 변환합니다.

    "TEST" => "tEST"

### Upper Case First
> 첫 번째 문자가 대문자인 문자열로 변환합니다.

    "test" => "Test"

### sPoNGe CaSE
> 임의의 대소문자가 적용된 문자열로 변환합니다.

    "Test String" => "tEst stRINg"

### sWAP cASE
> 대문자는 소문자로, 소문자는 대문자로 문자열을 변환합니다.

    "Test String" => "tEST sTRING"

### Title Case
> 영어 규칙에 따라 문자열을 제목 케이스로 변환합니다.

    "a simple test" => "A Simple Test"