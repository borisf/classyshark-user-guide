# Classyshark User Guide

[ClassyShark](https://github.com/google/android-classyshark) is under current and heavy development, so remember to check this page frequently :snowflake:.

## About ClassyShark

We developed this software because we needed something lighting fast and incredibly lightweight for browsing Android `APK`s, so that we could check right away if everything we wanted was right inside the final executable. And this is where the story begins - be sure to checkout the blogpost [Intro to ClassyShark](https://medium.com/@BorisFarber/welcome-classyshark-b632ae8488b4#.4zcdc3kwd) to understand the problem it solves.

## Open an archive
Before we can start browsing anything, we need to open it. And this is pretty straight forward: you can do it by clicking on the
folder icon in the top bar, as in this screenshot.

![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/1%20Open%20File.png)

Remember that **ClassyShark** does not stop to Android `APK`, but you actually see the content of `.dex` files, as well as `.class`, `.jar` and `.aar`s.

## Browse components
Right after **ClassyShark** loads your executable, you will see, in the left panel, the list of the root components of the archive.
In the example, we are using the Google IO Android app, and you can notice right away that we see the `AndroidManifest.xml` file and the `classes` and `res` folders
at the very top of the tree, as we just opened the `APK` file.

![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/2%20Browse%20components)

By clicking on the folders, we will see the tree expand and, when we reach a leaf (that would be a Java file, in this case), by clicking on it, we would see its content
on the right pane, where the **ClassyShark** logo is. Easy!

Now, what if we find, for instance, a class that extends `Activity` and we want to see what's in there? Well, we are just a double click away from knowing it!
In fact, by clicking twice on a type, **ClassyShark** will bring on the source for that type, so that you can browse the code freely. How cool is that?

## Inspect package method counts (multidex)
Raise your hand if you found yourself in the situation of counting the number of methods in your APK. We found ourselves in that critical situation while we tried to
reduce the size of the project we were working on and that is why we built a method counter interface inside **ClassyShark**.

See the method count, that your runtime sees

![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/5%20ClassesDexData.png)

You can activate the view by simply clicking on the *Methods count* tab on top of the navigation tree. In a blink of an eye, you will have a browsable chart of the methods used by everything in you APK, with the possibility of navigate even further by using the same mechanisms we saw in the previous paragraph.

![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/3%20Browse%20Method%20count)

## Incremental Search
*Why do I have to click all the navigation to my class?* Well, you **do not have to**!
**ClassyShark** ships with a handy search field, that you can use to filter the classes by writing a matching query, that will be automagically applied to the content of the archive.

![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/4%20Search)

You can also use the arrows on top to navigate back and forth the history of the app!

## Native Code

![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/3%20Browse%20Method%20count)


## Export
The *export* button, that will give you a report with all the relevant information about the archive and, on its side, you will find the *history* one, that will help you restoring previously loaded archives (they will persist upon application closing).

## Scenarios
1. Obfuscation
2. Dependencies
3. Dex Numbers
4. Native Code

## Command line
* [Command line reference](https://github.com/google/android-classyshark/blob/master/CommandLine.pdf)

## Related work
* [Android Digest 17 - Russian](https://dou.ua/lenta/digests/android-digest-17/)
* [App Diets are not a Fad](http://blog.nimbledroid.com/2016/06/15/app-diets-not-a-fad.html)
* [ClassyShark verrät, was sich im APK versteckt - German](http://www.heise.de/developer/artikel/ClassyShark-verraet-was-sich-im-APK-versteckt-3217655.html)
* [Tim Melor's multidex](https://github.com/tmelz/multidex_notes)
* [Droidcon IT 2016 recap](http://jeroenmols.com/blog/2016/04/08/droidconit/)
* [To infinity abd 65K](https://speakerdeck.com/dextor/to-65k-and-beyond)
* [Smaller APKs with ClassyShark](http://blog.jimbaca.com/2016/04/04/smaller-apks-with-classy-shark/)
* [Jianshu - Chinese](http://www.jianshu.com/p/8e8b88ea2197)
* [Shrinking your build with no rules](https://medium.com/@_tiwiz/shrinking-your-build-with-no-rules-8d9fb88281ac#.fiiqi3v3a)
* [Native code browsing with ClassyShark](https://medium.com/@BorisFarber/classyshark-supports-native-code-browsing-a4985e7126b1#.kkw2lt4wz)
* [Inspecting multidex APK with ClassyShark](https://medium.com/@BorisFarber/inspecting-your-apk-f53fb90136da#.d4os6nqdp)
* [Intro to ClassyShark](https://medium.com/@BorisFarber/welcome-classyshark-b632ae8488b4#.4zcdc3kwd)

## Future development
We are constantly looking for new features to make **ClassyShark** a better product, if you think we should add something, open an issue on the **ClassyShark** repo and we'll be happy to discuss about it!
