###################
**Shell Questions**
###################

1. What is the file redirection for success output, error output?
1 is positional parameter for success output and 2 is positional paramter for error output.
2. How can you provide both redirection for success and error output in same file?
&> {filename} this way you can redirect both success and failure output to one file.
3. What is the output for java -version?

The output of java -version is failure and its stored in positional paramter 2.

4. Write a shell script to determine if a file is present echo the file is present and if not file is not present?
```shell

#!/bin/bash

set -ex

echo "script to check if a file exists"

if [[ -e mahesh.txt ]]; #-e is operator to check if file exists and -z is for string if its empty or not.
then
        echo "File exists"
else
        echo "File doesn't exist"
fi

```
5. What is $1,$0, $?,$#,$@, $* in shell scripts?
$1 first positional parameter , $0 is name of script or command that is executed, $? is the exit status of shell script, $# is the count of positional parameters, $@ is the list of positional parameters (list a list in python), $* is where the entire positional parameters as one single string.
6. How can you determine if a directory is present and echo that the directory is available if not directory is not available?
To determine if a directory is empty -d parameter.

```shell

#!/bin/bash

set -ex

echo "script to check if a file exists"

if [[ -d /apps ]];
then
        echo "Directory exists"
else
        echo "Directory doesn't exist"
fi
```
