**CSE 15L Lab Report 5**

**Code:** <br />
```java
public class Calculator {
    public static void main(String[] args) {
        if (args.length == 3) {
            double num1 = Double.parseDouble(args[0]);
            double num2 = Double.parseDouble(args[2]);
            String operator = args[1];
            double result;

            if (operator.equals("add")) {
                result = num1 + num2;
                System.out.println("Result: " + result);
            } else if (operator.equals("sub")) {
                result = num1 - num2;
                System.out.println("Result: " + result);
            } else if (operator.equals("mul")) {
                result = num1 * num2;
                System.out.println("Result: " + result);
            } else if (operator.equals("div")) {
                result = num1 / num2;
                System.out.println("Result: " + result);
            }


        }

    }
}
```

**Terminal Output:** <br />
```
gianag@MacBook-Pro desktop % javac Calculator.java
gianag@MacBook-Pro desktop % java Calculator add 3 4
Exception in thread "main" java.lang.NumberFormatException: For input string: "add"
        at java.base/jdk.internal.math.FloatingDecimal.readJavaFormatString(FloatingDecimal.java:2054)
        at java.base/jdk.internal.math.FloatingDecimal.parseDouble(FloatingDecimal.java:110)
        at java.base/java.lang.Double.parseDouble(Double.java:792)
        at Calculator.main(Calculator.java:4)
gianag@MacBook-Pro desktop % 
```

**EdStem Post** <br />
**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?** <br />
Macbook Pro 2020, macOS Big Sur Ver 11.7.6, using VSCode for editor and terminal


**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.** <br />
When I try to run my code I am getting a FloatingDecimal error and I don't know what it means and how to fix it.


**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.** <br /> 
My code takes in two numbers and adds, subtracts, multiplies or divides them based on the given operator (add, sub, mult or div). When you run the code it should be operator num1 num2. But when I run the code it produces it an error.


**TA Response:** <br />
If the order of your argument is suppose to be operator num1 num2 then you should look at the order you put for each argument. Also, if you divide a number by 0, would an error occur? What would happen if the user provided a operator that is not add, sub, mult or div, would that produce an error? If so, what could you do to fix it. 

**Fixed Code:** <br />
```java
public class Calculator {
    public static void main(String[] args) {
        if (args.length == 3) {
            double num1 = Double.parseDouble(args[1]);
            double num2 = Double.parseDouble(args[2]);
            String operator = args[0];
            double result;

            if (operator.equals("add")) {
                result = num1 + num2;
                System.out.println("Result: " + result);
            } else if (operator.equals("sub")) {
                result = num1 - num2;
                System.out.println("Result: " + result);
            } else if (operator.equals("mul")) {
                result = num1 * num2;
                System.out.println("Result: " + result);
            } else if (operator.equals("div")) {
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("Result: " + result);
                } else {
                    System.out.println("Error: You cannot divide a number by 0.");
                }
            } else {
                System.out.println("Error: Invalid operator. Please choose from add, sub, mul, or div.");
            }
        }
    }
}
```
**Terminal Output:** <br />
```
gianag@MacBook-Pro desktop % javac Calculator.java 
gianag@MacBook-Pro desktop % java Calculator multiply 12 9
Error: Invalid operator. Please choose from add, sub, mul, or div.
gianag@MacBook-Pro desktop % java Calculator mul 12 9
Result: 108.0
gianag@MacBook-Pro desktop % java Calculator div 12 0
Error: You cannot divide a number by 0.
gianag@MacBook-Pro desktop % java Calculator sub 100 34
Result: 66.0
gianag@MacBook-Pro desktop % 
```

**Student Response:** <br />
"Thank you I did not realize the order of my args was swapped and I was able to add an if statement to check if num2 equals 0 and to send an error message when it does and also I added an error message at the end if a different operator is given from the options."


**Reflection** <br />
Something that I learned from my lab experience this quarter would be that it is very useful 
to have TAs that can actively help you with any issues you face while completing the lab task. 
I think that it is very important to ask questions when you are stuck because getting help, helps 
you grow as a programmer.
