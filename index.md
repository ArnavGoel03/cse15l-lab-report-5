# Interesting commands to pair up with 'grep'



### -r: 
- This option tells grep to search recursively through all subdirectories, rather than just the current directory. Using the -r option can also make the search process more efficient, as it eliminates the need to run multiple grep commands and manually specify the directories to search. This can save time and effort, especially when searching large directory structures.


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




### -l: 
- The '-l' option is used with the grep command to list only the names of files that contain a match for the specified pattern, rather than displaying the matching lines themselves. This can be useful when searching through multiple files and you only want to see which files contain the pattern, without having to sift through all of the matching lines within each file.

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




### -i: 
- This option makes the grep search case-insensitive, so that uppercase and lowercase letters are treated as the same.By using the -I option, we can tell grep to ignore binary files and only search text files. This can be useful in cases where you only want to search for information in plain text files and don't want to see the results of searching binary files.


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





### -n: 
- The '-n' option is used with the grep command to display the line numbers of the matching lines in the output. When this option is used, grep prefixes each matching line with its line number in the file, making it easier to locate the specific line(s) of interest. This option can be especially useful when searching through large files, where it can be difficult to manually find the matching line without the line number information.


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


- I used ChatGPT for aiding me in the completion of this project. I prompted it with four commands specifically-  One for asking about 4 commands that could be paired up with the grep function and the rest of them for the usefullness of those functions. The same can be recreated by following these steps 



1). [Click here](https://openai.com/blog/chatgpt/) to head to the chat Gpt website and then clcik on the try GPT option followed by a signup to create an account. 

The website upon clicking at first would look something like this ~

![A picture of the base page of Chat GPT](chatgpt.png)



2). Upon succesfull login inot your account the webpage would look something like this. Click on the new Chat button to proceed.

![A picture of the base page of Chat GPT](chatgpt2.png)



3).Enter the derised prompt( Instructions) for the Chat gpt to generate text and then hit enter or the arror button on the right of the text box.

![A picture of the base page of Chat GPT](chatgpt3.png)



4). A sample input and output has been attached underneath. 

![A picture of the base page of Chat GPT](chatgpt4.png)



***
***



