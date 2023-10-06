# Week-2-intermediate-javascript
Week 2
FILE READER 
In JavaScript, the File object represents a file that can be manipulated on the user's local system. The FileReader object provides methods to read the content of a File or a Blob (binary large object) asynchronously, using methods such as readAsText(), readAsDataURL(), and readAsArrayBuffer(). This asynchronous reading is particularly useful when working with large files or performing file operations that could potentially block the main thread, such as reading a file from the user's computer.
File Object:
A File object is created when the user selects a file using an <input type="file"> element in an HTML fo:rm. You can access properties and methods of the File object in JavaScript.
Filereader:
The FileReader object allows you to read the contents of a File or Blob asynchronously. As the reading proceeds, there are events:
loadstart – loading started.
progress – occurs during reading.
load – no errors, reading complete.
abort – abort() called.
error – error has occurred.
loadend – reading finished with either success or failure.
When the reading is finished, we can access the result as:
reader.result is the result (if successful)
reader.error is the error (if failed).
FETCH
fetch() is a modern JavaScript API for making network requests. It provides a more powerful and flexible feature set. fetch() allows you to make HTTP requests and handle responses using promises. It is built into most modern browsers and can be used both in the browser and in Node.js environments
POST REQUESTS
In JavaScript, you can make POST requests using the fetch() function, just as you would with GET requests. However, for POST requests, you need to include additional options in the fetch() call, such as the HTTP method, headers, and the request body.
Day 2
SENDING A SIMPLE FORM
Sending a simple form using JavaScript usually involves capturing data from HTML form fields, processing that data, and sending it to a server for further handling. adding values on a form using javascript
FORM DATA METHODS
In JavaScript, you can interact with form data using various methods and properties provided by the Document Object Model (DOM). Forms are a fundamental part of web applications, allowing users to input and submit data.
Accessing Form Elements:
You can access form elements using document.getElementById.
Getting and Setting Input Values:
You can retrieve or set the values of form input elements using their value property.
Form Submission:
To submit a form programmatically, you can use the submit() method of the form element.
Preventing Default Submission:
You can prevent the default form submission behavior by capturing the form's submit event and using event.preventDefault().
Form Validation:
You can validate form data using JavaScript by checking the input values and providing feedback to the user. You can use the required attribute on form elements for basic validation and implement custom validation logic as needed.
Form Reset:
To reset a form to its initial state, you can use the reset() method of the form element.
Serializing Form Data:
You can serialize form data into a query string using the FormData object and the URLSearchParams API. This is useful when sending data to a server.
SENDING A FORM WITH A FILE
Sending a form with a file using JavaScript typically involves using the FormData object to capture the form data, including the file, and then sending it to the server using an asynchronous method like XMLHttpRequest or the newer fetch API.
SENDING A FORM WITH BLOB DATA
Sending a form with Blob data involves creating a FormData object and appending the Blob data to it before sending it to the server using an asynchronous method such as fetch.
Fetch: download progress
To track the download progress of a file using the Fetch API in JavaScript, you can utilize the response.body property, which is a ReadableStream. By consuming chunks of data from this stream, you can calculate the progress and update a progress bar or display the progress percentage.
FETCH: ABORT
In JavaScript, the abort() method is used with AJAX (Asynchronous JavaScript and XML) requests to cancel the request before it is completed.
When you make an AJAX request using the XMLHttpRequest object or the Fetch API, the request is sent to the server, and the browser waits for the response.
You can abort a fetch request in JavaScript by using the AbortController interface. The AbortController allows you to associate a signal with one or more fetch requests, and then use the associated signal to abort those requests whenever you want.
DAY 3
FETCH: CROSS-ORIGIN REQUESTS
If we make a fetch from an arbitrary web-site, that will probably fail.
The core concept here is origin – a domain/port/protocol triplet.
Cross-origin requests – those sent to another domain (even a subdomain) or protocol or port – require special headers from the remote side. That policy is called “CORS”: Cross-Origin Resource Sharing.
USING FORMS
you can submit to an iframe using data entered in a form, you can GET/POST request to another site, even without networking methods. But as it’s forbidden to access the content of an <iframe>from another site, it wasn’t possible to read the response.
SIMPLE REQUESTS
A simple request is a request that satisfies two conditions: Simple method: GET, POST or HEAD
Performing simple requests in JavaScript can be done using the XMLHttpRequest object or the more modern fetch API. Both methods allow you to make HTTP requests to retrieve data from a server or send data to a server.
CORS FOR SIMPLE REQUESTS
Cross-Origin Resource Sharing (CORS) is a security feature implemented by web browsers that restricts web pages from making requests to a domain different from the one that served the web page. This policy is in place to prevent potential security vulnerabilities like Cross-Site Scripting (XSS) and data theft.
RESPONSE HEADERS
In JavaScript, response headers can be accessed using the `getResponseHeader()` method or the `getAllResponseHeaders()` method of the `XMLHttpRequest` object. 
The `getResponseHeader()` method returns the value of a specific header, identified by its name, for the current response, while the `getAllResponseHeaders()` method returns all the headers as a single string
PATTERNS AND FLAGS
In JavaScript, patterns and flags are often used in regular expressions. Regular expressions are patterns used to match character combinations in strings. Flags, on the other hand, are optional parameters that modify how a regular expression pattern is matched.
USAGE
In JavaScript, patterns and flags are often used with regular expressions. Regular expressions (regex) are patterns that are used to match character combinations in strings. Flags, on the other hand, are optional parameters that modify how a regular expression is interpreted and matched. Flags are specified after the closing slash of the regular expression literal.
FLAGS
Regular expressions may have flags that affect the search.
There are only 6 of them in JavaScript:
i
With this flag the search is case-insensitive: no difference between A and a (see the example below).
g
With this flag the search looks for all matches, without it – only the first one 
m
Multiline mode (covered in the chapter Multiline mode, flag "m").
s
“Dotall” mode, allows . to match newlines (covered in the chapter Character classes).
u
Enables full unicode support. The flag enables correct processing of surrogate pairs. More about that in the chapter  Unicode: flag "u".
y
Sticky mode (covered in the chapter Sticky flag "y", searching at position)
METHODS OF REGEXP AND STRING
In JavaScript, both regular expressions (RegExp objects) and strings (String objects) have methods that allow you to perform various operations. Below, I've outlined some of the most commonly used methods for both RegExp and String objects.

test(str): Tests if the regular expression matches a specified string. Returns true or false.
exec(str): Executes the search for a match in a specified string. Returns an array of information or null if no match is found.
toString(): Returns a string representation of the regular expression.
Methods of String Objects:
match(regexp): Retrieves the matches when matching a string against a regular expression. Returns an array of matches or null if no match is found.
search(regexp): Searches for a match within a string. Returns the index of the first match or -1 if no match is found.
replace(regexp, replacement): Searches for a match within a string and replaces the matched substring with a replacement string.
split(separator): Splits a string into an array of substrings based on a specified separator (which can be a regular expression).
toLowerCase() and toUpperCase(): Convert the string to lowercase or uppercase, respectively.
CHARACTER CLASSES
In JavaScript regular expressions, character classes are used to match a specific set of characters within a string. Character classes are denoted by square brackets [] and allow you to specify a list of characters to match. Here are some common uses of character classes in JavaScript regular expressions:
Matching a Single Character from a Set:
[abc]: Matches any one character a, b, or c.
Negating a Character Class:
[^abc]: Matches any character except a, b, or c
Shorthand Character Classes:
\d: Matches any digit, equivalent to [0-9].
\D: Matches any non-digit character, equivalent to [^0-9].
\w: Matches any word character (alphanumeric character plus underscore), equivalent to [a-zA-Z0-9_].
\W: Matches any non-word character, equivalent to [^a-zA-Z0-9_].
\s: Matches any whitespace character (space, tab, newline), equivalent to [\t\n\f\r\p{Z}].
\S: Matches any non-whitespace character, equivalent to [^\t\n\f\r\p{Z}].
Custom Character Classes:
[aeiou]: Matches any vowel (either a, e, i, o, or u).
Using Quantifiers with Character Classes:
[0-9]{2,4}: Matches 2 to 4 consecutive digits.
WORD BOUNDARY \b
In regular expressions, the word boundary \b is a zero-width assertion that matches the position between a word character (as defined by \w) and a non-word character (as defined by \W). Word characters include letters, digits, and underscores. Word boundaries are useful when you want to search for a whole word, not just a part of it.
Matching Whole Words:
Using Word Boundary with Quantifiers:
Using Word Boundary with Special Characters:
INVERSE CLASSES
In regular expressions, you can create inverse character classes using the ^ (caret) symbol inside square brackets []. When ^ appears as the first character inside square brackets, it negates the character class, meaning it matches any character that is not in the specified set.
Matching Characters Not in a Specific Set:
Using Inverse Character Classes with Shorthand Classes:
Using Inverse Word Boundaries:
SPACES ARE REGULAR CHARACTERS
In JavaScript regular expressions, spaces are indeed treated as regular characters, just like any other character. If you want to match spaces specifically, you include a space character in your regular expression pattern.
