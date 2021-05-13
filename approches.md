# Problem Approaches

---

## Stacks and Recursion Elimination

- **Removal of Tail Recursion**: An algorithm is said to be tail recursive if the recursive step is the last step in the algorithm. Recursion can be eliminated from a tail recursive algorithm by noting what happens during the recursive call. It is possible to accomplish the same effect without recursion by using a simple looping construct like a while do loop and a local variable instead of a subprogram parameter
  
  eg:
  
  ```java
  // function with recursion
  public static long fac(int n) {
    long returnValue;
    if (n == 0) returnValue = 1;
    else returnValue = n * fac(n - 1);
    return returnValue;
  }
  
  // removing recursion
  public static long fac(int n) {
    long returnValue = 1;
    while (n > 0) {
      returnValue = fac * n;
      n--;
    }
    return returnValue;
  }
  ```

- **Recursion Elimination using System Stack Simulation**: The following strategy can be used to the remove the recursion from a recursive routine, although notelegantly.
  
  1. Each time a recursive call is made in the algorithm, push the necessary information onto yourstack.
  
  2. When you complete processing at this deeper level, pop the simulated stack frame and continue processing in the higher level at the point dictated by the return address popped from the stack.
  
  3. Use an iterative control structure that loops until there are no return addresses left to pop from the stack
  
  ```javascript
  var stack = [];
  stack.push(firstObject);
  
  // while not empty
  while (stack.length) {
  
      // Pop off end of stack.
      obj = stack.pop();
  
      // Do stuff.
      // Push other objects on the stack as needed.
      ...
  
  }
  ```
