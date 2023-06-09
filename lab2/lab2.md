# StringServer
**Huaming Wu**
**A17526592**

## Part 1

Code:

![Image](lab2_code1.png)
![Image](lab2_code2.png)

1. **Adding hello!**
: The handleRequest method is called. It checks if the path from URI url contains "/add-message" and then checks the query to know what message to add to str. str is updated when handling this request. The first parameter for url is whether or not it equals s. If so, the method will concatenate the message from the second parameter and return the str. In this case, str is changed to hello!.

![Image](Lab2_1.png)

2. **Adding goodbye**
: The handleRequest method is also called. It checks if the path from URI url contains "/add-message" and then checks the query to know what message to add to str. str is updated when handling this request. The first parameter for url is whether or not it equals s. If so, the method will concatenate the message from the second parameter and return the str. In this case, str is changed to 

hello!

goodbye

![Image](lab2_2.png)

If a port number is not given as the second parameter for java StringServer, it will print out an error message.
There is also a Server.start() method that starts the server using the start method from Server.java

## Part 2

**Example code**

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

**Error Test**

```
@Test 
public void testReverseInPlace() {
   int[] input1 = {3, 5, 6, 7};
   ArrayExamples.reverseInPlace(input1);
   assertArrayEquals(new int[]{7, 6, 5, 3}, input1);
}
```

**Non-Error Test**

```
@Test 
public void testReverseInPlace() {
    int[] input1 = {3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3}, input1);
}
```
**Outputs**

Failure

![Image](Error2.png)

No Failure

![Image](Error.png)

**Bug Fix**

Bug

```
for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
```

Fix

```
for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
```

This change fixed the issue because the original does not have a temporary variable that holds the original value of arr[i]. This makes it so that we are losing some int values due to the loop. Furthermore, we need to make sure that the loop loops arr.length/2 times so that the indices can be replaced accordingly. We need this since we are basically swapping the beginning indices with its corresponding end indices.

## Part 3
I feel like I was able to practice my debugging a lot more. I have also been able to learn how to better impelement a server side program that makes my website a lot more dynamic. Lastly, I am becoming more comfortable using GitHub.

