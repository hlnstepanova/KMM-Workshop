# Getting Ready

Install latest [Android Studio version](https://developer.android.com/studio)

Install [XCode, command line tools and Simulator](https://apps.apple.com/us/app/xcode).

Make sure you have Ruby gem installed.
`gem list`

Make sure you have Java JDK installed.
`java --version`

To use the Android KMM Wizard Template, first you need to install a KMM plugin and restart AS.

<img width="508" alt="Screenshot 2022-09-03 at 11 53 31" src="https://user-images.githubusercontent.com/12126043/188325535-67ef7142-5a8e-4e07-a7ce-454774f36ff4.png">

Clone the repository. Try opening the starter project in Android Studio <b>(you need to choose the whole project, not only androidApp)</b>. 

Sync the dependencies:

<img width="338" alt="Screenshot 2022-09-03 at 13 26 34" src="https://user-images.githubusercontent.com/12126043/188325603-26d97612-a295-4111-afc2-5bd36cb10f72.png">

Build and run the app.

<img width="461" alt="Screenshot 2022-09-03 at 13 27 11" src="https://user-images.githubusercontent.com/12126043/188325610-64cf4d94-9eee-4a71-b7b8-958de8e84dd9.png">

If the emulator starts, then everything is fine 👌

<img width="264" alt="Screenshot 2022-09-03 at 13 29 33" src="https://user-images.githubusercontent.com/12126043/188325562-494b83e2-42d1-4a08-86e0-0e3dff6627ad.png">

For ios:
First, in XCode open the  workspace from project -> iosApp -> iosApp.xcwokspace

<img width="366" alt="image" src="https://github.com/user-attachments/assets/700052c0-bb74-4e1b-96bd-4775aec9c991">

Then run the app.

<img width="528" alt="image" src="https://github.com/user-attachments/assets/9caa5c20-09fb-4e57-9e40-e4ccb90c6cad">

You may see some errors regarding shared module first, but try running again.

## If it persists, it may be one of these:

### If you have a Apple M1 Chip and the next command in terminal returns empty:

`echo $LANG`

Then in terminal:

`open -e ~/.zshrc`

And add this line to the opened file:

<b>export LANG=en_US.UTF-8</b>

After saving your .zshrc file, you must run next command:

`source ~/.zshrc`

### If you’re running into Java JDK problem, do the following:
 1) `/usr/libexec/java_home -V`
 
 Your output should be something like:
 
18 (arm64) "Oracle Corporation" - "OpenJDK 18" …/Library/Java/JavaVirtualMachines/openjdk-18/Contents/Home
    1.8.0_292 (x86_64) "AdoptOpenJDK" - "AdoptOpenJDK 8" /Library/Java/JavaVirtualMachines/adoptopenjdk-8.jdk/Contents/Home

 2) `brew install openjdk@17`
 
`sudo ln -sfn /opt/homebrew/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-17.jdk`

 3) `/usr/libexec/java_home -V`
 
  Your output should be something like:

18 (arm64) "Oracle Corporation" - "OpenJDK 18" /Users/lenastepanova/Library/Java/JavaVirtualMachines/openjdk-18/Contents/Home
17.0.7 (arm64) "Homebrew" - "OpenJDK 17.0.7" /opt/homebrew/Cellar/openjdk@17/17.0.7/libexec/openjdk.jdk/Contents/Home
11.0.17 (arm64) "Amazon.com Inc." - "Amazon Corretto 11" /Users/lenastepanova/Library/Java/JavaVirtualMachines/corretto-11.0.17/Contents/Home

 4) `open ~/.zshrc`
 
In zshrc add and save: <b>export JAVA_HOME=$(/usr/libexec/java_home -v 17.0.7)</b>

 5) `export JAVA_HOME='/usr/libexec/java_home -v 17.0.7\'`

 6) Also make sure you're using the correct Gradle JDK version in Android Studio

<img width="400" alt="Screenshot 2023-05-06 at 12 12 08" src="https://user-images.githubusercontent.com/12126043/236618248-b6df361d-6f6c-4d5c-9ebe-97ed4d6acbd6.png">


