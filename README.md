<h1 align="center"> iPaymentButton 💵 </p>
<h3 align="center"> Quickly implement & easily customize the Apple Pay button. 🤑</h3>
<p align="center">
    <strong><a href="#get-started">Get Started</a></strong> |
    <strong><a href="#examples">Examples</a></strong> |
    <strong><a href="#customize">Customize</a></strong> |
    <strong><a href="#install">Install</a></strong> | 
</p>
<p align="center">
    <img src="https://github.com/AlexFine/SwiftUICode/blob/master/public/assets/img/iPaymentButton-Demo-1.gif" alt="CI" width="70%"/>
</p>

<br/>

## Get Started

1. [Install](https://github.com/benjaminsage/iPaymentButton/blob/main/INSTALL.md) `iPages`

2. Add `iPaymentButton` to your project
```swift
import SwiftUI
import iPaymentButton

struct ContentView: View {
    var body: some View {
        iPaymentButton(action: {
            // Add your custom payment code here 
        })
    }
}
```

3. Customize your `iPages`


## Examples
### Starter
<img src="https://iswiftui.com/assets/img/iPaymentsButtonDemo1Dark.gif" width="200">

Use our built-in `applePayDemo()` to demo a purchase experience.

```swift
import SwiftUI
import iPaymentButton
import iGraphics

struct ContentView: View {
    var body: some View {
        iGraphicsBox().stack(3)

        iPaymentButton(action: {
            iPaymentButton.applePayDemo()
            // Add your custom payment code here 
        })
    }
}
```


### Modern
<img src="https://iswiftui.com/assets/img/iPaymentsButtonDemo2Light.gif" width="200">
Change the button type and style.

```swift
import SwiftUI
import iPaymentButton
import iGraphics

struct ContentView: View {
    var body: some View {
        iGraphicsView(.first)

        iPaymentButton(type: .support, style: .whiteOutline, action: {
            iPaymentButton.applePayDemo()
            // Add your custom payment code here 
        })
    }
}
```


## Customize
`iPaymentButton` has one required parameter: an action to execute on button tap. `iPaymentButton` supports several custom initializers and one custom modifier.

**Example**: Change the text, style and corner radius with the following code block:
```swift
iPaymentButton(type: .support, style: .whiteOutline, action: { } )
    .cornerRadius(25)
```

Use our exhaustive input list to customize your views.

Modifier or Initializer | Description
--- | ---
`type: PKPaymentButtonType = .buy` | The text written on the button. 🆒
`type: PKPaymentButtonStyle = .black` | The color that the button should be. 🎨
`action: @escaping () -> Void` | The action to be performed when the user taps the button. 🎬▶️
`.cornerRadius(radius: CGFloat) -> iPaymentButton` | Modifies the corner radius of the payment button ⬛️⚫️. To remove the rounded courners, set this value to 0.0 0️⃣👌. The default value is set to 4.0 🍀.


## Install 
Use the Swift package manager to install. Find instructions [here](https://github.com/benjaminsage/iPaymentButton/blob/main/INSTALL.md)😀

