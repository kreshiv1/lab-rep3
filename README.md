# lab-rep3

## PART 1

## PART 2 
I will be using the `find` command for this report. br/

the first option i used was `-type`. br/

~~~
kreshivchawla@Kreshivs-MacBook-Air docsearch % find technical -type d

technical
technical/government
technical/government/About_LSC
technical/government/Env_Prot_Agen
technical/government/Alcohol_Problems
technical/government/Gen_Account_Office
technical/government/Post_Rate_Comm
technical/government/Media
technical/plos
technical/biomed
technical/911report
~~~
the above exmaple used `find` command with the option `-type` and its option `-d`. this displayed all directories inside the technical directory.
this is useful as when dealing with large number of files and directories, having a list of all the directories could be quite helpful.

~~~
kreshivchawla@Kreshivs-MacBook-Air docsearch % find technical ! -type f

technical
technical/government
technical/government/About_LSC
technical/government/Env_Prot_Agen
technical/government/Alcohol_Problems
technical/government/Gen_Account_Office
technical/government/Post_Rate_Comm
technical/government/Media
technical/plos
technical/biomed
technical/911report
~~~
the above exmaple used `find` command with the option `-type` but with the "not" option `!` before it and its option `-f`. this displayed everthing which is not a file inside the technical directory.
this is useful as when dealing with large number of files and directories, having a list of all the directories could be quite helpful.

## \n

second option is `-name`

~~~
kreshivchawla@Kreshivs-MacBook-Air docsearch % find technical -name "1468*. txt"

technical/biomed/1468-6708-3-10.txt
technical/biomed/1468-6708-3-4.txt
technical/biomed/1468-6708-3-7.txt
technical/biomed/1468-6708-3-3.txt
technical/biomed/1468-6708-3-1.txt
~~~
the above example shows all text files that start with "1468" in technical directory. finding specefic files with a name pattern is very useful.

~~~
kreshivchawla@Kreshivs-MacBook-Air docsearch % find technical -name biomed
technical/biomed
~~~
the above example displays the path of the entered directory.



