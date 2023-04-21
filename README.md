#KSA Compiler
This project is a Java compiler that performs the lexical, syntactic, and semantic process of a source code file in the KSA language. It uses JFlex and CUP tools to generate the lexer and parser.

The compiler takes a source code file in the KSA language as input and produces an assembler code file for the 68K architecture as output. The compiler is packaged in a .jar file that can be executed from the command line.

##Requirements
-Java 8 or higher
-JFlex
-CUP

##Installation
1. Clone or download the project repository.

2. Make sure JFlex and CUP are installed on your system. If they are not installed, download and install them following the instructions on each tool's website.

3. Open a terminal and navigate to the project root directory.

3. Compile the lexer and parser with the following commands:


$ jflex lexer.jflex
$ cup -parser Parser parser.cup

4. Compile the project with the following command:


$ javac -cp .:cup.jar *.java

5. Package the project into a .jar file with the following command:


$ jar cvfm KSACompiler.jar manifest.txt *.class

##Usage
To use the compiler, run the .jar file with the following command:

$ java -jar KSACompiler.jar input-file.ksa
Where input-file.ksa is the KSA language source code file you want to compile. The compiler will generate an input-file.s file that contains the assembler code for the 68K architecture.


