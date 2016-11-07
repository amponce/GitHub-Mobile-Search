# GitHub-Mobile-Search
IOS and Android Mobile Repo Search Tool, Tutorial found on Scotch.io credit (GeekyAnts) — Edit

React Github Mobile Search 
https://scotch.io/tutorials/nativebase-the-missing-piece-of-react-native%E2%80%8B

Getting Started

First make sure you have your React Native Dependencies

Node.js
Watchman (Installed with homebrew)

npm install -g react-native-cli 

Run a test project:

react-native init AwesomeProject
cd AwesomeProject 
react-native run-ios

You should see your new app running in the iOS Simulator shortly.

(react-native run-ios) is just one way to run your app. 
You can also run it directly from within Xcode or Nuclide.


Notes on the Scotch.io tutorial

The first issue I ran into was the port, I apparently had another active port on causing issues.  

To Resolve:
* update (npm)
* update (React native)  react-native upgrade

kill the active port with the following (cmd)

$ sudo lsof -n -i4TCP:8081 | grep LISTEN

kill -9 <PID>  

I had to run this as sudo, that might not be the case for everyone.. the port is the option right before (root)

The next issue I hit was with watchman. I had originally installed it outside of homebrew. 
This error was resolved easily with installing (brew watchman)

Icons
http://facebook.github.io/react-native/docs/linking-libraries-ios.html#content

Install a library with native dependencies:
In my case I was missing the icons: react-native-vector-icons

$ npm install <library-with-native-dependencies> --save

Link your native dependencies:

$ react-native link
