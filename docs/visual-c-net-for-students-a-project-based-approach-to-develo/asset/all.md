![](Image00085.jpg)

VISUAL C# .NET

FOR STUDENTS

A Project-Based Approach to Develop Desktop Applications

First Edition

VIVIAN SIAHAAN

Copyright © 2020 BALIGE Publishing

All rights reserved. No part of this book may be reproduced, stored in a retrieval system, or transmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embedded in critical articles or reviews. Every effort has been made in the preparation of this book to ensure the accuracy of the information presented. However, the information contained in this book is sold without warranty, either express or implied. Neither the authors, nor BALIGE Publishing or its dealers and distributors, will be held liable for any damages caused or alleged to have been caused directly or indirectly by this book. BALIGE Publishing has endeavored to provide trademark information about all of the companies and products mentioned in this book by the appropriate use of capitals. However, BALIGE Publishing cannot guarantee the accuracy of this information.

First published: August 2020

Production reference: 05082020

Published by BALIGE Publishing Ltd.

BALIGE, North Sumatera, Indonesia

ABOUT THE AUTHORS

![D:\vivi2.jpg](Image00000.jpg) Vivian Siahaan is a fast-learner who likes to do new things. She was born, raised in Hinalang Bagasan, Balige, on the banks of Lake Toba, and completed high school education from SMAN 1 Balige. She started herself learning Java, Android, JavaScript, CSS, C ++, Python, R, Visual Basic, Visual C #, MATLAB, Mathematica, PHP, JSP, MySQL, SQL Server, Oracle, Access, and other programming languages. She studied programming from scratch, starting with the most basic syntax and logic, by building several simple and applicable GUI applications. Animation and games are fields of programming that are interests that she always wants to develop. Besides studying mathematical logic and programming, the author also has the pleasure of reading novels. Vivian Siahaan has written dozens of ebooks that have been published on Sparta Publisher: Data Structure with Java; Java Programming: Cookbook; C ++ Programming: Cookbook; C Programming For High Schools / Vocational Schools and Students; Java Programming for SMA / SMK; Java Tutorial: GUI, Graphics and Animation; Visual Basic Programming: From A to Z; Java Programming for Animation and Games; C # Programming for SMA / SMK and Students; MATLAB For Students and Researchers; Graphics in JavaScript: Quick Learning Series; JavaScript Image Processing Methods: From A to Z; Java GUI Case Study: AWT & Swing; Basic CSS and JavaScript; PHP / MySQL Programming: Cookbook; Visual Basic: Cookbook; C ++ Programming for High Schools / Vocational Schools and Students; Concepts and Practices of C ++; PHP / MySQL For Students; C # Programming: From A to Z; Visual Basic for SMA / SMK and Students; C # .NET and SQL Server for High School / Vocational School and Students. At the ANDI Yogyakarta publisher, Vivian Siahaan also wrote a number of books including: Python Programming Theory and Practice; Python GUI Programming; Python GUI and Database; Build From Zero School Database Management System In Python / MySQL; Database Management System in Python / MySQL; Python / MySQL For Management Systems of Criminal Track Record Database; Java / MySQL For Management Systems of Criminal Track Records Database; Database and Critptography Using Java / MySQL; Build From Zero School Database Management System With Java / MySQL.

ABOUT THE BOOK

In chapter one, you will learn to know the properties and events of each control in a Windows Visual C# applications. You need to learn and know in order to be more familiar when applying them to some desktop applications in this book.

In chapter two, you will build Throwing Fire program. This program can be played by two human players or human player versus computer. You will use 12 labels, a large control panel, and three control buttons on the form. In the control panel, a smaller panel with two group box controls and a button control are placed. In the first group box, you will use 2 radio buttons; in the second box group, place 4 radio buttons. Next, two timer controls are added to the project. All label controls are used for titles and provide scoring and game information. The large panel (Panel1) is the playing field. Three button controls are used to start / stop a program, set options, and exit the program. One timer control is used to control game animation and another is used to represent the computer's decision process. The second control panel (Panel2) is used to select game options. One group box contains radio buttons which are used to select number of players. A group box contains radio buttons to select the level of difficulty of the game, when playing against a computer. A small button is used to close the options panel. The default properties are set for one-player games with the easiest game difficulty.

In chapter three, you will build Roasted Duck Delivery simulation. In this simulation, a number of decisions are needed. The basic idea is to read the order by incoming telephone and tell the delivery scooter to go to the location of the order. You also need to make sure that you always provide a roasted duck ready to be transported by the delivery scooter. The delivery area is a 20 by 20 square grid. The more roasted duck is sold, the more profit it gets. The panel control on the left side of the form contains the delivery grid. On the upper right are group boxes with two label controls to display the time or hour and sale results. The computer monitor (in a picture box) displays order and delivery status using a list box and label control. Another group box contains a roasting oven when the roasted ducks are displayed using eight picture box controls. Two button controls on the group box control the operation of the oven. Group boxes under the oven show how many ducks are ready to be delivered and how many are in the delivery scooter (a button control is to load the roasted duck into the scooter). The two button controls beneath are used to start/pause the game and to stop the game or exit the game. In the area under the form there are several timers for controlling a number of aspects in the program. The delivery grid consists of 400 label controls on 20 rows (marked with numbers) and 20 columns (marked with letters). Here, you will learn how to place controls on a form (or panel in this case) using code (when the program runs, not when designing the form). This mechanism can save time designing the form.

In chapter four, you will build a Drone Simulation. In this simulation, you control both vertical and horizontal thrusters to maneuver the ride to the landing pad. You will adjust the landing speed so that it is slow enough so that no accident occurs. You build the form in two stages, the first stage creates two option group boxes, and then the second stage uses both those group boxes as landing controls. Two control panels are placed on the left side of the form: one panel for drawing and another panel for the edge. On the right side of the form, place the two group control boxes. In the first group box, five radio buttons and a check box are added. In the second group box, two radio buttons are placed. In the below section of the form, three buttons are added. Finally, one timer control is added. Then in the form, a group box is added overlap panel. Then, 11 label controls are added to the group box. After that, a progress bar is added. Under the bar, two control panels are added, one high panel and one short panel. In the second (short) panel control, two small label controls are added. Underneath, three button controls are placed. Under these three buttons, a label control is added. For each label control, set the AutoSize property to False to be resized and set (temporarily) the BorderStyle property to FixedSingle so that you can see the edges to facilitate the layout process.

In chapter five, you will build Jumper game. In this game, you will move the jumper across the busy road, avoid the tiger, and cross the river with the changing current to get to house safely. You will place four label controls on the top part of the form (set the AutoSize property to False so that it can be resized and the BorderStyle property temporarily becomes FixedSingle so you can see the edges). Then, you use five panel controls below the labels. These panels will be a place for image graphics. Each panel has a width of 16 jumpers or 640 pixels, because one jumper will be given a width of 40 pixels. The first panel will be the jumper house, which will be given a height of 80 pixels. The next panel will become a river, with a height of 120 pixels. The next panel will be a place for tiger, 40 pixels high. Under the snake panel, there is a road panel. This panel will contain three boat lanes. Each boat has a height of 40 pixels, but you will give it a height of 140 pixels (not 120 pixels) to make room for lane markers. The fifth panel is the place where the jumper will begin its journey or leap. This panel will be given a height of 40 pixels. Add the last control panel below the form with three button controls. Then, finally, add four timer controls. Adjust the size of the form so that the panel controls can occupy according to the width of the form.

CONTENT

1 Visual C# Controls .......... . .......................................6

2 Tutorial 1: Throwing Fire .......... . ...............................17

3 Tutorial 2: Roasted Duck Delivery Simulation  ................... . ..79

4 Tutorial 3: Drone Simulation   .................. . .................148

5 Tutorial 4: Jumper   .................. . ...........................238

5 Bibliography   .................. . .................................347

INTRODUCTION

VISUAL C SHARP CONTROLS

In this chapter, you will get to know the properties and events of each control in a Windows Visual C# application. You need to learn and know in order to be more familiar when applying them to some applications in this book.

| 1.1 Form |

Forms are objects where the user interface is designed as shown in Figure 1.1\. The form is also known as a container or loader object, because it contains other controls. A number of controls are placed on the form having BackColor , ForeColor , and Font properties. To change it, you can select the desired control (after it is placed in the form) and change the desired properties. Another feature of this container control is that when Enable property is False , all controls on that form will be deactivated. Likewise, when this container control has a Visible property of False , then all controls on the form become invisible.

Here, a number of properties, methods, and events commonly used for forms will be presented. Recall that the property describes the appearance and value of a control, a method is an action or task performed by a control, and an event occurs when something is done to that control.

Following are the properties of the Form :

Table 1.1 A number of properties of the Form object

| Name | Used to get or set the form name. |
| AcceptButton | Used to get or set button that is clicked on form when user presses the ENTER key. |
| BackColor | Used to get or set the background color of the form. |
| CancelButton | Used to get or set button that is clicked on form when user presses the Esc key. |
| ControlBox | Used to get or set a value that indicates whether a control box is displayed on the caption bar of the form. |
| Enabled | If it is False , all controls on the form will be disabled. |
| Font | Used to get or set font name, size, and style. |
| ForeColor | Used to get or set the color of text or graphics. |
| FormBorderStyle | Used to set form boundaries to be fixed or dynamic. |
| Height | Form height in pixel. |
| Help | Used to get or set a value that indicates whether the Help button needs to be displayed or not. |
| Icon | Used to get or set an icon for a form. |
| Left | Distance from the left of the screen to the left edge of the form, in pixel. |
| MaximizeButton | Used to get or set a value that indicates whether the maximized button is displayed on the caption bar of the form. |
| MinimizeButton | Used to get or set a value that indicates whether the minimized button is displayed on the caption bar of the form. |
| StartPosition | Used to get or set the initial position of the form when the application is run. |
| Text | Used to get or set the form window title. |
| Top | Distance from the top of the screen to the top edge of the form, in pixel. |
| Width | Form width in pixel. |

The general syntax for calling a method is to write the name of the control, a dot, and then the method name. For the methods of the Form object, the name of the form used is this . This is a Visual C# keyword that is used to refer to a form. So, to close a form, you use: this.Close () .

Following are a number of methods defined for the Form object:

Table 1.2 A number of methods from the Form object

| Close | Close the form. |
| Focus | Set the focus on the form. |
| Hide | Hide the form. |
| Refresh | Force the form to be displayed again. |
| Show | Set the Visible property as True . |

Following are a number of Event procedures that are defined for the Form object:

Table 1.3 A number of Event Procedures from the Form object

| Activated | Occurs when the form is activated in the code or by the user. |
| Click | Occurs when the form is clicked by the user. |
| FormClosing | Occurs when the form is closed. |
| DoubleClick | Occurs when the form is double clicked. |
| Load | Occurs when a form is displayed for the first time. |
| Paint | Occurs when a form is reloaded. |

General uses of Form objects:

*   Set the Name and Text properties.
*   Set the StartPosition property, for example, to CenterScreen value.
*   Set the FormBorderStyle property to a certain value such as Fixed3D or Sizable .
*   Write down the initialization code needed in the Load event of the form. To access this event in the code window, double-click on the form.
*   Write the finalization code in the FormClosing event of the form.

| 1.2 Button |

The Button control is probably the most commonly used Visual C# control. This control is used to start, interrupt, or end certain processes. The following will be presented a number of properties, methods, and events for button control.

Table 1.4 A number of properties of the Button object

| Name | Used to get or set a Button object name. |
| BackColor | Used to get or set the background color of the button. |
| Enabled | If it is False , the button becomes visible, but it cannot accept clicks from user. |
| Font | Used to get or set font name, size, and style. |
| ForeColor | Used to get or set the color of text or graphics. |
| Image | Used to get or set the image to be displayed on the button control. |
| Text | Used to get or set the text or string displayed on the button. |
| TextAlign | Used to get or set text alignment on Button control. |

Table 1.5 A number of methods of Button object

| Focus | Used to assign focus to the button. |
| PerformClick | Generates a Click event for a button. |

Table 1.6 The most popular event of Button object

| Click | This event is triggered when the button is selected by clicking on it or by pressing the access key. |

General uses of Button control:

*   Set the Name and Text properties.
*   Write the code in the Click event.
*   You can also change the Font , Backcolor , and Forecolor properties.

| 1.3 Label |

The Label control is used to display text, which the user cannot edit directly. The text on a label can only be changed when the program is run when responding to an event.

The following will be presented a number of properties, methods, and events for label control.

Table 1.7 A number of properties of the Label object

| Name | Used to get or set a Lable object name. |
| AutoSize | Used to get or set a value that indicates whether the label automatically changes size or not. The default value is True . |
| BackColor | Used to get or set background color on label. |
| BorderStyle | Used to get or set edge style for label. |
| Font | Used to get or set the name, style, and size of the font. |
| ForeColor | Used to get or set the color of text or graphics. |
| Text | Used to get or set the string displayed on the label. |
| TextAlign | Used to get or set text alignment on label. |

Note, by default, label control cannot be resized. To do this, set the AutoSize property to False .

Table 1.8 One of methods of Label object

| Refresh | Force an update to the content of a Label control. |

Table 1.9 A number of Event Procedures from the Label object

| Click | Triggered when the user clicks on a label. |
| DblClick | Triggered when the user double clicks on a label. |

Common uses of Label controls:

*   Set the Name and Text properties.
*   Set the Font , BackColor , and ForeColor properties.
*   Set the AutoSize property to False and choose the desired value for TextAlign .

| 1.4 Timer |

The Timer control in Visual C# can generate events without any input from the user. This timer control works behind the scenes on your project, which results in events with the time interval you set. This event generation feature is very helpful when the screen wants to be updated at regular time intervals.

The following will be presented a number of properties and event of the Timer control.

Table 1.10 A number of properties of the Timer object

| Name | Used to get or set a Timer object name. |
| Enabled | Used to enable and disable timer. When the value is True , this timer control continues operations until the Enabled property is False . |
| Interval | Milliseconds (there are 1000 milliseconds in one second) between each Tick event call from the timer control. |

Table 1.11 One of events of Timer object

| Tick | This event procedure is called every interval (milliseconds) when the Enabled property is True . |

To use the Timer control, you add it to your application like other controls. This control will be placed in the area below the form in the design window.

The Enabled property of the timer control is False at design time. You enable a timer in the code by changing this property to True .

Common uses of the Timer control:

*   Set the Name property and the Interval property.
*   Write the code in the Tick event.
*   At some point in your application, set the Enabled property to True to start the timer. You can also make it False to stop the timer.

| 1.5 TextBox |

The TextBox control is used to display information entered at the time of design, by user when the program is run, or by code in the program.

Table 1.12 A number of properties of the TextBox object

| Name | Get or set the name of the text box. |
| AutoSize | Get or set a value that indicates whether the height of the text box automatically adjusts when the font in the control changes. |
| BackColor | Get or set the background color from the text box. |
| BorderStyle | Get or set the edge style of the text box. |
| Font | Get or set font name, style, and size. |
| ForeColor | Get or set the color of text or graphics. |
| HideSelection | Get or set a value that indicates whether the selected text in the text box control is still highlighted when the control loses focus. |
| Lines | Get or set a line of text in a text box control. |
| MaxLength | Get or set the maximum number of characters that a user can type in the text box control. |
| MultiLine | Get or set a value that indicates whether the text box can contain multi-line text. |
| PasswordChar | Get or set character to disguise password characters in a one-line TextBox control. |
| ReadOnly | Get or set a value that indicates whether the text in the text box control is read-only. |
| ScrollBars | Get or set which scroll bars are displayed without the multi-line text box control. |
| SelectedText | Get or set a value that indicates the text being selected. |
| SelectionLength | Get or set how many characters that are selected in the text box. |
| SelectionStart | Get or set the starting point of the selected text in the text box. |
| Tag | Stores a string expression. |
| Text | Get or set the current text in the text box. |
| TextAlign | Get or set text alignment on text box. |
| TextLength | Get the length of the text in the text box. |

Table 1.13 A number of methods of the TextBox object

| AppendText | Append text to currentvtext in the text box. |
| Clear | Clear all text in the text box. |
| Copy | Copy selected text to the clipboard. |
| Cut | Move selected text to the clipboard. |
| Focus | Put the cursor on the specified text box. |
| Paste | Replace the current selection in the text box with the content of the Clipboard. |
| SelectAll | Select all text in the text box. |
| Undo | Cancel the last edit operation of the text box. |

Table 1.14 A number of Events from the TextBox object

| Click | Occurs when the user clicks on the text box. |
| Enter | Occurs when the control receives focus. |
| KeyDown | Occurs when a key is pressed when the control has focus. |
| KeyPress | Occurs when a key is pressed when the control has focus. |
| Leave | Triggered when the user leaves the text box. This is a way to check the content of a text box when editing the text box is done. |
| TextChanged | Occurs when the value of the Text property has changed. |

General uses of the TextBox control as a viewer control:

*   Set the Name property. Initialize the Text property with the desired string.
*   Set the ReadOnly property to True .
*   If used to display text more than one line, set the MultiLine property to True .
*   You can also change the Font , BackColor , and ForeColor properties.

General uses of TextBox control as input device:

*   Set the Name property. Initialize the Text property with the desired string.
*   If used to display text more than one line, set the MultiLine property to True .
*   In the code, give Focus to the control when needed.
*   Provide the key entrapment code for the KeyPress event that will be discussed in this chapter.
*   Read the Text property when the Leave event occurs.
*   You can also change the Font , BackColor , and ForeColor properties.

| 1.6 CheckBox |

Visual C# has many controls that give users many choices just by clicking the mouse. These controls are attractive, familiar, and minimize the possibility of errors in your application. You will use a lot of these controls.

CheckBox control provides a way to provide a selection of a number of potential choices. CheckBox is used in many Windows applications.

Table 1.15 A number of properties of the CheckBox object

| Name | Get or set the name of the check box. |
| BackColor | Get or set the background color from the check box. |
| Checked | Get or set a value indicating whether the check box is checked. |
| Font | Get or set font name, style, and size. |
| ForeColor | Get or set the color of text or graphics. |
| Text | Get or set the string displayed next to the check box. |
| TextAlign | Get or set text alignment in the checkbox. |

Table 1.16 One of methods of CheckBox object

| Focus | Move focus to a specific check box. |

Table 1.17 A number of Events of the CheckBox object

| CheckedChanged | Occurs when the value of the Checked property changes, whether via code or when the check box is clicked. |
| Click | Triggered when a check box is clicked. The Checked property is automatically changed by Visual C#. |

When a check box is clicked, if there is no check mark there ( Checked = False ), then Visual C# will place a check mark there and set Checked property to True . If clicked and previously there was a check mark there ( Checked = True ), then the check mark will disappear and Checked property will be changed to Flase .

General uses of CheckBox control:

*   Set the Name and Text properties.
*   Initialize the Checked property.
*   Monitor the Click or CheckChanged event to determine whether the check box is checked.
*   Change Font , BackColor , and ForeColor properties.

| 1.7 RadioButton |

RadioButton control provides the capability to make mutually exclusive choices from a number of candidate choices. This means that the radio button works as a group, only one button can be selected. The radio button is widely used in Windows applications. Named as a radio button because it looks similar to a button on a transistor radio.

Following are a number of properties, methods, and events of the RadioButton control:

Table 1.18 A number of Properties of the RadioButton object

| Name | Get or set the name of the radio button. |
| BackColor | Get or set the background color from the radio button. |
| Checked | Get or set a value indicating whether the radio button is selected. |
| Font | Get or set font name, style, and size. |
| ForeColor | Get or set the color of text or graphics. |
| TextAlign | Get or set text alignment on radio buttons. |

Table 1.19 A number of Methods of the RadioButton object

| Focus | Move focus to the specified radio button. |
| PerformClick | Generates a Click event for a particular radio button, by simulating a click by the user. |

Table 1.20 A number of Events of the RadioButton object

| CheckedChanged | Occurs when the value of the Checked property changes, whether via a code or when the radio button is clicked. |
| Click | Triggered when a radio button is clicked. The Checked property is automatically changed by Visual C#. |

General uses of RadioButton control:

*   Create a radio button group.
*   For each button in a group, set the Name and Text properties.
*   Initialize the Checked property.
*   Monitor the Click or CheckChanged event on each radio button to determine which radio button is clicked.

| 1.8 GroupBox |

You already knew that check boxes and radio buttons work in a group. The GroupBox control provides a way to group related controls in a Visual C# application.

To place controls in a group box, you first need to drag or place GroupBox control into the form. Then, place each control into the group box.

The group box affects how the radio button works. The radio buttons on a GroupBox control work as a group, and are not related to the radio buttons on other GroupBox controls.

Table 1.21 A number of Properties of the GroupBox object

| Name | Get or set the name of the group box. |
| Enabled | Get or set a value indicating whether the group box is enabled. If it is False , then all controls in the group box will be disabled. |
| BackColor | Get or set the background color from the group box. |
| Font | Get or set font name, style, and size. |
| ForeColor | Get or set color of text. |
| Text | Get or set the string to be displayed in the title section of the group box. |
| Visible | If it is False , it will hide the group box (and all the controls it contains). |

The GroupBox control has a number of methods and events, but all of them are rarely used. You will focus more on the methods and events associated with the controls in the group box.

General uses of GroupBox control:

*   Set Text and Name properties.
*   Place the desired controls in the group box.
*   Monitor the events of each control in the group box.

| 1.9 PictureBox |

Visual C# offers a number of features for graphics. The PictureBox control is one of the main tools in exploiting these features. The picture box control can display graphic files (with various formats) and it can utilize a number of graphic functions and can be used for animation.

Table 1.22 A number of Properties of the PictureBox object

| Name | Get or set the name of the picture box. |
| BackColor | Get or set the background color from the picture box. |
| BorderStyle | Indicate the edge style for the picture box. |
| Height | Heighy of the picture box in pixels. |
| Image | Set the graphic file to display in the picture box. |
| Left | The distance from the left edge of the form to the left edge of the picture box, in pixels. |
| SizeMode | Indicats how the picture is displayed. |
| Top | Lower edge distance from the area of ​​the form title to the top edge of the picture box, in pixels. |
| Width | Width of the picture box in pixels. |

Table 1.23 One of Events of the PictureBox object

| Click | Triggered when a picture box is clicked. |

The Image property specifies the graphic file to be displayed. The five types of graphics files that can be placed in the image box are as follows:

Table 1.24 A number of acceptable graphic file types of PictureBox control

| Bitmap | An image is represented by pixels and stored as a collection that contains bits. This is the format most commonly used by scanner and paintbrush programs. Format has a .bmp extension. |
| Icon | A special type of bitmap file with a maximum size of 32 x 32 pixels. This format has the .ico extension. The icon is used to represent Windows applications. |
| Metafile | A file that stores an image as a collection that contains graphical objects (lines, circles, polygons), not pixels. Metafile has a more accurate resolution than bitmaps when the size is enlarged or reduced. This format has a .wmf extension. |
| JPEG | JPEG (Joint Photographic Experts Group) is a compressed BMP format that supports 8 bits and 24 bit colors. This format is popular on the Internet and is a common format for digital cameras. JPEG format has the extension .jpg. |
| GIF | GIF (Graphic Interchange Format) is a compressed bmp format originally developed by CompuServe. This format supports up to 256 bit colors and is also popular on the Internet. This format has a .gif extension. |

The SizeMode property states how a particular image will be displayed. There are five values ​​that can be given to this property: Normal , CenterImage , StretchImage , AutoSize , and Zoom . The effect of each of these values ​​is as follows:

| Value of SizeMode | Effect |
| Normal | The image is displayed at the initial size. If the picture box is larger than the image, there will be free space. If the picture box is smaller than the image, the image will be truncated. |
| CenterImage | The image is displayed at its initial size, centered on the picture box. If the picture box is larger than the image, there will be free space. If the picture box is smaller than the image, the image will be truncated. |
| StretchImage | The image will 'fill' the picture box. If the image is smaller than the picture box, the image will expand. If the image is larger than the picture box, the image will shrink. |
| AutoSize | The opposite of StretchImage . The picture box will change its dimensions to adjust the initial size of the image. |
| Zoom | Same with StretchImage . The image will adjust so it can be loaded in the picture box. |

Note that the dimensions remain unchanged for the Normal , CenterImage , StretchImage , and Zoom values. With AutoSize , the picture box will change size. This causes problems when the program runs if your form is not large enough to load the picture box.

General uses of the PicureBox control in displaying images:

*   Set the Name and SizeMode properties (often with a StretchImage value).
*   Specifiy the Image property, both at the time of design and when the program runs (run-time).

TUTORIAL 1

THROWING FIRE

In this tutorial, you will build Throwing Fire program. This program can be played by two human players or human player versus computer.

| Description |
| Start Visual C# and open the project and press <F5> to run it, you will see:![](Image00001.jpg)Figure 2.1 Throwing Fire game startsNext, press Options button. Choose One . With one player, you can also choose the level of difficulty of the game, as shown in Figure 2.1.Click OK and then click New Game button. Game will start, as shown in Figure 2.2.The controls of the player are done via the keyboard. Player 1 presses A key to move up, Z key to move down, and S key to throw fire.When you choose Two players from the Options button, this game can be played by two human players. Player 1 presses the same keys, while player 2 presses key K to move up, M to move down, and key J to throw fire, as shown in Figure 2.3.![](Image00002.jpg)Figure 2.2 User chooses one player and hard difficulty level![](Image00003.jpg)Figure 2.3 User play against computer![](Image00004.jpg)Figure 2.4 Human versus human |
| Tutorial Steps |
| Step 1 | You will start building Throwing Fire game project. Start a new project in Visual Basic. Place 12 labels, a large control panel, and three control buttons on the form. In the control panel, place a smaller panel with two group box controls and a button control. In the first group box, place 2 radio buttons; in the second box group, place 4 radio buttons. Add two timer controls to the project. Change the size and position of each control so that the form is now as shown in Figure 2.5.All label controls are used for titles and provide scoring and game information. The large panel ( Panel1 ) is the playing field. Three button controls are used to start / stop a program, set options, and exit the program. One timer control is used to control game animation and another is used to represent the computer's decision process. The second control panel ( Panel2 ) is used to select game options. One group box contains radio buttons which are used to select number of players. A group box contains radio buttons to select the level of difficulty of the game, when playing against a computer. A small button is used to close the options panel. The default properties are set for one-player games with the easiest game difficulty. |
| Step 2 | Set control properties using the Properties window:![](Image00005.jpg)Figure 2.5 All controls user in Throwing Fire game project 

&#124; A number of properties of the Form1 object &#124;
&#124; Name &#124; FormThrowingFire &#124;
&#124; BackColor &#124; Orange &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; KeyPreview &#124; True &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124; Text &#124; Throwing Fire &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label1 object &#124;
&#124; Name &#124; lblPlayer1 &#124;
&#124; Text &#124; You: &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label2 object &#124;
&#124; Text &#124; Hit &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label3 object &#124;
&#124; Name &#124; lblHitPlayer1 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Tex &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label4 object &#124;
&#124; Text &#124; Remaining &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label5 object &#124;
&#124; Name &#124; lblRemPlayer1 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Tex &#124; 20 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label6 object &#124;
&#124; Text &#124; Key A – UpKey Z – DownKey S - Throw &#124;
&#124; Font &#124; Arial Narrow, Size 11 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label7 object &#124;
&#124; Name &#124; lblPlayer2 &#124;
&#124; Text &#124; Computer: &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label8 object &#124;
&#124; Text &#124; Hit &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label9 object &#124;
&#124; Name &#124; lblHitPlayer2 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Tex &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label10 object &#124;
&#124; Text &#124; Remaining &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label11 object &#124;
&#124; Name &#124; lblRemPlayer2 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Tex &#124; 20 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel1 object &#124;
&#124; Name &#124; pnlGame &#124;
&#124; BackColor &#124; Gold &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button1 object &#124;
&#124; Name &#124; btnGame &#124;
&#124; Text &#124; New Game &#124;
&#124; Font Size &#124; 10 &#124;
&#124; TabStop &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button2 object &#124;
&#124; Name &#124; btnOption &#124;
&#124; Text &#124; Option &#124;
&#124; Font Size &#124; 10 &#124;
&#124; TabStop &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button3 object &#124;
&#124; Name &#124; btnExit &#124;
&#124; Text &#124; Exit &#124;
&#124; Font Size &#124; 10 &#124;
&#124; TabStop &#124; False &#124;
&#124;  &#124;  &#124;

&#124; One of properties of the Timer1 object &#124;
&#124; Name &#124; timComputer &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Timer2 object &#124;
&#124; Name &#124; timGame &#124;
&#124; Interval &#124; 50 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel2 object &#124;
&#124; Name &#124; pnlOption &#124;
&#124; BackColor &#124; Light Green &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox1 object &#124;
&#124; Name &#124; grpPlayer &#124;
&#124; Text &#124; Number of Player &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Font Style &#124; Bold &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton1 object &#124;
&#124; Name &#124; rdoOnePlayer &#124;
&#124; Text &#124; One &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton2 object &#124;
&#124; Name &#124; rdoTwoPlayers &#124;
&#124; Text &#124; Two &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox2 object &#124;
&#124; Name &#124; grpDifficulty &#124;
&#124; Text &#124; Difficulty &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Font Style &#124; Bold &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton3 object &#124;
&#124; Name &#124; rdoEasiest &#124;
&#124; Checked &#124; True &#124;
&#124; Text &#124; Easiest &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton4 object &#124;
&#124; Name &#124; rdoEasy &#124;
&#124; Text &#124; Easy &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton5 object &#124;
&#124; Name &#124; rdoHard &#124;
&#124; Text &#124; Hard &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton6 object &#124;
&#124; Name &#124; rdoHardest &#124;
&#124; Text &#124; Hardest &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button4 object &#124;
&#124; Name &#124; btnOK &#124;
&#124; Text &#124; OK &#124;
&#124;  &#124;  &#124;

When finished, the form will look like in the figure below.![](Image00006.jpg)Figure 2.6 Form after properties setting done |
| Step 3 | Run the project (press <F5>), the game is displayed as shwon in Figure 2.7\. You will now start writing project code. You first write the code that sets the status of the game based on the selected game options. |
| Step 4 | When the game starts, user will choose the options (number of players and the difficulty level of the game). Based on these choices, the form will display different information.![](Image00007.jpg)Figure 2.7 The form first startsWhen the user clicks Options button ( btnOption ), the following things occur: 
*   Disable btnGame .
*   Disable btnOption .
*   Disable Exit button.
*   Make pnlOption visible.

The code to implement these steps is placed in the Click event of the btnOption button:

&#124; 1234567 &#124; private void btnOption_Click( object sender, EventArgs e){    btnGame.Enabled = false ;    btnOption.Enabled = false ;    btnExit.Enabled = false ;    pnlOption.Visible = true ;} &#124;

Add this procedure to your project. When the project is run and the user clicks on the Options button, the form will be displayed as shown in Figure 2.8. |
| Step 5 | After the options panel is displayed, the user can choose one or two players and select game difficulty (if playing against computer). You will use an Integer variable named NumberOfPlayer to save number of players and an Integer variable with the name Difficulty to save the selected difficulty level. Add the following two form-level variable declarations to the project: 

&#124; 1 &#124; int NumberOfPlayer, Difficulty; &#124;

![](Image00008.jpg)Figure 2.8 When user clicks Options button |
| Step 6 | Add a Load event of FormThrowingFire to the project to initialize these variables to their default values: 

&#124; 12345 &#124; private void FormThrowingFire_Load( object sender, EventArgs e){    NumberOfPlayer = 1;    Difficulty = 1;} &#124;

 |
| Step 7 | If the one player radio button ( rdoOnePlayer ) is selected, user will play against computer and the following happens: 
*   Set NumberOfPlayer to 1.
*   Set Text property of lblPlayer1 to You: .
*   Set Text property of lblPlayer2 to Computer: .
*   Make lblInstructionPlayer2 control invisible.
*   Enable grpDifficulty .

If the two player ( rdoTwoPlayers ) radio button is selected, the user will play against another human and the following happens:

*   Set NumberOfPlayer to 2.
*   Set Text property of lblPlayer1 to Player 1: .
*   Set Text property of lblPlayer2 to Player 2: .
*   Make lblInstructionPlayer2 control visible.
*   Disable grpDifficulty .

Note that game difficulty levels are only selected when playing against computer (one player).The code to implement these steps is placed into a procedure named rdoPlayer_Click which handles Click events of both rdoOnePlayer and rdoTwoPlayers :

&#124; 1234567891011121314151617181920212223 &#124; private void rdoPlayer_Click( object sender, EventArgs e){    RadioButton ButtonClicked;    ButtonClicked = (RadioButton) sender;    if (ButtonClicked.Text == "One" )    {        NumberOfPlayer = 1;        lblPlayer1.Text = "You:" ;        lblPlayer2.Text = "Computer:" ;        lblInstructionPlayer2.Visible = false ;        grpDifficulty.Enabled = true ;    }    else    {        NumberOfPlayer = 2;        lblPlayer1.Text = "Player 1:" ;        lblPlayer2.Text = "Player 2:" ;        lblInstructionPlayer2.Visible = true ;        grpDifficulty.Enabled = false ;    }} &#124;

Add this procedure to your project. |
| Step 8 | Likewise, a procedure named rdoDifficulty_Click handles the Click event for four radio buttons on grpDifficulty . Based on which button is clicked, the Difficulty variable is set: 

&#124; 123456789101112131415161718192021 &#124; private void rdoDifficulty_Click( object sender, EventArgs e){    RadioButton ButtonClicked;    ButtonClicked = (RadioButton)sender;    switch (ButtonClicked.Text)    {        case "Easiest" :            Difficulty = 1;            break ;        case "Easy" :            Difficulty = 2;            break ;        case "Hard" :            Difficulty = 3;            break ;        case "Hardest" :            Difficulty = 4;            break ;    }} &#124;

Add this procedure to your project.![](Image00009.jpg)Figure 2.9 The game display will appear with default values ​​(one player, easiest difficulty level) |
| Step 9 | After the user selects options he wants, he clicks the OK button ( btnOK ) to close the options panel. The code in the Click event of the btnOK control is the opposite of the code in the Click event of the btnOption : 

&#124; 1234567 &#124; private void btnOK_Click( object sender, EventArgs e){    btnGame.Enabled = true ;    btnOption.Enabled = true ;    btnExit.Enabled = true ;    pnlOption.Visible = false ;} &#124;

Add this procedure to your project. At this point, game can begin. |
| Step 10 | Save and run the project. The game display will appear with default values ​​(one player, easiest difficulty level). Click Options button to bring up the options panel, as shown in Figure 2.9.Changing the level of difficulty will not change the appearance of the form. Changing number of players will change the form display. Select two players, the header information will change and the Difficulty group box will be disabled:![](Image00010.jpg)Figure 2.10 Changing number of players will change the form display |
| Step 11 | The configuration file will contain two pieces of information: number of players ( NumberOfPlayer ) and difficulty level ( Difficulty ). First, you will develop code to write the configuration file when the program ends. This code is placed into the FormClosing event: 

&#124; 12345678 &#124; private void FormThrowingFire_FormClosing( object sender, FormClosingEventArgs e){    StreamWriter FileOutput =        new StreamWriter(Application.StartupPath + "\\fire.ini" );    FileOutput.WriteLine(NumberOfPlayer);    FileOutput.WriteLine(Difficulty);    FileOutput.Close();} &#124;

As always, the configuration file is in bin\Debug folder. Add this procedure to your project. |
| Step 12 | Add this code to the Click event procedure of btnExit , so you can stop the project and write configuration file: 

&#124; 1234 &#124; private void btnExit_Click( object sender, EventArgs e){    this .Close();} &#124;

 |
| Step 13 | The configuration file is opened and read in the Load procedure of the form. Based on the values ​​read, you then simulate clicks on the radio buttons to select options. The hardest part of this procedure is that you can only simulate these clicks if the buttons are visible and enabled. You will do this in this code. The modified Load procedure of the form that opens the configuration file and selects the radio buttons is given below: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637 &#124; private void FormThrowingFire_Load( object sender, EventArgs e){    try    {        StreamReader fileMasukan =            new StreamReader(Application.StartupPath +            "\\bolasalju.ini" );        NumberOfPlayer = Convert. ToInt32(fileMasukan.ReadLine());        Difficulty = Convert.ToInt32(fileMasukan.ReadLine());        fileMasukan.Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;} &#124;

![](Image00011.jpg)Figure 2.11 The project is first displayed with default optionsNote that you use the default values ​​if the configuration file cannot be opened. Also note that you make the form ( this ) and panel ( pnlOption ) appear before selecting options. You choose the difficulty option first, because this option is not enabled if two players are selected. After the option is selected, the Visible property of the panel returnes to False . |
| Step 14 | Save and run the project. The project is first displayed with default options (one player and easiest difficulty level) as shown in Figure 2.11.Choose several options. For example, say you choose the number of players two. Then, click the OK button and the Exit button to stop the project. Run the project again and click the Options button to see that the last selected option is still saved in the form:![](Image00012.jpg)Figure 2.12 The last selected options are saved in the form |
| Step 15 | You will have a number of animated images on this project (players, fire, and shields). This is a good place to test object-oriented programming skills. You will build a class named TwoPlayer to represent the two player objects and its default constructor: 

&#124; 1234567 &#124; class TwoPlayer{    public TwoPlayer ()    {    }} &#124;

You will use three properties to describe a TwoPlayer object: MyImage ( Image data type), Location (type of Rectangle that describes size and location), an IsVisible (Boolean type that tells whether the object is visible or not). Add these declarations to the class file, which initializes IsVisible to False :

&#124; 12345678910 &#124; class TwoPlayer{    public TwoPlayer ()    {    }    public Image MyImage;    public Rectangle Location;    public bool IsVisible = false ;} &#124;

 |
| Step 16 | You will expand the class definition by adding several methods to help with the animation work. Class methods are used so that objects can do certain jobs. The method is written as a Visual Basic procedure. You will write three methods for the TwoPlayer object, one method that places it on a graphical object, one method that moves it to a new location, and another method that removes it. These three methods are added to the class definition just like the general method when added to the form code file. To add a method to the class description, you choose the name and data type of information that will be generated as a return value. In addition, you specify the arguments required by the method.The Place method places a TwoPlayer object into a graphical object named g (passed as argument): 

&#124; 12345 &#124; public void Place(Graphics g){    g.DrawImage( this .MyImage, this .Location);    this .IsVisible = true ;} &#124;

Note the use of the Me keyword to refer to the current object or the calling object. After the object is placed on g , you set IsVisible property to True .The Move method moves a TwoPlayer object to a new location. The arguments needed are g ( Graphics object), bc ( Brush object) to delete the previous location, dx (change in location x), and dy (change in location y):

&#124; 1234567 &#124; public void Move(Graphics g, Brush bc, int dx, int dy){    g.FillRectangle(bc, this .Location);    this .Location.X += dx;    this .Location.Y += dy;    g.DrawImage( this .MyImage, this .Location);} &#124;

The object was deleted first. The location is then updated and the object is redrawn.The Remove method removes a TwoPlayer object from a graphical object (using bc brush):

&#124; 12345 &#124; public void Remove(Graphics g, Brush bc){    g.FillRectangle(bc, this .Location);    this .IsVisible = false ;} &#124;

Add these three methods ( Place , Move , Remove ) to te TwoPlayer class file to create the latest version:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940 &#124; using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;namespace ThrowingFire{    class TwoPlayer    {        public TwoPlayer ()        {        }        public Image MyImage;        public Rectangle Location;        public bool IsVisible = false ;        public void Place(Graphics g)        {            g.DrawImage( this .MyImage, this .Location);            this .IsVisible = true ;        }        public void Move(Graphics g, Brush bc, int dx, int dy)        {            g.FillRectangle(bc, this .Location);            this .Location.X += dx;            this .Location.Y += dy;            g.DrawImage( this .MyImage, this .Location);        }        public void Remove(Graphics g, Brush bc)        {            g.FillRectangle(bc, this .Location);            this .IsVisible = false ;        }    }} &#124;

Using this class, a TwoPlayer object variable can be created using:

&#124; 1 &#124; TwoPlayer MyPlayer &#124;

The variable then is used to reference new TwoPlayer player:

&#124; 1 &#124; MyPlayer = new TwoPlayer() &#124;

Once created, the MyImage property can be specified using Image.FromFile method and the Location property can be assigned a Rectangle structure.TwoPlayer object is placed on a graphical object ( MyImage ) using: MyPlayer.Place (MyImage) . The TwoPlayer object is moved using: MyPlayer.Move(MyImage, MyBrush, dx, dy) , where MyBrush is a solid brush that has the same color as the background color of the graphical object, dx is how far you want to move the object horizontally, and dy is how far you want to move the object vertically. |
| Step 17 | You will now write the code to start and stop the game. You first need to define form-level variables to play and control the game. Return to the code of the form, add declarations to the project: 

&#124; 12345 &#124; Graphics MyGraphics;Brush MyBrush;TwoPlayer Player1, Player2;int Player1Hit, Player2Hit, Player1Rem, Player2Rem;const int FireMax = 20; &#124;

MyGraphics is the region of graphics used to play game and MyBrush will be used to erase images. Two TwoPlayer objects ( Player1 and Player2 ) represent two throwers. Player1Hit and Player2Hit will track how many successful throwing fire for each player. Players1Rem and Players2Rem will track how many throws each player still has. A FireMax constant (you can change it if you like) sets the number of initial pitches each player has. |
| Step 18 | Add code to Load of FormThrowingFire to initialize each of these variables. The modified procedure is given as follows: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152 &#124; private void FormThrowingFire_Load( object sender, EventArgs e){    try    {        StreamReader fileMasukan =            new StreamReader(Application.StartupPath +            "\\bolasalju.ini" );        NumberOfPlayer = Convert. ToInt32(fileMasukan.ReadLine());        Difficulty = Convert.ToInt32(fileMasukan.ReadLine());        fileMasukan.Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;    Player1Rem = FireMax;    Player2Rem = FireMax;    lblRemPlayer1.Text = Player1Rem.ToString();    lblRemPlayer2.Text = Player2Rem.ToString();    // Creates TwoPlayer objects    MyGraphics = pnlGame.CreateGraphics();    MyBrush = new SolidBrush(pnlGame.BackColor);    Player1 = new TwoPlayer();    Player2 = new TwoPlayer();    Player1.MyImage = Image.FromFile(Application.StartupPath +        "\\player1.ico" );    Player2.MyImage = Image.FromFile(Application.StartupPath +        "\\plyer2.ico" );} &#124;

Pay attention to the code to create two TwoPlayer objects and initialize MyImage property. Copy the player1.ico and player2.ico graphic files into bin\Debug folder. |
| Step 19 | At this point, the user can click on New Game ( btnGame ) to start the game. The following steps will be added: 
*   Remove all graphic objects.
*   Change the Text property from btnGame to Stop Game .
*   Disable btnOption .
*   Disable Exit button.
*   Reset Player1Hit and Player2Hit to 0.
*   Reset Player1Rem and Player2Rem to FireMax .
*   Place Player1 and Player2 objects to the starting position (using Place method of TwoPlayer class).

The code for these steps is quite simple. The Player1 object will be centered vertically on pnlGame near the left edge. The Player2 object will be centered vertically on pnlGame near the right edge.The btnGame button is also used to stop the game. When the user clicks btnGame button (when its Text property is Stop Game ), the following things need to be done:

*   Delete Player1 and Player2 objects (using Remove method of TwoPlayer class).
*   Change Text property from btnGame to Start Game .
*   Enable btnOption .
*   Enable Exit button.
*   Display “Game Over” message.

The code for all of these steps is placed in the Click event procedure of btnGame . The code is given as follows:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839 &#124; private void btnGame_Click( object sender, EventArgs e){    if (btnGame.Text == "New Game" )    {        MyGraphics.Clear(pnlGame.BackColor);        btnGame.Text = "Stop Game" ;        btnOption.Enabled = false ;        btnExit.Enabled = false ;        Player1Hit = 0;        Player2Hit = 0;        lblHitPlayer1.Text = "0" ;        lblHitPlayer2.Text = "0" ;        Player1Rem = FireMax;        Player2Rem = FireMax;        lblRemPlayer1.Text = Player1Rem.ToString();        lblRemPlayer2.Text = Player2Rem.ToString();        Player1.Location = new Rectangle(5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player1.MyImage.Height), Player1.MyImage.Width,            Player1.MyImage.Height);        Player2.Location = new Rectangle(pnlGame.ClientSize.Width –            Player2.MyImage.Width - 5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player2.MyImage.Height), Player2.MyImage.Width,            Player2.MyImage.Height);        Player1.Place(MyGraphics);        Player2.Place(MyGraphics);    }    else    {        Player1.Remove(MyGraphics, MyBrush);        Player2.Remove(MyGraphics, MyBrush);        btnGame.Text = "New Game" ;        btnOption.Enabled = true ;        btnExit.Enabled = true ;        MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),            Brushes.Yellow, 280, 160);    }} &#124;

Add this procedure to your project. Positioning “Game Over” message is obtained by trial and error. Save and run project. Click on New Game button and both players will appear as shown in Figure 2.13.Before quit the game, click Stop Game button to make sure the procedure is working properly and “Game Over” message is displayed, as shown in Figure 2.14.At this point, the user has the option to start a new game, change options or exit the program. |
| Step 20 | You need the capability to move player up and down the graphics region. If you choose to use the keyboard to control, use the KeyDown event. This event is the same as the KeyPress event that has been used before, but is more flexible. This event can be used to detect keys that are pressed, along with control keys such as Alt, Ctrl, Shift, cursor control, and other control keys. The form of the KeyDown event procedure of form is: 

&#124; 123 &#124; private void FormThrowingFire_KeyDown( object sender, KeyEventArgs e){} &#124;

![](Image00013.jpg)Figure 2.13 The Player1 object is centered vertically on pnlGame near the left edge and the Player2 object is centered vertically on pnlGame near the right edge.The KeyCode property is a member of the Keys class. There are a number of values ​​for each key that can be pressed. The Intellisense feature of the Visual Basic IDE will provide KeyCode values ​​when needed. KeyDown event generally have a Select Case structure with a Case clause for each possible key (or key combination).In this game, you choose the following keys to control the player's movement and to throw fire (selected from the keyboard):

&#124; Player 1 &#124; A – Up, Z – Down, S – Throw fire &#124;
&#124; Player 2 &#124; K – Up, M – Down, J – Throw fire &#124;

You can change it yourself if you like.![](Image00014.jpg)Figure 2.14 “Game Over” message appear when user clicks Stop Game buttonEach time the movement key is pressed, you will move the player (using Move method of PlayerTwo class) as far as PlayerIncrement (a value that you can change if needed) if you want to move it down and as far as - PlayerIncrement if you want to move it up. Add a form-level constant declaration to this value:

&#124; 1 &#124; const int PlayerIncrement = 5; &#124;

The code to move the player is placed into the KeyDown event procedure of the form:

&#124; 123456789101112131415161718192021222324252627282930313233 &#124; private void FormThrowingFire_KeyDown( object sender, KeyEventArgs e){    if (btnGame.Text == "New Game" )        return ;    switch (e.KeyCode)    {        case Keys.A:            Player1.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player1.Location.Y < 0)                Player1.Location.Y = 0;            break ;        case Keys.Z:            Player1.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player1.Location.Y > pnlGame.ClientSize.Height –                Player1.Location.Height)                Player1.Location.Y = pnlGame.ClientSize.Height –                    Player1.Location.Height;            break ;        case Keys.K:            Player2.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player2.Location.Y < 0)                Player2.Location.Y = 0;            break ;        case Keys.M:            Player2.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player2.Location.Y > pnlGame.ClientSize.Height –                Player2.Location.Height)                Player2.Location.Y = pnlGame.ClientSize.Height –                    Player2.Location.Height;            break ;    }} &#124;

Note that you do not allow KeyDown events to occur if the user has not started a game (that is, if btnGame still says New Game ). Add this procedure to your project.You need to make sure that form always has the focus to intercept the keys to move players. To be sure, add this line: Me.Focus() at the end of the Click procedure on btnGame which is used to start a new game.![](Image00015.jpg)Figure 2.15 Both players now can move up and down. |
| Step 21 | Save and run the project. Select Two option in grpPlayer so you can see whether both players can move. Click New Game . Press A and Z to move player 1 and press K and M to move player 2\. Make sure both players do not move past the upper or lower limit of the control panel as shown in Figure 2.15. |
| Step 22 | In this project, you will give players the ability to throw fire at each other. Fire will be represented by Image object just like player. The only difference here is that when fire is thrown, it moves without user interaction at a predetermined speed and its position is updated by the timer control. And, you need to constantly check if the fire collides with another object. TwoPlayer class does not have properties for speed, or methods that check collisions. So, you need a new class to define fire.You will explain fire using MovingFire class. This class will have a number of properties and methods from TwoPlayer class (using inheritance), plus the speed properties and a method for checking collision. To build this class, you can start from scratch, with all new properties and new methods. Or, you can take advantage of the concept of inheritance in object-oriented programming. Inheritance is a concept where you can build an existing class-based class, by adding its own properties and/or methods. This will save work.You will see how inheritance is used. You will add the collision checking method later. Now, just focus on class properties. Add a class to the project, name it MovinFire . Use the following class code: 

&#124; 123456789 &#124; class MovingFire : TwoPlayer{    public MovingFire ()    {    }    public int XSpeed;    public int YSpeed;} &#124;

This will make all the properties and methods of TwoPlayer class available to the new class ( MovingFire ). Other lines of code add speed properties ( XSpeed , speed in the horizontal direction; YSpeed , speed in the vertical direction). These two properties represent how far the MovingFire will move in a certain direction. |
| Step 23 | Fires are represented by two MovingFire objects ( Fire1 is fire thrown by player 1, while Fire2 is fire thrown by player 2). Horizontal speed is determined by the fire speed constant with zero vertical speed. Add the following level-form declarations to your project: 

&#124; 12 &#124; MovingFire Fire1, Fire2;const int FireSpeed = 20; &#124;

Speed ​​is another parameter that you can change yourself as you like with the value that you think is best. |
| Step 24 | Snowballs are created in the Load procedure from the form. Add the following four lines to the procedure (after the lines of code that specify the TwoPlayer objects): 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061 &#124; private void FormThrowingFire_Load( object sender, EventArgs e){    try    {        StreamReader fileMasukan =            new StreamReader(Application.StartupPath +            "\\bolasalju.ini" );        NumberOfPlayer = Convert. ToInt32(fileMasukan.ReadLine());        Difficulty = Convert.ToInt32(fileMasukan.ReadLine());        fileMasukan.Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;    Player1Rem = FireMax;    Player2Rem = FireMax;    lblRemPlayer1.Text = Player1Rem.ToString();    lblRemPlayer2.Text = Player2Rem.ToString();    // Creates TwoPlayer objects    MyGraphics = pnlGame.CreateGraphics();    MyBrush = new SolidBrush(pnlGame.BackColor);    Player1 = new TwoPlayer();    Player2 = new TwoPlayer();    Player1.MyImage = Image.FromFile(Application.StartupPath +        "\\player1.ico" );    Player2.MyImage = Image.FromFile(Application.StartupPath +        "\\plyer2.ico" );    Fire1 = new MovingFire();    Fire2 = new MovingFire();    Fire1.MyImage = Image.FromFile(Application.StartupPath +        "\\fire1.ico" );    Fire2.MyImage = Image.FromFile(Application.StartupPath +        "\\fire2.ico" );    btnGame.Focus();} &#124;

 |
| Step 25 | Player 1 throws fire by pressing the S key. Player 2 throws fire by pressing the J key. You set a number of rules in throwing the fire. First, you will only allow one fire from each player to be displayed on the screen at a time (no multi pitching). Second, the player cannot throw fire if he runs out of rations. If these conditions are met, when the player throws fire, these steps are carried out: 
*   Decrease the remaining fires.
*   Update the remaining fires.
*   Position the fire to the side of the player (in the right of player 1, in the left of player 2).
*   Place fire snowballs on graphic objects using Place method of TwoPlayer class.

This code for throwing fire is placed in the existing KeyDown event procedure. Here is the modified code:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960 &#124; private void FormThrowingFire_KeyDown( object sender, KeyEventArgs e){    if (btnGame.Text == "New Game" )        return ;    switch (e.KeyCode)    {        case Keys.A:            Player1.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player1.Location.Y < 0)                Player1.Location.Y = 0;            break ;        case Keys.Z:            Player1.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player1.Location.Y > pnlGame.ClientSize.Height –                Player1.Location.Height)                Player1.Location.Y = pnlGame.ClientSize.Height –                    Player1.Location.Height;            break ;        case Keys.S:            if (!Fire1.IsVisible && Player1Rem > 0)            {                Player1Rem--;                lblRemPlayer1.Text = Player1Rem.ToString();                                 Fire1.Location = new                    Rectangle(Player1.Location.X +                     Player1.Location.Width, Player1.Location.Y,                    Fire1.MyImage.Width, Fire1.MyImage.Height);                Fire1.Place(MyGraphics);            }            break ;        case Keys.K:            Player2.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player2.Location.Y < 0)                Player2.Location.Y = 0;            break ;        case Keys.M:            Player2.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player2.Location.Y > pnlGame.ClientSize.Height –                Player2.Location.Height)                Player2.Location.Y = pnlGame.ClientSize.Height –                    Player2.Location.Height;            break ;        case Keys.J:            if (!Fire2.IsVisible && Player2Rem > 0)            {                Player2Rem--;                lblRemPlayer2.Text = Player2Rem.ToString();                Fire2.Location = new                    Rectangle(Player2.Location.X –                    Player2.Location.Width, Player2.Location.Y,                    Fire1.MyImage.Width, Fire1.MyImage.Height);                Fire2.Place(MyGraphics);            }            break ;    }} &#124;

 |
| Step 26 | Save and run the project. Now, after the user presses S key and J key, the two fires are displayed.![](Image00016.jpg)Figure 2.16 The two fires appear when user press J and K keys |
| Step 27 | Once thrown, the movement or displacement of the fire is updated by the timGame control. You need the Click event code of btnGame to enable the timer (when a New Game is clicked) and to stop the timer (when Stop Game is clicked). You also need to clear the fire when the Stop Game is clicked. A modified version of the Click procedure of btnGame is given as follows: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445 &#124; private void btnGame_Click( object sender, EventArgs e){    if (btnGame.Text == "New Game" )    {        MyGraphics.Clear(pnlGame.BackColor);        btnGame.Text = "Stop Game" ;        btnOption.Enabled = false ;        btnExit.Enabled = false ;        Player1Hit = 0;        Player2Hit = 0;        lblHitPlayer1.Text = "0" ;        lblHitPlayer2.Text = "0" ;        Player1Rem = FireMax;        Player2Rem = FireMax;        lblRemPlayer1.Text = Player1Rem.ToString();        lblRemPlayer2.Text = Player2Rem.ToString();        Player1.Location = new Rectangle(5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player1.MyImage.Height), Player1.MyImage.Width,            Player1.MyImage.Height);        Player2.Location = new Rectangle(pnlGame.ClientSize.Width –            Player2.MyImage.Width - 5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player2.MyImage.Height), Player2.MyImage.Width,            Player2.MyImage.Height);        Player1.Place(MyGraphics);        Player2.Place(MyGraphics);        timGame.Enabled = true ;        this .Focus();    }    else    {        timGame.Enabled = false ;        Player1.Remove(MyGraphics, MyBrush);        Player2.Remove(MyGraphics, MyBrush);        Fire1.Remove(MyGraphics, MyBrush);        Fire2.Remove(MyGraphics, MyBrush);        btnGame.Text = "New Game" ;        btnOption.Enabled = true ;        btnExit.Enabled = true ;        MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),            Brushes.Yellow, 280, 160);    }} &#124;

 |
| Step 28 | In the Tick event procedure timGame , you update the position of the fire thrown using the horizontal speed value and Move method. You also check whether fire is past the edge of the panel. If so, you need to delete it from the panel to allow another throw. You also check the end of the game (both players are out of fires and both players are not visible). When the game ends, btnGame button will be clicked: 

&#124; 12345678910111213141516171819202122232425 &#124; private void timGame_Tick( object sender, EventArgs e){    // status of fire thrown by player 1    if (Fire1.IsVisible)    {        Fire1.Move(MyGraphics, MyBrush, FireSpeed, 0);        if (Fire1.Location.X > pnlGame.ClientSize.Width)            // past the edge of the panel            Fire1.Remove(MyGraphics, MyBrush);    }    //status of fire thrown by player 2    if (Fire2.IsVisible)    {        Fire2.Move(MyGraphics, MyBrush, -FireSpeed, 0);        if (Fire2.Location.X < 0)            // past the edge of the panel            Fire2.Remove(MyGraphics, MyBrush);    }    // Checks game status    if (!Fire1.IsVisible && Player1Rem == 0 && !Fire2.IsVisible &&          Player2Rem == 0)        btnGame.PerformClick();} &#124;

Add this procedure to your project. In the code, you select the Interval property of the timer control by 50 milliseconds. This is a parameter that you can change as you like. |
| Step 29 | Save and run project. Make sure you still use the two player option. Click New Game . Click the S and J keys to throw fire. Make sure the labels reflect the exact value of the remaining fires. If fire hits the player, the player's graphics will disappear. To bring it up again press one of the keys that move it up and down the panel, as shown in the figure below.![](Image00017.jpg)Figure 2.17 Both players now throw fire at each other |
| Step 30 | If fire is thrown at or hits a player, another player will get point (a hit). You need a way to check for such collision. Because rectangular region defines moving object here, you need to know what if two rectangular regions intersect. In Visual Basic, this test can be performed using ItersectsWith method of Rectangle structure.To see whether the two rectangular regions ( Rectangular1 and Rectangular2 ) intersect, you need to check the Boolean value of Rectangular1.IntersectsWith (Rectangular2) . If the value is True , then an intersection or collision occurs. If False , then there is no collision.To use it on this project, you will add a method, Collide , to MovingFire class. Open MovingFire.vb file and add the following change: 

&#124; 123456789101112131415161718192021222324 &#124; using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;namespace ThrowingFire{    class MovingFire : TwoPlayer    {        public MovingFire ()        {        }        public int XSpeed;        public int YSpeed;        public bool Collide(Rectangle r)        {            return ( this .Location.IntersectsWith(r));        }    }} &#124;

This method has a rectangular structural argument (r) for checking collision on the MovingFire object.As an example of using this method, you can check whether Fire1 collides with Player2 . The resulting Boolean value: Fire1.Collide(Player2. Location) will be True if a collision occurs. If a collision occurs, you need to clear the fire and update the thrower's score. |
| Step 31 | You check for collision between fire and player in the Click event procedure of timGame . Modified code for checking collision and updating score are given as follows: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637 &#124; private void timGame_Tick( object sender, EventArgs e){    // status of fire thrown by player 1    if (Fire1.IsVisible)    {        Fire1.Move(MyGraphics, MyBrush, FireSpeed, 0);        if (Fire1.Location.X > pnlGame.ClientSize.Width)            // past the edge of the panel            Fire1.Remove(MyGraphics, MyBrush);        else if (Fire1.Collide(Player2.Location))        {            Player1Hit++;            lblHitPlayer1.Text = Player1Hit.ToString();            Fire1.Remove(MyGraphics, MyBrush);        }    }    //status of fire thrown by player 2    if (Fire2.IsVisible)    {        Fire2.Move(MyGraphics, MyBrush, -FireSpeed, 0);        if (Fire2.Location.X < 0)            // past the edge of the panel            Fire2.Remove(MyGraphics, MyBrush);        else if (Fire2.Collide(Player1.Location))        {            Player2Hit++;            lblHitPlayer2.Text = Player2Hit.ToString();            Fire2.Remove(MyGraphics, MyBrush);        }    }    // Checks game status    if (!Fire1.IsVisible && Player1Rem == 0 && !Fire2.IsVisible &&          Player2Rem == 0)        btnGame.PerformClick();} &#124;

 |
| Step 32 | Save and run project. Now if user throws fire and hits another player, the fire will disappear, but the player remains. You can now try it:![](Image00018.jpg)Figure 2.18 User throws fire and hits another player, the fire will disappear, but the player remains. |
| Step 33 | As designed, the players have no protection from fire except for their ability to go up and down. You will change it. You will create two shields roaming the playing field. This shield will stop fire thrown.You will have two shields, each represented by a MovingFire object ( Shield1 and Shield2 ). The movements will be random, with few restrictions. Add the following form level declarations to your form to declare shield objects and random number object: 

&#124; 12 &#124; MovingFire Shield1, Shield2;Random MyRandom = new Random(); &#124;

Shield will follow some rules. Shield1 will only move vertically on the left side of the playing field, while Shield2 will only move vertically on the right side of the playing field. The vertical speed will be random between values ​​1 and 4 (you can change it yourself). Shield can move up and down. If it moves up, it will start from the bottom side of the playing field. If it moves down, it will start from the top side of the playing field. |
| Step 34 | Shield is constructed in the Load procedure of form. Add the following four lines to this Load procedure to specify the creation of the MovingFire objects for two shields: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768 &#124; private void FormThrowingFire_Load( object sender, EventArgs e){    try    {        StreamReader fileMasukan =            new StreamReader(Application.StartupPath +            "\\bolasalju.ini" );        NumberOfPlayer = Convert. ToInt32(fileMasukan.ReadLine());        Difficulty = Convert.ToInt32(fileMasukan.ReadLine());        fileMasukan.Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;    Player1Rem = FireMax;    Player2Rem = FireMax;    lblRemPlayer1.Text = Player1Rem.ToString();    lblRemPlayer2.Text = Player2Rem.ToString();    // Creates TwoPlayer objects    MyGraphics = pnlGame.CreateGraphics();    MyBrush = new SolidBrush(pnlGame.BackColor);    Player1 = new TwoPlayer();    Player2 = new TwoPlayer();    Player1.MyImage = Image.FromFile(Application.StartupPath +        "\\player1.ico" );    Player2.MyImage = Image.FromFile(Application.StartupPath +        "\\plyer2.ico" );    Fire1 = new MovingFire();    Fire2 = new MovingFire();    Fire1.MyImage = Image.FromFile(Application.StartupPath +        "\\fire1.ico" );    Fire2.MyImage = Image.FromFile(Application.StartupPath +        "\\fire2.ico" );    Shield1 = new MovingFire();    Shield2 = new MovingFire();    Shield1.MyImage = Image.FromFile(Application.StartupPath +        "\\shield.ico" );    Shield2.MyImage = Image.FromFile(Application.StartupPath +        "\\shield.ico" );    btnGame.Focus();} &#124;

 |
| Step 35 | Shields are initially placed in the game field when New Game button is clicked. When this happens, the two shields are randomly placed in the vertical restraints of the graphic object. And, both are assigned random speeds. The two shields will be removed when Stop Game button is clicked. The Click procedure of the modified btnGame that does this job is given below: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960 &#124; private void btnGame_Click( object sender, EventArgs e){    if (btnGame.Text == "New Game" )    {        MyGraphics.Clear(pnlGame.BackColor);        btnGame.Text = "Stop Game" ;        btnOption.Enabled = false ;        btnExit.Enabled = false ;        Player1Hit = 0;        Player2Hit = 0;        lblHitPlayer1.Text = "0" ;        lblHitPlayer2.Text = "0" ;        Player1Rem = FireMax;        Player2Rem = FireMax;        lblRemPlayer1.Text = Player1Rem.ToString();        lblRemPlayer2.Text = Player2Rem.ToString();        Player1.Location = new Rectangle(5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player1.MyImage.Height), Player1.MyImage.Width,            Player1.MyImage.Height);        Player2.Location = new Rectangle(pnlGame.ClientSize.Width –            Player2.MyImage.Width - 5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player2.MyImage.Height), Player2.MyImage.Width,            Player2.MyImage.Height);        Player1.Place(MyGraphics);        Player2.Place(MyGraphics);        Shield1.Location = new Rectangle(( int )(0.5 *            pnlGame.ClientSize.Width - Shield1.MyImage.Width),            MyRandom.Next(pnlGame.ClientSize.Height),            Shield1.MyImage.Width, Shield1.MyImage.Height);        Shield2.Location = new Rectangle(( int )(0.5 *            pnlGame.ClientSize.Width),            MyRandom.Next(pnlGame.ClientSize.Height),            Shield2.MyImage.Width, Shield2.MyImage.Height);        Shield1.YSpeed = ShieldSpeed();        Shield2.YSpeed = ShieldSpeed();        Shield1.Place(MyGraphics);        Shield2.Place(MyGraphics);        timGame.Enabled = true ;        this .Focus();    }    else    {        timGame.Enabled = false ;        Player1.Remove(MyGraphics, MyBrush);        Player2.Remove(MyGraphics, MyBrush);        Fire1.Remove(MyGraphics, MyBrush);        Fire2.Remove(MyGraphics, MyBrush);        Shield1.Remove(MyGraphics, MyBrush);        Shield2.Remove(MyGraphics, MyBrush);        btnGame.Text = "New Game" ;        btnOption.Enabled = true ;        btnExit.Enabled = true ;        MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),            Brushes.Yellow, 280, 160);    }} &#124;

Shield1 is placed just to the left of the center of the panel control, while Shield2 is to the right of the center of the panel control.Notice how both shields are randomly positioned vertically. |
| Step 36 | The speed of the shield is assigned using a general function, ShieldSpeed . As mentioned, you choose this value randomly, between 1 and 4\. Speed ​​can be positive (for downward movement) or negative (for upward movement): 

&#124; 1234567891011 &#124; private int ShieldSpeed(){    const int SpeedMin = 1;    const int SpeedMax = 4;    int Speed;    Speed = MyRandom.Next(SpeedMax - SpeedMin + 1) + SpeedMin;    if (MyRandom.Next(2) == 0)        Speed = -Speed;    return (Speed);} &#124;

 |
| Step 37 | The movement of the shield is updated on the Tick event of timGame timer. For each update, for each shield, you need to do these steps: 
*   Move shield using YSpeed ​​property.
*   Check whether shield has come out of the boundary of the game field.
*   If shield goes out of the boundary of the game field, do this: Calculate new speed; If the speed is positive, position shield to the top edge of the playing field so that it can move down; If the speed is negative, position shield to the bottom edge of the playing field so that it can move up;
*   After moving or repositioning the shield, check whether the thrown fire collides with it. If there is a collision, remove the fire from the game field.

The Tick event procedure of the modified timGame control is given as follows:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273747576 &#124; private void timGame_Tick( object sender, EventArgs e){    // Moves shield    Shield1.Move(MyGraphics, MyBrush, 0, Shield1.YSpeed);    if (Shield1.Location.Y < -Shield1.MyImage.Height &#124;&#124;        Shield1.Location.Y > pnlGame.ClientSize.Height)    {        // Recalculates speed        Shield1.YSpeed = ShieldSpeed();        if (Shield1.YSpeed > 0)            Shield1.Location.Y = -Shield1.MyImage.Height;        else            Shield1.Location.Y = pnlGame.ClientSize.Height;    }    Shield2.Move(MyGraphics, MyBrush, 0, Shield2.YSpeed);    if (Shield2.Location.Y < -Shield2.MyImage.Height &#124;&#124;        Shield2.Location.Y > pnlGame.ClientSize.Height)    {        // Recalculates speed        Shield2.YSpeed = ShieldSpeed();        if (Shield2.YSpeed > 0)            Shield2.Location.Y = -Shield2.MyImage.Height;        else            Shield2.Location.Y = pnlGame.ClientSize.Height;    }    // status of fire thrown by player 1    if (Fire1.IsVisible)    {        Fire1.Move(MyGraphics, MyBrush, FireSpeed, 0);        if (Fire1.Location.X > pnlGame.ClientSize.Width)            // past the edge of the panel            Fire1.Remove(MyGraphics, MyBrush);        else if (Fire1.Collide(Player2.Location))        {            Player1Hit++;            lblHitPlayer1.Text = Player1Hit.ToString();            Fire1.Remove(MyGraphics, MyBrush);        }        else if (Fire1.Collide(Shield1.Location) &#124;&#124;            Fire1.Collide(Shield2.Location))        {            Fire1.Remove(MyGraphics, MyBrush);        }    }    //status of fire thrown by player 2    if (Fire2.IsVisible)    {        Fire2.Move(MyGraphics, MyBrush, -FireSpeed, 0);        if (Fire2.Location.X < 0)            // past the edge of the panel            Fire2.Remove(MyGraphics, MyBrush);        else if (Fire2.Collide(Player1.Location))        {            Player2Hit++;            lblHitPlayer2.Text = Player2Hit.ToString();            Fire2.Remove(MyGraphics, MyBrush);        }        else if (Fire2.Collide(Shield1.Location) &#124;&#124;            Fire2.Collide(Shield2.Location))        {            Fire2.Remove(MyGraphics, MyBrush);        }    }    // Checks game status    if (!Fire1.IsVisible && Player1Rem == 0 && !Fire2.IsVisible &&          Player2Rem == 0)        btnGame.PerformClick();} &#124;

 |
| Step 38 | Save and run project. The two shields move up and down and can block fires thrown by players:![](Image00019.jpg)Figure 2.18 The two shields randomly move up and down and can block fires thrown by players |
| Step 39 | By using SoundPlayer class, which is located in the using System.Media namespace, you can add sound to this game.The SoundPlayer class is used to play sound represented by wav file. There are a number of wav files provided in the bin\Debug folder in your project: 

&#124; throw.wav &#124; Sound is played when the fire is thrown. &#124;
&#124; hit.wav &#124; Sound is played when fire hits a shield. &#124;
&#124; ouch.wav &#124; Sound is played when fire hits a player. &#124;
&#124; gameover.wav &#124; Sound is played when the game is over. &#124;

Before playing a sound, a SoundPlayer object needs to be declared using the usual Dim statement:

&#124; 1 &#124; SoundPlayer MySound; &#124;

The object is then constructed using:

&#124; 1 &#124; MySound = new System.Media.SoundPlayer(SoundFile) &#124;

where FileSound is the full path to the wav file that will be played.Sound is loaded into memory using the Load method of SoundPlayer class:

&#124; 1 &#124; MySound.Load() &#124;

You will modify the code to include sounds. Add the following four form-level declarations:

&#124; 1 &#124; SoundPlayer SoundThrow, SoundHit, SoundOuch, SoundGameOver; &#124;

 |
| Step 40 | The code to construct SoundPlayer object (using wav file) is placed in the Load event of the form. You also add code to load (using Load method) the four sounds: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768697071727374757677787980 &#124; private void FormThrowingFire_Load( object sender, EventArgs e){    try    {        StreamReader fileMasukan =            new StreamReader(Application.StartupPath +            "\\bolasalju.ini" );        NumberOfPlayer = Convert. ToInt32(fileMasukan.ReadLine());        Difficulty = Convert.ToInt32(fileMasukan.ReadLine());        fileMasukan.Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;    Player1Rem = FireMax;    Player2Rem = FireMax;    lblRemPlayer1.Text = Player1Rem.ToString();    lblRemPlayer2.Text = Player2Rem.ToString();    // Creates TwoPlayer objects    MyGraphics = pnlGame.CreateGraphics();    MyBrush = new SolidBrush(pnlGame.BackColor);    Player1 = new TwoPlayer();    Player2 = new TwoPlayer();    Player1.MyImage = Image.FromFile(Application.StartupPath +        "\\player1.ico" );    Player2.MyImage = Image.FromFile(Application.StartupPath +        "\\plyer2.ico" );    Fire1 = new MovingFire();    Fire2 = new MovingFire();    Fire1.MyImage = Image.FromFile(Application.StartupPath +        "\\fire1.ico" );    Fire2.MyImage = Image.FromFile(Application.StartupPath +        "\\fire2.ico" );    Shield1 = new MovingFire();    Shield2 = new MovingFire();    Shield1.MyImage = Image.FromFile(Application.StartupPath +        "\\shield.ico" );    Shield2.MyImage = Image.FromFile(Application.StartupPath +        "\\shield.ico" );    SoundThrow = new SoundPlayer(Application.StartupPath +        "\\throw.wav" );    SoundHit = new SoundPlayer(Application.StartupPath +        "\\hit.wav" );    SoundOuch = new SoundPlayer(Application.StartupPath +        "\\ouch.wav" );    SoundGameOver = new SoundPlayer(Application.StartupPath +        "\\gameover.wav" );    SoundThrow.Load();    SoundHit.Load();    SoundOuch.Load();    btnGame.Focus();} &#124;

 |
| Step 41 | SoundThrow will be played when fire is thrown. This occurs in the KeyDown event procedure of the form. The modified code is given the following: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061 &#124; private void FormThrowingFire_KeyDown( object sender, KeyEventArgs e){    if (btnGame.Text == "New Game" )        return ;    switch (e.KeyCode)    {        case Keys.A:            Player1.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player1.Location.Y < 0)                Player1.Location.Y = 0;            break ;        case Keys.Z:            Player1.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player1.Location.Y > pnlGame.ClientSize.Height –                Player1.Location.Height)                Player1.Location.Y = pnlGame.ClientSize.Height –                    Player1.Location.Height;            break ;        case Keys.S:            if (!Fire1.IsVisible && Player1Rem > 0)            {                SoundThrow.Play();                Player1Rem--;                lblRemPlayer1.Text = Player1Rem.ToString();                                 Fire1.Location = new                    Rectangle(Player1.Location.X +                     Player1.Location.Width, Player1.Location.Y,                    Fire1.MyImage.Width, Fire1.MyImage.Height);                Fire1.Place(MyGraphics);            }            break ;        case Keys.K:            Player2.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player2.Location.Y < 0)                Player2.Location.Y = 0;            break ;        case Keys.M:            Player2.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player2.Location.Y > pnlGame.ClientSize.Height –                Player2.Location.Height)                Player2.Location.Y = pnlGame.ClientSize.Height –                    Player2.Location.Height;            break ;        case Keys.J:            if (!Fire2.IsVisible && Player2Rem > 0)            {                SoundThrow.Play();                Player2Rem--;                lblRemPlayer2.Text = Player2Rem.ToString();                Fire2.Location = new                    Rectangle(Player2.Location.X –                    Player2.Location.Width, Player2.Location.Y,                    Fire1.MyImage.Width, Fire1.MyImage.Height);                Fire2.Place(MyGraphics);            }            break ;    }} &#124;

 |
| Step 42 | SoundHit will be played when a shield is hit by fire throw. SoundOuch will be played when a player is hit by fire throw and SoundGameOver will be played when both players run out of fires. All this happened at the Tick event of timGame timer: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273747576777879808182 &#124; private void timGame_Tick( object sender, EventArgs e){    // Moves shield    Shield1.Move(MyGraphics, MyBrush, 0, Shield1.YSpeed);    if (Shield1.Location.Y < -Shield1.MyImage.Height &#124;&#124;        Shield1.Location.Y > pnlGame.ClientSize.Height)    {        // Recalculates speed        Shield1.YSpeed = ShieldSpeed();        if (Shield1.YSpeed > 0)            Shield1.Location.Y = -Shield1.MyImage.Height;        else            Shield1.Location.Y = pnlGame.ClientSize.Height;    }    Shield2.Move(MyGraphics, MyBrush, 0, Shield2.YSpeed);    if (Shield2.Location.Y < -Shield2.MyImage.Height &#124;&#124;        Shield2.Location.Y > pnlGame.ClientSize.Height)    {        // Recalculates speed        Shield2.YSpeed = ShieldSpeed();        if (Shield2.YSpeed > 0)            Shield2.Location.Y = -Shield2.MyImage.Height;        else            Shield2.Location.Y = pnlGame.ClientSize.Height;    }    // status of fire thrown by player 1    if (Fire1.IsVisible)    {        Fire1.Move(MyGraphics, MyBrush, FireSpeed, 0);        if (Fire1.Location.X > pnlGame.ClientSize.Width)            // past the edge of the panel            Fire1.Remove(MyGraphics, MyBrush);        else if (Fire1.Collide(Player2.Location))        {            SoundOuch.Play();            Player1Hit++;            lblHitPlayer1.Text = Player1Hit.ToString();            Fire1.Remove(MyGraphics, MyBrush);        }        else if (Fire1.Collide(Shield1.Location) &#124;&#124;            Fire1.Collide(Shield2.Location))        {            SoundHit.Play();            Fire1.Remove(MyGraphics, MyBrush);        }    }    //status of fire thrown by player 2    if (Fire2.IsVisible)    {        Fire2.Move(MyGraphics, MyBrush, -FireSpeed, 0);        if (Fire2.Location.X < 0)            // past the edge of the panel            Fire2.Remove(MyGraphics, MyBrush);        else if (Fire2.Collide(Player1.Location))        {            SoundOuch.Play();            Player2Hit++;            lblHitPlayer2.Text = Player2Hit.ToString();            Fire2.Remove(MyGraphics, MyBrush);        }        else if (Fire2.Collide(Shield1.Location) &#124;&#124;            Fire2.Collide(Shield2.Location))        {            SoundHit.Play();            Fire2.Remove(MyGraphics, MyBrush);        }    }    // Checks game status    if (!Fire1.IsVisible && Player1Rem == 0 && !Fire2.IsVisible &&          Player2Rem == 0)        SoundGameOver.PlaySync();        btnGame.PerformClick();} &#124;

 |
| Step 43 | Save and run project. Play the two player game. You can now listen to the sounds of throwing, hitting and ouch. And, play until the fire is zero for both players so that the gameover sound is played. |
| Step 44 | You certainly can't always find a partner to play the game. So why not if computer becomes your opponent? In the one player option, this game can make a computer as player 2.For such computer control, you need to develop rules to be used by computer as opponent. There are two approaches that can be taken in writing code for computer opponent. You can use simple logic, which makes it very easy for human to win game. Or, you can write code with very detailed logic, which can defeat the human brain. With detailed logic, it will be harder for human to win the match. In this game, you will take both approaches. You first develop simple logic by playing a random game. Then, you use the difficulty level selected using the Options button to determine how often you use random logic versus how often you use detailed logic. The selected values ​​are as follows: 

&#124; Difficulty Level &#124; Simple Logic (%) &#124; Detailed logic (%) &#124;
&#124; Easiest &#124; 100 &#124; 0 &#124;
&#124; Easy &#124; 75 &#124; 25 &#124;
&#124; Hard &#124; 50 &#124; 50 &#124;
&#124; Hardest &#124; 25 &#124; 75 &#124;

So, when the Easiest level is selected, you use 100 percent simple logic during the game. When the Hardest level is selected, you use 75 percent of detailed logic (you can't possibly make the computer too smart, because human will always lose) and 25 percent of simple logic. The movement of the computer will be controlled by a separate timer control ( timComputer ). For easier games, you will create a greater value for the Interval property for this timer. This will slow down the computer process. The interval values ​​selected here:

&#124; Difficulty Level &#124; Interval &#124;
&#124; Easiest &#124; 1000 &#124;
&#124; Easy &#124; 750 &#124;
&#124; Hard &#124; 500 &#124;
&#124; Hardest &#124; 250 &#124;

So at the Difficult difficulty level, the computer moves four times more often than when the Easiest difficulty level is selected.You will use Integer variable ( RandComputer ) to represent a percentage of the simple logic time used and an Integer variable ( TimeComputer ) to represent the Interval property of the timer control. Add the following form level declarations to the project:

&#124; 1 &#124; int RandComputer, TimeComputer; &#124;

The value ​​for these two new variables are set in the Click event procedure of the rdoDifficulty . The modified procedure is given as follows:

&#124; 123456789101112131415161718192021222324252627282930 &#124; private void rdoDifficulty_Click( object sender, EventArgs e){    RadioButton ButtonClicked;    ButtonClicked = (RadioButton)sender;    switch (ButtonClicked.Text)    {        case "Easiest" :            Difficulty = 1;            RandComputer = 100;            TimeComputer = 1000;            break ;        case "Easy" :            Difficulty = 2;            RandComputer = 75;            TimeComputer = 750;            break ;        case "Hard" :            Difficulty = 3;            RandComputer = 50;            TimeComputer = 500;            break ;        case "Hardest" :            Difficulty = 4;            RandComputer = 25;            TimeComputer = 250;            break ;    }    timComputer.Interval = TimeComputer;} &#124;

 |
| Step 45 | You need to start the computer timer control ( timComputer ) when playing one-player games. And, you need to stop it when you finish playing. This is done in the Click event of btnGame : 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566 &#124; private void btnGame_Click( object sender, EventArgs e){    if (btnGame.Text == "New Game" )    {        MyGraphics.Clear(pnlGame.BackColor);        btnGame.Text = "Stop Game" ;        btnOption.Enabled = false ;        btnExit.Enabled = false ;        Player1Hit = 0;        Player2Hit = 0;        lblHitPlayer1.Text = "0" ;        lblHitPlayer2.Text = "0" ;        Player1Rem = FireMax;        Player2Rem = FireMax;        lblRemPlayer1.Text = Player1Rem.ToString();        lblRemPlayer2.Text = Player2Rem.ToString();        Player1.Location = new Rectangle(5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player1.MyImage.Height), Player1.MyImage.Width,            Player1.MyImage.Height);        Player2.Location = new Rectangle(pnlGame.ClientSize.Width –            Player2.MyImage.Width - 5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player2.MyImage.Height), Player2.MyImage.Width,            Player2.MyImage.Height);        Player1.Place(MyGraphics);        Player2.Place(MyGraphics);        Shield1.Location = new Rectangle(( int )(0.5 *            pnlGame.ClientSize.Width - Shield1.MyImage.Width),            MyRandom.Next(pnlGame.ClientSize.Height),            Shield1.MyImage.Width, Shield1.MyImage.Height);        Shield2.Location = new Rectangle(( int )(0.5 *            pnlGame.ClientSize.Width),            MyRandom.Next(pnlGame.ClientSize.Height),            Shield2.MyImage.Width, Shield2.MyImage.Height);        Shield1.YSpeed = ShieldSpeed();        Shield2.YSpeed = ShieldSpeed();        Shield1.Place(MyGraphics);        Shield2.Place(MyGraphics);        timGame.Enabled = true ;        if (NumberOfPlayer == 1)            timComputer.Enabled = true ;        this .Focus();    }    else    {        timGame.Enabled = false ;        timComputer.Enabled = false ;        Player1.Remove(MyGraphics, MyBrush);        Player2.Remove(MyGraphics, MyBrush);        Fire1.Remove(MyGraphics, MyBrush);        Fire2.Remove(MyGraphics, MyBrush);        Shield1.Remove(MyGraphics, MyBrush);        Shield2.Remove(MyGraphics, MyBrush);        btnGame.Text = "New Game" ;        btnOption.Enabled = true ;        btnExit.Enabled = true ;        MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),            Brushes.Yellow, 280, 160);    }} &#124;

 |
| Step 46 | Now, you will write down the rules of the computer game. You will start with a simple random rule. In this rule, the computer will only move up and down in the game field, and occasionally throw fire. The only non-random element added is that the computer can only throw fire if it has at least as many fires as the player has. This is to prevent the computer from throwing all the fires and becoming an easy target for human. The rules used are: 
*   Generate a random value from 0 to 4.
*   If the random value is 0, throw fire, if computer has at least as many as the remaining fires owned by the player.
*   If the random value is 1 or 2, move up.
*   If the random value is 3 or 4, make down.

With this rule, fires are thrown one by one in five up or down movements. The computer will move up 2 movements of 5 movements and move down 2 movements from 5 movements.In detailed (smart) logic game rules, you only need to think about how you want to win the game. The smart rule is to throw if other players are "within a certain range". And, avoid human player if he throws fire. In the rules given here, "in range" means that the vertical difference between two players is not more than 80 percent of the player's height:

*   If it is "in range" and the computer has at least as many fires as the player has, the computer will throw fire.
*   If the human player throws fire or the computer no longer has the remaining fires, the computer will make a defensive move: If human player is above the computer player, the computer will move down; If the human player is below the computer player, the computer will move up.
*   Otherwise, the computer will make an attacking move: If the human player is above the computer player, the computer will move up; If the human player is under the computer player, the computer will move down.

Note that the computer can only throw fire when it has at least as many fires left as the player has. You certainly don't want a computer to run out of fires before a human player.The code for both of these logic is placed in the Tick event procedure of timComputer control. Before writing this code, you need to overcome the problem of how you make computer player throw, move up, or move down. With human as the second player, pressing J key will make player 2 throw, K key pressing will make player 2 move up and pressing M key will make player 2 move down. It would be better if there was a way to make the computer press the same key for the job.Fortunately, Visual Basic has a procedure named SendKeys that can be used to simulate key presses on the keyboard. To press J key, the code is: SendKeys.Send("K") . Therefore, for computer player, you will use SendKeys procedure to implement computer actions.The Tick event procedure of timComputer control which implements computer player logic is given as follows:

&#124; 1234567891011121314151617181920212223242526272829303132333435363738 &#124; private void timComputer_Tick( object sender, EventArgs e){    int i;    if (MyRandom.Next(100) < RandComputer)    {        i = MyRandom.Next(5); // Moves randomly        if (i == 0)        {            if (Player2Rem >= Player1Rem)                SendKeys.Send( "J" ); // Throws fire        }        else if (i <= 2)            SendKeys.Send( "K" ); // Moves up        else            SendKeys.Send( "M" ); // Moves down    }    else    {        if (Math.Abs(Player1.Location.Y - Player2.Location.Y) <            ( int )(0.8 * Player1.MyImage.Height) && Player2Rem >=            Player1Rem)            SendKeys.Send( "J" ); // Throws fire        if (Fire1.IsVisible &#124;&#124; Player2Rem == 0)        {            if (Player1.Location.Y - Player2.Location.Y < 0)                SendKeys.Send( "M" ); // Moves up            else                SendKeys.Send( "K" ); // Moves down        }        else        {            if (Player1.Location.Y - Player2.Location.Y < 0)                SendKeys.Send( "K" ); // Moves up            else                SendKeys.Send( "M" ); // Moves down        }    }} &#124;

 |
| Step 47 | Save and run project. Click Options button, choose one player. Then, choose one level of difficulty. Click OK , then New Game . Now your opponent is a computer. |
|  |  |

| TwoPlayer.cs |
| 12345678910111213141516171819202122232425262728293031323334353637383940 | using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;namespace ThrowingFire{    class TwoPlayer    {        public TwoPlayer ()        {        }        public Image MyImage;        public Rectangle Location;        public bool IsVisible = false ;        public void Place(Graphics g)        {            g.DrawImage( this .MyImage, this .Location);            this .IsVisible = true ;        }        public void Move(Graphics g, Brush bc, int dx, int dy)        {            g.FillRectangle(bc, this .Location);            this .Location.X += dx;            this .Location.Y += dy;            g.DrawImage( this .MyImage, this .Location);        }        public void Remove(Graphics g, Brush bc)        {            g.FillRectangle(bc, this .Location);            this .IsVisible = false ;        }    }} |
|  |  |

| MovingFire.cs |
| 12345678910111213141516171819202122232425 | using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;namespace ThrowingFire{    class MovingFire : TwoPlayer    {        public MovingFire ()        {        }        public int XSpeed;        public int YSpeed;        public bool Collide(Rectangle r)        {            return ( this .Location.IntersectsWith(r));        }    }} |
|  |  |

| FormThrowingFire.cs |
| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197198199200201202203204205206207208209210211212213214215216217218219220221222223224225226227228229230231232234235236237238239240241242243244245246247248249250251252253254255256257258259260261262263264265266267268269270271272273274275276277278279280281282283284285286287288289290291292293294295296297298299300301302303304305306307308309310311312313314315316317318319320321322323324325326327328329330331332333334335336337338339340341342343344345346347348349350351352353354355356357358359360361362363364365366367368369370371372373374375376377378379380381382383384385386387388389390391392393394395396397398399400401402403404405406407408409410411412413414415416417418419420421422423424425426427428429430431432433434435436437438439440441442443444445446447448448450451452453454455456457458459460461462463464465466467468469470 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;using System.IO;using System.Media;namespace ThrowingFire{    public partial class FormThrowingFire : Form    {        int NumberOfPlayer, Difficulty;        Graphics MyGraphics;        Brush MyBrush;        TwoPlayer Player1, Player2;        int Player1Hit, Player2Hit, Player1Rem, Player2Rem;        const int FireMax = 20;        const int PlayerIncrement = 5;        MovingFire Fire1, Fire2;        const int FireSpeed = 20;        MovingFire Shield1, Shield2;        Random MyRandom = new Random();        SoundPlayer MySound;        SoundPlayer SoundThrow, SoundHit, SoundOuch, SoundGameOver;        int RandComputer, TimeComputer;        public FormThrowingFire ()        {            InitializeComponent();        }        private void btnOption_Click( object sender, EventArgs e)        {            btnGame.Enabled = false ;            btnOption.Enabled = false ;            btnExit.Enabled = false ;            pnlOption.Visible = true ;            lblInstructionPlayer2.Visible = false ;        }        private void FormThrowingFire_Load( object sender, EventArgs e)        {            try            {                StreamReader fileMasukan = new                    StreamReader(Application.StartupPath + "\\fire.ini" );                NumberOfPlayer = Convert.ToInt32(fileMasukan.ReadLine());                Difficulty = Convert.ToInt32(fileMasukan.ReadLine());                fileMasukan.Close();            }            catch            {                NumberOfPlayer = 1;                Difficulty = 1;            }            // Makes form visible so options can be clicked            this .Show();            pnlOption.Visible = true ;            if (Difficulty == 1)                rdoEasiest.PerformClick();            else if (Difficulty == 2)                rdoEasy.PerformClick();            else if (Difficulty == 3)                rdoHard.PerformClick();            else                rdoHardest.PerformClick();            if (NumberOfPlayer == 1)                rdoOnePlayer.PerformClick();            else                rdoTwoPlayers.PerformClick();            pnlOption.Visible = false ;            Player1Rem = FireMax;            Player2Rem = FireMax;            lblRemPlayer1.Text = Player1Rem.ToString();            lblRemPlayer2.Text = Player2Rem.ToString();            // Menciptakan objek-objek DuaPemain            MyGraphics = pnlGame.CreateGraphics();            MyBrush = new SolidBrush(pnlGame.BackColor);            Player1 = new TwoPlayer();            Player2 = new TwoPlayer();            Player1.MyImage = Image.FromFile(Application.StartupPath +                "\\player1.ico" );            Player2.MyImage = Image.FromFile(Application.StartupPath +                "\\player2.ico" );            Fire1 = new MovingFire();            Fire2 = new MovingFire();            Fire1.MyImage = Image.FromFile(Application.StartupPath +                "\\fire1.ico" );            Fire2.MyImage = Image.FromFile(Application.StartupPath +                "\\fire2.ico" );            Shield1 = new MovingFire();            Shield2 = new MovingFire();            Shield1.MyImage = Image.FromFile(Application.StartupPath +                "\\shield.ico" );            Shield2.MyImage = Image.FromFile(Application.StartupPath +                "\\shield.ico" );            SoundThrow = new SoundPlayer(Application.StartupPath +                "\\throw.wav" );            SoundHit = new SoundPlayer(Application.StartupPath + "\\hit.wav" );            SoundOuch = new SoundPlayer(Application.StartupPath + "\\ouch.wav" );            SoundGameOver = new SoundPlayer(Application.StartupPath +                "\\gameover.wav" );            SoundThrow.Load();            SoundHit.Load();            SoundOuch.Load();            btnGame.Focus();        }        private void rdoPlayer_Click( object sender, EventArgs e)        {            RadioButton ButtonClicked;            ButtonClicked = (RadioButton) sender;            if (ButtonClicked.Text == "One" )            {                NumberOfPlayer = 1;                lblPlayer1.Text = "You:" ;                lblPlayer2.Text = "Computer:" ;                lblInstructionPlayer2.Visible = false ;                grpDifficulty.Enabled = true ;            }            else            {                NumberOfPlayer = 2;                lblPlayer1.Text = "Player 1:" ;                lblPlayer2.Text = "Player 2:" ;                lblInstructionPlayer2.Visible = true ;                grpDifficulty.Enabled = false ;            }        }        private void rdoDifficulty_Click( object sender, EventArgs e)        {            RadioButton ButtonClicked;            ButtonClicked = (RadioButton)sender;            switch (ButtonClicked.Text)            {                case "Easiest" :                    Difficulty = 1;                    RandComputer = 100;                    TimeComputer = 1000;                    break ;                case "Easy" :                    Difficulty = 2;                    RandComputer = 75;                    TimeComputer = 750;                    break ;                case "Hard" :                    Difficulty = 3;                    RandComputer = 50;                    TimeComputer = 500;                    break ;                case "Hardest" :                    Difficulty = 4;                    RandComputer = 25;                    TimeComputer = 250;                    break ;            }            timComputer.Interval = TimeComputer;        }        private void btnOK_Click( object sender, EventArgs e)        {            btnGame.Enabled = true ;            btnOption.Enabled = true ;            btnExit.Enabled = true ;            pnlOption.Visible = false ;        }        private void FormThrowingFire_FormClosing( object sender,        FormClosingEventArgs e)        {            StreamWriter FileOutput = new StreamWriter(Application.StartupPath +                "\\fire.ini" );            FileOutput.WriteLine(NumberOfPlayer);            FileOutput.WriteLine(Difficulty);            FileOutput.Close();        }        private void btnExit_Click( object sender, EventArgs e)        {            this .Close();        }        private void btnGame_Click( object sender, EventArgs e)        {            if (btnGame.Text == "New Game" )            {                MyGraphics.Clear(pnlGame.BackColor);                btnGame.Text = "Stop Game" ;                btnOption.Enabled = false ;                btnExit.Enabled = false ;                Player1Hit = 0;                Player2Hit = 0;                lblHitPlayer1.Text = "0" ;                lblHitPlayer2.Text = "0" ;                Player1Rem = FireMax;                Player2Rem = FireMax;                lblRemPlayer1.Text = Player1Rem.ToString();                lblRemPlayer2.Text = Player2Rem.ToString();                Player1.Location = new Rectangle(5, ( int )(0.5 *                    pnlGame.ClientSize.Height - 0.5 * Player1.MyImage.Height),                    Player1.MyImage.Width, Player1.MyImage.Height);                Player2.Location = new Rectangle(pnlGame.ClientSize.Width –                    Player2.MyImage.Width - 5, ( int )(0.5 *                    pnlGame.ClientSize.Height - 0.5 * Player2.MyImage.Height),                    Player2.MyImage.Width, Player2.MyImage.Height);                Player1.Place(MyGraphics);                Player2.Place(MyGraphics);                Shield1.Location = new Rectangle(( int )(0.5 *                    pnlGame.ClientSize.Width - Shield1.MyImage.Width),                    MyRandom.Next(pnlGame.ClientSize.Height),                    Shield1.MyImage.Width, Shield1.MyImage.Height);                Shield2.Location = new Rectangle(( int )(0.5 *                    pnlGame.ClientSize.Width),                    MyRandom.Next(pnlGame.ClientSize.Height),                    Shield2.MyImage.Width, Shield2.MyImage.Height);                Shield1.YSpeed = ShieldSpeed();                Shield2.YSpeed = ShieldSpeed();                Shield1.Place(MyGraphics);                Shield2.Place(MyGraphics);                timGame.Enabled = true ;                if (NumberOfPlayer == 1)                    timComputer.Enabled = true ;                this .Focus();            }            else            {                timComputer.Enabled = false ;                timGame.Enabled = false ;                Player1.Remove(MyGraphics, MyBrush);                Player2.Remove(MyGraphics, MyBrush);                Fire1.Remove(MyGraphics, MyBrush);                Fire2.Remove(MyGraphics, MyBrush);                Shield1.Remove(MyGraphics, MyBrush);                Shield2.Remove(MyGraphics, MyBrush);                btnGame.Text = "New Game" ;                btnOption.Enabled = true ;                btnExit.Enabled = true ;                MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),                    Brushes.Yellow, 280, 160);            }        }        private int ShieldSpeed()        {            const int SpeedMin = 1;            const int SpeedMax = 4;            int Speed;            Speed = MyRandom.Next(SpeedMax - SpeedMin + 1) + SpeedMin;            if (MyRandom.Next(2) == 0)                Speed = -Speed;            return (Speed);        }        private void FormThrowingFire_KeyDown( object sender, KeyEventArgs e)        {            if (btnGame.Text == "New Game" )                return ;            switch (e.KeyCode)            {                case Keys.A:                    Player1.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);                    if (Player1.Location.Y < 0)                        Player1.Location.Y = 0;                    break ;                case Keys.Z:                    Player1.Move(MyGraphics, MyBrush, 0, PlayerIncrement);                    if (Player1.Location.Y > pnlGame.ClientSize.Height –                            Player1.Location.Height)                        Player1.Location.Y = pnlGame.ClientSize.Height –                            Player1.Location.Height;                    break ;                case Keys.S:                    if (!Fire1.IsVisible && Player1Rem > 0)                    {                        SoundThrow.Play();                        Player1Rem--;                        lblRemPlayer1.Text = Player1Rem.ToString();                        Fire1.Location = new Rectangle(Player1.Location.X +                            Player1.Location.Width, Player1.Location.Y,                            Fire1.MyImage.Width, Fire1.MyImage.Height);                        Fire1.Place(MyGraphics);                    }                    break ;                case Keys.K:                    Player2.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);                    if (Player2.Location.Y < 0)                        Player2.Location.Y = 0;                    break ;                case Keys.M:                    Player2.Move(MyGraphics, MyBrush, 0, PlayerIncrement);                    if (Player2.Location.Y > pnlGame.ClientSize.Height –                           Player2.Location.Height)                        Player2.Location.Y = pnlGame.ClientSize.Height –                           Player2.Location.Height;                    break ;                case Keys.J:                    if (!Fire2.IsVisible && Player2Rem > 0)                    {                        SoundThrow.Play();                        Player2Rem--;                        lblRemPlayer2.Text = Player2Rem.ToString();                        Fire2.Location = new Rectangle(Player2.Location.X –                            Player2.Location.Width, Player2.Location.Y,                            Fire1.MyImage.Width, Fire1.MyImage.Height);                        Fire2.Place(MyGraphics);                    }                    break ;            }        }        private void timGame_Tick( object sender, EventArgs e)        {            // Moves shield            Shield1.Move(MyGraphics, MyBrush, 0, Shield1.YSpeed);            if (Shield1.Location.Y < -Shield1.MyImage.Height &#124;&#124;                Shield1.Location.Y > pnlGame.ClientSize.Height)            {                // Recalculates speed                Shield1.YSpeed = ShieldSpeed();                if (Shield1.YSpeed > 0)                    Shield1.Location.Y = -Shield1.MyImage.Height;                else                    Shield1.Location.Y = pnlGame.ClientSize.Height;            }            Shield2.Move(MyGraphics, MyBrush, 0, Shield2.YSpeed);            if (Shield2.Location.Y < -Shield2.MyImage.Height &#124;&#124;                Shield2.Location.Y > pnlGame.ClientSize.Height)            {                // Recalculates speed                Shield2.YSpeed = ShieldSpeed();                if (Shield2.YSpeed > 0)                    Shield2.Location.Y = -Shield2.MyImage.Height;                else                    Shield2.Location.Y = pnlGame.ClientSize.Height;            }            // status of fire thrown by player 1            if (Fire1.IsVisible)            {                Fire1.Move(MyGraphics, MyBrush, FireSpeed, 0);                if (Fire1.Location.X > pnlGame.ClientSize.Width)                    // past the edge of the panel                    Fire1.Remove(MyGraphics, MyBrush);                else if (Fire1.Collide(Player2.Location))                {                    SoundOuch.Play();                    Player1Hit++;                    lblHitPlayer1.Text = Player1Hit.ToString();                    Fire1.Remove(MyGraphics, MyBrush);                }                else if (Fire1.Collide(Shield1.Location) &#124;&#124;                    Fire1.Collide(Shield2.Location))                {                    SoundHit.Play();                    Fire1.Remove(MyGraphics, MyBrush);                }            }            //status of fire thrown fby player 2            if (Fire2.IsVisible)            {                Fire2.Move(MyGraphics, MyBrush, -FireSpeed, 0);                if (Fire2.Location.X < 0)                    // past the edge of the panel                    Fire2.Remove(MyGraphics, MyBrush);                else if (Fire2.Collide(Player1.Location))                {                    SoundOuch.Play();                    Player2Hit++;                    lblHitPlayer2.Text = Player2Hit.ToString();                    Fire2.Remove(MyGraphics, MyBrush);                }                else if (Fire2.Collide(Shield1.Location) &#124;&#124;                    Fire2.Collide(Shield2.Location))                {                    SoundHit.Play();                    Fire2.Remove(MyGraphics, MyBrush);                }            }            // Checks game status            if (!Fire1.IsVisible && Player1Rem == 0 && !Fire2.IsVisible &&                Player2Rem == 0)            {                SoundGameOver.PlaySync();                btnGame.PerformClick();            }        }        private void timComputer_Tick( object sender, EventArgs e)        {            int i;            if (MyRandom.Next(100) < RandComputer)            {                i = MyRandom.Next(5); // Moves randomly                if (i == 0)                {                    if (Player2Rem >= Player1Rem)                        SendKeys.Send( "J" ); // Throws fire                }                else if (i <= 2)                    SendKeys.Send( "K" ); // Moves up                else                    SendKeys.Send( "M" ); // Moves down            }            else            {                if (Math.Abs(Player1.Location.Y - Player2.Location.Y) <                   ( int )(0.8 * Player1. MyImage.Height) && Player2Rem >= Player1Rem)                    SendKeys.Send( "J" ); // Throws fire                if (Fire1.IsVisible &#124;&#124; Player2Rem == 0)                {                    if (Player1.Location.Y - Player2.Location.Y < 0)                        SendKeys.Send( "M" ); // Moves up                    else                        SendKeys.Send( "K" ); // Moves down                }                else                {                    if (Player1.Location.Y - Player2.Location.Y < 0)                        SendKeys.Send( "K" ); // Moves up                    else                        SendKeys.Send( "M" ); // Moves down                }            }        }    }} |
|  |  |

TUTORIAL 2

ROASTED DUCK DELIVERY SIMULATION

In this tutorial, you will build Roasted Duck Delivery simulation. In this simulation, a number of decisions are needed. The basic idea is to read the order by incoming telephone and tell the delivery scooter to go to the location of the order. You also need to make sure that you always provide a roasted duck ready to be transported by the delivery scooter. The delivery area is a 20 by 20 square grid. The more roasted duck is sold, the more profit it gets.

| Description |
| The panel control on the left side of the form contains the delivery grid. On the upper right are group boxes with two label controls to display the time or hour and sale results. The computer monitor (in a picture box) displays order and delivery status using a list box and label control. Another group box contains a roasting oven when the roasted ducks are displayed using eight picture box controls. Two button controls on the group box control the operation of the oven. Group boxes under the oven show how many ducks are ready to be delivered and how many are in the delivery scooter (a button control is to load the roasted duck into the scooter). The two button controls beneath are used to start/pause the game and to stop the game or exit the game. In the area under the form there are several timers for controlling a number of aspects in the program.The delivery grid consists of 400 label controls on 20 rows (marked with numbers) and 20 columns (marked with letters). Here, you will learn how to place controls on a form (or panel in this case) using code (when the program runs, not when designing the form). This mechanism can save time designing the form.Before running the program, we will explain how to operate it first. You sell and send roasted duck from 6:00 to 11:00\. The time in the upper right corner shows the time. The actual game does not use the actual 5 hours in a single game, but only 15 minutes because the timer parameter adjustment has been made. The order window on the monitor shows what time the order came in, delivery coordinates, and the number of roasted ducks ordered. Orders are also displayed on the delivery grid.In the message on the monitor, you are notified of the current location of the delivery scooter on the delivery grid. At the start of the program, the scooter is in the restaurant (marked with the X symbol on the grid). The group boxes below tell you how many roasted ducks are being burned in the oven and how many are in the delivery scooter. To load a roasted duck into scooter, you need to click Load button. To tell the scooter to move to the delivery location, you click on a specific location on the delivery grid. The scooter will depart for the requested position. When it arrives, the scooter will make a sound and notify the results of the delivery. There are four possible outcomes of delivery: (1) on-time delivery, (2) delayed delivery, (3) insufficient roasted ducks in the scooter to be delivered, or (4) no ordering of roasted ducks at a given location. If you successfully deliver, number of sales will be updated.   ![](Image00020.jpg)Figure 3.1 All controls used in Roasted Duck Delivery simulationYou also need to control the roasting oven to make sure there are always roasted ducks available to be delivered. To roast ducks, click Put Into Oven button for each duck you want to roast. When the oven is filled, click on Roast Duck button. You will be notified when the duck will finish roasting. When finished roasting, the sound will play and the roasted ducks are moved to the available area. The Roasted group box always shows how many roasted ducks are available to be loaded into the delivery scooter. You can pause the program by clicking Pause Game button. To start the game again, click on Start Again . To stop the program before 11:00, click on the Stop Game button. After the program has stopped, sales reports will be reported on the sales results form.Run the project (press <F5>). Then, click on Start Game button. Wait a second, the phone will ring signaling the entry of roasted duck orders from a specific grid location. In this example, order comes from grid location N 15 at 6:04. You can see the random position of the duck restaurant at R 3:![](Image00021.jpg)Figure 3.2 Order comes from grid location N 15 at 6:04You can press Load button to load the available roasted duck (initial value of 8) into the delivery scooter. Then, click on the delivery location (in this example, N 15), as shown in Figure 3.3.While waiting for the delivery scooter to arrive at the delivery location, you need to prepare the duck to be roasted in the combustion oven by clicking Put Into Oven button (several clicks as needed, in this case, 8 roasted ducks are put into the oven). Then click Roast Duck :In Figure 3.4, it can be seen that the delivery scooter has arrived at the delivery location (N 15). In a few moments, other orders also comes and scooter departs for another delivery location.![](Image00022.jpg)Figure 3.3 While waiting for the delivery scooter to arrive at the delivery location, user need to prepare the duck to be roasted in the combustion oven![](Image00023.jpg)Figure 3.4 The delivery scooter has arrived at the delivery location (N 15). In a few moments, other orders also comes and scooter departs for another delivery location |
| Tutorial Steps |
| Step 1 | You will start to build Roasted Duck Delivery simulation project. This form will contain a delivery grid, monitor delivery status, oven and vehicle controls. Start a new project in Visual C#. Once created, it is recommended that you immediately save it with the name you choose. That way, folders and file structures will be created.Just like the previous projects, the form used on this project is quite large. Place a panel control on the left side of the form. The panel is a square with dimensions of 500 x 500 pixels. On the right side, add 2 group boxes at the top (each with a label control) and a picture box below the two group boxes. Place a list box control and a label control in the picture box. Place the other group box under the picture box control. In this group box, place 8 square picture control boxes (to display grilled fish) and two button controls.![](Image00024.jpg)Figure 3.5 All controls used and their sizes and positions on the formThen, add two more group boxes and two button controls. Add labels to the two group boxes and to the second group box, add a button control. For all label controls, set the AutoSize property to False so resizing can be done and set (temporarily) the BorderStyle property to FixedSingle so you can see the edges of the label. Add two small picture box controls under the two button controls (this cannot be seen when the project is run). Finally, add four timer controls to the form. These four timer controls will be in the area below the form, as shown in Figure 3.5.The control panel contains the delivery grid. The first two group boxes with labels display time and sales. The picture box control (with list and label boxes) displays order and scooter status. The third group box (with picture boxes and two buttons) displays and controls the roasting of ducks in the oven. The fourth group box displays the number of ducks that were roasted. The last group box is used to load roasted duck into the scooter. The last buttons (one to start and pause the game and one more button to stop and exit the project). Timer controls are used to control hour, order time, oven, and scooter. |
| Step 2 | Set the following property on each control using the Properties window: 

&#124; A number of properties of the Form1 object &#124;
&#124; Name &#124; FormDuckDelivery &#124;
&#124; Text &#124; Roasted Duck Delivery &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel1 object &#124;
&#124; Name &#124; pnlGrid &#124;
&#124; BackColor &#124; DarkOrange &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Width &#124; 500 &#124;
&#124; Height &#124; 500 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox1 object &#124;
&#124; Name &#124; grpTime &#124;
&#124; BackColor &#124; Orange &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; Text &#124; Time &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label1 object &#124;
&#124; Name &#124; lblTime &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; ForeColor &#124; White &#124;
&#124; Font Size &#124; 16 &#124;
&#124; Text &#124; 6:00 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox2 object &#124;
&#124; Name &#124; grpSale &#124;
&#124; BackColor &#124; DarkOrange &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; Text &#124; Sale &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label2 object &#124;
&#124; Name &#124; lblSale &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; ForeColor &#124; White &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; Rp. 0.0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox1 object &#124;
&#124; Name &#124; picOrder &#124;
&#124; Image &#124; monitor.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the ListBox1 object &#124;
&#124; Name &#124; lstOrder &#124;
&#124; Font &#124; Courier New, 11 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label3 object &#124;
&#124; Name &#124; lblOrder &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; YellowGreen &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; [Empty] &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox3 object &#124;
&#124; Name &#124; grpOven &#124;
&#124; BackColor &#124; Blue &#124;
&#124; ForeColor &#124; DeepPink &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; Text &#124; Roasting Oven &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox2 object &#124;
&#124; Name &#124; picDuck1 &#124;
&#124; Image &#124; duck.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox3 object &#124;
&#124; Name &#124; picDuck2 &#124;
&#124; Image &#124; duck.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox4 object &#124;
&#124; Name &#124; picDuck3 &#124;
&#124; Image &#124; duck.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox5 object &#124;
&#124; Name &#124; picDuck4 &#124;
&#124; Image &#124; duck.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox6 object &#124;
&#124; Name &#124; picDuck5 &#124;
&#124; Image &#124; duck.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox7 object &#124;
&#124; Name &#124; picDuck6 &#124;
&#124; Image &#124; duck.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox8 object &#124;
&#124; Name &#124; picDuck7 &#124;
&#124; Image &#124; duck.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox9 object &#124;
&#124; Name &#124; picDuck8 &#124;
&#124; Image &#124; duck.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button1 object &#124;
&#124; Name &#124; btnPutIntoOven &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Put Into Oven &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button2 object &#124;
&#124; Name &#124; btnRoastDuck &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Roast Duck &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox4 object &#124;
&#124; Name &#124; grpRoast &#124;
&#124; BackColor &#124; DeepPink &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; Text &#124; Roasted &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label4 object &#124;
&#124; Name &#124; lblDuckReady &#124;
&#124; AutoSize &#124; False &#124;
&#124; ForeColor &#124; White &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 16 &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox5 object &#124;
&#124; Name &#124; grpScooter &#124;
&#124; BackColor &#124; DeepPink &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; Text &#124; Ducks In Scooter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label5 object &#124;
&#124; Name &#124; lblInScooter &#124;
&#124; AutoSize &#124; False &#124;
&#124; ForeColor &#124; White &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 16 &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button3 object &#124;
&#124; Name &#124; btnLoadScooter &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Load &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button4 object &#124;
&#124; Name &#124; btnStartPause &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Start Game &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button5 object &#124;
&#124; Name &#124; btnExitStop &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Exit &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox10 object &#124;
&#124; Name &#124; picHScooter &#124;
&#124; Image &#124; hscooter.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox11 object &#124;
&#124; Name &#124; picVScooter &#124;
&#124; Image &#124; vscooter.jpg &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124;  &#124;  &#124;

&#124; Timer1 Object &#124;
&#124; Name &#124; timScooter &#124;
&#124;  &#124;  &#124;

&#124; Timer2 Object &#124;
&#124; Name &#124; timTime &#124;
&#124;  &#124;  &#124;

&#124; Timer3 Object &#124;
&#124; Name &#124; timPhone &#124;
&#124;  &#124;  &#124;

&#124; Timer4 Object &#124;
&#124; Name &#124; timOven &#124;
&#124;  &#124;  &#124;

This completes the form design. However, you still need a grid on the form. This grid itself will use more than 400 label controls added to the Load event procedure on the form. To do this, you need to know how to add controls when the program starts and how to link those controls to event procedures. |
| Step 3 | When building a Visual C# application, the process of adding controls and setting properties when designing is quite easy and simple. Sometimes, it is more beneficial to add controls when the program runs. For example, in this project, you need a 21 x 21 grid consisting of label controls. With short code, you can automate the work of adding controls to the form when the program runs. You also delete it if you like.To add a control when the program runs, you need five steps: (1) declare a control, (2) create a control, (3) set control properties, (4) add a control to the form, and (5) link the event procedure. You will see each of these steps separately for a generic control named MyControl with the type of ControlType .The first step is to declare a control using the usual statement. You can also declare array that contain controls. Then, the control is created using a constructor: MyControl = new ControlType() .At this point, MyControl is set with default properties. You can change the value of each property as you wish. Specifically, you need to set values ​​for the Left and Top properties. Otherwise, all of your new controls will overlap in the upper left corner of the form ( Left = 0, Right = 0 ). You can also change the Width and Height properties. After the properties are set, the control can be added to the form using the Add method of the Controls object: this.Controls.Add(MyControl) .In this project, define a two-dimensional form-level array that contains the following label controls: 

&#124; 1 &#124; Label[,] DeliveryGrid = new Label[21, 21]; &#124;

You will use the 0-th elements of the DeliveryGrid to represent column and row labels. You will ignore the DeliveryGrid (0, 0) , the grid in the upper left corner.The code to create this grid and display it in the control panel ( pnlGrid ) is placed in the Load event procedure of the form:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273 &#124; private void FormDuckDelivery_Load( object sender, EventArgs e){    int w = pnlGrid.Width / 22;    int l = w;    int t = w;    // j is row, i is column; Creates one row at a time    for ( int j = 0; j < 21; j++)    {        for ( int i = 0; i < 21; i++)        {            DeliveryGrid[i, j] = new Label();            DeliveryGrid[i, j].Width = w;            DeliveryGrid[i, j].Height = w;            DeliveryGrid[i, j].Top = t;            DeliveryGrid[i, j].Left = l;            DeliveryGrid[i, j].Font =                new Font( "Microsoft Sans Serif" , 10,                FontStyle.Bold);            DeliveryGrid[i, j].TextAlign =                ContentAlignment.MiddleCenter;            if (i == 0)            {                if (j != 0)                {                    // Row number                    DeliveryGrid[i, j].Text = j.ToString();                    DeliveryGrid[i, j].Width =                        Convert.ToInt32(1.5 * w);                    DeliveryGrid[i, j].Left =                        Convert.ToInt32(0.5 * w);                    DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                }            }            else if (j == 0)            {                if (i != 0)                {                    // Column letter                    DeliveryGrid[i, j].Text =                        (( char ) (i + 64)).ToString();                    DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                }            }            else            {                DeliveryGrid[i, j].BorderStyle =                    BorderStyle.FixedSingle;                DeliveryGrid[i, j].BackColor = Color.White;                DeliveryGrid[i, j].ForeColor = Color.Yellow;                if (i < 10)                    DeliveryGrid[i, j].Tag = "0" + i.ToString();                else                    DeliveryGrid[i, j].Tag = i.ToString();                if (j < 10)                    DeliveryGrid[i, j].Tag += "0" + j.ToString();                else                    DeliveryGrid[i, j].Tag += j.ToString();                DeliveryGrid[i, j].Click +=                    new System. EventHandler( this . DeliveryGrid _Click);            }            pnlGrid.Controls.Add(DeliveryGrid[i, j]);            l += w;        }        // New row        l = w;        t += w;    }} &#124;

This code builds a label control grid, one row at a time. Each control is declared first, and then the Top , Left , Width , and Height properties are given a value. You will use a square-sized label control, based on the width of the panel (1/23 of the width of the panel, so that there is still space left). You start from the top left corner, then to the right. After a row has been created, the Top property is incremented down one row and the Left property is returned to the left edge. Other properties are given based on location. Controls with column labels (J = 0) and row labels (I = 0) do not have the edge and are given letters or numbers accordingly. Notice how the row labels are shifted slightly to the left to make two-digit space. Internal labels (I = 1 to 20, J = 1 to 20) have a BorderStyle edge and a lime background to give a grid effect. |
| Step 4 | Save and run the project to see the result as shown in Figure 3.6.You now certainly realize the power of adding control when the program runs. Next, you will write the game code in several stages. As an initial step, you will write the code that initializes the game. Then, you add additional elements to the game, one at a time. During the code development process, you will modify certain procedures several times before arriving at the final result.Every time you start a project, there are a number of initializations that need to be done. All initialization to this project is done in the Load event procedure of the form.During initialization or when a new program is running, you need to make sure that the only thing a user can do is click Start Game or Exit button. User certainly cannot operate roasting oven or load roasted duck into scooter. Add the following two lines of code to the end of the Load event procedure from the form: 

&#124; 12 &#124; grpOven.Enabled = FalsegrpScooter.Enabled = False &#124;

![](Image00025.jpg)Figure 3.6 The delivery grid has beeen created on the form |
| Step 5 | Save and run the project to ensure that roasting oven and loading to scooter now are disabled, as shown in Figure 3.7.You are now starting to add other elements to this game, one by one. You will add codes to run time, take orders over the telephone, run a roasting oven, load ducks into scooter, move scooter, and evaluate delivery of ducks. Each element will need to "adjust" the parameters, i.e. values ​​that define how the game works. |
| Step 6 | The first element added to this game is time. The time will start at 6.00 and stop at 11:00\. You certainly don't want the game to end completely in five hours, so you need to speed things up a bit. You need to decide how fast you need and still be able to play the game. This requires adjusting parameters.![](Image00026.jpg)Figure 3.7 grpOven and grpScooter initially disabledThe time will be controlled by the timer control with the name timTime . With each Tick event for this control, you will add one minute to the time. You will define a constant ( MSecPerMen ) that tells you how many milliseconds ( Interval property of timTime ) needed for each minute of the hour. You can choose 15 minutes to complete a game, or simulate 300 minutes (5 hours x 60 minutes / hour) of delivering ducks. So, you need to call the Tick event 300 times in 900000 milliseconds (15 minutes x 60 seconds / minutes x 1000 milliseconds / second). The constant to be used is MSecPerMen = 900000/300 = 3000 milliseconds / minute. Add this constant to the form-level declaration: 

&#124; 1 &#124; const int MSecPerMen = 3000; &#124;

And, add this one line of code at the end of the Load event procedure of the form to create a timer control:

&#124; 1 &#124; timTime.Interval = MSecPerMen &#124;

As mentioned, with each Tick event, you add one minute to displayed time. Add the following to the form-level declaration:

&#124; 1 &#124; int HourTime, MinuteTime; &#124;

The Tick event procedure of the timTime control is given as follows:

&#124; 123456789101112131415161718 &#124; private void timTime_Tick( object sender, EventArgs e){    MinuteTime++;    if (MinuteTime > 59)    {        MinuteTime = 0;        HourTime++;        if (HourTime == 11)        {            lblTime.Text = "11:00" ;            btnExitStop.PerformClick();            return ;        }    }    lblTime.Text = HourTime.ToString() + ":" ;    if (MinuteTime < 10)        lblTime.Text += "0" ; lblTime.Text += MinuteTime.ToString();} &#124;

Notice that after 11:00 is reached, the game stops by clicking ExitStop button. |
| Step 7 | Now, you will write code that starts, pauses, starts, and stops the time in this game. You also need to add a code to exit the game. Two button controls control the game, btnStartPause and btnExitStop . These two buttons have certain interactions. The btnStartPause control has three possible Text properties.If the Text property is Start Game when clicked, the game will be initialized and will be in play mode: 
*   Change Text property to Pause Game .
*   Initialize the time to 6:00.
*   Start timTime .
*   Change Text property of btnExitStop to Stop Game .

If the Text property is Pause Game when clicked, the game will enter in pause mode:

*   Change the Text property to Start Again .
*   Stop the timTime .
*   Disable btnExitStop .

If the Text property is Start Again when clicked, the game will enter play mode:

*   Change the Text property to Pause Game .
*   Start timTime .
*   Enable btnExitStop .

The code that summarizes the steps above is placed in the Click event procedure of btnStartPause :

&#124; 12345678910111213141516171819202122232425262728293031 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop  Game" ;        HourTime = 6;        MinuteTime = 0;        lblTime.Text = "6:00" ;        timTime.Enabled = true ;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timTime.Enabled = false ;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        // Game starts again        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timTime.Enabled = true ;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    }} &#124;

Pay attention to the pause mode and play mode, you also disable/enable grpOven and grpScooter as needed. |
| Step 8 | Save and run the project. Click on the Start Game button and the clock will start counting up minute by minute. Try to pause and restart the game. How long does it take to get through an hour? Based on parameter adjustments, it takes 3 minutes. Look at Figure 3.8 and 3.9. |
| Step 9 | Add this declaration at the form-level for the Game Over sound: 

&#124; 1 &#124; System.Media.SoundPlayer SoundGameOver; &#124;

![](Image00027.jpg)Figure 3.8 The clock will start counting up minute by minuteYou use gameover.wav file for this sound, which is placed in the bin\Debug folder. Add this line of code at the end of the Load event of the form to load the sound:

&#124; 12 &#124; SoundGameOver = new System.Media.SoundPlayer(Application.StartupPath    + "\\gameover.wav" ); &#124;

 |
| Step 10 | Now, the Click event procedure of btnExitStop is given as follows: 

&#124; 1234567891011121314151617 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        SoundGameOver.Play();        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        timTime.Enabled = false ;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        this .Close();    }} &#124;

![](Image00028.jpg)Figure 3.9 The form when Pause Game button is clicked |
| Step 11 | Save and run the project. You can now start the game, pause the game, start again the game, and stop the game. Make sure everything goes as desired. Make sure you hear a sound when the game is over.You also need to make sure the program automatically stops when the clock reaches 11:00\. But you don't need to wait 15 minutes to see what happens. To speed up, temporarily change MSecPerMen to 10\. Then run the program, click on the Start Game button and see what happens. After the clock reaches 11:00, the sound will play and the program returns to a stop state. |
| Step 12 | In this project, orders are randomly telephoned. Orders (time, location, and number of ducks) are displayed in the list box control. Number of roasted ducks ordered are displayed at the right location on the delivery grid. You then use this information to send the scooter to deliver the roasted duck.Here are the rules made for ordering (you can change it if you like): 
*   Orders arrive at random times, within 1 to 7 minutes of increment.
*   Orders originate from random locations on the delivery grid.
*   Each order is 1 to 5 roasted ducks, using this probability: 1 roasted duck, 30 percent; 2 roasted ducks, 20 percent; 3 roasted ducks, 20 percent; 4 roasted ducks, 15 percent; 5 roasted ducks, 15 percent.
*   No orders can be received after 10:30 so the scooter can complete the order.

As mentioned, order information will be displayed in the list box control. You use a specific format for it. For example, say the order arrived at 6:20, from the G12 grid location, for 2 roasted ducks. The information on the list box is 6:20 G 12 -> 2.Two arrays will be used to track order information. DuckArr is a two-dimensional array that says how many ducks are ordered at a grid location and TimeDuckArr is a two-dimensional array that contains the ordering time (in minutes). Add the following two declarations at the form-level:

&#124; 12 &#124; int [,] DuckArr = new int [21, 21];int [,] TimeDuckArr = new int [21, 21]; &#124;

timPhone timer will control how often orders arrive. The Interval property will be set randomly. Add a declaration that creates this random object in the form-level declaration:

&#124; 1 &#124; Random MyRandom = new Random(); &#124;

 |
| Step 13 | You need to do certain initializations for processing order. Modify the Click event of the btnStartPause control to set the initial Interval value (1 to 7 minutes), to clear completed orders from the grid and to start / stop timer at the right times: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop  Game" ;        // Clears grid        for ( int i = 1; i < 21; i++)        {            for ( int j = 1; j < 21; j++)            {                DeliveryGrid[i, j].BackColor = Color.White;                DeliveryGrid[i, j].Text = "" ;                DuckArr[i, j] = 0;                TimeDuckArr[i, j] = 0;            }        }        lstOrder.Items.Clear();        HourTime = 6;        MinuteTime = 0;        lblTime.Text = "6:00" ;        timTime.Enabled = true ;        timPhone.Interval = MSecPerMen * (1 + MyRandom.Next(7));        timPhone.Enabled = true ;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timTime.Enabled = false ;        timPhone.Enabled = false ;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        // Game starts again        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timTime.Enabled = true ;        timPhone.Enabled = true ;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    }} &#124;

 |
| Step 14 | Modify the Click event of btnExitStop to turn off the timer when the game is stopped: 

&#124; 123456789101112131415161718 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        SoundGameOver.Play();        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        timTime.Enabled = false ;        timPhone.Enabled = false ;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        this .Close();    }} &#124;

 |
| Step 15 | When the order arrives, you will sound the phone. Add this declaration at the form-level: 

&#124; 1 &#124; System.Media.SoundPlayer SoundPhone; &#124;

You use the phone.wav file for this sound, which is placed in bin\Debug folder. Add this one line to the Load event of the form to load the sound:

&#124; 12 &#124; SoundPhone = new System.Media.SoundPlayer(Application.StartupPath +    "\\phone.wav" ); &#124;

The procedure of the Click event timPhone timer that implements the rules of the order by telephone and sounding the telephone is given as follows:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748 &#124; private void timPhone_Tick( object sender, EventArgs e){    int i, j, k;    String Message;    SoundPhone.Play();    if (HourTime == 10 && MinuteTime >= 30)    {        timPhone.Enabled = false ;        return ;    }    do {        i = 1 + MyRandom.Next(20);        j = 1 + MyRandom.Next(20);    } while (DuckArr[i, j] != 0);    k = MyRandom.Next(100);    if (k <= 29)        DuckArr[i, j] = 1;    else if (k <= 49)        DuckArr[i, j] = 2;    else if (k <= 69)        DuckArr[i, j] = 3;    else if (k <= 84)        DuckArr[i, j] = 4;    else        DuckArr[i, j] = 5;    TimeDuckArr[i, j] = MinuteTime + 60 * HourTime;    // Creates order string    Message = lblTime.Text + " " ;    if (lblTime.Text.Length == 4)        Message = " " + Message;    Message += (( char )(i + 64)).ToString() + " " ;    if (j < 10)        Message += " " ;    Message += j.ToString() + " -> " + DuckArr[i, j].ToString();    lstOrder.Items.Add(Message);    lstOrder.Refresh();    DeliveryGrid[i, j].BackColor = Color.DarkGreen;    DeliveryGrid[i, j].Text = DuckArr[i, j].ToString();    timPhone.Interval = MSecPerMen * (1 + MyRandom.Next(7));} &#124;

![](Image00029.jpg)Figure 3.10 The phone starts ringing, with orders placed in the list box and the delivery grid areaIn this code, you ring the telephone. If the time is past 10:30, this routine is no longer executed. Next, you select an unselected random column (I) and a random row (J) for the order. Using the set percentages, the number ordered roasted ducks are stored in the DuckArr . Likewise, ordering time is stored in TimeDuckArr .Then, the text string that will be placed in the list box is formatted and added to the list box. The associated grid location is marked with a dark violet background and the number of ordered ducks. Before the procedure is finished executing, a new random interval value is calculated. This will give you a delay (between 1 and 7 minutes) until the next order is called. |
| Step 16 | Save and run the project. Click on Start Game button and the phone starts ringing, with orders placed in the list box and the delivery grid area as shown in Figure 3.10.Check that you can pause the game, restart it, and stop the game. Next, you will see how to make roasted ducks ready for delivery. |
| Step 17 | Once you know where the order came from, you need to roast ordered ducks in the oven. The grpOven group control box is now used. As you can see, you can roast, at most, eight pieces of duck at a time, which is shown by the picture box controls. You need other rules, and you can change them if you like. After the duck is roasted (it takes 10 minutes), the duck is placed in the grpRoast group box for storage. Up to 20 pieces of duck can be stored there. All ducks that have been roasted and not adequately placed in storage must be thrown away, which wastes money.Define three constants at the following form-level: 

&#124; 123 &#124; const int MaxDuckReady = 20;const int MaxDuckRoast = 8;const int RoastTime = 10; &#124;

You use one variable ( DuckRoast ) to track the number of ducks there are in the oven and one other variable ( DuckReady ) to specify the number of ducks that have been roasted and stored. The TotalDuckRoast variable will track all roasted ducks in one game. Picture box controls are placed in an array of controls ( DuckInOven ). The RemMinuteRoast variable is used to tell how many minutes are left in the roasting process. And, you use a Boolean variable ( OvenOn ) to find out whether the oven is on or off. This variable is used when game is in pause state. Add these declarations at the form-level:

&#124; 12345 &#124; int DuckRoast, DuckReady;int TotalDuckRoast;PictureBox[] DuckInOven = new PictureBox[8];int RemMinuteRoast;bool OvenOn; &#124;

 |
| Step 18 | timOven timer will be used to measure the roasting time. Modify the Load event of the form to create an array of picture box controls and set the Interval property of this timer. You set the interval to MSecPerMen , by counting down roasting process one minute at a time: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768697071727374757677787980818283848586878889 &#124; private void FormDuckDelivery_Load( object sender, EventArgs e){    int w = pnlGrid.Width / 22;    int l = w;    int t = w;    // j is row, i is column; Creates one row at a time    for ( int j = 0; j < 21; j++)    {        for ( int i = 0; i < 21; i++)        {            DeliveryGrid[i, j] = new Label();            DeliveryGrid[i, j].Width = w;            DeliveryGrid[i, j].Height = w;            DeliveryGrid[i, j].Top = t;            DeliveryGrid[i, j].Left = l;            DeliveryGrid[i, j].Font =                new Font( "Microsoft Sans Serif" , 10,                FontStyle.Bold);            DeliveryGrid[i, j].TextAlign =                ContentAlignment.MiddleCenter;            if (i == 0)            {                if (j != 0)                {                    // Row number                    DeliveryGrid[i, j].Text = j.ToString();                    DeliveryGrid[i, j].Width =                        Convert.ToInt32(1.5 * w);                    DeliveryGrid[i, j].Left =                        Convert.ToInt32(0.5 * w);                    DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                }            }            else if (j == 0)            {                if (i != 0)                {                    // Column letter                    DeliveryGrid[i, j].Text =                        (( char ) (i + 64)).ToString();                    DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                }            }            else            {                DeliveryGrid[i, j].BorderStyle =                    BorderStyle.FixedSingle;                DeliveryGrid[i, j].BackColor = Color.White;                DeliveryGrid[i, j].ForeColor = Color.Yellow;                if (i < 10)                    DeliveryGrid[i, j].Tag = "0" + i.ToString();                else                    DeliveryGrid[i, j].Tag = i.ToString();                if (j < 10)                    DeliveryGrid[i, j].Tag += "0" + j.ToString();                else                    DeliveryGrid[i, j].Tag += j.ToString();            }            pnlGrid.Controls.Add(DeliveryGrid[i, j]);            l += w;        }        // New row        l = w;        t += w;    }    DuckInOven[0] = picDuck1;    DuckInOven[1] = picDuck2;    DuckInOven[2] = picDuck3;    DuckInOven[3] = picDuck4;    DuckInOven[4] = picDuck5;    DuckInOven[5] = picDuck6;    DuckInOven[6] = picDuck7;    DuckInOven[7] = picDuck8;    grpOven.Enabled = false ;    grpScooter.Enabled = false ;    timTime.Interval = MSecPerMen;    timOven.Interval = MSecPerMen;    SoundGameOver =        new System.Media.SoundPlayer(Application.StartupPath +        "\\gameover.wav" );    SoundPhone =        new System.Media.SoundPlayer(Application.StartupPath +        "\\phone.wav" );} &#124;

 |
| Step 19 | Modify the Click event of the btnStartPause control to clean the oven, initialize variables and start/stop the timer at the right time: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop  Game" ;        // Clears grid        for ( int i = 1; i < 21; i++)        {            for ( int j = 1; j < 21; j++)            {                DeliveryGrid[i, j].BackColor = Color.White;                DeliveryGrid[i, j].Text = "" ;                DuckArr[i, j] = 0;                TimeDuckArr[i, j] = 0;            }        }        lstOrder.Items.Clear();        for ( int i = 0; i < 8; i++)            DuckInOven[i].Visible = false ;        DuckRoast = 0;        DuckReady = MaxDuckRoast;        TotalDuckRoast = DuckReady;        lblDuckReady.Text = DuckReady.ToString();        HourTime = 6;        MinuteTime = 0;        lblTime.Text = "6:00" ;        timTime.Enabled = true ;        timPhone.Interval = MSecPerMen * (1 + MyRandom.Next(7));        timPhone.Enabled = true ;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timTime.Enabled = false ;        timPhone.Enabled = false ;        timPhone.Enabled = false ;        OvenOn = timOven.Enabled;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        // Game starts again        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timTime.Enabled = true ;        timPhone.Enabled = true ;        timOven.Enabled = OvenOn;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    }} &#124;

Notice how you use the OvenOn variable to pause and restart the game. |
| Step 20 | You need to make the same changes to the Click event of btnExitStop to turn off the timer when the game is stopped: 

&#124; 123456789101112131415161718 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        SoundGameOver.Play();        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        timTime.Enabled = false ;        timPhone.Enabled = false ;        timOven.Enabled = false ;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        this .Close();    }} &#124;

 |
| Step 21 | Ducks are put into oven by clicking Put Into Oven ( btnPutIntoOven ) button on the grpOven control. With each click on the button, you carry out the following steps: 
*   Do DuckRoast increment.
*   Make the corresponding DuckInOven picture box control visible.
*   If maximum number of ducks has been reached, btnPutIntoOven is disabled.

Notice after roasted duck is placed in the oven, it cannot be removed.The Click event procedure from btnPutIntoOven that implements the steps above is given as follows:

&#124; 12345678 &#124; private void btnPutIntoOven_Click( object sender, EventArgs e){    DuckRoast++;    DuckInOven[DuckRoast - 1].Visible = true ;    if (DuckRoast == MaxDuckRoast)        btnPutIntoOven.Enabled = false ;} &#124;

 |
| Step 22 | Save and run project. Click on the Start Game button, then click on btnPutIntoOven button several times. You will see a number of ducks now in the oven, as shown in Figure 3.11.![](Image00030.jpg)Figure 3.11 A number of ducks now in the oven |
| Step 23 | After the oven is filled, roasting starts by clicking the Roast Duck button. Steps that need to be done: 
*   Change grpOven background color to black.
*   Disable button controls.
*   Display the time when roasting is done.
*   Initialize RemMinuteRoast .
*   Enable timOven to start roasting.

The Click event procedure from the btnRoastDuck button is given as follows:

&#124; 123456789101112131415161718192021222325242526272829 &#124; private void btnRoastDuck_Click( object sender, EventArgs e){    int hOut, mOut;    if (DuckRoast == 0)        return ;    grpOven.BackColor = Color.Red;    btnPutIntoOven.Enabled = false ;    btnRoastDuck.Enabled = false ;    hOut = HourTime;    mOut = MinuteTime + RoastTime;    if (mOut > 59)    {        mOut -= 60;        hOut++;    }    if (DuckRoast == 1)        grpOven.Text = "Ducks finished roasting on " ;    else        grpOven.Text = "Ducks finished roasting on " ;    grpOven.Text += hOut.ToString() + ":" ;    if (mOut < 10)        grpOven.Text += "0" ;    grpOven.Text += mOut.ToString();    RemMinuteRoast = RoastTime;    timOven.Enabled = true ;} &#124;

![](Image00031.jpg)Figure 3.12 User now load the ducks into the oven and start the roasting process |
| Step 24 | Save and run the project. You can now load the ducks into the oven and start the roasting process, as shown in Figure 3.12.Always remember, a black oven is an oven that is on, while a pink oven is an oven that is off. Sometimes, when you're playing a game, you might forget to start the roasting process. |
| Step 25 | With each Tick event on the oven timer ( timOven ), you need to do the following steps: 
*   If RemMinuteRoast <> 0 , RemMinuteRoast is decreased by one; if not, proceed to the next step.
*   Play a certain sound.
*   Turn off the oven.
*   Increase both DuckReady and TotalDuckRoast by 1, check the limit of MaxDuckReady .
*   Set the Text property of grpOven to Oven Off ; change the background color to deep pink.
*   Remove all duck picture boxes.
*   Set DuckRoast to 0.
*   Enable btnPutIntoOvenbutton and btnRoastDuck buttons.

Note that when the roasting is complete, you will play a certain sound. Add the following declaration at the form-level for the sound:

&#124; 1 &#124; System.Media.SoundPlayer SoundDing; &#124;

You use the ding.wav file for this sound, which is placed in the bin\Debug folder. Add this line of code to the Load event of the form to load the sound:

&#124; 12 &#124; SoundDing = new System.Media.SoundPlayer(Application.StartupPath +    "\\ding.wav" ); &#124;

The Tick event procedure of timOven that implements the steps above is given as follows:

&#124; 12345678910111213141516171819202122232425 &#124; private void timOven_Tick( object sender, EventArgs e){    if (RemMinuteRoast != 0)        RemMinuteRoast--;    else    {        SoundDing.Play();        timOven.Enabled = false ;        DuckReady += DuckRoast;        TotalDuckRoast += DuckRoast;        if (DuckReady > MaxDuckReady)            DuckReady = MaxDuckReady;        lblDuckReady.Text = DuckReady.ToString();        grpOven.Text = "Oven Off" ;        grpOven.BackColor = Color.DeepPink;        for ( int i = 0; i < 8; i++)            DuckInOven[i].Visible = false ;        DuckRoast = 0;        btnPutIntoOven.Enabled = true ;        btnRoastDuck.Enabled = true ;    }} &#124;

![](Image00032.jpg)Figure 3.13 Observe all changes that have been achieved so far |
| Step 26 | Save and run the project. Observe all changes that have been achieved so far. Look at Figure 3.13. |
| Step 27 | Now you are almost done testing everything, but still need one more change. Note if you stop the game when the oven is on, the control buttons will be disabled, but the oven is still on with the ducks in it. To fix this, make a few changes to the Click event of btnExitStop : 

&#124; 1234567891011121314151617181920212223242526 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        SoundGameOver.Play();        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        timTime.Enabled = false ;        timPhone.Enabled = false ;        timOven.Enabled = false ;        grpOven.Text = "Oven Off" ;        grpOven.BackColor = Color.Blue;        for ( int i = 0; i < 8; i++)            DuckInOven[i].Visible = false ;        btnPutIntoOven.Enabled = true ;        btnRoastDuck.Enabled = true ;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        this .Close();    }} &#124;

![](Image00033.jpg)Figure 3.14 After 10 minutes have passed, you will hear the sound of ding and the ducks that are roasted will be moved to grpRoastSave and run the project. Click Start Game , then click Put Into Oven button several times. Click on Roast Duck and wait. After 10 minutes have passed (maybe 11 minutes depending on when you click Roast Duck ), you will hear the sound of ding and the ducks that are roasted will be moved to grpRoast , as shown in Figure 3.14.Continue roasting the ducks, but that you can only save up to 20 ducks. Make sure you can pause the game, start again, and stop the game.Next, you will learn how to move the ducks into the scooter and start delivering them to the customer. |
| Step 28 | The delivery scooter is used to take the ducks from the restaurant to the customer location on the grid. The first step in the delivery process is loading ducks from the grpRoast group box into the scooter. This is done by clicking the Load button on the grpScooter group control box. You use a DuckInScooter variable to track how many ducks there are in the scooter. You are assuming a maximum of 10 pieces of roasted ducks that can be in the scooter. Add the declaration and other constants ( MaxDuckInScooter ) at the form-level: 

&#124; 12 &#124; int DuckInScooter;const int MaxDuckInScooter = 10; &#124;

 |
| Step 29 | Add the modified code of the Click event of btnStartPause to initialize the scooter variable and make sure the btnLoadScooter button is enabled: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop  Game" ;        // Clears grid        for ( int i = 1; i < 21; i++)        {            for ( int j = 1; j < 21; j++)            {                DeliveryGrid[i, j].BackColor = Color.White;                DeliveryGrid[i, j].Text = "" ;                DuckArr[i, j] = 0;                TimeDuckArr[i, j] = 0;            }        }        lstOrder.Items.Clear();        for ( int i = 0; i < 8; i++)            DuckInOven[i].Visible = false ;        DuckRoast = 0;        DuckReady = MaxDuckRoast;        TotalDuckRoast = DuckReady;        lblDuckReady.Text = DuckReady.ToString();        DuckInScooter = 0;        lblInScooter.Text = "0" ;        btnLoadScooter.Enabled = true ;        HourTime = 6;        MinuteTime = 0;        lblTime.Text = "6:00" ;        timTime.Enabled = true ;        timPhone.Interval = MSecPerMen * (1 + MyRandom.Next(7));        timPhone.Enabled = true ;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timTime.Enabled = false ;        timPhone.Enabled = false ;        timPhone.Enabled = false ;        OvenOn = timOven.Enabled;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        // Game starts again        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timTime.Enabled = true ;        timPhone.Enabled = true ;        timOven.Enabled = OvenOn;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    }} &#124;

 |
| Step 30 | As mentioned, to load ducks into the scooter, you click the Load button in the grpScooter group box. The steps required are quite simple. If a maximum number of ducks can be loaded, you load that number of ducks into the scooter. The Click event of btnLoadScooter handling this work is given as follows: 

&#124; 12345678910111213141516171819 &#124; private void btnLoadScooter_Click( object sender, EventArgs e){    if (DuckReady == 0)        return ;    if (DuckReady > MaxDuckInScooter)    {        DuckInScooter += MaxDuckInScooter;        DuckReady -= MaxDuckInScooter;    }    else    {        DuckInScooter += DuckReady;        DuckReady = 0;    }    lblDuckReady.Text = DuckReady.ToString();    lblInScooter.Text = DuckInScooter.ToString();    btnLoadScooter.Enabled = false ;} &#124;

Note that you disable the L o ad button after the ducks are loaded into the delivery scooter. You will use the Enabled status of this button to tell whether the scooter has ducks ready to be delivered. |
| Step 31 | Save and run the project. Start the game, roast a few ducks and move them into the delivery scooter. |
| Step 32 | After the roasted ducks are loaded into the delivery scooter, you are ready to make the delivery. Click on a location on the delivery grid and the scooter will travel from the restaurant to that location. You follow the same process so that the scooter returns to the restaurant when you need more roasted ducks. There is a lot to be done here: defining the location of the restaurant (randomly); detect clicks on the delivery grid; identify which label controls are clicked; and move the delivery scooter to the location that was clicked.You need a number of variables to track a scooter. Add the following declarations at the form-level: 

&#124; 123456 &#124; int DuckC, DuckR;int DeliveryC, DeliveryR;int ScooterC, ScooterR;int deltaC, deltaR;int Distance;bool ScooterMove; &#124;

DuckC and DuckR are column and row numbers for duck restaurant location on the delivery grid (marked with the X symbol). DeliveryC and DeliveryR are column and row numbers for delivery (label control that is clicked). ScooterC and ScooterR are the column and row numbers for the current scooter location. DeltaC and DeltaR are the difference between the position of the scooter and the delivery. Finally, Distance is the number of grid locations that need to be traveled by scooter and ScooterMove indicates whether the scooter is now moving (used for pause mode in the game).The scooter timer control is used to make the scooter move. You define one constant to express the speed of the scooter:

&#124; 1 &#124; const int MinPer20Square = 3; &#124;

This tells how many minutes it will take to move the scooter across the delivery grid (20 square squares per minute).Modify Load event of the form to set the Interval property of the scooter timer:

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768697071727374757677787980818283848586878889909192 &#124; private void FormDuckDelivery_Load( object sender, EventArgs e){    int w = pnlGrid.Width / 22;    int l = w;    int t = w;    // j is row, i is column; Creates one row at a time    for ( int j = 0; j < 21; j++)    {        for ( int i = 0; i < 21; i++)        {            DeliveryGrid[i, j] = new Label();            DeliveryGrid[i, j].Width = w;            DeliveryGrid[i, j].Height = w;            DeliveryGrid[i, j].Top = t;            DeliveryGrid[i, j].Left = l;            DeliveryGrid[i, j].Font =                new Font( "Microsoft Sans Serif" , 10,                FontStyle.Bold);            DeliveryGrid[i, j].TextAlign =                ContentAlignment.MiddleCenter;            if (i == 0)            {                if (j != 0)                {                    // Row number                    DeliveryGrid[i, j].Text = j.ToString();                    DeliveryGrid[i, j].Width =                        Convert.ToInt32(1.5 * w);                    DeliveryGrid[i, j].Left =                        Convert.ToInt32(0.5 * w);                    DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                }            }            else if (j == 0)            {                if (i != 0)                {                    // Column letter                    DeliveryGrid[i, j].Text =                        (( char ) (i + 64)).ToString();                    DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                }            }            else            {                DeliveryGrid[i, j].BorderStyle =                    BorderStyle.FixedSingle;                DeliveryGrid[i, j].BackColor = Color.White;                DeliveryGrid[i, j].ForeColor = Color.Yellow;                if (i < 10)                    DeliveryGrid[i, j].Tag = "0" + i.ToString();                else                    DeliveryGrid[i, j].Tag = i.ToString();                if (j < 10)                    DeliveryGrid[i, j].Tag += "0" + j.ToString();                else                    DeliveryGrid[i, j].Tag += j.ToString();            }            pnlGrid.Controls.Add(DeliveryGrid[i, j]);            l += w;        }        // New row        l = w;        t += w;    }    DuckInOven[0] = picDuck1;    DuckInOven[1] = picDuck2;    DuckInOven[2] = picDuck3;    DuckInOven[3] = picDuck4;    DuckInOven[4] = picDuck5;    DuckInOven[5] = picDuck6;    DuckInOven[6] = picDuck7;    DuckInOven[7] = picDuck8;    grpOven.Enabled = false ;    grpScooter.Enabled = false ;    timTime.Interval = MSecPerMen;    timOven.Interval = MSecPerMen;    timScooter.Interval = MSecPerMen * MinPer20Square / 20;    SoundGameOver =        new System.Media.SoundPlayer(Application.StartupPath +        "\\gameover.wav" );    SoundPhone =        new System.Media.SoundPlayer(Application.StartupPath +        "\\phone.wav" );    SoundDing = new System.Media.SoundPlayer(Application.StartupPath        + "\\ding.wav" );} &#124;

 |
| Step 33 | Modify the Click event of btnStartPause to initialize the location of the roasted duck restaurant (also the starting location of the scooter) and to start/stop the timer at the right time: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768697071727374 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop  Game" ;        // Clears grid        for ( int i = 1; i < 21; i++)        {            for ( int j = 1; j < 21; j++)            {                DeliveryGrid[i, j].BackColor = Color.White;                DeliveryGrid[i, j].Text = "" ;                DuckArr[i, j] = 0;                TimeDuckArr[i, j] = 0;            }        }        lstOrder.Items.Clear();        for ( int i = 0; i < 8; i++)            DuckInOven[i].Visible = false ;        DuckRoast = 0;        DuckReady = MaxDuckRoast;        TotalDuckRoast = DuckReady;        lblDuckReady.Text = DuckReady.ToString();        DuckInScooter = 0;        lblInScooter.Text = "0" ;        btnLoadScooter.Enabled = true ;        // Initialize destination and scooter location        DeliveryGrid[ScooterC, ScooterR].Image = null ;        DuckC = 2 + MyRandom.Next(18);        DuckR = 2 + MyRandom.Next(18);        DeliveryGrid[DuckC, DuckR].BackColor = Color.Black;        DeliveryGrid[DuckC, DuckR].Text = "X" ;        ScooterC = DuckC;        ScooterR = DuckR;        Distance = 0;        lblOrder.Text = "Scooter in:\r\n" +            Display(ScooterC, ScooterR);        HourTime = 6;        MinuteTime = 0;        lblTime.Text = "6:00" ;        timTime.Enabled = true ;        timPhone.Interval = MSecPerMen * (1 + MyRandom.Next(7));        timPhone.Enabled = true ;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timTime.Enabled = false ;        timPhone.Enabled = false ;        timPhone.Enabled = false ;        OvenOn = timOven.Enabled;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        // Game starts again        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timTime.Enabled = true ;        timPhone.Enabled = true ;        timOven.Enabled = OvenOn;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    }} &#124;

You first remove all previous scooters on the delivery grid. Then, the roasted duck restaurant is placed on a random grid and marked with the symbol X. The scooter is positioned at this location and Distance is initialized zero. Message is used to announce that the scooter is currently in the restaurant. Notice how you use the ScooterMove variable to pause and restart the game. |
| Step 34 | The message in the code above uses a function, Display , that converts column and row numbers to column letters and row numbers. Add this function to your project: 

&#124; 1234 &#124; private String Display( int c, int r){    return ((( char )(c + 64)).ToString() + " " + r.ToString());} &#124;

Notice how the Chr function is used to convert column number C to a letter (based on ASCII code). |
| Step 35 | Modify the Click event of btnExitStop to disable the scooter timer when the game is stopped: 

&#124; 123456789101112131415161718192021222324252627 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        SoundGameOver.Play();        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        timTime.Enabled = false ;        timPhone.Enabled = false ;        timOven.Enabled = false ;        timScooter.Enabled = false ;        grpOven.Text = "Oven Off" ;        grpOven.BackColor = Color.Blue;        for ( int i = 0; i < 8; i++)            DuckInOven[i].Visible = false ;        btnPutIntoOven.Enabled = true ;        btnRoastDuck.Enabled = true ;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        this .Close();    }} &#124;

 |
| Step 36 | Save and run the project. Click on the Start Game button to make sure the roasted duck restaurant is marked and certain messages are displayed, as shown in Figure 3.15. |
| Step 37 | After orders arrive and the roasted duck is available in the scooter, you will start delivering. To move the scooter to the desired location on the delivery grid, all you have to do is click on that location. You will have a Click event procedure that handles 400 label controls (20 x 20) on the grid. The procedure has the name DeliveryGrid_Click . Add this empty procedure to your project:![](Image00034.jpg)Figure 3.15 The roasted duck restaurant is marked and certain messages are displayed 

&#124; 123 &#124; private void DeliveryGrid_Click( object sender, EventArgs e){} &#124;

After a grid location is clicked, you do the following steps:

*   Delivery can only be done if the scooter is not moving (timScooter is disabled), grpScooter is enabled (game in play mode), and btnLoadScooter is disabled (roasted ducks have been loaded into the scooter).
*   Specify the column ( DeliveryC ) and row ( DeliveryR ) of the label that was clicked.
*   Calculate DeltaC and DeltaR . If DeltaC = 0 and DeltaR = 0, exit.
*   Display a message stating where the scooter goes.
*   Enabled timScooter .

Every step is clear except how to determine DeliveryC and DeliveryR .You need a way to determine the row and column of the label that was clicked on the DeliveryGrid controls array. You will use the Tag property of the DeliveryGrid elements. Tag property ( String type) is a property that programmers define to use when needed. For each element in the DeliveryGrid array, the Tag property will have four numbers, where the first two numbers indicate the column number and the second two numbers indicate the row number. The Tag property will be specified in the Load event procedure of the form. In that procedure, you connect each element of the controls array to event procedure DeliveryGrid_Click . Modify the Load event of form, as follows:

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768697071727374757677787980818283848586878889909192939495 &#124; private void FormDuckDelivery_Load( object sender, EventArgs e){    int w = pnlGrid.Width / 22;    int l = w;    int t = w;    // j is row, i is column; Creates one row at a time    for ( int j = 0; j < 21; j++)    {        for ( int i = 0; i < 21; i++)        {            DeliveryGrid[i, j] = new Label();            DeliveryGrid[i, j].Width = w;            DeliveryGrid[i, j].Height = w;            DeliveryGrid[i, j].Top = t;            DeliveryGrid[i, j].Left = l;            DeliveryGrid[i, j].Font =                new Font( "Microsoft Sans Serif" , 10,                FontStyle.Bold);            DeliveryGrid[i, j].TextAlign =                ContentAlignment.MiddleCenter;            if (i == 0)            {                if (j != 0)                {                    // Row number                    DeliveryGrid[i, j].Text = j.ToString();                    DeliveryGrid[i, j].Width =                        Convert.ToInt32(1.5 * w);                    DeliveryGrid[i, j].Left =                        Convert.ToInt32(0.5 * w);                    DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                }            }            else if (j == 0)            {                if (i != 0)                {                    // Column letter                    DeliveryGrid[i, j].Text =                        (( char ) (i + 64)).ToString();                    DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                }            }            else            {                DeliveryGrid[i, j].BorderStyle =                    BorderStyle.FixedSingle;                DeliveryGrid[i, j].BackColor = Color.White;                DeliveryGrid[i, j].ForeColor = Color.Yellow;                if (i < 10)                    DeliveryGrid[i, j].Tag = "0" + i.ToString();                else                    DeliveryGrid[i, j].Tag = i.ToString();                if (j < 10)                    DeliveryGrid[i, j].Tag += "0" + j.ToString();                else                    DeliveryGrid[i, j].Tag += j.ToString();                DeliveryGrid[i, j].Click +=                  new System. EventHandler( this . DeliveryGrid _Click);            }            pnlGrid.Controls.Add(DeliveryGrid[i, j]);            l += w;        }        // New row        l = w;        t += w;    }    DuckInOven[0] = picDuck1;    DuckInOven[1] = picDuck2;    DuckInOven[2] = picDuck3;    DuckInOven[3] = picDuck4;    DuckInOven[4] = picDuck5;    DuckInOven[5] = picDuck6;    DuckInOven[6] = picDuck7;    DuckInOven[7] = picDuck8;    grpOven.Enabled = false ;    grpScooter.Enabled = false ;    timTime.Interval = MSecPerMen;    timOven.Interval = MSecPerMen;    timScooter.Interval = MSecPerMen * MinPer20Square / 20;    SoundGameOver =        new System.Media.SoundPlayer(Application.StartupPath +        "\\gameover.wav" );    SoundPhone =        new System.Media.SoundPlayer(Application.StartupPath +        "\\phone.wav" );    SoundDing = new System.Media.SoundPlayer(Application.StartupPath        + "\\ding.wav" );} &#124;

 |
| Step 38 | Using this Tag property, you can write code to implement the steps in the Click event procedure of the DeliveryGrid : 

&#124; 1234567891011121314151617181920212223 &#124; private void DeliveryGrid_Click( object sender, EventArgs e){    Label GridClicked;    if (!timScooter.Enabled && grpScooter.Enabled &&        !btnLoadScooter.Enabled)    {        GridClicked = (Label)sender;        DeliveryC =           Convert. ToInt32(GridClicked.Tag.ToString().Substring(0, 2));        DeliveryR =               Convert. ToInt32(GridClicked.Tag.ToString().Substring(2, 2));        deltaC = DeliveryC - ScooterC;        deltaR = DeliveryR - ScooterR;        if (deltaC == 0 && deltaR == 0)            return ;        lblOrder.Text = "Scooter departs for: \r\n" +            Display(DeliveryC, DeliveryR);        timScooter.Enabled = true ;    }} &#124;

 |
| Step 39 | Save and run the game. Click the Start Game button, then click Load . You can now click on the delivery grid. In the example where the location clicked is E 13 is shown in Figure 3.16. |
| Step 40 | Now, you will make the scooter move to the selected location. Remember the two small picture boxes hidden behind the Start Game button ( picHScooter and picVScooter )? You will use it to show how the scooter moves on the delivery grid.By clicking on a grid location, timScooter will be enabled. With each Tick event at this timer, you move the scooter by a square box. You make horizontal movement first, then vertical movement. The steps required are as follows: 
*   Remove the image of the scooter in its current position.
*   If DeltaC <> 0 : Increase Distance by 1; Set the image to picHScooter.Image ; Recalculate ScooterC ; Recalculate DeltaC .
*   If DeltaR <> 0 : Increase Distance by 1; Set the image to picVScooter.Image ; Recalculate ScooterR ; Recalculate DeltaR .
*   Draw a scooter at a new location.
*   If ScooterC = DeliveryC and ScooterR = DeliveryR :
*   Play certain sound;
*   Disable timScooter ;
*   If ScooterC = DuckC and ScooterR = DuckR : return to the duck restaurant; set message; remove the image of the scooter; set DuckInScooter to 0; Enable btnLoadScooter .
*   If it's not in the restaurant, the scooter is in the location that was clicked: display a message; check delivery status.

![](Image00035.jpg)Figure 3.16 The location clicked in delivery grid is E 13This process seems to require many steps, but is actually quite simple. Note, especially, when you re-enable btnLoadScooter when the delivery scooter returns to the duck restaurant to reload the ducks into the scooter.Pay attention, when the scooter stops, you will sound a certain sound. Add the following declaration at the form-level:

&#124; 1 &#124; System.Media.SoundPlayer SoundScooter; &#124;

You use the scooter.wav file for this sound, which is placed in the bin\Debug folder on your project. Add one line of this code to the Load event of the form:

&#124; 12 &#124; SoundScooter = new System.Media.SoundPlayer(Application.StartupPath    + "\\scooter.wav" ); &#124;

The Tick event procedure of timScooter timer implementing the steps above is given as follows:

&#124; 1234567891011121314151617181920212223242526272930313233343536373940414243444546474849 &#124; private void timScooter_Tick( object sender, EventArgs e){    Image ScooterImage;    DeliveryGrid[ScooterC, ScooterR].Image = null ;    // Moves horizontally first    if (deltaC != 0)    {        Distance++;        ScooterImage = picHScooter.Image;        ScooterC += Math.Sign(deltaC);        deltaC = DeliveryC - ScooterC;    }    else    {        Distance++;        ScooterImage = picHScooter.Image;        ScooterR += Math.Sign(deltaR);        deltaR = DeliveryR - ScooterR;    }    DeliveryGrid[ScooterC, ScooterR].Image = ScooterImage;    if (ScooterC == DeliveryC && ScooterR == DeliveryR)    {        SoundScooter.Play();        timScooter.Enabled = false ;        if (ScooterC == DuckC && ScooterR == DuckR)        {            lblOrder.Text = "Scooter in Restaurant :\r\n" +                Display(ScooterC, ScooterR);            DeliveryGrid[ScooterC, ScooterR].Image = null ;            DuckInScooter = 0;            lblInScooter.Text = "0" ;            btnLoadScooter.Enabled = true ;        }        else        {            lblOrder.Text = "Scooter in " +                Display(ScooterC, ScooterR);            // Checks delivery status        }    }} &#124;

 |
| Step 41 | Note the use of the Math.Sign function for the direction of movement of the scooter. Save and run the project. Click on Start Game , then click on Load to place the roasted ducks into the scooter. Now, click on a location on the grid and see how the scooter goes to that location. See Figure 3.17.![](Image00036.jpg)Figure 3.17 Scooter depart for delivery location |
| Step 42 | After the delivery scooter arrives at the chosen location, you need to check the delivery status at that location. You will also determine how delivery results in your income. The rules that are applied are as follows: 
*   Timely delivery is in the range of 30 minutes. Timely delivery costs in Rp. 10,000 for each roasted duck delivered. Timely delivery will have a green background on the grid.
*   Delayed delivery is between 30 to 60 minutes. Delayed delivery costs Rp. 5,000 for each roasted duck delivered. Delayed delivery will have a red background on the grid.
*   After 60 minutes, the order will be canceled and there is a penalty of Rp. 1,000 for each roasted duck that is not delivered.
*   Rp. 3,000 is cost to roast each duck.
*   Rp. 100 is cost for each square box taken by the delivery scooter.

The above rules are implemented on several constants. Add the following declarations at the form-level:

&#124; 1234567 &#124; const int MaxOrderTime = 60;const int DelayOrderTime = 30;const int DuckSoldNet = 10000;const int DuckDelayNet = 5000;const int CostCancelDuck = 1000;const int CostRoastDuck = 3000;const int CostDistance = 100; &#124;

You need variables to track delivery quantity. Add the following declarations at the form-level:

&#124; 1234 &#124; int DuckOnTime;int DuckDelay;int DeliveryCancel;int TotalSale; &#124;

DuckOnTime is the number of timely deliveries, DuckDelay is the number of late deliveries, DeliveryCancel is the number of canceled deliveries, and TotalSale is the amount of money during delivery. |
| Step 43 | Modify the Click event procedure of btnStartPause as follows: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop  Game" ;        // Clears grid        for ( int i = 1; i < 21; i++)        {            for ( int j = 1; j < 21; j++)            {                DeliveryGrid[i, j].BackColor = Color.White;                DeliveryGrid[i, j].Text = "" ;                DuckArr[i, j] = 0;                TimeDuckArr[i, j] = 0;            }        }        lstOrder.Items.Clear();        for ( int i = 0; i < 8; i++)            DuckInOven[i].Visible = false ;        DuckRoast = 0;        DuckReady = MaxDuckRoast;        TotalDuckRoast = DuckReady;        lblDuckReady.Text = DuckReady.ToString();        DuckInScooter = 0;        lblInScooter.Text = "0" ;        btnLoadScooter.Enabled = true ;        // Initialize destination and scooter location        DeliveryGrid[ScooterC, ScooterR].Image = null ;        DuckC = 2 + MyRandom.Next(18);        DuckR = 2 + MyRandom.Next(18);        DeliveryGrid[DuckC, DuckR].BackColor = Color.Black;        DeliveryGrid[DuckC, DuckR].Text = "X" ;        ScooterC = DuckC;        ScooterR = DuckR;        Distance = 0;        DuckOnTime = 0;        DuckDelay = 0;        DeliveryCancel = 0;       TotalSale = 0;       lblSale.Text = "Rp. 00" ;        lblOrder.Text = "Scooter in:\r\n" +            Display(ScooterC, ScooterR);        HourTime = 6;        MinuteTime = 0;        lblTime.Text = "6:00" ;        timTime.Enabled = true ;        timPhone.Interval = MSecPerMen * (1 + MyRandom.Next(7));        timPhone.Enabled = true ;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timTime.Enabled = false ;        timPhone.Enabled = false ;        timPhone.Enabled = false ;        OvenOn = timOven.Enabled;        grpOven.Enabled = false ;        grpScooter.Enabled = false ;    }    else    {        // Game starts again        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timTime.Enabled = true ;        timPhone.Enabled = true ;        timOven.Enabled = OvenOn;        grpOven.Enabled = true ;        grpScooter.Enabled = true ;    }} &#124;

 |
| Step 44 | Note that the indication of timely delivery is indicated by a white background color on the grid and late delivery is indicated by a red background color on the grid. The grid background is initialized in violet. After 30 minutes have passed after an order has been made, you need to change the background to red. And, after 60 minutes have passed for an order, it will be removed from the grid with penalty fees applied. This is all done in the Tick event procedure of timTime . At each Tick event, the following steps are performed: 
*   Check whether 60 minutes have passed for the first item in the list box. This is the longest order on the list and the only candidate to be deleted. If 60 minutes have passed, DeliveryCancel will be increased by the number of roasted duck ordered and the order will be removed from the delivery grid and list box.
*   For all other items in the list box, you check whether 30 minutes have passed. If so, and the background of the order location grid is not red, the background color is changed to red.

Modify the Tick event of timTime to implement the steps above:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354 &#124; private void timTime_Tick( object sender, EventArgs e){    int TotalMinuteTime;    int c, r;    String s;    bool Expire = false ;    MinuteTime++;    if (MinuteTime > 59)    {        MinuteTime = 0;        HourTime++;        if (HourTime == 11)        {            lblTime.Text = "11:00" ;            btnExitStop.PerformClick();            return ;        }    }    lblTime.Text = HourTime.ToString() + ":" ;    if (MinuteTime < 10)        lblTime.Text += "0" ; lblTime.Text += MinuteTime.ToString();    // Checks delayed order - checks whether it expires    TotalMinuteTime = MinuteTime + 60 * HourTime;    if (lstOrder.Items.Count != 0)    {        for ( int i = 0; i < lstOrder.Items.Count; i++)        {            s = lstOrder.Items[i].ToString();            c = (( int ) s[6]) - 64;            r = Convert.ToInt32(s.Substring(8,2));            if (i == 0 && TotalMinuteTime - TimeDuckArr[c, r] >=                MaxOrderTime)            {                Expire = true ;                DeliveryGrid[c, r].BackColor = Color.White;                DeliveryGrid[c, r].Text = "" ;                DeliveryCancel += DuckArr[c, r];                DuckArr[c, r] = 0;            }            else if (TotalMinuteTime - TimeDuckArr[c, r] >=                DelayOrderTime)            {                DeliveryGrid[c, r].BackColor = Color.DarkRed;            }        }        if (Expire)            lstOrder.Items.RemoveAt(0);    }} &#124;

Notice how you extract the column (C) and row (R) information from list box items. In the code, you use constants that are defined for timely delivery and delayed delivery. |
| Step 45 | Save and run the game. Click on the Start Game button. Notice when orders start to display a violet background, as shown in Figure 3.18\. After 30 minutes, orders that have passed 30 minutes will turn red, as shown in Figure 3.19.After 60 minutes, the orders are removed from the grid. Make sure the program works as desired. You can decrease MSecPerMen to speed up the timing. |
| Step 46 | As seen before, after the scooter arrives at the delivery location, check on the delivery status is performed. This check is done at the Click event of the timScooter . The following steps need to be done: 
*   If the delivery location does not order any duck, a message will be displayed.
*   If the delivery location requires more roasted ducks than is available, a message will be displayed.
*   If timely delivery is successful, DuckOnTime will be increased by the number of roasted ducks ordered. TotalSale is also updated.
*   If the delivery is elayed, DuckDelay will be increased by the number of roasted ducks ordered. TotalSale is also updated.
*   If delivery is successful (either on time or delayed), DuckInScooter is decremented and the order is removed from the delivery grid and from the list box control.

![](Image00037.jpg)Figure 3.18 Orders start to display a violet backgroundAdd the modified code of the Click event procedure of timScooter to implement the steps above:![](Image00038.jpg)Figure 3.19 After 30 minutes, orders that have passed 30 minutes will turn red

&#124; 12345678910111213141516171819202122232425262729303132333435363739404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110 &#124; private void timScooter_Tick( object sender, EventArgs e){    Image ScooterImage;    int i, c, r;    String s;    DeliveryGrid[ScooterC, ScooterR].Image = null ;    // Moves horizontally first    if (deltaC != 0)    {        Distance++;        ScooterImage = picHScooter.Image;        ScooterC += Math.Sign(deltaC);        deltaC = DeliveryC - ScooterC;    }    else    {        Distance++;        ScooterImage = picHScooter.Image;        ScooterR += Math.Sign(deltaR);        deltaR = DeliveryR - ScooterR;    }    DeliveryGrid[ScooterC, ScooterR].Image = ScooterImage;    if (ScooterC == DeliveryC && ScooterR == DeliveryR)    {        SoundScooter.Play();        timScooter.Enabled = false ;        if (ScooterC == DuckC && ScooterR == DuckR)        {            lblOrder.Text = "Scooter in Restaurant :\r\n" +                Display(ScooterC, ScooterR);            DeliveryGrid[ScooterC, ScooterR].Image = null ;            DuckInScooter = 0;            lblInScooter.Text = "0" ;            btnLoadScooter.Enabled = true ;        }        else        {            lblOrder.Text = "Scooter in " +                Display(ScooterC, ScooterR);            // Checks delivery status            if (DuckArr[DeliveryC, DeliveryR] == 0)            {                lblOrder.Text += "\r\nNo Ducks Ordered" ;            }            else            {                if (DuckArr [DeliveryC, DeliveryR] > DuckInScooter)                {                    lblOrder.Text += "\r\nDucks Not Enough" ;                }                else                {                    lblOrder.Text += "\r\nDelivered " +                        DuckArr[DeliveryC,                        DeliveryR].ToString() + " Ducks" ;                    if (DuckArr[DeliveryC, DeliveryR] > 1)                        lblOrder.Text += "- Thanks" ;                    // check on-time or delayed delivery                    if ((MinuteTime + 60 * HourTime) –                        TimeDuckArr[DeliveryC, DeliveryR] <=                        DelayOrderTime)                    {                        lblOrder.Text += ": On Time" ;                        T otalSale += DuckArr[DeliveryC, DeliveryR] *                            DuckSoldNet;                        DuckOnTime += DuckArr[DeliveryC, DeliveryR];                    }                    else                    {                        lblOrder.Text += ": Delayed!" ;                        T otalSale += DuckArr[DeliveryC, DeliveryR] *                            DuckDelayNet;                        D uckDelay += DuckArr[DeliveryC, DeliveryR];                    }                    lblSale.Text = "Rp. " + TotalSale.ToString();                    D uckInScooter -= DuckArr[DeliveryC, DeliveryR];                    lblInScooter. Text = DuckInScooter.ToString();                    DuckArr[DeliveryC, DeliveryR] = 0;                    De liveryGrid[DeliveryC, DeliveryR].BackColor =                        Color.White;                    DeliveryGrid[DeliveryC, DeliveryR].Text = "" ;                    // Removes from list                    for (i = 0; i < lstOrder.Items.Count; i++)                    {                        s = lstOrder.Items[i].ToString();                        c = (( int ) s[6]) - 64;                        r = Convert.ToInt32(s.Substring(8,2));                        if (c == DeliveryC && r == DeliveryR)                            break ;                    }                    lstOrder.Items.RemoveAt(i);                }            }        }    }} &#124;

Notice how you search the list box to find related item (matched column and row) to delete orders. |
| Step 47 | Save and run the project. You can run all game functionalities. You can take orders, roast ducks, load ducks in scooter, and move scooter to deliver orders to specific locations, as shown in Figure 3.20.![](Image00039.jpg)Figure 3.20 You can run all game functionalities. You can take orders, roast ducks, load ducks in scooter, and move scooter to deliver orders to specific locations |
|  |  |

| FormDuckDelivery.cs |

| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197198199200201202203204205206207208209210211212213214215216217218219220221222223224225226227228229230231232234235236237238239240241242243244245246247248249250251252253254255256257258259260261262263264265266267268269270271272273274275276277278279280281282283284285286287288289290291292293294295296297298299300301302303304305306307308309310311312313314315316317318319320321322323324325326327328329330331332333334335336337338339340341342343344345346347348349350351352353354355356357358359360361362363364365366367368369370371372373374375376377378379380381382383384385386387388389390391392393394395396397398399400401402403404405406407408409410411412413414415416417418419420421422423424425426427428429430431432433434435436437438439440441442443444445446447448449450451452453454455456457458459460461462463464465466467468469470471472473474475476477478479480481482483484485486487488489490491492493494495496497498499500501502503504505506507508509510511512513514515516517518519520521522523524525526527528529530531532533534535536537538539540541542543544545546547548549550551552553554555556557558559560561562563564565566567568569570571572573574575576577578579580581582583584585586587588589590591592 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;namespace Mengantar_Bebek_Bakar{    public partial class FormDuckDelivery : Form    {        Label[,] DeliveryGrid = new Label[21, 21];        const int MSecPerMen = 3000;        int HourTime, MinuteTime;        System.Media.SoundPlayer SoundGameOver;        int [,] DuckArr = new int [21, 21];        int [,] TimeDuckArr = new int [21, 21];        Random MyRandom = new Random();        System.Media.SoundPlayer SoundPhone;        const int MaxDuckReady = 20;        const int MaxDuckRoast = 8;        const int RoastTime = 10;        int DuckRoast, DuckReady;        int TotalDuckRoast;        PictureBox[] DuckInOven = new PictureBox[8];        int RemMinuteRoast;        bool OvenOn;        System.Media.SoundPlayer SoundDing;        int DuckInScooter;        const int MaxDuckInScooter = 10;        int DuckC, DuckR;        int DeliveryC, DeliveryR;        int ScooterC, ScooterR;        int deltaC, deltaR;        int Distance;        bool ScooterMove;        const int MinPer20Square = 3;        System.Media.SoundPlayer SoundScooter;        const int MaxOrderTime = 60;        const int DelayOrderTime = 30;        const int DuckSoldNet = 10000;        const int DuckDelayNet = 5000;        const int CostCancelDuck = 1000;        const int CostRoastDuck = 3000;        const int CostDistance = 100;        int DuckOnTime;        int DuckDelay;        int DeliveryCancel;        int TotalSale;        public FormDuckDelivery ()        {            InitializeComponent();        }        private void FormDuckDelivery_Load( object sender, EventArgs e)        {            int w = pnlGrid.Width / 22;            int l = w;            int t = w;            // j is row, i is column; Creates one row at a time            for ( int j = 0; j < 21; j++)            {                for ( int i = 0; i < 21; i++)                {                    DeliveryGrid[i, j] = new Label();                    DeliveryGrid[i, j].Width = w;                    DeliveryGrid[i, j].Height = w;                    DeliveryGrid[i, j].Top = t;                    DeliveryGrid[i, j].Left = l;                    DeliveryGrid[i, j].Font = new Font( "Microsoft Sans Serif" ,                        10, FontStyle.Bold);                    DeliveryGrid[i, j]. TextAlign = ContentAlignment.MiddleCenter;                    if (i == 0)                    {                        if (j != 0)                        {                            // Row number                            DeliveryGrid[i, j].Text = j.ToString();                            DeliveryGrid[i, j].Width = Convert.ToInt32(1.5 * w);                            DeliveryGrid[i, j].Left = Convert.ToInt32(0.5 * w);                            DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                        }                    }                    else if (j == 0)                    {                        if (i != 0)                        {                            // Column letter                            DeliveryGrid [i, j].Text = (( char ) (i + 64)).ToString();                            DeliveryGrid[i, j].ForeColor = Color.DarkBlue;                        }                    }                    else                    {                        DeliveryGrid[i, j]. BorderStyle = BorderStyle.FixedSingle;                        DeliveryGrid[i, j].BackColor = Color.White;                        DeliveryGrid[i, j].ForeColor = Color.Yellow;                        if (i < 10)                            DeliveryGrid[i, j].Tag = "0" + i.ToString();                        else                            DeliveryGrid[i, j].Tag = i.ToString();                        if (j < 10)                            DeliveryGrid[i, j].Tag += "0" + j.ToString();                        else                            DeliveryGrid[i, j].Tag += j.ToString();                        DeliveryGrid[i, j].Click += new                            System.EventHandler( this .DeliveryGrid_Click);                    }                    pnlGrid.Controls.Add(DeliveryGrid[i, j]);                    l += w;                }                // New row                l = w;                t += w;            }            DuckInOven[0] = picDuck1;            DuckInOven[1] = picDuck2;            DuckInOven[2] = picDuck3;            DuckInOven[3] = picDuck4;            DuckInOven[4] = picDuck5;            DuckInOven[5] = picDuck6;            DuckInOven[6] = picDuck7;            DuckInOven[7] = picDuck8;            grpOven.Enabled = false ;            grpScooter.Enabled = false ;            timTime.Interval = MSecPerMen;            timOven.Interval = MSecPerMen;            timScooter.Interval = MSecPerMen * MinPer20Square / 20;            SoundGameOver = new System.Media.SoundPlayer(Application.StartupPath                + "\\gameover.wav" );            SoundPhone = new System.Media.SoundPlayer(Application.StartupPath                + "\\phone.wav" );            SoundDing = new System.Media.SoundPlayer(Application.StartupPath                + "\\ding.wav" );            SoundScooter = new System.Media.SoundPlayer(Application.StartupPath                + "\\scooter.wav" );        }       private void timTime_Tick( object sender, EventArgs e)        {            int TotalMinuteTime;            int c, r;            String s;            bool Expire = false ;            MinuteTime++;            if (MinuteTime > 59)            {                MinuteTime = 0;                HourTime++;                if (HourTime == 11)                {                    lblTime.Text = "11:00" ;                    btnExitStop.PerformClick();                    return ;                }            }            lblTime.Text = HourTime.ToString() + ":" ;            if (MinuteTime < 10)                lblTime.Text += "0" ; lblTime.Text += MinuteTime.ToString();            // Checks delayed order - checks whether it expires            TotalMinuteTime = MinuteTime + 60 * HourTime;            if (lstOrder.Items.Count != 0)            {                for ( int i = 0; i < lstOrder.Items.Count; i++)                {                    s = lstOrder.Items[i].ToString();                    c = (( int ) s[6]) - 64;                    r = Convert.ToInt32(s.Substring(8,2));                    if (i == 0 && TotalMinuteTime - TimeDuckArr[c, r] >= MaxOrderTime)                    {                        Expire = true ;                        DeliveryGrid[c, r].BackColor = Color.White;                        DeliveryGrid[c, r].Text = "" ;                        DeliveryCancel += DuckArr[c, r];                        DuckArr[c, r] = 0;                    }                    else if ( TotalMinuteTime - TimeDuckArr[c, r] >= DelayOrderTime)                    {                        DeliveryGrid[c, r].BackColor = Color.DarkRed;                    }                }                if (Expire)                    lstOrder.Items.RemoveAt(0);            }        }        private void btnStartPause_Click( object sender, EventArgs e)        {            if (btnStartPause.Text == "Start Game" )            {                btnStartPause.Text = "Pause Game" ;                btnExitStop.Text = "Stop  Game" ;                // Clears grid                for ( int i = 1; i < 21; i++)                {                    for ( int j = 1; j < 21; j++)                    {                        DeliveryGrid[i, j].BackColor = Color.White;                        DeliveryGrid[i, j].Text = "" ;                        DuckArr[i, j] = 0;                        TimeDuckArr[i, j] = 0;                    }                }                lstOrder.Items.Clear();                for ( int i = 0; i < 8; i++)                    DuckInOven[i].Visible = false ;                DuckRoast = 0;                DuckReady = MaxDuckRoast;                TotalDuckRoast = DuckReady;                lblDuckReady.Text = DuckReady.ToString();                DuckInScooter = 0;                lblInScooter.Text = "0" ;                btnLoadScooter.Enabled = true ;                // Initialize destination and scooter location                DeliveryGrid[ScooterC, ScooterR].Image = null ;                DuckC = 2 + MyRandom.Next(18);                DuckR = 2 + MyRandom.Next(18);                DeliveryGrid[DuckC, DuckR].BackColor = Color.Black;                DeliveryGrid[DuckC, DuckR].Text = "X" ;                ScooterC = DuckC;                ScooterR = DuckR;                Distance = 0;                DuckOnTime = 0;                DuckDelay = 0;                DeliveryCancel = 0;                TotalSale = 0;                lblSale.Text = "Rp. 00" ;                lblOrder.Text = "Scooter in:\r\n" + Display(ScooterC, ScooterR);                HourTime = 6;                MinuteTime = 0;                lblTime.Text = "6:00" ;                timTime.Enabled = true ;                timPhone.Interval = MSecPerMen * (1 + MyRandom.Next(7));                timPhone.Enabled = true ;                grpOven.Enabled = true ;                grpScooter.Enabled = true ;            }            else if (btnStartPause.Text == "Pause Game" )            {                btnStartPause.Text = "Start Again" ;                btnExitStop.Enabled = false ;                timTime.Enabled = false ;                timPhone.Enabled = false ;                OvenOn = timOven.Enabled;                timOven.Enabled = false ;                ScooterMove = timScooter.Enabled;                timScooter.Enabled = false ;                grpOven.Enabled = false ;                grpScooter.Enabled = false ;            }            else            {                // Game starts again                btnStartPause.Text = "Pause Game" ;                btnExitStop.Enabled = true ;                timTime.Enabled = true ;                timPhone.Enabled = true ;                timOven.Enabled = OvenOn;                timScooter.Enabled = ScooterMove;                grpOven.Enabled = true ;                grpScooter.Enabled = true ;            }        }        private void btnExitStop_Click( object sender, EventArgs e)        {            if (btnExitStop.Text == "Stop Game" )            {                SoundGameOver.Play();                btnExitStop.Text = "Exit" ;                btnStartPause.Text = "Start Game" ;                timTime.Enabled = false ;                timPhone.Enabled = false ;                timOven.Enabled = false ;                timScooter.Enabled = false ;                grpOven.Text = "Oven Off" ;                grpOven.BackColor = Color.Blue;                for ( int i = 0; i < 8; i++)                    DuckInOven[i].Visible = false ;                btnPutIntoOven.Enabled = true ;                btnRoastDuck.Enabled = true ;                grpOven.Enabled = false ;                grpScooter.Enabled = false ;            }            else            {                this .Close();            }        }        private void timPhone_Tick( object sender, EventArgs e)        {            int i, j, k;            String Message;            SoundPhone.Play();            if (HourTime == 10 && MinuteTime >= 30)            {                timPhone.Enabled = false ;                return ;            }            do {                i = 1 + MyRandom.Next(20);                j = 1 + MyRandom.Next(20);            } while (DuckArr[i, j] != 0);            k = MyRandom.Next(100);            if (k <= 29)                DuckArr[i, j] = 1;            else if (k <= 49)                DuckArr[i, j] = 2;            else if (k <= 69)                DuckArr[i, j] = 3;            else if (k <= 84)                DuckArr[i, j] = 4;            else                DuckArr[i, j] = 5;            TimeDuckArr[i, j] = MinuteTime + 60 * HourTime;            // Creates order string            Message = lblTime.Text + " " ;            if (lblTime.Text.Length == 4)                Message = " " + Message;            Message += (( char )(i + 64)).ToString() + " " ;            if (j < 10)                Message += " " ;            Message += j.ToString() + " -> " + DuckArr[i, j].ToString();            lstOrder.Items.Add(Message);            lstOrder.Refresh();            DeliveryGrid[i, j].BackColor = Color.DarkGreen;            DeliveryGrid[i, j].Text = DuckArr[i, j].ToString();            timPhone.Interval = MSecPerMen * (1 + MyRandom.Next(7));        }        private void btnPutIntoOven_Click( object sender, EventArgs e)        {            DuckRoast++;            DuckInOven[DuckRoast - 1].Visible = true ;            if (DuckRoast == MaxDuckRoast)                btnPutIntoOven.Enabled = false ;        }        private void btnRoastDuck_Click( object sender, EventArgs e)        {            int hOut, mOut;            if (DuckRoast == 0)                return ;            grpOven.BackColor = Color.Red;            btnPutIntoOven.Enabled = false ;            btnRoastDuck.Enabled = false ;            hOut = HourTime;            mOut = MinuteTime + RoastTime;            if (mOut > 59)            {                mOut -= 60;                hOut++;            }            if (DuckRoast == 1)                grpOven.Text = "Ducks finished roasting on " ;            else                grpOven.Text = "Ducks finished roasting on " ;            grpOven.Text += hOut.ToString() + ":" ;            if (mOut < 10)                grpOven.Text += "0" ;            grpOven.Text += mOut.ToString();            RemMinuteRoast = RoastTime;            timOven.Enabled = true ;        }        private void timOven_Tick( object sender, EventArgs e)        {            if (RemMinuteRoast != 0)                RemMinuteRoast--;            else            {                SoundDing.Play();                timOven.Enabled = false ;                DuckReady += DuckRoast;                TotalDuckRoast += DuckRoast;                if (DuckReady > MaxDuckReady)                    DuckReady = MaxDuckReady;                lblDuckReady.Text = DuckReady.ToString();                grpOven.Text = "Oven Off" ;                grpOven.BackColor = Color.DeepPink;                for ( int i = 0; i < 8; i++)                    DuckInOven[i].Visible = false ;                DuckRoast = 0;                btnPutIntoOven.Enabled = true ;                btnRoastDuck.Enabled = true ;            }        }        private void btnLoadScooter_Click( object sender, EventArgs e)        {            if (DuckReady == 0)                return ;            if (DuckReady > MaxDuckInScooter)            {                DuckInScooter += MaxDuckInScooter;                DuckReady -= MaxDuckInScooter;            }            else            {                DuckInScooter += DuckReady;                DuckReady = 0;            }            lblDuckReady.Text = DuckReady.ToString();            lblInScooter.Text = DuckInScooter.ToString();            btnLoadScooter.Enabled = false ;        }        private String Display( int c, int r)        {            return ((( char )(c + 64)).ToString() + " " + r.ToString());        }        private void DeliveryGrid_Click( object sender, EventArgs e)        {            Label GridClicked;            if (!timScooter. Enabled && grpScooter.Enabled && !btnLoadScooter.Enabled)            {                GridClicked = (Label)sender;                DeliveryC =                    Convert.ToInt32(GridClicked.Tag.ToString().Substring(0, 2));                DeliveryR =                    Convert.ToInt32(GridClicked.Tag.ToString().Substring(2, 2));                deltaC = DeliveryC - ScooterC;                deltaR = DeliveryR - ScooterR;                if (deltaC == 0 && deltaR == 0)                    return ;                lblOrder.Text = "Scooter departs for: \r\n" + Display(DeliveryC, DeliveryR);                timScooter.Enabled = true ;            }        }        private void timScooter_Tick( object sender, EventArgs e)        {            Image ScooterImage;            int i, c, r;            String s;            DeliveryGrid[ScooterC, ScooterR].Image = null ;            // Moves horizontally first            if (deltaC != 0)            {                Distance++;                ScooterImage = picHScooter.Image;                ScooterC += Math.Sign(deltaC);                deltaC = DeliveryC - ScooterC;            }            else            {                Distance++;                ScooterImage = picHScooter.Image;                ScooterR += Math.Sign(deltaR);                deltaR = DeliveryR - ScooterR;            }            DeliveryGrid[ScooterC, ScooterR].Image = ScooterImage;            if (ScooterC == DeliveryC && ScooterR == DeliveryR)            {                SoundScooter.Play();                timScooter.Enabled = false ;                if (ScooterC == DuckC && ScooterR == DuckR)                {                    lblOrder.Text = "Scooter in Restaurant :\r\n" +                        Display(ScooterC, ScooterR);                    DeliveryGrid[ScooterC, ScooterR].Image = null ;                    DuckInScooter = 0;                    lblInScooter.Text = "0" ;                    btnLoadScooter.Enabled = true ;                }                else                {                    lblOrder.Text = "Scooter in " + Display(ScooterC, ScooterR);                    // Checks delivery status                    if (DuckArr[DeliveryC, DeliveryR] == 0)                    {                        lblOrder.Text += "\r\nNo Ducks Ordered" ;                    }                    else                    {                        if (DuckArr[DeliveryC, DeliveryR] > DuckInScooter)                        {                            lblOrder.Text += "\r\nDucks Not Enough" ;                        }                        else                        {                            lblOrder.Text += "\r\nDelivered " +                                DuckArr[DeliveryC, DeliveryR].ToString() +                                " Ducks" ;                            if (DuckArr[DeliveryC, DeliveryR] > 1)                                lblOrder.Text += "- Thanks" ;                            // check on-time or delayed delivery                            if ((MinuteTime + 60 * HourTime) –                              TimeDuckArr[DeliveryC, DeliveryR] <= DelayOrderTime)                            {                                lblOrder.Text += ": On Time" ;                                TotalSale += DuckArr[DeliveryC, DeliveryR] * DuckSoldNet;                                DuckOnTime += DuckArr[DeliveryC, DeliveryR];                            }                            else                            {                                lblOrder.Text += ": Delayed!" ;                                TotalSale += DuckArr[DeliveryC, DeliveryR] * DuckDelayNet;                                DuckDelay += DuckArr[DeliveryC, DeliveryR];                            }                            lblSale.Text = "Rp. " + TotalSale.ToString();                            DuckInScooter -= DuckArr[DeliveryC, DeliveryR];                            lblInScooter.Text = DuckInScooter.ToString();                            DuckArr[DeliveryC, DeliveryR] = 0;                            DeliveryGrid[ DeliveryC, DeliveryR].BackColor = Color.White;                            DeliveryGrid[DeliveryC, DeliveryR].Text = "" ;                            // Removes from list                            for (i = 0; i < lstOrder.Items.Count; i++)                            {                                s = lstOrder.Items[i].ToString();                                c = (( int ) s[6]) - 64;                                r = Convert.ToInt32(s.Substring(8,2));                                if (c == DeliveryC && r == DeliveryR)                                    break ;                            }                            lstOrder.Items.RemoveAt(i);                        }                    }                }            }        }    }} |

TUTORIAL 3

DRONE SIMULATION

In this tutorial, you will build a Drone Simulation. In this simulation, you control both vertical and horizontal thrusters to maneuver the ride to the landing pad. You will adjust the landing speed so that it is slow enough so that no accident occurs.

| Description |
| You build the form in two stages, the first stage creates two option group boxes, and then the second stage uses both those group boxes as landing controls. Two control panels are placed on the left side of the form: one panel for drawing and another panel for the edge. On the right side of the form, place the two group control boxes. In the first group box, five radio buttons and a check box are added. In the second group box, two radio buttons are placed. In the below section of the form, three buttons are added. Finally, one timer control is added.![](Image00040.jpg)Figure 4.1 All controls used in Drone Simulation projectThen in the form, a group box is added overlap panel. Then, 11 label controls are added to the group box. After that, a progress bar is added. Under the bar, two control panels are added, one high panel and one short panel. In the second (short) panel control, two small label controls are added. Underneath, three button controls are placed. Under these three buttons, a label control is added. For each label control, set the AutoSize property to False to be resized and set (temporarily) the BorderStyle property to FixedSingle so that you can see the edges to facilitate the layout process.![](Image00041.jpg)Figure 4.2 All type of controls used in Drone Simulation projectRun the program (press <F5>). You can choose one pilot level by checking or unchecking the auto-pilot option. Whenever you play a game, you can restore it and restart the game, as shown in Figure 4.3. |
| Tutorial Steps |
| Step 1 | You will now start to build this project. Open a new project in Visual C#. Once opened, it is recommended that you immediately save it with a name that you choose yourself. This will create the folders and file structure that your project needs.You will build the form in two stages, the first stage creates two option group boxes, and then the second stage uses both group groups as landing controls. Place two control panels on the left side of the form: one panel for drawing and another panel for the edge. On the right side of the form, place the two group control boxes. In the first group box, place five radio buttons and a check box. In the second group box, place the two radio buttons. In the bottom-right section of the form, place three control buttons. Add one timer control. The form will look as shown in Figure 4.4.![](Image00042.jpg)Figure 4.3 Drone Simulation runs with auto-pilot option![](Image00043.jpg)Figure 4.4 All controls used in this project and thei locationsOne control panel forms a frame that surrounds another panel that will display a drone landing animation. The first group box is used to select the pilot level and whether to use auto-pilot. The second group box is used to select measurement units. Two smaller button controls (one to start and pause the game and one other button to stop the game and exit the program) are used to control game operations. The larger button is used at the end of the game to see the landing result. Timer control is used to calculate landing position and speed and for animation updates. |
| Step 2 | Set the following property on each control using the Properties window: 

&#124; A Number of Properties of Form1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; FormDroneSimulation &#124;
&#124; Text &#124; Drone Simulation &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124; BackColor &#124; Gold &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Panel1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; pnlEdge &#124;
&#124; BackColor &#124; Maroon &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Panel2 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; pnlView &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of GroupBox1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; grpLevel &#124;
&#124; BackColor &#124; Cyan &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Difficulty Level &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of RadioButton1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoBeginner &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Beginner &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of RadioButton2 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoTrainee &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Trainee &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of RadioButton3 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoJunior &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Junior &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of RadioButton4 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoSenior &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Senior &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of RadioButton5 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoAdvanced &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Advanced &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of CheckBox1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; chkAutoPilot &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Auto-Pilot? &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of GroupBox2 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; grpUnit &#124;
&#124; BackColor &#124; Light Red &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Unit &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of RadioButton6 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoUnitMetric &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Metric &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of RadioButton7 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoUnitUS &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; US (Britain) &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Button1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnStartPause &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Start Game &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Button2 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnExitStop &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Exit &#124;
&#124;  &#124;  &#124;

![](Image00044.jpg)Figure 4.5 Setting properties in stage 1

&#124; A Number of Properties of Button3 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnFinish &#124;
&#124; BackColor &#124; Light Yellow &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Landing Complete &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Timer1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; timDrone &#124;
&#124; Interval &#124; 500 &#124;
&#124;  &#124;  &#124;

When the properties are set, the form will look as shown in Figure 4.5.Notice that the Visible property of larger button is False . In stage 2, you will now add the controls needed for the landing control group box.Add a group box in right side of panel. Add 11 label controls to the group box. Add a progress bar. Under the bar, add two control panels, one high panel and one short panel. In the second (short) control panel, add two small label controls. Underneath, place the three button controls. Under these three buttons, add a label control. For each label control, set the AutoSize property to False so that it can be resized and set (temporarily) the BorderStyle property to FixedSingle so that you can see the edges to facilitate the layout process.

&#124; A Number of Properties of GroupBox1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; grpControl &#124;
&#124; BackColor &#124; Crimson &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; Text &#124; Landing Control - Beginner &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Time (Sec.) &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label2 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblTime &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; 0.0 &#124;
&#124; TextAlign &#124; MiddleRight &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label3 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblPosition &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Position (m) &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label4 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblVel &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Vel. (m/sec) &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label5 Object &#124;
&#124; Property &#124; Value &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Altitudo &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label6 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblVPosition &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; 0.0 &#124;
&#124; TextAlign &#124; MiddleRight &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label7 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblVVel &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; 0.0 &#124;
&#124; TextAlign &#124; MiddleRight &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label8 Object &#124;
&#124; Property &#124; Value &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Lateral &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label9 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblHPosition &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; 0.0 &#124;
&#124; TextAlign &#124; MiddleRight &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label10 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblHVel &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; 0.0 &#124;
&#124; TextAlign &#124; MiddleRight &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label11 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblFuel &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font &#124; Bold, 10 &#124;
&#124; Text &#124; Fuel &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of ProgressBar1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; barFuel &#124;
&#124; Maximum &#124; 100 &#124;
&#124; Minimum &#124; 0 &#124;
&#124; Style &#124; Continuous &#124;
&#124; Value &#124; 100 &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Panel1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; pnlTrajectory &#124;
&#124; BackColor &#124; Black &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Panel2 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; pnlGuide &#124;
&#124; BackColor &#124; Dark Gray &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label12 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblDrone &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; Green &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label13 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblPad &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; Red &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Button1 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnThrustLeft &#124;
&#124; BackColor &#124; White &#124;
&#124; Image &#124; IMAGE\left.ico &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Button2 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnThrustDown &#124;
&#124; BackColor &#124; White &#124;
&#124; Image &#124; IMAGE\down.ico &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Button3 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnThrustRight &#124;
&#124; BackColor &#124; White &#124;
&#124; Image &#124; IMAGE\right.ico &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A Number of Properties of Label14 Object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblMessage &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; Text &#124; Auto-Pilot On &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

The form will look as shown in Figure 4.6.![](Image00040.jpg)Figure 4.6 Setting properties in stage 2 |
| Step 3 | Even though you don't have any code yet, you can run this game. The game now is in ‘stop’ state, as shown in Figure 4.7.In the “stop” state, what the user can do is choose one of the two options (Difficulty Level or Unit) or click the Start Game button or Exit . You can also decide if you want to enable Auto-Pilot . If the user chooses to start the game, two option group boxes will disappear and the landing group box ( grpControl ) will appear.You will use a variable ( LevelDifficulty ) that has a range of values ​​from 1 to 5 to track the level of the selected difficulty. Add this declaration at the form level: 

&#124; 1 &#124; int levelDifficulty = 1; &#124;

![](Image00045.jpg)Figure 4.7 The game now is in “stop” stateYou initialize the Beginner level ( LevelDifficulty = 1 ) to match the radio button that was originally selected.Code to set the LevelDifficulty is placed in the Click event procedure of rdoLevelDifficulty , which is the event for all radio buttons to select the difficulty level:

&#124; 123456789101112131415161718192021222324 &#124; private void rdoLevelDifficulty_Click( object sender, EventArgs e){    RadioButton ButtonClicked;    ButtonClicked = (RadioButton)sender;    switch (ButtonClicked.Text)    {        case "Beginner" :            levelDifficulty = 1;            break ;        case "Trainee" :            levelDifficulty = 2;            break ;        case "Junior" :            levelDifficulty = 3;            break ;        case "Senior" :            levelDifficulty = 4;            break ;        case "Advanced" :            levelDifficulty = 5;            break ;    }} &#124;

 |
| Step 4 | You will calculate this program in the metrics unit. This means all positions are in meter and all speeds are in meter/sec. If the user selects an US (Britain) unit, you need to multiply all results with a value that converts meters to feet. This value will be stored in a variable named Multiplier . Add the following declaration at the form level: 

&#124; 1 &#124; double Multiplier = 1.0; &#124;

The multiplier for the metric unit is specified in the Click event procedure of the rdoUnitMetric radio button:

&#124; 1234 &#124; private void rdoUnitMetric_Click( object sender, EventArgs e){    Multiplier = 1.0;} &#124;

And for US (Britain) unit, Multiplier is set to the Click event procedure of rdoUnitUS :

&#124; 1234 &#124; private void rdoUnitUS_Click( object sender, EventArgs e){    Multiplier = 3.2808;} &#124;

This states that one meter is equal to 3.2808 feet. |
| Step 5 | The key element in simpulation program is timer control ( timDrone ). This timer is used to update elapsed time, all values ​​calculated, and all graphic elements of the program. At this initialization stage, you only use it to update the time. Add this declaration at the form level: 

&#124; 1 &#124; double time; &#124;

Time is then updated in the Tick even procedure of timDrone control:

&#124; 123456 &#124; private void timDrone_Tick( object sender, EventArgs e){    time += Convert.ToDouble(timDrone.Interval) / 1000;    lblTime.Text = String.Format( "{0:f1}" , time);    lblTime.Refresh();} &#124;

You now have an Interval property of 500 milliseconds, so update is done every 0.5 second. |
| Step 6 | Now, you will start writing code to start, pause, restart, and stop the game. You will also write code to exit the program. Before doing so, you need to learn what happens at each difficulty level: 
*   Beginner : There is no lateral thrust control; no use of fuel.
*   Trainee : There is no vertical thrust control; no use of fuel.
*   Junior : All thrust controls are available; no use of fuel.
*   Senior , Advanced : All thrust controls are available; there is use of fuel.

If Auto-Pilot is on, you don't have thrust controls, so the label that says Auto-Pilot On will be made visible. Therefore, when the game starts, a number of different controls will/will not be displayed.There are two game controller buttons, btnStartPause and btnExitStop . These two buttons have certain interactions. The btnStartPause control can have three possible values ​​for the Text property. If the Text property is Start Game when clicked, the game will be initialized and switched to play mode using:

*   Change the Text property of btnStartPause to Pause Game .
*   Change the Text property of btnExitStop to Stop Game .
*   Set Visible property of grpLevel and grpUnit to False .
*   Set Visible property of grpControl to True .
*   If LevelDifficulty = 1 , then: set the Text property of grpControl to Beginner ; remove the fuel lever btnThrustLeft and btnThrustRight .
*   If LevelDifficulty = 2 , then: set the Text property of grpControl to Trainee ; remove the fuel lever btnThrustDown .
*   If LevelDifficulty = 3 , then: set the Text property of grpControl to Junior ; remove the fuel lever.
*   If LevelDifficulty = 4 , then: set the Text property of grpControl to Senior .
*   If LevelDifficulty = 5 , then: set the Text property of grpControl to Advanced .
*   If Auto-Pilot is checked, then: remove btnThrustLeft , btnThrustDown , btnThrustRight ; set the Visible property of lblMessage to True .
*   Determine lblPosition and lblVel ​​based on unit selection.
*   Initialize Time to zero.
*   Enable timDrone control.

When the Text property of btnStartPause is Pause Game and the button is clicked, the game enters pause mode:

*   Change the Text property to Start Again .
*   Disable btnExitStop .
*   Disable grpControl .
*   Disable timDrone control.

When the Text property of btnStartPause is Start Again and the button is clicked, the game enters play mode:

*   Change the Text property to Pause Game .
*   Enable btnExitStop .
*   Enable grpControl.
*   Enable timDrone control.

The code that implements these steps is placed in the Click event procedure of the btnStartPause control:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        grpLevel.Visible = false ;        grpUnit.Visible = false ;        grpControl.Visible = true ;        switch (levelDifficulty)        {            case 1:                grpControl.Text = "Landing Control-Beginner" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = false ;                btnThrustRight.Visible = false ;                btnThrustDown.Visible = true ;                break ;            case 2:                grpControl.Text = " Landing Control-Trainee" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = false ;                break ;            case 3:                grpControl.Text = " Landing Control-Junior" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 4:                grpControl.Text = " Landing Control-Senior" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 5:                grpControl.Text = " Landing Control-Advanced" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;        }        if (chkAutoPilot.Checked)        {            btnThrustLeft.Visible = false ;            btnThrustRight.Visible = false ;            btnThrustDown.Visible = false ;            lblMessage.Text = "Auto-Pilot On" ;            lblMessage.Visible = true ;        }        else        {            lblMessage.Visible = false ;        }        if (rdoUnitMetric.Checked)        {            lblPosition.Text = "Position (m)" ;            lblVel.Text = "Vel. (m/sec)" ;        }        else        {            lblPosition.Text = "Position (feet)" ;            lblVel.Text = "Vel. (feet/sec)" ;        }        time = 0.0;        lblTime.Text = "0.0" ;        timDrone.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        grpControl.Enabled = false ;        timDrone.Enabled = false ;    }    else    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        grpControl.Enabled = true ;        timDrone.Enabled = true ;    }} &#124;

 |
| Step 7 | Save and run the project. Perform each combination of the Difficulty Level, Auto-Pilot, and Unit Level selection. Make sure after clicking Start Game , the landing control group box displays the appropriate controls. Make sure the time increases with 0.5 seconds increment, as shown in Figure 4.8.![](Image00046.jpg)Figure 4.8 User chooses Junior optionAs desired, all thrust controls and fuel levers are displayed, when user selects junior difficulty level. Make sure Pause Game and Start Again buttons affect the displayed clock. The Stop Game button doesn't work yet, therefore, you will fix it. |
| Step 8 | When the user clicks Stop Game button, the following things are done: 
*   Change the Text property of btnExitStop to Exit .
*   Change the Text property of btnStartPause to Start Game .
*   Set the Visible property of grpLevel and grpUnit to True .
*   Set the Visible property of grpControl to False .
*   Disable timDrone control.

If btnExitStop is clicked when its Text property is Exit , the program will stop.The code to implement the steps above is placed in the Click event procedure of btnExitStop :

&#124; 12345678910111213141516 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        grpLevel.Visible = true ;        grpUnit.Visible = true ;        grpControl.Visible = false ;        timDrone.Enabled = false ;    }    else    {        this .Close();    }} &#124;

Save and run the project. You can now start the game, pause it, start it again, and stop the game. You can also exit the program. Make sure everything works properly as desired. Next, you will write code to implement the mathematics and physics behind the movement of the drone. |
| Step 9 | You will now start to learn a little about physics and mathematics. You will learn some equations that explain the position and speed of landing drone. As a first step, you need to define a coordinate system to do the calculation. It is assumed that graphic elements (drone, booster fire, pad, and background) are loaded in a rectangular region called Landscape .![](Image00047.jpg)A point in this region is specified by a Cartesian pair (x, y). In the diagram, notice the x (horizontal) coordinates increase from left to right, starting from 0 to Landscape.Width - 1 . The y (vertical) coordinates increase from top to bottom, from 0 to Landscape.Height - 1 . All measurements involve integers and in pixel units. In this program, it is assumed that one pixel is related to one meter distance.Each graphic element is also contained in a rectangular structure. The drone element ( Drone ) is located in the Cartesian pair ( DroneX , DroneY ) inside the rectangular Landscape :![](Image00048.jpg)Drone has Drone.Width width and Drone.Height height. DroneX and DroneY are assigned initial values ​​(at Time = 0 ). Drone speed is DroneXVel ​​and DroneYVel , which are initially given a zero value.After the initial values ​​for DroneX , DroneY , DroneXVel , and DroneYVel ​​are given, everything is updated (incremented or decremented) at certain times. Speed ​​is updated when thrusters are used. The speed and position are updated with each change from the starting time, which is set by timDrone control.The vertical thruster only affect vertical speed, DroneYVel . This thruster produces a change in velocity called YDelta , where the equation for changing the speed in the y-direction when the thruster is applied is: DroneYVel ​​-= YDelta , with the bottom thruster applied. Vertical thruster (bottom) slow down the vertical speed, so it can be used for proper landing.Horizontal thruster only affect horizontal speed, DroneXVel . This thruster produces a speed change called XDelta , where the equation for changing the speed in the x-direction when the thruster is applied is: DroneXVel ​​+= XDelta , with the left thruster applied and DroneXVel ​​-= XDelta , with the right thruster applied.The left thruster slows the drone moves towards the right; the right thruster slows the drone towards the left.By knowing the horizontal speed ( DroneXVel ) and vertical speed ( DroneYVel ), how do you know the position of DroneX and DroneY ? You will use the classic formula: Distance = Speed ​​x TravelTime .This equation is derived from a branch of mathematics known as Calculus. This calculation is done every time the timer updates it (in the Tick event of the timDrone ). Suppose that T is the interval of the timer control in seconds: T = timDrone.Interval / 1000, then the X and Y positions of the drone are updated each time cycle using: DroneX += DroneXVel * T and DroneY += DroneYVel * T .You certainly know that DroneXVel * T is the horizontal distance traveled by drone at one time cycle and DroneYVel * T is the horizontal distance traveled by drone at one time cycleVertical speed ( DroneYVel ) also changes at each time cycle. Gravity tends to increase when the drone approaches the surface. If the speed of gravity is Gravity, in T second, the speed increases according to: DroneYVel ​​+ = Gravity * T .You can also change the horizontal speed ( DroneXVel ) at each time cycle. If you apply horizontal thruster in one direction, the drone will continue in the direction of that driving thrust in the other direction applied. To counter this effect, if the drone moves horizontally, you can use the term "drag" to slow it down, even without a thruster. If the dragging constant is Drag , the resulting speed correction is DroneXVel​ ​-= Drag , if DroneXVel > 0 , and DroneXVel ​​+ = Drag , if DroneXVel ​​<0 .This concludes the updating equations for the position and speed of the drone. You then modify the project to include these equations. Add four form level variables to calculate position and speed: 

&#124; 12 &#124; double DroneX, DroneY;double DroneXVel, DroneYVel; &#124;

 |
| Step 10 | Initialize those variables in the Click event procedure of btnStartPause . For now, you set all of these variables to zero. Later, you will randomly assign DroneX : 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        grpLevel.Visible = false ;        grpUnit.Visible = false ;        grpControl.Visible = true ;        switch (levelDifficulty)        {            case 1:                grpControl.Text = "Landing Control-Beginner" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = false ;                btnThrustRight.Visible = false ;                btnThrustDown.Visible = true ;                break ;            case 2:                grpControl.Text = " Landing Control-Trainee" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = false ;                break ;            case 3:                grpControl.Text = " Landing Control-Junior" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 4:                grpControl.Text = " Landing Control-Senior" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 5:                grpControl.Text = " Landing Control-Advanced" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;        }        if (chkAutoPilot.Checked)        {            btnThrustLeft.Visible = false ;            btnThrustRight.Visible = false ;            btnThrustDown.Visible = false ;            lblMessage.Text = "Auto-Pilot On" ;            lblMessage.Visible = true ;        }        else        {            lblMessage.Visible = false ;        }        if (rdoUnitMetric.Checked)        {            lblPosition.Text = "Position (m)" ;            lblVel.Text = "Vel. (m/sec)" ;        }        else        {            lblPosition.Text = "Position (feet)" ;            lblVel.Text = "Vel. (feet/sec)" ;        }        time = 0.0;        lblTime.Text = "0.0" ;        DroneX = 0; DroneY = 0;        DroneXVel = 0; DroneYVel = 0;        timDrone.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        grpControl.Enabled = false ;        timDrone.Enabled = false ;    }    else    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        grpControl.Enabled = true ;        timDrone.Enabled = true ;    }} &#124;

 |
| Step 11 | Next, add four form-level constants to define changes in speed, gravity, and dragging effect: 

&#124; 1234 &#124; const double XDelta = 1.2;const double YDelta = 2.4;const double Gravity = 9.8 / 6.0;const double Drag = 0.1; &#124;

Each of these constants is found by trial and error. You can change it if you like.The vertical thruster is controlled by the btnThrustDown control. The Click event procedure for this control is:

&#124; 1234 &#124; private void btnThrustDown_Click( object sender, EventArgs e){        DroneYVel -= YDelta} &#124;

This will update the vertical speed due to the thruster.The horizontal thruster is controlled by the btnThrustLeft and btnThrustRight controls. The Click event procedure for these controls are:

&#124; 123456789 &#124; private void btnThrustLeft_Click( object sender, EventArgs e){      DroneXVel += XDelta}private void btnThrustRight_Click( object sender, EventArgs e){    DroneXVel -= XDelta} &#124;

These routines update the horizontal speed due to left and right thrusters. |
| Step 12 | Remember that the position and speed of the drone are updated on the Tick event of timDrone control. The steps carried out in this procedure: 
*   Update displayed time (already implemented).
*   Update DroneX and DroneY .
*   Display the status of the drone.
*   Update DroneXVel ​​and DroneYVel .

You use a procedure ( UpdateStatus ) to display the status of the drone. For the time being, this procedure only displays position and speed information (which is converted to certain unit using the Multiplier variable):

&#124; 12345678910111213 &#124; private void UpdateStatus(){    lblVPosition.Text = String.Format( "{0:f0}" , DroneY * Multiplier);    lblHPosition.Text = String.Format( "{0:f0}" , DroneX * Multiplier);    lblVVel.Text = String.Format( "{0:f1}" , -DroneYVel * Multiplier);    lblHVel.Text = String.Format( "{0:f1}" , DroneXVel * Multiplier);    lblVVel.Refresh();   lblHVel.Refresh();   lblVPosition.Refresh();   lblHPosition.Refresh();} &#124;

 |
| Step 13 | With the above function, modify Tick event of timDrone control that implement the new steps as follows: 

&#124; 12345678910111213141516171819 &#124; private void timDrone_Tick( object sender, EventArgs e){    time += Convert.ToDouble(timDrone.Interval) / 1000;    lblTime.Text = String.Format( "{0:f1}" , time);    lblTime.Refresh();    DroneX += DroneXVel * Convert.ToDouble(timDrone.Interval)/1000;    DroneY += DroneYVel * Convert.ToDouble(timDrone.Interval) / 1000;    UpdateStatus();    // Horizontal dragging    if (DroneXVel > 0)        DroneXVel -= Drag;    else if (DroneXVel < 0)        DroneXVel += Drag;    // Graivity    DroneYVel += Gravity * Convert.ToDouble(timDrone.Interval) / 1000;} &#124;

Additionally, return to the Click event from btnStartPause and add this line of code after initializing the speed and position of the drone: UpdateStatus() . This initializes the displays correctly. |
| Step 14 | Save and run the project. Choose Junior level. Click Start Game . Time will be incremented, as will position and speed in the vertical direction (labeled with Altitude ). Click on down thruster button and see that the vertical speed decrease. Try horizontal thrusters to ensure that you can move the drone left and right, as shown in Figure 4.9.![](Image00049.jpg)Figure 4.9 User now can update position and speed of the drone |
| Step 15 | As noted, the displayed values ​​do not answer the question how far is the drone from the landing pad. You are about to add a graphic element, Pad . The Pad element (a rectangular structure) is placed at a location ( Pad X, PadY ), with the width of the Pad.Width and height of the Pad.Height :![](Image00050.jpg)In this sketch, you add two distances. Altitude determines how far the drone is above the landing pad. This is the distance of the drone to the center of the runway: Altitude = (Landscape.Height - Pad.Height / 2) - (DroneY + Drone.Height) . Notice Altitude decreases when drone goes down ( DroneY increases). Altitude represents the height above the pad, which approaches zero when the drone gets closer to the runway.![D:\2___VB For Students\VB Projects\Mendarat di Mars\Mendarat di Mars\bin\Debug\landscape.jpg](Image00051.jpg)Figure 4.10 Landscape imageAnother distance, Lateral , sets the horizontal distance of the drone to the runway (pad). This is the middle distance of the drone to the center of the pad: Lateral = (DroneX + Drone.Width) - (PadX + Pad.Width) .Note that Lateral is positive if the drone is on the right side of the pad, negative if it is on the left of the pad. Lateral is zero if the drone is directly above the pad.You can add these equations to the program to get the value ​​of Altitude and Lateral , but one problem remains. You do not know the size of each image used. You will solve this now. You will use five images in the program: Landscape, Drone, Pad, HThrust, and VThrust. You will see each of these images.Landscape image ( landscape.jpg ) is an image with a width of 676 pixels and a height of 732 pixels, as shown in Figure 4.10.Drone Image (drone.png) is an image with a width of 105 pixels and a height of 115 pixels, as shown in Figure 4.11.![D:\2___VB For Students\VB Projects\Mendarat di Mars\Mendarat di Mars\bin\Debug\drone.png](Image00052.jpg)Figure 4.11 Drone imageThe Pad image (pad.png) is an image with a width of 143 pixels and a height of 64 pixels, as shown in Figure 4.12.![D:\2___VB For Students\VB Projects\Mendarat di Mars\Mendarat di Mars\bin\Debug\pad.png](Image00053.jpg)Figure 4.12 Pad imageHThrust image ( hthrust.png ) is an image with a width of 32 pixels and a height of 16 pixels. VThrust image ( vthrust.png ) is an image with a width of 24 pixels and a height of 32 pixels, as shown in Figure 4.13.![D:\2___VB For Students\VB Projects\Mendarat di Mars\Mendarat di Mars\bin\Debug\hthrust.png](Image00054.jpg) ![D:\2___VB For Students\VB Projects\Mendarat di Mars\Mendarat di Mars\bin\Debug\vthrust.png](Image00055.jpg)Figure 4.13 HThrust and VThrust imagesIn the program, each image is represented by an Image object. In the meantime, you only need to load it into the program to get the required dimensions ( Width and Height ). Later, you will use it in the landing animation. Add the following declarations at the form-level: 

&#124; 12345 &#124; Image Landscape;Image Drone;Image Pad;Image HThrust;Image VThrust; &#124;

 |
| Step 16 | To specify an Image object using a graphic file, you use the FromFile method. You do this in the Load event procedure of the form: 

&#124; 1234567891011 &#124; private void FormDroneSimulation_Load( object sender, EventArgs e){    Landscape = Image.FromFile(Application.StartupPath +        "\\landscape.jpg" );    Drone = Image.FromFile(Application.StartupPath + "\\drone.png" );    Pad = Image.FromFile(Application.StartupPath + "\\pad.png" );    HThrust = Image.FromFile(Application.StartupPath +        "\\hthrust.png" );    VThrust = Image.FromFile(Application.StartupPath +        "\\vthrust.png" );} &#124;

This code assumes you have copied the graphic files to the bin\Debug folder. |
| Step 17 | Now that you have the images and their dimensions, you can now modify the code to include calculations to display Altitude and Lateral . First, add the following form-level declarations: 

&#124; 12 &#124; double PadX, PadY;double Altitude, Lateral; &#124;

Calculations for Altitude and Lateral are placed in the general procedure UpdateStatus . Modify this procedure:

&#124; 12345678910111213141516171819202122232425 &#124; private void UpdateStatus(){    Altitude = (Landscape.Height - Pad.Height / 2) –        (DroneY + Drone.Height);    Lateral = (DroneX + Drone.Width / 2) - (PadX + Pad.Width / 2);    if (Altitude > 0)        lblVPosition.Text = String.Format( "{0:f0}" ,            Altitude * Multiplier);    else        lblVPosition.Text = "0" ;    if (Math.Abs(Lateral) < 1)        lblHPosition.Text = "Above" ;    else        lblHPosition.Text = String.Format( "{0:f0}" ,            Lateral * Multiplier);    lblVVel.Text = String.Format( "{0:f1}" , -DroneYVel * Multiplier);    lblHVel.Text = String.Format( "{0:f1}" , DroneXVel * Multiplier);    lblVVel.Refresh();   lblHVel.Refresh();   lblVPosition.Refresh();   lblHPosition.Refresh();} &#124;

You now have equations for calculating Altitude and Lateral . For vertical position labels, DroneY is replaced by Altitude (by limiting the value to zero). On the horizontal speed label, a negative sign is added to indicate a negative speed that indicates a reduced altitude. For horizontal position, DroneX is replaced by Lateral . |
| Step 18 | You can actually test the project now. However, you need to place the pad on the landscape. With each new game, you will randomly set the horizontal position of the pad (and drone) in the rectangular landscape. The pad will be placed under the rectangular landscape. Add the following random object at the form-level: 

&#124; 1 &#124; Random MyRandom = new Random(); &#124;

Then, modify the Click event of btnStartPause control:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        grpLevel.Visible = false ;        grpUnit.Visible = false ;        grpControl.Visible = true ;        switch (levelDifficulty)        {            case 1:                grpControl.Text = "Landing Control-Beginner" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = false ;                btnThrustRight.Visible = false ;                btnThrustDown.Visible = true ;                break ;            case 2:                grpControl.Text = " Landing Control-Trainee" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = false ;                break ;            case 3:                grpControl.Text = " Landing Control-Junior" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 4:                grpControl.Text = " Landing Control-Senior" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 5:                grpControl.Text = " Landing Control-Advanced" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;        }        if (chkAutoPilot.Checked)        {            btnThrustLeft.Visible = false ;            btnThrustRight.Visible = false ;            btnThrustDown.Visible = false ;            lblMessage.Text = "Auto-Pilot On" ;            lblMessage.Visible = true ;        }        else        {            lblMessage.Visible = false ;        }        if (rdoUnitMetric.Checked)        {            lblPosition.Text = "Position (m)" ;            lblVel.Text = "Vel. (m/sec)" ;        }        else        {            lblPosition.Text = "Position (feet)" ;            lblVel.Text = "Vel. (feet/sec)" ;        }        time = 0.0;        lblTime.Text = "0.0" ;        DroneX = (Landscape.Width - Drone.Width) *            MyRandom.NextDouble();        DroneY = 0;        DroneXVel = 0; DroneYVel = 0;        PadX = (Landscape.Width - Pad.Width) *            MyRandom.NextDouble();        PadY = Landscape.Height - Pad.Height;        UpdateStatus();        timDrone.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        grpControl.Enabled = false ;        timDrone.Enabled = false ;    }    else    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        grpControl.Enabled = true ;        timDrone.Enabled = true ;    }} &#124;

These new lines of code randomly place drone and pad within the boundaries of the Landscape image’s width. |
| Step 19 | Save and run the project. Select the Junior difficulty level and click Start Game . You can now see the altitude go down when the speed becomes greater (negative because it decreases). The lateral position will be near zero when the drone gets closer to the pad. |
| Step 20 | If you continue to run the simulation, Altitude will stop at zero, but the speed will continue to increase and you can still apply the thrust. You need a way to detect landing and determine whether landing is safe or not. You will do this during the Tick event procedure of timDrone control. Add this constant declaration at the form-level to define the maximum acceptable landing speed: 

&#124; 1 &#124; const double VelLandingSafe = 3.0; &#124;

Now, modify the Tick event of timDrone control:

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253 &#124; private void timDrone_Tick( object sender, EventArgs e){    time += Convert.ToDouble(timDrone.Interval) / 1000;    lblTime.Text = String.Format( "{0:f1}" , time);    lblTime.Refresh();    DroneX += DroneXVel * Convert.ToDouble(timDrone.Interval)/1000;    DroneY += DroneYVel * Convert.ToDouble(timDrone.Interval) / 1000;    UpdateStatus();    // Checks landing    if (Altitude <= 0)    {        timDrone.Enabled = false ;        btnThrustLeft.Visible = false ;        btnThrustRight.Visible = false ;        btnThrustDown.Visible = false ;        if (chkAutoPilot.Checked)            lblMessage.Text = "Auto-Pilot " ;        else        {            lblMessage.Text = "You " ;            lblMessage.Visible = true ;        }        // Crash?        if (DroneYVel > VelLandingSafe)        {            lblMessage.Text += "Crash!" ;        }        else        {            lblMessage.Text += "Land Safely" ;        }        // Makes btnFinish visible        btnStartPause.Visible = false ;        btnExitStop.Visible = false ;        btnFinish.Visible = true ;        return ;    }    // Horizontal dragging    if (DroneXVel > 0)        DroneXVel -= Drag;    else if (DroneXVel < 0)        DroneXVel += Drag;    // Graivity    DroneYVel += Gravity * Convert.ToDouble(timDrone.Interval) / 1000;} &#124;

In this code, after Altitude has reached zero, timDrone will be disabled, thruster buttons will be removed and certain landing message will be displayed based on vertical speed (and based on whether auto-pilot is enabled or not). |
| Step 21 | Save and run the project again. Now, when the altitude of the drone reaches zero, the program will stop and display the landing status. |
| Step 22 | Note the ( btnFinish ) button at the bottom can be clicked to continue the game. If you click on that button, nothing happens. You need to write the code for it.Add this code to the Click event procedure of the btnFinish button: 

&#124; 1234567 &#124; private void btnFinish_Click( object sender, EventArgs e){    btnFinish.Visible = false ;    btnStartPause.Visible = true ;    btnExitStop.Visible = true ;    btnExitStop.PerformClick();} &#124;

The code only re-assigns buttons to control the game so that options can be re-selected via clicking btnExitStop . If you try the game again, you can now use btnFinish . |
| Step 23 | Although no penalty is given if the landing fails, you need to know during the flight how close the drone is to the pad. One indication is the position value displayed on the label control. Graphic indicator will be very helpful. The first graphic indicator to be used are the green ( lblDrone ) and red ( lblPad ) labels on the panel ( pnlGuide ) under the trajectory panel.The green square represents the horizontal position of the drone, while the red square represents the landing pad. The midpoint of each label control in the guide will coincide with the middle of the drone image and the pad image in the landscape panel. Or, with a simple calculation of the Left propertiy, you get:lblDrone.Left = (DroneX + Drone.Width / 2) * (pnlGuide.Width / Landscape.Width) - lblDrone.Width / 2 and lblPad.Left = (PadX + Pad.Width / 2) * (pnlGuide.Width / Landscape.Width) - lblPad.Width / 2.Add these two equations to the end of the UpdateStatus procedure. 

&#124; 123456789101112131415161718192021222324252627282930 &#124; private void UpdateStatus(){    Altitude = (Landscape.Height - Pad.Height / 2) –        (DroneY + Drone.Height);    Lateral = (DroneX + Drone.Width / 2) - (PadX + Pad.Width / 2);    if (Altitude > 0)        lblVPosition.Text = String.Format( "{0:f0}" ,            Altitude * Multiplier);    else        lblVPosition.Text = "0" ;    if (Math.Abs(Lateral) < 1)        lblHPosition.Text = "Above" ;    else        lblHPosition.Text = String.Format( "{0:f0}" ,            Lateral * Multiplier);    lblVVel.Text = String.Format( "{0:f1}" , -DroneYVel * Multiplier);    lblHVel.Text = String.Format( "{0:f1}" , DroneXVel * Multiplier);    lblVVel.Refresh();    lblHVel.Refresh();    lblVPosition.Refresh();    lblHPosition.Refresh();    lblDrone.Left = Convert.ToInt32((DroneX + Drone.Width / 2) *        pnlGuide.Width / Landscape.Width - lblDrone.Width / 2);    lblPad.Left = Convert.ToInt32((PadX + Pad.Width / 2) *        pnlGuide.Width / Landscape.Width - lblPad.Width / 2);} &#124;

Save and run the project. Green and red squares will indicate the horizontal location of the lander against the pad. |
| Step 24 | This simulation is becoming more perfect. The last big challenge is to add graphic features. Before doing so, you need to add a few more changes.Some changes related to Difficulty Level need to be implemented. First, the two highest levels (Senior and Advanced) have limited fuel. You have added a code that displays fuel lever for these levels. You now need a code that calculates fuel usage and displays the remaining fuel on the lever. Add the following declaration at the form level to track the remaining fuel: 

&#124; 1 &#124; double RemFuel; &#124;

And, add the following three constants to the form-level:

&#124; 123 &#124; const double MaxFuel = 100;const double HFuel = 0.5;const double VFuel = 1.0; &#124;

The MaxFuel constant is initial fuel, HFuel is fuel that is burnt on horizontal thrust, and VFuel is fuel that is burnt on vertical thrust.Fuel and fuel lever are initialized in the Click event procedure of the btnStartPause control:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        grpLevel.Visible = false ;        grpUnit.Visible = false ;        grpControl.Visible = true ;        switch (levelDifficulty)        {            case 1:                grpControl.Text = "Landing Control-Beginner" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = false ;                btnThrustRight.Visible = false ;                btnThrustDown.Visible = true ;                break ;            case 2:                grpControl.Text = " Landing Control-Trainee" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = false ;                break ;            case 3:                grpControl.Text = " Landing Control-Junior" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 4:                grpControl.Text = " Landing Control-Senior" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 5:                grpControl.Text = " Landing Control-Advanced" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;        }        if (chkAutoPilot.Checked)        {            btnThrustLeft.Visible = false ;            btnThrustRight.Visible = false ;            btnThrustDown.Visible = false ;            lblMessage.Text = "Auto-Pilot On" ;            lblMessage.Visible = true ;        }        else        {            lblMessage.Visible = false ;        }        if (rdoUnitMetric.Checked)        {            lblPosition.Text = "Position (m)" ;            lblVel.Text = "Vel. (m/sec)" ;        }        else        {            lblPosition.Text = "Position (feet)" ;            lblVel.Text = "Vel. (feet/sec)" ;        }        time = 0.0;        lblTime.Text = "0.0" ;        DroneX = (Landscape.Width - Drone.Width) *            MyRandom.NextDouble();        DroneY = 0;        DroneXVel = 0; DroneYVel = 0;        PadX = (Landscape.Width - Pad.Width) *            MyRandom.NextDouble();        PadY = Landscape.Height - Pad.Height;        RemFuel = MaxFuel;        barFuel.Value = 100;        UpdateStatus();        timDrone.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        grpControl.Enabled = false ;        timDrone.Enabled = false ;    }    else    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        grpControl.Enabled = true ;        timDrone.Enabled = true ;    }} &#124;

Note that you set barFuel value to 100 (100% percent of the full tank) regardless of difficulty level. For four levels other than Senior and Advanced, barFuel is not displayed on the form, so this line of code has no effect. In addition, for these levels, you leave the rest of the fuel at the maximum fuel value, so that the fuel tank is always full. |
| Step 25 | Fuel is consumed in every thrust that is done. Modify each Click event of the thruster controls ( btnThrustDown , btnThrustLeft , and btnThrustRight ): 

&#124; 12345678910 &#124; private void btnThrustDown_Click( object sender, EventArgs e){               if (RemFuel > 0)    {        DroneYVel -= YDelta;        if (levelDifficulty > 3)            RemFuel -= VFuel;    }} &#124;

&#124; 12345678910 &#124; private void btnThrustLeft_Click( object sender, EventArgs e){    if (RemFuel > 0)    {        DroneXVel += XDelta;        if (levelDifficulty > 3)            RemFuel -= HFuel;    }} &#124;

&#124; 12345678910 &#124; private void btnThrustRight_Click( object sender, EventArgs e){    if (RemFuel > 0)    {        DroneXVel -= XDelta;        if (levelDifficulty > 3)            RemFuel -= HFuel;    }} &#124;

With these changes, thrust cannot be done when there is no fuel left and RemFuel is decremented only when the difficulty level is greater than 3 (Senior and Advanced). |
| Step 26 | Then, the fuel lever is updated in the UpdateStatus procedure. To give an audio effect, you make a certain sound when the fuel remaining is less than 10%: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637 &#124; private void UpdateStatus(){    Altitude = (Landscape.Height - Pad.Height / 2) –        (DroneY + Drone.Height);    Lateral = (DroneX + Drone.Width / 2) - (PadX + Pad.Width / 2);    if (Altitude > 0)        lblVPosition.Text = String.Format( "{0:f0}" ,            Altitude * Multiplier);    else        lblVPosition.Text = "0" ;    if (Math.Abs(Lateral) < 1)        lblHPosition.Text = "Above" ;    else        lblHPosition.Text = String.Format( "{0:f0}" ,            Lateral * Multiplier);    lblVVel.Text = String.Format( "{0:f1}" , -DroneYVel * Multiplier);    lblHVel.Text = String.Format( "{0:f1}" , DroneXVel * Multiplier);    lblVVel.Refresh();    lblHVel.Refresh();    lblVPosition.Refresh();    lblHPosition.Refresh();    lblDrone.Left = Convert.ToInt32((DroneX + Drone.Width / 2) *        pnlGuide.Width / Landscape.Width - lblDrone.Width / 2);    lblPad.Left = Convert.ToInt32((PadX + Pad.Width / 2) *        pnlGuide.Width / Landscape.Width - lblPad.Width / 2);    if (RemFuel > 0)        barFuel.Value = Convert.ToInt32(100 * RemFuel/MaxFuel);    else        barFuel.Value = 0;    if (barFuel.Value <= 10)        Console.Beep();} &#124;

 |
| Step 27 | Save and run the project. Choose Senior difficulty level. As the drone moves down, apply horizontal and vertical thrusters and notice how the fuel lever indicator drops. |
| Step 28 | At the lowest difficulty level ( Beginner ; LevelDifficulty = 1 ), the landing pad needs to be directly placed under the drone, because the two horizontal thrusters are not available. This is done in the Click event of the btnStartPause control: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        grpLevel.Visible = false ;        grpUnit.Visible = false ;        grpControl.Visible = true ;        switch (levelDifficulty)        {            case 1:                grpControl.Text = "Landing Control-Beginner" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = false ;                btnThrustRight.Visible = false ;                btnThrustDown.Visible = true ;                break ;            case 2:                grpControl.Text = " Landing Control-Trainee" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = false ;                break ;            case 3:                grpControl.Text = " Landing Control-Junior" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 4:                grpControl.Text = " Landing Control-Senior" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 5:                grpControl.Text = " Landing Control-Advanced" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;        }        if (chkAutoPilot.Checked)        {            btnThrustLeft.Visible = false ;            btnThrustRight.Visible = false ;            btnThrustDown.Visible = false ;            lblMessage.Text = "Auto-Pilot On" ;            lblMessage.Visible = true ;        }        else        {            lblMessage.Visible = false ;        }        if (rdoUnitMetric.Checked)        {            lblPosition.Text = "Position (m)" ;            lblVel.Text = "Vel. (m/sec)" ;        }        else        {            lblPosition.Text = "Position (feet)" ;            lblVel.Text = "Vel. (feet/sec)" ;        }        time = 0.0;        lblTime.Text = "0.0" ;        DroneX = (Landscape.Width - Drone.Width) *            MyRandom.NextDouble();        DroneY = 0;        DroneXVel = 0; DroneYVel = 0;        if (levelDifficulty != 1)            PadX = (Landscape.Width - Pad.Width) *                MyRandom.NextDouble();        else            PadX = (DroneX + Drone.Width / 2) - Pad.Width / 2;                  PadY = Landscape.Height - Pad.Height;        RemFuel = MaxFuel;        barFuel.Value = 100;        UpdateStatus();        timDrone.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        grpControl.Enabled = false ;        timDrone.Enabled = false ;    }    else    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        grpControl.Enabled = true ;        timDrone.Enabled = true ;    }} &#124;

Save and run the project. Select the Beginner level. Click on the Start Game button. Make sure the pad is right under the drone. |
| Step 29 | The last change that needs to be done in relation to difficulty level is related to the level of Advanced . At this level, you want the thrusters to have an unpredictable thrust, which results random push. For horizontal and vertical thrusters, you will have a value from 0 to twice the maximum speed delta. Modify the Click event of the three thrusters: 

&#124; 12345678910111213 &#124; private void btnThrustDown_Click( object sender, EventArgs e){               if (RemFuel > 0)    {        if (levelDifficulty != 5)            DroneYVel -= YDelta;        else            DroneYVel -= 2.0 * YDelta * MyRandom.NextDouble();        if (levelDifficulty > 3)            RemFuel -= VFuel;    }} &#124;

&#124; 12345678910111213 &#124; private void btnThrustLeft_Click( object sender, EventArgs e){    if (RemFuel > 0)    {        if (levelDifficulty != 5)            DroneXVel += XDelta;        else            DroneXVel += 2.0 * XDelta * MyRandom.NextDouble();         if (levelDifficulty > 3)            RemFuel -= HFuel;    }} &#124;

&#124; 12345678910111213 &#124; private void btnThrustRight_Click( object sender, EventArgs e){    if (RemFuel > 0)    {        if (levelDifficulty != 5)            DroneXVel -= XDelta;        else            DroneXVel -= 2.0 * XDelta * MyRandom.NextDouble();        if (levelDifficulty > 3)            RemFuel -= HFuel;    }} &#124;

 |
| Step 30 | Save and run the project. Try Advanced level and see how the fuel lever drops quickly. |
| Step 31 | At this point, the only thing needs to be modified in relation to the difficulty level is related to the level of Trainee ( LevelDifficulty = 2 ). At this level, you can only control horizontal thrusters to move the drone in the lateral direction. The vertical thrusters are controlled by a computer via auto-pilot. Since you haven't written the code for auto-pilot so far, you will definitely get into an accident at the Trainee level.Another one before you handle graphic effects is to add some sound. In the bin/Debug folder four wav files are provided. The vthrust.wav file is sounded when vertical thrusters are applied, hthrust.wav is played when horizontal thrusters are applied, safe.wav is sounded when a safe landing is successfully performed, and crash.wav is sounded when a landing accident occurs.Add the following declarations at the form-level: 

&#124; 1234 &#124; System.Media.SoundPlayer VSoundThrust;System.Media.SoundPlayer HSoundThrust;System.Media.SoundPlayer SoundSafeLanding;System.Media.SoundPlayer SoundCrashLanding; &#124;

The sounds are loaded in the Load event procedure of the form:

&#124; 1234567891011121314151617181920212223242526272829 &#124; private void FormDroneSimulation_Load( object sender, EventArgs e){    Landscape = Image.FromFile(Application.StartupPath +        "\\landscape.jpg" );    Drone = Image.FromFile(Application.StartupPath + "\\drone.png" );    Pad = Image.FromFile(Application.StartupPath + "\\pad.png" );    HThrust = Image.FromFile(Application.StartupPath +        "\\hthrust.png" );    VThrust = Image.FromFile(Application.StartupPath +        "\\vthrust.png" );    VSoundThrust = new        System.Media.SoundPlayer(Application.StartupPath +        "\\vthrust.wav" );    HSoundThrust = new        System.Media.SoundPlayer(Application.StartupPath +        "\\hthrust.wav" );    SoundSafeLanding = new        System.Media.SoundPlayer(Application.StartupPath +        "\\safe.wav" );    SoundCrashLanding = new        System.Media.SoundPlayer(Application.StartupPath +        "\\crash.wav" );    VSoundThrust.Load();    HSoundThrust.Load();    SoundSafeLanding.Load();    SoundCrashLanding.Load();} &#124;

 |
| Step 32 | Vertical thruster sound ( VSoundThrust ) is played when vertical thruster is applied, while horizontal thruster sound ( HSoundThrust ) is played when horizontal thrusters (left and right) are applied: 

&#124; 1234567891011121314 &#124; private void btnThrustDown_Click( object sender, EventArgs e){               if (RemFuel > 0)    {        VSoundThrust.Play();        if (levelDifficulty != 5)            DroneYVel -= YDelta;        else            DroneYVel -= 2.0 * YDelta * MyRandom.NextDouble();        if (levelDifficulty > 3)            RemFuel -= VFuel;    }} &#124;

&#124; 1234567891011121314 &#124; private void btnThrustLeft_Click( object sender, EventArgs e){    if (RemFuel > 0)    {        HSoundThrust.Play();        if (levelDifficulty != 5)            DroneXVel += XDelta;        else            DroneXVel += 2.0 * XDelta * MyRandom.NextDouble();         if (levelDifficulty > 3)            RemFuel -= HFuel;    }} &#124;

&#124; 1234567891011121314 &#124; private void btnThrustRight_Click( object sender, EventArgs e){    if (RemFuel > 0)    {        HSoundThrust.Play();        if (levelDifficulty != 5)            DroneXVel -= XDelta;        else            DroneXVel -= 2.0 * XDelta * MyRandom.NextDouble();        if (levelDifficulty > 3)            RemFuel -= HFuel;    }} &#124;

 |
| Step 33 | Landing sounds ( SoundSafeLanding and SoundCrashLanding ) are played after the landing, which is in the Tick event procedure of timDrone control: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354 &#124; private void timDrone_Tick( object sender, EventArgs e){    time += Convert.ToDouble(timDrone.Interval) / 1000;    lblTime.Text = String.Format( "{0:f1}" , time);    lblTime.Refresh();    DroneX += DroneXVel * Convert.ToDouble(timDrone.Interval)/1000;    DroneY += DroneYVel * Convert.ToDouble(timDrone.Interval) / 1000;    UpdateStatus();    // Checks landing    if (Altitude <= 0)    {        timDrone.Enabled = false ;        btnThrustLeft.Visible = false ;        btnThrustRight.Visible = false ;        btnThrustDown.Visible = false ;        if (chkAutoPilot.Checked)            lblMessage.Text = "Auto-Pilot " ;        else        {            lblMessage.Text = "You " ;            lblMessage.Visible = true ;        }        // Crash?        if (DroneYVel > VelLandingSafe)        {            SoundCrashLanding.PlaySync();            lblMessage.Text += "Crash!" ;        }        else        {            SoundSafeLanding.PlaySync();            lblMessage.Text += "Land Safely" ;        }        // Makes btnFinish visible        btnStartPause.Visible = false ;        btnExitStop.Visible = false ;        btnFinish.Visible = true ;        return ;    }    // Horizontal dragging    if (DroneXVel > 0)        DroneXVel -= Drag;    else if (DroneXVel < 0)        DroneXVel += Drag;    // Graivity    DroneYVel += Gravity * Convert.ToDouble(timDrone.Interval) / 1000;} &#124;

 |
| Step 34 | Save and run the project. Choose a difficulty level and play the simulation. Make sure you hear certain sound when thruster is applied. Make sure the safe landing will play safe landing sound, and the improper landing will play crash landing sound.Next, you will write the code for the path or trajectory panel under the label controls on the right side of the form. In this panel, you will draw a line that indicates the desired path from lander to pad. You will also describe the trajectory followed by the drone as it descends. |
| Step 35 | Now, you will draw a line on the trajectory panel. This line will connect the position of the initial drone with the position of the landing pad to provide the recommended trajectory to follow when making a landing. Steps that need to be done: 
*   Declare a Graphic object and name it as TrajectoryGraph .
*   Create an empty bitmap object for pnlTrajectory .
*   Create graphical object.
*   Create a Pen object (red pen with a width of 2 pixels).
*   At Time = 0.0 , remove the graphic object and draw a line (using DrawLine ) connecting the initial position of the drone to the position of the pad.

These steps are quite simple. The only thing that is not clear is the coordinates of the line. Look at the sketch of the starting position of the drone and the location of the pad on the Landscape element:![](Image00056.jpg)The line to draw connects the bottom center of the drone with the center of the pad. The Cartesian coordinate pair from the bottom of the lander is: X = DroneX + Drone.Width/2 and Y = DroneY + Drone.Height/2 . And the midpoint of the landing pad: X = PadX + Pad.Width / 2 and Y = PadY + Pad.Height / 2 .The coordinates are relative to the size of the Landscape element and you want to draw a line on pnlTrajectory . So, before drawing a line, you need to scale the X and Y coordinates to adjust the points in the pnlTrajectory . Each X coordinate must be multiplied by TrajectoryXScale , where TrajectoryXScale = pnlTrajectory.Width/Landscape.Width and Each Y coordinate must be multiplied by TrajectoryYScale , where TrajectoryYScale = pnlTrajectory.Height/Landscape.Height .You will then some modifications to draw the line. Add the following declaration to the form level:

&#124; 1 &#124; Graphics TrajectoryGraph; &#124;

Modify the Load event procedure of the form to create bitmap and graphic object:

&#124; 1234567891011121314151617181920212223242526272829303132333435 &#124; private void FormDroneSimulation_Load( object sender, EventArgs e){    Landscape = Image.FromFile(Application.StartupPath +        "\\landscape.jpg" );    Drone = Image.FromFile(Application.StartupPath + "\\drone.png" );    Pad = Image.FromFile(Application.StartupPath + "\\pad.png" );    HThrust = Image.FromFile(Application.StartupPath +        "\\hthrust.png" );    VThrust = Image.FromFile(Application.StartupPath +        "\\vthrust.png" );    pnlTrajectory. BackgroundImage = new Bitmap(pnlTrajectory.Width,        pnlTrajectory.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    TrajectoryGraph = Graphics.FromImage(        pnlTrajectory.BackgroundImage);    VSoundThrust = new        System.Media.SoundPlayer(Application.StartupPath +        "\\vthrust.wav" );    HSoundThrust = new        System.Media.SoundPlayer(Application.StartupPath +        "\\hthrust.wav" );    SoundSafeLanding = new        System.Media.SoundPlayer(Application.StartupPath +        "\\safe.wav" );    SoundCrashLanding = new        System.Media.SoundPlayer(Application.StartupPath +        "\\crash.wav" );    VSoundThrust.Load();    HSoundThrust.Load();    SoundSafeLanding.Load();    SoundCrashLanding.Load();} &#124;

 |
| Step 36 | Now, create a general procedure ( UpdateTrajectory ) to draw a trajectory path: 

&#124; 123456789101112131415161719202122232425 &#124; private void UpdateTrajectory(){    double TrajectoryXScale = Convert.ToDouble(        pnlTrajectory.Width) / Landscape.Width;    double TrajectoryYScale = Convert.ToDouble(        pnlTrajectory.Height) / Landscape.Height;    if (time == 0.0)    {        Pen tPen = new Pen(Color.Red, 2);        TrajectoryGraph.Clear(pnlTrajectory.BackColor);        TrajectoryGraph.DrawLine(tPen,            Convert.ToInt32(TrajectoryXScale *            (DroneX + Drone.Width / 2)),            Convert.ToInt32(TrajectoryYScale *            (DroneY+ Drone.Height)),            Convert.ToInt32(TrajectoryXScale *            (PadX + Pad.Width / 2)),            Convert.ToInt32(TrajectoryYScale *            (PadY + Pad.Height / 2)));    }    pnlTrajectory.Refresh();} &#124;

 |
| Step 37 | Modify the Click event procedure of btnStartPause to draw the recommended initial trajectory using the UpdateTrajectory procedure: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        grpLevel.Visible = false ;        grpUnit.Visible = false ;        grpControl.Visible = true ;        switch (levelDifficulty)        {            case 1:                grpControl.Text = "Landing Control-Beginner" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = false ;                btnThrustRight.Visible = false ;                btnThrustDown.Visible = true ;                break ;            case 2:                grpControl.Text = " Landing Control-Trainee" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = false ;                break ;            case 3:                grpControl.Text = " Landing Control-Junior" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 4:                grpControl.Text = " Landing Control-Senior" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 5:                grpControl.Text = " Landing Control-Advanced" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;        }        if (chkAutoPilot.Checked)        {            btnThrustLeft.Visible = false ;            btnThrustRight.Visible = false ;            btnThrustDown.Visible = false ;            lblMessage.Text = "Auto-Pilot On" ;            lblMessage.Visible = true ;        }        else        {            lblMessage.Visible = false ;        }        if (rdoUnitMetric.Checked)        {            lblPosition.Text = "Position (m)" ;            lblVel.Text = "Vel. (m/sec)" ;        }        else        {            lblPosition.Text = "Position (feet)" ;            lblVel.Text = "Vel. (feet/sec)" ;        }        time = 0.0;        lblTime.Text = "0.0" ;        DroneX = (Landscape.Width - Drone.Width) *            MyRandom.NextDouble();        DroneY = 0;        DroneXVel = 0; DroneYVel = 0;        if (levelDifficulty != 1)            PadX = (Landscape.Width - Pad.Width) *                MyRandom.NextDouble();        else            PadX = (DroneX + Drone.Width / 2) - Pad.Width / 2;                  PadY = Landscape.Height - Pad.Height;        RemFuel = MaxFuel;        barFuel.Value = 100;        UpdateStatus();        UpdateTrajectory();        timDrone.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        grpControl.Enabled = false ;        timDrone.Enabled = false ;    }    else    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        grpControl.Enabled = true ;        timDrone.Enabled = true ;    }} &#124;

 |
| Step 38 | Save and run the project. Select a pilot level and click Start Game . You can now see the trajectory to the pad on pnlTrajectory . |
| Step 39 | You are now modifying UpdateTrajectory procedure to draw a circle in the drone position when time is running. With this, you will have a trajectory that is followed by the drone when it makes a landing.The circle is centered at the bottom of the drone graph element. This point has been previously defined with: X = DroneX + Drone.Width/2 and Y = DroneY + Drone.Height . Remember that this position is relative to the landscape element so each point needs to be scaled to adjust the path.Modify UpdateTrajectory to draw a circle: 

&#124; 12345678910111213141516171920212223242526272829303132 &#124; private void UpdateTrajectory(){    double TrajectoryXScale = Convert.ToDouble(        pnlTrajectory.Width) / Landscape.Width;    double TrajectoryYScale = Convert.ToDouble(        pnlTrajectory.Height) / Landscape.Height;    Rectangle RectCircle = new        Rectangle(Convert.ToInt32(TrajectoryXScale *        (DroneX + Drone.Width / 2)) - 3,        Convert.ToInt32(TrajectoryYScale *        (DroneY + Drone.Height)) - 3, 6, 6);    if (time == 0.0)    {        Pen tPen = new Pen(Color.Red, 2);        TrajectoryGraph.Clear(pnlTrajectory.BackColor);        TrajectoryGraph.DrawLine(tPen,            Convert.ToInt32(TrajectoryXScale *            (DroneX + Drone.Width / 2)),            Convert.ToInt32(TrajectoryYScale *            (DroneY+ Drone.Height)),            Convert.ToInt32(TrajectoryXScale *            (PadX + Pad.Width / 2)),            Convert.ToInt32(TrajectoryYScale *            (PadY + Pad.Height / 2)));    }    TrajectoryGraph.DrawEllipse(Pens.LightGreen, RectCircle);    pnlTrajectory.Refresh();} &#124;

In the code, you create a Rectangle structure, which is centered on DroneX + Drone.Width / 2 , which contains a circle with a diameter of 6 pixels. Then, the ellipse is drawn using a cyan pen.The UpdateTrajectory procedure above is invoked at the Tick event of timDrone control:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455 &#124; private void timDrone_Tick( object sender, EventArgs e){    time += Convert.ToDouble(timDrone.Interval) / 1000;    lblTime.Text = String.Format( "{0:f1}" , time);    lblTime.Refresh();    DroneX += DroneXVel * Convert.ToDouble(timDrone.Interval)/1000;    DroneY += DroneYVel * Convert.ToDouble(timDrone.Interval) / 1000;    UpdateStatus();    UpdateTrajectory();    // Checks landing    if (Altitude <= 0)    {        timDrone.Enabled = false ;        btnThrustLeft.Visible = false ;        btnThrustRight.Visible = false ;        btnThrustDown.Visible = false ;        if (chkAutoPilot.Checked)            lblMessage.Text = "Auto-Pilot " ;        else        {            lblMessage.Text = "You " ;            lblMessage.Visible = true ;        }        // Crash?        if (DroneYVel > VelLandingSafe)        {            SoundCrashLanding.PlaySync();            lblMessage.Text += "Crash!" ;        }        else        {            SoundSafeLanding.PlaySync();            lblMessage.Text += "Land Safely" ;        }        // Makes btnFinish visible        btnStartPause.Visible = false ;        btnExitStop.Visible = false ;        btnFinish.Visible = true ;        return ;    }    // Horizontal dragging    if (DroneXVel > 0)        DroneXVel -= Drag;    else if (DroneXVel < 0)        DroneXVel += Drag;    // Graivity    DroneYVel += Gravity * Convert.ToDouble(timDrone.Interval) / 1000;} &#124;

 |
| Step 40 | Save and run the project. Select a difficulty level, then click Start Game . Try to make the landing safely using the thrusters provided. You will see that the trajectory panel provides a useful indication to show where the drone is relative to the pad. |
| Step 41 | Now, you will write the code to roll the background, then when that is done successfully, you will add a drone (and pad and thruster fires). Add the following declarations to the form level for new positioning variables and observational graphic object: 

&#124; 123 &#124; double LandscapeX, LandscapeY;double CentralX, CentralY;Graphics GraphicsView; &#124;

Modify the Load event procedure of the form to create GraphicsView and to calculate CentralX and CentralY :

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243 &#124; private void FormDroneSimulation_Load( object sender, EventArgs e){    Landscape = Image.FromFile(Application.StartupPath +        "\\landscape.jpg" );    Drone = Image.FromFile(Application.StartupPath + "\\drone.png" );    Pad = Image.FromFile(Application.StartupPath + "\\pad.png" );    HThrust = Image.FromFile(Application.StartupPath +        "\\hthrust.png" );    VThrust = Image.FromFile(Application.StartupPath +        "\\vthrust.png" );    pnlTrajectory. BackgroundImage = new Bitmap(pnlTrajectory.Width,        pnlTrajectory.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    TrajectoryGraph = Graphics.FromImage(        pnlTrajectory.BackgroundImage);    pnlView.BackgroundImage = new Bitmap(pnlView.Width,        pnlView.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    GraphicsView = Graphics. FromImage(pnlView.BackgroundImage);    VSoundThrust = new        System.Media.SoundPlayer(Application.StartupPath +        "\\vthrust.wav" );    HSoundThrust = new        System.Media.SoundPlayer(Application.StartupPath +        "\\hthrust.wav" );    SoundSafeLanding = new        System.Media.SoundPlayer(Application.StartupPath +        "\\safe.wav" );    SoundCrashLanding = new        System.Media.SoundPlayer(Application.StartupPath +        "\\crash.wav" );    VSoundThrust.Load();    HSoundThrust.Load();    SoundSafeLanding.Load();    SoundCrashLanding.Load();    CentralX = (pnlView.Width - Drone.Width) / 2;    CentralY = (pnlView.Height - Drone.Height) / 2;} &#124;

 |
| Step 42 | Add a general procedure ( UpdateView ) where you will place the code related to the landing animation: 

&#124; 123456789101112131415161718192021222324252627282930313233343536 &#124; private void UpdateView(){    Rectangle RectView = new Rectangle(0, 0,        pnlView.Width, pnlView.Height);    // Adjust landscape    LandscapeX = DroneX - CentralX;    if (LandscapeX <= 0)    {        LandscapeX = 0;    }    if (LandscapeX >= Landscape.Width - pnlView.Width)    {        LandscapeX = Landscape.Width - pnlView.Width;    }    LandscapeY = DroneY - CentralY;    if (LandscapeY <= 0)    {        LandscapeY = 0;    }    if (LandscapeY >= Landscape.Height - pnlView.Height)    {        LandscapeY = Landscape.Height - pnlView.Height;    }    // Draws landscape    Rectangle RectLandscape = new        Rectangle(Convert.ToInt32(LandscapeX),        Convert.ToInt32(LandscapeY), pnlView.Width,        pnlView.Height);    GraphicsView.DrawImage(Landscape, RectView,        RectLandscape, GraphicsUnit.Pixel);} &#124;

The above code determines LandscapeX and LandscapeY , then copies the related region of the landscape image to pnlView . |
| Step 43 | Modify the Click event procedure of btnStartPause to initialize the observation: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        grpLevel.Visible = false ;        grpUnit.Visible = false ;        grpControl.Visible = true ;        switch (levelDifficulty)        {            case 1:                grpControl.Text = "Landing Control-Beginner" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = false ;                btnThrustRight.Visible = false ;                btnThrustDown.Visible = true ;                break ;            case 2:                grpControl.Text = " Landing Control-Trainee" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = false ;                break ;            case 3:                grpControl.Text = " Landing Control-Junior" ;                lblFuel.Visible = false ;                barFuel.Visible = false ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 4:                grpControl.Text = " Landing Control-Senior" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;            case 5:                grpControl.Text = " Landing Control-Advanced" ;                lblFuel.Visible = true ;                barFuel.Visible = true ;                btnThrustLeft.Visible = true ;                btnThrustRight.Visible = true ;                btnThrustDown.Visible = true ;                break ;        }        if (chkAutoPilot.Checked)        {            btnThrustLeft.Visible = false ;            btnThrustRight.Visible = false ;            btnThrustDown.Visible = false ;            lblMessage.Text = "Auto-Pilot On" ;            lblMessage.Visible = true ;        }        else        {            lblMessage.Visible = false ;        }        if (rdoUnitMetric.Checked)        {            lblPosition.Text = "Position (m)" ;            lblVel.Text = "Vel. (m/sec)" ;        }        else        {            lblPosition.Text = "Position (feet)" ;            lblVel.Text = "Vel. (feet/sec)" ;        }        time = 0.0;        lblTime.Text = "0.0" ;        DroneX = (Landscape.Width - Drone.Width) *            MyRandom.NextDouble();        DroneY = 0;        DroneXVel = 0; DroneYVel = 0;        if (levelDifficulty != 1)            PadX = (Landscape.Width - Pad.Width) *                MyRandom.NextDouble();        else            PadX = (DroneX + Drone.Width / 2) - Pad.Width / 2;                  PadY = Landscape.Height - Pad.Height;        RemFuel = MaxFuel;        barFuel.Value = 100;        UpdateStatus();        UpdateTrajectory();        UpdateView();        timDrone.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        grpControl.Enabled = false ;        timDrone.Enabled = false ;    }    else    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        grpControl.Enabled = true ;        timDrone.Enabled = true ;    }} &#124;

 |
| Step 44 | And, modify the Tick event of timDrone control: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556 &#124; private void timDrone_Tick( object sender, EventArgs e){    time += Convert.ToDouble(timDrone.Interval) / 1000;    lblTime.Text = String.Format( "{0:f1}" , time);    lblTime.Refresh();    DroneX += DroneXVel * Convert.ToDouble(timDrone.Interval)/1000;    DroneY += DroneYVel * Convert.ToDouble(timDrone.Interval) / 1000;    UpdateStatus();    UpdateTrajectory();    UpdateView();    // Checks landing    if (Altitude <= 0)    {        timDrone.Enabled = false ;        btnThrustLeft.Visible = false ;        btnThrustRight.Visible = false ;        btnThrustDown.Visible = false ;        if (chkAutoPilot.Checked)            lblMessage.Text = "Auto-Pilot " ;        else        {            lblMessage.Text = "You " ;            lblMessage.Visible = true ;        }        // Crash?        if (DroneYVel > VelLandingSafe)        {            SoundCrashLanding.PlaySync();            lblMessage.Text += "Crash!" ;        }        else        {            SoundSafeLanding.PlaySync();            lblMessage.Text += "Land Safely" ;        }        // Makes btnFinish visible        btnStartPause.Visible = false ;        btnExitStop.Visible = false ;        btnFinish.Visible = true ;        return ;    }    // Horizontal dragging    if (DroneXVel > 0)        DroneXVel -= Drag;    else if (DroneXVel < 0)        DroneXVel += Drag;    // Graivity    DroneYVel += Gravity * Convert.ToDouble(timDrone.Interval) / 1000;} &#124;

 |
| Step 45 | Save and run the game. Select a difficulty level, then click the Start Game button. When you move the drone using a thruster, the landscape will now roll. |
| Step 46 | Placing the drone, pad and fire thruster graphics on the pnlView is a simple job once you know the background color. All code is placed in the general procedure UpdateView . Before modifying this procedure, you need to make a few changes. To add fire thruster graphics to an animation, you need to know whether the it is applied or not. Define the following three Boolean variables to tell whether a fire thruster is being used or not: 

&#124; 1 &#124; bool VThrustOn, LThrustOn, RThrustOn; &#124;

Then, in the Click event procedure of each thruster control button, set the value of these variables:

&#124; 123456789101112131415 &#124; private void btnThrustDown_Click( object sender, EventArgs e){               if (RemFuel > 0)    {        VSoundThrust.Play();        VThrustOn = true ;            if (levelDifficulty != 5)            DroneYVel -= YDelta;        else            DroneYVel -= 2.0 * YDelta * MyRandom.NextDouble();        if (levelDifficulty > 3)            RemFuel -= VFuel;    }} &#124;

&#124; 123456789101112131415 &#124; private void btnThrustLeft_Click( object sender, EventArgs e){    if (RemFuel > 0)    {        HSoundThrust.Play();        LThrustOn = true ;        if (levelDifficulty != 5)            DroneXVel += XDelta;        else            DroneXVel += 2.0 * XDelta * MyRandom.NextDouble();         if (levelDifficulty > 3)            RemFuel -= HFuel;    }} &#124;

&#124; 123456789101112131415 &#124; private void btnThrustRight_Click( object sender, EventArgs e){    if (RemFuel > 0)    {        HSoundThrust.Play();        RThrustOn = true ;        if (levelDifficulty != 5)            DroneXVel -= XDelta;        else            DroneXVel -= 2.0 * XDelta * MyRandom.NextDouble();        if (levelDifficulty > 3)            RemFuel -= HFuel;    }} &#124;

 |
| Step 47 | After landing, you need to make sure the thrusters are disabled. Modify the Tick event from the timDrone control: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162 &#124; private void timDrone_Tick( object sender, EventArgs e){    time += Convert.ToDouble(timDrone.Interval) / 1000;    lblTime.Text = String.Format( "{0:f1}" , time);    lblTime.Refresh();    DroneX += DroneXVel * Convert.ToDouble(timDrone.Interval)/1000;    DroneY += DroneYVel * Convert.ToDouble(timDrone.Interval) / 1000;    UpdateStatus();    UpdateTrajectory();    UpdateView();    // Checks landing    if (Altitude <= 0)    {        timDrone.Enabled = false ;        btnThrustLeft.Visible = false ;        btnThrustRight.Visible = false ;        btnThrustDown.Visible = false ;        VThrustOn = false ;        LThrustOn = false ;        RThrustOn = false ;        UpdateView();        if (chkAutoPilot.Checked)            lblMessage.Text = "Auto-Pilot " ;        else        {            lblMessage.Text = "You " ;            lblMessage.Visible = true ;        }        // Crash?        if (DroneYVel > VelLandingSafe)        {            SoundCrashLanding.PlaySync();            lblMessage.Text += "Crash!" ;        }        else        {            SoundSafeLanding.PlaySync();            lblMessage.Text += "Land Safely" ;        }        // Makes btnFinish visible        btnStartPause.Visible = false ;        btnExitStop.Visible = false ;        btnFinish.Visible = true ;        return ;    }    // Horizontal dragging    if (DroneXVel > 0)        DroneXVel -= Drag;    else if (DroneXVel < 0)        DroneXVel += Drag;    // Gravity    DroneYVel += Gravity * Convert.ToDouble(timDrone.Interval) / 1000;} &#124;

 |
| Step 48 | Note You need to update pnlView after all thrusters have been disabled. Now, modify the UpdateView procedure to draw the drone, pad and all thrusters (when active): 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273747576777879808182838485868788899091929394 &#124; private void UpdateView(){    Rectangle RectView = new Rectangle(0, 0,        pnlView.Width, pnlView.Height);    Rectangle RectDrone =        new Rectangle(Convert.ToInt32(CentralX),        Convert.ToInt32(CentralY), Drone.Width, Drone.Height);    System.Drawing.Imaging.ImageAttributes ColorTransparent =        new System.Drawing.Imaging.ImageAttributes();    ColorTransparent.SetColorKey(Color.Black, Color.Black);    // Adjust landscape    LandscapeX = DroneX - CentralX;    if (LandscapeX <= 0)    {        LandscapeX = 0;        RectDrone.X = Convert.ToInt32(DroneX);    }    if (LandscapeX >= Landscape.Width - pnlView.Width)    {        LandscapeX = Landscape.Width - pnlView.Width;        RectDrone.X = Convert.ToInt32(DroneX - LandscapeX);    }    LandscapeY = DroneY - CentralY;    if (LandscapeY <= 0)    {        LandscapeY = 0;        RectDrone.Y = Convert.ToInt32(DroneY);    }    if (LandscapeY >= Landscape.Height - pnlView.Height)    {        LandscapeY = Landscape.Height - pnlView.Height;        RectDrone.Y = Convert.ToInt32(DroneY - LandscapeY);    }    // Draws landscape    Rectangle RectLandscape = new        Rectangle(Convert.ToInt32(LandscapeX),        Convert.ToInt32(LandscapeY), pnlView.Width,        pnlView.Height);    GraphicsView.DrawImage(Landscape, RectView,        RectLandscape, GraphicsUnit.Pixel);    // Adds pad    Rectangle RectPad = new Rectangle(        Convert.ToInt32(PadX - LandscapeX),        Convert.ToInt32(PadY - LandscapeY), Pad.Width,        Pad.Height);    GraphicsView.DrawImage(Pad, RectPad, 0, 0, Pad.Width,        Pad.Height, GraphicsUnit.Pixel, ColorTransparent);    // Adds drone    GraphicsView.DrawImage(Drone, RectDrone, 0, 0, Drone.Width,        Drone.Height, GraphicsUnit.Pixel, ColorTransparent);    // Adds thrusters if on    if (VThrustOn)    {        Rectangle RectVThrust = new            Rectangle(Convert.ToInt32(RectDrone.X + 0.5 *            RectDrone.Width - 0.5 * VThrust.Width), RectDrone.Y +            RectDrone.Height - VThrust.Height, VThrust.Width,            VThrust.Height);        GraphicsView.DrawImage(VThrust, RectVThrust, 0, 0,            VThrust.Width, VThrust.Height, GraphicsUnit.Pixel,            ColorTransparent);        VThrustOn = false ;    }    if (LThrustOn)    {        Rectangle RectLThrust = new Rectangle(RectDrone.X - 5,            RectDrone.Y + 40, HThrust.Width, HThrust.Height);        GraphicsView.DrawImage(HThrust, RectLThrust, 0, 0,            HThrust.Width, HThrust.Height, GraphicsUnit.Pixel,            ColorTransparent);        LThrustOn = false ;    }    if (RThrustOn)    {        Rectangle RectRThrust = new Rectangle(RectDrone.X +            RectDrone.Width - HThrust.Width + 5,            RectDrone.Y + 40, HThrust.Width, HThrust.Height);        GraphicsView.DrawImage(HThrust, RectRThrust, 0, 0,            HThrust.Width, HThrust.Height, GraphicsUnit.Pixel,            ColorTransparent);        RThrustOn = false ;    }} &#124;

 |
| Step 49 | Save and run the project. Start the game. Click Pause Game . Look at Figure 4.14\. Notice the drone is not placed in the middle of the pnlView . This is because the landscape is in the upper limit ( LandscapeY = 0 ) and the drone is in the left corner. Click Start Again . Let the drone go down and try to do some thrusts. Stop the game again until it is in the middle of the view, as shown in Figure 4.15.Continue until the drone finally landed safely, as shown in Figure 4.16.![](Image00057.jpg)Figure 4.14 The drone is placed in the left corner of the pnlView |
| Step 50 | The auto-pilot option is used so that the computer controls the drone when it descends to surface. With the auto-pilot option, the computer controls horizontal and vertical thrusters to try to make a perfect landing.The following are the rules that are used to automatically enable the vertical thruster (below): 
*   If the Altitude is above 300 meters, then bottom thruster is applied to maintain the DroneYVel under 12 meters per second.
*   If the Altitude is between 10 and 300 meters, then the bottom thruster is applied to maintain DroneYVel below 6 meters per second.
*   If the Altitude is below 10 meters, then the bottom thruster is applied so that the DroneYVel is below 2 + 0.04 * Altitude .

What is being tried is to make sure the drone is not too high, then when it approaches the surface, the bottom thruster is activated so that the drone speed is close to 2 meters per second.![](Image00058.jpg)Figure 4.15 The drone goes down and user applies some thrusts![](Image00059.jpg)Figure 4.16 Drone safely lands on padThe code for auto-pilot is placed in the Tick event of the timDrone control:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667676869707172737475767778798081 &#124; private void timDrone_Tick( object sender, EventArgs e){    time += Convert.ToDouble(timDrone.Interval) / 1000;    lblTime.Text = String.Format( "{0:f1}" , time);    lblTime.Refresh();    DroneX += DroneXVel * Convert.ToDouble(timDrone.Interval)/1000;    DroneY += DroneYVel * Convert.ToDouble(timDrone.Interval) / 1000;    UpdateStatus();    UpdateTrajectory();    UpdateView();    // Checks landing    if (Altitude <= 0)    {        timDrone.Enabled = false ;        btnThrustLeft.Visible = false ;        btnThrustRight.Visible = false ;        btnThrustDown.Visible = false ;        VThrustOn = false ;        LThrustOn = false ;        RThrustOn = false ;        UpdateView();        if (chkAutoPilot.Checked)            lblMessage.Text = "Auto-Pilot " ;        else        {            lblMessage.Text = "You " ;            lblMessage.Visible = true ;        }        // Crash?        if (DroneYVel > VelLandingSafe)        {            SoundCrashLanding.PlaySync();            lblMessage.Text += "Crash!" ;        }        else        {            SoundSafeLanding.PlaySync();            lblMessage.Text += "Land Safely" ;        }        // Makes btnFinish visible        btnStartPause.Visible = false ;        btnExitStop.Visible = false ;        btnFinish.Visible = true ;        return ;    }    // Autopilot or beginner    if (chkAutoPilot.Checked &#124;&#124; levelDifficulty == 2)    {        if (Altitude > 300)        {            if (DroneYVel > 12)                btnThrustDown_Click( null , null );        }        else if (Altitude > 100)        {            if (DroneYVel > 6)                btnThrustDown_Click( null , null );        }        else        {            if (DroneYVel > (2 + 0.04 * Altitude))                btnThrustDown_Click( null , null );        }    }    // Horizontal dragging    if (DroneXVel > 0)        DroneXVel -= Drag;    else if (DroneXVel < 0)        DroneXVel += Drag;    // Gravity    DroneYVel += Gravity * Convert.ToDouble(timDrone.Interval) / 1000;} &#124;

In this new code, when the computer needs to implement a push, it immediately calls the Click event of btnThrustDown . Note that you use this auto-pilot option when the auto-pilot check box is checked and when LevelDifficulty = 2 (the player only needs to control the horizontal thrusters). |
| Step 51 | Save and run the project. Select the Beginner pilot level and check Auto-Pilot option. Click Start Game . The computer will take over the vertical thruster, as shown in Figure 4.17.Run the game again, this time with the Beginner difficulty level and the auto-pilot option unchecked. Make sure the computer provides the vertical thruster needed when you control the horizontal thrusters, as shown in Figure 4.18.![](Image00060.jpg)Figure 4.17 The computer takes over the vertical thruster![](Image00061.jpg)Figure 4.18 Computer provides the vertical thruster needed when user controls the horizontal thrusters |
| Step 52 | You will write the code for the final element of this game, which is horizontal autopilot. Add the following declaration at the form-level: 

&#124; 1 &#124; double Altitude0, Lateral0, Diff; &#124;

The initial altitude and lateral distance are specified in the procedure UpdateTrajectory :

&#124; 12345678910111213141516171920212223242526272829303132333435 &#124; private void UpdateTrajectory(){    double TrajectoryXScale = Convert.ToDouble(        pnlTrajectory.Width) / Landscape.Width;    double TrajectoryYScale = Convert.ToDouble(        pnlTrajectory.Height) / Landscape.Height;    Rectangle RectCircle = new        Rectangle(Convert.ToInt32(TrajectoryXScale *        (DroneX + Drone.Width / 2)) - 3,        Convert.ToInt32(TrajectoryYScale *        (DroneY + Drone.Height)) - 3, 6, 6);    if (time == 0.0)    {        Pen tPen = new Pen(Color.Red, 2);        TrajectoryGraph.Clear(pnlTrajectory.BackColor);        TrajectoryGraph.DrawLine(tPen,            Convert.ToInt32(TrajectoryXScale *            (DroneX + Drone.Width / 2)),            Convert.ToInt32(TrajectoryYScale *            (DroneY+ Drone.Height)),            Convert.ToInt32(TrajectoryXScale *            (PadX + Pad.Width / 2)),            Convert.ToInt32(TrajectoryYScale *            (PadY + Pad.Height / 2)));        Altitude0 = Altitude;        Lateral0 = Lateral;    }    TrajectoryGraph.DrawEllipse(Pens.LightGreen, RectCircle);    pnlTrajectory.Refresh();} &#124;

 |
| Step 53 | The code for horizontal auto-pilots are placed below the vertical auto-pilot code in the Tick event of timDrone control: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666767686970717273747576777879808182838485868788899091 &#124; private void timDrone_Tick( object sender, EventArgs e){    time += Convert.ToDouble(timDrone.Interval) / 1000;    lblTime.Text = String.Format( "{0:f1}" , time);    lblTime.Refresh();    DroneX += DroneXVel * Convert.ToDouble(timDrone.Interval)/1000;    DroneY += DroneYVel * Convert.ToDouble(timDrone.Interval) / 1000;    UpdateStatus();    UpdateTrajectory();    UpdateView();    // Checks landing    if (Altitude <= 0)    {        timDrone.Enabled = false ;        btnThrustLeft.Visible = false ;        btnThrustRight.Visible = false ;        btnThrustDown.Visible = false ;        VThrustOn = false ;        LThrustOn = false ;        RThrustOn = false ;        UpdateView();        if (chkAutoPilot.Checked)            lblMessage.Text = "Auto-Pilot " ;        else        {            lblMessage.Text = "You " ;            lblMessage.Visible = true ;        }        // Crash?        if (DroneYVel > VelLandingSafe)        {            SoundCrashLanding.PlaySync();            lblMessage.Text += "Crash!" ;        }        else        {            SoundSafeLanding.PlaySync();            lblMessage.Text += "Land Safely" ;        }        // Makes btnFinish visible        btnStartPause.Visible = false ;        btnExitStop.Visible = false ;        btnFinish.Visible = true ;        return ;    }    // Autopilot or beginner    if (chkAutoPilot.Checked &#124;&#124; levelDifficulty == 2)    {        if (Altitude > 300)        {            if (DroneYVel > 12)                btnThrustDown_Click( null , null );        }        else if (Altitude > 100)        {            if (DroneYVel > 6)                btnThrustDown_Click( null , null );        }        else        {            if (DroneYVel > (2 + 0.04 * Altitude))                btnThrustDown_Click( null , null );        }    }    // Autopilot - adjust horizontal thrust    if (chkAutoPilot.Checked)    {        Diff = Lateral - Altitude * (Lateral0 / Altitude0);        if (Diff > 2)            btnThrustRight_Click( null , null );        else if (Diff < -2)            btnThrustLeft_Click( null , null );    }    // Horizontal dragging    if (DroneXVel > 0)        DroneXVel -= Drag;    else if (DroneXVel < 0)        DroneXVel += Drag;    // Gravity    DroneYVel += Gravity * Convert.ToDouble(timDrone.Interval) / 1000;} &#124;

 |
| Step 54 | Save and run the project. Select the Senior difficulty level, and check the Auto-Pilot option. Here is the result when the game is run for 9.5 seconds:![](Image00062.jpg)Figure 4.19Here is the result when the game is run for 32 seconds:![](Image00063.jpg)Figure 4.20Here is the result when the game runs for 63.5 seconds, just before landing:![](Image00064.jpg)Figure 4.21Here is the result when the game runs for 91 seconds, after landing safely (no accident):![](Image00065.jpg)Figure 4.22 |
|  |  |

| FormDroneSimulation.cs |
| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197198199200201202203204205206207208209210211212213214215216217218219220221222223224225226227228229230231232234235236237238239240241242243244245246247248249250251252253254255256257258259260261262263264265266267268269270271272273274275276277278279280281282283284285286287288289290291292293294295296297298299300301302303304305306307308309310311312313314315316317318319320321322323324325326327328329330331332333334335336337338339340341342343344345346347348349350351352353354355356357358359360361362363364365366367368369370371372373374375376377378379380381382383384385386387388389390391392393394395396397398399400401402403404405406407408409410411412413414415416417418419420421422423424425426427428429430431432433434435436437438439440441442443444445446447448449450451452453454455456457458459460461462463464465466467468469470471472473474475476477478479480481482483484485486487488489490491492493494495496497498499500501502503504505506507508509510511512513514515516517518519520521522523524525526527528529530531532533534535536537538539540541542543544545546547548549550551552553554555556557558559560561562563564565566567568569570571572573574575576577578579580581582583584585586587588 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;namespace Mendarat_Di_Mars{    public partial class FormDroneSimulation : Form    {        int levelDifficulty = 1;        double Multiplier = 1.0;        double time;        double DroneX, DroneY;        double DroneXVel, DroneYVel;        const double XDelta = 1.2;        const double YDelta = 2.4;        const double Gravity = 9.8 / 6.0;        const double Drag = 0.1;        Image Landscape;        Image Drone;        Image Pad;        Image HThrust;        Image VThrust;        double PadX, PadY;        double Altitude, Lateral;        Random MyRandom = new Random();        const double VelLandingSafe = 3.0;        double RemFuel;        const double MaxFuel = 100;        const double HFuel = 0.5;        const double VFuel = 1.0;        System.Media.SoundPlayer VSoundThrust;        System.Media.SoundPlayer HSoundThrust;        System.Media.SoundPlayer SoundSafeLanding;        System.Media.SoundPlayer SoundCrashLanding;        Graphics TrajectoryGraph;        double LandscapeX, LandscapeY;        double CentralX, CentralY;        Graphics GraphicsView;        bool VThrustOn, LThrustOn, RThrustOn;        double Altitude0, Lateral0, Diff;        public FormDroneSimulation ()        {            InitializeComponent();        }        private void FormDroneSimulation_Load( object sender, EventArgs e)        {            Landscape = Image.FromFile(Application.StartupPath +                "\\landscape.jpg" );            Drone = Image.FromFile(Application.StartupPath + "\\drone.png" );            Pad = Image.FromFile(Application.StartupPath + "\\pad.png" );            HThrust = Image.FromFile(Application.StartupPath + "\\hthrust.png" );            VThrust = Image.FromFile(Application.StartupPath + "\\vthrust.png" );            pnlTrajectory.BackgroundImage = new Bitmap(pnlTrajectory.Width,                pnlTrajectory.Height,                System.Drawing.Imaging.PixelFormat.Format24bppRgb);            TrajectoryGraph = Graphics.FromImage(pnlTrajectory.BackgroundImage);            pnlView.BackgroundImage = new Bitmap(pnlView.Width, pnlView.Height,                System.Drawing.Imaging.PixelFormat.Format24bppRgb);            GraphicsView = Graphics.FromImage(pnlView.BackgroundImage);            VSoundThrust = new System.Media.SoundPlayer(Application.StartupPath                + "\\vthrust.wav" );            HSoundThrust = new System.Media.SoundPlayer(Application.StartupPath                + "\\hthrust.wav" );            SoundSafeLanding = new                System.Media.SoundPlayer(Application.StartupPath +                "\\safe.wav" );            SoundCrashLanding = new                System.Media.SoundPlayer(Application.StartupPath +                "\\crash.wav" );            VSoundThrust.Load();            HSoundThrust.Load();            SoundSafeLanding.Load();            SoundCrashLanding.Load();            CentralX = (pnlView.Width - Drone.Width) / 2;            CentralY = (pnlView.Height - Drone.Height) / 2;        }        private void rdoLevelDifficulty_Click( object sender, EventArgs e)        {            RadioButton ButtonClicked;            ButtonClicked = (RadioButton)sender;            switch (ButtonClicked.Text)            {                case "Beginner" :                    levelDifficulty = 1;                    break ;                case "Trainee" :                    levelDifficulty = 2;                    break ;                case "Junior" :                    levelDifficulty = 3;                    break ;                case "Senior" :                    levelDifficulty = 4;                    break ;                case "Advanced" :                    levelDifficulty = 5;                    break ;            }        }        private void rdoUnitMetric_Click( object sender, EventArgs e)        {            Multiplier = 1.0;        }        private void rdoUnitUS_Click( object sender, EventArgs e)        {            Multiplier = 3.2808;        }        private void timDrone_Tick( object sender, EventArgs e)        {            time += Convert.ToDouble(timDrone.Interval) / 1000;            lblTime.Text = String.Format( "{0:f1}" , time);            lblTime.Refresh();            DroneX += DroneXVel * Convert.ToDouble(timDrone.Interval)/1000;            DroneY += DroneYVel * Convert.ToDouble(timDrone.Interval) / 1000;            UpdateStatus();            UpdateTrajectory();            UpdateView();            // Checks landing            if (Altitude <= 0)            {                timDrone.Enabled = false ;                btnThrustLeft.Visible = false ;                btnThrustRight.Visible = false ;                btnThrustDown.Visible = false ;                VThrustOn = false ;                LThrustOn = false ;                RThrustOn = false ;                UpdateView();                if (chkAutoPilot.Checked)                    lblMessage.Text = "Auto-Pilot " ;                else                {                    lblMessage.Text = "You " ;                    lblMessage.Visible = true ;                }                // Crash?                if (DroneYVel > VelLandingSafe)                {                    lblMessage.Text += "Crash!" ;                    SoundCrashLanding.PlaySync();                }                else                {                    lblMessage.Text += "Land Safely" ;                    SoundSafeLanding.PlaySync();                }                // Makes btnFinish visible                btnStartPause.Visible = false ;                btnExitStop.Visible = false ;                btnFinish.Visible = true ;                return ;            }            // Autopilot or beginner            if (chkAutoPilot.Checked &#124;&#124; levelDifficulty == 2)            {                if (Altitude > 300)                {                    if (DroneYVel > 12)                        btnThrustDown_Click( null , null );                }                else if (Altitude > 100)                {                    if (DroneYVel > 6)                        btnThrustDown_Click( null , null );                }                else                {                    if (DroneYVel > (2 + 0.04 * Altitude))                        btnThrustDown_Click( null , null );                }            }            // Autopilot - adjust horizontal thrust            if (chkAutoPilot.Checked)            {                Diff = Lateral - Altitude * (Lateral0 / Altitude0);                if (Diff > 2)                    btnThrustRight_Click( null , null );                else if (Diff < -2)                    btnThrustLeft_Click( null , null );            }            // Horizontal dragging            if (DroneXVel > 0)                DroneXVel -= Drag;            else if (DroneXVel < 0)                DroneXVel += Drag;            // Graivity            DroneYVel += Gravity * Convert.ToDouble(timDrone.Interval) / 1000;        }        private void btnStartPause_Click( object sender, EventArgs e)        {            if (btnStartPause.Text == "Start Game" )            {                btnStartPause.Text = "Pause Game" ;                btnExitStop.Text = "Stop Game" ;                grpLevel.Visible = false ;                grpUnit.Visible = false ;                grpControl.Visible = true ;                switch (levelDifficulty)                {                    case 1:                        grpControl.Text = "Landing Control-Beginner" ;                        lblFuel.Visible = false ;                        barFuel.Visible = false ;                        btnThrustLeft.Visible = false ;                        btnThrustRight.Visible = false ;                        btnThrustDown.Visible = true ;                        break ;                    case 2:                        grpControl.Text = "Landing Control-Trainee" ;                        lblFuel.Visible = false ;                        barFuel.Visible = false ;                        btnThrustLeft.Visible = true ;                        btnThrustRight.Visible = true ;                        btnThrustDown.Visible = false ;                        break ;                    case 3:                        grpControl.Text = "Landing Control-Junior" ;                        lblFuel.Visible = false ;                        barFuel.Visible = false ;                        btnThrustLeft.Visible = true ;                        btnThrustRight.Visible = true ;                        btnThrustDown.Visible = true ;                        break ;                    case 4:                        grpControl.Text = "Landing Control-Senior" ;                        lblFuel.Visible = true ;                        barFuel.Visible = true ;                        btnThrustLeft.Visible = true ;                        btnThrustRight.Visible = true ;                        btnThrustDown.Visible = true ;                        break ;                    case 5:                        grpControl.Text = "Landing Control-Advanced" ;                        lblFuel.Visible = true ;                        barFuel.Visible = true ;                        btnThrustLeft.Visible = true ;                        btnThrustRight.Visible = true ;                        btnThrustDown.Visible = true ;                        break ;                }                if (chkAutoPilot.Checked)                {                    btnThrustLeft.Visible = false ;                    btnThrustRight.Visible = false ;                    btnThrustDown.Visible = false ;                    lblMessage.Text = "Auto-Pilot On" ;                    lblMessage.Visible = true ;                }                else                {                    lblMessage.Visible = false ;                }                if (rdoUnitMetric.Checked)                {                    lblPosition.Text = "Position (m)" ;                    lblVel.Text = "Vel. (m/sec)" ;                }                else                {                    lblPosition.Text = "Position (feet)" ;                    lblVel.Text = "Vel. (feet/sec)" ;                }                time = 0.0;                lblTime.Text = "0.0" ;                DroneX = (Landscape.Width - Drone.Width) *                    MyRandom.NextDouble();                DroneY = 0;                DroneXVel = 0; DroneYVel = 0;                if (levelDifficulty != 1)                    PadX = (Landscape.Width - Pad.Width) *                        MyRandom.NextDouble();                else                    PadX = (DroneX + Drone.Width / 2) - Pad.Width / 2;                PadY = Landscape.Height - Pad.Height;                RemFuel = MaxFuel;                barFuel.Value = 100;                UpdateStatus();                UpdateTrajectory();                UpdateView();                timDrone.Enabled = true ;            }            else if (btnStartPause.Text == "Pause Game" )            {                btnStartPause.Text = "Start Again" ;                btnExitStop.Enabled = false ;                grpControl.Enabled = false ;                timDrone.Enabled = false ;            }            else            {                btnStartPause.Text = "Pause Game" ;                btnExitStop.Enabled = true ;                grpControl.Enabled = true ;                timDrone.Enabled = true ;            }        }        private void btnExitStop_Click( object sender, EventArgs e)        {            if (btnExitStop.Text == "Stop Game" )            {                btnExitStop.Text = "Exit" ;                btnStartPause.Text = "Start Game" ;                grpLevel.Visible = true ;                grpUnit.Visible = true ;                grpControl.Visible = false ;                timDrone.Enabled = false ;            }            else            {                this .Close();            }        }        private void btnThrustDown_Click( object sender, EventArgs e)        {                       if (RemFuel > 0)            {                VSoundThrust.Play();                VThrustOn = true ;                if (levelDifficulty != 5)                    DroneYVel -= YDelta;                else                    DroneYVel -= 2.0 * YDelta * MyRandom.NextDouble();                if (levelDifficulty > 3)                    RemFuel -= VFuel;            }        }        private void btnThrustLeft_Click( object sender, EventArgs e)        {            if (RemFuel > 0)            {                HSoundThrust.Play();                LThrustOn = true ;                if (levelDifficulty != 5)                    DroneXVel += XDelta;                else                    DroneXVel += 2.0 * XDelta * MyRandom.NextDouble();                if (levelDifficulty > 3)                    RemFuel -= HFuel;            }        }        private void btnThrustRight_Click( object sender, EventArgs e)        {            if (RemFuel > 0)            {                HSoundThrust.Play();                RThrustOn = true ;                if (levelDifficulty != 5)                    DroneXVel -= XDelta;                else                    DroneXVel -= 2.0 * XDelta * MyRandom.NextDouble();                if (levelDifficulty > 3)                    RemFuel -= HFuel;            }        }        private void UpdateStatus()        {            Altitude = (Landscape.Height - Pad.Height / 2) –                (DroneY + Drone.Height);            Lateral = (DroneX + Drone.Width / 2) - (PadX + Pad.Width / 2);            if (Altitude > 0)                lblVPosition.Text = String.Format( "{0:f0}" ,                    Altitude * Multiplier);            else                lblVPosition.Text = "0" ;            if (Math.Abs(Lateral) < 1)                lblHPosition.Text = "Above" ;            else                lblHPosition.Text = String.Format( "{0:f0}" ,                    Lateral * Multiplier);            lblVVel.Text = String.Format( "{0:f1}" , -DroneYVel * Multiplier);            lblHVel.Text = String.Format( "{0:f1}" , DroneXVel * Multiplier);            lblVVel.Refresh();            lblHVel.Refresh();            lblVPosition.Refresh();            lblHPosition.Refresh();            lblDrone.Left = Convert.ToInt32((DroneX + Drone.Width / 2) *                pnlGuide.Width / Landscape.Width - lblDrone.Width / 2);            lblPad.Left = Convert.ToInt32((PadX + Pad.Width / 2) *                pnlGuide.Width / Landscape.Width - lblPad.Width / 2);            if (RemFuel > 0)                barFuel.Value = Convert.ToInt32(100 * RemFuel/MaxFuel);            else                barFuel.Value = 0;            if (barFuel.Value <= 10)                Console.Beep();        }        private void btnFinish_Click( object sender, EventArgs e)        {            btnFinish.Visible = false ;            btnStartPause.Visible = true ;            btnExitStop.Visible = true ;            btnExitStop.PerformClick();        }        private void UpdateTrajectory()        {            double TrajectoryXScale = Convert.ToDouble(pnlTrajectory.Width) /                Landscape.Width;            double TrajectoryYScale = Convert.ToDouble(pnlTrajectory.Height) /                Landscape.Height;            Rectangle RectCircle =                new Rectangle(Convert.ToInt32(TrajectoryXScale *                (DroneX + Drone.Width / 2)) - 3,                Convert.ToInt32(TrajectoryYScale * (DroneY + Drone.Height)) - 3,                6, 6);            if (time == 0.0)            {                Pen tPen = new Pen(Color.Red, 2);                TrajectoryGraph.Clear(pnlTrajectory.BackColor);                TrajectoryGraph.DrawLine(tPen,                    Convert.ToInt32( TrajectoryXScale * (DroneX + Drone.Width / 2)),                    Convert.ToInt32(TrajectoryYScale * (DroneY+ Drone.Height)),                    Convert.ToInt32(TrajectoryXScale * (PadX + Pad.Width / 2)),                    Convert. ToInt32(TrajectoryYScale * (PadY + Pad.Height / 2)));                Altitude0 = Altitude;                Lateral0 = Lateral;            }            TrajectoryGraph.DrawEllipse(Pens.LightGreen, RectCircle);            pnlTrajectory.Refresh();        }        private void UpdateView()        {            Rectangle RectView =                new Rectangle(0, 0, pnlView.Width, pnlView.Height);            Rectangle RectDrone =                new Rectangle(Convert.ToInt32(CentralX),                Convert.ToInt32(CentralY), Drone.Width, Drone.Height);            System.Drawing.Imaging.ImageAttributes ColorTransparent =                new System.Drawing.Imaging.ImageAttributes();            ColorTransparent.SetColorKey(Color.Black, Color.Black);            // Adjust landscape            LandscapeX = DroneX - CentralX;            if (LandscapeX <= 0)            {                LandscapeX = 0;                RectDrone.X = Convert.ToInt32(DroneX);            }            if (LandscapeX >= Landscape.Width - pnlView.Width)            {                LandscapeX = Landscape.Width - pnlView.Width;                RectDrone.X = Convert.ToInt32(DroneX - LandscapeX);            }            LandscapeY = DroneY - CentralY;            if (LandscapeY <= 0)            {                LandscapeY = 0;                RectDrone.Y = Convert.ToInt32(DroneY);            }            if (LandscapeY >= Landscape.Height - pnlView.Height)            {                LandscapeY = Landscape.Height - pnlView.Height;                RectDrone.Y = Convert.ToInt32(DroneY - LandscapeY);            }            // Draws landscape            Rectangle RectLandscape =                new Rectangle(Convert.ToInt32(LandscapeX),                Convert.ToInt32(LandscapeY), pnlView.Width, pnlView.Height);            GraphicsView.DrawImage(Landscape, RectView, RectLandscape,                GraphicsUnit.Pixel);            // Adds pad            Rectangle RectPad =                new Rectangle(Convert.ToInt32(PadX - LandscapeX),                Convert.ToInt32(PadY - LandscapeY), Pad.Width, Pad.Height);            GraphicsView.DrawImage(Pad, RectPad, 0, 0, Pad.Width,                Pad.Height, GraphicsUnit.Pixel, ColorTransparent);            // Adds drone            GraphicsView.DrawImage(Drone, RectDrone, 0, 0, Drone.Width,                Drone.Height, GraphicsUnit.Pixel, ColorTransparent);            // Adds thrusters if on            if (VThrustOn)            {                Rectangle RectVThrust =                    new Rectangle(Convert.ToInt32(RectDrone.X + 0.5 *                    RectDrone.Width - 0.5 * VThrust.Width), RectDrone.Y +                    RectDrone.Height - VThrust.Height, VThrust.Width,                    VThrust.Height);                GraphicsView.DrawImage(VThrust, RectVThrust, 0, 0,                    VThrust.Width, VThrust.Height, GraphicsUnit.Pixel,                    ColorTransparent);                VThrustOn = false ;            }            if (LThrustOn)            {                Rectangle RectLThrust = new Rectangle(RectDrone.X - 5,                    RectDrone.Y + 40, HThrust.Width, HThrust.Height);                GraphicsView.DrawImage(HThrust, RectLThrust, 0, 0,                    HThrust.Width, HThrust.Height, GraphicsUnit.Pixel,                    ColorTransparent);                LThrustOn = false ;            }            if (RThrustOn)            {                Rectangle RectRThrust = new                    Rectangle(RectDrone.X + RectDrone.Width - HThrust.Width + 5,                    RectDrone.Y + 40, HThrust.Width, HThrust.Height);                GraphicsView.DrawImage(HThrust, RectRThrust, 0, 0,                    HThrust.Width, HThrust.Height, GraphicsUnit.Pixel,                    ColorTransparent);                RThrustOn = false ;            }            pnlView.Refresh();        }    }} |
|  |  |

TUTORIAL 4

GAME: JUMPER

In this chapter, you will build Jumper game. In this game, you will move the jumper across the busy road, avoid the tiger, and cross the river with the changing current to get to house safely.

| Description |
| Open the project in Visual C# and you will see:![](Image00066.jpg)Figure 5.1 All controls used in Jumper game projectThe layout of the form is quite simple. There are label controls at the top of the form to track game scores. Then, several panels are used to load the graphics used. The jumper will move to the top of the screen. The bottom panel (purple) is where the jumper first is located. The next panel (pink) has moving traffic. Then, a panel (dodger blue) is a tiger trajectory, a panel (green) is a stream, and another panel (orange) is home to jumper. Two button controls are used to control the game. This game uses four timer controls to draw graphics and monitor game.Run the project (press <F5>). The game will appear as ‘stop’ state:![](Image00067.jpg)Figure 5.2 The game is on ‘stop’ stateYou can then click Start Game button to start the game:![](Image00068.jpg)Figure 5.3 The game is on ‘play’ state |
| Tutorial Steps |
| Step 1 | You will start building Jumper game project. Start a new project in Visual C #. Once created, it is recommended that you immediately save it with a name that you choose yourself. This will create the folders and file structure that your project needs.Place four label controls on the top part of the form (set the AutoSize property to False so that it can be resized and the BorderStyle property temporarily becomes FixedSingle so you can see the edges). Then, place five panel controls below the labels. These panels will be a place for image graphics. Each panel has a width of 16 jumpers or 640 pixels, because one jumper will be given a width of 40 pixels. The first panel will be the jumper house, which will be given a height of 80 pixels. The next panel will become a river, with a height of 120 pixels. The next panel will be a place for tiger, 40 pixels high.![](Image00069.jpg)Figure 5.4 All controls used in this project and their positionsUnder the snake panel, there is a road panel. This panel will contain three boat lanes. Each boat has a height of 40 pixels, but you will give it a height of 140 pixels (not 120 pixels) to make room for lane markers. The fifth panel is the place where the jumper will begin its journey or leap. This panel will be given a height of 40 pixels. Add the last control panel below the form with three button controls. Then, finally, add four timer controls. Adjust the size of the form so that the panel controls can occupy according to the width of the form.After completion, the form will look as shown in Figure 5.4.Labels display score information. The panels will contain graphic elements. Button controls are used to start/pause/ stop the game and display high scores. Timer controls are used to update game graphics and monitor game status. |
| Step 2 | Set the properties of each control using the Properties window: 

&#124; A number of properties of the Form1 object &#124;
&#124; Name &#124; FormJumper &#124;
&#124; BackColor &#124; Orange &#124;
&#124; Text &#124; Jumper – Level 1 &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label1 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font &#124; Comic Sans, 14 &#124;
&#124; ForeColor &#124; White &#124;
&#124; Text &#124; Score: &#124;
&#124; TextAlign &#124; MiddleLeft &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label2 object &#124;
&#124; Name &#124; lblScore &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Font Size &#124; 14 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlignt &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label3 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font &#124; Comic Sans, 14 &#124;
&#124; ForeColor &#124; White &#124;
&#124; Text &#124; Highest Score: &#124;
&#124; TextAlign &#124; MiddleLeft &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label4 object &#124;
&#124; Name &#124; lblHighestScore &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Font Size &#124; 14 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlignt &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel1 object &#124;
&#124; Name &#124; pnlHouse &#124;
&#124; BackColor &#124; Orange &#124;
&#124; Height &#124; 80 &#124;
&#124; Width &#124; 640 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel2 object &#124;
&#124; Name &#124; pnlRiver &#124;
&#124; BackColor &#124; Green &#124;
&#124; Height &#124; 80 &#124;
&#124; Width &#124; 640 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel3 object &#124;
&#124; Name &#124; pnlTiger &#124;
&#124; BackColor &#124; DodgerBlue &#124;
&#124; Height &#124; 40 &#124;
&#124; Width &#124; 640 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel4 object &#124;
&#124; Name &#124; pnlRoad &#124;
&#124; BackColor &#124; DeepPink &#124;
&#124; Height &#124; 140 &#124;
&#124; Width &#124; 640 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel5 object &#124;
&#124; Name &#124; pnlStart &#124;
&#124; BackColor &#124; MediumPurple &#124;
&#124; Height &#124; 40 &#124;
&#124; Width &#124; 640 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel6 object &#124;
&#124; Name &#124; pnlButton &#124;
&#124; BackColor &#124; Crimson &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button1 object &#124;
&#124; Name &#124; btnStartPause &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Start Game &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button2 object &#124;
&#124; Name &#124; btnExitStop &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Exit &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button3 object &#124;
&#124; Name &#124; btnHighestScore &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Highest Score &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Timer1 object &#124;
&#124; Name &#124; timRoad &#124;
&#124; Interval &#124; 80 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Timer2 object &#124;
&#124; Name &#124; timRiver &#124;
&#124; Interval &#124; 80 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Timer3 object &#124;
&#124; Name &#124; timTiger &#124;
&#124; Interval &#124; 100 &#124;
&#124;  &#124;  &#124;

&#124; Sejumlah Properti dari objek Timer4 &#124;
&#124; Name &#124; timStatus &#124;
&#124; Interval &#124; 20 &#124;
&#124;  &#124;  &#124;

After completion, the form will look as shown in Figure 5.1.You will now start writing code for the game. You will write it in several stages, starting with graphic elements. You have a number of moving objects in this game. First, you will write the code to move the the cars. Then, you add other elements to the game, one by one. During the code development process, you will make modifications to a number of methods before reaching a satisfying endpoint. |
| Step 3 | You can now use the DrawImage method, the Brush object, and the FillRectangle method to add methods to the MovingObj class. You need three methods for this class. One method to draw on graphical objects, one method to move it to a new location, and another method to remove it. These methods are added to the class definition like general methods added to the form code file. To add a method to the class definition, you need to choose the name and type of information that the method will produce (if any). You also need to determine the arguments needed by the method.Add MoveObj class to the project in Solution Explorer : 

&#124; 123456789101112131415161718 &#124; using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;using System.Data;namespace Jumper{    class MovingObj    {        public Image Picture;        public Rectangle Rectangular;        public int Speed;        public bool IsVisible = false ;    }} &#124;

 |
| Step 4 | Add the Draw method to the class to position a MovingObj object to a graphical object named g (passed as argument): 

&#124; 12345 &#124; public void Draw(Graphics g){    g.DrawImage( this .Picture, this .Rectangular);    this .IsVisible = true ;} &#124;

Note the use this keyword to refer to the calling object. After the object is placed on g , you set IsVisible of the object to true . |
| Step 5 | The Move method moves a MovingObj object to a new location (using Speed ​​property). The arguments needed are g ( Graphics object) and bc ( Brush object needed to remove it from the previous location): 

&#124; 123456 &#124; public void Move(Graphics g, Brush bc){    g.FillRectangle(bc, this .Rectangular);    this .Rectangular.X += this .Speed;    g.DrawImage( this .Picture, this .Rectangular);} &#124;

MovingObj object is first removed. The horizontal location is then updated and the object is redrawn. |
| Step 6 | The Remove Method removes a MovingObj object from a graphical object g (using a bc brush): 

&#124; 12345 &#124; public void Remove(Graphics g, Brush bc){    g.FillRectangle(bc, this .Rectangular);    this .IsVisible = false ;} &#124;

 |
| Step 7 | Add these three methods ( Draw , Move , Remove ) to MoveObj class file to create the final version of this class: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637 &#124; using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;using System.Data;namespace Jumper{    class MovingObj    {        public Image Picture;        public Rectangle Rectangular;        public int Speed;        public bool IsVisible = false ;        public void Draw(Graphics g)        {            g.DrawImage( this .Picture, this .Rectangular);            this .IsVisible = true ;        }        public void Move(Graphics g, Brush bc)        {            g.FillRectangle(bc, this .Rectangular);            this .Rectangular.X += this .Speed;            g.DrawImage( this .Picture, this .Rectangular);        }        public void Remove(Graphics g, Brush bc)        {            g.FillRectangle(bc, this .Rectangular);            this .IsVisible = false ;        }    }} &#124;

 |
| Step 8 | In this project, cars will be moving on the road panel ( pnlRoad ) and the movement will be controlled by timRoad . There are three different type of vehicles (car, truck, and trailer), with each moving from left or right.Car graphics measuring 40 x 40 pixels, truck graphics measuring 80 x 40 pixels, and trailer graphics measuring 120 x 40 pixels. These images will be used to form MovingObj objects.The road panel will have three lanes (each with a height of 40 pixels). In the upper lane, vehicles will move from left to right. In the two lanes below, each vehicle will go from right to left. Remember that the road panel has a height of 140 pixels, of which 120 pixels for three lanes and 20 pixels are allocated for lane markers.The boundary area of ​​each row is given a height of 5 pixels. You can ensure that the total height is 140 pixels. You will use 12 vehicles, four for each lane. Vehicles will be represented by an array which contains MovingObj objects.Vehicles in the upper lane are given a speed of +3 (moving to the right), vehicles in the middle lane are given a speed of -3 (moving to the left), and vehicles in the lower lane are given a speed of -2 (moving to the left).You will start writing the code. Place the following three lines of code in the form-level declaration: 

&#124; 123 &#124; const int numberOfVehicles = 12;MovingObj[] vehicleArr = new MovingObj[numberOfVehicles];Graphics roadGraphics; &#124;

The above declaration defines 12 MovingObj objects loaded in the vehicleArr array and declares a graphical object ( roadGraphics ) for the road panel. |
| Step 9 | Add this code to the Load event method of the form. This code creates graphical objects, an array of vehicles containing MovingObj objects, and images for these objects. This method also invokes another method, LocateVehicle , which assigns a starting position for each vehicle: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738 &#124; private void FormJumper_Load( object sender, EventArgs e){    // Creates road and vehicles    pnlRoad.BackgroundImage = new Bitmap(pnlRoad.Width,               pnlRoad.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    roadGraphics = Graphics.FromImage(pnlRoad.BackgroundImage);    for ( int i = 0; i < numberOfVehicles; i++)        vehicleArr[i] = new MovingObj();   vehicleArr[0].Picture = Image.FromFile(Application.StartupPath +        "\\trailer_right.png" );    vehicleArr[1].Picture = Image.FromFile(Application.StartupPath +        "\\truck_right.png" );    vehicleArr[2].Picture = Image.FromFile(Application.StartupPath +        "\\car_right.png" );    vehicleArr[3].Picture = Image.FromFile(Application.StartupPath +        "\\car_right.png" );    vehicleArr[4].Picture = Image.FromFile(Application.StartupPath +        "\\truck_right.png" );    vehicleArr[5].Picture = Image.FromFile(Application.StartupPath +        "\\car_left.png" );    vehicleArr[6].Picture = Image.FromFile(Application.StartupPath +        "\\truck_left.png" );    vehicleArr[7].Picture = Image.FromFile(Application.StartupPath +        "\\truck_left.png" );    vehicleArr[8].Picture = Image.FromFile(Application.StartupPath +        "\\car_left.png" );    vehicleArr[9].Picture = Image.FromFile(Application.StartupPath +        "\\trailer_left.png" );    vehicleArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    LocateVehicle();} &#124;

Note that the graphic files must already be in the bin\Debug folder. |
| Step 10 | The code for positioning of vehicles in LocateVehicle method is given as follows: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445 &#124; private void LocateVehicle(){    roadGraphics.Clear(pnlRoad.BackColor);    // Draws lanes    roadGraphics.DrawLine(Pens.White, 0, 2, pnlRoad.Width, 2);    roadGraphics.DrawLine(Pens.White, 0, pnlRoad.Height - 2,        pnlRoad.Width, pnlRoad.Height - 2);    roadGraphics.DrawLine(Pens.White, 0, 92, pnlRoad.Width, 92);    roadGraphics.DrawLine(Pens.Yellow, 0, 47, pnlRoad.Width, 47);    roadGraphics.DrawLine(Pens.Yellow, 0, 49, pnlRoad.Width, 49);    // Upper lane    vehicleArr[0].Rectangular = new Rectangle(20, 5, 120, 40);    vehicleArr[0].Speed = 3;    vehicleArr[1].Rectangular = new Rectangle(200, 5, 80, 40);    vehicleArr[1].Speed = 3;    vehicleArr[2].Rectangular = new Rectangle(380, 5, 40, 40);    vehicleArr[2].Speed = 3;    vehicleArr[3].Rectangular = new Rectangle(540, 5, 40, 40);    vehicleArr[3].Speed = 3;    // Middle lane    vehicleArr[4].Rectangular = new Rectangle(40, 50, 80, 40);    vehicleArr[4].Speed = -3;    vehicleArr[5].Rectangular = new Rectangle(220, 50, 40, 40);    vehicleArr[5].Speed = -3;    vehicleArr[6].Rectangular = new Rectangle(360, 50, 80, 40);    vehicleArr[6].Speed = -3;    vehicleArr[7].Rectangular = new Rectangle(520, 50, 80, 40);    vehicleArr[7].Speed = -3;    // Lower lane    vehicleArr[8].Rectangular = new Rectangle(60, 95, 40, 40);    vehicleArr[8].Speed = -2;    vehicleArr[9].Rectangular = new Rectangle(180, 95, 120, 40);    vehicleArr[9].Speed = -2;    vehicleArr[10].Rectangular = new Rectangle(380, 95, 40, 40);    vehicleArr[10].Speed = -2;    vehicleArr[11].Rectangular = new Rectangle(520, 95, 80, 40);    vehicleArr[11].Speed = -2;    for ( int i = 0; i < 12; i++)        vehicleArr[i].Draw(roadGraphics);} &#124;

Note that each vehicle is placed in a lane (using a Rectangle structure) to provide uniform spacing. This code also draws road lines. White lines are used to define the sides of the road and to separate the two lower lanes. Two yellow lines separate the movement of traffic in the opposite direction. |
| Step 11 | Save and run the project. The vehicles will be displayed on the form, as shown in Figure 5.5.![](Image00070.jpg)Figure 5.5 Position of each vehicle on the form |
| Step 12 | Remove the following code from LocateVehicle method: 

&#124; 12 &#124; for ( int i = 0; i < 12; i++)    vehicleArr[i].Draw(roadGraphics); &#124;

The road timer control ( timRoad ) defines the movement of each vehicle. You need to enable/disable this timer at certain times. Two buttons control the game, btnStartPause and btnExitStop . You will add a code for the Click event of these two buttons to move the vehicle. |
| Step 13 | Two control buttons have certain interactions. The btnStartPause control can have three possible values ​​from the Text property. If the Text property has “ Start Game ” value when clicked, the game will be initialized and put into play mode using: 
*   Change the Text property of btnStartPause to Pause Game .
*   Change the Text property of btnExitStop to Stop Game .
*   Draw vehicles.
*   Enable timRoad timer.

If the Text property of btnStartPause is Pause Game and the button is clicked, the game enters pause mode:

*   Change the Text property to Start Again .
*   Disable btnExitStop .
*   Disable timRoad timer.

If the Text property is Start Again and the button is clicked, the game enters play mode again:

*   Change the Text property to Pause Game .
*   Enable timRoad timer.

The code that implements the steps above is placed in the Click event method of btnStartPause :

&#124; 123456789101112131415161718192021222324252627 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        pnlRoad.Refresh();        timRoad.Enabled = true ;   }   else if (btnStartPause.Text == "Pause Game" )   {       btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )   {        btnStartPause.Text = "Pause Game" ;         btnExitStop.Enabled = true ;         timRoad.Enabled = true ;     }} &#124;

![](Image00071.jpg)Figure 5.6 Two control buttons have some interactions |
| Step 14 | When user clicks Stop Game ( btnExitStop ), the following steps are performed: 
*   Change the Text property to Exit .
*   Change the Text property of btnStartPause to Start Game .
*   Disable timRoad control.

If btnExitStop is clicked when it says Exit , the program will stop. The code that implements the above steps is placed in the Click event method of btnExitStop :

&#124; 1234567891011121314 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        timRoad.Enabled = false ;    }   else   {        this .Close();    }} &#124;

 |
| Step 15 | Save and run the project. When you click Start Game , the vehicles will appear. Notice how the buttons change the state when you start, refresh, and stop the game, as shown in Figure 5.6.You can also stop the program. Make sure everything is working as it should. Now, you can write down the code that makes each vehicle move. |
| Step 16 | After timRoad is enabled, with each Tick event, each vehicle is repositioned using the Move method of the MoveObj object (and Speed ​​property). At the end, the vehicle will leave the road panel. What do you do when the vehicle leaves the road panel? One possible approach is to immediately restart the vehicle on the opposite end of the panel. The problem with this approach is that if a large vehicle leaves the panel followed immediately by a smaller vehicle, the two vehicles will overlap when redrawn on opposite ends of the panel. To avoid this overlap, you are using a delay in redrawing the car by 80 pixels and a delay in redrawing the truck by 40 pixels. In this way, each vehicle will have its own buffer of 120 pixels, so there is no overlap.Add this code to the Tick method of timRoad timer. This code drives each vehicle (if IsVisible property is true ). If the vehicle leaves the right side of the form, it will be repositioned on the left side of the form (X = -120 pixels, to maintain a buffer zone of 120 pixels). If the vehicle leaves the left side of the form, it will be repositioned to the right side of the form (X depends on the width of the vehicle, to maintain a 120 pixel buffer): 

&#124; 12345678910111213141516171819202122 &#124; private void timRoad_Tick( object sender, EventArgs e){   for ( int i = 0; i < numberOfVehicles; i++)    {        if (vehicleArr[i].IsVisible)        {            vehicleArr[i].Move(roadGraphics, new                SolidBrush(pnlRoad.BackColor));            if ((vehicleArr[i].Rectangular.X > pnlRoad.Width &&                    vehicleArr[i].Speed > 0))                vehicleArr[i].Rectangular.X = -120;            if ((vehicleArr[i].Rectangular.X <                   -vehicleArr[i].Picture.Width &&                          vehicleArr[i].Speed < 0))                vehicleArr[i].Rectangular.X = pnlRoad.Width +                (120 - vehicleArr[i].Picture.Width);        }    }    pnlRoad.Refresh();} &#124;

Learn this code to make sure everything is working properly. Save and run the project. Click on Start Game and you will see each vehicle now moving. Note why there is no overlap between vehicles. Make sure you can make pause game and restart it. |
| Step 17 | Before continuing, there is another problem that needs to be addressed. This game will have a number of game levels, starting with the easy level (Level 1) and will get more difficult the longer the user plays. You will learn the levels of the game in more detail later. In the first level, if all 12 vehicles were used, it would make it very difficult for the jumper to jump across the road. You will start the game with only 7 vehicles, and remove vehicles 1, 4, 5, 7, and 11\. Vehicle removal is carried out at the Click event on btnStartPause : 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        // Removes cars for Level 1        vehicleArr[0].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[3].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[4].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[6].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[10].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();        timRoad.Enabled = true ;   }   else if (btnStartPause.Text == "Pause Game" )   {       btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )   {        btnStartPause.Text = "Pause Game" ;         btnExitStop.Enabled = true ;         timRoad.Enabled = true ;     }} &#124;

 |
| Step 18 | Save and run the project again, making sure only 7 vehicles are now in the form. There are 2 vehicles in the upper lane, 2 in the middle lane, and 3 vehicles in the lower lane, as shown in Figure 5.7.![](Image00072.jpg)Figure 5.7 There are only 2 vehicles in the upper lane, 2 in the middle lane, and 3 vehicles in the lower lane |
| Step 19 | Next, you will implement the next graphic element, the moving tree boats in the river panel. You will see a coding process that is almost identical to that for vehicles.The boats move in the river panel ( pnlRiver ) and the movement is controlled by the river timer ( timRiver ). There are three sizes of boats used.Small boat is 40 x 40 pixels, medium boat is 80 x 40 pixels, and long boat is 120 x 40 pixels. These images are used to create MovingObj objects. The program assumes that you have placed these image files in bin\Debug folder.The river panel will have three lines (40 pixels high each). In the top row and bottom row, each boat will flow from left to right. In the middle row, each boat will flow from right to left. The river is 120 pixels high. There are no boundaries between lines as in the road panel.You use 12 boats (the higher the game level, the fewer boats). There are five boats in the top row, four boats in the middle row, and three boats in the bottom row. These boats will be represented by an array of branches containing the MovingObj objects. Like a vehicle, every object requires an image, rectangular structure, and speed.The boats in the top row are given a speed of +5 (move to the right), in the middle row a speed of -3 (move to the left), and in the bottom row a speed of 2 (move to the right). Each boat is initially placed with uniform spacing.Place the following three lines in the form-level declaration: 

&#124; 123 &#124; const int numberOfBoats = 12;MovingObj[] boatArr = new MovingObj[numberOfBoats];Graphics riverGraphics; &#124;

This defines 12 MoveObj objects (inside boatArr ), which will be used as the boats in the river panel. |
| Step 20 | Add modified code of the Load method on the form. This code creates graphic objects, MoveObj objects in boatArr array, and images used for these objects. This method also calls LocateBoat method (which will be defined later) which assigns a starting position to each boat: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273747576 &#124; private void FormJumper_Load( object sender, EventArgs e){    // Creates road and vehicles    pnlRoad.BackgroundImage = new Bitmap(pnlRoad.Width,               pnlRoad.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    roadGraphics = Graphics.FromImage(pnlRoad.BackgroundImage);    for ( int i = 0; i < numberOfVehicles; i++)        vehicleArr[i] = new MovingObj();   vehicleArr[0].Picture = Image.FromFile(Application.StartupPath +        "\\trailer_right.png" );    vehicleArr[1].Picture = Image.FromFile(Application.StartupPath +        "\\truck_right.png" );    vehicleArr[2].Picture = Image.FromFile(Application.StartupPath +        "\\car_right.png" );    vehicleArr[3].Picture = Image.FromFile(Application.StartupPath +        "\\car_right.png" );    vehicleArr[4].Picture = Image.FromFile(Application.StartupPath +        "\\truck_right.png" );    vehicleArr[5].Picture = Image.FromFile(Application.StartupPath +        "\\car_left.png" );    vehicleArr[6].Picture = Image.FromFile(Application.StartupPath +        "\\truck_left.png" );    vehicleArr[7].Picture = Image.FromFile(Application.StartupPath +        "\\truck_left.png" );    vehicleArr[8].Picture = Image.FromFile(Application.StartupPath +        "\\car_left.png" );    vehicleArr[9].Picture = Image.FromFile(Application.StartupPath +        "\\trailer_left.png" );    vehicleArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    LocateVehicle();    // Creates river and boats    pnlRiver.BackgroundImage = new Bitmap(pnlRiver.Width,        pnlRiver.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    riverGraphics = Graphics.FromImage(pnlRiver.BackgroundImage);    for ( int i = 0; i < numberOfBoats; i++)        boatArr[i] = new MovingObj();    // Creates images    boatArr[0].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[1].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[2].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[3].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[4].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[5].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[6].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[7].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[8].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[9].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    LocateBoat();} &#124;

 |
| Step 21 | Note that graphic files must already exist in the bin\Debug folder in your project. The code for positioning the boats is placed in LocateBoat method: 

&#124; 12345678910111213141516171819202122232425262728293031323334 &#124; private void LocateBoat(){    riverGraphics.Clear(pnlRiver.BackColor);    // Upper row    boatArr[0].Rectangular = new Rectangle(20, 0, 80, 40);    boatArr[0].Speed = 5;    boatArr[1].Rectangular = new Rectangle(140, 0, 120, 40);    boatArr[1].Speed = 5;    boatArr[2].Rectangular = new Rectangle(300, 0, 40, 40);    boatArr[2].Speed = 5;    boatArr[3].Rectangular = new Rectangle(400, 0, 80, 40);    boatArr[3].Speed = 5;    boatArr[4].Rectangular = new Rectangle(540, 0, 80, 40);    boatArr[4].Speed = 5;    // Middle row    boatArr[5].Rectangular = new Rectangle(60, 40, 40, 40);    boatArr[5].Speed = -3;    boatArr[6].Rectangular = new Rectangle(180, 40, 120, 40);    boatArr[6].Speed = -3;    boatArr[7].Rectangular = new Rectangle(360, 40, 80, 40);    boatArr[7].Speed = -3;    boatArr[8].Rectangular = new Rectangle(500, 40, 120, 40);    boatArr[8].Speed = -3;    // Lower row    boatArr[9].Rectangular = new Rectangle(40, 80, 120, 40);    boatArr[9].Speed = 2;    boatArr[10].Rectangular = new Rectangle(280, 80, 80, 40);    boatArr[10].Speed = 2;    boatArr[11].Rectangular = new Rectangle(480, 80, 120, 40);    boatArr[11].Speed = 2;} &#124;

 |
| Step 22 | The river timer control ( timRiver ) defines the movement of the boats. Modify the Click event method of btnStartPause to draw boats and enable/disable them at the right time: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        // Removes cars for Level 1        vehicleArr[0].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[3].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[4].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[6].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[10].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();        LocateBoat();        for ( int i = 0; i < numberOfBoats; i++)            boatArr[i].Draw(riverGraphics);        pnlRiver.Refresh();        timRoad.Enabled = true ;        timRiver.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;        timRiver.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timRoad.Enabled = true ;        timRiver.Enabled = true ;     }} &#124;

 |
| Step 23 | Modify the Click event method of btnExitStop to stop the river timer when the game is stopped: 

&#124; 123456789101112131415 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        timRoad.Enabled = false ;        timRiver.Enabled = false ;    }   else   {        this .Close();    }} &#124;

 |
| Step 24 | Save and run the project. You will see the boats are now displayed on the river panel, when you click the Start Game button. The result is shown in Figure 5.8.![](Image00073.jpg)Figure 5.8 The boats are now displayed on the river panel |
| Step 25 | The code for moving the boats in the Tick event of the timRiver is identical to the one used to move the vehicles. With each Tick event, each boat is repositioned using the Move method of the MoveObj object (and Speed ​​property). When the boat leaves the panel, it will return from the opposite side (use the same 120 pixel buffer zone to avoid overlapping). Add this code to your project:![](Image00074.jpg)Figure 5.9 The vehicles and the boats are now moving 

&#124; 123456789101112131415161718192021 &#124; private void timRiver_Tick( object sender, EventArgs e){    for ( int i = 0; i < numberOfBoats; i++)    {        if (boatArr[i].IsVisible)        {            boatArr[i].Move(riverGraphics,                new SolidBrush(pnlRiver.BackColor));            if ((boatArr[i].Rectangular.X > pnlRiver.Width &&                   boatArr[i].Speed > 0))                boatArr[i].Rectangular.X = -120;            if ((boatArr[i].Rectangular.X <                -boatArr[i].Picture.Width && boatArr[i].Speed < 0))                boatArr[i].Rectangular.X = pnlRiver.Width +                    (120 - boatArr[i].Picture.Width);        }    }    pnlRiver.Refresh();} &#124;

 |
| Step 26 | Save and run the project. Click on Start Game and both the vehicles and the boats are now moving, as shown in Figure 5.9. |
| Step 27 | To make it harder for the jumper to complete their journey, the game will have a tiger randomly placed between the river and the road. The tiger will always move from left to right. The tiger moves on the tiger panel ( pnlTiger ) and the movement is regulated by the tiger timer ( timTiger ).The tiger measures 111 x 24 pixels. Both of these images will be used to define MovingObj objects. The program assumes that the two tiger files have been placed in the bin\Debug folder.The tiger panel is 40 pixels high. You will vertically make a tiger graphic in the middle of the panel. The tiger will have a speed of 5 and randomly appear on the left side of the panel.Place these four lines of code in the form-level declaration: 

&#124; 12345 &#124; Random myRand = new Random();MovingObj tiger;Image tiger1, tiger2;int tigerImage;Graphics tigerGraphics; &#124;

The lines of code above define a random number object ( myRand ) to place the tiger randomly, the MoveObj object ( tiger ) will be used for the tiger, two images ( tiger1 and tiger2 ) to display the tiger, the current image is being displayed ( tigerImage ) and a graphical object ( tigerGraphics ) for the tiger panel. |
| Step 28 | Add the modified code of the Load event method to the following form: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768697071727374757677787980818283848586878889 &#124; private void FormJumper_Load( object sender, EventArgs e){    // Creates road and vehicles    pnlRoad.BackgroundImage = new Bitmap(pnlRoad.Width,               pnlRoad.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    roadGraphics = Graphics.FromImage(pnlRoad.BackgroundImage);    for ( int i = 0; i < numberOfVehicles; i++)        vehicleArr[i] = new MovingObj();    vehicleArr[0].Picture = Image.FromFile(Application.StartupPath +        "\\trailer_right.png" );    vehicleArr[1].Picture = Image.FromFile(Application.StartupPath +        "\\truck_right.png" );    vehicleArr[2].Picture = Image.FromFile(Application.StartupPath +        "\\car_right.png" );    vehicleArr[3].Picture = Image.FromFile(Application.StartupPath +        "\\car_right.png" );    vehicleArr[4].Picture = Image.FromFile(Application.StartupPath +        "\\truck_right.png" );    vehicleArr[5].Picture = Image.FromFile(Application.StartupPath +        "\\car_left.png" );    vehicleArr[6].Picture = Image.FromFile(Application.StartupPath +        "\\truck_left.png" );    vehicleArr[7].Picture = Image.FromFile(Application.StartupPath +        "\\truck_left.png" );    vehicleArr[8].Picture = Image.FromFile(Application.StartupPath +        "\\car_left.png" );    vehicleArr[9].Picture = Image.FromFile(Application.StartupPath +        "\\trailer_left.png" );    vehicleArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    LocateVehicle();    // Creates river and boats    pnlRiver.BackgroundImage = new Bitmap(pnlRiver.Width,        pnlRiver.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    riverGraphics = Graphics.FromImage(pnlRiver.BackgroundImage);    for ( int i = 0; i < numberOfBoats; i++)        boatArr[i] = new MovingObj();    // Creates images    boatArr[0].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[1].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[2].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[3].Picture = Image.FromFile(Application.StartupPath         + "\\boat_medium.png" );    boatArr[4].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[5].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[6].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[7].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[8].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[9].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    LocateBoat();    // Creates tiger    pnlTiger.BackgroundImage = new Bitmap(pnlTiger.Width,        pnlTiger.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    tigerGraphics = Graphics. FromImage(pnlTiger.BackgroundImage);    tigerGraphics.Clear(pnlTiger.BackColor);    tiger1 = Image.FromFile(Application.StartupPath +        "\\tiger1.png" );    tiger2 = Image.FromFile(Application.StartupPath +        "\\tiger2.png" );    tiger = new MovingObj();    tiger.Rectangular = new Rectangle(0, 7,        tiger1.Width, tiger1.Height);} &#124;

 |
| Step 29 | The tiger timer control ( timTiger ) defines the movement of the tiger. Modify the Click event method of btnStartPause to enable/disable this timer at the correct times: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        // Removes cars for Level 1        vehicleArr[0].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[3].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[4].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[6].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[10].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();        LocateBoat();        for ( int i = 0; i < numberOfBoats; i++)            boatArr[i].Draw(riverGraphics);        pnlRiver.Refresh();        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;     }} &#124;

 |
| Step 30 | Modify the Click event method of btnExitStop to stop the tiger timer and remove the tiger (if any) when the game is stopped: 

&#124; 1234567891011121314151617181920212223 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        if (tiger.IsVisible)        {            tiger.Remove(tigerGraphics, new                SolidBrush(pnlTiger.BackColor));            pnlTiger.Refresh();        }        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;    }    else    {        this .Close();    }} &#124;

 |
| Step 31 | The code for moving the tiger is placed on the Tick event of timTiger timer: 

&#124; 12345678910111213141516171819202122232425262728293031323334 &#124; private void timTiger_Tick( object sender, EventArgs e){    if (!tiger.IsVisible)    {        if (myRand.Next(49) == 0)        {            tiger.Rectangular.X = -tiger1.Width;            tiger.Speed = 5;            tiger.Picture = tiger1;            tigerImage = 1;            tiger.Draw(tigerGraphics);        }    }    else    {        tiger.Move(tigerGraphics,            new SolidBrush(pnlTiger.BackColor));        if (tigerImage == 1)        {            tigerImage = 2;            tiger.Picture = tiger2;        }        else        {            tigerImage = 1;            tiger.Picture = tiger1;        }        if (tiger.Rectangular.X > pnlTiger.Width)            tiger.Remove(tigerGraphics,                new SolidBrush(pnlTiger.BackColor));            pnlTiger.Refresh();    }} &#124;

Tiger will be displayed randomly. To decide which tiger image to display, a random number from 0 to 49 is used. When the value is zero, the tiger will move. This means a snake will appear (on average) for every 50 Tick events. When it appears, the tiger is positioned to the left of the form. After the tiger has moved ( IsVisible is true ), any call to the Tick event from the timTiger timer will update its position using the Move method of the MoveObj object, which alternates between the two tiger images to give the moving effect. After the tiger leaves the right side of the form, it is removed from the screen. At this point, the program will wait for another tiger to appear. |
| Step 32 | Save and run the project. Click on Start Game . The vehicles and boats will move and finally a tiger will ove from the left side of the form, as shown in Figure 5.10.![](Image00075.jpg)Figure 5.10 The vehicles and boats will move and finally a tiger will ove from the left side of the formMake sure you can pause the game and restart the movement. Now that you understand how to move vehicles, branches, and tiger, it's time to write down the code so the jumper can jump. |
| Step 33 | The jumper will be created so that he can jump from panel to panel and move horizontally across the panels. You will use a MovingObj object to represent jumper. Four graphics will be used to represent jumper.Each jumper is 40 x 40 pixels in size. The program assumes that these files have been placed in the bin\Debug folder in your project.The jumper will begin his journey in the start panel ( pnlStart ) at the bottom of the form and end the journey (if successful) in the home panel ( pnlHouse ) at the top of the form. On its way, the jumper will cross the three lines of the road panel ( pnlRoad ), the tiger panel ( pnlTiger ), and the three rows of boats in the river panel ( pnlRiver ). You define a variable ( jumperLocation ) to track what panel (and where in the panel in the case of road and river) the jumper are currently in. The values ​​for this variable and its associated locations are given as follows: 

&#124; jumperLocation &#124; Location &#124;
&#124; 8 &#124; House panel &#124;
&#124; 7 &#124; River panel (upper row) &#124;
&#124; 6 &#124; River panel (middle row) &#124;
&#124; 5 &#124; River panel (lower row) &#124;
&#124; 4 &#124; Tiger panel &#124;
&#124; 3 &#124; Road panel (upper lane) &#124;
&#124; 2 &#124; Road panel (middle lane) &#124;
&#124; 1 &#124; Road panel (lower lane) &#124;
&#124; 0 &#124; Start panel &#124;

For horizontal movement within a panel, the jumper will jump in units of 40 pixels. So when the game starts, you will place the jumper around the center in the start panel at an even multiple of 40 pixels. You will select the starting location at 320 pixels.Now, you are going to write the code for the jumper graphics and create graphical objects for the start panel and the house panel. Add these declarations at the form-level:

&#124; 12345 &#124; MovingObj jumper;Image jumperUp, jumperLeft, jumperDown, jumperRight;int jumperLocation;Graphics startGraphics;Graphics houseGraphics; &#124;

This declares a moving object ( jumper ) to be used for the jumper, four images ( jumperUp , jumperLeft , jumperDown , jumperRight ) to display the jumper, location variable ( jumperLocation ) and graphical objects (startGraphics and houseGraphics ) for the start panel and house panel. |
| Step 34 | Add the modified code to the Load method of the form: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113 &#124; private void FormJumper_Load( object sender, EventArgs e){    // Creates road and vehicles    pnlRoad.BackgroundImage = new Bitmap(pnlRoad.Width,               pnlRoad.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    roadGraphics = Graphics.FromImage(pnlRoad.BackgroundImage);    for ( int i = 0; i < numberOfVehicles; i++)        vehicleArr[i] = new MovingObj();    vehicleArr[0].Picture = Image.FromFile(Application.StartupPath        + "\\trailer_right.png" );    vehicleArr[1].Picture = Image.FromFile(Application.StartupPath        + "\\truck_right.png" );    vehicleArr[2].Picture = Image.FromFile(Application.StartupPath        + "\\car_right.png" );    vehicleArr[3].Picture = Image.FromFile(Application.StartupPath        + "\\car_right.png" );    vehicleArr[4].Picture = Image.FromFile(Application.StartupPath        + "\\truck_right.png" );    vehicleArr[5].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[6].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    vehicleArr[7].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    vehicleArr[8].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[9].Picture = Image.FromFile(Application.StartupPath        + "\\trailer_left.png" );    vehicleArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    LocateVehicle();    // Creates river and boats    pnlRiver.BackgroundImage = new Bitmap(pnlRiver.Width,        pnlRiver.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    riverGraphics = Graphics.FromImage(pnlRiver.BackgroundImage);    for ( int i = 0; i < numberOfBoats; i++)        boatArr[i] = new MovingObj();    // Creates images    boatArr[0].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[1].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[2].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[3].Picture = Image.FromFile(Application.StartupPath         + "\\boat_medium.png" );    boatArr[4].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[5].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[6].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[7].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[8].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[9].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    LocateBoat();    // Creates tiger    pnlTiger.BackgroundImage = new Bitmap(pnlTiger.Width,        pnlTiger.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    tigerGraphics = Graphics. FromImage(pnlTiger.BackgroundImage);    tigerGraphics.Clear(pnlTiger.BackColor);    tiger1 = Image.FromFile(Application.StartupPath +        "\\tiger1.png" );    tiger2 = Image.FromFile(Application.StartupPath +        "\\tiger2.png" );    tiger = new MovingObj();    tiger.Rectangular = new Rectangle(0, 7,        tiger1.Width, tiger1.Height);    // Creates pnlStart    pnlStart.BackgroundImage = new Bitmap(pnlStart.Width,        pnlStart.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    startGraphics = Graphics.FromImage(pnlStart.BackgroundImage);    startGraphics.Clear(pnlStart.BackColor);    // Creates jumper house    pnlHouse.BackgroundImage = new Bitmap(pnlHouse.Width,        pnlHouse.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    houseGraphics = Graphics.FromImage(pnlHouse.BackgroundImage);    houseGraphics.Clear(pnlHouse.BackColor);    // Reads jumper graphics file    jumperUp = Image.FromFile(Application.StartupPath +        "\\jumper_up.png" );    jumperLeft = Image.FromFile(Application.StartupPath +        "\\jumper_left.png" );    jumperDown = Image.FromFile(Application.StartupPath +        "\\jumper_down.png" );    jumperRight = Image.FromFile(Application.StartupPath +        "\\jumper_right.png" );} &#124;

In the meantime, you treat the house panel as empty rectangular area. You will build up the area of ​the house after learning jumper’s movements and collision detection (to see if the jumper can get to the house). |
| Step 35 | Add a method to your project ( getNewJumper ) to initialize the jumper in the start panel jumperLocation = 0 ): 

&#124; 123456789 &#124; private void getNewJumper(){    jumperLocation = 0;    jumper.Rectangular = new Rectangle(320, 0,        jumperUp.Width, jumperUp.Height);    jumper.Picture = jumperUp;    jumper.Draw(startGraphics);    pnlStart.Refresh();} &#124;

 |
| Step 36 | Modify the Click event method of btnStartPause to initialize the jumper in the start panel: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        // Removes cars for Level 1        vehicleArr[0].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[3].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[4].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[6].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[10].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();        LocateBoat();        for ( int i = 0; i < numberOfBoats; i++)            boatArr[i].Draw(riverGraphics);        pnlRiver.Refresh();        getNewJumper();        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;     }} &#124;

 |
| Step 37 | Save and run the project. Click on Start Game . The jumper will be displayed and ready to start his journey, as shown in the Figure 5.11. |
| Step 38 | You will write the code to move the jumper. For now, you'll be moving the jumper around without worrying about crashing a vehicle or falling into a river. Later, you will write the code for this collision logic. To control the movement of the jumper, you will use the arrow cursor controls on the keyboard. You will learn how to detect keystrokes using the KeyDown method.![](Image00076.jpg)Figure 5.11 The jumper is displayed and ready to start his journeyYou need the capability to move jumper up and down from one panel to another and moving left and up across panels. You use the keyboard to control it, using the KeyDown event. This event can be used to detect keystrokes, along with Alt, Ctrl, Shift, cursor control, and other control keys. The form of the KeyDown event method for a form is given as follows: 

&#124; 1234 &#124; private void Form_KeyDown( object sender, KeyEventArgs e){} &#124;

There is a problem with cursor keys. In the container control (form, group box, panel) that contains other controls, cursor keys (arrows) are used to tab from one control to another. When such container control has focus, or is active, the KeyDown event is not triggered by the cursor key. So, to move the jumper using the cursor keys, you need to make sure the focus remains on the control panel. In this program, you will ensure that the focus remains on the start panel. To do so, add this line of code at the end of the Click event of btnStartPause :

&#124; 1 &#124; pnlStart.Focus(); &#124;

Using this line of code, after clicking any key, the focus will be placed back on the pnlStart , so that the cursor keys (arrows) can be detected by the KeyDown event. Now, you will write the code to move the jumper.You will add a jumping sound each time the jumper moves. The jump.wav sound file is provided in the bin\Debug folder of your project. Add this declaration at the form-level:

&#124; 1 &#124; System.Media.SoundPlayer soundJump; &#124;

Place these two lines of code at the end of the form's Load method to load this sound:

&#124; 123 &#124; soundJump = new System.Media.SoundPlayer(Application.StartupPath +    "\\jump.wav" );soundJump.Load(); &#124;

The code for moving the jumper is placed in the form's KeyDown event method:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546 &#124; private void FormJumper_KeyDown( object sender, KeyEventArgs e){    if (!timRiver.Enabled)        return ;    // Removed from current location    RemoveJumper();    if (e.KeyCode == Keys.Up)    {        soundJump.Play();        jumper.Picture = jumperUp;        jumperLocation++;        if (jumperLocation > 8)            jumperLocation = 8;    }    else if (e.KeyCode == Keys.Left)    {        soundJump.Play();        jumper.Picture = jumperLeft;        if (jumper.Rectangular.X > 0)            jumper.Rectangular.X -= 40;    }    else if (e.KeyCode == Keys.Down)    {        soundJump.Play();        jumper.Picture = jumperDown;        jumperLocation--;       if (jumperLocation < 0)            jumperLocation = 0;    }    else if (e.KeyCode == Keys.Right)    {        soundJump.Play();        jumper.Picture = jumperRight;        if (jumper.Rectangular.X < 600)            jumper.Rectangular.X += 40;    }    // Draws in new location    DrawJumper();} &#124;

 |
| Step 39 | This code uses two methods ( RemoveJumper and DrawJumper ) to perform movements. Add these methods: 

&#124; 1234567891011121314151617181920212223242526272829 &#124; public void RemoveJumper(){    if (jumperLocation == 0)    {        jumper.Remove(startGraphics,            new SolidBrush(pnlStart.BackColor));        pnlStart.Refresh();    }    else if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        jumper.Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();    }    else if (jumperLocation == 4)    {        jumper.Remove(tigerGraphics,            new SolidBrush(pnlTiger.BackColor));        pnlTiger.Refresh();    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6        &#124;&#124; jumperLocation == 7)    {        jumper.Remove(riverGraphics,            new SolidBrush(pnlRiver.BackColor));        pnlRiver.Refresh();    }} &#124;

&#124; 123456789101112131415161718192021222324252627282930313233343536373839 &#124; public void DrawJumper(){    if (jumperLocation == 0)    {        jumper.Rectangular.Y = 0;        jumper.Draw(startGraphics);        pnlStart.Refresh();    }    else if (jumperLocation == 1 &#124;&#124; jumperLocation == 2 &#124;&#124;        jumperLocation == 3)    {        jumper.Rectangular.Y = 140 - 45 * jumperLocation;        jumper.Draw(roadGraphics);        pnlRoad.Refresh();    }    else if (jumperLocation == 4)    {        jumper.Rectangular.Y = 0;        jumper.Draw(tigerGraphics);        pnlTiger.Refresh();    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;        jumperLocation == 7)    {        jumper.Rectangular.Y = 120 - 40 * (jumperLocation - 4);        jumper.Draw(riverGraphics);        pnlRiver.Refresh();    }    else if (jumperLocation == 8)    {        jumper.Rectangular.Y = 40;        jumper.Draw(houseGraphics);        pnlHouse.Refresh();    }} &#124;

Now you learn what happened here. First, note that no KeyDown event is triggered unless the timer is enabled. Then, in RemoveJumper , by using an if statement, you clean the jumper based on the current location (removing it from the corresponding graphical region). Then you find which arrow key is pressed. Sound of jumper jumps is played and corresponding jumper graphics is assigned.For vertical movement, the jumper location is adjusted (keeping it between 0 and 8). For horizontal movement, the X property of the Rectangular property of jumper object is adjusted (+40 pixels or -40 pixels), which ensures the object stays within the boundaries of the screen. Then, in DrawJumper , the jumper is drawn at its new location. In particular, pay attention to the block where the location of the jumper is used to determine certain lanes on the road panel and certain rows on the river panel. |
| Step 40 | One more thing that needs to be changed. You need to make sure the jumper is removed from the screen when the game is stopped. Make changes to the Click event method of btnExitStop : 

&#124; 1234567891011121314151617181920212223242526 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        if (tiger.IsVisible)        {            tiger.Remove(tigerGraphics, new                SolidBrush(pnlTiger.BackColor));            pnlTiger.Refresh();        }        if (jumper.IsVisible)            RemoveJumper();        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;    }    else    {        this .Close();    }} &#124;

 |
| Step 41 | Save and run the project. Click on Start Game . Try pressing the cursor control keys (arrows). Move the jumper up and down the screen. Make sure that the jumper cannot get past the house panel or under the start panel. Try moving left and right. Make sure the jumper doesn't leave the screen. Listen for a jumping sound, as shown in Figure 5.12.It is very easy for the jumper to get to house panel because there is no danger from vehicles or tiger and it can cross the river to any location on house panel. You need logic to see if the jumper has collided with a vehicle or a tiger, jumped on a boat running down the river and got home safely. Each of these steps involves a collision detection concept.![](Image00077.jpg)Figure 5.11 In the meantime, it is very easy for the jumper to get to house panel because there is no danger from vehicles or tiger and it can cross the river to any location on house panel |
| Step 42 | If the jumper collides with a vehicle while crossing the road, the journey will end (the jumper will be removed and the new jumper will be placed on the house panel). You would assume a collision when 10 percent of the jumper crossed the vehicle.Collision on this project will be monitored by a status timer ( timStatus ). You will also use this timer to update the score and other game information. Modify the Click event method of btnStartPause to enable/disable it at appropriate times: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        // Removes cars for Level 1        vehicleArr[0].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[3].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[4].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[6].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[10].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();        LocateBoat();        for ( int i = 0; i < numberOfBoats; i++)            boatArr[i].Draw(riverGraphics);        pnlRiver.Refresh();        getNewJumper();        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;        timStatus.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    pnlStart.Focus();} &#124;

 |
| Step 43 | Modify the Click event method of btnExitPause to disable the status timer when the game is stopped: 

&#124; 123456789101112131415161718192021222324252627 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        if (tiger.IsVisible)        {            tiger.Remove(tigerGraphics, new                SolidBrush(pnlTiger.BackColor));            pnlTiger.Refresh();        }        if (jumper.IsVisible)            RemoveJumper();        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;        timStatus.Enabled = false ;    }    else    {        this .Close();    }} &#124;

 |
| Step 44 | You will make a certain sound if the jumper collides with a vehicle. The sound file of hitrak.wav is placed in the bin\Debug folder of the project. Add this declaration to the form-level declaration: 

&#124; 1 &#124; System.Media.SoundPlayer soundCollide; &#124;

Place these two lines of code at the end of the form's Load method to load this sound:

&#124; 123 &#124; soundCollide = new System.Media.SoundPlayer(Application.StartupPath    + "\\tabrak.wav" );soundCollide.Load(); &#124;

 |
| Step 45 | Place this code on the Tick event method of the timStatus : 

&#124; 12345678910111213141516171819202122232425262728293031323334 &#124; private bool DoesCollide(Rectangle rect1, Rectangle rect2, double percentage){    Rectangle collision;   collision = Rectangle.Intersect(rect1, rect2);    if (collision.Width * collision.Height >= percentage *        rect2.Width * rect2.Height / 100)        return ( true );    else       return ( false );}private void timStatus_Tick( object sender, EventArgs e){    // Check collision    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        // Vehicles       for ( int i = 0; i < numberOfVehicles; i++)        {            if (vehicleArr[i].IsVisible)           {                if (DoesCollide(vehicleArr[i].Rectangular,                    jumper.Rectangular, 10))                {                    JumperNoMore();                    return ;                }            }        }    }} &#124;

In this code, on the road panel ( locationJumper = 1, 2, 3), you check whether the jumper has collided with the vehicle (10 percent of the jumper crossed the vehicle). If it is, JumperNoMore method is called to remove the jumper. If there's no collision, nothing happens. |
| Step 46 | JumperNoMore method plays s sound, removes the jumper from its current location and creates a new jumper: 

&#124; 1234567891011 &#124; private void JumperNoMore(){    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)   {        soundCollide.Play();    }    RemoveJumper();    getNewJumper();} &#124;

 |
| Step 47 | Save and run the project. Start the game. Try to cross the street. If jumper hits a vehicle, you will hear a certain sound and a new jumper will be displayed. |
| Step 48 | If the jumper manages to cross three lanes of the vehicle, it must pass the tiger (if it has one). If the jumper collides with the tiger, its journey will be over. You are assuming a collision when the jumper touches the tiger.You will play a sound sound when the jumper collides with the tiger. The tiger.wav sound file has been placed in the bin\Debug folder of your project. Add this declaration at the form-level: 

&#124; 1 &#124; System.Media.SoundPlayer soundTiger; &#124;

Add these two lines of code at the end of the form's Load method to load this sound:

&#124; 123 &#124; soundTiger = new System.Media.SoundPlayer(Application.StartupPath +    "\\tiger.wav" );soundTiger.Load(); &#124;

 |
| Step 49 | Place the modified code on the Tick event method of the timStatus : 

&#124; 12345678910111213141516171819202122232425262728293031323334 &#124; private void timStatus_Tick( object sender, EventArgs e){    // Check collision    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        // Vehicles       for ( int i = 0; i < numberOfVehicles; i++)        {            if (vehicleArr[i].IsVisible)           {                if (DoesCollide(vehicleArr[i].Rectangular,                    jumper.Rectangular, 10))                {                    JumperNoMore();                    return ;                }            }        }    }    else if (jumperLocation == 4)    {        // tiger        if (tiger.IsVisible)        {            if (DoesCollide( tiger. Rectangular , jumper.Rectangular , 1))            {                JumperNoMore();                return ;            }        }    }} &#124;

In this new code, if any part of the jumper (greater than 1 percent) collides with the snake, it will be removed.![](Image00078.jpg)Figure 5.12 If jumper hits a tiger, you will hear a certain sound and a new jumper will be displayed |
| Step 50 | Modify JumperNoMore as follows: 

&#124; 12345678910111213141516 &#124; private void JumperNoMore(){    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)   {        soundCollide.Play();    }    else if (jumperLocation == 4)    {        soundTiger.Play();    }    RemoveJumper();    getNewJumper();} &#124;

 |
| Step 51 | Save and run the project. Start the game. Try to cross the river. If your jumper hits a tiger, you will hear a certain sound and a new jumper will be displayed, as seen in Figure 5.12. |
| Step 52 | After the jumper has crossed the road and avoided the tiger, it's time for him to cross the river. To do this, the jumper must jump onto one of the boats that is floating in the river. Collision logic is different here. In the case of vehicles and tiger, in the event of a collision, the jumper's journey will end. Here, if there is a collision, you want the jumper to float on a boat. If there is no collision, the jumper’s journey will be over.Before learning the logic of floating on a boat, add a certain sound, when the jumper fails to jump on the boat. The file to use is drowned.wav , which is provided in the bin\Debug folder of your project. Add a declaration for this sound at the form-level: 

&#124; 1 &#124; System.Media.SoundPlayer soundDrowned; &#124;

Add these two lines of code at the end of the form's Load method to load this sound:

&#124; 123 &#124; soundDrowned = new System.Media.SoundPlayer(Application.StartupPath    + "\\drowned.wav" );soundDrowned.Load(); &#124;

 |
| Step 53 | Once the jumper has entered the river, you will need to check whether it is on the boat. If so, with the updated river timer, the jumper’s position will be same with the position of the boat. To see if jumper is on a boat, you use DoesCollide function. If 80 percent of the jumper are intersecting with a boat, it is said that the jumper is on the boat. You will be using a variable ( onBoat ) to identify which boat the jumper is on. Add the following declaration at the form-level: 

&#124; 1 &#124; int onBoat; &#124;

With each new jumper, onBoat is initialized to -1\. Add the modified code to the getNewJumper function to initialize the following:

&#124; 12345678910 &#124; private void getNewJumper(){    onBoat = -1;    jumperLocation = 0;    jumper.Rectangular = new Rectangle(320, 0, jumperUp.Width,        jumperUp.Height);    jumper.Picture = jumperUp;   jumper.Draw(startGraphics);    pnlStart.Refresh();} &#124;

 |
| Step 54 | Every time the jumper moves, you need to reset the boat to zero to see if it is on the boat. This is done in the modified code of the form's KeyDown event method: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950 &#124; private void FormJumper_KeyDown( object sender, KeyEventArgs e){    if (!timRiver.Enabled)        return ;    // // Removed from current location    RemoveJumper();    if (e.KeyCode == Keys.Up)    {        onBoat = -1;        soundJump.Play();        jumper.Picture = jumperUp;        jumperLocation++;        if (jumperLocation > 8)            jumperLocation = 8;    }    else if (e.KeyCode == Keys.Left)    {        onBoat = -1;        soundJump.Play();        jumper.Picture = jumperLeft;        if (jumper.Rectangular.X > 0)            jumper.Rectangular.X -= 40;    }    else if (e.KeyCode == Keys.Down)    {        onBoat = -1;        soundJump.Play();        jumper.Picture = jumperDown;        jumperLocation--;        if (jumperLocation < 0)            jumperLocation = 0;    }    else if (e.KeyCode == Keys.Right)    {        onBoat = -1;        soundJump.Play();        jumper.Picture = jumperRight;        if (jumper.Rectangular.X < 600)            jumper.Rectangular.X += 40;    }    // Draws in new location    DrawJumper();} &#124;

 |
| Step 55 | If the boat are 0 to 11, you will need to update the jumper’s horizontal position as the boat moves. This is done on the Tick event method of the timRiver control: 

&#124; 1234567891011121314151617181920212223242526272829303132333435 &#124; private void timRiver_Tick( object sender, EventArgs e){    for ( int i = 0; i < numberOfBoats; i++)    {        if (boatArr[i].IsVisible)        {            boatArr[i].Move(riverGraphics,                new SolidBrush(pnlRiver.BackColor));            if (onBoat == i)            {                jumper.Rectangular.X += boatArr[i].Speed;                if (jumper. Rectangular.X < 0 &#124;&#124; jumper.Rectangular.X                    > 640 - jumper.Rectangular.Width)                {                    JumperNoMore();                    return ;                }                jumper.Draw(riverGraphics);            }            if ((boatArr[i].Rectangular.X > pnlRiver.Width &&                   boatArr[i].Speed > 0))                boatArr[i].Rectangular.X = -120;            if ((boatArr[i].Rectangular.X <                -boatArr[i].Picture.Width && boatArr[i].Speed < 0))                boatArr[i].Rectangular.X = pnlRiver.Width +                    (120 - boatArr[i].Picture.Width);        }    }    pnlRiver.Refresh();} &#124;

In this code, the jumper moves in the same direction and the delta of movement is the same as the boat (the index of the boatArr is onBoat ). If the jumper falls into the river, his journey will end. Now, you will see how to assign a value to onBoat . |
| Step 56 | You check for boat collision in the Tick event method of timStatus . The necessary change is to set a value for onBoat : 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061 &#124; private void timStatus_Tick( object sender, EventArgs e){    // Check collision    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        // Vehicles        for ( int i = 0; i < numberOfVehicles; i++)        {            if (vehicleArr[i].IsVisible)            {                if (DoesCollide(vehicleArr[i].Rectangular,                    jumper.Rectangular, 10))                {                    JumperNoMore();                    return ;                }            }        }    }    else if (jumperLocation == 4)    {        // tiger        if (tiger.IsVisible)        {            if (DoesCollide( tiger. Rectangular , jumper.Rectangular , 1))            {                JumperNoMore();                return ;            }        }    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;        jumperLocation == 7)    {       // Checks whether jumper is on the boat       if (onBoat == -1)        {            for ( int i = 0; i < numberOfBoats; i++)            {                if (boatArr[i].IsVisible)                {                    if (DoesCollide(boatArr[i].Rectangular,                        jumper.Rectangular, 80))                    {                        onBoat = i;                        return ;                    }                }            }            if (onBoat == -1)            {                JumperNoMore();                return ;            }        }    }} &#124;

The steps in the code above are quite simple. If the jumper is not on the boat, the code above checks for 80 percent collision with the boat. If such a collision occurs, onBoat is given a value. If the collision didn't occur, the jumper would fall into the river and disappear. Note if there is a jumper on the boat ( onBoat ! = -1 ), no collision check is done. |
| Step 57 | Modify JumperNoMore method as follows: 

&#124; 12345678910111213141516171819202122 &#124; private void JumperNoMore(){    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        soundCollide.Play();    }    else if (jumperLocation == 4)    {        soundTiger.Play();    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6       &#124;&#124; jumperLocation == 7)    {        soundDrowned.Play();    }    RemoveJumper();    getNewJumper();} &#124;

When the jumper do not jump onto the boat (no collision occurs) on the river panel, a drowning sound will be played, the jumper will be removed, and new jumper are created in the start panel. |
| Step 58 | Save and run the project. Start the game. Do this so that the jumper can successfully cross the river, then avoid tiger. Try to get the jumper to jump into one of the boat running down the river as shown in Figure 5.13.![](Image00079.jpg)Figure 5.13 Jumper successfully cross the river, avoid tiger, and jump into one of the boatNotice how the jumper moves up the boat. Check the logic that stops the jumper from moving if it hovers on a boat but flows until it hits the form boundaries. Make sure you listen to the sound of drowning. Try to get the jumper to make it to the house panel. Now, you can do this so that the jumper can jump anywhere on the house panel. Next, you will create a house panel where only five specific places can be entered by jumper. |
| Step 59 | At this point, the jumper can jump to any location on the house panel. You will make it a little more difficult by specifying five rectangular regions on the house panel. If the jumper jumps on a boat and enters one of these regions (there is a complete collision), the jumper will be safe. Otherwise, the sound of drowning will be played and the jumper’s journey will be over.The house panel is 640 pixels wide (same as other panels) and 80 pixels high. You will define each house as a blue rectangular, 60 pixels wide and 60 pixels high. By making the house 60 pixels wide, you're giving the jumper (40 pixels wide) some slack when it jumps off the boat. These houses will be uniformly spread out on the house panel:Each house is 60 pixels wide and separated by 50 pixels apart. The left and right edges are 70 pixels wide. You make the edges wider to make it easier for the jumper to reach its home.Declare this variable at form-level: 

&#124; 1 &#124; Rectangle[] rectHouse = new Rectangle[5]; &#124;

In DrawHouse function, each rectangular is defined and drawn as a filled area:

&#124; 1234567891011121314 &#124; private void DrawHouse(){    rectHouse[0] = new Rectangle(70, 20, 60, 60);    rectHouse[1] = new Rectangle(180, 20, 60, 60);    rectHouse[2] = new Rectangle(290, 20, 60, 60);    rectHouse[3] = new Rectangle(400, 20, 60, 60);    rectHouse[4] = new Rectangle(510, 20, 60, 60);    for ( int i = 0; i < 5; i++)    {        houseGraphics.FillRectangle(Brushes.Blue, rectHouse[i]);    }    pnlHouse.Refresh();} &#124;

You will create the house when the game first starts, so add this line of code to the Load method of the form, which is placed after the house graphic region is created:

&#124; 1 &#124; DrawHouse() &#124;

The house area also needs to be removed when a new game starts. Add this modified code to the Click event method of btnStartPause :

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        // Removes cars for Level 1        vehicleArr[0].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[3].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[4].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[6].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[10].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();        LocateBoat();        for ( int i = 0; i < numberOfBoats; i++)            boatArr[i].Draw(riverGraphics);        pnlRiver.Refresh();        DrawHouse()        getNewJumper();        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;        timStatus.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    pnlStart.Focus();} &#124;

 |
| Step 60 | Save and run the project. The area of ​​the house will be displayed as shown in Figure 5.14.![](Image00080.jpg)Figure 5.14 The area of ​​the house is displayed |
| Step 61 | The background of the panel house is quite boring. You will fix it. Visual C # can be used to fill graphic object with a background using what is called a texture brush. You will use the brush to make jumper house surrounded by leaves. Declare a brushHouse (a TextureBrush object) at the form-level: 

&#124; 1 &#124; TextureBrush brushHouse; &#124;

Add this line of code to the form's Load event method before calling DrawHouse method:

&#124; 12 &#124; brushHouse = new TextureBrush( new Bitmap(Application.StartupPath +    "\\bush.png" )); &#124;

The brush is created using a graphic file named bush.png , which has been placed in the bin\Debug folder in your project.![](Image00067.jpg)Figure 5.15 Jumper house surrounded by leavesNow, add a modified code to DrawHouse function to fill the panel with the leaves graphic ( brushHouse ):

&#124; 12345678910111213141516 &#124; private void DrawHouse(){    houseGraphics.FillRectangle(brushHouse, 0, 0, pnlHouse.Width,        pnlHouse.Height);    rectHouse[0] = new Rectangle(70, 20, 60, 60);    rectHouse[1] = new Rectangle(180, 20, 60, 60);    rectHouse[2] = new Rectangle(290, 20, 60, 60);    rectHouse[3] = new Rectangle(400, 20, 60, 60);    rectHouse[4] = new Rectangle(510, 20, 60, 60);    for ( int i = 0; i < 5; i++)    {        houseGraphics.FillRectangle(Brushes.Blue, rectHouse[i]);    }    pnlHouse.Refresh();} &#124;

 |
| Step 62 | Save and run the project again. You will see a jumper house surrounded by leaves as shown in Figure 5.15. |
| Step 63 | Next, you will add logic to check if the jumper make it home safely. When the jumper jumps on the house panel, it is said to be safe if there is not yet one jumper on the house and if it collides perfectly with the rectangular structure of the house. In that case, you will play a sound indicating that he arrives. The jumper in house is represented by the graphic file katakrumah.png, which has been provided in the bin \ debug folder in your project.The sound that indicates the jumper’s safe arrival at home is represented by the file house.wav, which has also been provided in the bin\Debug folder in your project.Add these new declarations at the form-level: 

&#124; 123 &#124; Image jumperInHouse;System.Media.SoundPlayer soundHouse;bool [] jumperInHouseArr = new bool [5]; &#124;

jumperInHouse is the image of a jumper that has arrived at the house, soundHouse is a sound that indicates the jumper has survived to the house and jumperInHouseArr is an array of bool that will be used to find out the location of the house where the jumper is in. |
| Step 64 | Add the modified code to the Load method of the form to specify jumperInHouse and soundHouse as follows: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141 &#124; private void FormJumper_Load( object sender, EventArgs e){    // Creates road and vehicles    pnlRoad.BackgroundImage = new Bitmap(pnlRoad.Width,               pnlRoad.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    roadGraphics = Graphics.FromImage(pnlRoad.BackgroundImage);    for ( int i = 0; i < numberOfVehicles; i++)        vehicleArr[i] = new MovingObj();    vehicleArr[0].Picture = Image.FromFile(Application.StartupPath        + "\\trailer_right.png" );    vehicleArr[1].Picture = Image.FromFile(Application.StartupPath        + "\\truck_right.png" );    vehicleArr[2].Picture = Image.FromFile(Application.StartupPath        + "\\car_right.png" );    vehicleArr[3].Picture = Image.FromFile(Application.StartupPath        + "\\car_right.png" );    vehicleArr[4].Picture = Image.FromFile(Application.StartupPath        + "\\truck_right.png" );    vehicleArr[5].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[6].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    vehicleArr[7].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    vehicleArr[8].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[9].Picture = Image.FromFile(Application.StartupPath        + "\\trailer_left.png" );    vehicleArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    LocateVehicle();    // Creates river and boats    pnlRiver.BackgroundImage = new Bitmap(pnlRiver.Width,        pnlRiver.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    riverGraphics = Graphics.FromImage(pnlRiver.BackgroundImage);    for ( int i = 0; i < numberOfBoats; i++)        boatArr[i] = new MovingObj();    // Creates images    boatArr[0].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[1].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[2].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[3].Picture = Image.FromFile(Application.StartupPath         + "\\boat_medium.png" );    boatArr[4].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[5].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[6].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[7].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[8].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[9].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    LocateBoat();    // Creates tiger    pnlTiger.BackgroundImage = new Bitmap(pnlTiger.Width,        pnlTiger.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    tigerGraphics = Graphics.FromImage(pnlTiger.BackgroundImage);    tigerGraphics.Clear(pnlTiger.BackColor);    tiger1 = Image.FromFile(Application.StartupPath +        "\\tiger1.png" );    tiger2 = Image.FromFile(Application.StartupPath +        "\\tiger2.png" );    tiger = new MovingObj();    tiger.Rectangular = new Rectangle(0, 7,        tiger1.Width, tiger1.Height);    // Creates pnlStart    pnlStart.BackgroundImage = new Bitmap(pnlStart.Width,        pnlStart.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    startGraphics = Graphics.FromImage(pnlStart.BackgroundImage);    startGraphics.Clear(pnlStart.BackColor);    // Creates jumper house    pnlHouse.BackgroundImage = new Bitmap(pnlHouse.Width,        pnlHouse.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    houseGraphics = Graphics.FromImage(pnlHouse.BackgroundImage);    houseGraphics.Clear(pnlHouse.BackColor);    // Reads jumper graphics file    jumperUp = Image.FromFile(Application.StartupPath +        "\\jumper_up.png" );    jumperLeft = Image.FromFile(Application.StartupPath +        "\\jumper_left.png" );    jumperDown = Image.FromFile(Application.StartupPath +        "\\jumper_down.png" );    jumperRight = Image.FromFile(Application.StartupPath +        "\\jumper_right.png" );    jumperInHouse = Image.FromFile(Application.StartupPath +        "\\jumper_house.png" );    jumper = new MovingObj();     soundJump = new         System.Media.SoundPlayer(Application.StartupPath +         "\\jump.wav" );    soundJump.Load();    soundCollide = new         System.Media.SoundPlayer(Application.StartupPath +         "\\tabrak.wav" );    soundCollide.Load();    soundTiger = new        System.Media.SoundPlayer(Application.StartupPath +        "\\tiger.wav" );    soundTiger.Load();    soundDrowned = new        System.Media.SoundPlayer(Application.StartupPath +        "\\drowned.wav" );    soundDrowned.Load();    soundHouse = new        System.Media.SoundPlayer(Application.StartupPath +        "\\house.wav" );    soundHouse.Load();} &#124;

 |
| Step 65 | Add the modified code to DrawHouse function to initialize jumperInHouseArr array whenever the house panel is redrawn: 

&#124; 1234567891011121314151617 &#124; private void DrawHouse(){    houseGraphics.FillRectangle(brushHouse, 0, 0,        pnlHouse.Width, pnlHouse.Height);    rectHouse[0] = new Rectangle(70, 20, 60, 60);    rectHouse[1] = new Rectangle(180, 20, 60, 60);    rectHouse[2] = new Rectangle(290, 20, 60, 60);    rectHouse[3] = new Rectangle(400, 20, 60, 60);    rectHouse[4] = new Rectangle(510, 20, 60, 60);    for ( int i = 0; i < 5; i++)    {        houseGraphics.FillRectangle(Brushes.Blue, rectHouse[i]);        jumperInHouseArr[i] = false ;    }    pnlHouse.Refresh();} &#124;

 |
| Step 66 | Now you can add to the Tick event of timStatus timer to check for collisions on the house panel. Before doing this, first remove the following two lines of code from the DrawJumper method: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839 &#124; public void DrawJumper(){    if (jumperLocation == 0)    {        jumper.Rectangular.Y = 0;        jumper.Draw(startGraphics);        pnlStart.Refresh();    }    else if (jumperLocation == 1 &#124;&#124; jumperLocation == 2 &#124;&#124;        jumperLocation == 3)    {        jumper.Rectangular.Y = 140 - 45 * jumperLocation;        jumper.Draw(roadGraphics);        pnlRoad.Refresh();    }    else if (jumperLocation == 4)    {        jumper.Rectangular.Y = 0;        jumper.Draw(tigerGraphics);        pnlTiger.Refresh();    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;        jumperLocation == 7)    {        jumper.Rectangular.Y = 120 - 40 * (jumperLocation - 4);        jumper.Draw(riverGraphics);        pnlRiver.Refresh();    }    else if (jumperLocation == 8)    {        jumper.Rectangular.Y = 40;        jumper.Draw(houseGraphics);        pnlHouse.Refresh();    }} &#124;

You will only draw a jumper (in the Tick event of timStatus timer) on the house panel if the jumper reaches the house safely. |
| Step 67 | When the jumper reaches the house level, you check: 
*   Is the jumper in house rectangular? If so, continue; if not, the journey ends.
*   Is there jumper in the house rectangular? If so, the journey ends; if not, jumperInHouse is placed on the house rectangular and a certain sound is played.
*   Have all the jumpers arrived home? If so, clean the house and continue with the new jumper.
*   If not, continue with a new jumper.

Modify the Tick event of the timStatus timer to implement these steps:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990 &#124; private void timStatus_Tick( object sender, EventArgs e){    // Check collision    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        // Vehicles        for ( int i = 0; i < numberOfVehicles; i++)        {            if (vehicleArr[i].IsVisible)            {                if (DoesCollide(vehicleArr[i].Rectangular,                    jumper.Rectangular, 10))                {                    JumperNoMore();                    return ;                }            }        }    }    else if (jumperLocation == 4)    {        // tiger        if (tiger.IsVisible)        {            if (DoesCollide( tiger. Rectangular , jumper.Rectangular , 1))            {                JumperNoMore();                return ;            }        }    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;        jumperLocation == 7)    {       // Checks whether jumper is on the boat       if (onBoat == -1)        {            for ( int i = 0; i < numberOfBoats; i++)            {                if (boatArr[i].IsVisible)                {                    if (DoesCollide(boatArr[i].Rectangular,                        jumper.Rectangular, 80))                    {                        onBoat = i;                        return ;                    }                }            }            if (onBoat == -1)            {                JumperNoMore();                return ;            }        }    }    else if (jumperLocation == 8)    {        // Move to house        for ( int i = 0; i < 5; i++)        {            if (!jumperInHouseArr[i] &&                DoesCollide(rectHouse[i],                jumper.Rectangular, 100))            {                jumperInHouseArr[i] = true ;                houseGraphics.DrawImage(jumperInHouse,                    rectHouse[i].X + 10, rectHouse[i].Y + 10,                    jumperInHouse.Width, jumperInHouse.Height);                pnlHouse.Refresh();                soundHouse.PlaySync();                getNewJumper();                 // Check for collision                for ( int j = 0; j < 5; j++)                    if (!jumperInHouseArr[j])                        return ;                DrawHouse()                return ;            }        }        JumperNoMore();    }} &#124;

You can now understand how this code works. If the jumper maneuvers into the empty house, it will be drawn there and a sound will be played. If no collision or selected location has been filled, the jumper’s journey ends. If all the houses are filled, the houses will be emptied again. |
| Step 68 | Modify JumperNoMore function: 

&#124; 123456789101112131415161718192021222324252627 &#124; private void JumperNoMore(){    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        soundCollide.Play();    }    else if (jumperLocation == 4)    {        soundTiger.Play();    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6       &#124;&#124; jumperLocation == 7)    {        soundDrowned.Play();    }    else if (jumperLocation == 8)    {        soundDrowned.Play();    }    RemoveJumper();    getNewJumper();} &#124;

 |
| Step 69 | When the jumper can't get to the house, the sound of drowning will be played, the jumper is removed, and a new jumper is displayed. Save and run the project. Start the game. You can now move the jumper through the path, avoid the tiger, cross the river, and get to the house, as shown in Figure 5.16. |
| Step 70 | Like what is programmed, you can play this game forever, indefinitely. You have an infinite number of jumpers and the game remains at the same difficulty level no matter how long you play the game. You will change it now. First, you will limit the number of jumpers that are available in one game. After all your jumpers get home safely, the game will be over. Second, every time all the jumpers get home safely, you will increase the difficulty level of the game by speeding up all the moving objects, adding more vehicles and removing some boats in the river. The idea of ​​increasing the difficulty level is a fun feature of video games.![](Image00081.jpg)Figure 5.16 User can now move the jumper through the path, avoid the tiger, cross the river, and get to the houseYou will start with Level 1 (which is indicated in the title area of ​​the form). This is the level used so far (7 vehicles and 12 boats in the river). At this initial level, you will start with the five jumpers. You will display the number of remaining jumpers (using jumperUp , Image variable) in the top right corner of the form. Add the following declarations at the form-level to identify the level (level), keep track of the remaining jumpers ( remJumper ), and specify the form as a graphic object ( formGraphics ): 

&#124; 12 &#124; int level, remJumper;Graphics formGraphics; &#124;

 |
| Step 71 | Modify the form's Load event method to create new graphical objects: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148 &#124; private void FormJumper_Load( object sender, EventArgs e){    // From Graphics    this .BackgroundImage = new Bitmap( this .Width, this .Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    formGraphics = Graphics.FromImage( this .BackgroundImage);    formGraphics.Clear( this .BackColor);    // Creates road and vehicles    pnlRoad.BackgroundImage = new Bitmap(pnlRoad.Width,               pnlRoad.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    roadGraphics = Graphics.FromImage(pnlRoad.BackgroundImage);    for ( int i = 0; i < numberOfVehicles; i++)        vehicleArr[i] = new MovingObj();    vehicleArr[0].Picture = Image.FromFile(Application.StartupPath        + "\\trailer_right.png" );    vehicleArr[1].Picture = Image.FromFile(Application.StartupPath        + "\\truck_right.png" );    vehicleArr[2].Picture = Image.FromFile(Application.StartupPath        + "\\car_right.png" );    vehicleArr[3].Picture = Image.FromFile(Application.StartupPath        + "\\car_right.png" );    vehicleArr[4].Picture = Image.FromFile(Application.StartupPath        + "\\truck_right.png" );    vehicleArr[5].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[6].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    vehicleArr[7].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    vehicleArr[8].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[9].Picture = Image.FromFile(Application.StartupPath        + "\\trailer_left.png" );    vehicleArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\car_left.png" );    vehicleArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\truck_left.png" );    LocateVehicle();    // Creates river and boats    pnlRiver.BackgroundImage = new Bitmap(pnlRiver.Width,        pnlRiver.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    riverGraphics = Graphics.FromImage(pnlRiver.BackgroundImage);    for ( int i = 0; i < numberOfBoats; i++)        boatArr[i] = new MovingObj();    // Creates images    boatArr[0].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[1].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[2].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[3].Picture = Image.FromFile(Application.StartupPath         + "\\boat_medium.png" );    boatArr[4].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[5].Picture = Image.FromFile(Application.StartupPath        + "\\boat_small.png" );    boatArr[6].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[7].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[8].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[9].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    boatArr[10].Picture = Image.FromFile(Application.StartupPath        + "\\boat_medium.png" );    boatArr[11].Picture = Image.FromFile(Application.StartupPath        + "\\boat_big.png" );    LocateBoat();    // Creates tiger    pnlTiger.BackgroundImage = new Bitmap(pnlTiger.Width,        pnlTiger.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    tigerGraphics = Graphics.FromImage(pnlTiger.BackgroundImage);    tigerGraphics.Clear(pnlTiger.BackColor);    tiger1 = Image.FromFile(Application.StartupPath +        "\\tiger1.png" );    tiger2 = Image.FromFile(Application.StartupPath +        "\\tiger2.png" );    tiger = new MovingObj();    tiger.Rectangular = new Rectangle(0, 7,        tiger1.Width, tiger1.Height);    // Creates pnlStart    pnlStart.BackgroundImage = new Bitmap(pnlStart.Width,        pnlStart.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    startGraphics = Graphics.FromImage(pnlStart.BackgroundImage);    startGraphics.Clear(pnlStart.BackColor);    // Creates jumper house    pnlHouse.BackgroundImage = new Bitmap(pnlHouse.Width,        pnlHouse.Height,        System.Drawing.Imaging.PixelFormat.Format24bppRgb);    houseGraphics = Graphics.FromImage(pnlHouse.BackgroundImage);    houseGraphics.Clear(pnlHouse.BackColor);    // Reads jumper graphics file    jumperUp = Image.FromFile(Application.StartupPath +        "\\jumper_up.png" );    jumperLeft = Image.FromFile(Application.StartupPath +        "\\jumper_left.png" );    jumperDown = Image.FromFile(Application.StartupPath +        "\\jumper_down.png" );    jumperRight = Image.FromFile(Application.StartupPath +        "\\jumper_right.png" );    jumperInHouse = Image.FromFile(Application.StartupPath +        "\\jumper_house.png" );    jumper = new MovingObj();     soundJump = new         System.Media.SoundPlayer(Application.StartupPath +         "\\jump.wav" );    soundJump.Load();    soundCollide = new         System.Media.SoundPlayer(Application.StartupPath +         "\\tabrak.wav" );    soundCollide.Load();    soundTiger = new        System.Media.SoundPlayer(Application.StartupPath +        "\\tiger.wav" );    soundTiger.Load();    soundDrowned = new        System.Media.SoundPlayer(Application.StartupPath +        "\\drowned.wav" );    soundDrowned.Load();    soundHouse = new        System.Media.SoundPlayer(Application.StartupPath +        "\\house.wav" );    soundHouse.Load();} &#124;

 |
| Step 72 | Modify the Click event method of btnStartPause to initialize the new variables and represent the remaining jumpers in the top right corner of the form: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        // Removes cars for Level 1        vehicleArr[0].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[3].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[4].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[6].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[10].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();        LocateBoat();        for ( int i = 0; i < numberOfBoats; i++)            boatArr[i].Draw(riverGraphics);        pnlRiver.Refresh();        level = 1;        this .Text = "Jumper - Level 1" ;        remJumper = 4;        for ( int i = 0; i < remJumper; i++)            formGraphics.DrawImage(jumperUp,                new Rectangle( this .Width - (i + 1) *                jumperUp.Width - 10, 5, jumperUp.Width,                jumperUp.Height));        this .Refresh();        DrawHouse()        getNewJumper();        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;        timStatus.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    pnlStart.Focus();} &#124;

![](Image00082.jpg)Figure 5.17 Four jumpers are now displayed in the top right corner of the formWhy do you give the remaining jumpers an initial value of 4 when the player is given five jumpers at the start of the game? The answer is that the first jumper is already on the form in the start panel. |
| Step 73 | Save and run the project. Click Start Game . Notice four jumpers are now displayed in the top right corner of the form as shown in Figure 5.16. |
| Step 74 | Every time the jumper’s journey ends (crashing into a vehicle or tiger, or falling into the river), you want to remove one jumper from the remaining jumpers and check whether the game has ended (there are no more jumpers left). When the game is over, you will sound the game over. This gameOver.wav sound file has been provided in the bin\Debug folder of your project.Add this declaration for the form-level sound: 

&#124; 1 &#124; System.Media.SoundPlayer soundGameOver; &#124;

Place these two declarations at the end of the Load method on the form to load this sound:

&#124; 123 &#124; soundGameOver = new System.Media.SoundPlayer(Application.StartupPath    + "\\gameOver.wav" );soundGameOver.Load(); &#124;

 |
| Step 75 | Modify JumperNoMore function to check for the number of remaining jumpers: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637 &#124; private void JumperNoMore(){    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        soundCollide.Play();    }    else if (jumperLocation == 4)    {        soundTiger.Play();    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6       &#124;&#124; jumperLocation == 7)    {        soundDrowned.Play();    }    else if (jumperLocation == 8)    {        soundDrowned.Play();    }    RemoveJumper();    formGraphics.FillRectangle( new SolidBrush( this .BackColor),        new Rectangle( this .Width - remJumper * jumperUp.Width - 10 ,        5, jumperUp.Width, jumperUp.Height));    remJumper--;    this .Refresh();    if (remJumper >= 0)        getNewJumper();    else        btnExitStop.PerformClick();} &#124;

 |
| Step 76 | Notice how the location of the jumper to be deleted is determined using remJumper . Modify Click event on the btnExitStop control to play game-over sound: 

&#124; 12345678910111213141516171819202122232425262728 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        soundGameOver.PlaySync();        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        if (tiger.IsVisible)        {            tiger.Remove(tigerGraphics, new                SolidBrush(pnlTiger.BackColor));            pnlTiger.Refresh();        }        if (jumper.IsVisible)            RemoveJumper();        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;        timStatus.Enabled = false ;    }    else    {        this .Close();    }} &#124;

 |
| Step 77 | Save and run the project. Play until the remaining five jumpers on the top right side of the form are all cleared. Make sure the game ends with the game-over sound played. |
| Step 78 | So, now, the game is not endless, because you have limited the number of jumpers available. Next, you write logic code that increases the difficulty of the game as new level is reached. A new level is reached when you can get all five jumpers to house safely. At that point, you will play another sound, which uses newlevel.wav file, which has been provided in the bin\Debug folder in your project.Add a declaration for this sound at the form-level: 

&#124; 1 &#124; System.Media.SoundPlayer soundNewLevel; &#124;

Place these two declarations at the end of the Load method on the form to load this sound:

&#124; 123 &#124; soundNewLevel = new System.Media.SoundPlayer(Application.StartupPath    + "\\levelbaru.wav" );soundNewLevel.Load(); &#124;

 |
| Step 79 | You will write a new method GoToNextLevel to handle this level change. For now, place the following lines of code in this function: 

&#124; 1234567 &#124; private void GoToNextLevel(){    soundNewLevel.PlaySync();   level++;    this .Text = "Jumper - Level " + level.ToString();    DrawHouse();} &#124;

Here, you play a new level sound, increment the level variable and clear the house panel. |
| Step 80 | GoToNextLevel method is called from the Tick event method of timStatus timer. Make modifications to implement this: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273747576777879808182838485868788899091 &#124; private void timStatus_Tick( object sender, EventArgs e){    // Check collision    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        // Vehicles        for ( int i = 0; i < numberOfVehicles; i++)        {            if (vehicleArr[i].IsVisible)            {                if (DoesCollide(vehicleArr[i].Rectangular,                    jumper.Rectangular, 10))                {                    JumperNoMore();                    return ;                }            }        }    }    else if (jumperLocation == 4)    {        // tiger        if (tiger.IsVisible)        {            if (DoesCollide( tiger. Rectangular , jumper.Rectangular , 1))            {                JumperNoMore();                return ;            }        }    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;        jumperLocation == 7)    {        // Checks whether jumper is on the boat        if (onBoat == -1)        {            for ( int i = 0; i < numberOfBoats; i++)            {                if (boatArr[i].IsVisible)                {                    if (DoesCollide(boatArr[i].Rectangular,                        jumper.Rectangular, 80))                    {                        onBoat = i;                        return ;                    }                }            }            if (onBoat == -1)            {                JumperNoMore();                return ;            }        }    }    else if (jumperLocation == 8)    {        // Move to house        for ( int i = 0; i < 5; i++)        {            if (!jumperInHouseArr[i] &&                DoesCollide(rectHouse[i],                jumper.Rectangular, 100))            {                jumperInHouseArr[i] = true ;                houseGraphics.DrawImage(jumperInHouse,                    rectHouse[i].X + 10, rectHouse[i].Y + 10,                    jumperInHouse.Width, jumperInHouse.Height);                pnlHouse.Refresh();                soundHouse.PlaySync();                getNewJumper();                 // Check for collision                for ( int j = 0; j < 5; j++)                    if (!jumperInHouseArr[j])                        return ;                DrawHouse()                GoToNextLevel();                                return ;            }        }        JumperNoMore();    }} &#124;

 |
| Step 81 | Save and run the project. Play the program until the five jumpers enter all the houses available and make sure you move up to the next level, as shown in Figure 5.18.![](Image00083.jpg)Figure 5.18 After five jumpers enter all the houses and game moves up to the next levelWhen testing the game, you might be a little tired of trying to make the five jumpers get to their house. Here's a trick you can do. Look at the code where you checked the five houses whether they were filled in or not (in the Tick event of the timStatus timer): 

&#124; 123 &#124; // Check for collisionfor ( int j = 0; j < 5; j++)    if (!jumperInHouseArr[j])        return ; &#124;

Change for (int j = 0; j <5; j ++) to for (int j = 2; j <3; j ++) . With this change, you only need to make one jumper to the middle house to complete a level. This makes your job checking the levels easier to do. Make sure to return it to for (int j = 0; j <5; j ++) after you finish the level check. |
| Step 82 | You can now move to higher levels with each group of jumpers arriving at their home safely. At each level, of course, you want the game to change (more difficult). There are a number of rules that can be made. At higher levels, all objects are faster, the number of vehicles is increased and some boats are removed. And, at each level, you will be given a new jumper (up to a maximum of five). The rules are developed here: 
*   Decrement Interval property of timRiver and timRoad by 10 (minimum value 30).
*   If number of levels are odd (> 1), a jumper is added (maximum number of 5).
*   At Level 2, boatArr[0] is deleted.
*   At Level 3, boatArr [6] removed, vehicleArr[0] and vehicleArr[4] added.
*   At Level 4, boatArr[11] removed, vehicleArr[6] and vehicleArr[10] added.
*   At Level 5, vehicleArr[4] added.

Once you reach Level 5, there are 12 vehicles on the road and 9 boats on the river. At this level, the Interval property for the river and road panels is lowered to 40 milliseconds. At each level, you also reposition the boats and vehicles to all position to avoid overlapping problem.All of the above rules are implemented in GoToNextLevel function:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960 &#124; private void GoToNextLevel(){    soundNewLevel.PlaySync();    level++;    this .Text = "Jumper - Level " + level.ToString();    DrawHouse();    // Moves faster    timRoad.Interval -= 10;    if (timRoad.Interval < 30)        timRoad.Interval = 30;    timRiver.Interval -= 10;    if (timRiver.Interval < 30)        timRiver.Interval = 30;    // Increases jumpers on next level (max 5)    if (level % 2 == 1)    {        if (remJumper < 5)        {            remJumper++;            formGraphics.DrawImage(jumperUp,                new Rectangle( this .Width - remJumper *                jumperUp.Width - 10, 5, jumperUp.Width,                jumperUp.Height));            this .Refresh();        }    }    // Reposition boats and cars    LocateBoat();    LocateVehicle();    // Erases boats, increases cars    switch (level)    {        case 2:            boatArr[0].Remove(riverGraphics, new                SolidBrush(pnlRiver.BackColor));            break ;        case 3:            boatArr[6].Remove(riverGraphics, new                SolidBrush(pnlRiver.BackColor));            vehicleArr[0].Draw(roadGraphics);            vehicleArr[4].Draw(roadGraphics);            break ;        case 4:            boatArr[11].Remove(riverGraphics,                new SolidBrush(pnlRiver.BackColor));            vehicleArr[6].Draw(roadGraphics);            vehicleArr[10].Draw(roadGraphics);            break ;        default :            vehicleArr[3].Draw(roadGraphics);            break ;    }} &#124;

 |
| Step 83 | Since you have changed the Interval property of timRoad and timRiver , you need to make sure that they are returned to their original values ​​when a new game starts. Add the following modified code to the Click event method on btnStartPause : 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        // Removes cars for Level 1        vehicleArr[0].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[3].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[4].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[6].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[10].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();        LocateBoat();        for ( int i = 0; i < numberOfBoats; i++)            boatArr[i].Draw(riverGraphics);        pnlRiver.Refresh();        level = 1;        this .Text = "Jumper - Level 1" ;        remJumper = 4;        for ( int i = 0; i < remJumper; i++)            formGraphics.DrawImage(jumperUp,                new Rectangle( this .Width - (i + 1) *                jumperUp.Width - 10, 5, jumperUp.Width,                jumperUp.Height));        this .Refresh();        DrawHouse()        getNewJumper();        // Resets Interval        timRoad.Interval = 80;        timRiver.Interval = 80;        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;        timStatus.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    pnlStart.Focus();} &#124;

 |
| Step 84 | Save and run the project. See how the game changes as you reach higher levels. |
| Step 85 | Every time someone plays a game, he certainly wants to know the score that was obtained. And, of course, he wanted to see if he was better than other people. Here you will add capabilities to this game. This scoring will require rules to be defined later.Add this declaration at the form level: 

&#124; 1 &#124; int score, highestScore; &#124;

This score tracks the score in the game being played, while highestScore tracks the highest score ever played.Add this line of code at the end of the form's Load event method to initialize highestScore to zero:

&#124; 1 &#124; highestScore = 0; &#124;

 |
| Step 86 | Add the modified code to the Click event method of btnStartPause control to reset the score for each new game: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475 &#124; private void btnStartPause_Click( object sender, EventArgs e){    if (btnStartPause.Text == "Start Game" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Text = "Stop Game" ;        LocateVehicle();        for ( int i = 0; i < numberOfVehicles; i++)            vehicleArr[i].Draw(roadGraphics);        // Removes cars for Level 1        vehicleArr[0].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[3].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[4].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[6].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        vehicleArr[10].Remove(roadGraphics,            new SolidBrush(pnlRoad.BackColor));        pnlRoad.Refresh();        LocateBoat();        for ( int i = 0; i < numberOfBoats; i++)            boatArr[i].Draw(riverGraphics);        pnlRiver.Refresh();        score = 0;        lblScore.Text = "0" ;        level = 1;        this .Text = "Jumper - Level 1" ;        remJumper = 4;        for ( int i = 0; i < remJumper; i++)            formGraphics.DrawImage(jumperUp,                new Rectangle( this .Width - (i + 1) *                jumperUp.Width - 10, 5, jumperUp.Width,                jumperUp.Height));        this .Refresh();        DrawHouse()        getNewJumper();        // Resets Interval        timRoad.Interval = 80;        timRiver.Interval = 80;        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    else if (btnStartPause.Text == "Pause Game" )    {        btnStartPause.Text = "Start Again" ;        btnExitStop.Enabled = false ;        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;        timStatus.Enabled = false ;    }    else if (btnStartPause.Text == "Start Again" )    {        btnStartPause.Text = "Pause Game" ;        btnExitStop.Enabled = true ;        timRoad.Enabled = true ;        timRiver.Enabled = true ;        timTiger.Enabled = true ;        timStatus.Enabled = true ;    }    pnlStart.Focus();} &#124;

 |
| Step 87 | The scoring rules used: 
*   Each successful jumping forward is awarded 100 points.
*   Every successful reverse jumping is given 50 points.
*   Each successful jumping left or right is awarded 1 point.
*   Each jumper who makes it to the house is awarded 200 points.
*   Each level completed is awarded 1000 points.

Modify the form's KeyDown event method to increase the scoring for each jump:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354 &#124; private void FormJumper_KeyDown( object sender, KeyEventArgs e){    if (!timRiver.Enabled)        return ;    // Removed from current location    RemoveJumper();    if (e.KeyCode == Keys.Up)    {        score += 100;        onBoat = -1;        soundJump.Play();        jumper.Picture = jumperUp;        jumperLocation++;        if (jumperLocation > 8)            jumperLocation = 8;    }    else if (e.KeyCode == Keys.Left)    {        score += 1;        onBoat = -1;        soundJump.Play();        jumper.Picture = jumperLeft;        if (jumper.Rectangular.X > 0)            jumper.Rectangular.X -= 40;    }    else if (e.KeyCode == Keys.Down)    {        score += 50;        onBoat = -1;        soundJump.Play();        jumper.Picture = jumperDown;        jumperLocation--;        if (jumperLocation < 0)            jumperLocation = 0;    }    else if (e.KeyCode == Keys.Right)    {        score += 1;        onBoat = -1;        soundJump.Play();        jumper.Picture = jumperRight;        if (jumper.Rectangular.X < 600)            jumper.Rectangular.X += 40;    }    // Draws in new location    DrawJumper();} &#124;

 |
| Step 88 | The score for the jumper who made it to the house and the score for each level, as well as the update of the score labels were carried out on the Tick event method of timStatus : 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273747576777879808182838485868788899091929394 &#124; private void timStatus_Tick( object sender, EventArgs e){    UpdateScore();    // Check collision    if (jumperLocation == 1 &#124;&#124; jumperLocation == 2        &#124;&#124; jumperLocation == 3)    {        // Vehicles        for ( int i = 0; i < numberOfVehicles; i++)        {            if (vehicleArr[i].IsVisible)            {                if (DoesCollide(vehicleArr[i].Rectangular,                    jumper.Rectangular, 10))                {                    JumperNoMore();                    return ;                }            }        }    }    else if (jumperLocation == 4)    {        // tiger        if (tiger.IsVisible)        {            if (DoesCollide( tiger.Rectangular, jumper.Rectangular, 1))            {                JumperNoMore();                return ;            }        }    }    else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;        jumperLocation == 7)    {        // Checks whether jumper is on the boat        if (onBoat == -1)        {            for ( int i = 0; i < numberOfBoats; i++)            {                if (boatArr[i].IsVisible)                {                    if (DoesCollide(boatArr[i].Rectangular,                        jumper.Rectangular, 80))                    {                        onBoat = i;                        return ;                    }                }            }            if (onBoat == -1)            {                JumperNoMore();                return ;            }        }    }    else if (jumperLocation == 8)    {        // Move to house        for ( int i = 0; i < 5; i++)        {            if (!jumperInHouseArr[i] &&                DoesCollide(rectHouse[i],                jumper.Rectangular, 100))            {                score += 200;                jumperInHouseArr[i] = true ;                houseGraphics.DrawImage(jumperInHouse,                    rectHouse[i].X + 10, rectHouse[i].Y + 10,                    jumperInHouse.Width, jumperInHouse.Height);                pnlHouse.Refresh();                soundHouse.PlaySync();                getNewJumper();                 // Check for collision                for ( int j = 0; j < 5; j++)                    if (!jumperInHouseArr[j])                        return ;                score += 200;                GoToNextLevel();                                return ;            }        }        JumperNoMore();    }} &#124;

 |
| Step 89 | The score display is updated in the method UpdateScore : 

&#124; 12345678910111213 &#124; private void UpdateScore(){    // Updates score    lblScore.Text = score.ToString();    lblScore.Refresh();    if (score > highestScore)    {        highestScore = score;        lblHighestScore.Text = highestScore.ToString();    }} &#124;

 |
| Step 90 | Notice how the high score label controls are updated as needed. Add the modified code to the Click method of btnExitStop to update the score when the game is stopped. This line is required when the game is stopped before the score update is made: 

&#124; 1234567891011121314151617181920212223242526272829 &#124; private void btnExitStop_Click( object sender, EventArgs e){    if (btnExitStop.Text == "Stop Game" )    {        soundGameOver.PlaySync();        btnExitStop.Text = "Exit" ;        btnStartPause.Text = "Start Game" ;        if (tiger.IsVisible)        {            tiger.Remove(tigerGraphics, new                SolidBrush(pnlTiger.BackColor));            pnlTiger.Refresh();        }        if (jumper.IsVisible)            RemoveJumper();        timRoad.Enabled = false ;        timRiver.Enabled = false ;        timTiger.Enabled = false ;        timStatus.Enabled = false ;        UpdateScore();    }    else    {        this .Close();    }} &#124;

 |
| Step 91 | Save and run the project. You now have a score updatedwhile playing, as shown in Figure 5.19.![](Image00084.jpg)Figure 5.19 Score updated while user is playing |
|  |  |

| MovingObj.cs |  |
|  | 12345678910111213141516171819202122232425262728293031323334353637 | using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;using System.Data;namespace Jumper{    class MovingObj    {        public Image Picture;        public Rectangle Rectangular;        public int Speed;        public bool IsVisible = false ;        public void Draw(Graphics g)        {            g.DrawImage( this .Picture, this .Rectangular);            this .IsVisible = true ;        }        public void Move(Graphics g, Brush bc)        {            g.FillRectangle(bc, this .Rectangular);            this .Rectangular.X += this .Speed;            g.DrawImage( this .Picture, this .Rectangular);        }        public void Remove(Graphics g, Brush bc)        {            g.FillRectangle(bc, this .Rectangular);            this .IsVisible = false ;        }    }} |
|  |  |  |  |

| Jumper.cs |
| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197198199200201202203204205206207208209210211212213214215216217218219220221222223224225226227228229230231232234235236237238239240241242243244245246247248249250251252253254255256257258259260261262263264265266267268269270271272273274275276277278279280281282283284285286287288289290291292293294295296297298299300301302303304305306307308309310311312313314315316317318319320321322323324325326327328329330331332333334335336337338339340341342343344345346347348349350351352353354355356357358359360361362363364365366367368369370371372373374375376377378379380381382383384385386387388389390391392393394395396397398399400401402403404405406407408409410411412413414415416417418419420421422423424425426427428429430431432433434435436437438439440441442443444445446447448449450451452453454455456457458459460461462463464465466467468469470471472473474475476477478479480481482483484485486487488489490491492493494495496497498499500501502503504505506507508509510511512513514515516517518519520521522523524525526527528529530531532533534535536537538539540541542543545546547548549550551552553554555556557558559560561562563564565566567568569570571572573574575576577578579580581582583584585586587588589590591592593594595596597598599600601602603604605606607608609610611612613614615616617618619620621622623624625626627628629630631632633634635636637638639640641642643644645646647648649650651652653654655656657658659660661662663664665666667668669670671672673674675676677678679680681682683684685686687688689690691692693694695696697698699700701702703704705706707708709710712713714715716717718719720721722723724725726727728729730731732733734735736737738739740741742743744745746747748749750751752753754755756757758759760761762763764765766767768769770771772773774775776777778779780781782783784785786787788789790791792793794795796797798799800801802803804805806807808809810811812813814815816817818819820821822823824825826827828829830831832833834835836837838839840841842843844845846847848849850851852853854855856857858859860861862 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;namespace Jumper{    public partial class FormJumper : Form    {        const int numberOfVehicles = 12;        MovingObj[] vehicleArr = new MovingObj[numberOfVehicles];        Graphics roadGraphics;        const int numberOfBoats = 12;        MovingObj[] boatArr = new MovingObj[numberOfBoats];        Graphics riverGraphics;        Random myRand = new Random();        MovingObj tiger;        Image tiger1, tiger2;        int tigerImage;        Graphics tigerGraphics;        MovingObj jumper;        Image jumperUp, jumperLeft, jumperDown, jumperRight;        int jumperLocation;        Graphics startGraphics;        Graphics houseGraphics;        System.Media.SoundPlayer soundJump;        System.Media.SoundPlayer soundCollide;        System.Media.SoundPlayer soundTiger;        System.Media.SoundPlayer soundDrowned;        int onBoat;        Rectangle[] rectHouse = new Rectangle[5];        TextureBrush brushHouse;        Image jumperInHouse;        System.Media.SoundPlayer soundHouse;        bool [] jumperInHouseArr = new bool [5];        int level, remJumper;        Graphics formGraphics;        System.Media.SoundPlayer soundGameOver;        System.Media.SoundPlayer soundNewLevel;        int score, highestScore;        public FormJumper ()        {            InitializeComponent();        }        private void FormJumper_Load( object sender, EventArgs e)        {            // From Graphics            this .BackgroundImage = new Bitmap( this .Width, this .Height,            System.Drawing.Imaging.PixelFormat.Format24bppRgb);            formGraphics = Graphics.FromImage( this .BackgroundImage);            formGraphics.Clear( this .BackColor);            // Creates road and vehicles            pnlRoad.BackgroundImage = new Bitmap(pnlRoad.Width, pnlRoad.Height,                 System.Drawing.Imaging.PixelFormat.Format24bppRgb);            roadGraphics = Graphics.FromImage(pnlRoad.BackgroundImage);            for ( int i = 0; i < numberOfVehicles; i++)                vehicleArr[i] = new MovingObj();            vehicleArr[0].Picture = Image.FromFile(Application.StartupPath +                "\\trailer_right.png" );            vehicleArr[1].Picture = Image.FromFile(Application.StartupPath +                "\\truck_right.png" );            vehicleArr[2].Picture = Image.FromFile(Application.StartupPath +                "\\car_right.png" );            vehicleArr[3].Picture = Image.FromFile(Application.StartupPath +                "\\car_right.png" );            vehicleArr[4].Picture = Image.FromFile(Application.StartupPath +                "\\truck_right.png" );            vehicleArr[5].Picture = Image.FromFile(Application.StartupPath +                "\\car_left.png" );            vehicleArr[6].Picture = Image.FromFile(Application.StartupPath +                "\\truck_left.png" );            vehicleArr[7].Picture = Image.FromFile(Application.StartupPath +                "\\truck_left.png" );            vehicleArr[8].Picture = Image.FromFile(Application.StartupPath +                "\\car_left.png" );            vehicleArr[9].Picture = Image.FromFile(Application.StartupPath +                "\\trailer_left.png" );            vehicleArr[10].Picture = Image.FromFile(Application.StartupPath +                "\\car_left.png" );            vehicleArr[11].Picture = Image.FromFile(Application.StartupPath +                "\\truck_left.png" );            LocateVehicle();            // Creates river and boats            pnlRiver.BackgroundImage = new Bitmap(pnlRiver.Width,                pnlRiver.Height,                System.Drawing.Imaging.PixelFormat.Format24bppRgb);            riverGraphics = Graphics.FromImage(pnlRiver.BackgroundImage);            for ( int i = 0; i < numberOfBoats; i++)                boatArr[i] = new MovingObj();            // Creates images            boatArr[0].Picture = Image.FromFile(Application.StartupPath +                "\\boat_medium.png" );            boatArr[1].Picture = Image.FromFile(Application.StartupPath +                "\\boat_big.png" );            boatArr[2].Picture = Image.FromFile(Application.StartupPath +                "\\boat_small.png" );            boatArr[3].Picture = Image.FromFile(Application.StartupPath +                "\\boat_medium.png" );            boatArr[4].Picture = Image.FromFile(Application.StartupPath +                "\\boat_medium.png" );            boatArr[5].Picture = Image.FromFile(Application.StartupPath +                "\\boat_small.png" );            boatArr[6].Picture = Image.FromFile(Application.StartupPath +                "\\boat_big.png" );            boatArr[7].Picture = Image.FromFile(Application.StartupPath +                "\\boat_medium.png" );            boatArr[8].Picture = Image.FromFile(Application.StartupPath +                "\\boat_big.png" );            boatArr[9].Picture = Image.FromFile(Application.StartupPath +                "\\boat_big.png" );            boatArr[10].Picture = Image.FromFile(Application.StartupPath +                "\\boat_medium.png" );            boatArr[11].Picture = Image.FromFile(Application.StartupPath +                "\\boat_big.png" );            LocateBoat();            // Creates tiger            pnlTiger.BackgroundImage = new Bitmap(pnlTiger.Width,                pnlTiger.Height,                System.Drawing.Imaging.PixelFormat.Format24bppRgb);            tigerGraphics = Graphics.FromImage(pnlTiger.BackgroundImage);            tigerGraphics.Clear(pnlTiger.BackColor);            tiger1 = Image.FromFile(Application.StartupPath + "\\tiger1.png" );            tiger2 = Image.FromFile(Application.StartupPath + "\\tiger2.png" );            tiger = new MovingObj();            tiger.Rectangular = new Rectangle(0, 7, tiger1.Width,                tiger1.Height);            // Creates pnlStart            pnlStart.BackgroundImage = new Bitmap(pnlStart.Width,                pnlStart.Height,                System.Drawing.Imaging.PixelFormat.Format24bppRgb);            startGraphics = Graphics.FromImage(pnlStart.BackgroundImage);            startGraphics.Clear(pnlStart.BackColor);            // Creates jumper house            pnlHouse.BackgroundImage = new Bitmap(pnlHouse.Width,                pnlHouse.Height,                System.Drawing.Imaging.PixelFormat.Format24bppRgb);            houseGraphics = Graphics.FromImage(pnlHouse.BackgroundImage);            houseGraphics.Clear(pnlHouse.BackColor);            brushHouse = new TextureBrush( new Bitmap(Application.StartupPath +                "\\bush.png" ));            DrawHouse();            // Reads jumper graphics file            jumperUp = Image.FromFile(Application.StartupPath +                "\\jumper_up.png" );            jumperLeft = Image.FromFile(Application.StartupPath +                "\\jumper_left.png" );            jumperDown = Image.FromFile(Application.StartupPath +                "\\jumper_down.png" );            jumperRight = Image.FromFile(Application.StartupPath +                "\\jumper_right.png" );            jumperInHouse = Image.FromFile(Application.StartupPath +                "\\jumper_house.png" );            jumper = new MovingObj();            soundJump = new System.Media.SoundPlayer(Application.StartupPath +                "\\jump.wav" );            soundJump.Load();            soundCollide = new System.Media.SoundPlayer(Application.StartupPath                + "\\tabrak.wav" );            soundCollide.Load();            soundTiger = new System.Media.SoundPlayer(Application.StartupPath +                "\\tiger.wav" );            soundTiger.Load();            soundDrowned = new System.Media.SoundPlayer(Application.StartupPath                + "\\drowned.wav" );            soundDrowned.Load();            soundHouse = new System.Media.SoundPlayer(Application.StartupPath +                "\\house.wav" );            soundHouse.Load();            soundGameOver = new System.Media.SoundPlayer(Application.StartupPath                + "\\gameOver.wav" );            soundGameOver.Load();            soundNewLevel = new System.Media.SoundPlayer(Application.StartupPath                + "\\newlevel.wav" );            soundNewLevel.Load();            highestScore = 0;        }        private void getNewJumper()        {            onBoat = -1;            jumperLocation = 0;            jumper.Rectangular = new Rectangle(320, 0,                jumperUp.Width, jumperUp.Height);            jumper.Picture = jumperUp;            jumper.Draw(startGraphics);            pnlStart.Refresh();        }        private void LocateBoat()        {            riverGraphics.Clear(pnlRiver.BackColor);            // Upper row            boatArr[0].Rectangular = new Rectangle(20, 0, 80, 40);            boatArr[0].Speed = 5;            boatArr[1].Rectangular = new Rectangle(140, 0, 120, 40);            boatArr[1].Speed = 5;            boatArr[2].Rectangular = new Rectangle(300, 0, 40, 40);            boatArr[2].Speed = 5;            boatArr[3].Rectangular = new Rectangle(400, 0, 80, 40);            boatArr[3].Speed = 5;            boatArr[4].Rectangular = new Rectangle(540, 0, 80, 40);            boatArr[4].Speed = 5;            // Middle row            boatArr[5].Rectangular = new Rectangle(60, 40, 40, 40);            boatArr[5].Speed = -3;            boatArr[6].Rectangular = new Rectangle(180, 40, 120, 40);            boatArr[6].Speed = -3;            boatArr[7].Rectangular = new Rectangle(360, 40, 80, 40);            boatArr[7].Speed = -3;            boatArr[8].Rectangular = new Rectangle(500, 40, 120, 40);            boatArr[8].Speed = -3;            // Lower row            boatArr[9].Rectangular = new Rectangle(40, 80, 120, 40);            boatArr[9].Speed = 2;            boatArr[10].Rectangular = new Rectangle(280, 80, 80, 40);            boatArr[10].Speed = 2;            boatArr[11].Rectangular = new Rectangle(480, 80, 120, 40);            boatArr[11].Speed = 2;        }        private void LocateVehicle()        {            roadGraphics.Clear(pnlRoad.BackColor);            // Draws lanes            roadGraphics.DrawLine(Pens.White, 0, 2, pnlRoad.Width, 2);            roadGraphics.DrawLine(Pens.White, 0, pnlRoad.Height - 2,                pnlRoad.Width, pnlRoad.Height - 2);            roadGraphics.DrawLine(Pens.White, 0, 92, pnlRoad.Width, 92);            roadGraphics.DrawLine(Pens.Yellow, 0, 47, pnlRoad.Width, 47);            roadGraphics.DrawLine(Pens.Yellow, 0, 49, pnlRoad.Width, 49);            // Upper lane            vehicleArr[0].Rectangular = new Rectangle(20, 5, 120, 40);            vehicleArr[0].Speed = 3;            vehicleArr[1].Rectangular = new Rectangle(200, 5, 80, 40);            vehicleArr[1].Speed = 3;            vehicleArr[2].Rectangular = new Rectangle(380, 5, 40, 40);            vehicleArr[2].Speed = 3;            vehicleArr[3].Rectangular = new Rectangle(540, 5, 40, 40);            vehicleArr[3].Speed = 3;            // Middle lane            vehicleArr[4].Rectangular = new Rectangle(40, 50, 80, 40);            vehicleArr[4].Speed = -3;            vehicleArr[5].Rectangular = new Rectangle(220, 50, 40, 40);            vehicleArr[5].Speed = -3;            vehicleArr[6].Rectangular = new Rectangle(360, 50, 80, 40);            vehicleArr[6].Speed = -3;            vehicleArr[7].Rectangular = new Rectangle(520, 50, 80, 40);            vehicleArr[7].Speed = -3;            // Lower lane            vehicleArr[8].Rectangular = new Rectangle(60, 95, 40, 40);            vehicleArr[8].Speed = -2;            vehicleArr[9].Rectangular = new Rectangle(180, 95, 120, 40);            vehicleArr[9].Speed = -2;            vehicleArr[10].Rectangular = new Rectangle(380, 95, 40, 40);            vehicleArr[10].Speed = -2;            vehicleArr[11].Rectangular = new Rectangle(520, 95, 80, 40);            vehicleArr[11].Speed = -2;        }        private void btnStartPause_Click( object sender, EventArgs e)        {            if (btnStartPause.Text == "Start Game" )            {                btnStartPause.Text = "Pause Game" ;                btnExitStop.Text = "Stop Game" ;                LocateVehicle();                for ( int i = 0; i < numberOfVehicles; i++)                    vehicleArr[i].Draw(roadGraphics);                // Removes cars for Level 1                vehicleArr[0].Remove(roadGraphics,                    new SolidBrush(pnlRoad.BackColor));                vehicleArr[3].Remove(roadGraphics,                    new SolidBrush(pnlRoad.BackColor));                vehicleArr[4].Remove(roadGraphics,                    new SolidBrush(pnlRoad.BackColor));                vehicleArr[6].Remove(roadGraphics,                    new SolidBrush(pnlRoad.BackColor));                vehicleArr[10].Remove(roadGraphics,                    new SolidBrush(pnlRoad.BackColor));                pnlRoad.Refresh();                LocateBoat();                for ( int i = 0; i < numberOfBoats; i++)                    boatArr[i].Draw(riverGraphics);                pnlRiver.Refresh();                score = 0;                lblScore.Text = "0" ;                level = 1;                this .Text = "Jumper - Level 1" ;                remJumper = 4;                for ( int i = 0; i < remJumper; i++)                    formGraphics.DrawImage(jumperUp, new Rectangle(                        this .Width - (i + 1) * jumperUp.Width - 10,                        5, jumperUp.Width, jumperUp.Height));                this .Refresh();                DrawHouse();                getNewJumper();                // Reset Interval                timRoad.Interval = 80;                timRiver.Interval = 80;                timRoad.Enabled = true ;                timRiver.Enabled = true ;                timTiger.Enabled = true ;                timStatus.Enabled = true ;            }            else if (btnStartPause.Text == "Pause Game" )            {                btnStartPause.Text = "Start Again" ;                btnExitStop.Enabled = false ;                timRoad.Enabled = false ;                timRiver.Enabled = false ;                timTiger.Enabled = false ;                timStatus.Enabled = false ;            }            else if (btnStartPause.Text == "Start Again" )            {                btnStartPause.Text = "Pause Game" ;                btnExitStop.Enabled = true ;                timRoad.Enabled = true ;                timRiver.Enabled = true ;                timTiger.Enabled = true ;                timStatus.Enabled = true ;            }            pnlStart.Focus();        }        private void btnExitStop_Click( object sender, EventArgs e)        {            if (btnExitStop.Text == "Stop Game" )            {                soundGameOver.PlaySync();                btnExitStop.Text = "Exit" ;                btnStartPause.Text = "Start Game" ;                if (tiger.IsVisible)                {                    tiger.Remove(tigerGraphics,                        new SolidBrush(pnlTiger.BackColor));                    pnlTiger.Refresh();                }                if (jumper.IsVisible)                    RemoveJumper();                timRoad.Enabled = false ;                timRiver.Enabled = false ;                timTiger.Enabled = false ;                timStatus.Enabled = false ;                UpdateScore();            }            else            {                this .Close();            }        }        private void timRoad_Tick( object sender, EventArgs e)        {            for ( int i = 0; i < numberOfVehicles; i++)            {                if (vehicleArr[i].IsVisible)                {                    vehicleArr[i].Move(roadGraphics,                        new SolidBrush(pnlRoad.BackColor));                    if ((vehicleArr[i].Rectangular.X > pnlRoad.Width &&                        vehicleArr[i].Speed > 0))                        vehicleArr[i].Rectangular.X = -120;                    if ((vehicleArr[i].Rectangular.X <                         -vehicleArr[i]. Picture.Width && vehicleArr[i].Speed < 0))                        vehicleArr[i].Rectangular.X = pnlRoad.Width +                            (120 - vehicleArr[i].Picture.Width);                }            }            pnlRoad.Refresh();        }        private void timRiver_Tick( object sender, EventArgs e)        {            for ( int i = 0; i < numberOfBoats; i++)            {                if (boatArr[i].IsVisible)                {                    boatArr[i].Move(riverGraphics,                        new SolidBrush(pnlRiver.BackColor));                    if (onBoat == i)                    {                        jumper.Rectangular.X += boatArr[i].Speed;                        if (jumper.Rectangular.X < 0 &#124;&#124; jumper.Rectangular.X >                            640 - jumper.Rectangular.Width)                        {                            JumperNoMore();                            return ;                        }                        jumper.Draw(riverGraphics);                    }                    if ((boatArr[i].Rectangular.X > pnlRiver.Width &&                          boatArr[i].Speed > 0))                        boatArr[i].Rectangular.X = -120;                    if ((boatArr[i].Rectangular.X < -boatArr[i].Picture.Width &&                            boatArr[i].Speed < 0))                        boatArr[i].Rectangular.X = pnlRiver.Width + (                            120 - boatArr[i].Picture.Width);                }            }            pnlRiver.Refresh();        }        private void timTiger_Tick( object sender, EventArgs e)        {            if (!tiger.IsVisible)            {                if (myRand.Next(49) == 0)                {                    tiger.Rectangular.X = -tiger1.Width;                    tiger.Speed = 5;                    tiger.Picture = tiger1;                    tigerImage = 1;                    tiger.Draw(tigerGraphics);                }            }            else            {                tiger.Move(tigerGraphics, new SolidBrush(pnlTiger.BackColor));                if (tigerImage == 1)                {                    tigerImage = 2;                    tiger.Picture = tiger2;                }                else                {                    tigerImage = 1;                    tiger.Picture = tiger1;                }                if (tiger.Rectangular.X > pnlTiger.Width)                    tiger.Remove(tigerGraphics,                        new SolidBrush(pnlTiger.BackColor));                pnlTiger.Refresh();            }        }        private void FormJumper_KeyDown( object sender, KeyEventArgs e)        {            if (!timRiver.Enabled)                return ;            // Removed from current location            RemoveJumper();            if (e.KeyCode == Keys.Up)            {                score += 100;                onBoat = -1;                soundJump.Play();                jumper.Picture = jumperUp;                jumperLocation++;                if (jumperLocation > 8)                    jumperLocation = 8;            }            else if (e.KeyCode == Keys.Left)            {                score += 1;                onBoat = -1;                soundJump.Play();                jumper.Picture = jumperLeft;                if (jumper.Rectangular.X > 0)                    jumper.Rectangular.X -= 40;            }            else if (e.KeyCode == Keys.Down)            {                score += 50;                onBoat = -1;                soundJump.Play();                jumper.Picture = jumperDown;                jumperLocation--;                if (jumperLocation < 0)                    jumperLocation = 0;            }            else if (e.KeyCode == Keys.Right)            {                score += 1;                onBoat = -1;                soundJump.Play();                jumper.Picture = jumperRight;                if (jumper.Rectangular.X < 600)                    jumper.Rectangular.X += 40;            }            // Draws in new location            DrawJumper();        }        public void RemoveJumper()        {            if (jumperLocation == 0)            {                jumper.Remove(startGraphics,                    new SolidBrush(pnlStart.BackColor));                pnlStart.Refresh();            }            else if (jumperLocation == 1 &#124;&#124; jumperLocation == 2 &#124;&#124;                  jumperLocation == 3)            {                jumper.Remove(roadGraphics, new SolidBrush(pnlRoad.BackColor));                pnlRoad.Refresh();            }            else if (jumperLocation == 4)            {                jumper.Remove(tigerGraphics,                    new SolidBrush(pnlTiger.BackColor));                pnlTiger.Refresh();            }            else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;                jumperLocation == 7)            {                jumper.Remove(riverGraphics,                    new SolidBrush(pnlRiver.BackColor));                pnlRiver.Refresh();            }        }        public void DrawJumper()        {            if (jumperLocation == 0)            {                jumper.Rectangular.Y = 0;                jumper.Draw(startGraphics);                pnlStart.Refresh();            }            else if (jumperLocation == 1 &#124;&#124; jumperLocation == 2 &#124;&#124;                jumperLocation == 3)            {                jumper.Rectangular.Y = 140 - 45 * jumperLocation;                jumper.Draw(roadGraphics);                pnlRoad.Refresh();            }            else if (jumperLocation == 4)            {                jumper.Rectangular.Y = 0;                jumper.Draw(tigerGraphics);                pnlTiger.Refresh();            }            else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;                jumperLocation == 7)            {                jumper.Rectangular.Y = 120 - 40 * (jumperLocation - 4);                jumper.Draw(riverGraphics);                pnlRiver.Refresh();            }            else if (jumperLocation == 8)            {                jumper.Rectangular.Y = 40;                jumper.Draw(houseGraphics);                pnlHouse.Refresh();            }        }        private bool DoesCollide(Rectangle rect1, Rectangle rect2, double percentage)        {            Rectangle collision;            collision = Rectangle.Intersect(rect1, rect2);            if (collision.Width * collision.Height >= percentage *                  rect2.Width * rect2.Height / 100)                return ( true );            else                return ( false );        }        private void timStatus_Tick( object sender, EventArgs e)        {            UpdateScore();            // Check collision            if (jumperLocation == 1 &#124;&#124; jumperLocation == 2 &#124;&#124; jumperLocation == 3)            {                // Vehicles                for ( int i = 0; i < numberOfVehicles; i++)                {                    if (vehicleArr[i].IsVisible)                    {                        if (DoesCollide(vehicleArr[i].Rectangular,                              jumper.Rectangular, 10))                        {                            JumperNoMore();                            return ;                        }                    }                }            }            else if (jumperLocation == 4)            {                // tiger                if (tiger.IsVisible)                {                    if (DoesCollide(tiger.Rectangular, jumper.Rectangular, 1))                    {                        JumperNoMore();                        return ;                    }                }            }            else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;                 jumperLocation == 7)            {                // Checks whether jumper is on the boat                if (onBoat == -1)                {                    for ( int i = 0; i < numberOfBoats; i++)                    {                        if (boatArr[i].IsVisible)                        {                            if (DoesCollide(boatArr[i].Rectangular,                                 jumper.Rectangular, 80))                            {                                onBoat = i;                                return ;                            }                        }                    }                    if (onBoat == -1)                    {                        JumperNoMore();                        return ;                    }                }            }            else if (jumperLocation == 8)            {                // Move to house                for ( int i = 0; i < 5; i++)                {                    if (!jumperInHouseArr[i] && DoesCollide(rectHouse[i],                          jumper.Rectangular, 100))                    {                        score += 200;                        jumperInHouseArr[i] = true ;                        houseGraphics.DrawImage(jumperInHouse, rectHouse[i].X + 10 ,                            rectHouse[i].Y + 10, jumperInHouse.Width,                            jumperInHouse.Height);                        pnlHouse.Refresh();                        soundHouse.PlaySync();                        getNewJumper();                        // Check for collision                        for ( int j = 0; j < 5; j++)                            if (!jumperInHouseArr[j])                                return ;                        score += 200;                        GoToNextLevel();                        return ;                    }                }                JumperNoMore();            }        }        private void UpdateScore()        {            // Updates score            lblScore.Text = score.ToString();            lblScore.Refresh();            if (score > highestScore)            {                highestScore = score;                lblHighestScore.Text = highestScore.ToString();            }        }        private void JumperNoMore()        {            if (jumperLocation == 1 &#124;&#124; jumperLocation == 2 &#124;&#124; jumperLocation == 3)            {                soundCollide.Play();            }            else if (jumperLocation == 4)            {                soundTiger.Play();            }            else if (jumperLocation == 5 &#124;&#124; jumperLocation == 6 &#124;&#124;                jumperLocation == 7)            {                soundDrowned.Play();            }            else if (jumperLocation == 8)            {                soundDrowned.Play();            }            RemoveJumper();            formGraphics.FillRectangle( new SolidBrush( this .BackColor),                new Rectangle( this .Width - remJumper * jumperUp.Width - 10,                5, jumperUp.Width, jumperUp.Height));            remJumper--;            this .Refresh();            if (remJumper >= 0)                getNewJumper();            else                btnExitStop.PerformClick();        }        private void DrawHouse()        {            houseGraphics.FillRectangle(brushHouse, 0, 0,                pnlHouse.Width, pnlHouse.Height);            rectHouse[0] = new Rectangle(70, 20, 60, 60);            rectHouse[1] = new Rectangle(180, 20, 60, 60);            rectHouse[2] = new Rectangle(290, 20, 60, 60);            rectHouse[3] = new Rectangle(400, 20, 60, 60);            rectHouse[4] = new Rectangle(510, 20, 60, 60);            for ( int i = 0; i < 5; i++)            {                houseGraphics.FillRectangle(Brushes.Blue, rectHouse[i]);                jumperInHouseArr[i] = false ;            }            pnlHouse.Refresh();        }        private void GoToNextLevel()        {            soundNewLevel.PlaySync();            level++;            this .Text = "Jumper - Level " + level.ToString();            DrawHouse();            // Moves faster            timRoad.Interval -= 10;            if (timRoad.Interval < 30)                timRoad.Interval = 30;            timRiver.Interval -= 10;            if (timRiver.Interval < 30)                timRiver.Interval = 30;            // Increases jumpers on next level (max 5)            if (level % 2 == 1)            {                if (remJumper < 5)                {                    remJumper++;                    formGraphics.DrawImage(jumperUp,                        new Rectangle( this . Width - remJumper * jumperUp.Width - 10,                        5, jumperUp.Width, jumperUp.Height));                    this .Refresh();                }            }            // Reposition boats and cars            LocateBoat();            LocateVehicle();            // Erases boats, increases cars            switch (level)            {                case 2:                    boatArr[0].Remove(riverGraphics,                        new SolidBrush(pnlRiver.BackColor));                    break ;                case 3:                    boatArr[6].Remove(riverGraphics,                        new SolidBrush(pnlRiver.BackColor));                    vehicleArr[0].Draw(roadGraphics);                    vehicleArr[4].Draw(roadGraphics);                    break ;                case 4:                    boatArr[11].Remove(riverGraphics,                        new SolidBrush(pnlRiver.BackColor));                    vehicleArr[6].Draw(roadGraphics);                    vehicleArr[10].Draw(roadGraphics);                    break ;                default :                    vehicleArr[3].Draw(roadGraphics);                    break ;            }        }    }} |
|  |  |