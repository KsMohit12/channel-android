# Channel SDK for Android

[ ![Download Here]() ](https://s3-us-west-2.amazonaws.com/co.getchannel.builds/android-sdk/channel.aar)

 Channel SDK is a library designed to simplify the development with our API.
 
 ## Setup SDK
 
 ### 1.dowload our SDK to your library 
 ### 2.add maven repositories and config library directory in your project build.gradle 
   ```gradle
allprojects {
    repositories {
        jcenter()
        maven { url "https://jitpack.io"} // maven repository
        flatDir{dirs 'libs'} //direct path to your library folder
    }
}
```
 ### 3.add dependencies to your project build.gradle
  ```gradle
        classpath 'com.github.dcendents:android-maven-gradle-plugin:1.3'
        classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.7.1'
```
### 4.add code below to your module build.gradle
 ```gradle
    compile (name: 'channel-release', ext:'aar')
    compile 'com.github.jkwiecien:EasyImage:1.3.1'
    compile 'com.afollestad.material-dialogs:core:0.9.0.2'
    compile "com.google.android:flexbox:0.2.5"
    compile "com.android.support:appcompat-v7:26.0.0-alpha1"
    compile "com.android.support:cardview-v7:26.0.0-alpha1"
    compile "com.android.support:design:26.0.0-alpha1"
    compile "com.github.siyamed:android-shape-imageview:0.9.3"
    compile "me.relex:circleindicator:1.2.2@aar"
```
### 5.set up channel application key in your main activity
 ```java
  Channel.setupActivityWithApplicationID(new WeakReference<Activity>((Activity)this),"YOUR_APPLICAION_KEY",null,null);
 ```
