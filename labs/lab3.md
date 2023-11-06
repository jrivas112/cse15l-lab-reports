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
### Bug: reversed()
The error in the reversed() method was that we weren't putting anything in reverse into the new array
called newArray, in addition, we were just returned this array we had alrady inputed and modified. We were not returning
newArray
```
    static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
    return arr;
  }
```
### Solution: reversed()
The solution is to properly set newArray to the reverse order of arr and returning newArray as you see below
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
### Bug 2: reversedInPlace()
The bug here is that we are not storing the value we replaced, so if we have the list 1,2,3, when we switch spots between 1 and 3, 3 will go to arr[0] but 1 won't 
go to arr[2]. We need a temporiry variable to hold the value we are replacing in order to store it in the new index. In addition, we dont wan't to reverse the order for 
arr.length iterations, we only want to iterare the array for arr.length/2 since we are just replacing an index i for an index arr.length-i.
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
### Solution 2: reversedInPlace()
The solution is to essentially replace the elementns in indicies i with elements in indices arr.length-i and in addition we implemented the temporary variable in order to store the element we are replacing.
```
  static void reverseInPlace(int[] arr) {
    int temp = 0;
    for(int i = 0; i < (arr.length/2); i += 1) {
      temp = arr[i];
      arr[i] = arr[arr.length-1 - i];
      arr[arr.length-i-1] = temp;
    }
  }
```
### Part 2 - Researching Commands
