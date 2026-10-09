# Ohm’s Law Calculator

This is my Part A project for EECE 2140. The program takes a voltage and resistance and calculates the current using I = V / R.

## Setup
The program uses C++17. To build and test it, you need Ubuntu or WSL with g++, Git, Bash, and diff installed.

## Input and Output
Enter the voltage in volts first, followed by the resistance in ohms. Separate the numbers with a space.

For example, entering:
```text
12 4
```

gives:
```text
Current: 3 A
```

If either value is not numeric or the resistance is zero or negative, the program prints:
```text
Invalid input
```

## Build and Run
Run these commands in the project folder:
```bash
mkdir -p build
g++ -std=c++17 -Wall -Wextra -pedantic src/main.cpp -o build/app
./build/app
```

Then enter the two numbers.

## Testing
Run:
```bash
bash test.sh
```

The script compiles the program and checks two cases: a normal calculation and a resistance of zero. It uses diff to compare the actual output with the expected output. If both tests pass, it prints “All acceptance tests passed.”

GitHub Actions also runs the tests whenever changes are pushed or a pull request is opened.

## Limitations
The program does one calculation each time it runs. It does not ask for another input after finishing. It uses the default number formatting, ignores extra input after the first two values, and may not handle extremely large numbers correctly.

## Debugging Reflection
Both tests passed when I ran the script locally. The resistance check prevents division by zero. I also learned that the expected output has to match the program’s output exactly, including spaces and capitalization.

## AI Use
I used ChatGPT to clarify questions and directions in the assignment. It also helped me with terminal commands and organizing the README. The program and workflow were based on the provided Part A example, and I ran the tests locally to check the results.bash results