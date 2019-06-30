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

var myNumbers = 1...150

for i in myNumbers {
print(i)
}

***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

var myNumbers = 142...158

for i in myNumbers {
print(i)
}

var myNumbers = 142...159

for i in myNumbers where i >= 142 && i < 159 {
print(i)
}


***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

var myNumbers = 15...80

for i in myNumbers where i % 2 == 0 {
print(i)
}

***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

var myNumbers = 19...51

for i in myNumbers where i % 2 == 1 {
print(i)
}


***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

var myNumbers = 1...20

for i in myNumbers where i % 2 == 1 {
print(i * 5)
}

***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

var myNumbers = 1...40

for i in myNumbers where i % 10 == 7 {
print(i)
}


***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

var givenRange = 20...150

for i in givenRange where i % 3 == 0 {
print(i)
}

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

var myNumbers = 20...150

for i in myNumbers where i % 2 == 0 && i % 3 == 0 {
print(i)
}


***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`


var myNumbers = 20...150

for i in myNumbers where i % 10 == 4{
print(i)
}


***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

var myNumbers = 20...150

for i in myNumbers {
if i == 31 {
print(i)
}
if i == 35 {
print(i)
}
if i >= 40 && i <= 60 {
print(i)
}
}

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Your explanation here

Infinite. The code says to repeat as long as i is larger than 3. i starts at 5, which is larger than 3, and grows by one each time.
```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
var i = 5

while (i <= 8) {
i += 1
print(i)
}


***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```

var i = 5

while (i > 3 && i < 1005) {
i += 1
}

OR

var i = 5

while (i > 3 && i < 1005) {
i += 1
print(i)
}

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
    i += 1
}
```
var i = 5

while (i > 3 && i < 1005) {
i += 1
if i % 2 == 0 {
print(i)
}
}


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

The outputs are the same. 

The first one prints i each time, adding one, until it is equal to 10. It also prints i when equal to 10. As long as (while) the stated is valid (true), it loops.

The second one exectures the body funtion before checking the condition. It then checks the condition

***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

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

[]1 X
[]2 X
[]3 X
[]4 
[]5
[]6
[]7
[]8 X
[]9 X
[]10 X

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

[]1 X
[]2 X
[]3 X
[]4
[]5
[]6
[]7
[]8
[]9
[]10

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

x = 1, y = 1
x = 2, y = 1
x = 3, y = 1

It runs through the looped iteration for each X while Y=1, printing each time. Then it starts the next round of X, for which Y=2, meaning it continues back to the top of the iteration without printing, with only the outerloop, which does not satisfy the print condition.. 

```

***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

for i in 0...10 {
for j in 0...10 {
print("\(i),\(j)", separator: "", terminator: " ")
}
print("")
}



***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

for i in 0...10 {
for j in 0...10 where i - j >= 5 {
print("\(i),\(j)", separator: "", terminator: " ")
}
print("")
}

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

var n = 1...5

for i in n {
print((i * i))
}

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
