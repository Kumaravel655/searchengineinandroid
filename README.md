# Ex.No:6 Build a program to create a first display screen of any search engine using Auto Complete Text View.
## AIM:

To develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as searchengine and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using AutoComplete TextView in activity_main.xml.

Step 6: Display screen of search engine in MainActivity file.

Step 7: Save and run the application.
## PROGRAM:

/*
Program to print the text “display screen of any search engine”.<br>
Developed by: Kumaravel.V <br>
Registeration Number : 212220230027
*/

### activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#77DC79"
    tools:context=".MainActivity">


    <AutoCompleteTextView
        android:id="@+id/autoCompleteTextView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:completionThreshold="1"
        android:text="search"
        android:textColor="#03A9F4"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.106"
        tools:layout_editor_absoluteX="0dp" />

    <TextView
        android:id="@+id/textview1"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:fontFamily="sans-serif-black"
        android:textColor="#9C27B0"
        android:textColorHighlight="#4CAF50"
        android:textColorHint="#03A9F4"
        android:textColorLink="#1EAFE9"
        android:textSize="36sp"
        android:textStyle="italic"
        app:layout_constraintTop_toTopOf="parent"
        tools:layout_editor_absoluteX="-16dp" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

### main activity.java

```java
package com.example.kumaravelex6;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.AutoCompleteTextView;
import android.widget.TextView;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
    AutoCompleteTextView auto;
    String[] words={"Apple ","buffalo","cat","dog","elephant","python","kit","lick","sight","tick","zebraz"};

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        auto = (AutoCompleteTextView) findViewById(R.id.autoCompleteTextView);


        ArrayAdapter adapter = new
                ArrayAdapter(this, android.R.layout.simple_list_item_1, words);

        auto.setAdapter(adapter);
        auto.setThreshold(1);


    }
}

```
## Output:
![Screenshot (17)](https://user-images.githubusercontent.com/75235334/169633628-677668d0-ffbd-46b9-a4d4-de14776354c4.png)
![Screenshot (18)](https://user-images.githubusercontent.com/75235334/169633632-baabe137-d1fb-476f-8539-135ac7143fc5.png)
![Screenshot (19)](https://user-images.githubusercontent.com/75235334/169633637-e4b550a0-3804-4450-a918-371331a995a4.png)

## RESULT
Thus a Simple Android Application develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio is developed and executed successfully.

