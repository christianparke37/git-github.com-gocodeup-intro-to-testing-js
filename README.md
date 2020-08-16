
@ -246,9 +246,9 @@ Our next exercise is to follow the TDD workflow to develop incremental tests and
         - returns false when executed with `isEven(3)`
         - returns false when called with `isEven("banana")`
         - returns true when called with `isEven("8")`
         - returns false when called with `isEven(infinity)`
         - returns false when called with `isEven(Infinity)`
         - return false when called with a boolean input like `isEven(true)` or `isEven(false)`
         - returns false when calles without an argument like `isEven()`
         - returns false when called without an argument like `isEven()`
 - Refactor when and where you can. Be careful not to refactor before you have a handful of green tests.
 - Repeat until the tests are robust and the function works as intended.
 - Commit your work to git and push to GitHub before moving forward.
## Exercise #12 Test Drive an `isVowel` function
- Start with the smallest tests first.
- Write just enough code to green the test
- Build up functionality one small piece at a time.
- Commit your work to git at each step.
- Write each assertion, confirm the test fails, write only enough code to green that specific test, refactor, then repeat.
    - Remember to add and then "green" one test at a time. That's part of the fundamental approach of TDD.
    - Assert that:
        - `isVowel` always returns a boolean
        - `isVowel("a")` returns true
        - `isVowel("A")` returns true
        - `isVowel("y")` returns false
        - `isVowel(4)` returns false
        - `isVowel(true)` or `isVowel(false)` both return false
        - `isVowel("banana")` returns false
        - `isVowel()` returns false
- Refactor when appropriate and possible.
- Repeat until the tests are robust and the function works as intended.
- Commit your work to git and push to GitHub before moving forward.
## Exercise #13 Test Drive an `add` function
- The `add` function should sum two numbers, as long as each input is a number or a string containing a number.
- Write each assertion, confirm the test fails, write only enough code to green that specific test, refactor, then repeat (move onto the next test.)
- Assert that `add`:
    - `add(2, 3)` returns 5
    - `add(-3, -9)` returns -12
    - `add("5", 6)` returns 11
    - `add("-4", "10")` returns 6
    - `add("banana", "split")` returns NaN
    - `add(2, "apples")` returns NaN
    - `add()` returns NaN
- Start with the smallest tests first.
- Write just enough code to green the test
- Build up functionality one small piece at a time.
- If any input is not a number, return NaN
- Refactor, if possible
- Repeat until the tests are robust and the function works as intented.
- Commit your work to git and push to GitHub.
## Conclusion and completeness
- With each successive assertion/expectation in a test for a specific function, we make that unit more robust and reliable, and usually easier to refactor.
- Completeness of the unit: 
    - If the implementation for an `add` function only passes one assertion that `add(2, 3)` returns `5`, but does not work with any other numbers, then the unit is not considered complete. The implementation is incomplete, and the unit test composed of multiple assertions/expectations should demonstrate this clearly.
    - Another example: if the `isVowel` function only works for lowercase letters but fails to account , then we would consider the implementation to be incorrect. The "unit" of functionality is incomplete
    - Another example: 
- It is not feasible to test an infinite number of inputs with our assertions/expectations in a unit test. To prove that a function works in all cases is a practice closer to mathematical proofs. This is known as [Correctness](https://en.wikipedia.org/wiki/Correctness_(computer_science)) and is outside the scope of most software development due to economic and time constraints. 
- Moving forward, any time you find a bug in your implementation, here is the best practice:
    1. Author test code that reproduces that bug in an automated way. This may involve adding one or more assertions/expectations to a unit test. 
    2. Refactor your implementation, relying on your newly added automated test to guide the solution. 
    3. Now that the steps to reproduce the bug are part of your test suite, you may move forward with more confidence.
## Jasmine Documentation
- [Jasmine Global Functions](https://jasmine.github.io/api/3.3/global.html)
- [Jasmine Matchers](https://jasmine.github.io/api/3.3/matchers.html)
## More resources
- [Intro to TDD](https://www.youtube.com/watch?v=QCif_-r8eK4)
- [Sandi Metz on testing and what to test](https://www.youtube.com/watch?v=URSWYvyc42M)
- [Bob Martin on TDD and Code Quality](https://www.youtube.com/watch?v=is41fgDrqn0)
- [Three Laws of TDD](http://butunclebob.com/ArticleS.UncleBob.TheThreeRulesOfTdd)
