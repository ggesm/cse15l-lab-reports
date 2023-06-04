**CSE 15L Lab Report 5**

```
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

**EdStem Post** <br />
**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?** <br />
Macbook Pro 2020, macOS Big Sur Ver 11.7.6, using VSCode for editor and terminal


**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.** <br />



**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.** <br /> 



**Reflection** <br />
Something that I learned from my lab experience this quarter would be that it is very useful 
to have TAs that can actively help you with any issues you face while completing the lab task. 
I think that it is very important to ask questions when you are stuck because getting help, helps 
you grow as a programmer.
