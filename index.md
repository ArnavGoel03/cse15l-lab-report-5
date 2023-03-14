# Interesting commands to pair up with 'find'



### -name: 
- The -name option in the find command is used to search for files by their name. It can be used to search for specific files, files with a certain extension, or files that match a certain pattern. This makes it a powerful tool for locating files on a Unix or Linux system.


#### Examples -


##### Example 1 - Prompt with output 
```
Input - 

grep 'Hello' -r written_2

Output -

written_2/non-fiction/OUP/Berk/CH4.txt:Children’s earliest efforts at make-believe also reveal how challenging they ﬁnd the task of detaching thought from reality. Initially, object substitutions are closely tied to the real things they represent. Toddlers between ages 1 1/2 and 2 generally use only realistic-looking objects while pretending—a toy telephone to talk into or a cup to drink from.9 Once, I handed a 21-month-old a small wooden block, put another to my ear, and called her on the phone: “Ring! Ring! Hello, Lynnay!” She responded by throwing down the block and turning to another activity. Yet when given a plastic replica of a push-button phone, Lynnay readily put the receiver to her ear and pretended to converse.
written_2/non-fiction/OUP/Berk/CH4.txt:As children engage in play talk, they not only build their vocabularies but correct one another’s errors, either directly or by demonstrating the acceptable way to speak. In one instance, a kindergartner enacting a telephone conversation said, “Hello, come to my house, please.” Her play partner quickly countered with appropriate telephone greeting behavior: “No, ﬁrst you’ve got to say ‘How are you? What are you doing?’”28
written_2/travel_guides/berlitz1/WhereToFrance.txt:        Saint-Wandrille, Le Bec-Hellouin, and Caen, culminating in their

```
This basically fetches all the lines while looking for all the files in the directory recursively. It printed out the file names along with specific lines that had them.


##### Example 2 - Prompt with output 
```
Input -

grep 'bye' -r written_2

Output -

written_2/non-fiction/OUP/Castro/chN.txt:Good-bye my Lady

```
This is essentially the same thing as the last set of commands just with the difference of the string being searched for.




### -type: 
- The -type option in the find command is used to search for files based on their type. This option takes a single character argument and matches it against the type of each file in the directory tree being searched. The matched files are then returned as the output of the find command. It can be used to find all directories, all regular files, or all symbolic links, for example.


#### Examples -


##### Example 1 - Prompt with output 
```
Input -

grep 'Hello' -rl written_2

Output -

written_2/non-fiction/OUP/Berk/CH4.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt

```

This examples builds up on what we learnt about -r in the last section for ease in exploring all the files. It also inclused the '-l' which just prints the file name whilst leaving out the line content which has this string.


##### Example 2 - Prompt with output 
```
Input - 

grep 'bye' -rl written_2

Output -

written_2/non-fiction/OUP/Castro/chN.txt

```

Similar to the last case we came across just with a different string 'bye' .




### -mtime: 
- The -mtime option in the find command is used to search for files based on their modification time. It can be used to find all files modified within a certain timeframe, such as within the last day or week. This option takes a numeric argument that specifies the number of 24-hour periods (or days) ago the file was last modified. The matched files are then returned as the output of the 'find' command.


#### Examples -

##### Example 1 - Prompt with output 
```
Input - 

grep 'Hello' -rli written_2

Output -

written_2/non-fiction/OUP/Berk/CH4.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
written_2/travel_guides/berlitz1/WhereToHongKong.txt

```
It's the same command used in the first examples of the two alterations we explored above but with another modification '-i'. This makes the search case insentive and helps us focus on the word rather than the specifc formatting of it and we end up matching with more of the files/


##### Example 2 - Prompt with output 
```
Input - 

grep 'bye' -rli written_2

Output -

written_2/non-fiction/OUP/Castro/chN.txt

```

The same case as previous but implemented using a different string/





### -size: 
- The -size option is useful in situations where you want to search for files based on their size. It can be used to find files that are taking up a lot of disk space, or files that are smaller than a certain size. This option takes a numeric argument and matches it against the size of each file in the directory tree being searched. 

#### Examples -

##### Example 1 - Prompt with output 
```
Input -

grep 'bye' -rin written_2

Output -

written_2/non-fiction/OUP/Castro/chN.txt:32:Good-bye my Lady

```

This commands adds the speific line number on which the word is found on top of the text from the line. The same can be seen in this example as the line number 32 is printed in the output.


##### Example 2 - Prompt with output 
```
Input - 

grep 'Hello' -rlin written_2

Output - 

written_2/non-fiction/OUP/Berk/CH4.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
written_2/travel_guides/berlitz1/WhereToHongKong.txt

```

Note - This command can't be paired up with '-l' as '-l' excludes the line altogther making the concept of outputting line numbers and thus using '-n' redundant & useless. This can be clearly concluded from the example above.





***

## Softwares used - Chat GPT


- I used ChatGPT for aiding me in the completion of this project. I prompted it with four commands specifically-  One for asking about 4 commands that could be paired up with the 'find' function and the rest of them for the usefullness of those functions. The same can be recreated by following these given steps ~



1). [Click here](https://openai.com/blog/chatgpt/) to head to the chat Gpt website and then clcik on the try GPT option followed by a signup to create an account. 

The website upon clicking at first would look something like this ~

![A picture of the base page of Chat GPT](chatgpt.png)



2). Upon succesfull login inot your account the webpage would look something like this. Click on the new Chat button to proceed.

![A picture of the base page of Chat GPT](report5ss2.png)



3).Enter the derised prompt (Instructions) for the Chat gpt to generate text and then hit enter or the arror button on the right of the text box.

![A picture of the base page of Chat GPT](report5ss3.png)



4). A sample input and output has been attached underneath. 

![A picture of the base page of Chat GPT](report5ss4.png)



***
***



