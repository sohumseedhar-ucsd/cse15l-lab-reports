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
* The fix addressed the issue because in the original method, the original values of the array that needs to be reversed are being overwritten before the entire array is reversed. As a result, some elements may be swapped multiple times, leading to incorrect results when performing testing for an array with multiple elements. I first wrote a test case expecting the result of reversing an array list with multiple elements to reveal the bug. I then fixed the `reverseInPlace` method by creating `tempArray` to compute the reversed list, and then copy the values from `tempArray` over to the original array `arr`. This way, each element is only swapped once and the reversal of elements occurs correctly.

## `less` Command:
### `-N` (Line Numbers):
*The `less -N` command enables line numbering when using the less pager to view a file. When you open the file with `less -N`, you'll see line numbers on the left side of the screen, making it easier to navigate and reference specific lines in the file. If you use the `less -N` command with a directory instead of a file, less will typically display a list of files in the directory along with line numbers.
### `-S` (Chop Long Lines):
When you use `less` with the `-S` option, it causes long lines to be truncated at the edge of the terminal screen, making it easier to read lines that are too long to fit on one line. Using `-S` is particularly useful when viewing files because it displays as much of the line as can fit within the terminal window, making it more convenient to read. When using `less -S` on a directory, `less` will display a list of filenames in the specified directory, and each line will be truncated if the filenames are too long to fit within the terminal width.
### `-G` (Highlight Search Matches):
The `less -G` command-line option in the less pager stands for "highlight search matches" and when used it enables the highlighting of search matches in the displayed text. Once you are inside `less`, you can use the search feature by typing `/` followed by a `search pattern` and then pressing Enter. if whatever you use as your `search pattern` is present in the file, the matches will be highlighted, making them visually distinct from the rest of the text.
### `-p pattern` (start at pattern):
When you use the command `less -p pattern` and pass a filename, `less` will open the file and position the view at the first occurrence of the specified search `pattern`. If you use `less -p pattern` on a directory, `less` will display a list of filenames that match the specified `pattern` in the directory. 

### `less -N` used on file:
* Command:
```
(base) sohum@Sohums-MacBook-Pro-280 OANC-GrAF % cd data/written_1/fiction/eggan
(base) sohum@Sohums-MacBook-Pro-280 eggan % less -N TheStory.txt
```
* Output:
```
      1 
      2         
      3                 
      4                         
      5                                 The Story Continues . . . a serial enovel by Ferd Eggan
      6                         
      7                         1 Welcome to Hotel Real Desert 
      8                         But he never fell into the error of arresting his intellectual
      9                                 development by any formal acceptance of creed or system, or of
     10                                 mistaking, for a house in which to live, an inn that is but suitable for
     11                                 the sojourn of a night in which there are no stars and the moon is in
     12                                 travail . . 1
```
* Explanation: This command reads out the contents of the file with line numbering enabled on the side. I did not include the entire output since it was too long, but the code snipped should show the utility of having line numbering when reading a file as it makes it easier to navigate and reference lines of a file. 


### `less -N` used on directory:
* Command:
```

```
* Output:
```

```
* Explanation: This command reads out the contents of the file with line numbering enabled on the side. I did not include the entire output since it was too long, but the code snipped should show the utility of having line numbering when reading a file as it makes it easier to navigate and reference lines of a file. 
### `less -S` used on file:
* Command:
```

```
* Output:
```

```
* Explanation: This command reads out the contents of the file with line numbering enabled on the side. I did not include the entire output since it was too long, but the code snipped should show the utility of having line numbering when reading a file as it makes it easier to navigate and reference lines of a file. 
### `less -S` used on directory:

### `less -G` used on file:

### `less -G` used on directory:

### `less -p pattern` used on file:

### `less -p pattern` used on directory:







