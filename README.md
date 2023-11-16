
# Ex.No:12 Design an application that draws basic graphical primitives on the screen.


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
Developed by: Rajesh.K
Registeration Number :21222122041
*/
```
# Activity_main.xml:
```
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
            
xmlns:tools="http://schemas.android.com/tools"
            
android:layout_width="match_parent"
            
android:layout_height="match_parent"
            
tools:context=".MainActivity">

<ImageView
    android:id="@+id/imageView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    tools:srcCompat="@tools:sample/avatars" />
```
# MainActivity.java:
package com.example.shapes;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Bitmap;

import android.graphics.Canvas;

import android.graphics.Color;

import android.graphics.Paint;

import android.graphics.drawable.BitmapDrawable;

import android.os.Bundle;

import android.widget.ImageView;

public class MainActivity extends AppCompatActivity {
```
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    try {
        Bitmap bitmap = Bitmap.createBitmap(720, 1280, Bitmap.Config.ARGB_8888);
        ImageView imageView = findViewById(R.id.imageView);
        imageView.setBackground(new BitmapDrawable(getResources(), bitmap));
        Canvas canvas = new Canvas(bitmap);
        Paint paint = new Paint();
        paint.setColor(Color.BLUE);
        paint.setTextSize(50);
        canvas.drawText("Rectangle", 420, 150, paint);
        canvas.drawRect(400, 200, 650, 700, paint);
        canvas.drawText("Circle", 120, 150, paint);
        canvas.drawCircle(200, 350, 150, paint);
        canvas.drawText("Square", 120, 800, paint);
        canvas.drawRect(50, 850, 350, 1150, paint);
        canvas.drawText("Line", 420, 800, paint);
        canvas.drawLine(520, 850, 520, 1150, paint);
    } catch (Exception e) {
        e.printStackTrace();
    }
}
```

## OUTPUT
# ![image](https://github.com/Roselineb/Mobile-Application-Development/assets/128909895/062a38c6-7332-46ec-a626-1fb6d3f9e2ed)
# ![image](https://github.com/Roselineb/Mobile-Application-Development/assets/128909895/c7190c60-21fc-4d5c-af69-efe1814f2961)
# ![image](https://github.com/Roselineb/Mobile-Application-Development/assets/128909895/02ecf263-379e-40b1-badf-4191c0756ced)

## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
