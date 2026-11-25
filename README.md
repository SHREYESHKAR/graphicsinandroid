
# Experiment 7: Design an application that draws basic graphical primitives on the screen
## NAME : SHREYESHKAR SEKAR
## REGISTRATION NUMBER : 212224220099


## AIM:

To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “graphical″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Draw basic object details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application that draws basic graphical primitives on the screen.
Developed by: SHREYESHKAR SEKAR
Registeration Number : 212224220099
*/
```
MainActivity.java

```
package com.example.exp7;
import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.graphics.drawable.BitmapDrawable;
import android.os.Bundle;
import android.widget.ImageView;

public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        
        //Creating a Bitmap
        Bitmap bg = Bitmap.createBitmap(720, 1280, Bitmap.Config.ARGB_8888);
        
        //Setting the Bitmap as background for the ImageView
        ImageView i = (ImageView) findViewById(R.id.imageView1);
        i.setBackgroundDrawable(new BitmapDrawable(bg));
        
        //Creating the Canvas Object
        Canvas canvas = new Canvas(bg);
        
        //Creating the Paint Object and set its TextSize
        Paint paint = new Paint();
        paint.setTextSize(50);
        
        //To draw a Circle (Red)
        paint.setColor(Color.RED);
        canvas.drawText("Circle", 120, 150, paint);
        canvas.drawCircle(200, 350, 150, paint);
        
        //To draw a Rectangle (Blue)
        paint.setColor(Color.YELLOW);
        canvas.drawText("Rectangle", 420, 150, paint);
        canvas.drawRect(400, 200, 650, 700, paint);
        
        //To draw a Square (Magenta)
        paint.setColor(Color.GREEN);
        canvas.drawText("Square", 120, 800, paint);
        canvas.drawRect(50, 850, 350, 1150, paint);
        
        //To draw a Line (Cyan)
        paint.setColor(Color.BLACK);
        canvas.drawText("Line", 500, 800, paint);
        canvas.drawLine(520, 850, 520, 1150, paint);
    }
}

```
activity_main.xml

```

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <ImageView
        android:id="@+id/imageView1"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:ignore="ContentDescription"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>

```



## OUTPUT

<img width="1917" height="1026" alt="Screenshot 2026-11-25 085922" src="https://github.com/user-attachments/assets/0df26a30-e201-4b1c-84c0-f32bd05ffed6" />


<img width="410" height="913" alt="image" src="https://github.com/user-attachments/assets/a8260e58-26b8-40fc-b64c-2c8377d4d3ff" />





## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
