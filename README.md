# Classyshark User Guide
ClassyShark <link> is a handy Android and Java executable browser. This doc will guide you over the steps, how to use 
ClassyShark effectively.

## Open an archive
The first steps is to open an APK. Click on the open button and select your APK file. In addition to APK ClassyShark 
can open and show other Android and Java binary files such as dex, class, jar and aar.


![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/1%20Open%20File.png)

## Browse components
Once ClassyShark finishes reading the APK, you see the following APK breakdown (here I am using the Google IO app).

![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/2%20Browse%20components)

Click on the left tree and explore the elements and data on the right panel. 

## Inspect package method counts (multidex)
Click on methods count tab. On the right panel you see the packages pie-chart and packages contribution to classes.dex. Clicking on chart elements will bring the furth sub package methods break down.

![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/3%20Browse%20Method%20count)

## Incremental Search
Note the incremental search bar on top, where you can search & filter classes by either writing the full name or camel search.

The ==> arrow open the top most class while the <== arrow returns to the full classes list.

![alt text](https://github.com/borisf/classyshark-user-guide/blob/master/images/4%20Search)


## Command line
* [Command line reference](https://github.com/google/android-classyshark/blob/master/CommandLine.pdf)

## Related work

* [Android Difest 17 - Russian](https://dou.ua/lenta/digests/android-digest-17/)
* [App Diets are not a Fad](http://blog.nimbledroid.com/2016/06/15/app-diets-not-a-fad.html)
* [Tim Melor's multidex](https://github.com/tmelz/multidex_notes)
* [Droidcon IT 2016 recap](http://jeroenmols.com/blog/2016/04/08/droidconit/)
* [To infinity abd 65K](https://speakerdeck.com/dextor/to-65k-and-beyond)
* [Smaller APKs with ClassyShark](http://blog.jimbaca.com/2016/04/04/smaller-apks-with-classy-shark/)
* [Jianshu - Chinese](http://www.jianshu.com/p/8e8b88ea2197)
* [Shrinking your build with no rules] (https://medium.com/@_tiwiz/shrinking-your-build-with-no-rules-8d9fb88281ac#.fiiqi3v3a)
* [Native code browsing with ClassyShark](https://medium.com/@BorisFarber/classyshark-supports-native-code-browsing-a4985e7126b1#.kkw2lt4wz)
* [Inspecting multidex APK with ClassyShark](https://medium.com/@BorisFarber/inspecting-your-apk-f53fb90136da#.d4os6nqdp)
* [Intro to ClassyShark](https://medium.com/@BorisFarber/welcome-classyshark-b632ae8488b4#.4zcdc3kwd)




