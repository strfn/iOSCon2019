# iOSCon 2019 Day 2

---
## Keynote: The Business Case For Your Code 
Why are we coding what we code ?
from where current task you are working on ?
Is part of the company strategy to deliver value

> Building and understanding
- start high level to see the value of what the company needs to deliver and then drill down to understand where are your responsibility to deliver that goal.


---
## Cellular View Controllers 

> Dave DeLong watch WWDC and a better MVC video/articles

leverage stack view if the number of items is limited
Each cell can embed a view controller
needs to figure out how to reuse VC.
actually embedding VC becomes bloated and overcomplicated.

> Check texture https://github.com/TextureGroup/Texture

> Check snapshot testing https://github.com/pointfreeco/swift-snapshot-testing

---
## Better Together 

Final goal is to have successful app ! regardless of the platform, consider the market share

collaboration across team if the platform are managed by two teams. Keeping the platform in sync facilitate communication for the business as both platform release in sync with the context.

Cross functional team increase communication and team productivity, at monzo teams are cross functional QA/iOS/Android/Designers. SQUAD 

Semantic Emojis in communication on online chats prefixing each message with an emoji so you know what is about.

Also PR have emoji to identify size and category

Monthly mobile team meetings to share what it has been done

Pair programming also cross platform to brings new idea

With Kotlin the differences between iOS and Android is minimum from a language perspective.

you can use Kotiln (with Kotlin native) on iOS also other way around is possible but not as advanced 

some time cross platform might be a good option, Flutter is advised even if is now is gaining a lot of traction in a short time. Toolset is well integrated.

Firebase is growing 

CI: 
- Circle CI 

---
## The Evolution of Swift: Are we there yet?

Hacking with swift: live                                
---
## Live Podcast: Swift over Coffee


---
## Beyond TDD 

If the developer write also the test i will reflect the limited understanding of the problem, needs to talk to extend the knowledge
QA are BAs they can understand the problem and how the system is supposed to work !

Behavior driven development: talks with somebody else on what the software is supposed to do and transform in  tests.

TDD is good for designing good architecture but might fail short on testing the overall logic.

Defined invariants and the contact, let the computer take care of creating all the input combination and see if the implementation is valid.


CocoaByContract

---
## Lightning Talk: ABI Stability & the LLVM 

Why from GCC to LLVM:
- Modularity
- Optimization
- Easier support for new HW
LLVC has a intermediary language so the most of compiler can be re-used across different hw platforms.

ABI stability:
- Without ABI stability each IPA is tight to a particular swift version.
- The swift runtime needs to be packaged with every IPA
- Once API is stable the runtime stays the same.
- With stable APi the runtime  the runtime can be moved to the device OS.

---
## Lightning Talk: Use Sourcery to Make Your iOS Code Write Itself 

example with dependency injection
template language is stencil
define your own annotation and use it to filter all your types.

---
## Lightning Talk: Meeting Business Users Expectations 

---
## Jaimee Newberry - Keynote
