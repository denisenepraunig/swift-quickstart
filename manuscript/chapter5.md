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

```swift
var obj = ["key": "value",
           "key2": "value2",
           "key3": "value3"]

obj["key"] = "blabla"   // super awesome comment

enum ImageStyleValues: String {
   case person = "mimi"
   case product =  "fooo"
   case nonFioriStyle = "none"
}

func colorFrom2(string: String) -> UIColor {
    
    let color = colors.filter {
        print("the key:", $0)
        print("the value:", $1)
        print($0 == string)
        return $0 == string
    }
    print(color.count)
    
    let theColor = color.first?.1 ?? UIColor.clear
    
    return theColor
}
```
