# Arrays lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

Create an array of strings called `colors` that contain "orange", "red", "yellow", "turquoise", and "lavender".

Then, using array subscripting and string interpolation, print out the String `"orange, yellow, and lavender are some of my favorite colors"`.
```
var colors = ["orange", "red", "yellow", "turquoise", "Lavender"]

print("\(colors[0]) , \(colors[2]) and \(colors[4]) are some of my favorite colors")
```

## Question 2

Remove "Illinois" and "Kansas" from the array below.

`var westernStates = ["California", "Oregon", "Washington", "Idaho", "Illinois", "Kansas"]`
```
var westernStates = ["California", "Oregon", "Washington", "Idaho", "Illinois", "Kansas"]
westernStates.remove(at:5)
westernStates.remove(at:4)
print(westernStates)
```

## Question 3

Iterate through the array below. For each state, print out the name of the state, a colon, and whether it is or is not **in the continental United States.**

`let moreStates = ["Hawaii", "New Mexico", "Alaska", "Montana", "Texas", "New York", "Florida"]`
```
var moreStates = ["Hawaii", "New Mexico", "Alaska", "Montana", "Texas", "New York", "Florida"]
var outside = "Hawaii"
var emptyArr = [""]
var currentIndex = 0
var anotherIndex = 0

for i in moreStates{
if i == outside{
//    print(i)
break
}
currentIndex += 1
}
for i in moreStates{
if i != outside{
moreStates[anotherIndex].append(": it is in the continental United States")
}
else{
moreStates[currentIndex].append(": it is not in continental USA")
}
anotherIndex += 1
}
print(moreStates)
```

## Question 4

Print out how many non-whitespace characters are in `myString`:

`let myString = "This is good practice with Strings!"`

```
var spaceCounter = 0
var emptySpace = " "

let myString = "This is good practice with Strings!"
for char in myString{
if String(char) != emptySpace{
spaceCounter += 1
}
}
print("There are this many non-whitespace characters \(spaceCounter)")
```

Iterate through the array below. For each sentence, print out how many non-whitespace characters are in it.

`let myFavoriteQuotes = ["To be or not to be, that is the question.", "The only source of knowledge is experience.", "Mr. Gorbachev, tear down this wall!", "Four score and twenty years ago..."]`

```
for char in myFavoriteQuotes{
for i in myFavoriteQuotes[indexCounter]{
if String(i) != emptySpace{
//spaceCounter += 1
}
//print(i, terminator: "")
spaceCounter += 1
}
indexCounter += 1
}
print("There are this many non-whitespace characters \(spaceCounter)")
```

## Question 5

Iterate through `garden` and place any 🌷 that you find into the `basket`. Replace any 🌷 that you pick up with `"dirt"`. Then print how many 🌷 are in your `basket`.

```swift
var garden = ["dirt","🌷","dirt","🌷","dirt","dirt","🌷","dirt","🌷","dirt"]
var basket = [String]()
```
```
var flower = "🌷"
var dirty = "dirt"
var counter = 0
var newGarden = ""

var garden = ["dirt","🌷","dirt","🌷","dirt","dirt","🌷","dirt","🌷","dirt"]
var basket = [String]()

for plant in garden{
if plant == flower{
basket.append(flower)
}
}
for _ in garden{
newGarden.append(garden[counter].replacingOccurrences(of: "🌷", with: " dirt "))
counter += 1
}
print("\(basket) there are \(basket.count) flowers")
print(newGarden.components(separatedBy: " "))
```

## Question 6

The below array represents an unfinished batting lineup for a baseball team. **You, the coach,** need to make some last minute changes:

- Add "Suzuki" to the end of your lineup.
- Change "Jeter" to "Tejada".
- Change "Thomas" for "Guerrero"
- Put "Reyes" to bat 8th instead.

`var battingLineup = ["Reyes", "Jeter", "Ramirez", "Pujols","Griffey","Thomas","Jones", "Rodriguez"]`
```
var battingLineup = ["Reyes", "Jeter", "Ramirez", "Pujols","Griffey","Thomas","Jones", "Rodriguez"]

var arrCount = 0

battingLineup.append("Suzuki")
for i in battingLineup{
if i == "Jeter"{
battingLineup[arrCount] = "Tejada"
}
else if i == "Thomas" {
battingLineup[arrCount] = "Guerrero"
}
else if i == "Reyes"{
battingLineup.swapAt(7, arrCount)
}
arrCount += 1
}
print("\(battingLineup) This is the batting lineup")
```

## Question 7

Given an array of Ints, find out if it contains a target number.  

(The built-in `contains(_:)` function will do this, but you aren't allowed to use it for this exercise.)


```swift
var numbers: [Int]

let target: Int = 32
```

Ex.1

```swift
numbers = [4,2,6,73,32,4,2,1]

target = 32

//true
```

Ex. 2

```swift
numbers = [32459,2,4,5,1,4,2,1]

target = 3

//false
```

```
var numbers = [4,2,6,73,32,4,2,1]
let target: Int = 32
var count = 0

for i in numbers{
if i == target{
count += 1
}
}
if count > 0{
print("True it contains the target number")
}
else{
print("False it does not contain the target number")
}
```


## Question 8

Find the largest value in an array of Int.  Do not use the built-in `max()` method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.
```
```
var arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

var index = 0
var max = 0

for i in arrayOfNumbers{
//print(i, terminator: " ")
if arrayOfNumbers[index] > max{
max = arrayOfNumbers[index]
}
index += 1
}
print("This is the biggest number: \(max)")
```


## Question 9

Find the smallest value in an array of Int.  Do not use the built in min() method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.
```

```
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

var index = 0
var min = 201

for i in arrayOfNumbers{
print(i, terminator: " ")
if arrayOfNumbers[index] < min{
min = arrayOfNumbers[index]
}
index += 1
}
print("This is the smallest number: \(min)")
```


## Question 10

Iterate through `secondListOfNumbers`, and print out all the odd numbers.

`var secondListOfNumbers = [19,13,14,19,101,10000,141,404]`
```
var secondListOfNumbers = [19,13,14,19,101,10000,141,404]

for i in secondListOfNumbers{
if i % 2 != 0 {
print(i)
}
}
```

## Question 11

Iterate through `thirdListOfNumbers`, and print out the sum.

`var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]`

```
var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]
var sum = thirdListOfNumbers.reduce(0, +)

print(sum)
```

## Question 12

Iterate through `thirdListOfNumbers`, and print out the sum of all the even numbers.

`var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]`
```
var thirdListOfNumbers = [2,4,3,6,7]
var sum = 0
for i in thirdListOfNumbers{
if i % 2 == 0 {
sum += i
}
}
print(sum)
```

## Question 13

Append every Int that appears in both `listOne` and `listTwo` to the `sharedElements` array. Then print **how many Ints** are shared.

```swift
var listOne = [28, 64, 7, 96, 13, 32, 94, 11, 80, 68]
var listTwo = [18, 94, 48, 6, 42, 68, 79, 76, 13, 7]
var sharedElements = [Int]()
```


## Question 14

Write code such that `noDupeList` has all the same Ints as `dupeFriendlyList`, but has no more than one of each Int.

```swift
var dupeFriendlyList = [4,2,6,2,2,6,4,9,2,1]
var noDupeList: [Int] = []
```
```
var dupeFriendlyList = [4,2,6,2,2,6,4,9,2,1]
var noDupeList: [Int] = []

for i in dupeFriendlyList{
if !noDupeList.contains(i){
noDupeList.append(i)
}
}
print(noDupeList)
```

## Question 15

Find the second smallest number in an Array of Ints

`let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}`

```
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

var sort = arrayOfNumbers.sorted()
print(sort)
print("This is the second smallest number\(sort[1])")
```

## Question 16

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below 1000.
```
var sum = 0
for i in 1..<1000{
if i % 3 == 0 || i % 5 == 0{
//print(i)
sum += i
}
}
print("Sum of all numbers below 1000: \(sum)")
```

## Question 17

Make an array that contains all elements that appear **more than twice** in `someRepeatsAgain`.

```swift
var someRepeatsAgain = [25,11,30,31,50,28,4,37,13,20,24,38,28,14,44,33,7,43,39,35,36,42,1,40,7,14,23,46,21,39,11,42,12,38,41,48,20,23,29,24,50,41,38,23,11,30,50,13,13,16,10,8,3,43,10,20,28,39,24,36,21,13,40,25,37,39,31,4,46,20,38,2,7,11,11,41,45,9,49,31,38,23,41,16,49,29,14,6,6,11,5,39,13,17,43,1,1,15,25]
```
```
var someRepeatsAgain = [1,2,1,3,4,5,2,2]
var repeated = ""

for i in someRepeatsAgain{
var test = someRepeatsAgain.filter{ $0 == i}
if test.count >= 2{
repeated.append("\(test)")
}
}
print(repeated)
```

## Question 18

Identify if there are 3 integers that sum to 10 in the following array. If so, print them as a triplet. If there are multiple triplets, print all possible triplets.

`var tripleSumArr = [-20,-14, -8,-5,-3,-2,1,2,3,4,9,15,20,30]`

```
var tripleSumArr = [-20,-14, -8,-5,-3,-2,1,2,3,4,9,15,20,30]

for i in tripleSumArr{
for j in tripleSumArr{
for k in tripleSumArr{
if i + j + k == 10{
print("\(i) \(j) \(k)")
}
}
}
}
```

## Question 19

Given an array of Strings, find the the String with the most "a"s in it.

input: `["apes", "abba", "apple"]`

output: `"abba"`
```
var input = ["apes", "abba", "apple"]
let a = input[0].components(separatedBy: "a")
let b = input[1].components(separatedBy: "a")
let c = input[2].components(separatedBy: "a")
if a.count > b.count && a.count > c.count{
print("Most a in \(input[0])")
}
else if b.count > c.count && b.count > a.count{
print("Most a in \(input[1])")
}
else{
print("Most a in \(input[2])")
}
```

## Question 20

Given an Array of Arrays of Ints, find the Array of Ints with the largest sum:

Input: `[[2,4,1],[3,0],[9,3]]`

Output: `[9,3]`
```
var input = [[2,4,1],[3,0],[9,3]]
let a = input[0].reduce(0 , +)
let b = input[1].reduce(0 , +)
let c = input[2].reduce(0 , +)
if a > b && a > c{
print("Biggest sum \(input[0])")
}
else if b > c && b > a{
print("Biggest sum \(input[1])")
}
else{
print("Biggest sum \(input[2])")
}
```


## Question 21

Given an Array of Tuples of type `(Int, Int)`, create an array containing all the tuples where the first Int is equal to the second Int.

Input: `[(4,2), (-3,-3), (1,1), (3,9)]`

Output: `[(-3,-3), (1,1)]`

```
var Input = [(4,2), (-3,-3), (1,1), (3,9)]
var empArr: [Int] = []
//print(Input[0].1)
var index = 0

for i in Input{
if Input[index].0 == Input[index].1{
empArr.append(Input[index].0)
empArr.append(Input[index].1)
}
index += 1
}
print(empArr)
```

## Question 22

Given an Array of Bools, make a variable called `allAreTrue` that is true if all of the Bools are true and false if any of them are false.

Input: `[true, false, true, true]`

Output: `false`
```
var Input = [true, false, true, true]
var allAreTrue = 0

for i in Input{
if i == true{
allAreTrue += 1
}
}
if allAreTrue == Input.count{
print("All inputs are true")
}
else{
print("not all inputs are true")
}
```


## Question 23

Given an Array of Ranges of Ints, create an array that has all the values from all the ranges in order from smallest to greatest with no duplicates.

Input: `[0..<3 , 2..<10, -4..<6, 13..<14]`

Output: `[-4,-3,-2,-1,0,1,2,3,4,5,6,7,8,9,10,13]`


## Question 24

Given an array of Characters, create a String ignoring uppercase Characters and spaces.  Then uppercase every other character of the String.

Input: `let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C,"e"]`

Output: `"ApLeAuE"`
```
let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C","e"]
var newArr = ""
var index = 0
var newString = ""

for i in arr{
if i.isLowercase{
newArr.append(i)
}
}
for i in newArr{
var test = Array(newArr)
print(test[index].uppercased())
index += 2
}
```



## Question 25

Print out each element in `myMatrix`

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`
```
var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]
var index = 0

for i in myMatrix{
for j in myMatrix[index]{
print(j, terminator: " ")
}
index += 1
}
```

## Question 26

Print out the sum of the diagonals of `myMatrix`.

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`

```
var myMatrix = [[10, 14, 12],
[91, 1, 9],
[31, 3, 21]]
var sum = 0
var index = 0

for i in myMatrix{
sum = sum + myMatrix[index][index]
index += 1
}
print(sum)
```


## Question 27

Using for loops, rotate `matrixToRotate` 90 degrees.

var matrixToRotate = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

![Matrix Rotation](images/rotated_matrix.jpeg)
