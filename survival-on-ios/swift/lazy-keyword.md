---
description: "지금까지 이런 키워드는 없었다...! 전지적 효율 시점 \U0001F914"
---

# "Lazy" Keyword

Lazy Variable : 처음 참조되기 전까지 연산을 진행하지 않는 변수

```swift
lazy var x: Int = add(3, 4)
```

라면, 

`print(x)` 과 같이 x를 참조하지 않는 한 x에 해당하는 저 함수는 실행되지 않음. 아마 리소스 관리가 편해져서 사용하지 않을까? 싶음

