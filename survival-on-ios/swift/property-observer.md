---
description: 변수 하나 만들 때도 한땀한땀 정성들여 만들자
---

# Property Observer

Property의 값이 변경될 때 원하는 동작을 수행할 수 있도록 해주는 것

`willSet()` - Property가 바뀌기 직전에 호출 \(바뀔 값을 표현하는 암시적 매개변수 **newValue**\)

`didSet()` - Property가 바뀐 직후에 호출 \(바뀌기 전 값을 표현하는 암시적 매개변수 **oldValue**\)

* **연산 프로퍼티에서는 프로퍼티 감시자를 사용할 수 없다! \(왜? 저장된 값이 변할 때 호출되는 메서드이기 때문에!\)**
* 지역/전역 변수에도 Observer를 사용할 수 있다.

