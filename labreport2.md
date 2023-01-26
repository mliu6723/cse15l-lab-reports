# Week 3 Lab Report

# Part 1
**Below is the code for my StringServer**
![Lab 3 Code](images/labThreeCode.png)

**Below are the screenshots of using `/add-message`** 

![First Run](images/firstRun.png)

In this first screenshot, firstly the main method is called when the program is run. Then, the `handleRequest` method is run. The value "Missing port number! Try any number between 1024 to 49151" is used to notify the user that they did not specify a port number when starting the server. 

For the main method, the primary relevant argument is the input in the terminal, which communicates which port to start the web server on. In this case, it is 4000. 

For the `handleRequest method`, there are several important arguments and values. Firstly, there is the method parameter `URI url` which represents the url of the web server that is being run. Second, there is the `ArrayList<String> list`. This list represents a list of the strings that are being stored on the web server. Finally, there is also `String display`. This string represents what is going to be output to the web server. It represents all the strings in the arraylist list with line breaks between each element. From this specific request, the String arraylist list is changed because a new element is added to it, "hello". The String display is also changed to "hello \n" because list was changed. 

Other specific values include "/" which is used to check if there is a path or if the path is just "/". "Path: " is used to format the output to print out the path of the url. "/add-message" is used to check if the path is equal to "/add-message" which is the desired path for this program. There is also "=" which serves as an indicator to split the query section of the url. "s" is the value that is before this indicator and after this indicator is the String that we will be storing on the web server. The value "404 Not Found!" is used in case the url was not formatted as we expected. The value "" is an empty string and is used twice, once in case the path is just "/" as there is no String to store, and secondly when declaring `String display`. This is to set the initial value of this String to an empty String.

![Second Run](images/secondRun.png)

In this second screenshot, firstly the main method is called when the program is run. Then, the `handleRequest method` method is run. The value "Missing port number! Try any number between 1024 to 49151" is used to notify the user that they did not specify a port number when starting the server. 

For the main method, the primary relevant argument is the input in the terminal, which communicates which port to start the web server on. In this case, it is 4000. 

For the `handleRequest` method, there are several important arguments and values. Firstly, there is the method parameter `URI url` which represents the url of the web server that is being run. Second, there is `ArrayList<String> list`. This list represents a list of the strings that are being stored on the web server. Finally, there is also `String display`. This string represents what is going to be output to the web server. It represents all the strings in the arraylist list with line breaks between each element. From this specific request, the String arraylist list is changed because a new element is added to it, "How are you". The String display is also changed to "hello \n How are you \n" because list was changed. 

Other specific values include "/" which is used to check if there is a path or if the path is just "/". "Path: " is used to format the output to print out the path of the url. "/add-message" is used to check if the path is equal to "/add-message" which is the desired path for this program. There is also "=" which serves as an indicator to split the query section of the url. "s" is the value that is before this indicator and after this indicator is the String that we will be storing on the web server. The value "404 Not Found!" is used in case the url was not formatted as we expected. The value "" is an empty string and is used twice, once in case the path is just "/" as there is no String to store, and secondly when declaring `String display`. This is to set the initial value of this String to an empty String.

# Part 2
Failure-inducing input for `averageWithoutLowest` :  
```
@Test
  public void testAverageWithoutLowest() {
    double[] input1 = {3, 1, 1, 1, 5 };
    assertEquals(4.0, ArrayExamples.averageWithoutLowest(input1), 0);
  }
 ```
Input that doesn't induce a failure for `averageWithoutLowest`
```
@Test
  public void testAverageWithoutLowesWorkst() {
    double[] input1 = {3, 1, 5 };
    assertEquals(4.0, ArrayExamples.averageWithoutLowest(input1), 0);
  }
 ```

Symptom as output of running tests: 
![Failed Tests](images/failedTests.png)

Bug (Before): 
```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
        if(num != lowest) { 
            sum += num; 
        }
    }
    return sum / (arr.length-1);
  }
```

Bug (After):
```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    int counter = 0;
    for(double num: arr) {
        if(num != lowest) { 
            sum += num; 
        }else{
            counter++;
        }
    }
    return sum / (arr.length - counter);
  }
```

# Part 3
From lab in week 2 and week 3, I learned a lot about web servers, something that I did not know before. I learned specifically how to run a web server from the terminal and how to then access that web server. Furthermore, I learned the basics of constructing a web server in VSCode from scratch. 

