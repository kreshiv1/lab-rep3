# lab-rep3

## PART 1

FAILED TEST-
```
import static org.junit.Assert.assertArrayEquals;
public class TestReverseInPlace {
  @org.junit.Test
  public void testReverseInPlace() {
    int[] input1 = {3, 4, 5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{5, 4, 3}, input1);
  }
}
```
PASSED TEST-
```
import static org.junit.Assert.assertArrayEquals;
public class TestReverseInPlace {
  @org.junit.Test
  public void testReverseInPlace() {
    int[] input1 = {3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3}, input1);
  }
}

```

SYMPTOM-
!IMAGE[3BABCC67-B20C-4CAE-93CF-D35FA2D2318A_4_5005_c.jpeg]












CODE BEFORE FIXING BUG-
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
  arr[i] = arr[arr.length - i - 1];
  }
}
```
CODE AFTER FIXING BUG-
```
 static void reverseInPlace(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[i];
      
    }
  }
```







## PART 2 
I will be using the `find` command for this report. <br/>

the first option i used was `-type`. <br/>

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

## 

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

##

third option is exec which is short for execute. this exectues a specfic command to the files which match the name pattern.

```
kreshivchawla@Kreshivs-MacBook-Air docsearch % find technical -name "1468*. txt" -exec rm {} \;
```
the above code produces no output in the terminal. it uses `-exec` and its `rm` option which removes everything that matches the `-name` pattern.
in this example, it removed every text file whose name starts with "1468". being able to remove files based on a naming pattern is very useful.


```
kreshivchawla@Kreshivs-MacBook-Air docsearch % find technical -name plos -exec rm <} \;
rm: technical/plos: is a directory
```
in the above example I entered a directory name before executing the remove command. this resulted in a messsage which stated the path of the directory. this means we cannot remove a directory using these commands.

##

the fourth command option is `size`

~~~
kreshivchawla@Kreshivs-MacBook-Air docsearch % find technical -size +200k

technical/government/About_LSC/commission_report.txt
technical/government/Env_Prot_Agen/bill.txt
technical/government/Gen Account_Office/GovernmentAuditingStandardsyb2002ed.txt
technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
technical/government/Gen Account_Office/d01591sp.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-3.txt
~~~

this dispayed all files whose size was greater than 200 Kilo Bytes. filtering out files based on their memory size is very useful.

```
kreshivchawla@Kreshivs-MacBook-Air docsearch % find technical -size +300k
```

this produced no output as not file in technical was more than 300 Kilo Bytes.


##
SOURCE:
I used the `man` command in  terminal and read through the manual of the `find` command to write a report about its options.


























