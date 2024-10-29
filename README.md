# Calculator App

## Overview

This is a simple calculator application built for Android using Java. The app supports basic arithmetic operations like addition, subtraction, multiplication, and division, as well as the use of brackets for more complex calculations.

## Features

- Basic operations: Addition, subtraction, multiplication, and division.
- Support for parentheses for order of operations.
- Clear (C) and All Clear (AC) buttons for input management.
- Responsive UI built with Android's Material Design components.

## Technologies Used

- Java
- Android SDK
- Material Design Components
- Mozilla Rhino JavaScript Engine for evaluating mathematical expressions

## Code Structure
MainActivity.java: The main logic of the application, handling button clicks and performing calculations.
activity_main.xml: The layout file that defines the UI components of the calculator.
XML Layout
The layout consists of:

## Two TextView components:
solution_tv: Displays the current expression.
result_tv: Displays the result of the evaluated expression.
A LinearLayout that contains the buttons for numbers and operations.
Important Code Snippets
Button Click Handling:

## java
Copy code
public void onClick(View view) {
    MaterialButton button = (MaterialButton) view;
    String buttonText = button.getText().toString();
    // Logic for handling button clicks
}
## Expression Evaluation:

java
Copy code
String getResult(String data) {
    try {
        Context context = Context.enter();
        context.setOptimizationLevel(-1);
        Scriptable scriptable = context.initStandardObjects();
        String finalResult = context.evaluateString(scriptable, data, "Javascript", 1, null).toString();
        return finalResult;
    } catch (Exception e) {
        return "Err";
    }
}
## Getting Started

### Prerequisites

- Android Studio
- Android SDK
- A physical device or emulator to run the application

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   Contributing
## Contributions are welcome! Please feel free to submit a pull request or open an issue for any suggestions or improvements.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

css
Copy code

Feel free to modify any sections to better fit your project details or style!

