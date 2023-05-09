# Lab 3

**Huaming Wu**

## Grep ##

This is the current directory:
```
chapter-1.txt   chapter-11.txt  chapter-13.1.txt  chapter-13.3.txt  chapter-13.5.txt  chapter-3.txt  chapter-6.txt  chapter-8.txt  preface.txt
chapter-10.txt  chapter-12.txt  chapter-13.2.txt  chapter-13.4.txt  chapter-2.txt     chapter-5.txt  chapter-7.txt  chapter-9.txt
```
1. **grep -i**


In this example, I am using grep to find files that start with chapter. When I add on -i as an additional command line option, it will make it so that uppercase or lowercase is ignored. I will be using ls combined with "|" to redirect the output of ls into the grep command. If you just use grep CHAPTER in the 911report directory, it will not show anything. This can be helpful to make sure that there are no typing errors where you have an accidental capital letter like l instead of I.


Example 1:

```
[cs15lsp23oy@ieng6-202]:911report:243$ ls | grep chapter

chapter-1.txt   chapter-13.1.txt  chapter-13.5.txt  chapter-6.txt  preface.txt
chapter-10.txt  chapter-13.2.txt  chapter-2.txt     chapter-7.txt
chapter-11.txt  chapter-13.3.txt  chapter-3.txt     chapter-8.txt
chapter-12.txt  chapter-13.4.txt  chapter-5.txt     chapter-9.txt

[cs15lsp23oy@ieng6-202]:911report:243$ ls | grep -i CHAPTER

chapter-1.txt   chapter-13.1.txt  chapter-13.5.txt  chapter-6.txt  preface.txt
chapter-10.txt  chapter-13.2.txt  chapter-2.txt     chapter-7.txt
chapter-11.txt  chapter-13.3.txt  chapter-3.txt     chapter-8.txt
chapter-12.txt  chapter-13.4.txt  chapter-5.txt     chapter-9.txt
```

In this instance, I am doing it to a file instead of a directory. This will into the file to check if scramble exists inside the file. This can be useful to scout out the file as well. It also highlights the word scramble, which is useful for finding certain sentenes or related topics while not having to worry about capitalization.

Example 2:

```
[cs15lsp23oy@ieng6-202]:911report:243$ cat chapter-1.txt | grep -i SCRAMBLE

Below is a portion of this grep output:
Prior to 9/11, it was understood that an order to shoot down a commercial aircraft would have to be issued by the National Command Authority (a phrase used to describe the president and secretary of defense). Exercise planners also assumed that the aircraft would originate from outside the United States, allowing time to identify the target and scramble interceptors. The threat of terrorists hijacking commercial airliners within the United States-and using them as guided missiles-was not recognized by NORAD before 9/11. Notwithstanding the identification of these emerging threats, by 9/11 there were only seven alert sites left in the United States, each with two fighter aircraft on alert. This led some NORAD commanders to worry that NORAD was not postured adequately to protect the United States.
    FAA: Hi. Boston Center TMU [Traffic Management Unit], we have a problem here. We have a hijacked aircraft headed towards New York, and we need you guys to, we need someone to scramble some F-16s or something up there, help us out.
```
   
2. **grep -c**

grep - c acts similarly to wc. It will give the number of lines that contain the input. This can be useful in checking whether or not a file has an expected number of words or number of lines. It gives a general idea of what the file may contain.

Example 1:
```
[cs15lsp23oy@ieng6-202]:911report:244$ cat chapter-1.txt | grep -c out

126

```

This command can help you find out whether or not you are looking at the right text document. If you are looking for specific keywords, it is easier to see that there are none in that file.

Example 2:
```
[cs15lsp23oy@ieng6-202]:911report:248$ cat chapter-1.txt | grep -c CSE15L  

0

```

3. **grep -n

This option is very usefulf for finding the actual line a word occurs in. This can help narrow down the search for specific topics in text files dramatically.

Example 1:

```
[cs15lsp23oy@ieng6-202]:911report:255$ cat chapter-13.1.txt | grep -n about 

39:            Much of the public commentary about the 9/11 attacks has dealt with "lost
189:                    analysis, pooling all-source intelligence, foreign and domestic, about
235:                    the field became part of the government's institutional memory about Islamist
239:                    not easily be resolved, then the disagreement about roles and missions could be
292:                so poorly defined or so ambiguously delegated that action gets lost." That comment was made more than 40 years ago, about Pearl
293:                Harbor. We hope another commission, writing in the future about another attack, does
389:                    choices about moving resources, he or she must have the power to reach across
407:                    study. Even the most basic information about how much money is actually
626:                today. Opponents of declassification argue that America's enemies could learn about
629:                methods. The U.S. government readily provides copious information about spending on
676:            Intelligence gathered about transnational terrorism should be processed, turned into
764:                Congress have the broad knowledge of intelligence activities or the know-how about
883:            The concern about the FBI is that it has long favored its criminal justice mission
1036:                receive some of the information being developed about what is happening, or may
```

While this may be less useful, you could also use this for directories. This can help you get an idea of the location of directories and files in relation to each other.

Example 2:

```
ls | grep -n 2

2:chapter-10.txt  chapter-13.2.txt  chapter-2.txt     chapter-7.txt
4:chapter-12.txt  chapter-13.4.txt  chapter-5.txt     chapter-9.txt
```

4. **grep -v**

This will show all the lines that do not contain the input. This can be useful if there is a lot of information and you want to cut down on the information you don't want to see. In this case, I would remove all lines containin FDNY if I don't want to read about them.

```
Example 1:
[cs15lsp23oy@ieng6-202]:911report:263$ cat chapter-9.txt | grep -v FDNY

Example text:
reported to have contained only a handful of descending civilians at an earlier
                point in the morning. But just before the tower collapsed, a team of NYPD ESU
                officers encountered a stream of civilians descending an unidentified stairwell in
                the 20s. These civilians may have been descending from at or above the impact
                    zone.
```
If there are files that you do not currently need, this can help you find the files you do need.

```
Example 2:
cs15lsp23oy@ieng6-202]:911report:280$ ls | grep -v preface 
chapter-10.txt  chapter-13.2.txt  chapter-2.txt     chapter-7.txt
chapter-11.txt  chapter-13.3.txt  chapter-3.txt     chapter-8.txt
chapter-12.txt  chapter-13.4.txt  chapter-5.txt     chapter-9.txt
```

All the examples from this page are from https://en.wikibooks.org/wiki/Grep
