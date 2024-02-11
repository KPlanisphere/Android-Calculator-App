# Android Calculator App

A simple calculator application developed using Android Studio. This project demonstrates the implementation of basic arithmetic operations in an Android app, featuring a user-friendly interface and efficient Kotlin code.

## Features

- Basic arithmetic operations: addition, subtraction, multiplication, and division.
- Clear and backspace functionalities.
- Responsive user interface compatible with various screen sizes.
- Efficient Kotlin implementation for core functionalities.

## Notable Files

### MainActivity.kt

This file contains the main activity code, initializing the user interface and handling user interactions.

```kotlin
package com.example.calculadora

import android.os.Bundle
import androidx.appcompat.app.AppCompatActivity
import kotlinx.android.synthetic.main.activity_main.*

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
        // Set up button click listeners
        // Example for the number button
        button_one.setOnClickListener { appendOnExpression("1", true) }
        
        // More button setup and event listeners...
    }
    
    private fun appendOnExpression(string: String, canClear: Boolean) {
        // Append text to the expression display
    }
}
```

### Calculator.kt

This file contains the logic for performing arithmetic operations.

```kotlin
package com.example.calculadora

class Calculator {
    fun add(a: Double, b: Double): Double {
        return a + b
    }
    
    fun subtract(a: Double, b: Double): Double {
        return a - b
    }
    
    fun multiply(a: Double, b: Double): Double {
        return a * b
    }
    
    fun divide(a: Double, b: Double): Double {
        if (b == 0.0) {
            throw IllegalArgumentException("Cannot divide by zero")
        }
        return a / b
    }
}
```

## Installation

1.  Clone the repository:
    
    ```sh
    git clone https://github.com/KPlanisphere/android-calculator.git
    ```
    
2.  Open the project in Android Studio.
3.  Build and run the application on an emulator or physical device.

## Usage

1.  Launch the application on your Android device.
2.  Use the on-screen buttons to perform arithmetic operations.
3.  Clear or backspace as needed to correct input.