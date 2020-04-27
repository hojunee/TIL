---
description: Swift에서 자료형을 어떻게 다루면 좋을까? - is / as
---

# Type Casting

### is

* 타입 체크 연산자
* **인스턴스가 특정 서브클래스 타입인지 Check** \(with if, switch\)

### as

* Downcasting에 사용
* 어떤 클래스의 인스턴스는 실제로는 그 서브클래스의 인스턴스인 경우인 상황이 있음.
* 이 상황에서 **클래스→서브클래스 로의 타입변환** : Downcasting
* 실패할 수도 있어서 옵셔널\(?, !\)와 함께 사용한다.

