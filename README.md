# java_csv_sqlite
Read Comma Separated Value (CSV), analyse, read and validate the csv data and write to SQLite Database with log, update to custom log file and view information and detail in realtime

## To Compile 
The program uses the JDBC for SQLite which is located in the [lib](./lib/) folder [sqlite-jdbc-3.23.1.jar](https://github.com/mahidharakarapu/java_csv_sqlite/blob/master/lib/sqlite-jdbc-3.23.1.jar)
The source files in the src folder is compiled with the JDBC library. Compile the java source files to a /dist/ directory in main folder
Navigate to the [src/javacsv](./src/javacsv/) folder. The source file s will be listed which includes.
	- Main.form - for Netbeans Designer 
	- Main.java - the source code
	
### Compiling for immediate test.
```bash

$ javac -d ../../dist/ -classpath ".:../../lib/sqlite-jdbc-3.23.1.jar" Main.java
$ java Main

```
	
### Compiling to Java Executable (jar).
```bash

$ cd ./src/javacsv
$ mkdir "../../dist/" && mkdir "../../dist/lib/" && mkdir "../../dist/META-INF/"
$ javac -d ../../dist/ *.java
$ cd ../../dist/
$ cp ../lib/sqlite-jdbc-3.23.1.jar ./lib/
$ echo Main-Class: javacsv.Main > ./META-INF/MANIFEST.MF
$ jar cmvf META-INF/MANIFEST.MF java_csv_sqlite.jar javacsv/*.class
$ rm -R "./javacsv" && rm -R "./META-INF"

```