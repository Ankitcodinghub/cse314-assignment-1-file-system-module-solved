# cse314-assignment-1-file-system-module-solved
**TO GET THIS SOLUTION VISIT:** [CSE314 Assignment 1-File System Module Solved](https://www.ankitcodinghub.com/product/cse314-assignment-1-file-system-module-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;96984&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE314 Assignment 1-File System Module Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

1 Assignment Description

You are given the following binary file format, which we will call from now on SF (i.e. “section file”) format. A SF file consists in two areas: a header and a body. The overall SF file structure is illustrated below. It can be noted that the file header is situated at the beginning of the file, before the file’s body.

<pre>                        SF FILE STRUCTURE
</pre>
HEADER BODY

A SF file’s header contains information that identifies the SF format and also describes the way that file’s body should be read. Such information is organized as a sequence of fields, each field stored on a certain number of bytes and having a specific meaning. The header’s structure is illustrated in the HEADER box below, specifying a name for each header’s field and the number of bytes that field is stored on (separated by “: ”). Some fields are just simple numbers (i.e. MAGIC, HEADER SIZE, VERSION, and NR OF SECTIONS), while others (i.e. SECTION HEADERS and SECTION HEADER) have a more complex structure, containing their own sub-fields. Such, the SECTION HEADERS is actually composed by a sequence of SECTION HEADER fields (elements), each such field in its turn being composed by four sub-fields: SECT NAME, SECT TYPE, SECT OFFSET, and SECT SIZE.

HEADER

<pre> MAGIC: 4
 HEADER_SIZE: 2
 VERSION: 1
 NO_OF_SECTIONS: 1
 SECTION_HEADERS: NO_OF_SECTIONS * sizeof(SECTION_HEADER)
</pre>
<pre>     SECTION_HEADER: 10 + 1 + 4 + 4
         SECT_NAME: 10
</pre>
<pre>         SECT_TYPE: 1
         SECT_OFFSET: 4
         SECT_SIZE: 4
</pre>
The meaning of each field is the following:

• The MAGIC field identifies the SF files. Its value is specified below.

1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
<ul>
<li>The HEADER SIZE field indicates the size of the SF files’ header.</li>
<li>The VERSION field identifies the version of the SF file format, presuming the SF format could be changed a bit from one version to another, though not the case in your assignment, even if the version numbers could be different between different SF files — see below.</li>
<li>The NO OF SECTIONS field specifies the number of the next SECTION HEADER elements, which are covered in the description above by the SECTION HEADERS name (field).</li>
<li>The SECTION HEADER’s sub-fields are either self explanatory (e.g. SECT NAME or SECT TYPE) or their meaning is explained below.
The SF file’s body, basically a sequence of bytes, is organized as a collection of sections. A section consists in a sequence of SECT SIZE consecutive bytes, starting from the byte at offset SECT OFFSET in the SF file. Consecutive sections could not necessarily be placed one near the other. In other words, there could be bytes between two consecutive sections not belonging to any section described in the SF file’s header. A SF file’s section contains printable characters and special line-ending characters. We would say thus that they are text sections. Bytes between sections could contain any value. They are however of no relevance for anyone interpreting a SF file’s contents. The box below illustrates two sections and their corresponding headers in a possible SF file.

<pre>                PARTIAL SF FILE’s HEADER AND BODY
</pre>
Offset Bytes
</li>
</ul>
<pre> 0000:   ...
 ...     ...
 xxxx:   SECT_1 TYPE_1 1000 10
 yyyy:   SECT_2 TYPE_2 2000 10
 ...     ...
</pre>
<pre> 1000:   1234567890
</pre>
<ul>
<li>… &nbsp;…</li>
<li>… &nbsp;…</li>
</ul>
<pre> 2000:   1234567890
 ...     ...
</pre>
The following restrictions apply to the values certain fields in a SF file could take:

<ul>
<li>The MAGIC’s value is “jAWa”.</li>
<li>VERSION’s value must be between 12 and 37, including that values.</li>
<li>The NO OF SECTIONS’s value must be between 4 and 15, including that values.</li>
<li>Valid SECT TYPE’s values are: 10 25 .</li>
<li>Section lines are separated by the following sequence of line-ending bytes
(values are hexadecimal): 0A.

2
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
2 Assignment’s Requirements

Your are required to write a C program named “a1.c” that implements the following requirements.

2.1 Compilation and Running

Your C program must be compiled with no error in order to be accepted. A sample compilation command should look like the following:

<pre>                       Compilation Command
</pre>
<pre> gcc -Wall a1.c -o a1
</pre>
Warnings in the compilation process will trigger a 10% penalty to your final score.

When run, your resulted executable (we name it “a1”) must provide the minimum required functionality and expected results, in order to be accepted. What such minimum means, will be defined below. The following box illustrates the way your program could be run. The options and parameters your program must accept and their meaning will be explained in the following sections.

<pre>                         Running Command
 ./a1 [OPTIONS] [PARAMETERS]
</pre>
2.2 Variant Output

Each student receives a slightly modified variant of the SF format and the assignment’s requirements. For the first task, you should be able to output the identifier of your assignment variant, when your program will be run like below. Display Variant Command

<pre> ./a1 variant
            Output Sample for Display Variant Command
</pre>
55777

2.3 Listing Directory Contents

When being given the “list” option, your program must display on the screen the names of some elements (i.e. files, sub-directories) in the directory whose path is specified with the command line “path” option in the form illustrated in the following box.

<pre>                      List Directory Command
 ./a1 list [recursive] &lt;filtering_options&gt; path=&lt;dir_path&gt;
</pre>
Note that the command line options could be given in any order, e.g. the “recursive” option could be given before or after the other options.

Which element names must be displayed is determined based on the filtering criteria mentioned below. Each element name must be displayed on a different line, with no blank lines between valid names, in the form illustrated by the box below, i.e. the element’s name prepended with the directory path specified by the “path” option. If no name complying the requested criteria is found, nothing but the “SUCCESS” string must be displayed.

3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
<pre>     Sample Output for List Directory Command (Success Case)
 SUCCESS
</pre>
<pre> test_root/test_dir/file_name_1
 test_root/test_dir/file_name_2
 test_root/test_dir/file_name_3
 ...
</pre>
If the “recursive” option is also specified, your program should traverse the entire sub-tree starting from the given directory, entering recursively in all the sub-folders, sub-sub-folders and so on. Found element names must also contain their path relative to the given directory. The two boxes below illustrate the way the program could be run recursively and a possible output for that case, respectively.

<pre>                  Sample List Directory Command
 ./a1 list recursive path=test_root/test_dir/
</pre>
<pre>     Sample Output for List Directory Command (Success Case)
 SUCCESS
</pre>
<pre> test_root/test_dir/file_name_1
 test_root/test_dir/file_name_2
 test_root/test_dir/subdir_1/file_name_1
 test_root/test_dir/subdir_1/subdir_1_1/file_name_2
 test_root/test_dir/subdir_2/file_name_3
</pre>
…

In case an error is encountered, an error message followed by an explanation must be displayed, in the form illustrated by the following box.

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>          Output for List Directory Command (Error Case)
 invalid directory path
</pre>
The filtering criteria used to select the elements whose names must be dis- played on the screen are the following:

<ul>
<li>Element’s name must end with the sequence of characters specified with the filtering option “name ends with=string”. You should consider any type of elements, e.g. both files and directories.</li>
<li>The listed element must have “write” permission for its owner, specified by the filtering option “has perm write”. You should consider any type of elements, e.g. both files and directories.
Note that even if in practice more filtering criteria could be given in the same command line, our tests use only one single criterion at a moment. Though, your program could consider the more general case, if you want, even if not a compulsory requirement.

Also note that the order of the listed names is not important for our tests, but only their number and value.

4
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
ERROR

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
2.4 Identifying and Parsing Section Files

When being given the “parse” option, your program must check if the file whose path is specified with the command line “path” option complies or not the SF format. The way the program could be run for this is illustrated in the following box.

<pre>                     Check SF Format Command
 ./a1 parse path=&lt;file_path&gt;
</pre>
Similar to the note above, the command line options could be given in any order, and your program should support this.

The way the SF format compliance must be checked is based on the following criteria:

<ul>
<li>The value of the magic field is the one mentioned before, i.e. “jAWa”.</li>
<li>The values of the file version must be one from the interval mentioned
above, i.e. between 12 and 37, including that values.
</li>
<li>The number of sections must be between the mentioned values, i.e. 4 and 15, including that values.</li>
<li>The existing sections’ type must be only in the set mentioned above, i.e. 10 25 .
When all the above criteria are met, the file could be considered as being compliant with the SF format, even if some other inconsistencies could still be found in it, like the size of the file being less than at least one section’s beginning (i.e. section’s offset) or end (i.e. section’s offset plus section’s size), or having overlapping sections.

In case the given file does not comply the SF format, an error message must be displayed on the screen, followed by the failure reason mentioning the first field the checking failed on, in the form illustrated by the box below.
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>               Sample Output for an Invalid SF File
 wrong magic|version|sect_nr|sect_types
</pre>
In case the given file complies the SF format, some of its checked fields must be displayed on the screen in the form illustrated by the box below.

<pre>                Sample Output for a Valid SF File
</pre>
<pre> SUCCESS
 version=&lt;version_number&gt;
 nr_sections=&lt;no_of_sections&gt;
 section1: &lt;NAME_1&gt; &lt;TYPE_1&gt; &lt;SIZE_1&gt;
 section2: &lt;NAME_2&gt; &lt;TYPE_2&gt; &lt;SIZE_2&gt;
 ...
</pre>
5

</div>
</div>
<div class="layoutArea">
<div class="column">
ERROR

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
2.5 Working With Sections

When being given the “extract” option, your program must find and display some part of a certain section of a SF file. In particular, a single line must be extracted. The needed command line arguments are given using the “path”, “section” and “line” options, for the file path, section number and line number respectively, as illustrated in the following box.

<pre>                   Extract Section Line Command
 ./a1 extract path=&lt;file_path&gt; section=&lt;sect_nr&gt; line=&lt;line_nr&gt;
</pre>
In case an error is encountered, an error message followed by an explanation must be displayed, in the form illustrated by the following box.

<pre>   Sample Output for Extract Section Line Command (Error Case)
 ERROR
</pre>
<pre> invalid file|section|line
</pre>
In case the given file is of the SF format and the searched section and line are found, the result should be displayed as illustrated in the box below.

<pre>  Sample Output for Extract Section Line Command (Success Case)
 SUCCESS
 &lt;line_content&gt;
</pre>
The line numbers are counted from the section start, the first line being line 1.

The lines should be displayed in reversed order (from the last character to the first).

2.6 Section Filtering

When being given the “findall” option, your program must function similar to the case when run with the “list recursive” options, though it must search only for SF files that have no section with size greater than 1202.

The way the program could be run for this is illustrated in the following box.

<pre>                  Find Certain SF Files Command
 ./a1 findall path=&lt;dir_path&gt;
</pre>
In case an error is encountered, an error message followed by an explanation must be displayed, in the form illustrated by the following box.

<pre>      Output for Find Certain SF Files Command (Error Case)
 ERROR
</pre>
<pre> invalid directory path
</pre>
Normal output must be displayed in the form illustrated by the box below.

<pre>  Sample Output for Find Certain SF Files Command (Success Case)
 SUCCESS
 test_root/test_dir/file_name_1
 test_root/test_dir/file_name_2
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
…

</div>
</div>
<div class="layoutArea">
<div class="column">
6

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
3 User Manual 3.1 Self Assessment

In order to generate and run tests for your solution you could simply run the “tester.py” script provided with your assignment requirements. The script re- quires Python 3.x, not Python 2.x.

<pre>               Sample Command for Tests Generation
 python3 tester.py
</pre>
Even if the script could be run in MS Windows OS (and other OSes), we highly recommend running it in Linux, while this is how we run it by ourselves, when evaluating your solutions.

When running the script, it generates a “test root” directory, containing all sort of files and sub-directories used to check your solution. Even if the contents of the “test root” directory is randomly generated for each student, for the same student it is (with a high probability) the same, independently of how many times you run the script. The only difference could be between different OSes.

After creating the testing directory’s contents, the “test root” script also runs your program against it, displaying the results of the different tests it runs. There should be normally 65 test, though sometimes less than that could also happen. The maximum grade (10) is gained when all tests pass and no penalty is applied (see below). The precise grade is calculated by scaling the number of points your solution gains due to test passing to the 0-10 scale.

Restrictions:

• You are required and restricted to use only the OS system calls, i.e. low- level functions, not higher-level one, in your entire solution, in all lab as- signments. For instance, regarding the file accesses, you MUST use system calls like open(), read(), write() etc., but NOT higher-level functions like fopen(), fgets(), fscanf(), fprintf() etc. The only accepted ex- ceptions from this requirement are the functions to read from STDIN or display to STDOUT / STDERR, like scanf(), printf(), perror() and func- tions for string manipulation and conversion like sscanf(), snprintf().

Recommendations:

• For string tokenization (i.e. separate a string into elements based on specific separators, like spaces) we recommend you using the strtok() or strtok r() functions.

3.2 Evaluation and Minimum Requirements

<ul>
<li>If your program has compilation warnings, a 10% penalty is applied.</li>
<li>If your program has memory leaks (found by valgrind), a 10% penalty
is applied.
</li>
<li>If your program doesn’t comply to the required coding style, a penalty up to 10% is applied (decided by your instructor).
7
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 8">
<div class="layoutArea">
<div class="column">
Do not cheat as we run plagiarism detection tools on all provided solutions.

Notes: The provided tests are not exactly the tests we will run on your provided solution. Do not write solutions displaying expected results based on testing file names. Besides, check on your code that the required functionality is completed and correctly provided as just running some set of tests does not necessarily cover all possible cases and prove the solution if perfect. It would thus be possible that some exceptional cases to be covered only be tests that we will run.

</div>
</div>
<div class="layoutArea">
<div class="column">
8

</div>
</div>
</div>
