# Part 1

## Part 2
For the reverse in place method in ArrayExamples.java, a failure inducing input is shown in the JUnit test below. This test shows that the method is not reversing the list as it is supposed to be.
`@Test
  public void testReverseInPlace2(){
    int[] input2 = {5,6,7};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{7,6,5}, input2);
  }`
 An input that does not produce a failure can be seen as below. 
 
The symptom is that the array was not being reversed. 

One bug in the code was that it should not run through the whole array but only half because it is swapping the left and right side. The other bug was that there has to be a temporary integer variable that works to swap both sides of the array; it does this by storing each value of the array in the variable temp and then swapping them.

Before:
` static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  
After: 
`static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }`
  
These changes fixed the bug because now the array will be properly reversed; the right and left sides are swapped after doing arr.length/2. Also the temp variable stores each index so that it can swap the index on the left with the one it mirrors on the right.


## Part 3
Something from lab 3 that I did not know before 
