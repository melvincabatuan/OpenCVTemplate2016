# Minimal Android OpenCV Template Project 2016

* Android Studio 2.2 (Preview 3)
* OpenCV Version 3.1.0
* Tested on API 19 (Kitkat Android 4.4.4)

![](https://github.com/melvincabatuan/OpenCVTemplate2016/blob/master/device-2016-06-12-142556.png)

## App 'build.gradle'

```
apply plugin: 'com.android.application'

android {
    compileSdkVersion 23
    buildToolsVersion "23.0.2"
    defaultConfig {
        applicationId "ph.edu.dlsu.opencvtemplate2016"
        minSdkVersion 19
        targetSdkVersion 23
        versionCode 1
        versionName "1.0"
        testInstrumentationRunner "android.support.test.runner.AndroidJUnitRunner"
    }
    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
    }
}

dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
    compile 'com.android.support:appcompat-v7:23.4.0'
    compile 'com.android.support.constraint:constraint-layout:1.0.0-alpha3'
    testCompile 'junit:junit:4.12'
    androidTestCompile 'com.android.support.test.espresso:espresso-core:2.2.2'
    androidTestCompile 'com.android.support.test:runner:0.5'
    androidTestCompile 'com.android.support:support-annotations:23.4.0'

    compile project(":opencv-java")
}
```
