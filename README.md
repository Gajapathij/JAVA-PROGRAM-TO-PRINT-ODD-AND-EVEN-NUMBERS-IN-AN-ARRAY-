# JAVA-PROGRAM-TO-PRINT-ODD-AND-EVEN-NUMBERS-IN-AN-ARRAY-

## AIM:
To print odd and even numbers using Java programming language.

## APPARATUS REQUIRED:

ØComputer ØEclipse IDE

## THEORY:
Java is a high-level, class-based, object-oriented programming language that is designed to have as few implementation dependencies as possible. It is a general-purpose programming language intended to let programmers write once, run anywhere (WORA), meaning that compiled Java code can run on all platforms that support Java without the needto recompile. Java applications are typically compiled to bytecode that can run on any Java virtual machine (JVM) regardless of the underlying computer architecture. The syntax of Java is similar to C and C++, but has fewer low-level facilities than either of them. The Java runtime provides dynamic capabilities (such as reflection and runtime code modification) that are typically not available in traditional compiled languages. As of 2019, Java was one of the most popular programming languages in use according to GitHub particularly for client–server web applications, with a reported 9 million developers.


## PROCEDURE:
1. Launch Eclipse IDE

o Open Eclipse.

o Select a workspace (folder for saving your projects).

2. Create a New Project

o Click File > New > Java Project

o Enter the project name.

o Click Finish.

3. Create a New Class 

o Right-click on your package → New > Class.

o Enter the class name (e.g., Main).

o Check public static void main(String[] args) (for Java).

o Click Finish.

4. Write Your Program

o Eclipse opens the code editor automatically.

o Type or paste your source code.

5. Save the Program

o Press Ctrl + S or click File > Save.

6. Compile and Run the Program

o Click the Run button (green ▶) on the toolbar.

o View output in the Console window.

7. Close Eclipse

o After finishing, click File > Exit to close Eclipse IDE.

## PROGRAM:
MainActivity.java

package com.example.tokendispenser; import android.os.Bundle;

import android.view.View; import android.widget.*;

import androidx.appcompat.app.AppCompatActivity; import java.util.ArrayList;

public class MainActivity extends AppCompatActivity { EditText nameInput;

Button getTokenButton; TextView tokenDisplay; ListView tokenListView; int tokenCount = 0;

ArrayList tokenList; ArrayAdapter adapter; @Override

protected void onCreate(Bundle savedInstanceState) { super.onCreate(savedInstanceState); setContentView(R.layout.activity_main); nameInput = findViewById(R.id.nameInput);

getTokenButton = findViewById(R.id.getTokenButton); tokenDisplay = findViewById(R.id.tokenDisplay); tokenListView = findViewById(R.id.tokenListView); tokenList = new ArrayList<>();

adapter = new ArrayAdapter<>(this, android.R.layout.simple_list_item_1, tokenList); tokenListView.setAdapter(adapter);

getTokenButton.setOnClickListener(new View.OnClickListener() { @Override

public void onClick(View v) {

String name = nameInput.getText().toString().trim(); if (!name.isEmpty()) {

tokenCount++;

String tokenInfo = "Token " + tokenCount + " - " + name; tokenDisplay.setText("Issued: " + tokenInfo); tokenList.add(tokenInfo); adapter.notifyDataSetChanged();

nameInput.setText(""); } else {

Toast.makeText(MainActivity.this, "Please enter a name", Toast.LENGTH_SHORT).show(); }

} });

} }

activity_main.xml

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" android:layout_width="match_parent" android:layout_height="match_parent"

android:orientation="vertical" android:padding="20dp"> <TextView

android:id="@+id/titleText" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="Token Dispenser" android:textSize="24sp" android:textStyle="bold" android:layout_gravity="center" android:paddingBottom="16dp" />

<EditText android:id="@+id/nameInput" android:layout_width="match_parent"

android:layout_height="wrap_content" android:hint="Enter your name" android:inputType="textPersonName" />

## OUTPUT:
<img width="247" height="201" alt="image" src="https://github.com/user-attachments/assets/2edd25d7-c782-458c-a1d5-e5b28c82bd8c" />




## RESULT:
