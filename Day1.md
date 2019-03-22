# iOSCon 2019 
## Keynote

DecisionKit:
 - Context drive the decision and context change over time.
    - what are we trying to build
    - what will be the tech challenges (what is that we have not done before, where is the innovation ?)
    - what skills we have in the team 
    - current codebase ? you want consistency
    - deadlines ?Be pragmatic don't overdo 
    > for example network: is a complex subject but it depends on your requirements. If you need full network capabilities you better off with a framework, if you just need to pull some data make sense to use urlsession
    - Implementing yourself has value also for learning and fun. DO enough research to understand complexity.
    - commercial option might save you time
- Impact analysis
    - cost vs benefits
    - maintenance
        -   look at encapsulation, reduce the impact on the other components.
        - how many files will need to change to adopt the decision?
    - how much lock in, don't put yourself in a corner.
        - is your app becoming an X app? like react native? Flux ? same for design patterns and architectures rxSwift, RFP.
- **BUILD PROTOTYPES !**
    - > Why
    - quickly invalidate incompatible solutions.
    - reduce rewrites and refactors
    - learn
    - Investment for the team and the product
    - > How
    - narrow scope
    - easily throw away like playground or new branch
    - define GOALS
    - code quality and structure doesn't matter at this stage
    - Focus on high level concepts.
- Abstractions
    - protocols
    - free form functions
- Make the decision
    - compare prototypes and project fit
    - document 

---
## Best Practices for Notifications Features
Best practice, be relevant and respectful, do not send duplicates. Be meaningful providing context also when the user set the notification preference to never show content.
Relevant actions: allow to act without opening the app. get something done without wasting user time, create trust.

### Notification settings screen
provide user granular control on what the user receives
when, what, how.
Server settings and local client cofiguration.
Deep link the app custom setting page from the iOS setting page. Callback in the app delegate.

- POP to increase testability, use Unit test to ensure best practice are met.
    - Apple singleton are difficult to control for testing.
    -  crate a protocol that encapsulate the methods from the standard library
    - add a method that wrap the protocol ?? **TO CHECK**
    - mock class enriched to facilitate unit test, adding the capability to add assets block.
- Quick wins
    - add descriptive text for hidden notification
    - add the custom app setting page
    - test local notification !
- Complexity, the user receive a notification when he click on it it expect the content to be available in the app but the app might have not fetch the data. Use content available flag in the APNS payload so you can start background fetch. be mindful is throttled !
- Payload versioning, Apple API has changed over version.
- When creating new abstraction  weekly design workshop where developers share what they are going to build next and how. A lot of documentation.

---
## Parsing Formal Languages with Swift
Check slices, both for array and string, can be used as a powerful optimization if you need to move  around a collection. It do not duplicate the data but just keep start and end index of the part of the collection we need.

---
## 30 Xcode Tips in 45 Minutes 

swift news, youtube channel

- #warning("refactor")  better than todos as it shows in the build result
- track build times, to be done in the terminal showbuildopetationduration
- Assistant editor layout cmd shift click
- recent files back and forth with shortcut go well together with cmd shift J to highlight the file in the navigator
- cmd-shift-l to open library
- To avoid further editor to a VC in storyboard there is a lock option in the inspector
- Previous screen on multiple devices, from storyboard click on the 4 squares and then select preview, you can select the screens sizes
- Stress test labels double length sudo languages
- color assets: go into assets click + color set, shows in storyborard
- highlight structure hold cmd and hover the curly brackets.
- rename in scope to cmd i and select a variable
- Multiline editing cmd shift
- multiple tabs --> shortcut for expose
- breakpoints sounds useful for when you have multiple concurrent actions so you can understand the order.
- build setting description --> option double click on the setting you want more details.

---
## Keynote: The Monad Lurking Under Your Bed At Night 

has to be watched
dimsumthinking.com
doctor franker funster and the omnaster

---
## Mr. Wolf's Horror Stories 

Undertand the language and embrace it.
Composition better than inheritance
Factories, use enum ith associated values
Use injection don;t create objects yourself
### Reason for refactorinig:
- Achitectural purpose
    - remove dependency 
    - easier to change
    - easier to mantain
    - faster/testable/
- How:
    - Iterative
    - short leved branches, do not create a refactoring branch
    - Create an abstraction that can levarage either the new or the old implementaiton and then gradually migrate the consumer via injection
### Automation
measure the length of the task and how often you do the task. 
- pre commit hook for testing.
- use swiftlint
Versioning
- feature flags is an enabler to do CI **merge often**

---
## Workshop: Secure Software Development: From Rookie to Hardcore in 90 Minutes 

cossack labs consultancy in security

GDPR requires also to monitor for leaks. Check aricle 32 of GDPR.
Repo: https://github.com/vixentael/ios-datasec-basics


SDLC
- Security controls
    - Proactive, good code
    - reactive: DETECT !
        - be able to revoke access token when attack is detected
        - mobile app could be part of SIEM
    - OWASP MASVS

### Storage encr and Key management

If well encrypted and key is protected the data can be stored anywhere 
encription can be weak if using wrong mode and paramters in algorithm.
check diffrence between GCM and CBC mode
To protect the password don't use hash use KDF, it repats the hashing thousands of time, it's more time consuming to crack

Use boring crypto library that hide crypto details and i well tested.

### Key management
two types: built-in (embeded in the app) or App flow, keys received from the server.

Encrypted data is not representable as string so needs to be encoded (fpr example base64) in order to trasfer over the wire.

obfuscation do not add secirity.

if you use KDF any string can be used as an encription key.

Store a secret like a password

Keychain is resiliant to user deleting the app, user default is not. use user default to identify first launch. At first launch make sure to delete the keychain data.






---
### Keynote: Burnout

