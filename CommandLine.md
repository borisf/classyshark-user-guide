# Command Line

Together with a stylish UI ClassyShark provides a rich API and command line functionality. In this part we are 
going to explore what ClassyShark can do for you from the command line.  In the upcoming API section we see how
ClassyShark provides APIs to every data in String form. One can use the export Java APIs as part of one’s build 
and continuous integration pipeline. Here are the command line services.

**Open APK with ClassyShark**
```bash
 java -jar ClassyShark.jar -open <YOUR_APK.apk>
 ```

**Open your APK in ClassyShark and show a specific class in GUI**
```bash
java -jar ClassyShark.jar -open <BINARY_FILE> <FULLY_QUALIFIED_CLASS_NAME>
```
Opens the ClassyShark GUI with the specific class showing in the UI plane.

**Export APK**
```bash
java -jar ClassyShark.jar -export <BINARY_FILE>
```

ClassyShark will analyze the APK and dump out the following files, in a grep friendly fashion:
* all_classes.txt - list of all classes
* all_methods.txt - all the method names and signatures from all the dexes
* all_strings.txt - all the string tables from all the dexesall_strings.txt - all the string tables from all the dexes
* AndroidManifest.xml_dump - goes without saying

**Export a specific class from APK**
```bash
java -jar ClassyShark.jar -export <BINARY_FILE> <FULLY_QUALIFIED_CLASS_NAME>
```
ClassyShark generates and dumps a text file, which is a human readable representation of the class, passed as parameter.

**Dump all packages with their method counts**
```bash
java -jar ClassyShark.jar -methodcounts <BINARY_FILE>
```
ClassyShark dumps all the packages tree with packages method counts.

**Inspect APK(experimental)**
```bash
java -jar ClassyShark.jar -inspect <YOUR_APK.apk>
```
Dumps out to command prompt all the classes that have test as their class names, native and abstract methods.



