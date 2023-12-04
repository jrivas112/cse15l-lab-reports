<body>

<h1>Student Post</h1>

<p>Hi everyone,</p>

<p>
        I'm having a weird issue with my Java program. I've attached a screenshot below that shows the output I'm
        getting. The program is supposed to calculate the factorial of a given number, but as you can see, the
        result is way off. I've tried different input values, and it always gives me unexpected output.
</p>

<img src="link_to_screenshot" alt="Java Program Screenshot">
<p>
        Here's a snippet of my code:
</p>


<p>
        I'm not sure what's causing this strange behavior. Any help would be appreciated!
</p>

<h1>Response from TA</h1>
<p>Hey there!</p>
<p>
        Thanks for providing the details. It seems like your factorial calculation logic might be correct, but
        let's try to debug this step by step. Can you print intermediate values inside your
        <code>calculateFactorial</code> method to see what's happening at each step? You can add some
        <code>System.out.println</code> statements to help with that.
</p>
<p>
        Try modifying your <code>calculateFactorial</code> method like this:
</p>

    <pre><code>public static long calculateFactorial(int n) {
    System.out.println("Calculating factorial for n = " + n);
    
    if (n == 0 || n == 1) {
        return 1;
    } else {
        long result = n * calculateFactorial(n - 1);
        System.out.println("Intermediate result for n = " + n + " is: " + result);
        return result;
    }
}</code></pre>
<p>
        Run the program again with these changes and share the output. This should give us more insight into where
        the issue might be.
</p>
