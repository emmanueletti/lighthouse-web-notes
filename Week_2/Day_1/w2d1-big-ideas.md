### Big Ideas from W2D1 - TDD

- TDD is super important
- write the test first and use them as the driver towards creating the solution

#### Debbugging / reading code tips

- read through the file the way JS would execute it
- when you encounter varaible definitions - add thier existence to your memory heap within the scope of where you are
- when you encounter function definitions - skip them and add thier existance to your memory heap
- when the function is then called with passed in arguements
  - go to thier definition "filed away in heap memory" and dive into what is being done
  - assign the functions local variables to the passed in varaibles (if variables are anonympus)
  - if variables are not anonymous, then pass them over by value or reference depending on what they are
