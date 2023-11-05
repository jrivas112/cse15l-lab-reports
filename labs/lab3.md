## [Lab Report 3 - Bugs and Commands (Week 5)]

## Part 1 - Bugs
Choose one of the bugs from week 4’s lab.

Provide:

1. A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
```
@Test 
 public void testReverseInPlace() {
    int[] input1 = {1,2,3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3,2,1}, input1);
	}


@Test
  public void testReversed() {
    int[] input1 = {1,2,3};
    assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input1));
  }
```
2.An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
```
 @Test
    public void testReverseInPlace() {
        int[] input1 = {3};
        ArrayExamples.reverseInPlace(input1);
        assertArrayEquals(new int[]{3}, input1);
    }


    @Test
    public void testReversed() {
        int[] input1 = {};
        assertArrayEquals(new int[]{}, ArrayExamples.reversed(input1));
    }
```
3.The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
### Successful Test
These are the inputs that doesn't induce test failure, as mentioned above. 
![Alt text](images/successfultest.png "Successful Test")
### Failure Inducing Test
These are the inputs that induce test failure, as mentioned above. 
![Alt text](images/failedtest.png "Failed Test")
4.The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
