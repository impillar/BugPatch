Use gradle to build Android projects without GUI in Ubuntu.

**1. Cannot find specific Build Tools**

```sh
FAILURE: Build failed with an exception.

* What went wrong:
A problem occurred configuring project ':app'.
> failed to find Build Tools revision 23.0.3
```
Please run the command to get the list of build tools.
```sh
[ANDROID_SDK]/tools/android list sdk -a
```
It will return a list of tools as follows:

```sh
Packages available for installation or update: 150
   1- Android SDK Tools, revision 25.1.1
   2- Android SDK Tools, revision 25.1.2 rc1
   3- Android SDK Platform-tools, revision 23.1
   4- Android SDK Platform-tools, revision 24 rc2
   5- Android SDK Build-tools, revision 24 rc3
   6- Android SDK Build-tools, revision 23.0.3
   7- Android SDK Build-tools, revision 23.0.2
   8- Android SDK Build-tools, revision 23.0.1
   9- Android SDK Build-tools, revision 23 (Obsolete)
```
Then you can install the specific build tool with 

```sh
[ANDROID_SDK]/tools/android update sdk -u -a -t [ITEM_NUM]
```
The `-a` option means `--all`, `-u` means `--no-ui`, `-t` is used to specify the number of items. 


**2. Cannot find aapt**

When you run `gradle build` in the Android project, you may encounter a problem that cannot find the aapt program like the following

```sh
java.io.IOException: Cannot run program "[ANDROID_SDK]/build-tools/23.0.3/aapt": error=2, No such file or directory```

You can fix it by installing `lib32stdc++6` and  `lib32z1`

