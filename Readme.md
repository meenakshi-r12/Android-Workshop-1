## Workshop-1

## Aim:
     Getting two values and Display the result (sumation Value) in the text box using Android Studio

## Algorithm:
```
1.Open Android Studio → New Project → Empty Activity.
2.Open activity_main.xml to design the layout.
3.Add a TextView for the heading (“Workshop 1”).
4.Add another TextView for the subtitle/title (“Addition of Two Numbers”).
5.Add two EditText boxes for number inputs.
6.Add a Button to perform the summation.
7.Add a TextView to display the result.
8.In MainActivity.java, handle the button click → get values → calculate sum → display result.
```
## Program:
```
Program to print the text create your own content providers to get contacts details.
Developed by:Meenakshi.R
Registeration Number :212224220062
```
## activity_main:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:padding="20dp"
    android:gravity="center_horizontal"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#F9F9F9">

    <!-- Heading -->
    <TextView
        android:id="@+id/heading"
        android:text="Workshop 1"
        android:textSize="28sp"
        android:textStyle="bold"
        android:textColor="#000000"
        android:layout_marginBottom="10dp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

    <!-- Display Title -->
    <TextView
        android:id="@+id/title"
        android:text="Addition of Two Numbers"
        android:textSize="18sp"
        android:textStyle="italic"
        android:textColor="#555555"
        android:layout_marginBottom="30dp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

    <!-- First Number Input -->
    <EditText
        android:id="@+id/num1"
        android:hint="Enter First Number"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginBottom="15dp" />

    <!-- Second Number Input -->
    <EditText
        android:id="@+id/num2"
        android:hint="Enter Second Number"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginBottom="25dp" />

    <!-- Button -->
    <Button
        android:id="@+id/btnSum"
        android:text="Calculate Sum"
        android:textSize="16sp"
        android:backgroundTint="#6200EE"
        android:textColor="#FFFFFF"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

    <!-- Result Text Box -->
    <TextView
        android:id="@+id/result"
        android:text="Result will appear here"
        android:textSize="18sp"
        android:textStyle="bold"
        android:textColor="#000000"
        android:layout_marginTop="30dp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

</LinearLayout>
```
## MainActivity.java:
```
package com.example.workshop1;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button btnSum;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Link UI elements
        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        btnSum = findViewById(R.id.btnSum);
        result = findViewById(R.id.result);

        // Button Click Listener
        btnSum.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                // Get the numbers from input boxes
                String n1Str = num1.getText().toString();
                String n2Str = num2.getText().toString();

                if (n1Str.isEmpty() || n2Str.isEmpty()) {
                    result.setText("Please enter both numbers!");
                } else {
                    int n1 = Integer.parseInt(n1Str);
                    int n2 = Integer.parseInt(n2Str);
                    int sum = n1 + n2;
                    result.setText("Sum: " + sum);
                }
            }
        });
    }
}
```
## Output:

<img width="1920" height="1080" alt="Screenshot (169)" src="https://github.com/user-attachments/assets/0aa06722-740a-40b8-a479-c7edbb73e402" />

##  Result:
Thus the Android application takes two numerical inputs from the user and displays their sum in a text box when the "Calculate Sum" button is executed successfully.
