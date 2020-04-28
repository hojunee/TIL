---
description: 인생은 B(Birth)와 D(Death)사이의 C(Chicken)!
---

# 생성자와 소멸자 \(init/deinit\)

**프로퍼티 초기값**

* 스위프트의 모든 인스턴스는 초기화와 동시에 모든 프로퍼티에 유효한 값이 할당되어 있어야 함
* 클래스 프로퍼티에 미리 기본값을 할당해두면 인스턴스가 생성됨과 동시에 초기값을 지니게 됨

**생성자\(init\)**

* 초기화 단계에서 생성자를 사용해 초기화하는 것도 가능하다
* 이는 Designated Init\(지정 생성자\)로서, 모든 값에 대한 초기화를 진행해주어야 함

```swift
class Person {
	var name: String
	var age: Int
	var address: String

	init(name: String, age: Int, nickName: String) { // 생성자!
		self.name = name
		self.age = age
		self.address = address
	}
}
```

**만약 프로퍼티의 초기값이 꼭 필요 없다면?**

* Optional을 사용!
* Convenience init\(편의 생성자\) 사용 → 일부만 초기화 가능

```swift
class Person {
	var name: String
	var age: Int
	var address: String

	init(name: String, age: Int, nickName: String) { // 생성자!
		...
	}

	convenience int(name: String, age: Int, address: String) {
		init(name: name, age:age) // 이미 있는 init을 사용하는 구조
		self.address = address
	}
}
```

* Implicit Optional은 인스턴스 사용에 꼭 필요하지만 초기값을 할당하지 않을 때 사용

```swift
class Cat {
	var name: String
	var owner: Person! // implicit optional
}
```

소멸자**\(deinit\)**

* 클래스의 인스턴스가 메모리에서 해제되는 시점에 호출
* deinit은 **매개변수를 지닐 수 없다**
* **class** type에만 구현가능

```swift
class Person {
	var name: String
	var age: Int
	var address: String

	init(name: String, age: Int, nickName: String) { // 생성자!
		...
	}

	deinit {
		if let petName = pet?.name {
			print("\\(name)가 \\(child.name)에게 \\(petName)를 인도합니다."
			self.pet?.owner = child
		}
	}
}
```

