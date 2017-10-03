
# Android Project structure simplified

For developing any project which has various files, a build tool is required. Various tools like Ninja, Maven, MAKE and Gradle can be used to build projects. Earlier maven was used to build Android applications in eclipse. Android applications at the OS level are built using MAKE. Generally, now we use Gradle to build android applications.

Gradle is a build tool. It configures how the app is built. There are certain task which need to be performed for an Android application to compile eg Javac compiles java files, XML needs to be encoded, images are compressed and much more. Gradle manages this bulid system and performs the necessary tasks.    


The basic structure of an Android Application built using gradle is shown below.

![](images/projStructure.png)

* **AndroidDemo**

    AndroidDemo is our project name. One project can have more than one app and various modeules. By Default there is only one application in the 'app' folder. You can add more apps in this folder. A project has more than app so that various app can share data between them,

    * **.gradle**

      This is a hidden folder. It is used to store gradle cache. Libraries downloaded are stored. It stores Snapshots and other automatically generated files. Generally there is no need to change anything in this folder.

    * **.idea**

      Android Studio is based on Intellij by Jetbrain. All Intellij IDE settings are stored in '.idea' folder. Example if you increase font for a particular file in AS, the font size remains same when you open the next time. All these type of settings are stored in this folder.

    * **bulid**

      When we build an android app various temporary files are generated like compiled files, compressed files. Build folder contents can be deleted to clean build a project. One point to note is that the built app apk is stored in build folder as well.

    * **Gradle**

      ![](images/gradle.png)

      ![](images/gradleWrapper.png)

      In Gradle folder, we have a wrapper folder, which has a file for gradle properties. It denotes version of the gradle that is used to build the project. Android Studio automatically makes it to the latest version available.

    * **gradle.properties**

      When gradle is run, set property when gradle run. You can increase ram it can consume more than 1.5 or decrease

     * **bulild.gradle**

        We are depending on gradle plugin to run our project. In this file gradle plugin version is mentioned. Android Studio version and gradle plugin version should be same. If you open an earlier project then this version should be changed to match the cureent Android Stusuio version.

      * **settings.gradle**

        In the project modules which are needed to be built are listed in this file. By default it only has 'app'.
