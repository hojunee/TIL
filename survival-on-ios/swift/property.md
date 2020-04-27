---
description: 클래스만 있던 시절의 field가 그립다 그리워!
---

# Property

**struct, class, enum 내부에 구현할 수 있는 변수\(attribute\)**

**연산 프로퍼티**를 위주로 봐주자!

## 종류

### 인스턴스 저장 프로퍼티

* 어떤 값을 저장하기 위한 프로퍼티



### 인스턴스 **연산** 프로퍼티

* 자신이 가지고 있는 저장 프로퍼티를 통해 값을 알아서 변환시켜주는 프로퍼티

Example\)

```swift
struct Student {
	// 저장 프로퍼티
	var name : String = "Hojun Lee"
	var koreanAge : Int = 0
	
	// 연산 프로퍼티
	var westernAge : Int {
		get {
			return koreanAge - 1
		}

		set(inputValue) { // 안써주게 되면 `newValue`라는 이름으로 implicit하게 들어옴
			koreanAge = inputValue + 1
		}
	}
}
```

* 타입\(==static\) 저장 프로퍼티

```swift
static var typeDescription : String = "학생"
```

* Read-only 인스턴스 **연산** 프로퍼티

```swift
var selfIntroduction : String {
	get {
		return "저는 \\(self.name)입니다"
	}
}
```



* 지역/전역 변수에도 Operation을 사용하여 정의할 수 있다!

