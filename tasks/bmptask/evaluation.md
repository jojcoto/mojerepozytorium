# Evaluation

## Topic covarage

* Git version control system
* GitHub service
* Apache Commons IO library
* Guava library
* JUnit test framework
* Mockito test framework
* Maven
* operations on bits and bytes

## Implementation remarks

* Use proper directories layout for test resources e.g. src/test/resources
* Mockito should be test-scoped dependency
* Eclipse project metadata (.settings, .project) should not be kept in version control system
* Binaries and other build artifacts should not be kept in version control system
* Why ImageTransformerFactory and FileUtility are Enums? Why not plain classes?
* Avoid static methods, instead of it use singletons or shared single instance.
* In ImageTransformerBMP256Colors fields should be final, since they are assigned once in constructor.
* String literals should be declared as static fields
* ImageTransformerBMP256Colors has at least two responsibilities (violation of single responsibility principle): transforming bitmap bytes and saving to file.
* Tests should cover more cases, especially corner cases: invalid bitmap, empty bitmap, large bitmap etc.
* Tests could be parameterized with more original+rotated cases, JUnit offers utils for parameterized tests and theories
* Tests could be more smart: e.g. when rotating n times we should get the original image, width*height is constant after rotation, etc.
* rotateTest is too generic name for a test method, instead it should explain what feature it tests
* Don't see TDD and usage of mocks!
* Revision graph (see network tab alongside) looks peculiar (master vs mater2 branches) but it look like git newbie's problems ;)

## Recommendation for further training

* Make use of git branches/merges to learn it -> lecture: Git documentation
* Make TDD! -> lecture: Growing object-oriented system with tests
* Learn about are the alternatives for static methods -> lecture: clean code
* Do the exercise: imagine that customer now needs to rotate by 90, 180 and 270 degrees in given direction. How would you refactor the code?

