---
description: 편리하게 View(ViewController)를 바꿀 수 있는 UITabBarController를 알아보자
---

# UITabBarController

### Tab Bar Controller가 무엇인가?

* **Container ViewController** \(VC를 담는 VC. 여러 자료형을 담는 리스트같은 느낌\)
* 사용자는 이 Tab 중 하나를 눌러서 ViewController를 교체할 수 있음
* 다르지만 **유사\(comparable\)**한 VC를 묶는 것이 좋다!  
* 많은 앱에서 UI의 중심으로, 유저에게 접근 가능한 목록들을 나열해서 보여줌



### Tab Bar Configuration

```swift
// example tab bar of "Instagram"

let homeVC = HoneViewController()
let searchVC = SearchViewController()
let postVC = PostViewController()
let activityVC = ActivityViewController()
let userVC = UserViewController()

let tabBarController = UITabBarController() // UITabBarController의 Instance 생성!
tabBarController.viewControllers = [homeVC, searchVC, postVC, activityVC, userVC]
```

* 5개의 다른 VC를 생성, `UITabBarController()`의 인스턴스를 생성
* 배열의 형태로 VC들이 TabBar에 전달



### Tab Bar Item Configuration

```swift
// UITabBarItem의 instance!
let item = UITabBarItem()
item.title = "Home"
item.image = UIImage(named: "home_icon")

let homeVC = HomeViewController()
homeVC.tabBarItem = item
let tabBarController = UITabBarController() // UITabBarController의 Instance 생성!
tabBarController.viewControllers = [homeVC, searchVC, postVC, activityVC, userVC]
```

* UITabBarItem\(\)의 인스턴스를 생성 → ViewController\(\)에 할당



### 실제 코드단에서 더 쉽게 작성하기\(added on 5/6\)

```swift
class TabBarController: UITabBarController {
    
    // 1. Initialize UINavigationController(with root VC)
    private var homeVC = UINavigationController(rootViewController: ...)
    ...
    
    // on ViewDidLoad
    // 2. Set viewControllers on UITabBarController
    self.viewControllers = [homeVC, ...]
    // 3. Set tabBarItem with initializer - title, image, tag
    homeVC.tabBarItem = .init(title: "홈", image: nil, tag: 0)
    ...
    // 4. Hide NavBar(since we use TabBarController)
    homeVC.navigationBar.isHidden = true
}
```

