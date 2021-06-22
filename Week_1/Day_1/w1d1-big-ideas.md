### Big Ideas from W1D1

- Pseudo-code is a powerful step in problem solving by abstracting language specific syntax and focusing on the core F.O.C.A.L steps invovled in solving the problem

- F.O.C.A.L is the core fundamentals to problem solving found in most programming languages

  - F - functions
  - O - objects
  - C - conditionals
  - A - arrays
  - L - loops

- When solving a problem:

  1. start with re-stating the problem into simple english
     - what are the inputs?
     - what are the constraints?
     - what is the expected output?
  2. divide the problem into smaller and smaller sub-problems / chunks . Keep dividing till each "chunk" is simple
  3. write out the pseudocode algorithmic steps needed given the inputs
     - go through the first few iterations by hand
     - build inital solution with fundamental F.O.C.A.L toolkit
     - after solution works, then refactor for simplicity, readability, DRY, and abstraction using higher level language specific methods such as (split, join, map, etc.)
     - pseudo code example:

  ```code
  Declare a variable initialized to an empty string

  Function with array input:

    Loop from index 0 of array to end

      If our index position !== the last index:
        take element in index position
        concatenate it to empty string + comma + space
      Otherwise:
        take element in index position
        concatenate it to empty string
      End if

    End loop

  End function
  ```

- saying this again because it was super important: learnt to focus on building the initial solution to a code problem using language agnositic F.O.C.A.L fundamentals THEN refactoring using relavant languge specific methods (e.g map, join, splice, etc.)

- Learn about using DRY idea to see opportunities for simplification in code solutions

- Leant how to access arguements passed to a javscript file in the node runtime environment using nodes global argument array process.argv

- Learnt about basic unit testing using console.assert and a custom made assertEqual function

  1. learnt how to use the unit testing framework to test array outputs
