# JavaScript Intro/Setup

### JavaScript Intro

JavaScript is a programming language that was built to address the need for interactivity in web sites. It wasn't considered a language for serious development initially, but over the years, as large companies such as Facebook and Google created more complex web applications, JavaScript evolved to meet those needs.

Today it is the most popular programming language, due to the popularity of the internet and the fact that JavaScript is still the only language that can be used within a web browser.

### How Does JavaScript Code Get Executed?

It is not the web browser that runs the JavaScript code, but what is called a JavaScript Engine. The engine is embedded within the web browser, and the web browser passes the JavaScript code to the engine to execute it.

There are several different JavaScript engines and each browser can choose which one they want to use. The Chrome Browser uses the V8 Engine, which is development by Google. Firefox uses one called SpiderMonkey.

![](<.gitbook/assets/image (99).png>)



As interesting development happened in 2009. A developer took the open-source code for Google's V8 JavaScript  Engine and embedded it inside a C++ program he called Node. This allowed developers to create JavaScript applications outside of the web browser for the first time. 

It also opened up the ability to build a full web application, including both the front-end and the back-end completely in one language: JavaScript. This was a huge win for bringing new developers into web development. 

![](<.gitbook/assets/image (100).png>)

### Running JavaScript Code

* [Adding JavaScript to an HTML file](https://shawnr.gitbooks.io/practical-introduction-to-javascript/content/basic-syntax/41-adding-javascript-to-an-html-file.html)
* Running JavaScript from Node.js
* [JavaScript Runtime](javascript/javascript-runtime-environment.md)

### What is Programming?

Solving Problems by manipulating data.

Find the smallest number in a list of integers

#### C

```clike
int find_smallest_int(const int numbers[]) {
  int min = numbers[0];
  for (size_t i = 1; i < numbers.length; i++)
    if (numbers[i] < res)
      min = numbers[i];
  return min;
}
```

#### JavaScript

```javascript

function findSmallestInteger(numbers) {
  let min = numbers[0];
  for(let i = 0; i< numbers.length; i++) {
    min = min < numbers[i] ? min : number[i];
  }
  return min;
}
```

#### Haskell

```haskell
findSmallestInteger :: [Int] -> Int
findSmallestInteger [n] = n
findSmallestInteger (n:ns) = min n (findSmallestInteger)
```

#### Go

```go
func SmallestIntegerFinder(numbers []int) int {
  min := numbers[0]
  for _, value := range numbers {
    if value < min {
      min = value
    }
  }
  return min
```
