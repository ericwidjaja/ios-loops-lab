# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1
Write code that prints all the numbers from 1 to 150, **inclusive.**
```
for index in 1...150 {
    print("\(index)")
    }
```
***
## Question 2
Write code that prints all the numbers from 142 to 159, **exclusive.**
```
let theRange = 142..<159
    for i in theRange {
        print (i)
    }
```
***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**
```
for i in 15...80 where i % 2 == 0 {
    print(i)
    }
```
***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**
```
for i in 19...51 where i % 2 != 0 {
    print(i)
    }
```
***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**
```
for i in 1..<100
    where i % 5 == 0 && i % 10 != 0 {
        print(i)
    }
```
***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**
```
for i in 1...40
    where i % 10 == 7 {
        print(i)
    }
```
***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`
```
for i in 20...150
    where i % 3 == 0 {
        print(i)
    }
```
***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`
```
for i in 20...150
    where i % 6 == 0{
        print (i)
    }
```
***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`
```
for i in 20...150
    where i % 10 == 4 {
        print(i)
    }
```
***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

```for i in 20...150
    where i == 31 || i == 35 || i >= 40 && i <= 60 {
        print (i)
    }
```
***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.
```swift
var i = 5
while (i > 3) {
    i += 1
}
```
```
//Since the integer 5 is bigger than 3, and it will continue to get bigger in each loop, this particular loop is an infinite loop.
```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5
while (i > 3) {
    i += 1
```    
```
var i = 5
    while (i < 9) {
        i += 1
    }
```
***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5
while (i > 3) {
    i += 1
}
```
```
var i = 5
    while (i <= 1004) {
        i += 1
    }
```
***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5
while (i > 3) {
    i += 1
}
```
```
var i = 5
    while (i <= 1004) {
        if i % 2 == 0 {
            print (i)
        }
        i += 1
    }
```
***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10
```
//
Even though these two loops have the same results, because their first `testConditions` are true. In the `repeat...while loop` the statement is executed first before checking `testCondition`. Only then,  `testCondition` is checked. If the `testCondition` is true, the statement is executed, followed by evaluation on `testCondition`. This process will stop when the `testCondition`’s value is false.

***
## Question 16

```swift
What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.
```
//The `break` statement stops the execution of a loop or a switch statement entirely.
```
`break` example: 
for i in 1...5 {
if i == 3 {
break
}
print(i)
}
```
//The `continue` statement is used to stop executing the next statements in loop and start from the beginning of next iteration of loop.
```
`continue` example:
for i in 1...5 {
if i == 3 {
continue
}
print(i)
}
```
***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```
```
[x] 1
[x] 2
[x] 3
[ ] 4
[ ] 5
[ ] 6
[ ] 7
[x] 8
[x] 9
[x] 10
```
***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```
```
[x] 1
[x] 2
[x] 3
[ ] 4
[ ] 5
[ ] 6
[ ] 7
[ ] 8
[ ] 9
[ ] 10
```
***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}
```
```
This loop will print:
x = 1, y = 1
x = 2, y = 1
x = 3, y = 1
The loop starts with `outerloop`, it takes X=1, then takes Y=1 from the `insideloop`. It continues to print “X=1, Y=1” since the `condition` is false. The loop will go back to the beginning of the `outerloop`, it takes X=2, BUT it will not take the next value of Y  since the `condition` is true this time (Y=2). It will print X=2, Y=1, then it will continue to the beginning of the outerloop to take X=3, skipped the next Y’s value and print X=3, Y=1.
```
***
## Question 20

```Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.
```

```
for x in 0...10 {
    for y in 0...10 {
        print("(\(x),\(y))", separator: "", terminator: "  ")
        }
    print("")
    }
```
***
## Question 21

```Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.
```
```
for x in 0...10 {
    for y in 0...10 {
        if x-y >= 5 || y-x >= 5 {
            print("(\(x),\(y))", separator: "", terminator: "  ")
            }
        }
        print("")
    }
```
***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`
Output:
```swift
1
4
9
16
25
```
```
var N = 5
    for i in 1...N {
        print((i*i),terminator: "   ")
    }
```
***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`
Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

***
```
var N = 3
    for _ in 1...N {
    for _ in 1...N {
        print("*", separator: "", terminator: "")
        }
    print("")
    }
```
