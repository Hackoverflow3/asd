# Guessing Game using Anonymous Pipes

## Author
- Abhisek Mohapatra
- Stevens email: amohapat1@stevens.edu

## Bugs or Issues
- The server sometimes crashes when the client sends unexpected input.

## Description of Resolved Issue
During testing, I found that if the client sends unexpected input (e.g., non-integer values), the server would crash unexpectedly. This was due to the server not handling invalid input properly, leading to undefined behavior such as buffer overflow or segmentation fault.

To solve this issue, I implemented input validation in both the client and server processes. In the client, I added checks to ensure that only integer inputs are sent to the server. In the server, I added error handling to gracefully handle invalid input from the client, such as displaying an error message and prompting the client for a valid input again.
