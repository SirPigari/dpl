Dank Programming Language (DPL) Keywords and Features
=====================================================

Control Flow
------------

### alpha

Defines a function.

    alpha greet() {
        throw ln("Hello!");
    }

### beta

Defines a lambda function.

    let square = beta(x) => x * x;
    sigma result = square(5);

### by

Used in interrupt statements to specify sleep duration in seconds or ignore lines.

    interrupt self by 3;  // Pauses execution for 3 seconds

### call

Invokes a function.

    alpha greet() {
        throw ln("Hello!");
    }
    
    call greet();

### dont give back

Specifies that a function does not return a value.

    alpha say_hello() {
        throw ln("Hello!");
        dont give back;
    }

### fanum tax

Reverses the boolean value of a variable.

    sigma x = false;
    fanum tax x;

### for

Looping structure for iterating over collections.

    for sigma i = 0; i < 5; i = i + 1 {
        throw ln("Iteration: " + i);
    }

### forgot

Revives a forgotten variable.

    sigma x = false;
    fanum tax x;
    forgot x;
    throw ln("Value of x: " + x);

### fuck it

Exits the program without error.

    alpha exit() {
        fuck it;
    }

### fuck out

Exits the program with an error.

    alpha error(message) {
        throw ln("Error: " + message);
        fuck out;
    }

### give back

Returns a value from a function.

    alpha add(a, b) {
        give back a + b;
    }
    
    sigma result = add(3, 5);
    throw ln("Result: " + result);

### ignore

Skips a statement or block of code.

    ignore {
        throw ln("This code is ignored.");
    }

### let

Declares variables.

    let num = 10;
    throw ln("Number: " + num);

### make

Creates instances or copies of variables.

    sigma x = 5;
    sigma y make x;

### object

Defines a class-like structure.

    object Person {
        alpha __init__(self, name) {
            self.name = name;
        }
        
        alpha greet(self) {
            throw ln("Hello, " + self.name + "!");
        }
    }
    
    sigma person = make Person("Alice");
    call person.greet();

### of

Used with \`rob\` to import specific elements from a module.

    rob math of *;
    sigma sqrt_result = math.sqrt(25);

### remind me

Revives a variable that was previously deleted.

    sigma x = 10;
    thanos snap x;  // Deletes x
    remind me of x;
    throw ln("Value of x: " + x);

### rob

Imports libraries or specific elements.

    rob math of *;
    sigma sqrt_result = math.sqrt(25);

### sigma

Declares variables or handles I/O operations.

    sigma name;
    ask(name);
    throw ln("Hello, " + name + "!");

### steal

Imports a library or module.

    steal math;

### thanos snap

Deletes a variable.

    sigma x = 10;
    thanos snap x;

### yall

Looping structure.

    sigma i = 0;
    yall (i < 5) {
        throw ln("Iteration: " + i);
        i = i + 1;
    }

### yeet, yeet again, yeet last

Conditional statements (\`if\`, \`else if\`, \`else\`).

    yeet (x > 0) {
        throw ln("x is positive");
    } yeet again (x == 0) {
        throw ln("x is zero");
    } yeet last {
        throw ln("x is negative");
    }

Built-in Functions
------------------

### ask

Prompts the user for input.

    sigma name;
    ask(name);
    throw ln("Hello, " + name + "!");

### catch

Catches and handles exceptions.

    try {
        throw ln("Hello");
    } catch e {
        call error(e);
    }

### interrupt

Pauses execution for a specified duration.

    interrupt self by 3;  // Sleeps for 3 seconds

### lifetime

Sets a lifetime for variables.

    sigma x make lifetime 10;

### see

Compares variables or values.

    sigma x = 5;
    see x;

### throw f

Throws a formatted message.

    throw f("Value of x is {x}");

### throw ln

Throws a line of text.

    throw ln("Hello, World!");

### try

Starts a block of code and handles exceptions.

    try {
        throw ln("Hello");
    } catch e {
        call error(e);
    }

Booleans
--------

### false

Boolean value representing false.

    sigma flag = false;

### maybe

Boolean value that may change.

    sigma flag = maybe;

### null

Represents a null or undefined value.

    sigma data = null;

### true

Boolean value representing true.

    sigma flag = true;

Functions
---------

### error

Throws an error message and exits the program.

    alpha error(message) {
        throw ln("Error: " + message);
        fuck out;
    }

### other

Handles other cases or conditions.

    yeet (x) {
        throw f("{x}");
    } yeet last {
        throw f("{x}");
    }

### self

Refers to the current object or context.

    object Person {
        alpha __init__(self, name) {
            self.name = name;
        }
        
        alpha greet(self) {
            throw ln("Hello, " + self.name + "!");
        }
    }
    
    sigma person = make Person("Alice");
    call person.greet();

### success

Indicates successful execution.

    alpha success(message) {
        throw ln("Success: " + message);
    }
