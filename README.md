# Q4WineGUI-macOS
I compiled this for apple silicon for whatever reason lol.

# NOTES, important. #

run these two commands
```
 brew install qt
 mv "q4wine.app" "/opt/homebrew/Cellar/qt/6.9.0/lib/"  
 ```
 It was kind of a beezy to compile this on macOS, after it was a 'success' i had an app that wouldnt run, i hit it with lldb and ran exec directly, with clean exits and no useful debug info, but discovered upon trying again with sudo, it was actually looking for a dylib in several paths, if you have SIP enabled, the homebrew one was the only one writeable directory. The actual location which was actually like /opt/homebrew/Cellar/qt/6.9.0/lib../../../TheQ.app/Frameworks/A/el-Dylib which boils down to the path i suggested, its not worth compiling properly or fixing that dylib path, to be completely honest, but I thought id slap this here, Before any of you Wine + macOS users and enthusiasts waste time on this. 
