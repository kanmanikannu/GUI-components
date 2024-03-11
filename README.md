# Ex.No: 1 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Set up the project: Create a new Android project in your preferred IDE (Android Studio, IntelliJ IDEA, etc.).

Design the layout: Design the layout of your application using XML in the res/layout directory. Include the GUI components such as TextView for displaying text, and Button for interaction.

Define variables and constants: Define variables to hold the font size, text color, and references to GUI components in your MainActivity.java file.

Initialize GUI components: In the onCreate() method of your MainActivity.java, initialize the GUI components by finding their views using findViewById().

Set click listeners: Set click listeners for the buttons to handle user interactions.

Implement font size functionality: In the click listener for the font size button, increment the font size by a predefined amount and set it to the TextView. If the font size exceeds a certain limit, reset it to the initial value.

Implement color change functionality: In the click listener for the color change button, cycle through a predefined set of colors for the text in the TextView. Update the text color accordingly.

Handle UI updates: After modifying the font size or text color, update the UI by setting the new font size or text color to the TextView.

Testing: Test your application on different devices and screen sizes to ensure proper functionality and user experience.


## PROGRAM:

```
import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{
    int ch=1;
    float font=30;
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t= (TextView) findViewById(R.id.textView);
        Button b1= (Button) findViewById(R.id.button2);
        b1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                t.setTextSize(font);
                font = font + 5;
                if (font == 50)
                    font = 30;
            }
        });
        Button b2= (Button) findViewById(R.id.button3);
        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                switch (ch) {
                    case 1:
                        t.setTextColor(Color.RED);
                        break;
                    case 2:
                        t.setTextColor(Color.GREEN);
                        break;
                    case 3:
                        t.setTextColor(Color.BLUE);
                        break;
                    case 4:
                        t.setTextColor(Color.CYAN);
                        break;
                    case 5:
                        t.setTextColor(Color.YELLOW);
                        break;
                    case 6:
                        t.setTextColor(Color.MAGENTA);
                        break;
                }
                ch++;
                if (ch == 7)
                    ch = 1;
            }
        });
    }
}

## OUTPUT

![Output](https://github.com/kanmanikannu/GUI-components/assets/114866367/8eef67c0-d6fb-48a8-bf7c-fe88205327d1)


## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


