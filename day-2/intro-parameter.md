## Functions with Parameters

### Students Will Be Able To
- Define a function with a return value and one parameter
- Explain the difference between a parameter and an argument

### Why
We've used lots of built-in Swift methods, and most of them were were more flexible than the functions we've been writing so far today. For instance, when we used the contains() method for arrays we were able to pass a value into the function. We can pass anything into a function that we create. Otherwise, we would have very little flexibility in the behavior off functions

### Anticipated Pain Points
- understanding the scope of arguments: where they can and cannot be used.

### Walkthrough

- To pass a value into a function, we add a parameter to the definition. This parameter defines the name that we will use to hold the value which we pass in. The actual value passed in is called the argument.

- Yesterday, we used the modulo operation (%, used to find the remainder of a division operation) to see if a number is even or odd. Packaging up this code into a method lets us reuse it whenever we want.
```Swift
func isEven(num: Int) -> Bool {
    if num % 2 == 0 {
        return true
    }
    return false
}
isEven(num: 4) //returns true
isEven(num: 3) //returns false
```

- Earlier today, we made some methods for greeting people.
```Swift
func greeting() -> String {
  return "Hello! How are you doing?"
}
print(greeting()) //returns "Hello! How are you doing?"
```
- We can make this a little more personal by including a function parameter. A parameter is a variable that is used inside the function. The value of the variable assignment, called the argument, goes inside the parentheses after the function's name. We need to specify the name and type of the parameter in the function's definition.
```Swift
func personalizedGreeting(name: String) -> String {
  return "Hello, \(name)! How are you doing?"
}

print(personalizedGreeting(name: "Joe")) //returns "Hello, Joe! How are you doing?"
```
- We can even pass in an array as the argument.
```Swift
var stations: [String] = ["14 St-Uniun Sq", "Astor Pl", "Bleeker St", "Spring St", "Canal St", "Brooklyn Bridge-City Hall", "Fulton St", "Wall St", "Bowling Green"]

func subwayDescription(stations: [String]) -> String {
    return "The first stop on this line is \(stations[0]) and the last stop is \(stations[stations.index(before: stations.endIndex)])"
}

subwayDescription(stations: stations)
//returns "The first stop on this line is 14 St-Uniun Sq and the last stop is Bowling Green"
```

Break for [functions practice - 2](https://github.com/upperlinecode/intro-to-swift/tree/master/day-2/FunctionsPractice2.playground)
