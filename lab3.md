# Lab 3

**Huaming Wu**

## Grep ##

**Bolded is the actual command**

1. grep -i

In this example, I am using grep to find files that start with chapter. When I add on -i as an additional command line option, it will make it so that uppercase or lowercase is ignored. I will be using ls combined with | to redirect the output of ls into the grep command. If you just use grep CHAPTER in the 911report directory, it will not show anything.

Example 1:

```
[cs15lsp23oy@ieng6-202]:911report:243$ **ls | grep chapter**

chapter-1.txt   chapter-13.1.txt  chapter-13.5.txt  chapter-6.txt  preface.txt
chapter-10.txt  chapter-13.2.txt  chapter-2.txt     chapter-7.txt
chapter-11.txt  chapter-13.3.txt  chapter-3.txt     chapter-8.txt
chapter-12.txt  chapter-13.4.txt  chapter-5.txt     chapter-9.txt

[cs15lsp23oy@ieng6-202]:911report:243$ **ls | grep -i CHAPTER**

chapter-1.txt   chapter-13.1.txt  chapter-13.5.txt  chapter-6.txt  preface.txt
chapter-10.txt  chapter-13.2.txt  chapter-2.txt     chapter-7.txt
chapter-11.txt  chapter-13.3.txt  chapter-3.txt     chapter-8.txt
chapter-12.txt  chapter-13.4.txt  chapter-5.txt     chapter-9.txt
```

Example 2:
```
[cs15lsp23oy@ieng6-202]:911report:243$ cat chapter-1.txt | grep -i SCRAMBLE

Below is a portion of this grep output:
Prior to 9/11, it was understood that an order to shoot down a commercial aircraft would have to be issued by the National Command Authority (a phrase used to describe the president and secretary of defense). Exercise planners also assumed that the aircraft would originate from outside the United States, allowing time to identify the target and **scramble** interceptors. The threat of terrorists hijacking commercial airliners within the United States-and using them as guided missiles-was not recognized by NORAD before 9/11. Notwithstanding the identification of these emerging threats, by 9/11 there were only seven alert sites left in the United States, each with two fighter aircraft on alert. This led some NORAD commanders to worry that NORAD was not postured adequately to protect the United States.
    FAA: Hi. Boston Center TMU [Traffic Management Unit], we have a problem here. We have a hijacked aircraft headed towards New York, and we need you guys to, we need someone to **scramble** some F-16s or something up there, help us out.
```
   



