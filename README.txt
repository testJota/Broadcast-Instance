Here I write a code to execute one broadcast instance (one source, crash tolerant),
the main purpose of this code is to code is to get used to the Akka library,
that will probably be an import part in future projects.


## Important Notes


In order to use the akka library correctly, it seems that installing Maven is necessary.
The installation is quite simple, but on windows it can be troublesome:

 - First we need to download it in Maven's website: https://maven.apache.org/

 - After obtaining the files, we need to add the "bin" directory to the Path

 - Since windows complicate Path variables, in order to add "bin" to the Path I
used the PowerShell command:

* [Environment]::SetEnvironmentVariable("Path", $env:Path + ";C:\apache-maven-3.8.2\bin", "Machine")

Which does it permanently. And now the "mvn" command is available on PowerShell.


 - In order to change the file with the main class, first it is needed to modify
the "pom" file in the "broadcast" directory. After <<Java>> and <<-classpath>> you
have the name of the file with the main class.