---
description: 'Java때 했던 Interface와 유사한 목적을 지님. 일단 만들어, 그리고 구현해!'
---

# Delegate\(대리자\)

### An Object that executes a group of methods on behalf of another object 

다른 객체 대신에 메서드의 그룹을 실행하는 **객체**

### Why? 

To Reuse View!

* 같은 ListView에서도 어떻게 다른 설정을 부여할 수 있을까?
* View는 자신의 Delegate에 몇가지 질문을 던짐
  * 새 글자가 들어오면 어떡하지?
  * return 버튼이 눌리면 어떻게 반응하지?
  * Edit이 활성화되면 어쩌지?
  * ...

