# 🔥 JavaScript Brain Teasers & Debugging Interview Questions

## 🚀 About This Repository

Welcome to the **JavaScript Brain Teasers & Debugging Interview Questions** repository! 🎯 This is your go-to resource for **real-world JavaScript debugging challenges** and **tricky interview questions**, inspired by actual problems faced by developers in top tech companies.

If you've ever spent hours debugging **weird JavaScript behavior**, this repo is for you! You'll find **structured explanations**, **solutions**, and **best practices** to sharpen your debugging skills and **ace JavaScript interviews**.

---

## 📌 Table of Contents

1. [Tricky JavaScript Questions](#-tricky-javascript-questions)

2. [Contributing](#-contributing)
---

## 🧠 Tricky JavaScript Questions

- 1- JS types
    
    ```jsx
    console.log(typeof NaN);
    console.log(typeof undefined);
    console.log(typeof null);
    console.log(typeof 1);
    console.log(typeof typeof "1");
    console.log(typeof typeof 1);
    console.log(typeof Number);
    ```
    
- 2- Temporal Dead Zone (TDZ) for let variables
    
    ```jsx
    let x = 1;
    function outer() {
        console.log(x);
        let x = 2;
    }
    outer();
    // What's the output and why?
    ```
    
- 3- Block scope TDZ
    
    ```jsx
    let x = 1;
    {
        console.log(x);
        let x = 2;
    }
    ```
    
- 4- const with different types
    
    ```jsx
    
    const number = 42;
    const numbers = [1, 2, 3];
    const obj = {
        count: 0
    };
    
    // Test Cases:
    console.log(number++);                          // Case 1
    console.log(numbers.push(4));                   // Case 2
    console.log(numbers = [5, 6]);                  // Case 3
    console.log(obj.count++);                       // Case 4
    console.log(obj = { count: 1 });                // Case 5
    ```
    
- 5- Hoisting
    
    ```jsx
    function sayHi() {
        console.log(name);
        console.log(age);
        var name = "John";
        let age = 20;
    }
    sayHi();
    ```
    
- 6- Function declaration hoisting
    
    ```jsx
    function getMessage() {
        function message() {
            return "Hello";
        }
        return message();
        function message() {
            return "Goodbye";
        }
    }
    console.log(getMessage());
    ```
    
- 7- Boolean & Number conversion of strings
    
    ```jsx
    console.log(Boolean("false"));
    console.log(Boolean(false));
    console.log(Number("false"));
    console.log(Number(false));
    console.log(Number("1"));
    console.log(Number(1));
    ```
    
- 8- Type coercion with unary plus
    
    ```jsx
    console.log("b" + "a" + +"a" + "a");
    ```
    
- 9-  Unary plus type conversion
    
    ```jsx
    console.log(+"");
    console.log(+[]);
    console.log(+{});
    ```
    
- 10- Basic array/object coercion
    
    ```jsx
    console.log([] + []);
    console.log(![] + []);
    console.log([] + {});
    console.log({} + []);
    console.log({} + {});
    ```
    
- 11- Complex coercion and array indexing
    
    ```jsx
    console.log((![] + [])[+[]] + (![] + [])[+!+[]] + ([![]] + [][[]])[+!+[] + [+[]]])
    ```
    
- 12- Number Method Syntax & JavaScript Parser Behavior
    
    ```jsx
    console.log(5.toString());
    console.log(5..toString());
    console.log(1.0.toString());
    console.log(-1 .toString());
    console.log(parseInt(".5"));
    ```
    
- 13- Numeric Literal Syntax and Octal Numbers
    
    ```jsx
    const num1 = 02020;
    const num2 = 0o2020;
    console.log(num1);
    console.log(num2);
    ```
    
- 14- Floating-point precision in JavaScript
    
    ```jsx
    let result = 0.1 + 0.2;
    console.log(result === 0.3);
    console.log(((0.1 + 0.2 * 10) / 10) === 0.3);
    console.log((0.1 + 0.2 + 0.3).toFixed(1));
    ```
    
- 15- Math.min/max with no arguments
    
    ```jsx
    console.log(Math.min() > Math.max());
    console.log(Math.min() < Math.max());
    console.log(Math.min() === -Infinity);
    ```
    
- 16- Number Type Conversion Methods & Parsing Behavior
    
    ```jsx
    console.log(parseInt("123abc"));   
    console.log(Number("123abc"));      
    
    console.log(parseInt("abc123"));     
    console.log(Number("abc123"));       
    
    console.log(parseInt("12.34"));     
    console.log(Number("12.34"));    
    
    console.log(parseInt(""));         
    console.log(Number(""));             
    ```
    
- 17-  Type coercion in loose equality
    
    ```jsx
    console.log(null == undefined);  
    console.log(null == false);      
    console.log(undefined == false); 
    console.log(null == 0);     
    console.log(undefined == 0);  
    console.log([] == ![]);
    ```
    
- 18- Type coercion with + operator
    
    ```jsx
    console.log(1 + "2" + "2");
    console.log(1 + +"2" + "2");
    console.log([1,2] + [3,4]);
    console.log(+true + "");
    console.log(true + false);
    ```
    
- 19- Object and array addition
    
    ```jsx
    console.log([] + {});
    console.log({} + []);
    console.log([] + []);
    console.log({} + {});
    ```
    
- 20-  Null comparisons
    
    ```jsx
    console.log(null > 0);
    console.log(null == 0);
    console.log(null >= 0);
    console.log(null > false);
    console.log(null == false);
    console.log(null >= false);
    ```
    
- 21- Array self-comparison
    
    ```jsx
    const arr = [1, 2, 3];
    console.log(arr > arr);
    console.log(arr >= arr);
    console.log([] > []);
    ```
    
- 22- Array and negated array and Object comparison
    
    ```jsx
    console.log([] > ![]); 
    console.log([] == ![]);
    console.log([] === ![]);
    console.log({} > {});
    console.log({} >= {});
    console.log({} == {});
    ```
    
- 23- Chained comparison operators
    
    ```jsx
    console.log(1 < 2 < 3);
    console.log(3 > 2 > 1);
    console.log(3 > 2 > 0);
    ```
    
- 24- Reference vs reassignment
    
    ```jsx
    let x = [1, 2, 3];
    let y = x;
    x = [4, 5, 6];
    console.log(y);
    ```
    
- 25- Array length with sparse arrays
    
    ```jsx
    const numbers = [1, 2, 3];
    numbers[10] = 10;
    console.log(numbers.length);
    ```
    
- 26- delete operator return values
    
    ```jsx
    let x = { y: 1 };
    console.log(delete x.y);
    console.log(delete x.z);
    ```
    
- 27- Object coercion precedence (valueOf vs toString)
    
    ```jsx
    const obj = {
        valueOf() { return 1; },
        toString() { return '2'; }
    };
    console.log(+obj);
    console.log(`${obj}`);
    console.log(obj + '3');
    ```
    
- 28- Array coercion with spread operator
    
    ```jsx
    const arr1 = [1, 2];
    const arr2 = [3, 4];
    console.log(arr1 + arr2);
    console.log([...arr1] + [...arr2]);
    console.log(+[...arr1, ...arr2]);
    ```
    
- 29- Function object coercion
    
    ```jsx
    function fn() {}
    fn.toString = () => '1';
    fn.valueOf = () => 2;
    console.log(fn + 1);
    console.log(`${fn}`);
    console.log(+fn);
    ```
    
- 30-  Array with custom toString
    
    ```jsx
    const arr = ['1', '2', '3'];
    arr.toString = () => '4';
    console.log(+arr);
    console.log([...arr] + []);
    console.log(arr + '5');
    ```
    
- 31- Constructor function without new
    
    ```jsx
    function User() {
        this.name = "John";
    }
    const user = User();
    console.log(user?.name);
    ```
    
- 32- Unreachable code after return
    
    ```jsx
    function greet(name) {
        return `Hello ${name}!`
        console.log("This won't run");
    }
    console.log(greet("John"));
    ```
    
- 33- Duplicate parameter names
    
    ```jsx
    function sum(a, a, c) {
        return a + a + c;
    }
    console.log(sum(1, 2, 3));
    ```
    
- 34-  Automatic semicolon insertion
    
    ```jsx
    function test(x) {
        return 
        {
            value: x
        }
    }
    console.log(test(1));
    ```
    
- 35- Optional chaining returns undefined
    
    ```jsx
    const obj = {
        prop: 'exists'
    };
    console.log(obj.prop1?.prop2);
    ```
    
- 36-  String padding default behavior
    
    ```jsx
    const name = "John";
    console.log(`Hello ${name.padEnd(10)}`);
    ```
    
- 37- Nullish coalescing operator
    
    ```jsx
    console.log(undefined ?? "default");
    console.log(null ?? "default");
    console.log("" ?? "default");
    ```
    
- 38- Increment operator type conversion
    
    ```jsx
    let x = "5";
    let y = 5 ;
    console.log(++x);
    console.log(++y);
    ```
    
- 39- Array Methods Return Values and Mutations
    
    ```jsx
    function arrayMagic(...args) {
        let result = args.push(args.pop());
        result += args.unshift(result);
        return args.push(result);
    }
    
    console.log(arrayMagic(1, 2, 3));  
    console.log(arrayMagic(1));        
    console.log(arrayMagic());  
    ```
    
- 40- Promise + setTimeout + Event Loop
    
    ```jsx
    console.log('start');
    Promise.resolve().then(() => {
        setTimeout(() => {
            console.log('timeout');
        }, 0);
        console.log('promise');
    });
    setTimeout(() => {
        console.log('timeout2');
    }, 0);
    console.log('end');
    ```
    
- 41- Event Loop and closure value capture
    
    ```jsx
    let i = 0;
    setTimeout(() => console.log(i), 0);
    i++;
    ```
    
- 42-  var in loops with setTimeout
    
    ```jsx
    for(var i = 0; i < 3; i++) {
        setTimeout(() => console.log(i), 1000);
    }
    ```
    
- 43- async/await + setTimeout + Promise
    
    ```jsx
    async function foo() {
        console.log(1);
        setTimeout(() => console.log(2), 0);
        await Promise.resolve().then(() => console.log(3));
        console.log(4);
    }
    foo();
    console.log(5);
    ```
    
- 44-  async forEach + Promise resolution
    
    ```jsx
    const arr = [1, 2, 3];
    arr.forEach(async (num) => {
        await new Promise(resolve => 
            setTimeout(resolve, 1000)
        );
        console.log(num);
    });
    console.log('done');
    ```
    
- 45- setInterval + Promise + Closure
    
    ```jsx
    let count = 0;
    const interval = setInterval(() => {
        Promise.resolve().then(() => console.log(++count));
        if(count > 2) clearInterval(interval);
    }, 0);
    ```
    
- 46- Promise reuse + setTimeout + Callback
    
    ```jsx
    const promise = new Promise(resolve => {
        setTimeout(() => resolve('first'), 1000);
    });
    promise.then(console.log);
    promise.then(console.log);
    ```
    
- 47- this context + async/await + Closure
    
    ```jsx
    let obj = {
        async method() {
            let that = this;
            await Promise.resolve();
            return () => {
                console.log(this === that);
            };
        }
    };
    obj.method().then(fn => fn());
    ```
    
- 48- async/await + Variable Mutation + Execution Order
    
    ```jsx
    let x = 0;
    async function increment() {
        x++;
        await Promise.resolve();
        x++;
        return x;
    }
    increment();
    increment();
    console.log(x);
    ```
    
- 49- Error Handling + Event Loop + Multiple Async Operations
    
    ```jsx
    const fn = async () => {
        await Promise.resolve();
        throw new Error('oops');
    };
    fn().catch(console.log);
    setTimeout(() => console.log('timeout'), 0);
    Promise.resolve().then(() => console.log('promise'));
    ```
    
- 50- Custom Promise + async/await + Return Value
    
    ```jsx
    function delay(ms) {
        return new Promise(resolve => setTimeout(resolve, ms));
    }
    async function sequence() {
        console.log(1);
        await delay(1000);
        console.log(2);
        return Promise.resolve(3);
    }
    sequence().then(console.log);
    console.log(4);
    ```
    
- 51- Nested array access with coercion
    
    ```jsx
    console.log([[]][+[]] + []);
    console.log([[]][!+[]] + []);
    console.log([[]] + [![]]);
    ```
    
- 52-  Parallel Promises + Dynamic Timeouts + forEach async
    
    ```jsx
    const array = [1, 2, 3];
    array.forEach(async (num) => {
        await new Promise(r => setTimeout(r, 3 - num));
        console.log(num);
    });
    Promise.resolve().then(() => console.log('done'));
    ```
    
- 53- ALL async Concepts
    
    ```jsx
    console.log('1'); // Sync
    
    setTimeout(() => console.log('2'), 0); // Macro
    
    const promise = new Promise(resolve => {
        console.log('3'); // Sync
        resolve('4');
        console.log('5'); // Sync
    }).then(msg => {
        console.log(msg); // Micro
        Promise.resolve('6').then(msg => console.log(msg)) // Micro
    });
    
    async function test() {
        console.log('7'); // Sync
        await Promise.resolve('8');
        console.log('9'); // Micro
    }
    
    test();
    console.log('10'); // Sync
    ```
    
- 54- ALL Falsy/Truthy Values
    
    ```jsx
    // Part 1: Comparison chains
    console.log(null == undefined > 0);   // Tests: null==undefined, undefined>0
    console.log("" == false == 0);        // Tests: string==boolean==number
    console.log(NaN !== NaN < true);      // Tests: NaN self-comparison, boolean conversion
    
    // Part 2: Mixed operations 
    console.log(+null + "" + false);      // Tests: null to number, string concat
    console.log(!"" + +undefined + []);    // Tests: empty string to boolean, undefined to number
    console.log(typeof NaN + Boolean(0));  // Tests: typeof NaN, explicit boolean conversion
    
    // Part 3: Object conversions
    console.log([null] == "null");        // Tests: array with null to string
    console.log([undefined] == false);     // Tests: array with undefined coercion
    ```
    
- 55- JavaScript Number Boundaries and Special Values
    
    ```jsx
    
    // Part 1: Boundary Comparisons
    console.log(Number.MAX_VALUE + Number.MAX_VALUE);          // Infinity
    console.log(Number.MAX_VALUE > Infinity);                  // false
    console.log(-Number.MAX_VALUE < -Infinity);                // false
    console.log(Number.MIN_VALUE + Number.MIN_VALUE);          // Still positive!
    
    // Part 2: Safe Integer Edge Cases
    console.log(Number.MAX_SAFE_INTEGER + 1 === Number.MAX_SAFE_INTEGER + 2);  // true!
    console.log(Number.MAX_SAFE_INTEGER + 1.1);               // Precision loss
    console.log(Math.pow(2, 53) === Math.pow(2, 53) + 1);     // true, beyond safe
    
    // Part 3: Special Operations
    console.log(Infinity / Infinity);                         // NaN
    console.log(Number.MIN_VALUE / 2);                        // Underflow behavior
    console.log(Number.MAX_VALUE * Number.MIN_VALUE);         // Interesting result
    ```
  
---

## 🚀 Contributing

Want to add your own tricky JavaScript question or debugging challenge? **Contributions are welcome!**

1. Fork the repository
2. Create a new branch (`feature/my-question`)
3. Add your tricky question with an explanation
4. Submit a Pull Request 🚀

---

## 📢 Spread the Word

If you found this repo useful, **give it a ⭐ and share it with others!**\
Happy coding! 🚀🔥

