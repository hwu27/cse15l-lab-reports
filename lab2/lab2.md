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

If a port number is not given as the second parameter for java StringSerrver, it will print out an error message.
There is also a Server.start() method that starts the server using the start method from Server.java

## Part 2

**Example code**

```
class EvensExample {
  static int sumEvenIndices(int[] nums) {
    int sum = 0;
    for(int i = 0; i < nums.length; i += 2) {
      sum += nums[i + 1];
    }
    return sum;
  }
}
```

**Error Test**

```
@Test 
public void testSumEvenLength5() {
    int[] input1 = { 12, 13, 7, 2, 33};
    assertEquals(EvensExample.sumEvenIndices(input1), 52);
}
```
