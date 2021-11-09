## Flow of Program

In this article we'll learn about control flows, flowcharts and pseudocode of a program.

## Flowcharts
Flowcharts is just a visual represemtation of the logic we think or an algorithm we create to solve a particular problem.
As every language we speak has some sort of grammer and rules to follow, think of flowcharts as a pictorial language where certain symbols carry specific meanings.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jmqzpihfy44irmoyj6hw.png)

- start/end: indicates Start or End of the program
- arrows: Used to relate various representative shapes. Used to show flow direction of the program 
- input/output: Input that we take from user and output that we provide to our user
- process: Anything and everything (operations) that we do on imput data to produce output data
- decision: We use this shape to decide between one or more options to proceed further. For example, we might want to change flow of our code based upon the fact whether a student got more or less than 60 marks in exam

Let us understand these things using some simple examples...
1.Take a name from user and print 'Hello name'

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/74segth713uitnmb7chj.png)

2.Take salary input form user. Add a bonus of Rs.2000 if the salary is greater than Rs.10000 else add a bonus of Rs.1000

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fzgo92vnjlfzr00p723j.png)

In the above flowchart, we used diamond shape to write an if statement (if salary>1000)

3.Input a number and print whether its prime or not

We know that _prime numbers_ numbers are the numbers which are only divisible by 1 & the number itself. So the 1st thought to approach this problem could be,

Check for all the numbers between 1 & the target number, if any number divides the target number. If any of them can completely divide the target number then the target number is not prime otherwise its a prime number.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3jtx8sud7uxkkfiaprhe.png)

In the above flowchart, there is a `%` operator which some of you might not be familiar with. `%` operator basically shows reminder when number at LHS (left hand side) is divided by number at RHS (right hand side)
```
4 % 2 =0   # because 4 is completely dividible by 2
5 % 2 =1   # because 2x2 is 4 and 1 is the reminder of division
```
Another thing which one can observe is that we have created a loop to check all the numbers between 1 & the target number. Its also evident from the flowchart cause we have a cyclic figure between the conditions, signifying a loop. We will learn about loops in depth in out further articles, for now I just want you to get a basic gist of it!

## Pseudocode
Sometimes we want to share our logic or algorithm with someone and we really do not care about the rules of programming language that the person want to use. We just need to share our logic irrespective of the syntactical specifications. At such times we can use pseudocode. Pseudocode in simple terms can be stated as a rough code for our logic.

Lets try and understand this with our previous example.
```
START
input num
count = 2
while count <= num:
    if (num % count)=0:
        output "NOT Prime"
    count = count + 1
end while
output "Prime"
END
```
As we can see we use if conditions and loops as conditionsals. We also used them in the flowchart. One can say that flowchart and pseudocodes are just different ways of representing a logic or an algorithm without caring about syntax (A rough idea of the code.)

Now lets try and optimize above logic. Lets take example of number 28
```
# Factors of 28
1x28 = 28
2x14 = 28
4x7 = 28
7x4 = 28
14x2 = 28
28x1 = 28
```
This is what we were doing in the prime number example, we were looking for all the factors of a number and if any number has more than 2 (1 & the target number) factors then the number is not prime.

In the above cell we can see that there is repetetion when we check for those factors. Once we have checked `2x14=28` there is no need to check `14x2=28` agian. We are repeating ourselves. This unnecessarily increases time & memory required to process our code.  So check only for
```
# Factors of 28
1x28 = 28
2x14 = 28
4x7 = 28
```

Similarly for `36` we check only till `6` for `49` we check only till `7` and so on. If we observe carefully we can easily find the pattern. For every target number, we only have to check till its square root
```
sqrt(28)=5.29
sqrt(36)=6
sqrt(49)=7
```
These minute changes might feel insignificant when we are dealing with smaller numbers like `28`, `36`, and `49` but tehy make huge difference when the target number is in millions or billions.

for example, if we want to check prime status of a number `876187398013` it will require 876187398013 iterations by our initial logic but only sqrt(876187398013) = __936048__ iterations by our optimized logic.

So our optimized pseudocode and the flowchart for the program is
```
START
input num
count = 2
while count <= sqrt(num):
    if (num % count)=0:
        output "NOT Prime"
    count = count + 1
end while
output "Prime"
END
```
flowchart
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ewjwxwyzim0fwph9fxqr.png)

Hope ya'll have got an idea of how the flow direction of program works and how we can tray and test our logic without actually writing the code using flowcharts and pseudocodes.

#### Reference
%[https://www.youtube.com/watch?vlhELGQAV4gg]