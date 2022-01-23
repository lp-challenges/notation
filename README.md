## Big O Notation
It is the process of describing the efficiency of algorithms as their input size grows. The notion of tracking algorithmic performance can reveal much about a solution’s effectiveness. Even though we sometimes think of algorithms as complex systems, in essence, they are merely recipes for completing a series of operations.

## LINEAR TIME 
We can write a simple algorithm to find a specific number in a sequence:
```
let sequence : Array<Int> = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
//linear time - O(n)
func linearSearch(for value: Int, list: Array<Int>) -> Bool {
    
    //check all possible values
    for number in list {
        if number == value {
            return true
        }
    }
    
    return false
}
//execute search
let isFound: Bool = linearSearch(for: 8, list: sequence)
```

When evaluating this function we say that it works in linear time — O(n) because the effectiveness of its main action is directly related to the size of its input. As a result, we can conclude that it would take longer for the function to find the value of 10 than 2 or 3. To summarize, the algorithm will have to iterate through the complete set of values when searching for a non-present value like 16. In most cases, linear time operations are referred to as being “brute force” because little effort goes into how they could run more efficiently. 

## CONSTANT TIME
When evaluating algorithms, it’s often ideal to code a solution where the size of the data input has no direct relationship on performance. Consider successful search algorithms like Google or machine learning solutions used on websites like Netflix and Amazon. These systems run in constant time and are represented with the symbol O(1). A significant difference between a linear and constant operation is logic. In the case of Google, many hardware and software complexities are put in place to ensure things work as quickly as possible. However, not all constant time operations need to be complicated.

```
//constant time operations - O(1)
class Stack<T> {
    var store : [T] = []
func peek() -> T? {
        return store.last
    }
func push(_ value: T) {
        store.append(value)
    }
func pop() -> T? {
        return store.isEmpty ? nil : store.removeLast()
    }
}
```

Known as a Stack data structure, this implementation is a favorite among hiring managers when conducting technical interviews. The reason? A Stack combines ideas found in native iOS Development (e.g., UINavigationController) along with specific language syntax (e.g., collections and generics) coupled with knowledge of Big O Notation. As shown, what makes a Stack useful is how it performs. For example, all actions can be executed without having to search through or analyze previously added items.

##algorithmic running times / logarithmic time
![time_complexity](https://user-images.githubusercontent.com/3194444/150688894-d80e53ad-f7f1-473e-b938-7bf5c25fa8ee.png)

