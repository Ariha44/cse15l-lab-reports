# Lap Report 3

# Researching Commands

## Choosing a command to experiment with using command-line options

| Commands | Description | 
| -------- | ------- |
| `less` | displays text files one page at a time |
| `find` | searches and locates files and directories using specified conditions |
| `grep` | searches and matches text files using specified string(s) | 

 * For this lab report, I chose the `grep` command to experiment

## Using command-line option `-n`
The first command-line option I used was `-n`, which displays the lines and their respective line numbers. Source used: [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
 * **Example 1 Input:**
```
grep -n "welcome" technical/biomed/*.txt
``` 
 * **Example 1 Output:**
```
technical/biomed/1471-2458-2-25.txt:167:          moderator, and note taker welcomed and oriented the
technical/biomed/1471-2458-2-25.txt:172:          opinions were welcomed, no answer was right or wrong and
technical/biomed/1472-684X-1-5.txt:125:          life, studies suggest that patients welcome inquiry about
technical/biomed/1472-6947-3-8.txt:624:        biomedical data sets. Public comment is welcomed.
technical/biomed/gb-2001-2-11-research0046.txt:737:          these strains would provide welcome models for exploring
technical/biomed/gb-2002-3-9-research0051.txt:12:        process, an impetus that is particularly welcome because
```
 * As we can see, the terminal shows the matched lines and their line numbers using the string "welcome" in the biomed directory. The line numbers are displayed after the file's path starting with a colon `:`.
 * **Example 2 Output:**
```
grep -n "welcome" technical/government/*/*.txt
```
 * **Example 2 Output:**
```
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:54:welcome to walk through them unimpeded and unchallenged.
technical/government/Env_Prot_Agen/multi102902.txt:2619:last few years has been a welcome change to boilermakers.
technical/government/Gen_Account_Office/d0269g.txt:1396:inquiries. This "welcome" package is hand delivered during a site
technical/government/Gen_Account_Office/gg96118.txt:1392:for the results of their programs. Managers generally welcomed
technical/government/Gen_Account_Office/Testimony_cg00010t.txt:22:the General Accounting Office (GAO). We welcome this opportunity to
technical/government/Media/Legal_Aid_attorney.txt:50:welcomed their first child into their lives last week, Sophia Clare
technical/government/Media/Lockyer_Warns.txt:31:Elena Popp, executive director of the foundation, welcomed the
```
 * In this example, I looked into the government directory for text files that had "welcome" in it and found the line numbers. Command option `e` can be useful in searching for the lines that have specific keyword by using the given location.


## Using command-line option `-A num`
The second command-line option I used was `-A num`, which prints the searched line and the lines after. Source used: [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
 * **Example 3 Input:**
```
grep -A 737 "welcome" technical/biomed/gb-2001-2-11-research0046.txt
``` 
 * **Example 3 Output:**
```
          these strains would provide welcome models for exploring
          genetic background effects that plague much of the
          current work on transgenic and knockout mice [ 37].
          Second, by genotyping and selectively breeding the most
          highly recombinant animals it should be possible to
          generate RI strain sets with map expansions that
          significantly exceed that predicted by the
          Haldane-Waddington equation, an equation that assumes
          random mating of sibs. A six- to eight-fold expansion
          should be attainable, particularly if recombinations are
          tracked before and during the inbreeding process (Figure\
          
          ...
          
        A 284 Microsoft Excel file that can be used to compare
        the overall genetic similarity of any two strains that are
        members of the BXN set. This file is an extended version of
        Table 6.
        Click here for additional data file
```
 * The output successfully shows the only mention of "welcome" in the gb-2001-2-11-research0046.txt file (determined by the output of Example 1) and the lines after.
 * **Example 4 Input:**
```
grep -A 3500 "A 284 Microsoft Excel file" technical/biomed/gb-2001-2-11-research0046.txt    
```
 * **Example 4 Output:**
```
        A 284 Microsoft Excel file that can be used to compare
        the overall genetic similarity of any two strains that are
        members of the BXN set. This file is an extended version of
        Table 6.
        Click here for additional data file
```
 * As we can see, we were able to output the last paragraph in the gb-2001-2-11-research0046.txt file with the matched string "A 284 Microsoft Excel file". This command-line option is useful in finding a string and the results after the match.

## Using command-line option `-c`
The third command-line option I used was `-c`, which prints the count of number of matches. Source used: [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
 * **Example 5 Input:**
```
grep -c "welcome" technical/biomed/gb-2001-2-11-research0046.txt

``` 
 * **Example 5 Output:**
```
1
```
 * As we know from Example 1's output, the gb-2001-2-11-research0046.txt file only has one line with "welcome in it". Command-line option `-c` confirms the count of lines with "welcome" in it with the number 1.
 * **Example 6 Input:**
```
grep -c "welcome" technical/government/*/*.txt
```
 * **Example 6 Output:**
```
technical/government/About_LSC/Comments_on_semiannual.txt:0
technical/government/About_LSC/commission_report.txt:0
technical/government/About_LSC/conference_highlights.txt:0
technical/government/About_LSC/CONFIG_STANDARDS.txt:0
...
technical/government/Post_Rate_Comm/Mitchell_spyros-first-class.txt:0
technical/government/Post_Rate_Comm/Redacted_Study.txt:0
technical/government/Post_Rate_Comm/ReportToCongress2002WEB.txt:0
technical/government/Post_Rate_Comm/WolakSpeech_usps.txt:0 
```
 * The output shows all the counts of "welcome" in all the text files in the government directory. Using `-c` is great for knowing how common a word is in specified files.

## Using command-line option `-v`
The last command-line option I used was `-v`, which outputs the lines that do not match the given pattern. Source used: [https://www.geeksforgeeks.org/grep-command-in-unixlinux/](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
 * **Example 7 Input:**
```
grep -v "[aeiouAEIOU]" technical/biomed/gb-2001-2-11-research0046.txt      
``` 
 * **Example 7 Output:**
```
C
            c /(1 + 6
            B :
          1,536 SDPs.
          4).
          PCR
        7.
```
 * I used the command-line `-v` to display all the lines in gb-2001-2-11-research0046.txt file that do not have any vowels in it. We can see that only seven lines with characters are given as output from the whole file. The gb-2001-2-11-research0046.txt has 1101 lines in total: 
```
wc -l technical/biomed/gb-2001-2-11-research0046.txt
``` 
```
1101 technical/biomed/gb-2001-2-11-research0046.txt
```
 * **Example 8 Input:**
```
grep -vc "[aeiouAEIOU]" technical/biomed/gb-2001-2-11-research0046.txt
```
 * **Example 8 Output:**
```
75
```
 * We used `-c` with `-v` to count how many lines do not have any vowels in the gb-2001-2-11-research0046.txt. Example 7's output shows 7 lines with characters, but I believe the rest of the 68 lines are blank lines that were counted as lines with no vowels. `-v` is a powerful tool in filtering out certain lines in given files or directories.
  
