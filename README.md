# glfw-android-port

Hacked Together Port to get GLFW working on Android

**This is still incomplete and needs a lot of refactoring**

Go to `app/src/main/cpp/glfw` to view the GLFW code

Inspiration: https://github.com/xCuri0/glfw-android-example


## Building
You need to have the Android SDK, NDK, Java and Gradle setup

Use `gradle build` to build the project.

The Resulting APK: `app/build/outputs/apk/debug/app-debug.apk`


# TODO
- [X] Initialize Basic Application
- [X] Add OpenGL ES Support
- [ ] Implement Miscellaneous Methods
- [X] Add Vulkan Support
- [ ] Get Input from Keyboard
- [ ] Get Input from Mouse
- [ ] Get Input from Joystick
- [ ] Implement Java and JNI*
