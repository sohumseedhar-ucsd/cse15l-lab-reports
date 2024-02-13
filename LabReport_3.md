## Failure Inducing Input for `reverseInPlace` Method:
```
@Test 
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);

    int[] input2 = {1, 2, 3, 4, 5, 6};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{6, 5, 4, 3, 2, 1}, input2);
}
```
## Input That Did Not Induce Failure for `reverseInPlace` Method:
```
@Test 
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
}
```
## The Symptom:

![Image](https://github.com/sohumseedhar-ucsd/cse15l-lab-reports/blob/main/Screenshot%202024-02-12%20at%204.38.13%20PM.png?raw=true)

## The Bug:
### Before:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = arr[arr.length - i - 1];
    }
  }
```
### After:
```
static void reverseInPlace(int[] arr) {
    int[] tempArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        tempArray[i] = arr[arr.length - i - 1];
    }
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = tempArray[i];
    }
}
```



* Which methods in your code are called?
  The `handleRequest` method in the `ChatHandler` class is called to handle the incoming request.
  Example:
  ```
  ChatHandler.handleRequest(URI url);
  ```
