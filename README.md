# PBD-Ass1-2

**Assignment1**

**Commonly Used Fuction** 

**Is Prime Number()** // Commoon code for finding that is a number prime number or not
{
  First IF statement is for checking if the number is divided by 2 it will retun false value because no even number can be prime number except 2.
  
  Second IF statement is for checking the number which are prime numbers starting from 3 taking a jump of 2 and only looking through odd numbers and it will stop at the half of the number because no number is divisible by more than its half. So, that we're also reducing the complexity of the code. The part where i'm adding two into the half of the number is because of the some minor cases at the starting of the count.
}


**Task1:**

loop=1 \\ It controls the rotating of the number, for example, in number 13 first we have to remove 3 and the add it to back of 1, so, we take the mod with 10 and then multiply with 10 and add it with 1, so, we get 31.
loop_count=0 \\ It Controls the how many time a number has to be rotated, for, example for number 3 we don't have to rotate the number , but, for number 13 we have to rotate it one time
CPM=0 \\ The count of Circular Prime Numbers

for i in range (2,4): \\ This loop for the exceptional cases of 2 to 4 where the prime number code doesn't work
    flag=0
    for j in range (2,i):
        if i % j == 0 :
            flag=1
            break
    if flag == 0:
        CPM = CPM + 1
        print(i)
for i in range (4,1000000): This loop now gives the whole answer, it will check all the numbers under One million one by one
    #if i ==95000:
        #print('Crossed')
    if i >= loop*10: // It checks the rotation of the number, for example, how many times it has to be rotated
        loop = loop * 10 // it will increase the loop variable by multiplication of 10, so we can easily manage the rotation of the number accordingly. e.g, for 13 the loop will be 10, and for 113 the loop will be 100 and so on.
        #print(i)
        #print(loop)
        loop_count = loop_count + 1 // it will increase the loop variable by addition of 1, so we can easily manage the no. of rotation of the number accordingly. e.g, for 13 the rotation would be 1, and for 113 the rotation would be 2 and so on.
        #print(loop_count)
    f = isPrime(i) // Calls the number to check if the given number is prime or not
    if f == 1: // If the number is prime the function will return the value of 1 and this IF statement will check the rotated numbers using the variables loop and loop_count
        num = i
        count = 0
        for j in range (0,loop_count): // This LOOP will rotate according to the lenght of the number, for example, for 1 the rotation is 0 and for 10 is 1
            mod=num%10 // removing the last digit of the number and saving it in the variable mod
            if mod==2 or mod==4 or mod==6 or mod==8 or mod==0 : // if the mod value is 2, 4, 6, 8 or 0 then the number will be even and it cannot be prime
                break
            #print(i)
            #print(num)
            num= int(num / 10) // removimg the last numbere from the number itself
            #print(num)
            mod=mod*loop // for adding the digit the the last of the number it will mutiply the number with the value of loop to place it in the right place
            #print(num)
            num=num+mod // adding the number of mod into the original for checking the prime number
            #print(i)
            #print(num)
            f = isPrime(num) // checking the rotated number
            if f == 1:
                count = count + 1 // if the rotated number is also prime the local count is updated by 1, to telly the local count and loop_count at the end of the loop
            else:
                break // the loop will end if one of the rotated number is not prime
        if loop_count == count : // This IF statement wil check the local count and loop_count if, both are same then it meand that the original number and rotated numbers are all prime.
            CPM = CPM + 1 // It wiil increase the counter of Circular Prime Number of by 1
            #print(i)

Task2


Task3 


Task4


Task5


Task6



Assignment 2

Task1



Task2



Task3
