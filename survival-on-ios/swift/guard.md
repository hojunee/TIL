---
description: Look Before You Leap
---

# guard

Swift에서는 무엇을 진행할 때 그 타입을 체크하여 조건을 만족하지 못했을 때 이를 조기에 return할 수 있는 기능이 있다. 이를 **조기반환\(early return\)이라고 하는데,** 이를 통해서 

* 디버깅을 더 쉽게 진행할 수도 있고, 
* 부정적인 if문을 넣지 않음으로써 가독성을 유지할 수 있다!

사용법은 다음과 같다.

```swift
//Notation
guard (statement) else {
    // type something, will be executed when statement is false
}

//Example
func sqrt(number: Int) -> Int?
{
    guard number >= 0 else {
        return nil
    }
    
    // sqrt를 연산한 후에 number의 제곱근을 반환
    return ...
}
```

