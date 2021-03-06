# Swift ViewController Examples

This repository is UIViewController and a sample using UINavigationController created in Swift. This is an example of screen transition in UINavigationController and segue, and an example of embedding UIViewController as a part in ContainerView.

# NavigationControllerBasic

This is simple example using UINavigationController.
It' use segue to showing another ViewController.

- Storyboard, UINavigationController and ViewController structure.  

![Basic usage of UINavigationController](assets/seque_sb.jpg "Basic usage of UINavigationController.")

- Demo  

![ViewController Segue transition](assets/segue.gif "Basic usage of UINavigationController.Segue transiton")

## How to implement the back button

1. Implement unwindSegue in the previous ViewController class.

1. CTRL + Drag from ViewContorlller part on Storyboard and tie it to exit.

```swift
import UIKit

class FirstViewController: UIViewController {
  override func viewDidLoad() {
    super.viewDidLoad()
  }

  @IBAction func unwindActionFirstVC(unwindSegue _: UIStoryboardSegue) {}
}
```

# NavigationInContainerView

This is an example of UINavigationController in Containter View.
Containter View can include ViewController as a child.
It can also contain a container-type ViewController such as UINavigationController or UITabBarController.
In this example, ViewController transition same as NavigationControllerBasic project is performed in Container View.

- Storyboard, UINavigationController is embedded in Container View.

![ UINavigationController in Containter View](assets/ContainerView.jpg " UINavigationController in Containter View")

- Demo

![ UINavigationController in Containter View](assets/ContainerView.gif " UINavigationController in Containter View")

# NavigationWithBanner
This is an example using two container views.
The first is a Container View that includes UINavigationController and can switch ViewController.
Another Container View contains a ViewController that displays a banner. This is always shown regardless of the first ViewController switch.

- Storyboard, UINavigationController is embedded in Container View and Banner is embedded other Container View.

![ NavigationWithBanner](assets/ContainterAndBanner.jpg )

- Demo

![ NavigationWithBanner](assets/Container_banner.gif )

- View Structure(view hierarchy)

![ NavigationWithBanner View Structure](assets/ContainerAndBanner_structure.jpg )

# References

* [UIViewController \- UIKit \| Apple Developer Documentation](https://developer.apple.com/documentation/uikit/uiviewcontroller)

* [View Controller Programming Guide for iOS: Implementing a Container View Controller](https://developer.apple.com/library/archive/featuredarticles/ViewControllerPGforiPhoneOS/ImplementingaContainerViewController.html)


