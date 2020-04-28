---
description: 자세한건 Delegate에 물어봐!
---

# Delegate Pattern

* 추상화 아이디어를 가진 Abstract나 Interface와 유사
* 하나의 객체가 모든 일을 처리하는 것이 아니라, 처리해야 할 일 중 일부를 다른 객체에 넘기는 것

Example\)

```swift
func textField(_ textField: UITextField, shouldChangeCharactersIn range: NSRange, replacementString string: String) -> Bool {

        // Figure out what the new text will be, if we return true
        var newText = textField.text! as NSString
        newText = newText.replacingCharacters(in: range, with: string) as NSString
        
        // hide the label if the newText will be an empty string
        self.characterCountLabel.isHidden = (newText.length == 0)
        
        // Write the length of newText into the label
        self.characterCountLabel.text = String(newText.length)
        
        // returning true gives the text field permission to change its text
        return true;
    }
```

1. User가 Keyboard를 누른다
2. Textfield는 Text가 바뀔 것임을 인지한다
3. Textfield는 `:shouldChangeCharactersInRange:` 를 Invoke\(발동\)
4. VC가 이 Invoke를 받아들임
5. VC가 새로운 Text를 조합
6. VC가 Label을 Update
7. VC가 true를 반환함으로서 변화가 일어님

**1~7의 과정을 통해 우리가 일상생활에서 썼던 Flow가 일어남!**

