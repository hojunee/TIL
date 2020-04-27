# struct vs class

## **struct는 Value를 만들고 class는 Object를 만든다**

**struct**

* Call by Value Assignment, Parameter 전달 시 Value Copy가 이뤄짐
* Stack Memory 사용 - 속도가 빠르다
  * Scope Based Lifetime : Compile단에서 Complier가 언제 메모리를 할당/해제 해야할지 정확히 인지
  * Data Locality : 순차적으로 쌓으므로 CPU 캐시 히트율이 높음
* 상속 불가능 \(단, protocol은 사용 가능\)
* `NSData`로 Serialize 불가능
* `Codable` Protocol을 이용해서 손쉬운 JSON↔struct 변환 가능
* 항상 새로운 변수로 copy가 일어나기때문에 multi-thread 환경에서 공유변수로 인해 문제를 일으킬 확률이 적음

**class**

* Call by Reference Assignment, Parameter 전달 시 객체를 가리키는 메모리 주소값만 복사됨 \(C언어의 Pointer를 생각하자\)
* Heap Memory에 할당 - 속도가 느리다
  * 런타임에 직접 malloc하며 Reference counting을 통해 dealloc이 필요
  * Memory Fragmentation 등의 Overhead\(Process를 위해 들어가는 간접적인 처리 시간\) 존재
* 상속 가능
* `NSData` Serialize 가능
* `Codable` 사용 불가능
* 런타임에 타입 캐스팅을 통해서 클래스/인스턴스에 따라 여러 동작이 가능
* deinitializer 존재

