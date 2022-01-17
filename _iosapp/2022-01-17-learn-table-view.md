---
permalink: /autolayout/iosapp-01/
classes: wide
title: "[앱 개발] 테이블 뷰 이해하기"
date: 2022-01-17
categories:
  - Table View
tags:
  - swift
  - iOS
  - table view
toc: true
toc_label: "목차"
toc_icon: bars
toc_sticky: true
---

### 테이블 뷰란?

---

항목을 표로 보여주는 뷰를 테이블 뷰라고 한다.

비슷하게 콜렉션 뷰도 있지만 테이블 뷰를 더 많이 사용한다고 한다.

#### UITableView vs. UITableViewController

![UIKit class hierarchy]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/uikit_classes.jpg){: .align-center}

> 상단 이미지는 [developer.apple.com](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/CocoaFundamentals/WhatIsCocoa/WhatIsCocoa.html#//apple_ref/doc/uid/TP40002974-CH3-SW10) 사이트에 나와있다.

위의 UIKit 계층뷰를 보면 TableView가 붙은 단어가 여러개 보인다.

간단하게 뒤에 View가 오는건 보여주는 기능을 하고 Controller가 오는건 처리까지 해준다고 생각하면 된다.

### Xcode 실습

---

![in strybord]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/tableThree.png){: .align-center}

스토리보드에서 오브젝트를 추가할 때 테이블뷰를 검색하면 위의 3개가 나온다.

Table View Controller를 사용하면 편하지만 이번 포스트에선 기능에 대해 자세히 알아보기 위해 Table View를 사용할 것이다.

테이블 뷰의 인스펙터를 보면 Content에 Dynamic Prototypes와 Static Cells옵션이 있는데 이게 무엇일까?

- Dynamic Prototypes : 정해진 길이 없이 계속 늘어난다.

- Static Cells : 정해진 길이 만큼만 보여준다.

![add table view]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/addTableView.png){: .align-center}

일반적으로 테이블 뷰는 화면을 꽉 채우므로 leading, top, trailing, bottom 제약을 모두 0으로 주었다.

![link table view]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/linkTable.png){: .align-center}

어시스턴트 에디터를 열어 소스 파일과 테이블 뷰를 연결시켜 주었다.

### 프로토콜 채택과 준수

---

```swift
class ViewController: UIViewController, UITableViewDelegate, UITableViewDataSource {
//        자식             부모              프로토콜               프로토콜
    @IBOutlet weak var table: UITableView!
    
```

<div class="notice--primary" markdown="1">
**소스가 너무 길어요**

아래와 같이 소스를 나눌 수 있다.

```swift
class ViewController: UIViewController{ }
extension ViewController: UITableViewDelegate{ }
extension ViewController: UITableViewDataSource{ }
```
</div>

> UITableViewDelegate

[developer.apple.com](https://developer.apple.com/documentation/uikit/uitableviewdelegate/) 사이트를 참고해봤을 때 UITableViewDelegate은 필수 메소드가 없기 때문에 채택만 해주어도 된다.

> UITableViewDataSource

![error]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/protocolErr.png){: .align-center}

이 프로토콜에는 필수 메소드가 있기 때문에 채택만 해줄 경우 위와 같은 에러가 발생하게 된다.

Fix를 눌러주면 Xcode가 알아서 필수 메소드를 추가해준다.

```swift
func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
    // code
}

func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
    // code
}
```

`tableView(_:cellForRowAt:)`과 `tableView(_:numberOfRowsInSection)`이 추가된 것을 확인할 수 있다.

#### 섹션과 행 / 셀

프로토콜을 준수할 때 추가된 함수에서 `numberOfRowsInSection`을 볼 수 있다.

여기에서 말하는 섹션과 row(행)는 무엇일까?

![row and section]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/rowncell.png){: .align-center}

섹션은 묶음이라 볼 수 있고 행은 한 줄 한 줄을 말한다.

행과 셀은 같은 의미이지만 일반적으로 row란 단어가 많이 쓰인다.

섹션의 경우 보통 하나만 사용하는 것이 일반적이므로 UITableViewDataSource 프로토콜의 numberOfSections 메소드에서 기본적으로 하나의 섹션으로 테이블을 생성한다.

해당 프로토콜의 필수 메소드에 numberOfSections가 없는 이유이기도 하다.

#### 필수 메소드 완성

```swift
func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
    return 5 // 섹션 안의 행의 수를 5줄로 한다.
}
    
func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
    return UITableViewCell() // 객체 생성
    // 이 메소드의 리턴형이 UITableViewCell? 형이므로 UITableViewCell 객체를 써주었다.
    // 에러가 나지 않게 하기 위해 임시로 써준 것이다.
}
```

#### 실행 화면

![screen]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/screen.png){: .align-center}

여러 줄의 회색 선을 볼 수 있다.

### UITableViewCell 알아보기

---

#### 생성자 활용

```swift
func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
    let cell = UITableViewCell.init(style: .default, reuseIdentifier: "myCell")
    // .init은 생략해도 무관하다.
    cell.textLabel?.text = "\(indexPath.row)"
    return cell
}
```

우선 위와 같이 적어주었다.

indexPath의 row를 출력하고 싶었지만 실행화면은 아무것도 나오지 않을것이다.

<div class="notice--primary" markdown="1">
**아래 소스를 추가해주자**

```swift
override func viewDidLoad() {
    super.viewDidLoad()

    table.delegate = self
    table.dataSource = self
    // table의 delegate과 dataSource를 내 클래스에서 처리할 것이라는 의미
}
```
</div>

![screen]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/screen2.png){: .align-center}

추가해주었다면 위와 같은 실행 화면이 나올 것이다.

앞에서 numberOfRowsInSection의 값을 5로 주었기 때문에 4까지 나온걸 확인할 수 있다.

> style?

![cell style]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/cellstyle.png){: .align-center}

셀의 디자인을 지정한다.

총 네 가지의 디자인이 있으며 위의 이미지를 보면 각각의 특징을 알 수 있다.

> cell.textLabel?.text

textLabel은 옵셔널형으로 default 스타일에서 제공하는 프로퍼티이다.

#### section 수 지정해보기

---

```swift
func numberOfSections(in tableView: UITableView) -> Int {
    return 2
}
```

![screen]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/screen3.png){: .align-center}

실행 화면을 보면 지정해준 행의 개수만큼 반복이 되는 걸 볼 수 있다.

#### indexPath 알아보기

```swift
func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
    let cell = UITableViewCell.init(style: .subtitle, reuseIdentifier: "myCell")
    cell.textLabel?.text = "\(indexPath.row)"
    cell.detailTextLabel?.text = indexPath.description
    return cell
}
```

섹션의 수를 2로 지정해주고 위와 같이 입력한다면 결과는 어떻게 나오게 될까

![screen]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/screen4.png){: .align-center}

실행 화면을 보면 [`섹션의 번호`, `셀의 번호`]의 형태를 갖고있다.

즉, indexPath는 각 섹션과 셀의 정보를 갖고있다.

#### 셀에 이미지 넣기

```swift
cell.imageView?.image = UIImage(named: "sun.png")
```

imageView가 옵셔널 형이기 때문에 `...png")`뒤에 `!`기호를 써주는 것이 좋다.
{: .notice--primary}

위의 소스를 추가하면 셀 안에 이미지를 넣을 수 있다.

![screen]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/screen5.png){: .align-center}

### 셀 커스텀하기

---

![add cell]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/suctomcell1.png){: .align-center}

스토리 보드에서 테이블 뷰에 table view cell을 추가해주면 prototype cells가 나온다.

이 prototype cells를 자신이 원하는 대로 커스텀해주면 된다.

#### cell 관리할 클래스 만들기

Cocoas Touch Class를 이용해 UITableViewCell을 부모 클래스로 하는 자식 클래스를 하나 만든다.

![create file]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/customcell1.png){: .align-center}

클래스를 만들었다면 커스텀 해줄 셀과 연결해준다.

![link class]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/customcell2.png){: .align-center}

#### 커스텀한 cell 적용하기

![add label]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/customcell3.png){: .align-center}

간단하게 꾸며보았다.

이 상태로 시뮬레이터를 실행해 보면 커스텀한 셀이 적용되지 않을 것이다.

적용되게 하려면 먼저 레이블과 클래스를 연결시켜야 한다.

![link label]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/customcell4.png){: .align-center}

어시스턴트 에디터를 사용해 연결해준다.

그리고 ViewController.swift파일을 아래와 같이 수정해준다.

```swift
func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
        let cell = tableView.dequeueReusableCell(withIdentifier: "taeCell", for: indexPath) as! taeTableViewCell
        // Table View Cell의 인스펙터 창에서 설정해준 Identifier를 써주어야 한다.
        // 부모에서 자식의 Label에 접근이 불가하다.
        // 다운캐스팅을 통해 taeTableViewCell형으로 바꿔준다.
        cell.taeLabel.text = indexPath.description
        // 다운캐스팅을 해주었기에 taeLabel에 접근이 가능해졌다.
        return cell
    }
```

![screen]({{ site.url }}{{ site.baseurl }}/assets/images/iosapp/customcell5.png){: .align-center}

### cell이 선택되었을 때 반응하기

```swift
func tableView(_ tableView: UITableView, didSelectRowAt indexPath: IndexPath) {
    print(indexPath)
}
```

위의 소스를 추가해주면 셀이 선택되었을 때 콘솔창에 해당 셀의 indexPath가 나오게 된다.


**Notice:** 이 게시물은 [Smile Han](https://www.youtube.com/watch?v=F5WhaFcK9sg&list=PLJqaIeuL7nuF9UoSxZLxIl3GC5WmeMSSU&index=52 "Smile Han님 유튜브")님의 유튜브를 참고하였습니다.
{: .notice--info}