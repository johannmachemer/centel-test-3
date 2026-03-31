# centel-test-3

A lightweight JavaScript utility library providing math operations, string utilities, and configuration management.

## Modules

### index.js

Core functions for greetings and basic arithmetic.

- `greet(name)` — Returns a greeting string (`"Hello, <name>!"`)
- `add(a, b)` — Returns the sum of two numbers
- `subtract(a, b)` — Returns the difference of two numbers

### math.js

Advanced math functions.

- `multiply(a, b)` — Returns the product of two numbers
- `divide(a, b)` — Returns the quotient (throws on division by zero)
- `factorial(n)` — Returns the factorial of a non-negative integer
- `fibonacci(n)` — Returns the nth Fibonacci number

### utils.js

String manipulation utilities.

- `capitalize(str)` — Capitalizes the first character of a string
- `reverse(str)` — Reverses a string
- `isPalindrome(str)` — Checks if a string is a palindrome (case-insensitive, ignoring non-alpha characters)

### config.js

Configuration management with defaults and validation.

- `defaults` — Default configuration object (`port`, `host`, `debug`, `logLevel`, `maxRetries`, `timeout`)
- `getConfig(overrides)` — Merges overrides into the default configuration
- `validateConfig(config)` — Validates that `port` and `timeout` are non-negative numbers

## Usage

```js
const { greet, add, subtract } = require('./index');
const { multiply, factorial } = require('./math');
const { capitalize, isPalindrome } = require('./utils');
const { getConfig, validateConfig } = require('./config');

greet('World');         // "Hello, World!"
add(2, 3);             // 5
subtract(10, 4);       // 6
multiply(3, 4);        // 12
factorial(5);          // 120
capitalize('hello');   // "Hello"
isPalindrome('racecar'); // true

const config = getConfig({ port: 8080 });
validateConfig(config); // true
```

## Running Tests

```bash
node test.js
```
