# Lab 3

**Huaming Wu**

## Grep ##

1. grep -i

In this example, I am using grep to find files that start with chapter. When I add on -i as an additional command line option, it will make it so that uppercase or lowercase is ignored. I will be using ls combined with | to redirect the output of ls into the grep command. If you just use grep CHAPTER in the 911report directory, it will not show anything.
```
ls | grep chapter

chapter-1.txt   chapter-13.1.txt  chapter-13.5.txt  chapter-6.txt  preface.txt
chapter-10.txt  chapter-13.2.txt  chapter-2.txt     chapter-7.txt
chapter-11.txt  chapter-13.3.txt  chapter-3.txt     chapter-8.txt
chapter-12.txt  chapter-13.4.txt  chapter-5.txt     chapter-9.txt

ls | grep -i CHAPTER

chapter-1.txt   chapter-13.1.txt  chapter-13.5.txt  chapter-6.txt  preface.txt
chapter-10.txt  chapter-13.2.txt  chapter-2.txt     chapter-7.txt
chapter-11.txt  chapter-13.3.txt  chapter-3.txt     chapter-8.txt
chapter-12.txt  chapter-13.4.txt  chapter-5.txt     chapter-9.txt
```
