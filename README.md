# SwiftUI Spring Animations Cheat Sheet for Developers

## Try the new Spring Animation in SwiftUI: <a href="https://gist.github.com/amosgyamfi/9d9d41bc662cf5b66d325bb231dd88b8#file-newspring-swift"> Snippet</a>
![Try the new Spring Animation in SwiftUI ](https://github.com/amosgyamfi/open-swiftui-animations/blob/master/AllGIF/extraBounce.gif)

## Animate chat bubbles an extra bounce spring
![Animate chat bubbles an extra bounce spring ](https://github.com/amosgyamfi/open-swiftui-animations/blob/master/AllGIF/amLiveFinal3.gif)
---

## Springy Duo: <a href=""> Available soon</a>
![Springy Duo ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/springyDuo.gif)

## Download and try the companion Mac App: <a href="https://apps.apple.com/us/app/motionscape-animation-studio/id1616840951"> MotionScape - Animation Studio</a>
## Check the companion open-source project: <a href="https://github.com/GetStream/motionscape-app"> MotionScape - Animation Studio</a>

## Realistic Chain: <a href="https://gist.github.com/amosgyamfi/fa899f1026ed71db52c83da5afb69ecf"> Swift file</a>
![Realistic Chain ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/chains.gif)

Unlock the secrets of iOS spring animations using SwiftUI. Learn all the SwiftUI spring animation types, understand their parameters, and discover how to create organic and fine-grained spring animations to enhance the user experience of your next iOS app.


<p><strong>Watch the video: (<a href="https://youtu.be/-ymASV6jH4U" target="_blank">YouTube tutorial</a>) </strong></p>

![HSwiftUI spring animation parameters ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/springParameters.svg)


## A Chained Spring: <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/Introduction/ChainedSpring.swift"> Swift file</a>
![Chained Spring ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/springAnimation.gif)

## A Bouncy Transition: <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/BouncyHamburger.swift"> Swift file</a>
![Bouncy Transition ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/bouncyHamburgers.gif)

## Transition a hamburger menu to a back icon <a href="https://gist.github.com/amosgyamfi/71546754e7b04a152bbe57ec0708b338#file-hamburgertobackicontransition-swift"> Swift file</a>
![ Transition a hamburger menu to a back icon ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/hamburgerToBack.gif)


<hr/>

## SwiftUI Spring Animation Types


## 1 .spring()
A spring with no parameters. It applies gentle and sensible spring-feel to the object you want to animate.

### Menu - Close icon transition: <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/Spring.swift"> Swift file</a>
![Menu - Close icon ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/menuToClose.gif)


## 2 .interactiveSpring()
An interactive spring with no parameters. This creates a spring animation with high stiffness and low response. It makes the animation is less snappy:

### Menu - Close icon transition: <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/InteractiveSpring.swift"> Swift file</a>
![Menu - Close icon ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/menuTocloseInteractive.gif)

## 3 .interpolatingSpring(stiffness, damping)
This allows you to create a spring animation that is based on stiffness and damping. 
  * **Stiffness:** 
    It is defined as the tensile strength of the spring. A higher stiffness will result in snappier animations. This affects the force applied to the object   
    and changes how quickly the object moves towards its target.
  * **Damping:** You can think of damping as the braking of a car or the back-drag frictional force on the surface the object is resting on. Its purpose is to     stop the object over time. It also affects the ability to overshoot the object. **Hint**: Start with a damping of 15 and stiffness of 170. Reducing the   
    damping for example, to a value of 5 will create a spring animation that has higher bounciness.

### Chat message reactions: <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/ReactionsViewInterpolatingSpringSD.swift"> Swift file</a>
![Chat message reactions ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/reactions.gif)


## 4 .interpolatingSpring(mass, stiffness, damping, initialVelocity)
This allows you to create a spring animation that is based on mass, stiffness, damping, and initial velocity. Default values: .interpolatingSpring (mass: Double = 1.0, stiffness: Double, damping: Double, initialVelocity: Double = 0.0).
  * **Mass:** Think of mass as the weight of the object animating. It changes the inertial of the object attached to the spring. That is the willingness of an               object to move or stop moving. It is conceptually heavier and can be used to create a spring animation that overshoots. The heavier the mass, the               longer it takes to move the object, speed it up, and slow it down.  
  * **Initial Velocity:** The initial velocity is defined as the speed at which the animation object changes at the beginning of the animation. The default initial velocity is set to zero. It is measured in units per second of the animation. 
### Chat message reactions (Heart icon): <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/ReactionsSpringsWithParameters.swift"> Swift file</a>
![Chat message reactions ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/messengerReacrions.gif)

## 5 .spring(response, dampingFraction, blendDuration)
This allows you to create a spring animation that is based on response, damping fraction, and blend duration. Default values: .spring (response: Double = 0.55, dampingFraction: Double = 0.825, blendDuration: Double = 0). A higher response value will slow down the animation. A lower response speeds it up. 
  * **Response:** It controls how quickly an animating property value will try and get to a target. You can use the response to create an infinitely-stiff spring by setting its value to zero. 
  * **Damping Fraction:** 
     Damping fraction causes a gradual reduction in the spring's oscillation. Using damping fraction, you can define how rapidly the                        
     oscillations decay from one bounce to the next. Additionally, you can damp the spring in the following ways:
     
      ![Chat message reactions ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/dampedSprings.gif)
      - **Over Damping:** Set the damping fraction to a value greater than 1. It lets the object you are animating, quickly return to the rest position.
      - **Critical Damping:** Set the damping fraction = 1. It lets the object return to the rest position within the shortest possible time.
      -  **Under Damping:** Set the damping fraction to be less than 1. It lets the object overshoot multiple times passing the rest position and gradually               reaching the rest position.
      - **Undamped:** Set the damping fraction = 0. This lets the object oscillate forever.
  * **Blend Duration:** Blend duration is a frame of time during which a previous animation stops and the next animation starts. Changing the blend duration of       any of the examples in this repository, does not produce any visual change. This makes it difficult to see what it actually does. 

 ### Chat message reactions (Thumbs up icon): <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/ReactionsSpringsWithParameters.swift"> Swift file</a>
![Chat message reactions ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/messengerReacrions.gif)


## 6 .interactiveSpring(response, dampingFraction, blendDuration)
This allows you to create a spring animation that is based on response, damping fraction, and blend duration. Default values: interactiveSpring (response: Double = 0.15, dampingFraction: Double = 0.86, blendDuration: Double = 0.25). You can use this spring as an alternative to .spring(response, dampingFraction, blendDuration). Always start with the default values above. To check the default values in XCode, Control-click the spring modifier and select "Show Quick Help". The thumbs down animation below uses this spring. The damping fraction is inversely proportional to the springiness of the animation. Reducing the default damping fraction will make the animation bouncier. As mentioned in step 5 above, blend duration has no visible effect on the spring, at the time of writing this article.  
 
### Chat message reactions (Thumbs down icon): <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/ReactionsSpringsWithParameters.swift"> Swift file</a>
![Chat message reactions ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/messengerReacrions.gif)

<hr/>

## SwiftUI Spring Animation Properties and Effects

### Damping Fraction: High, medium, low, and no bounce

<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/Spring%20Properties/DampingFractionBounce.swift"> Swift file</a>
![Damping Fraction ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/dampingFractionBounce.gif)

### Stiffness Bounce: High, low, medium, and very low stiffness

<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/Spring%20Properties/StiffnessBounce.swift"> Swift file</a>
![Stiffness Bounc](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/stiffnessBounce.gif)


### Varying Stiffness and Damping: Stiff, gentle, wobble, and no wobble

<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/StifnessDamping.swift"> Swift file</a>
![Damping Fraction](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/stiffnessDamping.gif)

<hr/>

## SwiftUI Spring Animation Examples

## Proceed with TouchID: <a href="soon"> Swift file</a>
![Proceed with TouchID ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/touchIDAnimation.gif)

## Text Spring 1: <a href="https://gist.github.com/amosgyamfi/36858c4d8466f6d384b091bb90538fa8#file-textspring-swift"> Swift file</a>
![Text Spring 1 ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/texSpring.gif)

## Heart Icon Animation: Twitter Like Reaction Clone<a href="#"> Swift file (coming soon)</a>
![Heart Icon Animation: Twitter Like Reaction Clone ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/SwiftUITwitterLike.gif)

## Animated Font Weight: 
<p align="center">
 <img src="https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/animateFontWeight.gif"/>
</p>

```swift
import SwiftUI

struct AnimateFont: View {
    @State private var isMagicallyMoving = false
    
    var body: some View {
        Text("Animate SwiftUI Text Like Your Boss' Boss!")
            .font(isMagicallyMoving ? .title : .largeTitle)
            //.fontWeight(isMagicallyMoving ? .black : .ultraLight)
            .multilineTextAlignment(.center)
            .foregroundColor(isMagicallyMoving ? .indigo : .cyan)
            .animation(.interpolatingSpring(stiffness: 170, damping: 15).repeatForever(autoreverses: true), value: isMagicallyMoving)
            .onAppear {
                isMagicallyMoving.toggle()
            }
    }
}
```

## Text Spring 2: <a href="https://gist.github.com/amosgyamfi/e8c215de81bc5a48e19a425f18487bcd#file-streamtextspring-swift"> Swift file</a>
![Text Spring 2 ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/streamSpringDemo.gif)

## Chat Emojis: <a href="https://gist.github.com/amosgyamfi/1852a73764ccc6790bed18f10057579a"> Swift file</a>
![Chat Emojis ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/chatEmojis.gif)

## Draggable Menu ( <a href="https://www.hackingwithswift.com/books/ios-swiftui/customizing-animations-in-swiftui"> Inapired by Hackingwithswift</a>):  <a href="https://gist.github.com/amosgyamfi/37bf602c0fd145e3f5a8e6384dd5f796"> Swift file</a>
![Draggable Menu ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/draggableMenu.gif)

### Silent Mode: On 
Animate a bell to fall and rotate after falling. It is similar to the iOS silent mode (on) animation. Since this animation emulates the presence of sound, it uses a very low damping to create a high bounce. <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/SilentModeOn.swift"> Swift file</a>
![Silent Mode: On](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/silentModeOn.gif)

### Silent Mode: Off  
Animate a slashed bell to fall and rotate after falling. It uses a rectangular mask to show and hide the bell icon. Since this animation simulates the absence of sound, it uses moderate damping to prevent the bell from bouncing. <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/SilentModeOff.swift"> Swift file</a>
![Silent Mode: Off](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/silentModeOff.gif)

### Position Spring Animation
Animate a ball's position so that it appears to be pulled towards a target by a spring. <a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/Fundamentals/PositionSpringAnimation.swift"> Swift file</a>
![Position Spring Animation](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/positionSpringAnimation.gif)


### Scale Spring Animation
Create a spring animation that bounces a ball into view by animating its scale from 1 to 2. 
<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/Fundamentals/ScaleSpringAnimation.swift"> Swift file</a>
![Scale Spring Animation ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/scaleSpringanimation.gif)

### Recording Spring Animation: 
Create a recording effect using different springs. 
<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/Recording.swift"> Swift file</a>
![Create a recording effect using different springs. ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/recordingSpringAnimation.gif)

### Animate a photo preview to its fill view 
<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/MessengerPhotoView/ConversationsPhotoZoom.swift"> Swift file</a>
![ Animate a photo preview to full view ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/messagePhotoZoom.gif)

### Zoom a photo from its gallery 
<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/MessengerPhotoView/ConversationsPhotoZoom.swift"> Swift file</a>
![ Zoom a photo from gallery ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/galleryPhotoZoom.gif)

### Animate a photo from its fit view to a fullscreen view
<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/PhotoZoom.swift"> Swift file</a>
![ Animate a photo from its fit view to a fullscreen view ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/photoZoom.gif)

### Animate a ball to fall and bounce
<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/FallingBall.swift"> Swift file</a>
![Animate a ball to fall and bounce ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/fallingBallWithBounce.gif)

### Animate a bell to rotate with springiness
<a href="https://github.com/GetStream/swiftui-spring-animations/blob/main/SwiftUISpringAnimations/SpringExamples/NotificationAnimation.swift"> Swift file</a>
![Animate a bell to rotate with springiness ](https://github.com/GetStream/swiftui-spring-animations/blob/main/Misc/bellNotification.gif)


<hr/>

** Related Links **
- [https://developer.apple.com/documentation/quartzcore/caspringanimation#2826917](https://developer.apple.com/documentation/quartzcore/caspringanimation#2826917)
- [https://developpaper.com/ios-spring-animations/](https://developpaper.com/ios-spring-animations/)
- [https://popmotion.io/#quick-start-animation-animate-spring-options](https://popmotion.io/#quick-start-animation-animate-spring-options)
- [https://www.raywenderlich.com/books/ios-animations-by-tutorials/v6.0/chapters/4-springs](https://www.raywenderlich.com/books/ios-animations-by-tutorials/v6.0/chapters/4-springs)
