# MVVM Pattern

![&#xAE30;&#xC874;&#xC758; MVC &#xD328;&#xD134;](../../.gitbook/assets/image%20%281%29.png)

디자인 패턴에는 종류가 많다. 오늘은 그중에서도 이번 프로젝트에서 사용되는 MVVM 패턴에 대해 학습해보자.  


![MVVM&#xC758; &#xAE30;&#xBCF8; Structure](../../.gitbook/assets/image%20%285%29.png)

## Notation of Structure

### Model

App에서 사용되는 데이터와 그 데이터를 처리하는 부분

### View\(↔ViewController\)

사용자에게 보여지는 UI 부분

### ViewModel

View를 표현하기 위해 만든, View를 위한 Model View를 나타내주기 위한 Model이자 View를 나타내기 위한 데이터 처리를 하는 부분

## How it works?

1. 사용자의 Action은 View를 통해 들어옴
2. View에 Action이 들어오면, Command 패턴으로 VM에 Action을 전달
3. ViewModel은 Model에 데이터를 요청
4. Model은 VIewModel에게 요청받은 데이터를 응답
5. View Model은 응답 받은 데이터를 가공하여 저장
6. View는 View Model과 Data Binding하여 화면을 나타냄

\*Data Binding : 화면에 있는 객체와 데이터를 일치시키는 것 \(django에서 Template Language를 생각해보자\)

## Code에서 각 함수의 역할

* `attribute()` - 사용하는 View에 대한 설정을 하기 위해 사용하는 함수
* `layout()` - View에 대한 Layout을 구성할 때 사용하는 함수
* `bind()` - 값을 받아서 Binding하거나 Event를 전달하기 위해 사용하는 함수

