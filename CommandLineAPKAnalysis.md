# Command Line APK Analysis
This doc explains how to analyse an APK with ClassyShark using command line only. This fits for working on remote machines, Pixel Books or just from the terminal :). 

## (Optional) Get Java & create a working folder
* Get Java - as you need it to run ClassyShark
* $ sudo apt-get install default-jdk
* Create a test folder (to keep all the stuff per APK) $ mkdir testCS

## Install tools
* Use the [script](https://github.com/borisf/effective-bash/blob/master/dev/install.sh)
* Wget from github
* Make it chmod 777
* run

Or the script steps
* // Install fzf - incremental filter
$ wget https://github.com/junegunn/fzf-bin/releases/download/0.17.5/fzf-0.17.5-linux_amd64.tgz
*tar xvzf fzf-0.17.5-linux_amd64.tgz
*chmod 777 ./fzf
*// Install ClassyShark
$ wget https://github.com/google/android-classyshark/releases/download/8.2/ClassyShark.jar

## Get the APK
* Call ClassyShark export with the APK
$ java -jar ClassyShark.jar -export test.apk

Let’s examine the files by the order of importance:

```bash
AndroidManifest.xml_dump - cat AndroidManifest.xml_dump | ./fzf
Package tree - cat all_methods
all_classes.txt - all classes names sorted, could be useful for understanding the packages & dependencies cat all_classes.txt | ./fzf

Browse the relevant class
Mostly if will not need it as it is the most advanced feature
```
Use the [script](https://github.com/borisf/effective-bash/blob/master/dev/class.sh) 
wget from github
Make it chmod 777
run

Or the script steps
```bash
$ cat all_classes.txt | fzf
Select the relevant class and press Enter
FZF will dump the class name
$ java -jar ClassyShark.jar -export test.apk com.google.x  ⇐ note no ending
$tac com.google.x_dump | fzf
```
