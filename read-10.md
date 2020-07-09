# Call stack

**A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function.**

* When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.

* When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.

* If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

The key takeaways from the call stack are:

1. It is single-threaded. Meaning it can only do one thing at a time.

2. Code execution is synchronous.

3. A function invocation creates a stack frame that occupies a temporary memory.

4. It works as a LIFO — Last In, First Out data structure.

>Most of your time as a developer is spent reading code followed by debugging that same code, most likely to be able to read it or solve an “unexpected feature” (which, joking aside, is more correctly known as a “bug”).

>Being able to read error messages and practising debugging is one of your biggest weapons has a developer, do it frequently and with enough time you will notice a great decrease in the time you spend on each error that you find along the way. And remember, before a commit/push, remove all the debugging stuff from your code, we don’t want the client or another developer to get stuck on a debugger now.