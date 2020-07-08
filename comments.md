git init
git add .
git commit -m 'first'
gst

flutter create flutter_exercise_six

android studio, remember it's important to create a virtual device WITH the play store feature !!! Don't waste 1 GB !!!
Pixel 2 with Android Pie API 28 created

flutter run (-------> or better --> in taskbar(up), Run, Run Without Debugging)

R          ==>> restart in emulator!

intl: ^0.16.1

flutter packages get

don't forget the power of option-shift-F, formatting ! Problem with VS Code update version ! USE MOUSEPAD OPTIONS WAY !!!!

open -a Simulator.app

extract widget              --->  splitting up widgets within the file !! super handy !!

flutter packages get  (----> in terminal) (if needed, normally flutter will get the packages automatically)

! Using the flutter built-in Futures work well as is, but for readability and because we are used to try/catch & async/await/finally from JS, here it is !

! A Future in Flutter is the equivalent of a Promise in JavaScript !

flutter clean
flutter pub cache repair
flutter pub get
flutter run
===================================================
FIREBASE RULES:
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {

    match /users/{uid} {
    	allow write: if request.auth != null && request.auth.uid == uid;
    }
    
    match /users/{uid} {
    	allow read: if request.auth != null;
    }
    
    match /chats/{document=**} {
      allow read, create: if request.auth != null;
    }
  }
}
============================================