# Lab 5 Report
**Huaming Wu**
**A17526592**

![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/ce2a0a9f-a016-4618-af7d-e212292337ee)

![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/b950261b-a210-48d6-987c-178cb55d93d2)

![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/51fdf20d-2f88-47cb-adad-0f3c9ddd2bfc)

Comments:

**TA**

Hey! Thanks for being detailed in your question.

You might want to double check your inputs in your bash file. Notice how your num1 and num2 is strictly based off args[1] and args[2]?
This assumes that there is an initial input that dictates whether it should be added or subtracted. What happens when that input isn't there?

Secondly, it seems that there might be another error that you didn't notice. Generally, you want to use .equals() when comparing Strings instead of
==. 
(also 7-4 is not equal to 3) 

Students Attempt to Fix:

Adding a filler argument:

![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/03d5ea75-32f6-4729-b68f-6ff5e3cf8852)

Using .equals() instead

![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/8f1f0fa3-1348-425f-9a87-efe84f3ac91d)

Running the new code:

![image](https://github.com/hwu27/cse15l-lab-reports/assets/130116077/268c0eaf-b7a7-4c27-930d-49883c197028)

Problem:

The problem was a few things. I first needed to make sure that I kept the args index in mind. Since I wrote my code in a way that needed 3 arguments,
I need to make sure I was providing 3. I added a filler argument so that the code can run correctly. Secondly, I used ==, which incorrectly compared the
String to check if it was add. I fixed it using .equals(). I also did my math wrong :(.

Reflection:

I really enjoyed creating the grading scripts. I always thought it was a little crazy how autograder would be able to just check if your code was correct or not,
but now, I have a good idea of how it does it. I think my debugging skills have also improved greatly. 

