## Part 1
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    ArrayList<String> array = new ArrayList<>();


    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return concatString(array);
        } 
        else if (url.getPath().equals("/add-message")){
            String[] parameters = url.getQuery().split("=");
            array.add(parameters[1]);
            return concatString(array);
        }
        return "404 Not Found!";
    }

    public String concatString(ArrayList<String> array){
        String s = "";
        for (int i=0; i<array.size(); i++){
            s = s+array.get(i)+"\n";
        }
        return s;
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing string");
            return;
        }

        int port = Integer.parseInt(args[0]);
        Server.start(port,new Handler());
    }
}
```

## Part 2
For the reverse in place method in ArrayExamples.java, a failure inducing input is shown in the JUnit test below. This test shows that the method is not reversing the list as it is supposed to be.
TEST #1:
```
@Test
  public void testReverseInPlace2(){
    int[] input2 = {5,6,7};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{7,6,5}, input2);
  }
 ```
An input that does not produce a failure can be seen as below. Since there is only one element in the list, that element in the list is the only thing being returned. 
 TEST #2:
```
 @Test 
  public void testReverseInPlace3(){
    int[] input3 = {0};
    ArrayExamples.reverseInPlace(input3);
    assertArrayEquals(new int[]{0}, input3);
  }
 ```
Symptom from TEST #1:
![Image](lab2-ss1)
The symptom that is being produced here is due to the fact that the list is not being reversed. Index 2 should be 5 (reversing the list should give you {7,6,5}) but instead, it is 7.

Symptom from TEST #2:
![Image](lab2-ss2)
No error output is being produced here because there is only one element in the list (one element being reversed is just that element itself).

One bug in the code was that it should not run through the whole array but only half because it is swapping the left and right side. The other bug was that there has to be a temporary integer variable that works to swap both sides of the array; it does this by storing each value of the array in the variable temp and then swapping them.

Before:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
```
After: 
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
 ```
These changes fixed the bug because now the array will be properly reversed; the right and left sides are swapped after doing arr.length/2. Also the temp variable stores each index so that it can swap the index on the left with the one it mirrors on the right.


## Part 3
Something from lab 3 that I did not know before is that you can create your own server through VS code! I found it very interesting that I could make changes to the command line arguments when running NumberServer.java and it would lead to a browser on my computer that had the updated command line arguments. Furthermore, I learned different path and query combinations that made changes to the server, which I found very cool!
