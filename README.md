# Calculator App

A simple and interactive Android application that allows users to perform basic arithmetic operations like addition, subtraction, multiplication, and division. The app features a clean user interface built with Material Design components.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Contributing](#contributing)
- [License](#license)

## Features
- Perform basic arithmetic operations: addition, subtraction, multiplication, and division.
- Clear (C) and All Clear (AC) buttons to manage inputs effectively.
- Support for parentheses to manage order of operations.
- Responsive user interface with a modern design.

## Technologies Used
- Java
- Android SDK
- XML (for layout design)
- Material Design Components


## Usage
Adding Numbers and Operations: Tap on the buttons to input numbers and operations.
Using Clear (C) and All Clear (AC):
C: Deletes the last character.
AC: Clears the entire input.
Evaluating Expressions: Tap the = button to calculate the result of the expression displayed.

## How It Works
The application maintains a string representing the current expression. When a button is pressed, the input is appended to this string. Upon pressing the = button, the expression is evaluated using the Mozilla Rhino JavaScript engine, allowing for complex calculations, including those with parentheses.

The UI is built using XML, and the layout is designed to be user-friendly, ensuring that buttons are easily accessible and clearly labeled.

Important Code Snippets
Button Click Handling:

java
public void onClick(View view) {
    MaterialButton button = (MaterialButton) view;
    String buttonText = button.getText().toString();
    // Logic for handling button clicks
}

Expression Evaluation:
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


## Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue for any suggestions or improvements.

License
This project is licensed under the MIT License. See the LICENSE file for details.

vbnet
Copy code

### Instructions:
- Replace `https://github.com/yourusername/calculator.git` with the actual URL of your GitHub repository.
- Adjust any sections as needed to reflect your project accurately.

Feel free to modify any part of the README to better suit your project's details and requirements!
