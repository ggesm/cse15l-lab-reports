**CSE 15L Lab Report 5**

Code: <br />
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

Terminal: <br />
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



**Reflection** <br />
Something that I learned from my lab experience this quarter would be that it is very useful 
to have TAs that can actively help you with any issues you face while completing the lab task. 
I think that it is very important to ask questions when you are stuck because getting help, helps 
you grow as a programmer.
