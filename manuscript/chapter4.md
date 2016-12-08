# Chapter 4

Now here some source code examples with turning off line-numbers.

{language=swift,line-numbers=off}

Here comes the source code. It is formatted with tilde.

~~~~~~~~
func first() -> () -> Int {
   var counter = 0
    
   func second() -> Int {
      counter += 1
      return counter
   }
   return second
}
let incrementor = first()
print("The count is \(incrementor())")  // "The count is 1"
~~~~~~~~

Now with the default github formatting.

{line-numbers=off}

```swift
func first() -> () -> Int {
   var counter = 0
    
   func second() -> Int {
      counter += 1
      return counter
   }
   return second
}
let incrementor = first()
print("The count is \(incrementor())")  // "The count is 1"
```
