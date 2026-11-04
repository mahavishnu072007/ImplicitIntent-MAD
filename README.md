# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
1.Launch the Android application.
2.Create an Implicit Intent object.
3.Specify the required action (ACTION_VIEW, ACTION_DIAL, ACTION_SEND, etc.).
4.Attach the required data using Uri.parse().
5.Invoke startActivity() with the Intent.
6.Android searches for a compatible application.
7.Display the app chooser if multiple apps are available.
8.Launch the selected application.
9.Perform the requested action.

## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: MAHA VISHNU S
Registeration Number :212225220059
*/
```
## MainActivity.java
```
package com.example.implicitintent;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        EditText editText;
        Button button;
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editTextText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="148dp"
        android:layout_height="42dp"
        android:text="Enter Website"
        android:textSize="24sp"
        app:layout_constraintBottom_toTopOf="@+id/editTextText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="284dp"
        android:ems="10"
        android:inputType="text"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="144dp"
        android:text="Navigate"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT

<img width="1430" height="752" alt="image" src="https://github.com/user-attachments/assets/7412cb97-5b0d-4dbc-9f3b-074ff51a670c" />
<img width="1427" height="766" alt="image" src="https://github.com/user-attachments/assets/6f121858-7ccf-4703-a183-a55bbafd4e02" />
<img width="1441" height="735" alt="image" src="https://github.com/user-attachments/assets/edd3d5e6-8b5c-4584-97b4-e4a3dbe9ec7d" />


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


