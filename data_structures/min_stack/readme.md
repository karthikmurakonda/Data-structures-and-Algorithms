# Min stack or Monotonic stack

A stack that supports push, pop, top, and retrieving the minimum element all in constant time.

## Implementation

```cpp
class MinStack {
public:
    // store the element and the current minimum
    stack<pair<int,int>> s;

    MinStack() {
    }
    
    void push(int x) {
        if(s.empty())
            s.push({x,x});
        else
            s.push({x,min(x,s.top().second)});
    }
    
    void pop() {
        s.pop();
    }

    int top() {
        return s.top().first;
    }

    int getMin() {
        return min_s.top().second;
    }
}
```
If there are any monotonic indices. then we can only push new element if it is minimum than the current minimum. In that case we cannot get top element from data structure but we can get the minimum element in constant time.

## Complexity
| Operation | Time Complexity |
|-----------|-----------------|
| push      | O(1)            |
| pop       | O(1)            |
| top       | O(1)            |
| getMin    | O(1)            |

## Use cases

- when you need to find the minimum element in a stack in constant time and all operations of the stack are in constant time

- [TBA]

## Practice Problems
- [Leetcode 155. Min Stack][https://leetcode.com/problems/min-stack/]
- [TBA]
