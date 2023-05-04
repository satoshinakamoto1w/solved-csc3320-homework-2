Download Link: https://assignmentchef.com/product/solved-csc3320-homework-2
<br>
<span class="kksr-muted">Rate this product</span>

PART 1

<ol>

 <li>What are the differences among grep, egrep and fgrep? Describe using an example.</li>

 <li>Which utility can be used to compress and decompress files? And how to compress multiple files into a single file? Please provide one example for it.</li>

 <li>Which utility (or utilities) can break a line into multiple fields by defining a separator? What is the default separator? How to define a separator manually in the command line? Please provide one example for defining the separator for each utility.</li>

 <li>What does the sort command do? What are the different possible fields? Explain using an example.</li>

</ol>

Part IIa

5. What is the output of the following sequence of bash commands: echo ‘Hello World’ | sed ‘s/$/!!!/g’

6. What is the output for each of these awk script commands?

— 1 &lt;= NF { print $5 }— NR &gt;= 1 &amp;&amp; NR &gt;= 5 { print $1 } — 1,5 { print $0 }— {print $1 }

7. What is the output of the following command line:

echo good | sed ‘/Good/d’8. Which awk script outputs all the lines where a plus sign + appears

at the end of line?

9. What is the command to delete only the first 5 lines in a file “foo”? Which command deletes only the last 5 lines?

Part IIb (10pts each): 50pts

Describe the function (5pts) and output (5pts) of the following commands.

9.

$ cat float

Wish I was floating in blue across the sky, my imagination is strong, And I often visit the daysWhen everything seemed so clear.Now I wonder what I’m doing here at all…

$ cat h1.awkNR&gt;2 &amp;&amp; NR&lt;4{print NR “:” $0

$ awk ‘/.*ing/ {print NR “:” $1}’ float

10. As the next command following question 9, $ awk -f h1.awk float

11.$ cat h2.awk BEGIN { print

“Start to scan file” } {print $1 “,” $NF}

END {print “END-” , FILENAME } $ awk -f h2.awk float

12. sed ‘s/s/t/g’ float

13.

$ ls *.awk| awk ‘{print “grep –color ‘BEGIN’ ” $1 }’ |sh (Notes: sh file runs file as a shell script . $1 should be the output of ‘ ls *.awk ‘ in this case, not the 1st field )

14.

$ mkdir test test/test1 test/test2 $cat&gt;test/testt.txtThis is a test file ^D

$ cd test$ ls -l . | grep ‘^d’ | awk ‘{print “cp -r ” $NF ” ” $NF “.bak”}’ | sh

Part III Programming: 15pts

15. Sort all the files in your class working directory (or your home directory) as per the following requirements:

<ol>

 <li>A copy of each file in that folder must be made. Append the string “_copy” to the name of the file</li>

 <li>The duplicate (copied) files must be in separate directories with each directory specifying the type of the file (e.g. txt files in directory named txtfiles, pdf files in directory named pdffiles etc).</li>

 <li>The files in each directory must be sorted in chronological order of months.</li>

 <li>An archive file (.tar) of each directory must be made. The .tar files must be sorted by name in ascending order.</li>

 <li>An archive file of all the .tar archive files must be made and be available in your home directory.</li>

</ol>