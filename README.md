# SNPE_Image_Classifier
This is the implementation step of SNPE Image Classifier Tutorial, fixed some out-of-date problem in original code.

As the tutorial is writen for old version, directly follow the tutorial will cause a lot of problem. so we should make some change in its gradle files.

In *build.gradle(Project:image-classifiers)*, we substitute,
```
compile files('libs/snpe-release.aar')
```
with
```
implementation files('libs/snpe-release.aar')
```
And chage *compileSdkVersion* to *21*, *buildToolsVersion* to *"21"*.

Then change the *sourceSets* with,
```
  sourceSets {
      main{
          jniLibs.srcDirs=['src/main/libs']
      }
  }
```

In *build.gradle(Project:image-classifiers)*, we add *google()* at the top of *buildscript->repositories*.

Finally, if you use Andriod Studio, go to *file->project structure* and set *Android Gradle Plugin Version* to *3.3.2*, *Gradle Version* to *4.10.1*.

