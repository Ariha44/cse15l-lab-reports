# Lap Report 2

## Researching Commands

# Choosing a command to experiment with by using command-line options

| Commands | Description | 
| -------- | ------- |
| `less` | displays text files one page at a time |
| `find` | searches and locates files and directories using specified conditions |
| `grep` | searchs and matches text files using specified string(s) | 

 * For this lab report, I chose the `grep` command to experiment

# Using command-line options
 * The first command-line option I used was `n`, which displays the lines and their respective line numbers
 * **Example 1 Input:**
```
grep -e "welcome" -e "welcome"  technical/biomed/*.txt
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
 * Example 2 Input:
```
grep -n "welcome" technical/government/*/*.txt
```
 * Example 2 Output:
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





  
  
3. Trying Some Commands
 * Experiment with commands such as `cd`, `ls`, `pwd`, `mkdir`, and `cp`

| Commands | Description | 
| -------- | ------- |
| `cd` | changes directories |
| `ls` | lists files on the current or specified directory|
| `pwd` | prints the working directory | 
| `mkdir` | creates directories or subdirectories | 
| `cp` | copies files or directories |

 * Exit out of the remove server using the command `exit` or the keys Ctrl-D
 ![Commands](commands.png)
 * As shown by the image above, I used commands `pwd`, `ls -lat`, and `exit`. 
 * Note: `ls -lat` lists all visible and hidden files and directories in the working directory with information such as the date the contents were modified and the size of each of them.

