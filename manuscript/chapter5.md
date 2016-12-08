# Chapter 5

Now let's test if we can turn off those line numbers...

{linenos=off}

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

So please Leanpub - turn off those line-numbers, all those **copy-pasters** will love us!
