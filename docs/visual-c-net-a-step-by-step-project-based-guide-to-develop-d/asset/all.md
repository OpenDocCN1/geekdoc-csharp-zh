![](Image00084.jpg)

VISUAL C# .NET

A Step By Step, Project-Based Guide to Develop Desktop Applications

First Edition

VIVIAN SIAHAAN

RISMON HASIHOLAN SIANIPAR

Copyright © 2020 BALIGE Publishing

All rights reserved. No part of this book may be reproduced, stored in a retrieval system, or transmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embedded in critical articles or reviews. Every effort has been made in the preparation of this book to ensure the accuracy of the information presented. However, the information contained in this book is sold without warranty, either express or implied. Neither the authors, nor BALIGE Publishing or its dealers and distributors, will be held liable for any damages caused or alleged to have been caused directly or indirectly by this book. BALIGE Publishing has endeavored to provide trademark information about all of the companies and products mentioned in this book by the appropriate use of capitals. However, BALIGE Publishing cannot guarantee the accuracy of this information.

First published: August 2020

Production reference: 07082020

Published by BALIGE Publishing Ltd.

BALIGE, North Sumatera, Indonesia

ABOUT THE AUTHORS

![D:\vivi2.jpg](Image00000.jpg) Vivian Siahaan is a fast-learner who likes to do new things. She was born, raised in Hinalang Bagasan, Balige, on the banks of Lake Toba, and completed high school education from SMAN 1 Balige. She started herself learning Java, Android, JavaScript, CSS, C ++, Python, R, Visual Basic, Visual C #, MATLAB, Mathematica, PHP, JSP, MySQL, SQL Server, Oracle, Access, and other programming languages. She studied programming from scratch, starting with the most basic syntax and logic, by building several simple and applicable GUI applications. Animation and games are fields of programming that are interests that she always wants to develop. Besides studying mathematical logic and programming, the author also has the pleasure of reading novels. Vivian Siahaan has written dozens of ebooks that have been published on Sparta Publisher: Data Structure with Java; Java Programming: Cookbook; C ++ Programming: Cookbook; C Programming For High Schools / Vocational Schools and Students; Java Programming for SMA / SMK; Java Tutorial: GUI, Graphics and Animation; Visual Basic Programming: From A to Z; Java Programming for Animation and Games; C # Programming for SMA / SMK and Students; MATLAB For Students and Researchers; Graphics in JavaScript: Quick Learning Series; JavaScript Image Processing Methods: From A to Z; Java GUI Case Study: AWT & Swing; Basic CSS and JavaScript; PHP / MySQL Programming: Cookbook; Visual Basic: Cookbook; C ++ Programming for High Schools / Vocational Schools and Students; Concepts and Practices of C ++; PHP / MySQL For Students; C # Programming: From A to Z; Visual Basic for SMA / SMK and Students; C # .NET and SQL Server for High School / Vocational School and Students. At the ANDI Yogyakarta publisher, Vivian Siahaan also wrote a number of books including: Python Programming Theory and Practice; Python GUI Programming; Python GUI and Database; Build From Zero School Database Management System In Python / MySQL; Database Management System in Python / MySQL; Python / MySQL For Management Systems of Criminal Track Record Database; Java / MySQL For Management Systems of Criminal Track Records Database; Database and Critptography Using Java / MySQL; Build From Zero School Database Management System With Java / MySQL.

![D:\RH_SIANIPAR.jpg](Image00001.jpg) Rismon Hasiholan Sianipar was born in Pematang Siantar, in 1994\. After graduating from SMAN 3 Pematang Siantar 3, the writer traveled to the city of Jogjakarta. In 1998 and 2001 the author completed his Bachelor of Engineering (S.T) and Master of Engineering (M.T) education in the Electrical Engineering of Gadjah Mada University, under the guidance of Prof. Dr. Adhi Soesanto and Prof. Dr. Thomas Sri Widodo, focusing on research on non-stationary signals by analyzing their energy using time-frequency maps. Because of its non-stationary nature, the distribution of signal energy becomes very dynamic on a time-frequency map. By mapping the distribution of energy in the time-frequency field using discrete wavelet transformations, one can design non-linear filters so that they can analyze the pattern of the data contained in it. In 2003, the author received a Monbukagakusho scholarship from the Japanese Government. In 2005 and 2008, he completed his Master of Engineering (M.Eng) and Doctor of Engineering (Dr.Eng) education at Yamaguchi University, under the guidance of Prof. Dr. Hidetoshi Miike. Both the master's thesis and his doctoral thesis, R.H. Sianipar combines SR-FHN (Stochastic Resonance Fitzhugh-Nagumo) filter strength with cryptosystem ECC (elliptic curve cryptography) 4096-bit both to suppress noise in digital images and digital video and maintain its authenticity. The results of this study have been documented in international scientific journals and officially patented in Japan. One of the patents was published in Japan with a registration number 2008-009549.

Aside from being an active writer teaching in the Electrical Engineering University of Mataram, he is also active in collaborating with several universities and research institutions in Japan, particularly in the fields of cryptography, cryptanalysis and audio / image / video digital forensics. R.H. Sianipar also has experience in conducting code-breaking methods (cryptanalysis) on a number of intelligence data that are the object of research studies in Japan. R.H. Sianipar has a number of Japanese patents, and has written a number of national / international scientific articles, and dozens of national books. R.H. Sianipar has also participated in a number of workshops related to cryptography, cryptanalysis, digital watermarking, and digital forensics. In a number of workshops, R.H. Sianipar helps Prof. Hidetoshi Miike to create applications related to digital image / video processing, steganography, cryptography, watermarking, non-linear screening, intelligent descriptor-based computer vision, and others, which are used as training materials. Field of interest in the study of R.H. Sianipar is multimedia security, signal processing / digital image / video, cryptography, digital communication, digital forensics, and data compression / coding. Until now, R.H. Sianipar continues to develop applications related to analysis of signal, image, and digital video, both for research purposes and for commercial purposes based on the Python programming language, MATLAB, C ++, C, VB.NET, C # .NET, R, and Java.

ABOUT THE BOOK

In chapter one, you will learn to know the properties and events of each control in a Windows Visual C# application. You need to learn and know in order to be more familiar when applying them to some applications in this book.

In chapter two, you will build a project so that children can practice basic skills in addition, subtraction, multiplication, and division operations. This Math Game project can be used to choose the types of questions and what factors you want to use. This project has three timing options. Random math problems using values ​​from 0 to 9 will be presented. Timing options are provided to measure accuracy and speed. There are many controls used. Two label controls are used for title information, two for displaying scores. There is a wide label in the middle of the form to display math questions. And, long skinny label is used as separator. Two button controls are used to start and stop question and one button to exit the project. There are three group control boxes. The first group box holds four check box controls that are used to select the type of questions. The second group box holds eleven radio buttons that are used to select values ​​that are used as factors in calculations. The third group box contains three radio button controls for timing options. A scroll bar control rod is used to change the time.

In chapter three, you will build Bank Code game. The storage box is locked and can only be opened if you enter the correct digit combination. Combinations can be 2 to 4 non-repetitive digits (range of digits from 1 to 9). After a guess is given, you will be notified of how many digits are right and how many digits are in the right position. Based on this information, you will give another guess. You continue to guess until you get the right combination or until you stop the game. On the left side of the form is a large picture box control. On the right side, two group box controls and two button controls are placed. In the picture box, a control panel is placed. In the panel, there are four label controls (set the AutoSize property to False ) and nine button controls. In the first group box control, place three radio buttons. In the second group box control, a text box control is placed. The picture box contains an image of bank and a panel. The label controls in the panel are used to display the combinations entered (the BorderStyle property set to FixedSingle to display the label size). The nine buttons on the panel are used to enter combinations. Radio buttons are used to set options. The buttons (one to start and stop the game and another to exit the project) are used to control game operations. The text box displays the results of the combinations entered.

In chapter four, you will build Horse Racing game. This is a simple game. Up to 10 horses will race to the finish line. You guessed two horses that you thought could win the race. By clicking on the Start button, the race will start. All horses will race speed to get to the finish line. Labels are used to display instructions and number of horses in a race. Four button controls are used: two buttons to change number of horses, one button to start the game, and one other button to stop the game. The picture box control is used to load the horse image. A timer control is used to update the horse's movement during the race.

In chapter five, you will build Catching Ball game. The bird flew and dropped ball from the sky. Users are challenged to position man under the fallen ball to catch it. Labels are used for instructions and to display game information (remaining time, number of balls captured, and game difficulty level). Two buttons are used to change the game difficulty level, one button to start the game, and another button to stop the game. Picture box controls hold images for man, bird, and ball.

In chapter six, you will build Smart Tic Tac Toe game. That said, this is the first game ever programmed on a computer and one that had been programmed by Bill Gates himself when he was a teenager while attending Lakeside School in Seattle. The aim of this game is to win the game on a 3 x 3 grid with the victory of three identical symbols (X or O) on horizontal, diagonal, or vertical lines. The players will play alternately. In this game given two game options: player 1 against player 2 or human player against computer. A smart but simple strategy will be developed for computer logic to be a formidable opponent for humans.

In chapter seven, you will build Fighting Plane program. This program can be played by two human players or human player versus computer. The controls of the player are done via the keyboard. Player 1 presses A key to move up, Z key to move down, and S key to throw rudal. When you choose Two players from the Options button, this game can be played by two human players. Player 1 presses the same keys, while player 2 presses key K to move up, M to move down, and key J to throw rudal. All label controls are used for titles and provide scoring and game information. The large panel (Panel1) is the playing field. Three button controls are used to start / stop a program, set options, and exit the program. One timer control is used to control game animation and another is used to represent the computer's decision process. The second control panel (Panel2) is used to select game options. One group box contains radio buttons which are used to select number of players. A group box contains radio buttons to select the level of difficulty of the game, when playing against a computer. A small button is used to close the options panel. The default properties are set for one-player games with the easiest game difficulty.

CONTENT

Tutorial 1: Visual C SHARP Controls ....... . ........................6

Tutorial 2: Math Game ............... . .............................17

Tutorial 3: Bank Code  .......... . .................................57

Tutorial 4: Horse Racing  .......... . ..............................89

Tutorial 5: Catching Ball  .......... . ............................108

Tutorial 6: Smart Tic Tac Toe  .......... . ........................138

Tutorial 7: Fighting Plane  .......... . ...........................177

TUTORIAL 1

VISUAL C# CONTROLS

In this chapter, you will learn to know the properties and events of each control in a Windows Visual C# application. You need to learn and know in order to be more familiar when applying them to some applications in this book.

| Form |

Forms are objects where the user interface is designed. The form is also known as a container or loader object, because it contains other controls. A number of controls are placed on the form having BackColor , ForeColor , and Font properties. To change it, you can select the desired control (after it is placed in the form) and change the desired properties. Another feature of this container control is that when Enable property is False , all controls on that form will be deactivated. Likewise, when this container control has a Visible property of False , then all controls on the form become invisible.

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

| Button |

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

| Label |

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

| Timer |

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

| TextBox |

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

| CheckBox |

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

| RadioButton |

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

| GroupBox |

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

| PictureBox |

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

TUTORIAL 2

MATH GAME

In this tutorial, you will build a project so that children can practice basic skills in addition, subtraction, multiplication, and division operations. This Math Game project can be used to choose the types of questions and what factors you want to use. This project has three timing options.

Random math problems using values ​​from 0 to 9 will be presented. Timing options are provided to measure accuracy and speed.

| Description |
| There are many controls used. Two label controls are used for title information, two for displaying scores. There is a wide label in the middle of the form to display math questions. And, long skinny label is used as separator. Two button controls are used to start and stop question and one button to exit the project. There are three group control boxes.![D:\2___VB For Students\Image2.png](Image00002.jpg)Figure 2.1 Controls used in Math Game projectThe first group box holds four check box controls that are used to select the type of questions. The second group box holds eleven radio buttons that are used to select values ​​that are used as factors in calculations. The third group box contains three radio button controls for timing options. A scroll bar control rod is used to change the time.Run the project (press <F5>). This math game program will be displayed as follows:![](Image00003.jpg)Figure 2.2 Math Game when first runsMany options are available. First, select the type of question from Type of Question group box. Select addition, subtraction, multiplication, and/or division questions. You can also choose Factor , any value from 0 to 9, or choose Random for random factor. These options can be changed at any time. To start game, click on Start Training button as shown in Figure 2.3. |
| Tutorial Steps |
| Step 1 | You will start building this math game project. Start a new project in Visual Basic. Place six label controls (for four of them, set the AutoSize property to False ), three group box controls, and two button controls on your form. Add timer control to the project. In the first group box, place four check box controls. In the second group box, place eleven radio button controls. In the third group box, place three radio buttons, a label (with AutoSize property set to False ), and a vertical scroll bar. Change the size and position of each control so that the form looks as shown in Figure 2.4.![](Image00004.jpg)Figure 2.3 Math Game when user clicks Start Training button![](Image00005.jpg)Figure 2.4 Controls placed on the formThe first four label controls are used to store information. Wide label is used to display math questions that are asked. Wide and thin label used as separator. The first group box is used to select the type of questions, the second group box is used to choose a factor, and the third group box is used to select the timer option. One button to start and stop question and another button to exit the project. The timer control is used to tell the time spent. |
| Step 2 | Set control properties using the Properties window: 

&#124; A number of properties of the Form1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; FormMathGame &#124;
&#124; BackColor &#124; LightYellow &#124;
&#124; KeyPreview &#124; True &#124;
&#124; Text &#124; Math Game &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Text &#124; Tested: &#124;
&#124; Font Size &#124; 16 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label2 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblTested &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; BackColor &#124; Red &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Font Size &#124; 16 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label3 object &#124;
&#124; Property &#124; Value &#124;
&#124; Text &#124; Correct: &#124;
&#124; Font Size &#124; 16 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label4 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblCorrect &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; BackColor &#124; Red &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Font Size &#124; 16 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label5 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblQuestion &#124;
&#124; Text &#124; [Kosong] &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124; AutoSize &#124; False &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Font Name &#124; Comic Sans MS &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label6 object &#124;
&#124; Property &#124; Value &#124;
&#124; Text &#124; [Empty] &#124;
&#124; BackColor &#124; Red &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; grpType &#124;
&#124; Text &#124; Type of Question &#124;
&#124; BackColor &#124; LightBlue &#124;
&#124; ForeColor &#124; DarkBlue &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Font Style &#124; Bold &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the CheckBox1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; chkAdd &#124;
&#124; Text &#124; Addition (+) &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the CheckBox2 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; chkSubs &#124;
&#124; Text &#124; Substraction (-) &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the CheckBox3 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; chkMul &#124;
&#124; Text &#124; Multiplication (*) &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the CheckBox4 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; chkDiv &#124;
&#124; Text &#124; Division (/) &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox2 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; grpFactor &#124;
&#124; Text &#124; Factor &#124;
&#124; BackColor &#124; LightBlue &#124;
&#124; ForeColor &#124; DarkBlue &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Font Style &#124; Bold &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactorRandom &#124;
&#124; Text &#124; Random &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton2 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor0 &#124;
&#124; Text &#124; 0 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton3 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor1 &#124;
&#124; Text &#124; 1 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton4 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor2 &#124;
&#124; Text &#124; 2 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton5 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor3 &#124;
&#124; Text &#124; 3 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton6 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor4 &#124;
&#124; Text &#124; 4 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton7 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor5 &#124;
&#124; Text &#124; 5 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton8 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor6 &#124;
&#124; Text &#124; 6 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton9 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor7 &#124;
&#124; Text &#124; 7 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton10 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor8 &#124;
&#124; Text &#124; 8 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton11 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFactor9 &#124;
&#124; Text &#124; 9 &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox3 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; grpTimer &#124;
&#124; Text &#124; Timer &#124;
&#124; BackColor &#124; LightBlue &#124;
&#124; ForeColor &#124; DarkBlue &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Font Style &#124; Bold &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton12 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoTimerOff &#124;
&#124; Text &#124; Off &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton13 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoTimerForward &#124;
&#124; Text &#124; Forward Count &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton14 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoTimerBackward &#124;
&#124; Text &#124; Backward Count &#124;
&#124; ForeColor &#124; Black &#124;
&#124; Checked &#124; True &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label7 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblTimer &#124;
&#124; AutoSize &#124; False &#124;
&#124; Text &#124; 0:00 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124; BackColor &#124; White &#124;
&#124; ForeColor &#124; Red &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Font Size &#124; 14 &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the VScrollBar1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; vsbTimer &#124;
&#124; Value &#124; 1 &#124;
&#124; Minimum &#124; 1 &#124;
&#124; Maximum &#124; 60 &#124;
&#124; SmallChange &#124; 1 &#124;
&#124; LargeChange &#124; 1 &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnStart &#124;
&#124; Text &#124; Start Training &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button2 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnExit &#124;
&#124; Text &#124; Exit &#124;
&#124; Font Size &#124; 10 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Timer1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; timerQuestion &#124;
&#124; Interval &#124; 1000 &#124;
&#124;  &#124;  &#124;

When setting all the properties is done, your form will look like the following:![](Image00006.jpg)Figure 2.5 Form When setting all the properties is doneYou will start writing code for the application. You will do it in a few steps. As an initial step, you will write code to generate a random problem or question, read the answer from user, and update the score. |
| Step 3 | For now, you will ignore the timer option. After this initial code works satisfactorily, the timing issue will be discussed. A step-by-step approach to building a project is always easier than building it all at once.Here is what happens when Start Training ( btnStart ) button is clicked: 
*   Set Text property of btnStart to Stop Training .
*   Disable Exit button.
*   Set how many questions to be tested and set how many correct answer to zero.
*   Generate and display a question on lblQuestion .
*   Get answers from user.
*   Check answer and update score.

After each question is answered, the next question will be generated and answered. The user answers the question until he clicks Stop Training (or until the time runs out). The following steps need to be carried out:

*   Set Text property of btnStart to Start Training .
*   Enable Exit button.
*   Clear lblQuestion .
*   Present the result.

First, create a Random object and declare two form-level variables to track how many questions that have been answered and how many answers are correct:

&#124; 12 &#124; Random MyRandom = new Random();int Answered, Correct; &#124;

 |
| Step 4 | Write code for Click event of btnStart to implement the steps above, except to present the result: 

&#124; 12345678910111213141516171819 &#124; private void btnStart_Click( object sender, EventArgs e){    if (btnStart.Text == "Start Training" )    {       btnStart.Text = "Stop Training" ;        btnExit.Enabled = false ;        Answered = 0;        Correct = 0;        lblTested.Text = "0" ;        lblCorrect.Text = "0" ;        blQuestion.Text = GetQuestion();    }    else    {        btnStart.Text = "Start Training" ;        btnExit.Enabled = true ;        lblQuestion.Text = "" ;    }} &#124;

 |
| Step 5 | The code in Step 4 uses GetQuestion function to generate random questions and generate them as a String type. Add this (you complete it later): 

&#124; 1234 &#124; private string GetQuestion(){    return ( "Question!" )} &#124;

 |
| Step 6 | And, now, you can write the code for Click event of btnExit : 

&#124; 1234 &#124; private void btnExit_Click( object sender, EventArgs e){    this .Close();} &#124;

 |
| Step 7 | Save, run the project, and click Start Training button. The form will now be displayed as shown in Figure 2.6:![](Image00007.jpg)Figure 2.6 The Math Game after user clicks Start Training button, |
| Step 8 | You will continue to write the code for generating questions and getting answers (including score) from the user. Then, later you will also learn timer and how to present results.To generate a question, you need to check the latest options selected by user and generate a random question based on those choices. All code will be placed in the function GetQuestion .Look at each step of the question generation process. The first step is to choose a type of random question for a maximum of four possibilities. You will use a simple approach, first generating a random value from 1 to 4 (1 represents addition, 2 for subtraction, 3 for multiplication, and 4 represents division). If the check box (in the Type of Question group box) with the random number is checked, then it will be a type of question. If the check box with the random number is not checked, then you will choose another random value. You continue this process until the type of question is selected. Note this approach assumes that at least one check box is always in the checked position.The code to choose the type of question is as follows: 

&#124; 12345678910111213141516171819202122232425 &#124; int PType, P;P = 0;do{    PType = MyRandom.Next(4) + 1;    if (PType == 1 && chkAdd.Checked)    {        // Addition        P = PType;    }    else if (PType == 2 && chkSubs.Checked)    {        // Substraction        P = PType;    else if (PType == 3 && chkMul.Checked)    {        // Multiplication        P = PType;    else if (PType == 4 && chkDiv.Checked)    {        // Division        P = PType;    }} while (P == 0); &#124;

After the type of question is selected, you determine the factor used to generate a question. This factor can be a value from 0 to 9, or a random value from 0 to 9, based on the radio button selected in Factor group box.The GetFactor function provides a factor based on radio button selection in the Factor group box and type of question, P . For random factor, this function ensures that zero is not used as a return value if a division problem is being generated.Write the definition of GetFactor function:

&#124; 12345678910111213141516171819202122232425262728293031 &#124; private int GetFactor( int p){    if (rdoFactor0.Checked)        return (0);    else if (rdoFactor1.Checked)        return (1);    else if (rdoFactor2.Checked)        return (2);    else if (rdoFactor3.Checked)        return (3);    else if (rdoFactor4.Checked)        return (4);    else if (rdoFactor5.Checked)        return (5);    else if (rdoFactor6.Checked)        return (6);    else if (rdoFactor7.Checked)        return (7);    else if (rdoFactor8.Checked)        return (8);    else if (rdoFactor9.Checked)        return (9);    else    {        // Random        if (p == 4)            return (MyRandom.Next(9) + 1);        else            return (MyRandom.Next(10));    }} &#124;

If a random option ( rdoFactorRandom ) is selected, 0 to 9 is generated for addition, subtraction, and multiplication problems; 1 to 9 are generated for the division problem (p = 4). In other cases, the selected factor is used as a return value. |
| Step 9 | Now it is time for you to start writing the definition of the GetQuestion function. First, add declaration for the following three form-level variables: 

&#124; 12 &#124; int CorrectAnswer, Digits;string Question; &#124;

Then, write the definition of GetQuestion function:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364 &#124; private string GetQuestion(){    int PType, P, RandValue, Factor;    P = 0;    do    {        PType = MyRandom.Next(4) + 1;        if (PType == 1 && chkAdd.Checked)        {            // Addition            P = PType;            RandValue = MyRandom.Next(10);            Factor = GetFactor(1);            CorrectAnswer = RandValue + Factor;            Question = RandValue.ToString() + " + " +                Factor.ToString() + " = " ;        }        else if (PType == 2 && chkSubs.Checked)        {            // Substraction            P = PType;            Factor = GetFactor(2);            CorrectAnswer = MyRandom.Next(10);            RandValue = CorrectAnswer + Factor;            Question = RandValue.ToString() + " - " +                Factor.ToString() + " = " ;        }        else if (PType == 3 && chkMul.Checked)        {            // Multiplication            P = PType;            RandValue = MyRandom.Next(10);            Factor = GetFactor(3);            CorrectAnswer = RandValue * Factor;            Question = RandValue.ToString() + " x " +                Factor.ToString() + " = " ;        }        else if (PType == 4 && chkDiv.Checked)        {            // Division            P = PType;            Factor = GetFactor(4);            CorrectAnswer = MyRandom.Next(10);            RandValue = CorrectAnswer * Factor;            Question = RandValue.ToString() + " / " +                Factor.ToString() + " = " ;        }    } while (P == 0);    if (CorrectAnswer < 10)    {        Digits = 1;        return (Question + "?" );    }    else    {        Digits = 2;        return (Question + "??" );    }} &#124;

 |
| Step 10 | Add the code to the project. Save and run the project. Click Start Training and you will see a random addition problem:![](Image00008.jpg)![](Image00009.jpg)Figure 2.7 Addition question given when Math Game first runsTwo question marks tell the user that there are two digits to the correct answer. You will see how to get the right answer. At this point, what you can do is click Stop Training . You can then click Start Training to see other addition problems. |
| Step 11 | After a question is displayed, user can enter the digits as the answer. The digits will be entered using the keyboard. Key presses are handled by the KeyPress event of the form. When the form has focus, any key pressed will be interpreted and used.In form designing, you have set the KeyPreview property of the form to True . This is needed so that all key presses are processed by the KeyPress event, before they are used by other controls. You will also make sure the form has focus when it needs it.The steps for reading and checking answer are as follows: 
*   Make sure the pressed key is a value between 0 to 9.
*   If the correct value is entered, then the value will be used as part of the answer to replace the question mark on the question.
*   If the question mark is still left, another key press will be awaited.
*   If all question marks have been replaced, the answer will be compared with the correct answer.
*   Increment the number of the questions that have been tested.
*   If the answer is correct, the number of questions that have been answered correctly will be incremented.
*   Update score label controls.
*   Generate another question.

You need to declare two form-level variables to load user’s answer and the current number of digits of the answer:

&#124; 12 &#124; string YourAnswer;int NumberDigitsAnswer; &#124;

Write the Keypress event of the form which implements the steps above:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839 &#124; private void FormMathGame_KeyPress( object sender, KeyPressEventArgs e){    if (btnStart.Text == "Start Training" )        return ;    // Only allows 0-9 keys    if (e.KeyChar >= '0' && e.KeyChar <= '9' ) {        e.Handled = false ;        YourAnswer += e.KeyChar;        lblQuestion.Text = Question + YourAnswer;        if (NumberDigitsAnswer != Digits)        {            NumberDigitsAnswer++;            lblQuestion.Text += "?" ;            return ;        }        else        {            Answered++;            // Checks answer            if (Convert.ToInt32(YourAnswer) == CorrectAnswer) {                Correct++;            }            lblTested.Text = Answered.ToString();            lblTested.Refresh();            lblCorrect.Text = Correct.ToString();            lblCorrect.Refresh();            lblQuestion.Text = GetQuestion();            lblQuestion.Refresh();        }    }    else    {        e.Handled = true ;    }} &#124;

 |
| Step 12 | You need to add a few lines of code to the GetQuestion function to initialize YourAnswers and NumberDigitsAnswer , in each new question, and also to give focus on the form, so that answer can be typed: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768 &#124; private string GetQuestion(){    int PType, P, RandValue, Factor;    P = 0;    do    {        PType = MyRandom.Next(4) + 1;        if (PType == 1 && chkAdd.Checked)        {            // Addition            P = PType;            RandValue = MyRandom.Next(10);            Factor = GetFactor(1);            CorrectAnswer = RandValue + Factor;            Question = RandValue.ToString() + " + " +                Factor.ToString() + " = " ;        }        else if (PType == 2 && chkSubs.Checked)        {            // Substraction            P = PType;            Factor = GetFactor(2);            CorrectAnswer = MyRandom.Next(10);            RandValue = CorrectAnswer + Factor;            Question = RandValue.ToString() + " - " +                Factor.ToString() + " = " ;        }        else if (PType == 3 && chkMul.Checked)        {            // Multiplication            P = PType;            RandValue = MyRandom.Next(10);            Factor = GetFactor(3);            CorrectAnswer = RandValue * Factor;            Question = RandValue.ToString() + " x " +                Factor.ToString() + " = " ;        }        else if (PType == 4 && chkDiv.Checked)        {            // Division            P = PType;            Factor = GetFactor(4);            CorrectAnswer = MyRandom.Next(10);            RandValue = CorrectAnswer * Factor;            Question = RandValue.ToString() + " / " +                Factor.ToString() + " = " ;        }    } while (P == 0);    YourAnswer = "" ;    NumberDigitsAnswer = 1;    this .Focus();    if (CorrectAnswer < 10)    {        Digits = 1;        return (Question + "?" );    }    else    {        Digits = 2;        return (Question + "??" );    }} &#124;

Save and run the project. You can now type an answer. You can stop whenever you want by clicking the Stop Training button.![](Image00010.jpg)![](Image00011.jpg)Figure 2.8 Correct answer now can be verified |
| Step 13 | Choosing question types seems quite simple. You only need to check one or a number of check boxes that you want and the questions will be raised. But there are a number of problems here. Until now, nothing prevented the user from unchecking all check boxes, so that no type of question was selected. You must ensure that at least one check box is always selected. And, if the question of division is selected, you cannot allow zero as a factor. You can now write the code to overcome these two problems.You can use a technique where one method can handle multiple events to process checking for check boxes in the Type of Question group box. You will create a method named chkType_CheckedChanged that will handle CheckedChanged event for four check boxes: chkAdd , chkSubs , chkMul , and chkDiv .In this method, the following steps are involved: 
*   Determine which check box i checked.
*   Determine how many check boxes are checked.
*   If chkDiv is checked, you need to ensure that zero is not selected as a factor; if 0 is selected by the user as a factor, you need to change that factor to 1\. Also, if chDiv is checked, you need to disable rdoFactor0 .
*   If no check box is checked, you need to check the check box that was last selected.
*   Establish focus on the form.

Write the chkType_CheckedChanged method which implements these steps:

&#124; 123456789101112131415161718192021222324252627282930313233343536 &#124; private void chkType_CheckedChanged( object sender, EventArgs e){    CheckBox CheckClicked;              int NumberCheck;    // Determines which checkbox is selected    CheckClicked = (CheckBox)sender;    // Determines how many check boxes are checked    NumberCheck = 0;    if (chkAdd.Checked)        NumberCheck++;    if (chkSubs.Checked)        NumberCheck++;    if (chkMul.Checked)        NumberCheck++;    if (chkDiv.Checked)    {        NumberCheck++;        // Ensures that zero is not selected as a factor        if (rdoFactor0.Checked)            rdoFactor1.PerformClick();        rdoFactor0.Enabled = false ;    }    else    {        rdoFactor0.Enabled = true ;    }    //If no check box is checked,    //you need to check the check box that was last selected    if (NumberCheck == 0)        CheckClicked.Checked = true ;    this .Focus();} &#124;

 |
| Step 14 | Save and run the project. Make sure all the newly written code does its job. Try to uncheck all question type check boxes. One check box will still be checked. Check the division question and notice that option 0 for the factor is disabled. Choose 0 as a factor. Now, check again the type of division question. Notice the factor is changed to 1 and option 0 is disabled. You have now solved the problem type problem with any factor.![](Image00012.jpg)Figure 2.9 Option 0 for the factor is disabled when user choose division question |
| Step 15 | After writing down the code for generating questions and checking answers, you will now solve the problem of using timer in this math game project. Until now, you assumed no timer is used. You have two choices for a timer: (1) when the timer is counting forward, which tracks how long you are solving the problem, and (2) when the timer is counting down from a specified value. In both cases, a control ( lblTimer ) will display the time in minute: second format. In the second case, a vertical scroll bar ( vsbTimer ) will be used to set the value. Timing will be controlled by a timer control at intervals of 1 second (1000 milliseconds).You will use a form-level variable ( QuestionTime ) to store the time value (whether the count is forward or backward) in seconds. Add this variable to the general declaration area: 

&#124; 1 &#124; int QuestionTime; &#124;

 |
| Step 16 | Then, you need to write the code to switch from one timing option to another. You will use a method to handle the CheckedChanged event for all three radio buttons in the grpTimer group box. The steps involved are as follows: 
*   If rdoTimerOff is selected, lblTimer and vsbTimer will be disabled.
*   If the forward counting ( rdoTimerForward ) is selected, lblTimer will be displayed and vsbTimer will be disabled. The QuestionTime variable is initialized with 0.
*   If the countdown ( rdoTimerBackward ) is selected, lblTimer and vsbTimer will be displayed. The QuestionTime variable is initialized with 30 times the Value property of vsbTimer (30 seconds for each increment).

Write the rdoTimer_CheckedChanged method which implements these steps:

&#124; 12345678910111213141516171819202122 &#124; private void rdoTimer_CheckedChanged( object sender, EventArgs e){    if (rdoTimerOff.Checked)    {        lblTimer.Visible = false ;        vsbTimer.Visible = false ;    }    else if (rdoTimerForward.Checked)    {        QuestionTime = 0;        lblTimer.Text = GetWaktu(QuestionTime);        lblTimer.Visible = true ;        vsbTimer.Visible = false ;    }    else if (rdoTimerBackward.Checked)    {        QuestionTime = 30 * vsbTimer.Value;        lblTimer.Text = GetWaktu(QuestionTime);        lblTimer.Visible = true ;        vsbTimer.Visible = true ;    }} &#124;

 |
| Step 17 | The rdoTimer_CheckedChanged event above uses a public GetTime function that generates formatted time. Write GetTime function definition: 

&#124; 12345678910111213 &#124; private string GetTime( int s){    int min, det;    string ms, ss;    min = ( int )(s / 60);    det = s - 60 * min;    ms = min.ToString();    ss = det.ToString();    if (det < 10)        ss = "0" + ss;    return (ms + ":" + ss);} &#124;

This function takes the time ( s ) in seconds and breaks it down into minutes and seconds. Add this new code to your project. |
| Step 18 | When rdoTimerBackward is checked, then the Value property of the scroll bar ( vsbTimer ) is used to initialize QuestionTime variable. In the code, each increment on the scroll bar will add 30 seconds to the timer. If you look back at how you set the control properties, you will see the Maximum property for this scroll bar is 60\. This will allow a maximum of 30 minutes (1800 seconds) so that the game session is finished. You need the Scroll event of vsbTimer to change the displayed time whenever the arrow keys of the scrollbar are clicked.Write this method: 

&#124; 12345 &#124; private void vsbTimer_Scroll( object sender, ScrollEventArgs e){   lblTimer.Text = GetTime(30 * vsbTimer.Value);   lblTimer.Refresh();} &#124;

 |
| Step 19 | You allow changing the type of questions and factors when the user plays the math game. It would not make sense to change the timer options when the user is working on the question. Timing is not right. You will only allow the selection of time options before clicking Start Training . Clicking Start Training will start the timing process (which is controlled by timerQuestion ). The steps involved are as follows: 
*   Disable grpTimer .
*   If rdoTimerOff is selected, do nothing.
*   If rdoTimerForward is selected, QuestionTime is initialized to 0 and then displayed. Then timerQuestion control is enabled.
*   If rdoTimerBackward is selected, QuestionTime is initialized with 30 times the Value property of vsbTimer and then displayed. Then the timerQuestion control is enabled.

Clicking Stop Training will stop the timing process. The steps involved are as follows:

*   Enable grpTimer .
*   Disable timerQuestion .

Each of these steps is handled by the modified btnStart_Click event as follows:

&#124; 12345678910111213141516171819202122232425262728293031323334 &#124; private void btnStart_Click( object sender, EventArgs e){    if (btnStart.Text == "Start Training" )    {       btnStart.Text = "Stop Training" ;        btnExit.Enabled = false ;        Answered = 0;        Correct = 0;        lblTested.Text = "0" ;        lblCorrect.Text = "0" ;        grpTimer.Enabled = false ;        if (!rdoTimerOff.Checked)       {            if (rdoTimerForward.Checked)               QuestionTime = 0;           else                QuestionTime = 30 * vsbTimer.Value;           lblTimer.Text = GetTime(QuestionTime);           timerQuestion.Enabled = true ;       }        blQuestion.Text = GetQuestion();    }    else    {        grpTimer.Enabled = true ;       timerQuestion.Enabled = false ;        btnStart.Text = "Start Training" ;        btnExit.Enabled = true ;        lblQuestion.Text = "" ;    }} &#124;

 |
| Step 20 | When the timer ( timerQuestion ) is enabled, the displayed time ( lblTimer ) will be updated every second using the Interval property with a value of 1000\. The displayed time will be incremented if forward count is selected, decremented if backward count is selected.The steps involved in forward counting are as follows: 
*   Increment QuestionTime by 1.
*   Display QuestionTime .
*   If QuestionTime is 1800 (30 minutes), question solving is stopped.

The steps involved in backward counting are as follows:

*   Decrement QuestionTime by 1.
*   Display QuestionTime .
*   If QuestionTime is 0, question solving is stopped.

Write the code to implement the steps above which is placed into Tick event of timerQuestion control:

&#124; 1234567891011121314151617181920212223242526 &#124; private void timerQuestion_Tick( object sender, EventArgs e){   if (rdoTimerForward.Checked)    {        QuestionTime++;        lblTimer.Text = GetTime(QuestionTime);        if (QuestionTime >= 1800)        {            btnStart.PerformClick();            return ;       }    }   else    {        QuestionTime--;        lblTimer.Text = GetTime(QuestionTime);        if (QuestionTime == 0)        {            btnStart.PerformClick();            return ;        }   }   lblTimer.Refresh();} &#124;

![](Image00013.jpg)Figure 2.10 Option Forward Count appliedAdd the code to your project. You have finished implementing the modification to the timing. Save and run the project. You need to make sure all timer options are running well. First, check whether the project can run without timer.Once you are sure that the without timer option is working properly, stop training and select forward count option. Run the project. Ensure that the timer is correctly incremented, as shown in Figure 2.10.Click Stop Training at a certain time. Select Backward Count option. Change the time using the scroll bar. Make sure it reaches a maximum value of 30:00 (and a minimum value of 0:30). Then, click Start Training . Ensure that the time is decremented appropriately:![](Image00014.jpg)Figure 2.11 Option Backward Count applied |
| Step 21 | After the user stops solving problems, you want him to know how good he is at answering questions. This information includes: 
*   The number of questions have been tried.
*   The number of answers are answered correctly.
*   The percentage score.
*   If the timer is activated, the time spent on each problem.

If the forward count option is selected, the time spent is equal to QuestionTime . If the backward count option is selected, the time spent equal to the initial time which is reduced by QuestionTime .All of this information is available on a number of variables in the program code. The results are presented in the Click event method of the btnS QuestionTime tart control. You only need to use a simple message box to display the results:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869 &#124; private void btnStart_Click( object sender, EventArgs e){    int Score;    string Message = "" ;    if (btnStart.Text == "Start Training" )    {        btnStart.Text = "Stop Training" ;        btnExit.Enabled = false ;        Answered = 0;        Correct = 0;        lblTested.Text = "0" ;        lblCorrect.Text = "0" ;        grpTimer.Enabled = false ;        if (!rdoTimerOff.Checked)        {            if (rdoTimerForward.Checked)                QuestionTime = 0;            else                QuestionTime = 30 * vsbTimer.Value;            lblTimer.Text = GetTime(QuestionTime);            timerQuestion.Enabled = true ;        }        blQuestion.Text = GetQuestion();    }    else    {        grpTimer.Enabled = true ;        timerQuestion.Enabled = false ;        btnStart.Text = "Start Training" ;        btnExit.Enabled = true ;        lblQuestion.Text = "" ;       if (Answered > 0)        {            Score = ( int )(100 * ( double ) (Correct) / Answered);            Message = "The number of questions tried: " +                Answered.ToString() + "\r\n" ;            Message += " The number of questions correctly answered: " +                Correct.ToString() + " (" + Score.ToString() + "%)"                + "\r\n" ;            if (rdoTimerOff.Checked)            {                Message += "Timer Off" ;            }            else            {                if (rdoTimerBackward.Checked)                {                    QuestionTime =                        30 * vsbTimer.Value - QuestionTime;                }                Message += "Total time spent: " +                    GetTime(QuestionTime) + "\r\n" ;                Message += "Average time every question: " +                    String.Format( "{0:f2}" ,                    ( double )(QuestionTime) / Answered) + " seconds" ;            }            MessageBox.Show(Message, "Results" ,                MessageBoxButtons.OK, MessageBoxIcon.Information);        }    }} &#124;

 |
| Step 22 | Save and run project. Answer a number of questions and see the results. Make sure the results are displayed correctly whether the timing is active or not:![](Image00015.jpg)![](Image00016.jpg)Figure 2.12 Displaying results |
|  |  |

| Form1.cs |
| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197198199200201202203204205206207208209210211212213214215216217218219220221222223224225226227228229230231232233234235236237238239240242243244245246247248249250251252253254255256257258259260261262263264265266267269270271272273274275276277278279280281282283284285286287288289290291292293294295296297298299300301302303304305306307308309310311312313314315316317318319320321322323324325326327328329330331332333334335336337338339340341342343344345346347348349350351352353354 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;namespace Game_Matematika_Flash_Card{    public partial class FormMathGame : Form    {        Random MyRandom = new Random();        int Answered, Correct;        int CorrectAnswer, Digits;        string Question;        string YourAnswer;        int NumberDigitsAnswer;        int QuestionTime;        public FormMathGame ()        {            InitializeComponent();        }        private void btnStart_Click( object sender, EventArgs e)        {            int Score;            string Message = "" ;            if (btnStart.Text == "Start Training" )            {                btnStart.Text = "Stop Training" ;                btnExit.Enabled = false ;                Answered = 0;                Correct = 0;                lblTested.Text = "0" ;                lblCorrect.Text = "0" ;                grpTimer.Enabled = false ;                if (!rdoTimerOff.Checked)                {                    if (rdoTimerForward.Checked)                        QuestionTime = 0;                    else                        QuestionTime = 30 * vsbTimer.Value;                    lblTimer.Text = GetTime(QuestionTime);                    timerQuestion.Enabled = true ;                }                lblQuestion.Text = GetQuestion();            }            else            {                grpTimer.Enabled = true ;                timerQuestion.Enabled = false ;                btnStart.Text = "Start Training" ;                btnExit.Enabled = true ;                lblQuestion.Text = "" ;                if (Answered > 0)                {                    Score = ( int )(100 * ( double ) (Correct) / Answered);                    Message = "The number of questions tried: " +                        Answered.ToString() + "\r\n" ;                    Message += "The number of questions correctly answered: "                        + Correct.ToString() + " (" + Score.ToString()                        + "%)" + "\r\n" ;                    if (rdoTimerOff.Checked)                    {                        Message += "Timer Off" ;                    }                    else                    {                        if (rdoTimerBackward.Checked)                        {                            QuestionTime =                                30 * vsbTimer.Value - QuestionTime;                        }                        Message += "Total time spent: " +                            GetTime(QuestionTime) + "\r\n" ;                        Message += "Average time every question: " +                            String.Format( "{0:f2}" ,                            ( double )(QuestionTime) / Answered) +                            " seconds" ;                    }                    MessageBox.Show(Message, "Results" ,                        MessageBoxButtons.OK, MessageBoxIcon.Information);                }            }        }       private void btnExit_Click( object sender, EventArgs e)        {            this .Close();        }        private int GetFactor( int p)        {            if (rdoFactor0.Checked)                return (0);            else if (rdoFactor1.Checked)                return (1);            else if (rdoFactor2.Checked)                return (2);            else if (rdoFactor3.Checked)                return (3);            else if (rdoFactor4.Checked)                return (4);            else if (rdoFactor5.Checked)                return (5);            else if (rdoFactor6.Checked)                return (6);            else if (rdoFactor7.Checked)                return (7);            else if (rdoFactor8.Checked)                return (8);            else if (rdoFactor9.Checked)                return (9);            else            {                // Random                if (p == 4)                    return (MyRandom.Next(9) + 1);                else                    return (MyRandom.Next(10));            }        }        private string GetQuestion()        {            int PType, P, RandValue, Factor;            P = 0;            do            {                PType = MyRandom.Next(4) + 1;                if (PType == 1 && chkAdd.Checked)                {                    // Addition                    P = PType;                    RandValue = MyRandom.Next(10);                    Factor = GetFactor(1);                    CorrectAnswer = RandValue + Factor;                    Question = RandValue.ToString() + " + "                        + Factor.ToString() + " = " ;                }                else if (PType == 2 && chkSubs.Checked)                {                    // Substraction                    P = PType;                    Factor = GetFactor(2);                    CorrectAnswer = MyRandom.Next(10);                    RandValue = CorrectAnswer + Factor;                    Question = RandValue.ToString() + " - " +                        Factor.ToString() + " = " ;                }                else if (PType == 3 && chkMul.Checked)                {                    // Multiplication                    P = PType;                    RandValue = MyRandom.Next(10);                    Factor = GetFactor(3);                    CorrectAnswer = RandValue * Factor;                    Question = RandValue.ToString() + " x " +                        Factor.ToString() + " = " ;                }                else if (PType == 4 && chkDiv.Checked)                {                    // Division                    P = PType;                    Factor = GetFactor(4);                    CorrectAnswer = MyRandom.Next(10);                    RandValue = CorrectAnswer * Factor;                    Question = RandValue.ToString() + " / " +                        Factor.ToString() + " = " ;                }            } while (P == 0);            YourAnswer = "" ;            NumberDigitsAnswer = 1;            this .Focus();            if (CorrectAnswer < 10)            {                Digits = 1;                return (Question + "?" );            }            else            {                Digits = 2;                return (Question + "??" );            }        }        private void FormMathGame_KeyPress( object sender, KeyPressEventArgs e)        {            if (btnStart.Text == "Start Training" )                return ;            // Only allows 0-9 keys            if (e.KeyChar >= '0' && e.KeyChar <= '9' ) {                e.Handled = false ;                YourAnswer += e.KeyChar;                lblQuestion.Text = Question + YourAnswer;                if (NumberDigitsAnswer != Digits)                {                    NumberDigitsAnswer++;                    lblQuestion.Text += "?" ;                    return ;                }                else                {                    Answered++;                    // Checks answer                    if (Convert.ToInt32(YourAnswer) == CorrectAnswer) {                        Correct++;                    }                    lblTested.Text = Answered.ToString();                    lblTested.Refresh();                    lblCorrect.Text = Correct.ToString();                    lblCorrect.Refresh();                    lblQuestion.Text = GetQuestion();                    lblQuestion.Refresh();                }            }            else            {                e.Handled = true ;            }        }        private void chkType_CheckedChanged( object sender, EventArgs e)        {            CheckBox CheckClicked;                      int NumberCheck;            // Determines which checkbox is selected            CheckClicked = (CheckBox)sender;            // Determines how many check boxes are checked            NumberCheck = 0;            if (chkAdd.Checked)                NumberCheck++;            if (chkSubs.Checked)                NumberCheck++;            if (chkMul.Checked)                NumberCheck++;            if (chkDiv.Checked)            {                NumberCheck++;                // Ensures that zero is not selected as a factor                if (rdoFactor0.Checked)                    rdoFactor1.PerformClick();                rdoFactor0.Enabled = false ;            }            else            {                rdoFactor0.Enabled = true ;            }            //If no check box is checked,            //you need to check the check box that was last selected            if (NumberCheck == 0)                CheckClicked.Checked = true ;            this .Focus();        }        private void rdoTimer_CheckedChanged( object sender, EventArgs e)        {            if (rdoTimerOff.Checked)            {                lblTimer.Visible = false ;                vsbTimer.Visible = false ;            }            else if (rdoTimerForward.Checked)            {                QuestionTime = 0;                lblTimer.Text = GetTime(QuestionTime);                lblTimer.Visible = true ;                vsbTimer.Visible = false ;            }            else if (rdoTimerBackward.Checked)            {                QuestionTime = 30 * vsbTimer.Value;                lblTimer.Text = GetTime(QuestionTime);                lblTimer.Visible = true ;                vsbTimer.Visible = true ;            }        }        private string GetTime( int s)        {            int min, det;            string ms, ss;            min = ( int )(s / 60);            det = s - 60 * min;            ms = min.ToString();            ss = det.ToString();            if (det < 10)                ss = "0" + ss;            return (ms + ":" + ss);        }        private void vsbTimer_Scroll( object sender, ScrollEventArgs e)        {            lblTimer.Text = GetTime(30 * vsbTimer.Value);            lblTimer.Refresh();        }        private void timerQuestion_Tick( object sender, EventArgs e)        {            if (rdoTimerForward.Checked)            {                QuestionTime++;                lblTimer.Text = GetTime(QuestionTime);                if (QuestionTime >= 1800)                {                    btnStart.PerformClick();                    return ;                }            }            else            {                QuestionTime--;                lblTimer.Text = GetTime(QuestionTime);                if (QuestionTime == 0)                {                    btnStart.PerformClick();                    return ;                }            }            lblTimer.Refresh();        }    }} |
|  |  |

TUTORIAL 3

BANK CODE

In this tutorial, you will build Bank Code game. The storage box is locked and can only be opened if you enter the correct digit combination. Combinations can be 2 to 4 non-repetitive digits (range of digits from 1 to 9). After a guess is given, you will be notified of how many digits are right and how many digits are in the right position. Based on this information, you will give another guess. You continue to guess until you get the right combination or until you stop the game.

| Description |
| On the left side of the form is a large picture box control. On the right side, two group box controls and two button controls are placed. In the picture box, a control panel is placed. In the panel, there are four label controls (set the AutoSize property to False ) and nine button controls. In the first group box control, place three radio buttons. In the second group box control, a text box control is placed.![](Image00017.jpg)Figure 3.1 All controls used in Bank Code projectThe picture box contains an image of bank and a panel. The label controls in the panel are used to display the combinations entered (the BorderStyle property set to FixedSingle to display the label size). The nine buttons on the panel are used to enter combinations. Radio buttons are used to set options. The buttons (one to start and stop the game and another to exit the project) are used to control game operations. The text box displays the results of the combinations entered.![](Image00018.jpg)Figure 3.2 User chooses 3 Digits Combination and clicks Start Game button![](Image00019.jpg)Figure 3.3 User guesses three digits and the result displayed on text box controlRun the project (press <F5>). The game will be displayed in a "stop" state. You can then choose the combination option 2, 3, or 4 digits. If you choose a 3 digit combination and click Start Game button, it will appear as shown in Figure 3.2Because 3 digits combination option is selected, only three labels are displayed to enter the combination. Now you can select the three digit guesses by pressing the number keys provided. After you select the guess, the results will be displayed in the text box to the right of the form as shown in Figure 3.3. |
| Tutorial Steps |
| Step 1 | You will start building the Bank Code game project. Start a new project in Visual C#. It is recommended that you immediately save it with a name that you choose yourself. This will create the folders and file structure needed for your project. |
| Step 2 | Place a large picture box control on the left side of the form. On the right side, place two group box controls and two button controls. In the picture box, place a control panel. In the panel, place four label controls (set AutoSize property to False in order to be resizable) and nine button controls. In the first group control box, place three radio buttons. In the second group control box, place a text box control. The form now is as shown in Figure 3.4:![](Image00020.jpg)Figure 3.4 All controls used and their positions in the formThe picture box contains an image of bank and a panel. The label controls in the panel are used to display the combinations entered (the BorderStyle property set to FixedSingle to display the label size). The nine buttons on the panel are used to enter combinations. Radio buttons are used to set options. The buttons (one to start and stop the game and another to exit the project) are used to control game operations. The text box displays the results of the combinations entered. |
| Step 3 | Set control properties using the Properties window: 

&#124; A number of properties of the Form1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; FormBankCode &#124;
&#124; Text &#124; Bank Code &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; picBank &#124;
&#124; Image &#124; bank3.png &#124;
&#124; SizeMode &#124; StretchImage &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; pnlBank &#124;
&#124; BackColor &#124; Light Yellow &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblCombol1 &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font &#124; Bold, 18 &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label2 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblCombol2 &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font &#124; Bold, 18 &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label3 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblCombol3 &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font &#124; Bold, 18 &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label4 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; lblCombol4 &#124;
&#124; BackColor &#124; White &#124;
&#124; BorderStyle &#124; FixedSingle &#124;
&#124; Font &#124; Bold, 18 &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btn1 &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; 1 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button2 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btn2 &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; 2 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button3 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btn3 &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; 3 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button4 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btn4 &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; 4 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button5 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btn5 &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; 5 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button6 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btn6 &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; 6 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button7 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btn7 &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; 7 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button8 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btn8 &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; 8 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button9 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btn9 &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; 9 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; grpOption &#124;
&#124; BackColor &#124; LightBlue &#124;
&#124; Text &#124; Options &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoTwoDigits &#124;
&#124; Text &#124; 2 Digits Combination &#124;
&#124; Checked &#124; True &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton2 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoThreeDigits &#124;
&#124; Text &#124; 3 Digits Combination &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton3 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; rdoFourDigits &#124;
&#124; Text &#124; 4 Digits Combination &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button10 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnStartStop &#124;
&#124; Text &#124; Start Game &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button11 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; btnExit &#124;
&#124; Text &#124; Exit Game &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox2 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; grpResult &#124;
&#124; Text &#124; Results &#124;
&#124; BackColor &#124; LightBlue &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the TextBox1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; textResult &#124;
&#124; BackColor &#124; White &#124;
&#124; MultiLine &#124; True &#124;
&#124; ReadOnly &#124; True &#124;
&#124; ScrollBars &#124; Vertical &#124;
&#124;  &#124;  &#124;

 |
| Step 4 | When setting properties is complete, the form now looks as shown in Figure 3.5\. This completes the form design. You will now start writing code for the game. You will write the code in a few steps. As a first step, you will write the code that starts the game and sets the "stop" state. Then, you will determine how to switch the game to "playing" state by clicking Start Game button. During the code development process, you will modify a number of methods before the process endpoint is encountered.![](Image00021.jpg)Figure 3.5 Setting properties is complete and you start writing code for the game |
| Step 5 | Every time the project starts, there are a number of initializations that need to be done. You will see a number of initializations that this game requires. All initialization is placed in the Load event method of the form.To simplify the task, you will create an array to contain the four control labels that are used to display combinations and an array to contain the nine control buttons that are used to enter combination values. These two arrays are defined at the form-level: 

&#124; 12 &#124; Label[] Combo = new Label[4];Button[] ComboButton = new Button[9]; &#124;

 |
| Step 6 | And write assignments placed on the Load event method from the form as follows: 

&#124; 123456789101112131415161718 &#124; private void FormBankCode_Load( object sender, EventArgs e){    // Disables pnlBank and creates two arrays    pnlBank.Enabled = false ;    Combo[0] = lblCombol1;    Combo[1] = lblCombol2;    Combo[2] = lblCombol3;    Combo[3] = lblCombol4;    ComboButton[0] = btn1;    ComboButton[1] = btn2;    ComboButton[2] = btn3;    ComboButton[3] = btn4;    ComboButton[4] = btn5;    ComboButton[5] = btn6;    ComboButton[6] = btn7;    ComboButton[7] = btn8;    ComboButton[8] = btn9;} &#124;

The utility of these two arrays will become more apparent when the code is further developed. Although this code is still very minimal, you can run the project to ensure that the form is initialized correctly. Do this and you will see a "stop" state of the game (using the default properties). |
| Step 7 | You have two choices at this point: choose an option and click btnStartStop button (button that says Start Game ) or click the btnExit button (button that says Exit ).The code to exit the project is quite simple. Place the following code in the Click event method of btnExit control: 

&#124; 1234 &#124; private void btnExit_Click( object sender, EventArgs e){    this .Close();} &#124;

It only says that whenever Exit button is clicked, the project will close. |
| Step 8 | The code for btnStartStop button is much more complex. You will build it in several stages. First, you will see how to switch the game from the "stop" to the "play" state.When the user clicks Start Game button in the "stop" state, several things happen to switch the game to the "play" state: 
*   Change the Text property from btnStartStop to Stop Game .
*   Disable grpOptions (does not allow selection of options when playing).
*   Disable Exit button.
*   Enable pnlBank in order that a combination can be entered.
*   Clear textResult (delete the previous contents).
*   Display label controls to indicate a combination.
*   Determine the secret combination.
*   Check whether the input matches a secret combination.
*   Display the results.

Now, you will implement each of these steps except setting a secret combination and checking user input. The steps will be implemented separately.Add this line of code to the form-level declaration to define a variable for number of digits in combination:

&#124; 1 &#124; int NumberOfDigit; &#124;

Write the code for the Click event method of btnStartStop control that implements all the steps above except the last three steps:

&#124; 123456789101112131415161718192021222324252627282930313233343536 &#124; private void btnStartStop_Click( object sender, EventArgs e){    btnStartStop.Text = "Stop Game" ;    grpOption.Enabled = false ;    btnExit.Enabled = false ;    pnlBank.Enabled = true ;    textResult.Text = "" ;    // Determines number of digits in combination               if (rdoTwoDigits.Checked)    {        NumberOfDigit = 2;    }    else if (rdoThreeDigits.Checked)    {        NumberOfDigit = 3;    }    else    {        NumberOfDigit = 4;    }    for ( int i = 0; i < NumberOfDigit; i++)    {        Combo[i].Visible = true ;        Combo[i].Text = "" ;    }    if (NumberOfDigit != 4)    {        for ( int i = NumberOfDigit; i < 4; i++)        {            Combo[i].Visible = false ;        }    }} &#124;

Notice how the label control array ( Combo ) is used to display the label controls needed for the combination. |
| Step 9 | Save and run the project. Click Start Game button, select the three-digit combination option, and the game will switch to the "play" state, as shown in Figure 3.6.Ensure that number of label boxes are displayed according to the selected digits combination option. Notice Stop Game button doesn't do anything for now. You will fix it later.![](Image00018.jpg)Figure 3.6 Number of label boxes displayed is according to the selected digits combination option |
| Step 10 | When user clicks Stop Game button in the "play" state, several things must be done to switch the game to the "stop" state: 
*   Change Text property of btnStartStop to Start Game .
*   Enable grpOptions .
*   Enable Exit button.
*   Enable pnlBank .

Modify Click event method of btnStartStop :

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445 &#124; private void btnStartStop_Click( object sender, EventArgs e){    if (btnStartStop.Text == "Start Game" )    {    btnStartStop.Text = "Stop Game" ;    grpOption.Enabled = false ;    btnExit.Enabled = false ;    pnlBank.Enabled = true ;    textResult.Text = "" ;    // Determines number of digits in combination               if (rdoTwoDigits.Checked)    {        NumberOfDigit = 2;    }    else if (rdoThreeDigits.Checked)    {        NumberOfDigit = 3;    }    else    {        NumberOfDigit = 4;    }    for ( int i = 0; i < NumberOfDigit; i++)    {        Combo[i].Visible = true ;        Combo[i].Text = "" ;    }    if (NumberOfDigit != 4)    {        for ( int i = NumberOfDigit; i < 4; i++)        {            Combo[i].Visible = false ;        }    }    else    {        btnStartStop.Text = "Start Game" ;        grpOption.Enabled = true ;        btnExit.Enabled = true ;        pnlBank.Enabled = false ;    }} &#124;

 |
| Step 11 | Save and run project. You can now switch from "stop" to "play" and vice versa. Make sure you can display 2, 3, and 4 digit combinations, as shown in Figure 3.7.You can now see three other steps in the program: generating secret combinations and accepting and checking user input.![](Image00022.jpg)Figure 3.7 Project now can be switched from "stop" to "play" and vice versa |
| Step 12 | The critical step in this project is to generate the secret combination that the player will guess. With the options selected, you know that combinations can be 2 to 4 digits. You also specify that there are no repetitive digits in the combination.Because repetitive digits is not allowed, for each digit in combination, you generate a random number from 1 to 9, but only add it to the combination if the random value has not been used before. Here is a code snippet to do this task: 

&#124; 1234567891011121314151617181920212223 &#124; // Determines combinationSecretCombo = "" ;int j;bool UniqueDigit;for ( int i = 0; i < NumberOfDigit; i++){    // Chooses unique digit    do    {        j = MyRandom.Next(9) + 1;        UniqueDigit = true ;        if (i != 0)        {            for ( int k = 0; k < i; k++)            {                if (SecretCombo[k].ToString() == j.ToString())                     UniqueDigit = false ;            }        }    }    while (!UniqueDigit);    SecretCombo += j.ToString();} &#124;

In the code above, a string variable ( SecretCombo ) is used to store a combination. Initially this variable is empty. One digit at a time ( numberDigits ) is added to the SecretCombo using string splicing.A random digit J (from 1 to 9) is raised. You then look at the latest digit in the code to check whether the newly generated digit is a digit unit. If so, the digit is added to the SecretCombo . If it is not unique, a new random digit will be raised. All of this logic is implemented in loop Do . Learn how Mid function is used to see individual digits in SecretCombo . |
| Step 13 | Add the following declarations to the form-level to define secret combinations and assign random number objects: 

&#124; 12 &#124; String SecretCombo;Random MyRandom = new Random(); &#124;

 |
| Step 14 | Add the snippet code above to the Click event method from the btnStartStop button as follows: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970 &#124; private void btnStartStop_Click( object sender, EventArgs e){    if (btnStartStop.Text == "Start Game" )    {        btnStartStop.Text = "Stop Game" ;       grpOption.Enabled = false ;        btnExit.Enabled = false ;        pnlBank.Enabled = true ;        textResult.Text = "" ;        // Determines number of digits in combination                  if (rdoTwoDigits.Checked)        {            NumberOfDigit = 2;        }        else if (rdoThreeDigits.Checked)        {            NumberOfDigit = 3;        }        else        {            NumberOfDigit = 4;        }        for ( int i = 0; i < NumberOfDigit; i++)        {            Combo[i].Visible = true ;            Combo[i].Text = "" ;        }        if (NumberOfDigit != 4)        {            for ( int i = NumberOfDigit; i < 4; i++)            {                Combo[i].Visible = false ;            }        }        // Determines combination        SecretCombo = "" ;        int j;        bool UniqueDigit;        for ( int i = 0; i < NumberOfDigit; i++)        {            // Chooses unique digit            do            {                j = MyRandom.Next(9) + 1;                UniqueDigit = true ;                if (i != 0)                {                    for ( int k = 0; k < i; k++)                    {                        if ( SecretCombo[k]. ToString() == j.ToString())                            UniqueDigit = false ;                    }                }            }            while (!UniqueDigit);            SecretCombo += j.ToString();        }    }    else    {        btnStartStop.Text = "Start Game" ;        grpOption.Enabled = true ;        btnExit.Enabled = true ;        pnlBank.Enabled = false ;    }} &#124;

You can now generate a secret combination, but you can't see it yet. You will change it later. On many occasions, when developing a project, you want to check the results before the project is complete. This means you need to add temporary code for debugging purposes. Place this line of code after Next in the code that generates the combination: Console.WriteLine (SecretCombo) .This line of code will write the secret combination generated in the Output window of the debugger so that you can see whether each resulting combination meets the specified requirements (number of digits according to chosen option and do not have repeated digits). |
| Step 15 | Save and run the project. Click Start Game . Open Output window and see the resulting combination. Make sure the combination meets the requirements. Click Stop Game . Repeat this process for various combinations to ensure the combination is generated correctly. When finished, you need to delete the debug line from the code. |
| Step 16 | You are now ready to accept the player's guess to guess the secret combination using 9 keypad buttons. You can just write a Click event method for each of these buttons to get user input. Or, you can implement smarter steps by using an event method to handle clicking on the nine key controls.After the secret combination is raised, the next step is to let the user enter his guess. This is done using 9 number keys on the pnlBank control. The steps are as follows: 
*   Read the digits entered by the user.
*   If this is the first digit of a combination, all previous guesses are deleted on label controls.
*   Determine which button clicked.
*   Disable buttons that are clicked due to repeated digits is not permitted.
*   Add number in Text property of the button that was clicked into the user input combination.
*   Display the number on the corresponding label control.
*   If all digits have been entered, the buttons are enabled again and user input is compared with the actual secret combination. If not, repeat the steps above.

The code to perform these steps is placed in a method called btnCombo_Click . This method is to handle the Click event for the nine buttons for user input ( btn1 through btn9 ). |
| Step 17 | Add these declarations at the form-level to save the combinations entered by the user and number of digits entered: 

&#124; 12 &#124; int DigitEntered;String ComboEntered; &#124;

 |
| Step 18 | Initialize those two variables in the Click event method from btnStartStop button as follows: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172 &#124; private void btnStartStop_Click( object sender, EventArgs e){    if (btnStartStop.Text == "Start Game" )    {        btnStartStop.Text = "Stop Game" ;        grpOption.Enabled = false ;        btnExit.Enabled = false ;        pnlBank.Enabled = true ;        textResult.Text = "" ;        // Determines number of digits in combination                   if (rdoTwoDigits.Checked)        {            NumberOfDigit = 2;        }        else if (rdoThreeDigits.Checked)        {            NumberOfDigit = 3;        }        else        {            NumberOfDigit = 4;        }        for ( int i = 0; i < NumberOfDigit; i++)        {            Combo[i].Visible = true ;            Combo[i].Text = "" ;        }        if (NumberOfDigit != 4)        {            for ( int i = NumberOfDigit; i < 4; i++)            {                Combo[i].Visible = false ;            }        }        // Determines combination        SecretCombo = "" ;        int j;        bool UniqueDigit;        for ( int i = 0; i < NumberOfDigit; i++)        {            // Chooses unique digit            do            {                j = MyRandom.Next(9) + 1;                UniqueDigit = true ;                if (i != 0)                {                    for ( int k = 0; k < i; k++)                    {                        if ( SecretCombo[k].ToString() == j.ToString())                            UniqueDigit = false ;                    }                }            }            while (!UniqueDigit);            SecretCombo += j.ToString();        }        ComboEntered = "" ;        DigitEntered = 0;    }    else    {        btnStartStop.Text = "Start Game" ;        grpOption.Enabled = true ;        btnExit.Enabled = true ;        pnlBank.Enabled = false ;    }} &#124;

 |
| Step 19 | Modify the still empty btnCombo_Click method to implement the steps needed to check user input: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839 &#124; private void btnCombo_Click( object sender, EventArgs e){    String n;    // Determines which button clicked    Button ButtonClicked;    ButtonClicked = (Button) sender;    // Text property of clicked button    n = ButtonClicked.Text;    // Disables clicked button    ButtonClicked.Enabled = false ;    // If first button clicekd, clear all labels    if (DigitEntered == 0)    {        Combo[0].Text = "" ;        Combo[1].Text = "" ;        Combo[2].Text = "" ;        Combo[3].Text = "" ;    }    // Add Text property of clicked button in ComboEntered    ComboEntered += n;    DigitEntered++;    Combo[DigitEntered - 1].Text = n;    // If all digits has been entered, check combination    if (DigitEntered == NumberOfDigit)    {        // Resets combination buttons        for ( int i = 0; i < 9; i++)            ComboButton[i].Enabled = true ;        // Checks combination        Console.WriteLine(ComboEntered);    }} &#124;

![](Image00023.jpg)Figure 3.8 The combinations entered are the correct digits (have the number of digits according to the chosen option and do not violate the terms of repetitive digitsNotice the Text property of the button being clicked is the desired digit (variable n ). You use the Console line to display the combinations entered in the Output window. |
| Step 20 | Save and run project. Make sure the combinations entered are the correct digits (have the number of digits according to the chosen option and do not violate the terms of repetitive digits), as shown in Figure 3.8. |
| Step 21 | You now have the capability to generate a combination of secrets and read user's guesses. You need code that compares two string variables and displays the results. If it matches, it means the user has managed to guess the secret combination. If not, the user will be notified of how many digits are right and how many digits are in the right position.After the user has finished entering the guess, these steps need to be carried out: 
*   Display the user's guess ( ComboEntered ) in the textResult .
*   If the user's guess ( ComboEntered ) is the same as the secret combination ( SecretCombo ), then the game will be switched to the "stop" state.
*   If the guess is incorrect, number of exact digits and number of digits that are in the right position will be determined. Then, this information is displayed in the textResult control.
*   Clear user's guess for the next guess.

The code to implement these steps is placed in the Click event method of the btnCombo control:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970 &#124; private void btnCombo_Click( object sender, EventArgs e){    String n;    int CorrectDigits, CorrectPositions;    // Determines which button clicked    Button ButtonClicked;    ButtonClicked = (Button) sender;    // Text property of clicked button    n = ButtonClicked.Text;    // Disables clicked button    ButtonClicked.Enabled = false ;    // If first button clicekd, clear all labels    if (DigitEntered == 0)    {        Combo[0].Text = "" ;        Combo[1].Text = "" ;        Combo[2].Text = "" ;        Combo[3].Text = "" ;    }    // Add Text property of clicked button in ComboEntered    ComboEntered += n;    DigitEntered++;    Combo[DigitEntered - 1].Text = n;    // If all digits has been entered, check combination    if (DigitEntered == NumberOfDigit)    {        // Resets combination buttons        for ( int i = 0; i < 9; i++)            ComboButton[i].Enabled = true ;        // Checks combination        textResult.AppendText( "Entered: " +            ComboEntered + "\r\n" );        if (ComboEntered == SecretCombo)            btnStartStop.PerformClick();        else        {            CorrectDigits = 0;            for ( int i = 0; i < NumberOfDigit; i++)            {                n = ComboEntered[i].ToString();                for ( int j = 0; j < NumberOfDigit; j++)                    if (n == SecretCombo[j].ToString())                        CorrectDigits++;            }            // Number of digits in correct position            CorrectPositions = 0;            for ( int i = 0; i < NumberOfDigit; i++)                if (SecretCombo[i] == ComboEntered[i])                    CorrectPositions++;            textResult.AppendText(CorrectDigits.ToString() +                " correct digits" + "\r\n" );            textResult.AppendText(CorrectPositions.ToString() +                " in correct position" + "\r\n" );            textResult.AppendText( "Please try again ..." +                "\r\n\r\n" );            // Clears combination            ComboEntered = "" ;            DigitEntered = 0;          }    }} &#124;

The above code first counts the exact digits of the user input. The Code that checks if the digits are in the right position compares each digit in ComboEntered and SecretCombo . All results are displayed in the text box. |
| Step 22 | If the correct combination is entered, you will return the game to the "stop" state. An easy way to do this is to programmatically click Stop Game button using the PerformClick method. Using this approach, you need to add code to the Click event method of btnStartStop .The code is used to distinguish game termination before guessing the combination from game termination because the secret combination has been guessed.Modify the Click event method of btnStartStop control: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778 &#124; private void btnStartStop_Click( object sender, EventArgs e){    if (btnStartStop.Text == "Start Game" )    {        btnStartStop.Text = "Stop Game" ;        grpOption.Enabled = false ;        btnExit.Enabled = false ;        pnlBank.Enabled = true ;        textResult.Text = "" ;        // Determines number of digits in combination                   if (rdoTwoDigits.Checked)        {            NumberOfDigit = 2;        }        else if (rdoThreeDigits.Checked)        {            NumberOfDigit = 3;        }        else        {            NumberOfDigit = 4;        }        for ( int i = 0; i < NumberOfDigit; i++)        {            Combo[i].Visible = true ;            Combo[i].Text = "" ;        }        if (NumberOfDigit != 4)        {            for ( int i = NumberOfDigit; i < 4; i++)            {                Combo[i].Visible = false ;            }        }        // Determines combination        SecretCombo = "" ;        int j;        bool UniqueDigit;        for ( int i = 0; i < NumberOfDigit; i++)        {            // Chooses unique digit            do            {                j = MyRandom.Next(9) + 1;                UniqueDigit = true ;                if (i != 0)                {                    for ( int k = 0; k < i; k++)                    {                        if ( SecretCombo[k].ToString() == j.ToString())                            UniqueDigit = false ;                    }                }            }            while (!UniqueDigit);            SecretCombo += j.ToString();        }        ComboEntered = "" ;        DigitEntered = 0;    }    else    {        if (ComboEntered == SecretCombo)            textResult.AppendText( "Correct!!!!" + "\r\n" );        else            textResult.AppendText( "Game Stopped" + "\r\n" );        textResult.AppendText( "Combination: " + SecretCombo);        btnStartStop.Text = "Start Game" ;        grpOption.Enabled = true ;        btnExit.Enabled = true ;        pnlBank.Enabled = false ;    }} &#124;

 |
| Step 23 | Save and run project. The game now works perfectly. Try playing a few times to make sure everything works correctly:![](Image00024.jpg)Figure 3.9 Game now works perfectly |
| Step 24 | In the bin\Debug folder on this project, you have been provided two wav files that can be used for sound. The wrong.wav is used when guesses are incorrect. The true.wav is used when the user's guess is right.Add the following declarations to the form-level to represent the two sounds: 

&#124; 12 &#124; System.Media.SoundPlayer WrongSound;System.Media.SoundPlayer RightSound; &#124;

 |
| Step 25 | Modify the Load event method of the form to create sound objects: 

&#124; 12345678910111213141516171819202122232425 &#124; private void FormBankCode_Load( object sender, EventArgs e){    // Disables pnlBank and creates two arrays    pnlBank.Enabled = false ;    Combo[0] = lblCombol1;    Combo[1] = lblCombol2;    Combo[2] = lblCombol3;    Combo[3] = lblCombol4;    ComboButton[0] = btn1;    ComboButton[1] = btn2;    ComboButton[2] = btn3;    ComboButton[3] = btn4;    ComboButton[4] = btn5;    ComboButton[5] = btn6;    ComboButton[6] = btn7;    ComboButton[7] = btn8;    ComboButton[8] = btn9;    WrongSound = new        System.Media.SoundPlayer(Application.StartupPath +        "\\wrong.wav" );    RightSound = new        System.Media.SoundPlayer(Application.StartupPath +        "\\right.wav" );} &#124;

 |
| Step 26 | Finally, activate both sounds at the exact locations of the Click method of btnCombo : 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768697071727374 &#124; private void btnCombo_Click( object sender, EventArgs e){    String n;    int CorrectDigits, CorrectPositions;    // Determines which button clicked    Button ButtonClicked;    ButtonClicked = (Button) sender;    // Text property of clicked button    n = ButtonClicked.Text;    // Disables clicked button    ButtonClicked.Enabled = false ;    // If first button clicekd, clear all labels    if (DigitEntered == 0)    {        Combo[0].Text = "" ;        Combo[1].Text = "" ;        Combo[2].Text = "" ;        Combo[3].Text = "" ;    }    // Add Text property of clicked button in ComboEntered    ComboEntered += n;    DigitEntered++;    Combo[DigitEntered - 1].Text = n;    // If all digits has been entered, check combination    if (DigitEntered == NumberOfDigit)    {        // Resets combination buttons        for ( int i = 0; i < 9; i++)            ComboButton[i].Enabled = true ;        // Checks combination        textResult.AppendText( "Entered: " +            ComboEntered + "\r\n" );        if (ComboEntered == SecretCombo)        {            RightSound.Play();            btnStartStop.PerformClick();        }        else        {            WrongSound.Play();            CorrectDigits = 0;            for ( int i = 0; i < NumberOfDigit; i++)            {                n = ComboEntered[i].ToString();                for ( int j = 0; j < NumberOfDigit; j++)                    if (n == SecretCombo[j].ToString())                        CorrectDigits++;            }            // Number of digits in correct position            CorrectPositions = 0;            for ( int i = 0; i < NumberOfDigit; i++)                if (SecretCombo[i] == ComboEntered[i])                    CorrectPositions++;            textResult.AppendText(CorrectDigits.ToString() +                " correct digits" + "\r\n" );            textResult.AppendText(CorrectPositions.ToString() +                " in correct position" + "\r\n" );            textResult.AppendText( "Please try again ..." +                "\r\n\r\n" );            // Clears combination            ComboEntered = "" ;            DigitEntered = 0;          }    }} &#124;

 |
| Step 27 | Save and run the project. You now have the full version of this game. Enjoy this game. See how you find strategies in winning matches. |
|  |  |

| Form1.cs |
| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197198199200201202203204205206207208209210211 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;namespace Kode_Rahasia{    public partial class FormBankCode : Form    {        Label[] Combo = new Label[4];        Button[] ComboButton = new Button[9];        int NumberOfDigit;        String SecretCombo;        Random MyRandom = new Random();        int DigitEntered;        String ComboEntered;        System.Media.SoundPlayer WrongSound;        System.Media.SoundPlayer RightSound;        public FormBankCode ()        {            InitializeComponent();        }        private void FormBankCode_Load( object sender, EventArgs e)        {            // Disables pnlBank and creates two arrays            pnlBank.Enabled = false ;            Combo[0] = lblCombol1;            Combo[1] = lblCombol2;            Combo[2] = lblCombol3;            Combo[3] = lblCombol4;            ComboButton[0] = btn1;            ComboButton[1] = btn2;            ComboButton[2] = btn3;            ComboButton[3] = btn4;            ComboButton[4] = btn5;            ComboButton[5] = btn6;            ComboButton[6] = btn7;            ComboButton[7] = btn8;            ComboButton[8] = btn9;            WrongSound = new System.Media.SoundPlayer(Application.StartupPath +                "\\salah.wav" );            RightSound = new System.Media.SoundPlayer(Application.StartupPath +                "\\benar.wav" );        }        private void btnExit_Click( object sender, EventArgs e)        {            this .Close();        }        private void btnStartStop_Click( object sender, EventArgs e)        {            if (btnStartStop.Text == "Start Game" )            {                btnStartStop.Text = "Stop Game" ;                grpOption.Enabled = false ;                btnExit.Enabled = false ;                pnlBank.Enabled = true ;                textResult.Text = "" ;                // Determines number of digits in combination                           if (rdoTwoDigits.Checked)                {                    NumberOfDigit = 2;                }                else if (rdoThreeDigits.Checked)                {                    NumberOfDigit = 3;                }                else                {                    NumberOfDigit = 4;                }                for ( int i = 0; i < NumberOfDigit; i++)                {                    Combo[i].Visible = true ;                    Combo[i].Text = "" ;                }                if (NumberOfDigit != 4)                {                    for ( int i = NumberOfDigit; i < 4; i++)                    {                        Combo[i].Visible = false ;                    }                }                // Determines combination                SecretCombo = "" ;                int j;                bool UniqueDigit;                for ( int i = 0; i < NumberOfDigit; i++)                {                    // Chooses unique digit                    do                    {                        j = MyRandom.Next(9) + 1;                        UniqueDigit = true ;                        if (i != 0)                        {                            for ( int k = 0; k < i; k++)                            {                                if (SecretCombo[k].ToString() == j.ToString())                                    UniqueDigit = false ;                            }                        }                    }                    while (!UniqueDigit);                    SecretCombo += j.ToString();                }                ComboEntered = "" ;                DigitEntered = 0;            }            else            {                if (ComboEntered == SecretCombo)                    textResult.AppendText( "Correct!!!!" + "\r\n" );                else                    textResult.AppendText( "Game Stopped" + "\r\n" );                textResult.AppendText( "Combination: " + SecretCombo);                btnStartStop.Text = "Start Game" ;                grpOption.Enabled = true ;                btnExit.Enabled = true ;                pnlBank.Enabled = false ;            }        }        private void btnCombo_Click( object sender, EventArgs e)        {            String n;            int CorrectDigits, CorrectPositions;            // Determines which button clicked            Button ButtonClicked;            ButtonClicked = (Button) sender;            // Text property of clicked button            n = ButtonClicked.Text;            // Disables clicked button            ButtonClicked.Enabled = false ;            // If first button clicekd, clear all labels            if (DigitEntered == 0)            {                Combo[0].Text = "" ;                Combo[1].Text = "" ;                Combo[2].Text = "" ;                Combo[3].Text = "" ;            }            // Add Text property of clicked button in ComboEntered            ComboEntered += n;            DigitEntered++;            Combo[DigitEntered - 1].Text = n;            // If all digits has been entered, check combination            if (DigitEntered == NumberOfDigit)            {                // Resets combination buttons                for ( int i = 0; i < 9; i++)                    ComboButton[i].Enabled = true ;                // Checks combination                textResult.AppendText( "Entered: " + ComboEntered + "\r\n" );                if (ComboEntered == SecretCombo)                {                    RightSound.Play();                    btnStartStop.PerformClick();                }                else                {                    WrongSound.Play();                    CorrectDigits = 0;                    for ( int i = 0; i < NumberOfDigit; i++)                    {                        n = ComboEntered[i].ToString();                        for ( int j = 0; j < NumberOfDigit; j++)                            if (n == SecretCombo[j].ToString())                                CorrectDigits++;                    }                    // Number of digits in correct position                    CorrectPositions = 0;                    for ( int i = 0; i < NumberOfDigit; i++)                        if (SecretCombo[i] == ComboEntered[i])                            CorrectPositions++;                    textResult.AppendText(CorrectDigits.ToString() +                        " correct digits" + "\r\n" );                    textResult.AppendText(CorrectPositions.ToString() +                        " in correct position" + "\r\n" );                    textResult.AppendText( "Please try again ..." + "\r\n\r\n" );                    // Clears combination                    ComboEntered = "" ;                    DigitEntered = 0;                }            }        }    }} |
|  |  |

TUTORIAL 4

HORSE RACING

In this tutorial, you will build Horse Racing game. This is a simple game. Up to 10 horses will race to the finish line. You guessed two horses that you thought could win the race. By clicking on the Start button, the race will start. All horses will race speed to get to the finish line.

| Description |
| Labels are used to display instructions and number of horses in a race. Four button controls are used: two buttons to change number of horses, one button to start the game, and one other button to stop the game. The picture box control is used to load the horse image. A timer control is used to update the horse's movement during the race.![](Image00025.jpg)Figure 4.1 All controls used in Horse Racing game projectRun the program (press <F5>). The game will run in the 'initial' state. The program description and instructions will be displayed. At this point, the user can click Start button to start the game, click the arrow button to change number of horses to be competed or click Stop to stop the program.![](Image00026.jpg)Figure 4.2 The Horse Racing game is at initial state showing program description and instructionsChange number of horses if you want (for example, 8) by clicking the right arrow button under Number of Horses . Click Start button to start the game. Program instructions will disappear. Eight horses will be displayed, ready to race:![](Image00027.jpg)Figure 4.3 Eight horses are ready to raceIn this situation, the user needs to choose two horses that are considered to win the race. To do this, the user only needs to click on the desired horses using mouse, and a red X symbol will be displayed next to the selected horses, as shown in Figure 4.4.![](Image00028.jpg)Figure 4.4 Two red X symbols will appear when user choose two horses guessed to win raceThen, the user can click on the Start button to start the race. All horses race across the screen to reach the finish line:![](Image00029.jpg)Figure 4.5 All horses race to finish line when user clicks Start button |
| Tutorial Steps |
| Step 1 | You will start building Horse Racing game project. Start a new project in Visual Basic. It is recommended that you immediately save it with a name that you choose yourself. This will create the folders and file structure needed for your project. |
| Step 2 | Place two panel controls on the form (one panel with a width of 100 pixels on the left side, one other panel with a width of 900 pixels on the right side). Place two labels and four buttons in the left panel. Place a label control and a picture box control in the right panel. Add a timer control. The form will now look as shown in Figure 4.6.Labels are used to display information. Two buttons are used to change number of horses, two other buttons to start and stop the game. The timer control sets the horse's movements. |
| Step 3 | Set control properties using the Properties window: 

&#124; A number of properties of the Form1 object &#124;
&#124; Property &#124; Value &#124;
&#124; Name &#124; FormHorseRacing &#124;
&#124; Text &#124; Horse Racing &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124;  &#124;  &#124;

![](Image00030.jpg)Figure 4.6 All controls used in this project and their positions

&#124; One of properties of the Panel1 object &#124;
&#124; BackColor &#124; DeepPink &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label1 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Text &#124; Number of Horses &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label3 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; Name &#124; lblHorse &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; ForeColor &#124; White &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button1 object &#124;
&#124; Name &#124; btnLeft &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; < &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button2 object &#124;
&#124; Name &#124; btnRight &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; > &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button3 object &#124;
&#124; Name &#124; btnStart &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; Start &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button4 object &#124;
&#124; Name &#124; btnStop &#124;
&#124; Font Size &#124; 12 &#124;
&#124; Text &#124; Stop &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel2 object &#124;
&#124; Name &#124; pnlGame &#124;
&#124; BackColor &#124; White &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label2 object &#124;
&#124; Name &#124; lblInstruction &#124;
&#124; Font Size &#124; 12 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox1 object &#124;
&#124; Name &#124; picHorse &#124;
&#124; Image &#124; horse.png &#124;
&#124; SizeMode &#124; AutoSize &#124;
&#124; Visible &#124; True &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Timer1 object &#124;
&#124; Name &#124; timerHorse &#124;
&#124; Interval &#124; 100 &#124;
&#124;  &#124;  &#124;

You will now start writing code for this game. You will write the code in several stages. As an initial step, you will write the code that starts the game and set the initial state. Then, you will see how to set the 'stop' state due to clicking Stop button. Finally, you will write the code for the horse race after Start button is clicked again. During code development, you will modify certain procedures several times before reaching the end point. |
| Step 4 | Whenever the user starts the program, there are several initializations that need to be done. You will see what initializations are needed in this project. When the program starts, you naturally want to display game instructions. You also want to initialize (provide initial values) to NumberOfHorses and StatusGame . This initialization is in the Load procedure of the form.![](Image00031.jpg)Figure 4.7 The initialization in the Load procedure of the formYou declare the following three variables ( NumberOfHorses , StatusGame , and PanelGame ) as form level variables: 

&#124; 123 &#124; int NumberOfHorses;string StatusGame;Graphics PanelGame; &#124;

&#124; 12345678910111213141516171819202122 &#124; private void FormHorseRacing_Load( object sender, EventArgs e){    NumberOfHorses = 3;   StatusGame = "Start" ;   lblInstruction.Text = "HORSE RACING GAME \n\n" ;    lblInstruction.Text += "Two horses are racing to arrive at the        finish line. \n" +        "Guess which horse will arrive first to the end." ;    lblInstruction.Text += "\n\nChoose number of horses to race " +        "by pressing the left button to decrease, " +       "the right button to add." ;    lblInstruction.Text += "\n\nClick on the Start button to start        the game." ;   lblInstruction.Text += "\n\nClick on the Stop button to end the         game." ;    lblHorse.Text = NumberOfHorses.ToString();    PanelGame = pnlGame.CreateGraphics();} &#124;

NumberOfHorses are set to 3 and StatusGame is set to " Start ". Next, after creating a graphic object ( PanelGame ), using a series of statements, you write game instructions in lblInstruction . |
| Step 5 | Save and run the program to see what shown in Figure 4.7. |
| Step 6 | To change number of horses, user can click on one of the two arrow keys provided. The code to do so is placed in the Click event procedure of btnLeft and btnRight : 

&#124; 1234567891011121314151617181920212223 &#124; private void btnLeft_Click( object sender, EventArgs e){    if (StatusGame == "Start" ) // Decreases number of horses    {       NumberOfHorses -= 1;       if (NumberOfHorses < 3)            NumberOfHorses = 3;        lblHorse.Text = NumberOfHorses.ToString();    }}private void btnRight_Click( object sender, EventArgs e){    if (StatusGame == "Start" ) // Decreases number of horses   {        NumberOfHorses += 1;       if (NumberOfHorses >10)            NumberOfHorses = 10;        lblHorse.Text = NumberOfHorses.ToString();   }} &#124;

This code is quite simple. Number of horses is only changed when the game is in the "Start" state. If the < button is clicked, the program will reduce number of horses by one (with a minimum of 3). If the > button is clicked, the program will add number of horses by one (with a maximum of 10). New value ​​for number of horses is then displayed. |
| Step 7 | Save and run program. Make sure both the arrow keys work well which changes the value of number of horses between 3 and 10, as shown in Figure 4.8. |
| Step 8 | After number of horses are set, the next step is to click on Start button to allow the user to select two horses. So, you need a code to move from the "Start" state to the "Stop" state. When Start button is clicked on the "Start" state, you need to do these steps: 
*   Change StatusGame to "Stop".
*   Clear the game screen.
*   Draw a horse and a race track for each horse.
*   Draw the finish line of the race.
*   Display instructions for the user.

![](Image00032.jpg)Figure 4.8 User now can change number of horses using two arrow keysTo draw a horse, you divide the race region into 10 equal areas (of the maximum number of horses). The image stored on picHorse is used to represent horses.Now, add this code to the Click event procedure from btnStart :

&#124; 12345678910111213141516171819202122232425262728293031 &#124; private void btnStart_Click( object sender, EventArgs e){    if (StatusGame == "Start" ) //User clicks Start button    {        StatusGame = "Stop" ;        lblInstruction.Visible = false ;        PanelGame.Clear(Color.White); //Draws horse and trajectory        for ( int i = 1; i <= NumberOfHorses; i++)        {            PanelGame.DrawImage(picHorse.Image, 50,                (i - 1) * 60 + 10);            PanelGame.DrawLine(Pens.Green, 50, (i - 1) * 60 + 35,                820, (i - 1) * 60 + 35);        }        //Draws finisih line        PanelGame.FillRectangle(Brushes.Pink, 820, 10, 10,            NumberOfHorses * 60 - 10);        Font MyFont = new Font( "Arial" , 14);        PanelGame.DrawString( "Click on the two horses you choose." ,            MyFont, Brushes.Red, 200, 40);        PanelGame.DrawString( " Click the Start button to start the race. " ,            MyFont, Brushes.Red, 200, 70);        NumberOfHorsesByUser = 0;        for ( int i = 1; i <= NumberOfHorses; i++)            HorsesChosenArr[i] = 0;    }} &#124;

Pay attention to how you draw each horse. Two new variables added. NumberOfHorsesByUser is initialized to zero. HorsesChosenArr array is used to track which horses the user choose. Add the following declaration:

&#124; 12 &#124; int [] HorsesChosenArr = new int [10];int NumberOfHorsesByUser; &#124;

 |
| Step 9 | Save and run the program. Choose number of horses (for example, 7). Click Start button and you will see:![](Image00033.jpg)Figure 4.9 Every horse, trajectory and finish line are drawn on panel |
| Step 10 | The next step is to choose two horses that you want to compete with. You will write the code for it. However, you first need to handle one other thing that needs to be done in the "Start" state, which is to stop the program.One last thing that can be done while the game is in the "Start" state is to click Stop button. This will stop the program. This code is quite simple. Add the following lines to the Click event procedure from btnStop : 

&#124; 12345 &#124; private void btnStop_Click( object sender, EventArgs e){    if (StatusGame == "Start" )        this .Close();} &#124;

Save and run program to prove it. |
| Step 11 | After the game is in the "Stop" condition, the user can choose two horses that he wants to compete to reach finish line. To detect click on a horse, you need to know its location and size. From the code that places the horse on pnlGame , you can see for i-th horse (where i starts from 1 to NumberOfHorses ): 

&#124; 1 &#124; PanelGame.DrawImage(picHorse.Image, 50, (i - 1) * 60 + 10) &#124;

The HorsesChosenArr is used to tell which horses are selected. A red X will be placed next to the selected horse. After two horses are selected ( NumberOfHorsesByUser = 2), you can start the race by clicking Start . If the user clicks on two horses and wants to change the race, the user can click on the horse which has been deleted and the red X will disappear so the user can choose another.When a horse is clicked, the following steps are taken:

*   If the horse has been selected before, then NumberOfHorsesByUser is decremented, set HorsesChosenArr[i] to 0 and delete the letter X next to the horse.
*   If the horse is not selected before and NumberOfHorsesByUser is less than 2, then NumberOfHorsesByUser is incremented, set HorsesChosenArr[i] to 1 and draw a red X next to the horse.

You follow these steps in that order to ensure that the user does not click on a horse that has been previously selected.![](Image00034.jpg)Figure 4.10 User can select two horses to competeThe code for horse selection is placed inside MouseDown event procedure from pnlGame :

&#124; 123456789101112131415161718192021222324252627282930313233 &#124; private void pnlGame_MouseDown( object sender, MouseEventArgs e){   int HorseClicked;    if (StatusGame == "Stop" )    {       //User chooses two horses        Decimal ValHorses = (e.Y - 10)/60;        HorseClicked = Convert.ToInt32(Math.Floor(ValHorses) + 1);        //if horse has been clicked before, delete letter X        if (HorsesChosenArr[HorseClicked] == 1)        {           NumberOfHorsesByUser -= 1;            HorsesChosenArr[HorseClicked] = 0;            PanelGame.FillRectangle(Brushes.White, 10,                (HorseClicked - 1) * 60 + 20, 30, 30);        }        else if (NumberOfHorsesByUser < 2)        {            //If the horse is not selected before            NumberOfHorsesByUser += 1;            HorsesChosenArr[HorseClicked] = 1;            PanelGame.DrawLine(Pens.Red, 10,                (HorseClicked - 1) * 60 + 20, 40,                (HorseClicked - 1) * 60 + 50);            PanelGame.DrawLine(Pens.Red, 10,                (HorseClicked - 1) * 60 + 50, 40,                (HorseClicked - 1) * 60 + 20);       }    }} &#124;

 |
| Step 12 | Save and run the program. Set number of horses to five. Select two of those horses and notice X letter next to each horse, as shown in Figure 4.10. |
| Step 13 | After two horses are selected, user can click on Start button to start the race, which puts the game into "Moving" state. So, when Start button is clicked in the "Stop" state, the following steps will be performed: 
*   Change StatusGame to "Move".
*   Clear instructions.
*   For each horse, the final random position is determined before the finish line.
*   Two winners are chosen at random.
*   Move horses to their final positions.
*   Change StatusGame to "Start" before another race starts.

To move a horse, you use the timer control ( timerHorse ). With each Tick event, you move each horse as far as a fraction of the difference between its starting and ending position. This method gives a smooth animation to the final position in 5000 milliseconds (5 seconds). Because the interval is 100 milliseconds, you move each horse for 1/50 times the difference between the starting and ending positions for each Click event. You can change this value. The code that starts moving horses is added to the Click event on btnStart :

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657 &#124; private void btnStart_Click( object sender, EventArgs e){    if (StatusGame == "Start" ) //User clicks Start button    {        StatusGame = "Stop" ;        lblInstruction.Visible = false ;        PanelGame.Clear(Color.White); //Draws horse and trajectory        for ( int i = 1; i <= NumberOfHorses; i++)        {            PanelGame.DrawImage(picHorse.Image, 50,                (i - 1) * 60 + 10);            PanelGame.DrawLine(Pens.Green, 50, (i - 1) * 60 + 35,                820, (i - 1) * 60 + 35);        }        //Draws finisih line        PanelGame.FillRectangle(Brushes.Pink, 820, 10, 10,            NumberOfHorses * 60 - 10);        Font MyFont = new Font( "Arial" , 14);        PanelGame.DrawString( "Click on the two horses you choose." ,            MyFont, Brushes.Red, 200, 40);        PanelGame.DrawString( " Click the Start button to start the race. " ,            MyFont, Brushes.Red, 200, 70);        NumberOfHorsesByUser = 0;        for ( int i = 1; i <= NumberOfHorses; i++)            HorsesChosenArr[i] = 0;    }    else if (StatusGame == "Stop" && NumberOfHorsesByUser == 2){       StatusGame = "Moving" ;       PanelGame.FillRectangle(Brushes.White, 150, 40, 450, 50);        //Determines starting position/final position        NumberOfMoves = 0;        for ( int i = 1; i <= NumberOfHorses; i++)       {            HorsePosition[i] = 50;            LastPosition[i] = 400 + MyRandom.Next(360);       }        //Chooses two winners        Winner[0] = MyRandom.Next(NumberOfHorses) + 1;   NextWinner:       Winner[1] = MyRandom.Next(NumberOfHorses) + 1;        if (Winner[0] == Winner[1])            goto NextWinner;        LastPosition[Winner[0]] = 850;        LastPosition[Winner[1]] = 850;        timerHorse.Start();    }} &#124;

Notice how the final positions and the two winners are determined. Some new variables are given and declared as form-level variables:

&#124; 12345 &#124; int NumberOfMoves;int [] HorsePosition = new int [10];int [] LastPosition = new int [10];int [] Winner = new int [2];Random MyRandom = new Random(); &#124;

NumberOfMoves determines how many Tick events have been called. The HorsePosition is an array containing the current horse locations, while LastPosition is an array containing the final positions. The Winner contains two winners. MyRandom is used to generate random locations. |
| Step 14 | Movement starts with enabling timerHorse . The code to move the horse is placed in the Tick event procedure of timerHorse : 

&#124; 12345678910111213141516171819 &#124; private void timerHorse_Tick( object sender, EventArgs e){    NumberOfMoves += 1;   for ( int i = 1; i <= NumberOfHorses; i++)    {        PanelGame.FillRectangle(Brushes.White,            HorsePosition[i], (i - 1) * 60 + 10, 50, 50);        HorsePosition[i] += (LastPosition[i] - 50) / 50;        PanelGame.DrawImage(picHorse.Image,            HorsePosition[i], (i - 1) * 60 + 10);   }    if (NumberOfMoves == 49)    {        timerHorse.Stop();        StatusGame = "Start" ;    }} &#124;

 |
| Step 15 | Save and run program. Choose number of horses as you like (for example, 9). Click Start button, and choose horses turtles you guess that can win the race:![](Image00035.jpg)Figure 4.11 Final version of Horse Racing game |
|  |  |

| Form1cs |
| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;namespace Horse_Racing{    public partial class FormHorseRacing : Form    {        int NumberOfHorses;        String StatusGame;        Graphics PanelGame;        int [] HorsesChosenArr = new int [10];        int NumberOfHorsesByUser;        int NumberOfMoves;        int [] HorsePosition = new int [10];        int [] LastPosition = new int [10];        int [] Winner = new int [2];        Random MyRandom = new Random();        public FormHorseRacing ()        {            InitializeComponent();        }        private void btnStart_Click( object sender, EventArgs e)        {            if (StatusGame == "Start" ) //User clicks Start button            {                StatusGame = "Stop" ;                lblInstruction.Visible = false ;                PanelGame.Clear(Color.White); //Draws horse and trajectory                for ( int i = 1; i <= NumberOfHorses; i++)                {                    PanelGame.DrawImage(picHorse.Image, 50, (i - 1) * 60 + 10);                    PanelGame.DrawLine(Pens.Green, 50,                        (i - 1) * 60 + 35, 820, (i - 1) * 60 + 35);                }                //Draws finisih line                PanelGame.FillRectangle(Brushes.Pink, 820, 10, 10,                    NumberOfHorses * 60 - 10);                Font MyFont = new Font( "Arial" , 14);                PanelGame.DrawString( "Click on the two horses you choose." ,                    MyFont, Brushes.Red, 200, 40);                PanelGame.DrawString( " Click the Start button to start the race. " ,                    MyFont, Brushes.Red, 200, 70);                NumberOfHorsesByUser = 0;                for ( int i = 1; i <= NumberOfHorses; i++)                    HorsesChosenArr[i] = 0;            }            else if (StatusGame == "Stop" && NumberOfHorsesByUser == 2){                StatusGame = "Moving" ;                PanelGame.FillRectangle(Brushes.White, 150, 40, 450, 50);                //Determine starting position/final position                NumberOfMoves = 0;                for ( int i = 1; i <= NumberOfHorses; i++)                {                    HorsePosition[i] = 50;                    LastPosition[i] = 400 + MyRandom.Next(360);                }                //Chooses two winners                Winner[0] = MyRandom.Next(NumberOfHorses) + 1;            NextWinner:                Winner[1] = MyRandom.Next(NumberOfHorses) + 1;                if (Winner[0] == Winner[1])                    goto NextWinner;                LastPosition[Winner[0]] = 850;                LastPosition[Winner[1]] = 850;                timerHorse.Start();            }        }        private void FormHorseRacing_Load( object sender, EventArgs e)        {            NumberOfHorses = 3;            StatusGame = "Start" ;            lblInstruction.Text = "HORSE RACING GAME \n\n" ;            lblInstruction.Text += "Two horses are racing to arrive at the finish line. \n" +                "Guess which horse will arrive first to the end." ;            lblInstruction.Text += "\n\nChoose number of horses to race " +                "by pressing the left button to decrease, " +                "the right button to add." ;            lblInstruction.Text += "\n\nClick on the Start button to start the game." ;            lblInstruction.Text += "\n\nClick on the Stop button to end the game." ;            lblHorse.Text = NumberOfHorses.ToString();            PanelGame = pnlGame.CreateGraphics();        }        private void btnLeft_Click( object sender, EventArgs e)        {            if (StatusGame == "Start" ) // Decreases number of horses            {                NumberOfHorses -= 1;                if (NumberOfHorses < 3)                    NumberOfHorses = 3;                lblHorse.Text = NumberOfHorses.ToString();            }        }        private void btnRight_Click( object sender, EventArgs e)        {            if (StatusGame == "Start" ) // Decreases number of horses            {                NumberOfHorses += 1;                if (NumberOfHorses >10)                    NumberOfHorses = 10;                lblHorse.Text = NumberOfHorses.ToString();            }        }        private void btnStop_Click( object sender, EventArgs e)        {            if (StatusGame == "Start" )                this .Close();        }        private void pnlGame_MouseDown( object sender, MouseEventArgs e)        {            int HorseClicked;            if (StatusGame == "Stop" )            {                //User chooses two horses                Decimal ValHorses = (e.Y - 10)/60;                HorseClicked = Convert.ToInt32(Math.Floor(ValHorses) + 1);                //if horse has been clicked before, delete letter X                if (HorsesChosenArr[HorseClicked] == 1)                {                    NumberOfHorsesByUser -= 1;                    HorsesChosenArr[HorseClicked] = 0;                    PanelGame.FillRectangle(Brushes.White, 10,                        (HorseClicked - 1) * 60 + 20, 30, 30);                }                else if (NumberOfHorsesByUser < 2)                {                    //If the horse is not selected before                    NumberOfHorsesByUser += 1;                    HorsesChosenArr[HorseClicked] = 1;                    PanelGame.DrawLine(Pens.Red, 10,                        (HorseClicked - 1) * 60 + 20, 40,                        (HorseClicked - 1) * 60 + 50);                    PanelGame.DrawLine(Pens.Red, 10,                        (HorseClicked - 1) * 60 + 50, 40,                        (HorseClicked - 1) * 60 + 20);                }            }        }        private void timerHorse_Tick( object sender, EventArgs e)        {            NumberOfMoves += 1;            for ( int i = 1; i <= NumberOfHorses; i++)            {                PanelGame.FillRectangle(Brushes.White,                    HorsePosition[i], (i - 1) * 60 + 10, 50, 50);                HorsePosition[i] += (LastPosition[i] - 50) / 50;                PanelGame.DrawImage(picHorse.Image,                    HorsePosition[i], (i - 1) * 60 + 10);            }            if (NumberOfMoves == 49)            {                timerHorse.Stop();                StatusGame = "Start" ;            }        }    }} |
|  |  |

TUTORIAL 6

CATCHING BALL GAME

In this tutorial, you will build Catching Ball game. The bird flew and dropped ball from the sky. Users are challenged to position man under the fallen ball to catch it.

| Description |
| Labels are used for instructions and to display game information (remaining time, number of balls captured, and game difficulty level). Two buttons are used to change the game difficulty level, one button to start the game, and another button to stop the game. Picture box controls hold images for man, bird, and ball.Run the program (press <F5>). The game will appear in the "starting" state. Description and program instructions are given. At this point, the user can click Start button to start the game, click the arrow buttons to change the difficulty level of the game or click Stop button to stop the program.![](Image00036.jpg)Figure 3.1 All controls used in Catching Ball game project![](Image00037.jpg)Figure 6.2 The Catcing Ball game is at “starting” state showing program description and instructionsChange the game's difficulty level if desired (for example 5) by clicking on the small arrow buttons below Difficulty label. Then click on Start button. Program instructions will disappear. A bird is displayed above the screen dropping ball. This is the "playing" state:![](Image00038.jpg)Figure 6.3 Game is at “playing” stateYou can shift or move man to below the ball to catch it. You can move man using the arrow keys on the keyboard or by pressing the left or right mouse button. When the ball reaches man, you will get one point. If the ball is not captured and passes man, the score does not increase:![](Image00039.jpg)Figure 6.4 User can move man to below the ball to catch it, using arrow keys on the keyboard or by pressing the left or right mouse button![](Image00040.jpg)Figure 6.5 Final result is displayed in a message boxThe game continues for 60 seconds. Remaining time is displayed. And the final result is displayed in the message box that appears at the end of the game, as shown in Figure 6.5. |
| Tutorial Steps |
| Step 1 | You will start building Catching Ball game project, by designing the form. Start a new project in Visual Basic. Once started, it is recommended that you save the project with the name you choose. This will create the folder and file structure needed for your project.Place two control panels on the form (one panel with a width of 100 pixels on the left side and one other panel with a width of 900 pixels on the right side). Make the two panels have a height of 600 pixels. Place six labels and four buttons in the left panel. Place a label control and three picture box controls on the right panel. Add a timer control. The form will look like this:![](Image00041.jpg)Figure 6.6 All controls user and their positions formThe labels on the left panel are used to display game information. Two buttons are used to change the game difficulty level, one button to start the game, and one other button to stop the game. The label controls on the right panel are used to display game instructions. Picture boxes are used to contain Man, Bird, and Ball images. Timer is used to control the game. |
| Step 2 | Set control properties using the Properties window: 

&#124; A number of properties of the Form1 object &#124;
&#124; Name &#124; FormCatchingBall &#124;
&#124; Text &#124; Catching Ball &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; KeyPreview &#124; True &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124;  &#124;  &#124;

&#124; One of properties of the Panel1 object &#124;
&#124; BackColor &#124; DeepPink &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label1 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Text &#124; Remaining Time: &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label2 object &#124;
&#124; Name &#124; lblTime &#124;
&#124; AutoSize &#124; False &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; ForeColor &#124; White &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label3 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Text &#124; Ball: &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label4 object &#124;
&#124; Name &#124; lblScore &#124;
&#124; AutoSize &#124; False &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; ForeColor &#124; White &#124;
&#124; Text &#124; 0 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label5 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; ForeColor &#124; Yellow &#124;
&#124; Text &#124; Difficulty: &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label6 object &#124;
&#124; Name &#124; lblDifficulty &#124;
&#124; AutoSize &#124; False &#124;
&#124; Font &#124; Bold, 12 &#124;
&#124; ForeColor &#124; White &#124;
&#124; Text &#124; 1 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button1 object &#124;
&#124; Name &#124; btnLeft &#124;
&#124; FontSize &#124; 12 &#124;
&#124; Text &#124; < &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button2 object &#124;
&#124; Name &#124; btnRight &#124;
&#124; FontSize &#124; 12 &#124;
&#124; Text &#124; > &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button3 object &#124;
&#124; Name &#124; btnStart &#124;
&#124; FontSize &#124; 12 &#124;
&#124; Text &#124; Start &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button4 object &#124;
&#124; Name &#124; btnStop &#124;
&#124; FontSize &#124; 12 &#124;
&#124; Text &#124; Stop &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel2 object &#124;
&#124; Name &#124; pnlGame &#124;
&#124; BackColor &#124; Gold &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label7 object &#124;
&#124; Name &#124; lblInstruction &#124;
&#124; FontSize &#124; 12 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox1 object &#124;
&#124; Name &#124; picMan &#124;
&#124; Image &#124; man.png &#124;
&#124; SizeMode &#124; AutoSize &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox2 object &#124;
&#124; Name &#124; picBird &#124;
&#124; Image &#124; bird.png &#124;
&#124; SizeMode &#124; AutoSize &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the PictureBox3 object &#124;
&#124; Name &#124; picBall &#124;
&#124; Image &#124; ball.png &#124;
&#124; SizeMode &#124; AutoSize &#124;
&#124; Visible &#124; False &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Timer1 object &#124;
&#124; Name &#124; timerGame &#124;
&#124; Interval &#124; 100 &#124;
&#124;  &#124;  &#124;

When finished, the form will look like in the figure below.![](Image00042.jpg)Figure 6.7 Form after properties setting done |
| Step 3 | You will now start writing the code for this game in a few steps. As an initial step, you will write the code that starts the program and sets the ‘starting’ state. Then, you will see how to set the 'playing' state (position all graphic elements) after Start button is clicked. You then write the code to move the ball to the bottom of the screen, shift man (using a mouse click or keyboard key), and check whether man is able to capture the ball. During the code development process, you will modify certain procedures repeatedly before reaching the final definition.Every time the program starts, there are several initializations that need to be done. Look at the initializations needed in this game. When the program first starts, you naturally want to display game instructions. You also need to initialize the game's difficulty level ( Difficulty ) and game status ( StatusGame ). This initialization is carried out in the Load event procedure on the form.You declare two form-level variables ( Difficulty and StatusGame ): 

&#124; 12 &#124; int Difficulty;String StatusGame; &#124;

 |
| Step 4 | Add the following code to the Load event procedure from the form: 

&#124; 1234567891011121314151617181920 &#124; private void FormCatchingBall_Load( object sender, EventArgs e){   //Catching Ball Game    Difficulty = 1;    StatusGame = "Starting" ;    lblInstruction.Text = "CATCHING BALL GAME \n\n" ;    lblInstruction.Text += "In this game, you will try to \n" +        "catch as many as possible fallen ball." ;    lblInstruction.Text += "\n\nUse the left and right arrow key " +        "or the left and right mouse buttons to " +       "move man under the fallen ball." ;    lblInstruction.Text += "\n\ nChoose the game difficulty level by pressing " +       "the left or right mouse button." ;   lblInstruction.Text += "\n\ nClick Start button to start the game." +        "\nClick Stop button to stop the game." ;    lblDifficulty.Text = Difficulty.ToString();} &#124;

Save and run the program to see what shown in Figure 6.8. |
| Step 5 | The Difficulty variable is used to determine how fast the ball falls (the higher the difficulty, the higher the speed of the ball falls). To change the difficulty, the user can click on one of the arrow keys. The code to do so is placed in the Click event procedure of the btnLeft and btnRight buttons: 

&#124; 12345678910111213141516171819202122 &#124; private void btnLeft_Click_1( object sender, EventArgs e){   if (StatusGame == "Starting" ) // Decreases difficulty level    {        Difficulty -= 1;        if (Difficulty < 1)            Difficulty = 1;        lblDifficulty.Text = Difficulty.ToString();    }}private void btnRight_Click_1( object sender, EventArgs e){    if (StatusGame == "Starting" ) // Increases difficulty level                {        Difficulty += 1;        if (Difficulty > 10)            Difficulty = 10;        lblDifficulty.Text = Difficulty.ToString();    }} &#124;

![](Image00037.jpg)Figure 6.8 When the program first starts, it displays game description and instructions.Save and run program. Make sure the arrow keys work correctly. Make sure the difficulty level is between values ​​1 and 10.![](Image00043.jpg)Figure 6.9 To change the difficulty, the user can click on one of the arrow keys. |
| Step 6 | After the game difficulty level is set, the next step is to click on Start button so the game can start. So, you need a code to get from the "Starting" state to the "Playing" state. When Start button is clicked on the "Starting" state, these steps need to be carried out: 
*   Change StatusGame to "Playing".
*   Clean the screen.
*   Initialize the score and remaining time.
*   Place man on the bottom area of the screen.
*   Place bird and ball on the top area of the screen randomly.
*   Drop ball.

There is a lot that needs to be done here, you will do it step by step. First, you will initialize the variables and position man at the bottom of the screen.Two variables are used to control the game. RemainingTime is an integer value that tells how much time is left in the game (in milliseconds). You choose the game to last, for example, in 60 seconds. The Score tells how many balls man caught. PanelGame is a graphics region which is a place for games.Add the following form level variable declarations:

&#124; 123 &#124; int RemainingTime;int Score;Graphics PanelGame; &#124;

In the code, you specify width ( ManW ) and height ( ManH ). Man is positioned below the screen, around the middle. The ManX and ManY variables tell where man is. ManDeltaX is used to tell how far man moved by pressing a button or clicking the mouse. All of these variables are useful for seeing whether or not man can catch the dropped ball. Add the following form level variable declarations:

&#124; 1 &#124; int ManW, ManH, ManX, ManY, ManDeltaX; &#124;

 |
| Step 7 | Add this code to the Click event procedure from the btnStart control: 

&#124; 1234567891011121314151617181920 &#124; private void btnStart_Click( object sender, EventArgs e){    //Start button clicked    StatusGame = "Playing" ;    lblInstruction.Visible = false ;    PanelGame = pnlGame.CreateGraphics();    PanelGame.Clear(Color.Gold); //time/score    RemainingTime = 60 * 1000;  //milliseconds    Score = 0;    DisplayTimeScore();    //Man    ManW = picMan.Width;    ManH = picMan.Height;    ManDeltaX = 10;    ManX = 375;    ManY = pnlGame.Height - ManH;    PanelGame.DrawImage(picMan.Image, ManX, ManY);} &#124;

Here, the panel is cleared and the variables are set so that man is positioned below and around the center of screen.Pay attention to the following line of code: DisplayTimeScore() . This line calls a function that updates the displayed value for RemainingTime and Score . Add this function at the end of your program:

&#124; 12345 &#124; private void DisplayTimeScore(){    lblTime.Text = (RemainingTime / 1000).ToString();    lblScore.Text = Score.ToString();} &#124;

 |
| Step 8 | Save and run the program. Select the level of difficulty of the game (for example 3). Click Start button to look like the figure below.![](Image00044.jpg)Figure 6.10 Man is positioned below and around the center of screen |
| Step 9 | The final initialization step is to place bird and ball randomly on the screen. You specify the width and height of bird ( BirdW and BirdH ) and ball length and height ( BallW and BallH ). This will help determine whether man caught the ball or not. Add the following form level variable declarations: 

&#124; 123 &#124; int BirdW, BirdH, BirdX;int BallW, BallH, BallX, BallY;Random MyRandom = new Random(); &#124;

BirdX is the x-position of the bird (zero position y, above the screen). Ball has position ( BallX , BallY ). MyRandom is needed for generating random numbers. |
| Step 10 | Add the following modified code to Click event procedure of btnStart control: 

&#124; 123456789101112131415161718192021222324252626272829 &#124; private void btnStart_Click( object sender, EventArgs e){    //Start button clicked    StatusGame = "Playing" ;    lblInstruction.Visible = false ;    PanelGame = pnlGame.CreateGraphics();    PanelGame.Clear(Color.Gold); //time/score    RemainingTime = 60 * 1000;  //milliseconds    Score = 0;    DisplayTimeScore();    //Man    ManW = picMan.Width;    ManH = picMan.Height;    ManDeltaX = 10;    ManX = 375;    ManY = pnlGame.Height - ManH;    PanelGame.DrawImage(picMan.Image, ManX, ManY);    //Bird    BirdW = picBird.Width;    BirdH = picBird.Height;    //Ball    BallW = picBall.Width + 10;    BallH = picBall.Height;    PlaceBirdAndBall();} &#124;

 |
| Step 11 | The code in Step 10 uses a separate subroutine ( PlaceBirdAndBall ) to randomly position the bird and the ball on the screen. Add this subroutine to your program: 

&#124; 12345678 &#124; private void PlaceBirdAndBall(){    BirdX = MyRandom.Next(pnlGame.Width - BirdW);    PanelGame.DrawImage(picBird.Image, BirdX, 0);   BallX = BirdX + Convert.ToInt32(0.5 * (BirdW - BallW));    BallY = BirdH + 10;    PanelGame.DrawImage(picBall.Image, BallX, BallY);} &#124;

 |
| Step 12 | Save and run the program. Set the Difficulty (for example 3). Click the Start button to see:![](Image00045.jpg)Figure 6.11 The final initialization step is to place bird and ball randomly on the screen.You still need the code to drop the ball and move man along the bottom of the screen. You will write the code shortly. But, first, you need to do something to stop the program. |
| Stop 13 | One last thing that can be done when the game is in the "Starting" state is to click the Stop button. This will stop the program. The code here is quite simple. Add the following code to the Click event procedure of btnStop button: 

&#124; 12345 &#124; private void btnStop_Click( object sender, EventArgs e){    if (StatusGame == "Starting" )        this .Close();} &#124;

 |
| Step 14 | Save and run the program. Make sure Stop button works properly. This completes the code to move the "Starting" game status to "Playing" state. Now, you will write the code to move man along the bottom of the screen. |
| Step 15 | When the program starts, the ball will be dropped. User will move man along the bottom of the screen to try to catch the dropped ball. Here, you will write code that drops ball. A variable named BallSpeed will determine how fast the ball will be dropped. Add the following form-level declaration: 

&#124; 1 &#124; int BallSpeed; &#124;

You assign BallSpeed based on the Difficulty value:

&#124; 1 &#124; BallSpeed = 0.5 * Difficulty + 5 &#124;

Timer control ( timerGame ) is used to control ball movement. Add the modified code to the Click event procedure of btnStart :

&#124; 12345678910111213141516171819202122232425262627282930313233 &#124; private void btnStart_Click( object sender, EventArgs e){    //Start button clicked    StatusGame = "Playing" ;    lblInstruction.Visible = false ;    PanelGame = pnlGame.CreateGraphics();    PanelGame.Clear(Color.Gold); //time/score    RemainingTime = 60 * 1000;  //milliseconds    Score = 0;    DisplayTimeScore();    //Man    ManW = picMan.Width;    ManH = picMan.Height;    ManDeltaX = 10;    ManX = 375;    ManY = pnlGame.Height - ManH;    PanelGame.DrawImage(picMan.Image, ManX, ManY);    //Bird    BirdW = picBird.Width;    BirdH = picBird.Height;    //Ball    BallW = picBall.Width + 10;    BallH = picBall.Height;    PlaceBirdAndBall();    //Start timer    BallSpeed = Convert.ToInt32(0.5 * Difficulty) + 5;    timerGame.Start();} &#124;

 |
| Step 16 | The ball position is updated in the Tick event procedure of timerGame using the following code: 

&#124; 123456 &#124; private void timerGame_Tick( object sender, EventArgs e){   ClearBall();    BallY = BallY + BallSpeed;    PanelGame.DrawImage(picBall.Image, BallX, BallY);} &#124;

The code uses the new subroutine ClearBall which removes the ball from its current location before moving it to a new position. Add this subroutine to your program:

&#124; 12345 &#124; private void ClearBall(){    PanelGame.FillRectangle(Brushes.Gold, BallX, BallY,        BallW + 5, BallH + 5);} &#124;

 |
| Step 17 | Save and run program. Then click on Start button. Now, the ball is dropped in a random position:![](Image00046.jpg)Figure 6.12 Ball is dropped in a random position:But the ball still falls until it disappears across the screen. You need two more pieces of code: one to move man under the ball and another one to determine whether man can catch the falling ball or not. |
| Step 18 | The aim of the game is to move man under the falling ball so he can catch it. Man can be moved using two different methods: First, he can be moved using the left and right buttons on the keypad. With each key press, you change ManX to the extent that ManDeltaX is in a certain direction. You use a new variable KeyPressed to track which key is being pressed. Add the following declarations to the form-level declaration: 

&#124; 1 &#124; String KeyPressed = "Empty" ; &#124;

You detect a key presses on KeyDown procedure of form with the following code:

&#124; 12345678 &#124; private void FormCatchingBall_KeyDown( object sender, KeyEventArgs e){   //Check which arry key is pressed to move man    if (e.KeyCode == Keys.Left)        KeyPressed = "Left" ;    else if (e.KeyCode == Keys.Right)        KeyPressed = "Right" ;} &#124;

 |
| Step 19 | You also need a code to notify when the key is released. This code is placed into the KeyUp event procedure of the form: 

&#124; 1234 &#124; private void FormCatchingBall_KeyUp( object sender, KeyEventArgs e){    KeyPressed = "Empty" ;} &#124;

 |
| Step 20 | Add the modified code of Tick event procedure of timerGame control: 

&#124; 1234567891011121314151617181920212223 &#124; private void timerGame_Tick( object sender, EventArgs e){   ClearBall();    BallY = BallY + BallSpeed;    PanelGame.DrawImage(picBall.Image, BallX, BallY);    //Move man    ClearMan();    if (KeyPressed == "Left" )    {        ManX = ManX - ManDeltaX;        if (ManX < 0)            ManX = 0;    }    else if (KeyPressed == "Right" )    {        ManX = ManX + ManDeltaX;        if (ManX > (pnlGame.Width - ManW))            ManX = pnlGame.Width - ManW;     }    PanelGame.DrawImage(picMan.Image, ManX, ManY);} &#124;

Just like the code that moves the ball, this code uses another subroutine ClearMan to delete man from its current location. Add the following subroutine:

&#124; 12345 &#124; private void ClearMan(){    PanelGame.FillRectangle(Brushes.Gold, ManX,        ManY, ManW + 50, ManH);} &#124;

 |
| Step 21 | Save and run the project. Click on the Start button. Make man move by pressing left and right arrow keys:![](Image00047.jpg)Figure 6.13 User now can move man to left and right using arrow keys |
| Step 22 | Now, you will write the code for the second method to move man: use the left and right buttons on the mouse. Define a form level variable to track which button is clicked ( ButtonClicked ): 

&#124; 1 &#124; String ButtonClicked = "Empty" ; &#124;

Now, add this code to the MouseDown event procedure of pnlGame :

&#124; 1234567 &#124; private void pnlGame_MouseDown( object sender, MouseEventArgs e){   if (e.Button == MouseButtons.Left)        ButtonClicked = "Left" ;    else if (e.Button == MouseButtons.Right)       ButtonClicked = "Right" ;} &#124;

With this code, when the mouse is on the game panel, the left and right mouse buttons will replace the click action of the left and right arrow keys. Add the following code to the MouseUp event procedure from pnlGame :

&#124; 1234 &#124; private void pnlGame_MouseUp( object sender, MouseEventArgs e){    ButtonClicked = "Empty" ;} &#124;

 |
| Step 23 | Then, add the modified code to the Tick event procedure of timerGame control: 

&#124; 1234567891011121314151617181920212223 &#124; private void timerGame_Tick( object sender, EventArgs e){   ClearBall();    BallY = BallY + BallSpeed;    PanelGame.DrawImage(picBall.Image, BallX, BallY);    //Move man    ClearMan();    if (KeyPressed == "Left" &#124;&#124; ButtonClicked == "Left " )    {        ManX = ManX - ManDeltaX;        if (ManX < 0)            ManX = 0;    }    else if (KeyPressed == "Right" &#124;&#124; ButtonClicked == "Right " )    {        ManX = ManX + ManDeltaX;        if (ManX > (pnlGame.Width - ManW))            ManX = pnlGame.Width - ManW;     }    PanelGame.DrawImage(picMan.Image, ManX, ManY);} &#124;

 |
| Step 25 | Save and run program. Make sure you can now move man with the left and right arrow keys and with both mouse buttons:![](Image00048.jpg)Figure 6.14 User now can now move man with the left and right arrow keys and with both mouse buttons |
| Step 26 | When the ball approaches the bottom of the screen, you need to see if man can catch it. The code to check this is in the Tick event procedure of timerGame . You need to do two things: 
*   Check whether the ball is caught. If so, the ball is cleared and the score is incremented and the bird and ball appear again at a random location at the top of the screen.
*   Check whether the ball has reached the same vertical position as man and has not been caught. If yes, bird and ball reappears.

How do you know when man catches ball? You need to see if man's graphics collide with the ball graphics. The inspection could not be carried out until the ball overlaps man. This happens when: BallY + BallH> ManY .You will use a boolean variable ( Passed ) to see this. After this condition is met, you can see that man collides with ball (or catches ball) when:ManX + ManW> BallX and ManX <BallX + BallW .This says that the right side of man must be "more right" than the left side of the ball and the left side of man must be "more left" than the right side of the bal. Another boolean variable ( Collision ) is used to check this condition.Declare these two new variables:

&#124; 1 &#124; bool Passed, Collision; &#124;

Add this modified code from the Tick event procedure of timerGame :

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041 &#124; private void timerGame_Tick( object sender, EventArgs e){   ClearBall();    BallY = BallY + BallSpeed;    PanelGame.DrawImage(picBall.Image, BallX, BallY);    //Move man    ClearMan();    if (KeyPressed == "Left" &#124;&#124; ButtonClicked == "Left " )    {        ManX = ManX - ManDeltaX;        if (ManX < 0)            ManX = 0;    }    else if (KeyPressed == "Right" &#124;&#124; ButtonClicked == "Right " )    {        ManX = ManX + ManDeltaX;        if (ManX > (pnlGame.Width - ManW))            ManX = pnlGame.Width - ManW;     }    PanelGame.DrawImage(picMan.Image, ManX, ManY);    //Checks whether ball collides with or passes man    Passed = false ;    Collision = false ;    if (BallY + BallH > ManY)    {        Passed = true ;        if (ManX + ManW > BallX && ManX < BallX + BallW)            Collision = true ;        if (Passed)            if (Collision)                Score += 1;        ClearBird();        ClearBall();        PlaceBirdAndBall();    }    DisplayTimeScore();} &#124;

 |
| Step 27 | You now understand the steps implemented. In particular, pay attention to how the new bird is positioned after Passed is True (and how the score is incremented if the Collision is True ). This new code requires a new subroutine called ClearBird which removes bird from their current position: 

&#124; 12345 &#124; private void ClearBird(){    PanelGame.FillRectangle(Brushes.Gold, BirdX, 0,        BirdW + 30, BirdH + 30);} &#124;

 |
| Step 28 | Save and run the program. Change the difficulty level if desired. Click on Start button. Now you can move man under the falling ball, and the score will increase and the bird appears again in the next random position. If man fails to catch the ball, the score will not be incremented and the bird will reappear in the next random position:![](Image00049.jpg)Figure 6.15 User can move man under the falling ball, and the score will increase and the bird appears again in the next random position. |
| Step 29 | You are almost done. With the current code, you can play the game as long as you like. Note that remaining time displayed is still 60\. You need to implement logic that ends the game after 60 seconds (and updates the remaining time displayed).To do this, add this modified code of Tick event procedure to timerGame control: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556 &#124; private void timerGame_Tick( object sender, EventArgs e){   ClearBall();    BallY = BallY + BallSpeed;    PanelGame.DrawImage(picBall.Image, BallX, BallY);    //Move man    ClearMan();    if (KeyPressed == "Left" &#124;&#124; ButtonClicked == "Left " )    {        ManX = ManX - ManDeltaX;        if (ManX < 0)            ManX = 0;    }    else if (KeyPressed == "Right" &#124;&#124; ButtonClicked == "Right " )    {        ManX = ManX + ManDeltaX;        if (ManX > (pnlGame.Width - ManW))            ManX = pnlGame.Width - ManW;     }    PanelGame.DrawImage(picMan.Image, ManX, ManY);    //Checks whether ball collides with or passes man    Passed = false ;    Collision = false ;    if (BallY + BallH > ManY)    {        Passed = true ;        if (ManX + ManW > BallX && ManX < BallX + BallW)            Collision = true ;        if (Passed)            if (Collision)                Score += 1;        ClearBird();        ClearBall();        PlaceBirdAndBall();    }    //Updates time    RemainingTime = RemainingTime - timerGame.Interval;    DisplayTimeScore();    if (RemainingTime == 0)    {        ClearBird();        ClearBall();        ClearMan();        timerGame.Stop();        MessageBox.Show( "You successfully catch "            + Score.ToString() + " balls." , "Game Over" );        StatusGame = "Starting" ;    }} &#124;

In this new code, with each Tick event, RemainingTime will be decremented by the Interval . After RemainingTime is zero, then the graphical elements (bird, ball, and man) will be removed from the screen, the timer is deactivated, and the result is displayed in a message box. |
| Step 30 | Save and run program. Click on the Start button. Time will count down:![](Image00050.jpg)Figure 6.16 After RemainingTime is zero, then the graphical elements (bird, ball, and man) will be removed from the screen, the timer is deactivated, and the result is displayed in a message box |
| Step 31 | One more last that needs to be changed. You can stop the program before 60 seconds are finished. To do this, you click the Stop button when the game is in "Playing" state. The code is simple. Add the modified code of the Click event procedure of btnStop control: 

&#124; 123456789101112131415 &#124; private void btnStop_Click( object sender, EventArgs e){    if (StatusGame == "Starting" )        this .Close();    else    {        //Stop button clicked when game played        timerGame.Stop();        StatusGame = "Starting" ;        MessageBox.Show( "You quit the game." , "Game Over" );        ClearMan();        ClearBird();        ClearBall();    }} &#124;

 |
| Step 32 | Save and run program. Click on Start button, and then click on the Stop button. You will see:![](Image00051.jpg)Figure 6.17 User can stop program before 60 seconds is up |
|  |  |

| Form1.cs |
| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197198199200201202203204205206207208209210211212213214215216217218219220221222223224225226227228229230231232234235236237238239240241242243244245246247248249250251252253254255256257258 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;namespace Horse_Racing{    public partial class FormCatchingBall : Form    {        int Difficulty;        String StatusGame;        int RemainingTime;        int Score;        Graphics PanelGame;        int ManW, ManH, ManX, ManY, ManDeltaX;        int BirdW, BirdH, BirdX;        int BallW, BallH, BallX, BallY;        Random MyRandom = new Random();        int BallSpeed;        String KeyPressed = "Empty" ;        String ButtonClicked = "Empty" ;        bool Passed, Collision;        private void timerGame_Tick( object sender, EventArgs e)        {            ClearBall();            BallY = BallY + BallSpeed;            PanelGame.DrawImage(picBall.Image, BallX, BallY);            //Move man            ClearMan();            if (KeyPressed == "Left" &#124;&#124; ButtonClicked == "Left" )            {                ManX = ManX - ManDeltaX;                if (ManX < 0)                    ManX = 0;            }            else if (KeyPressed == "Right" &#124;&#124; ButtonClicked == "Right" )            {                ManX = ManX + ManDeltaX;                if (ManX > (pnlGame.Width - ManW))                    ManX = pnlGame.Width - ManW;            }            PanelGame.DrawImage(picMan.Image, ManX, ManY);            //Checks whether ball collides with or passes man            Passed = false ;            Collision = false ;            if (BallY + BallH > ManY)            {                Passed = true ;                if (ManX + ManW > BallX && ManX < BallX + BallW)                    Collision = true ;                if (Passed)                    if (Collision)                        Score += 1;                ClearBird();                ClearBall();                PlaceBirdAndBall();            }            //Updates time            RemainingTime = RemainingTime - timerGame.Interval;            DisplayTimeScore();            if (RemainingTime == 0)            {                ClearBird();                ClearBall();                ClearMan();                timerGame.Stop();                MessageBox.Show( "You successfully catch "                    + Score.ToString() + " balls." , "Game Over" );                StatusGame = "Starting" ;            }        }        private void ClearBird()        {            PanelGame.FillRectangle(Brushes.Gold, BirdX, 0, BirdW + 30, BirdH + 30);        }        private void ClearMan()        {            PanelGame.FillRectangle(Brushes.Gold, ManX, ManY, ManW + 50, ManH);        }        private void FormCatchingBall_KeyDown( object sender, KeyEventArgs e)        {            //Check which arry key is pressed to move man            if (e.KeyCode == Keys.Left)                KeyPressed = "Left" ;            else if (e.KeyCode == Keys.Right)                KeyPressed = "Right" ;        }        private void FormCatchingBall_KeyUp( object sender, KeyEventArgs e)        {            KeyPressed = "Empty" ;        }        private void pnlGame_MouseDown( object sender, MouseEventArgs e)        {            if (e.Button == MouseButtons.Left)                ButtonClicked = "Left" ;            else if (e.Button == MouseButtons.Right)                ButtonClicked = "Right" ;        }        private void pnlGame_MouseUp( object sender, MouseEventArgs e)        {            ButtonClicked = "Empty" ;        }        private void ClearBall()        {            PanelGame. FillRectangle(Brushes.Gold, BallX, BallY, BallW + 5, BallH + 5);        }        private void btnStop_Click( object sender, EventArgs e)        {            if (StatusGame == "Starting" )                this .Close();            else            {                //Stop button clicked when game played                timerGame.Stop();                StatusGame = "Starting" ;                MessageBox.Show( "You quit the game." , "Game Over" );                ClearMan();                ClearBird();                ClearBall();            }        }        private void btnStart_Click( object sender, EventArgs e)        {            //Start button clicked            StatusGame = "Playing" ;            lblInstruction.Visible = false ;            PanelGame = pnlGame.CreateGraphics();            PanelGame.Clear(Color.Gold); //time/score            RemainingTime = 60 * 1000;  //milliseconds            Score = 0;            DisplayTimeScore();            //Man            ManW = picMan.Width;            ManH = picMan.Height;            ManDeltaX = 10;            ManX = 375;            ManY = pnlGame.Height - ManH;            PanelGame.DrawImage(picMan.Image, ManX, ManY);            //Bird            BirdW = picBird.Width;            BirdH = picBird.Height;            //Ball            BallW = picBall.Width + 10;            BallH = picBall.Height;            PlaceBirdAndBall();            //Start timer            BallSpeed = Convert.ToInt32(0.5 * Difficulty) + 5;            timerGame.Start();            pnlGame.Focus();        }        private void PlaceBirdAndBall()        {            BirdX = MyRandom.Next(pnlGame.Width - BirdW);            PanelGame.DrawImage(picBird.Image, BirdX, 0);            BallX = BirdX + Convert.ToInt32(0.5 * (BirdW - BallW));            BallY = BirdH + 10;            PanelGame.DrawImage(picBall.Image, BallX, BallY);        }        private void DisplayTimeScore()        {            lblTime.Text = (RemainingTime / 1000).ToString();            lblScore.Text = Score.ToString();        }        public FormCatchingBall ()        {            InitializeComponent();        }        private void FormCatchingBall_Load( object sender, EventArgs e)        {            this .KeyPreview = true ;            //Catching Ball Game            Difficulty = 1;            StatusGame = "Starting" ;            lblInstruction.Text = "CATCHING BALL GAME \n\n" ;            lblInstruction.Text += "In this game, you will try to \n" +                "catch as many as possible fallen ball." ;            lblInstruction.Text += "\n\nUse the left and right arrow key " +                "or the left and right mouse buttons to " +                "move man under the fallen ball." ;            lblInstruction.Text += "\n\nChoose the game difficulty level by pressing " +                "the left or right mouse button." ;            lblInstruction.Text += "\n\nClick Start button to start the game." +                "\nClick Stop button to stop the game." ;            lblDifficulty.Text = Difficulty.ToString();            PanelGame = pnlGame.CreateGraphics();        }        private void btnLeft_Click_1( object sender, EventArgs e)        {            if (StatusGame == "Starting" ) // Decreases difficulty level            {                Difficulty -= 1;                if (Difficulty < 1)                    Difficulty = 1;                lblDifficulty.Text = Difficulty.ToString();            }        }        private void btnRight_Click_1( object sender, EventArgs e)        {            if (StatusGame == "Starting" ) // Increasesdifficulty level            {                Difficulty += 1;                if (Difficulty > 10)                    Difficulty = 10;                lblDifficulty.Text = Difficulty.ToString();            }        }    }} |
|  |  |

TUTORIAL 6

SMART TIC TAC TOE

In this tutorial, you will build Smart Tic Tac Toe game. That said, this is the first game ever programmed on a computer and one that had been programmed by Bill Gates himself when he was a teenager while attending Lakeside School in Seattle. The aim of this game is to win the game on a 3 x 3 grid with the victory of three identical symbols (X or O) on horizontal, diagonal, or vertical lines. The players will play alternately. In this game given two game options: player 1 against player 2 or human player against computer. A smart but simple strategy will be developed for computer logic to be a formidable opponent for humans.

| Description |
| Run the project (press <F5>). The game will be displayed in the 'stop' state, the grid will be cleared and waiting for you to choose game options (one or two players and, if one player, who plays first and how smart the computer will oppose).![](Image00052.jpg)Figure 6.1 All controls used in Smart Tic Tac Toe game project![](Image00053.jpg)Figure 6.2 The game is at “stop” stateYou can choose the two players option and then press Start Game button:![](Image00054.jpg)Figure 6.3 User chooses two players optionIn addition, you can choose the option of one player with a random computer or a smart computer opponent:![](Image00055.jpg)Figure 6.4 User chooses one player option |
| Tutorial Steps |
| Step 1 | You will build Smart Tic Tac Toe game project. Start a new project in Visual C#. Once created, you are advised to save the project immediately with the name you choose. This will create the folders and file structure that your project requires.![](Image00056.jpg)Figure 6.5 All controls user and their positions formYou need 14 label controls (with the AutoSize property set to False so that the size can be changed and the BorderStyle property temporarily set to FixedSingle to see edges) on the left side of the form. Place the three group boxes on the right side, along with the two control buttons. Place two radio button controls in each group box. The form will look as shown in Figure 6.5.Label controls are used to display messages, to display symbols (X and O), and to form a grid. The radio buttons are used to set game options. Buttons (one to start the game and one to end the game) are used to control game operations. |
| Step 2 | Set control properties using the Properties window: 

&#124; A number of properties of the Form1 object &#124;
&#124; Name &#124; FormTicTacToe &#124;
&#124; BackColor &#124; White &#124;
&#124; Text &#124; Smart Tic Tac Toe &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label1 object &#124;
&#124; Name &#124; lblMessage &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; Crimson &#124;
&#124; ForeColor &#124; White &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Font &#124; Bold, 24 &#124;
&#124; Text &#124; X’s Turn &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label2 object &#124;
&#124; Name &#124; lblBox1 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label3 object &#124;
&#124; Name &#124; lblBox2 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label4 object &#124;
&#124; Name &#124; lblBox3 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label5 object &#124;
&#124; Name &#124; lblBox4 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label6 object &#124;
&#124; Name &#124; lblBox5 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label7 object &#124;
&#124; Name &#124; lblBox6 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label8 object &#124;
&#124; Name &#124; lblBox7 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label8 object &#124;
&#124; Name &#124; lblBox7 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label9 object &#124;
&#124; Name &#124; lblBox8 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label10 object &#124;
&#124; Name &#124; lblBox9 &#124;
&#124; AutoSize &#124; False &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Font Size &#124; 48 &#124;
&#124; Text &#124; X &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label11 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; Orange &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label12 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; Orange &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label13 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; Orange &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Label14 object &#124;
&#124; AutoSize &#124; False &#124;
&#124; BackColor &#124; Orange &#124;
&#124; BorderStyle &#124; None &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox1 object &#124;
&#124; Name &#124; grpPlayer &#124;
&#124; BackColor &#124; DeepPink &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton1 object &#124;
&#124; Name &#124; rdoTwoPlayers &#124;
&#124; ForeColor &#124; White &#124;
&#124; Font Size &#124; 9 &#124;
&#124; Text &#124; Two Players &#124;
&#124; Checked &#124; True &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton2 object &#124;
&#124; Name &#124; rdoOnePlayer &#124;
&#124; ForeColor &#124; White &#124;
&#124; Font Size &#124; 9 &#124;
&#124; Text &#124; One Player &#124;
&#124; Checked &#124; True &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox2 object &#124;
&#124; Name &#124; grpFirst &#124;
&#124; BackColor &#124; DeepPink &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton3 object &#124;
&#124; Name &#124; rdoYouFirst &#124;
&#124; ForeColor &#124; White &#124;
&#124; Font Size &#124; 9 &#124;
&#124; Text &#124; You Play First &#124;
&#124; Checked &#124; True &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton4 object &#124;
&#124; Name &#124; rdoComputerFirst &#124;
&#124; ForeColor &#124; White &#124;
&#124; Font Size &#124; 9 &#124;
&#124; Text &#124; Computer Play First &#124;
&#124; Checked &#124; True &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the GroupBox3 object &#124;
&#124; Name &#124; grpComputer &#124;
&#124; BackColor &#124; DeepPink &#124;
&#124; Text &#124; [Empty] &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton5 object &#124;
&#124; Name &#124; rdoRandom &#124;
&#124; ForeColor &#124; White &#124;
&#124; Font Size &#124; 9 &#124;
&#124; Text &#124; Random Computer &#124;
&#124; Checked &#124; True &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the RadioButton6 object &#124;
&#124; Name &#124; rdoSmart &#124;
&#124; ForeColor &#124; White &#124;
&#124; Font Size &#124; 9 &#124;
&#124; Text &#124; Smart Computer &#124;
&#124; Checked &#124; True &#124;
&#124;  &#124;  &#124;

![](Image00057.jpg)Figure 6.6 Form after properties setting done

&#124; A number of properties of the Button1 object &#124;
&#124; Name &#124; btnStartStop &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Start Game &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Button2 object &#124;
&#124; Name &#124; btnExit &#124;
&#124; Font Size &#124; 10 &#124;
&#124; Text &#124; Exit &#124;
&#124;  &#124;  &#124;

When finished, the form will look like as shown in Figure 6.6.This completes the form design. You will start writing the code for this game. You will write the code in several stages. As a first step, you will write the code that starts the game and sets the 'stop' state. Then, you will write the code for the 'playing' state after Start Game button is clicked. During the code development process, you will modify certain methods several times before arriving at the final process. |
| Step 3 | Every time you start a project, a number of initializations are needed. In this case, all initializations are placed in the Load event method of the form.To simplify the task, you will specify an array of controls ( LabelArr ) for the nine label controls that are used to display X and O marks on the grid. This array is defined in the form-level declaration: 

&#124; 1 &#124; Label[] LabelArr = new Label[9]; &#124;

![](Image00058.jpg)Figure 6.7 The game is in “stop” stateAssignments are performed in the Load event method of FormTicTacToe . You also create a message in lblMessage control and clear the label controls that display the symbol. Finally, you want the game to be initialized in Two Players mode so you disable two group boxes related to options for single player mode:

&#124; 123456789101112131415161718192021 &#124; private void FormTicTacToe_Load( object sender, EventArgs e){    // Fills array    LabelArr[0] = lblBox1;    LabelArr[1] = lblBox2;    LabelArr[2] = lblBox3;    LabelArr[3] = lblBox4;    LabelArr[4] = lblBox5;    LabelArr[5] = lblBox6;    LabelArr[6] = lblBox7;    LabelArr[7] = lblBox8;    LabelArr[8] = lblBox9;    // Clears labels    for ( int i = 0; i < 9; i++)        LabelArr[i].Text = "" ;    lblMessage.Text = "Game Stopped" ;    grpFirst.Enabled = false ;    grpComputer.Enabled = false ;} &#124;

 |
| Step 4 | Save and run the project to make sure everything works correctly, as shown in Figure 6.8. |
| Step 5 | As desired, the game is initialized in Two Players mode. You have two choices at this point: clicking btnStartStop (Start Game button) or clicking btnExit . You can also change to One Player mode. You will handle this later.The code to exit the program is quite simple. Click event from the control btnExit : 

&#124; 1234 &#124; private void btnExit_Click( object sender, EventArgs e){    this .Close();} &#124;

It only says that whenever the Exit button is clicked, the project will close. Add this code to your project.The code for the btnStartStop button is much more complex. You will write it in several stages. First, you will switch the code to shift the game from the stop state to the playing state. |
| Step 6 | When user clicks Start Game button in the "stop" state, several things happen to switch the Tic Tac Toe game to the "play" state: 
*   Change Text property of btnStartStop to Stop Game .
*   Disable group boxes (do not allow selection of options when playing).
*   Disable Exit button.
*   Set X's turn (because the X symbol is always used first).
*   Clear label controls that display symbols.
*   Allow user to enter symbols on the grid.

You create three variables in the form-level declaration to help track a number of situations in the game:

&#124; 123 &#124; bool XTurn;bool Clickable = false ;int NumberOfClick; &#124;

If XTurn is true , then the X symbol will appear, otherwise the O symbol will appear. Clickable is used to determine whether user can click on label controls. If this variable is true , if the game is in progress. Instead, it is false (initial value) when the game stops. NumberOfClick tracks how many grid labels have been clicked (maximum 9).![](Image00059.jpg)Figure 6.9 The game is in “playing” stateThe code for the Click event of btnStartStop that implements the steps above is given below:

&#124; 1234567891011121314151617 &#124; private void btnStartStop_Click( object sender, EventArgs e){    btnStartStop.Text = "Stop Game" ;    grpPlayer.Enabled = false ;    grpFirst.Enabled = false ;    grpComputer.Enabled = false ;    btnExit.Enabled = false ;    XTurn = true ;    lblMessage.Text = "X's Turn" ;    // Clears LabelArr    for ( int i = 0; i < 9; i++)        LabelArr[i].Text = "" ;    Clickable = true ;    NumberOfClick = 0;} &#124;

 |
| Step 7 | Save and run the project. Click Start Game button and the game will switch to the "playing" state, as shown in Figure 6.9.The game waits until the first player clicks on one of the grid locations (you will write the code in a minute). Notice Stop Game button doesn't do anything for now. |
| Step 8 | When user clicks Stop Game button in "playing" state with two-players mode, several things must occur to switch Tic Tac Toe game to the "stop" state: 
*   Change the Text property of btnStartStop to Start Game .
*   Display “Game Ends” message.
*   Enable grpPlayer .
*   Enable grpFirst and grpComputer with one player mode.
*   Enable Exit button.
*   Set Clickable to false .

The modified code that performs these steps is placed in the Click event method of the btnStartStop control:

&#124; 12345678910111213141516171819202122232425262728293031323334 &#124; private void btnStartStop_Click( object sender, EventArgs e){    if (btnStartStop.Text == "Start Game" )    {        btnStartStop.Text = "Stop Game" ;        grpPlayer.Enabled = false ;        grpFirst.Enabled = false ;        grpComputer.Enabled = false ;        btnExit.Enabled = false ;        XTurn = true ;        lblMessage.Text = "X's Turn" ;        // Clears LabelArr        for ( int i = 0; i < 9; i++)            LabelArr[i].Text = "" ;        Clickable = true ;        NumberOfClick = 0;    else    {        btnStartStop.Text = "Start Game" ;        lblMessage.Text = "Game Ends" ;        grpPlayer.Enabled = true ;        if (rdoOnePlayer.Checked)        {            grpFirst.Enabled = true ;            grpComputer.Enabled = true ;        }        btnExit.Enabled = true ;        Clickable = false ;    }} &#124;

 |
| Step 9 | Save and run project. You can now move from the "stop" to the "playing" state and vice versa. When stop, make sure the group boxes are enabled for one and two player options.![](Image00060.jpg)Figure 6.10 User now can move from the "stop" to the "playing" state and vice versaYou will write the code for the two player option, by first writing the code to display the symbol on the grid. |
| Step 10 | In the Tic Tac Toe game with a two player option, when a player clicks on a box on the grid, an appropriate symbol (X or O) will appear. After that, you then need to see if someone wins the game. If there is no win, and there is still an empty box, the turn switch to another player.So, when a grid box is clicked, these steps need to be done: 
*   Verify that there is no symbol on the grid before.
*   Increment NumberOfClick .
*   Place the right symbol (X if XTurn is true , otherwise O).
*   Switch turn to the next player (not required if there is a win or a draw).
*   Check for winning. If there is a win, the winner is announced and the game is stopped.
*   Check if NumberOfClick = 9 (board is full but no win). If yes, the draw is announced and the game is stopped.

The code to perform these steps will be placed in the method named lblBox_Click . This method was created to handle the Click event for the nine label controls used on the grid ( lblBox1 , lblBox2 , lblBox3 , lblBox4 , lblBox5 , lblBox6 , lblBox7 , lblBox8 , and lblBox9 .Add this method ( lblBox_Click ) to your project. This implements the steps needed to receive symbols on the grid:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849 &#124; private void lblBox_Click( object sender, EventArgs e){    String WhoWin = "" ;    int i;    if (Clickable)    {        // See which box clicked        Label BoxClicked;        BoxClicked = (Label) sender;        // Last digit is the number extracted        i = Convert.ToInt32(            BoxClicked. Name[BoxClicked.Name.Length - 1].ToString()) - 1;        // If it has been clicked, exit        if (LabelArr[i].Text != "" )            return ;        NumberOfClick++;        if (XTurn)        {            LabelArr[i].Text = "X" ;            XTurn = false ;            lblMessage.Text = "O's Turn" ;        }        else        {            LabelArr[i].Text = "O" ;            XTurn = true ;            lblMessage.Text = "X's Turn" ;        }        if (WhoWin != "" )        {            lblMessage.Text = WhoWin + " wins” ;            btnStartStop.PerformClick();            return ;        }        else if (NumberOfClick == 9)        {            // Draw            lblMessage.Text = "Game is draw!" ;            btnStartStop.PerformClick();            return ;        }    }} &#124;

![](Image00061.jpg)Figure 6.11 After all grid locations are filled with symbols, the game returns to the "stop" stateLook at this code. Clicking on one of the nine label controls on the grid will invoke this method. The first part of the code determines the index element of the label controls array ( LabelArr ) that is clicked (i). This index is the last character in the label name that is converted to numeric. If there is a symbol (not empty), then the method is complete. If it is empty, the symbol will be placed in LabelArr(i) . After that, you check the winning (only the comment line, because the code will be given later). If the WhoWin variable is not empty, the winner will be declared. Otherwise, if it is blank, clicks will be accepted until the grid is full and the game is draw. |
| Step 11 | Save and run project. At this point, you can click on each grid location, which places the X and O symbols alternately. After all grid locations are filled with symbols, the game returns to the "stop" state as shown in Figure 6.11. |
| Step 12 | You will write a general function ( CheckWinning ) that checks the game grid and determines whether there is a winner or not. If there is, a win will be announced and this function will produce a return value in the form of a string containing the symbol (X or O) for the winner or blank if there is no winner. You need a strategy to do it.There are eight ways to determine winning (3 horizontal, 3 vertical, 2 diagonal). Consider the indices of the label controls array ( LabelArr ) used in the following game grid: 

&#124; 1 &#124; 2 &#124; 3 &#124;
&#124; 4 &#124; 5 &#124; 6 &#124;
&#124; 7 &#124; 8 &#124; 9 &#124;

If you declare a string array named WinningArr , eight elements:

&#124; 123456789 &#124; // Possible winningsWinningArr[0] = "012" ;WinningArr[1] = "345" ;WinningArr[2] = "678" ;WinningArr[3] = "036" ;WinningArr[4] = "147" ;WinningArr[5] = "258" ;WinningArr[6] = "048" ;WinningArr[7] = "246" ; &#124;

So, the logic here is to check every possible winning and see if the all elements of the LabelArr have the same symbol (X or O, but not empty). If yes, the winner will be declared.Add the following level-form declaration:

&#124; 1 &#124; String[] WinningArr = new String[8]; &#124;

Modify the Load method of FormTicTacToe to set the values ​​of the array:

&#124; 12345678910111213141516171819202122232425262728293031 &#124; private void FormTicTacToe_Load( object sender, EventArgs e){    // Fills array    LabelArr[0] = lblBox1;    LabelArr[1] = lblBox2;    LabelArr[2] = lblBox3;    LabelArr[3] = lblBox4;    LabelArr[4] = lblBox5;    LabelArr[5] = lblBox6;    LabelArr[6] = lblBox7;    LabelArr[7] = lblBox8;    LabelArr[8] = lblBox9;    // Possible winnings    WinningArr[0] = "012" ;    WinningArr[1] = "345" ;    WinningArr[2] = "678" ;    WinningArr[3] = "036" ;    WinningArr[4] = "147" ;    WinningArr[5] = "258" ;    WinningArr[6] = "048" ;    WinningArr[7] = "246" ;    // Clears labels    for ( int i = 0; i < 9; i++)        LabelArr[i].Text = "" ;    lblMessage.Text = "Game Stopped" ;    grpFirst.Enabled = false ;    grpComputer.Enabled = false ;} &#124;

 |
| Step 13 | Add the general function, CheckWinning , to your project: 

&#124; 123456789101112131415161718192021222324252627 &#124; private String CheckWinning(){    String Winner = "" ;    int [] BoxNumber = new int [3];    String[] Symbol = new String[3];    // Checks all possible winning    for ( int i = 0; i < 8; i++)    {        for ( int j = 0; j < 3; j++)        {            BoxNumber[j] =                Convert.ToInt32(WinningArr[i][j].ToString());            Symbol[j] = LabelArr[BoxNumber[j]].Text;        }        if (Symbol[0] == Symbol[1] && Symbol[0] == Symbol[2] &&           Symbol[1] == Symbol[2] && Symbol[0] != "" )        {            // There is a winner            Winner = Symbol[0];            for ( int j = 0; j < 3; j++)                LabelArr[BoxNumber[j]].BackColor = Color.Red;        }    }    return (Winner);} &#124;

This code checks all possible winning. If all symbols on horizontal lines, vertical lines, or diagonal lines are the same symbols, then the background color of the line is changed to blue. BoxNumber array contains the indexes of LabelArr array for each possible win. |
| Step 14 | You can now modify the Click event of lblBox to check the winnings, but you need one other modification. Notice when a victory or draw game is declared, you stop the game by clicking on btnStartStop button. You need a way to differentiate the way the game is terminated from the way the game is terminated by clicking the button (which stops the game before the win or draw game is declared). Add this variable to the form level declaration: 

&#124; 1 &#124; bool GameOver; &#124;

If GameOver is true , there will be a victory or a draw game. If false , the Stop Game button is clicked before the game ends.Modify the Click event method of btnStartStop :

&#124; 12345678910111213141516171819202122232425262728293031323334353637 &#124; private void btnStartStop_Click( object sender, EventArgs e){    if (btnStartStop.Text == "Start Game" )    {        btnStartStop.Text = "Stop Game" ;        grpPlayer.Enabled = false ;        grpFirst.Enabled = false ;        grpComputer.Enabled = false ;        btnExit.Enabled = false ;        XTurn = true ;        lblMessage.Text = "X's Turn" ;        // Clears LabelArr        for ( int i = 0; i < 9; i++)        {            LabelArr[i].Text = "" ;            LabelArr[i].BackColor = Color.White;        }        Clickable = true ;        NumberOfClick = 0;    else    {        btnStartStop.Text = "Start Game" ;        if (!GameOver)            lblMessage.Text = "Game Ends" ;        grpPlayer.Enabled = true ;        if (rdoOnePlayer.Checked)        {            grpFirst.Enabled = true ;            grpComputer.Enabled = true ;        }        btnExit.Enabled = true ;        Clickable = false ;    }} &#124;

This change does several things. The BackColor property of the label controls on the grid is returned to White when the win is displayed. The GameOver variable is set to false when starting a new game. And, the Game Ends message is not displayed if GameOver is true (which means that the winner or draw game is declared). |
| Step 15 | Now, modify the Click event method of lbBox to involve CheckWinning function and new GameOver variable: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354 &#124; private void lblBox_Click( object sender, EventArgs e){    String WhoWin = "" ;    int i;    if (Clickable)    {        // See which box clicked        Label BoxClicked;        BoxClicked = (Label) sender;        // Last digit is the number extracted        i = Convert.ToInt32(            BoxClicked. Name[BoxClicked.Name.Length - 1].ToString()) - 1;        // If it has been clicked, exit        if (LabelArr[i].Text != "" )            return ;        NumberOfClick++;        if (XTurn)        {            LabelArr[i].Text = "X" ;            XTurn = false ;            lblMessage.Text = "O's Turn" ;        }        else        {            LabelArr[i].Text = "O" ;            XTurn = true ;            lblMessage.Text = "X's Turn" ;        }        // Who wins?        WhoWin = CheckWinning();        if (WhoWin != "" )        {            lblMessage.Text = WhoWin + " wins” ;            GameOver = true ;            btnStartStop.PerformClick();            return ;        }        else if (NumberOfClick == 9)        {            // Draw            lblMessage.Text = "Game is draw!" ;            GameOver = true ;            btnStartStop.PerformClick();            return ;        }    }} &#124;

 |
| Step 16 | Save and run project. The winner or draw game can now be announced:![](Image00062.jpg)Figure 6.12 The winner or draw game can now be announcedTwo-player mode is now complete. Now, you will see how to implement the game in one player mode, where user will fight the computer. You will start by making the computer make random moves (no brain!). |
| Step 17 | An important part of playing the player against the computer is deciding what thought process or decision is given to the computer. You have two choices: random computer and smart computer. You will start by writing down the code for a random computer. Then, you will write the code for a smart computer, which makes the computer a pretty tough opponent.All logics behind the movement of computer will be implemented in a method called ComputerTurn . For random movements, the computer will only randomly select one of the empty boxes on the grid and place symbol on that box (X if the computer starts the game first, O if human starts the game first). Add a random object at the following form level: 

&#124; 1 &#124; Random MyRandom = new Random(); &#124;

Write the following method, ComputerTurn , on your project:

&#124; 12345678910111213141516171819202122232425262728 &#124; private void ComputerTurn(){    int BoxSelected;    int i, n;    if (rdoRandom.Checked)    {        // Random logic        // Put symbol on N-th empty box        n = MyRandom.Next(9 - NumberOfClick) + 1;        i = 0;        for (BoxSelected = 0; BoxSelected < 9; BoxSelected++)        {            if (LabelArr[BoxSelected].Text == "" )                i++;            if (i == n)                break ;        }        // Put symbol on BoxSelected        lblBox_Click(LabelArr[BoxSelected], null );    }    else    {        // Smart computer    }} &#124;

The logic behind the code in ComputerTurn is quite simple. At any time, you have as many as 9 - NumberOfClick empty boxes on the grid. To give a symbol to a particular LabelArr(BoxSelected) , you simulate a click on the box by calling the lblBox_Click method with the appropriate sender argument (first argument): lblBox_Click (LabelArr(BoxSelected), null) . The program will know whether to place the X or O symbol in the box based on the logic that has been implemented. |
| Step 18 | Now, you will implement ComputerTurn method so that the computer is against human. You need to modify two methods. First, when you start the game, if the computer plays the game first, you need to call ComputerTurn method. Modify the Click event method of the following btnStartStop : 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041 &#124; private void btnStartStop_Click( object sender, EventArgs e){    if (btnStartStop.Text == "Start Game" )    {        btnStartStop.Text = "Stop Game" ;        grpPlayer.Enabled = false ;        grpFirst.Enabled = false ;        grpComputer.Enabled = false ;        btnExit.Enabled = false ;        XTurn = true ;        lblMessage.Text = "X's Turn" ;        // Clears LabelArr        for ( int i = 0; i < 9; i++)        {            LabelArr[i].Text = "" ;            LabelArr[i].BackColor = Color.White;        }        Clickable = true ;        NumberOfClick = 0;        Gameover = false;       if (rdoComputerFirst.Checked && rdoOnePlayer.Checked)            ComputerTurn();    else    {        btnStartStop.Text = "Start Game" ;        if (!GameOver)            lblMessage.Text = "Game Ends" ;        grpPlayer.Enabled = true ;        if (rdoOnePlayer.Checked)        {            grpFirst.Enabled = true ;            grpComputer.Enabled = true ;        }        btnExit.Enabled = true ;        Clickable = false ;    }} &#124;

And, after a symbol is placed by a human player, the computer needs to take a turn. This logic is in the Click event method of lblBox . Some changes need to be made:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960 &#124; private void lblBox_Click( object sender, EventArgs e){    String WhoWin = "" ;    int i;    if (Clickable)    {        // See which box clicked        Label BoxClicked;        BoxClicked = (Label) sender;        // Last digit is the number extracted        i = Convert.ToInt32(            BoxClicked. Name[BoxClicked.Name.Length - 1].ToString()) - 1;        // If it has been clicked, exit        if (LabelArr[i].Text != "" )            return ;        NumberOfClick++;        if (XTurn)        {            LabelArr[i].Text = "X" ;            XTurn = false ;            lblMessage.Text = "O's Turn" ;        }        else        {            LabelArr[i].Text = "O" ;            XTurn = true ;            lblMessage.Text = "X's Turn" ;        }        // Who wins?        WhoWin = CheckWinning();        if (WhoWin != "" )        {            lblMessage.Text = WhoWin + " wins” ;            GameOver = true ;            btnStartStop.PerformClick();            return ;        }        else if (NumberOfClick == 9)        {            // Draw            lblMessage.Text = "Game is draw!" ;            GameOver = true ;            btnStartStop.PerformClick();            return ;        }        if (rdoOnePlayer.Checked)            if ((XTurn && rdoComputerFirst.Checked) &#124;&#124;                   (!XTurn && rdoYouFirst.Checked))                ComputerTurn();    }} &#124;

With this code, computer will take its turn when it plays first and gives an X symbol or takes its turn when human play first and gives the symbol O. |
| Step 19 | Save and run program. Select one player option and make sure Random Computer is selected. Play several times. Make sure everything works correctly. You will see that the computer is very easy to conquer, as shown in the figure below.![](Image00063.jpg)Figure 6.13 Random logic works well |
| Step 20 | You have experienced the fun part of this game project. How do you make computer a smart opponent? In every game where a computer becomes a human opponent, you need to write down rules that give the computer intelligence. Many computer opponents that can not be conquered. For example, in chess games, computer beats human more often than vice versa.So how do you make computer as a better opponent in this Tic Tac Toe game? You certainly design how logic when human plays it. So, for computer to be intelligent player, programmer also needs to be intelligent. This generally requires practice and learning. For the Tic Tac Toe game, you can develop a simple, but very smart strategy.When it becomes the computer's turn, what movements need to be done? The rules used here are: 
*   If the computer can win the game in one move, then the move must be made and the game ends. So, if there is one line with two symbols given by the computer and an empty box, then the empty space must be given a symbol by the computer.
*   If the computer can block with one move, then the move must be done and the opponent will not be able to win the game in the next move. So, if there is a line with two symbols given by human and an empty box, then the empty space must be taken over by computer by giving it a symbol.
*   If there is no possibility of winning or blocking that is possible, then the movement is carried out in this order: the middle box, one of the four corner boxes, or one of the four side squares.

You might ask about the third step above, why the order is important. Remember that there are 8 possible ways to win the game (3 horizontal, 3 vertical, and 2 diagonal). The square box is involved in 4 possible wins, the corner box is involved in three possible wins, and the side box is involved in only two wins.You will implement these steps. The following is a modified version of the ComputerTurn method that implements this smart logic:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273747576777879808182838485868788899091929394 &#124; private void ComputerTurn(){    int BoxSelected;    int i, n;    int j, k;    String ComputerSymbol, PlayerSymbol, WhichSymbol;    int [] BoxNumber = new int [3];    String[] Symbols = new String[3];    int EmptyBox;    int [] BestMove = { 4, 0, 2, 6, 8, 1, 3, 5, 7 };    if (rdoRandom.Checked)    {        // Random logic        // Put symbol on N-th empty box        n = MyRandom.Next(9 - NumberOfClick) + 1;        i = 0;        for (BoxSelected = 0; BoxSelected < 9; BoxSelected++)        {            if (LabelArr[BoxSelected].Text == "" )                i++;            if (i == n)                break ;        }        // Put symbol on BoxSelected        lblBox_Click(LabelArr[BoxSelected], null );    }    else    {        // Smart computer        // Determines who has what symbol        if (rdoComputerFirst.Checked)        {            ComputerSymbol = "X" ;            PlayerSymbol = "O" ;        }        else        {            ComputerSymbol = "O" ;            PlayerSymbol = "X" ;        }        //Step 1 (K = 1) - checks winning: if there is one line with        //two Symbols given by the computer And an empty box        //Step 2 (K = 2) - checks blocking: if there is a line with        //two Symbols given by human And an empty box        for (k = 1; k <= 2; k++)        {            if (k == 1)                WhichSymbol = ComputerSymbol;            else                WhichSymbol = PlayerSymbol;            for (i = 0; i < 8; i++)            {                n = 0;                EmptyBox = 0;                for (j = 0; j < 3; j++)                {                    BoxNumber[j] =                      Convert.ToInt32(WinningArr[i][j].ToString());                    Symbols[j] = LabelArr[BoxNumber[j]].Text;                    if (Symbols[j] == WhichSymbol)                        n++;                    else if (Symbols[j] == "" )                        EmptyBox = BoxNumber[j];                }                if (n == 2 && EmptyBox != 0)                {                    //Give symbol on empty box to win                    //(K = 1) or to block(K = 2)                    lblBox_Click(LabelArr[EmptyBox], null );                    return ;                }            }        }        // Step 3: Find the best movement        for (i = 0; i < 9; i++)        {            if (LabelArr[BestMove[i]].Text == "" )            {                lblBox_Click(LabelArr[BestMove[i]], null );                return ;            }        }    }} &#124;

In this smart logic, you find out whether the computer has X or O. Step 1 and 2 of computer logic are done in a for loop with k as an index. In that loop, all possible wins are sought on a line with 2 identical symbols and an empty box. For k = 1, you look for the computer symbol and an empty box, which gives the computer the next move. For k = 2, you look for a human symbol and an empty box, which gives the computer a blockage in the next move.If either step 1 or step 2 is successful, you move to step 3\. The next best move is done in the order in BestMove array. In step 3, you read this array, look for available empty boxes and move there. |
| Step 21 | Save and run project. The game is now fully functional. You can fight the computer. You will know that computers cannot be conquered. The best thing to do is draw:![](Image00064.jpg)Figure 6.14 With smart computer, the best thing user can do is draw game |
| Step 22 | You will add some sounds to the game Tic Tac Toe. draw.wav file is the sound that is used when the game ends in a draw. win.wav file is the sound when the game is won by one of the players.Add declarations for the following two sounds at the form-level: 

&#124; 12 &#124; System.Media.SoundPlayer DrawSound;System.Media.SoundPlayer WinSound; &#124;

 |
| Step 23 | Modify the Load method of FormTicTacToe to create these sound objects: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738 &#124; private void FormTicTacToe_Load( object sender, EventArgs e){    // Fills array    LabelArr[0] = lblBox1;    LabelArr[1] = lblBox2;    LabelArr[2] = lblBox3;    LabelArr[3] = lblBox4;    LabelArr[4] = lblBox5;    LabelArr[5] = lblBox6;    LabelArr[6] = lblBox7;    LabelArr[7] = lblBox8;    LabelArr[8] = lblBox9;    // Possible winnings    WinningArr[0] = "012" ;    WinningArr[1] = "345" ;    WinningArr[2] = "678" ;    WinningArr[3] = "036" ;    WinningArr[4] = "147" ;    WinningArr[5] = "258" ;    WinningArr[6] = "048" ;    WinningArr[7] = "246" ;    // Clears labels    for ( int i = 0; i < 9; i++)        LabelArr[i].Text = "" ;    lblMessage.Text = "Game Stopped" ;    grpFirst.Enabled = false ;    grpComputer.Enabled = false ;    DrawSound = new        System.Media.SoundPlayer(Application.StartupPath +        "\\draw.wav" );    WinSound = new        System.Media.SoundPlayer(Application.StartupPath +        "\\win.wav" );} &#124;

Note that the sound files are loaded from Application.StartupPath directory, i.e. folder bin\Debug in your project. |
| Step 24 | Finally, you put both sounds at the correct locations in the Click of lblBox method: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162 &#124; private void lblBox_Click( object sender, EventArgs e){    String WhoWin = "" ;    int i;    if (Clickable)    {        // See which box clicked        Label BoxClicked;        BoxClicked = (Label) sender;        // Last digit is the number extracted        i = Convert.ToInt32(            BoxClicked. Name[BoxClicked.Name.Length - 1].ToString()) - 1;        // If it has been clicked, exit        if (LabelArr[i].Text != "" )            return ;        NumberOfClick++;        if (XTurn)        {            LabelArr[i].Text = "X" ;            XTurn = false ;            lblMessage.Text = "O's Turn" ;        }        else        {            LabelArr[i].Text = "O" ;            XTurn = true ;            lblMessage.Text = "X's Turn" ;        }        // Who wins?        WhoWin = CheckWinning();        if (WhoWin != "" )        {            WinSound.Play();            lblMessage.Text = WhoWin + " wins” ;            GameOver = true ;            btnStartStop.PerformClick();            return ;        }        else if (NumberOfClick == 9)        {            // Draw            DrawSound.Play();            lblMessage.Text = "Game is draw!" ;            GameOver = true ;            btnStartStop.PerformClick();            return ;        }        if (rdoOnePlayer.Checked)            if ((XTurn && rdoComputerFirst.Checked) &#124;&#124;                   (!XTurn && rdoYouFirst.Checked))                ComputerTurn();    }} &#124;

 |
| Step 25 | Save and run the project. Now, you have the full version of the Smart Tic Tac Toe game.![](Image00065.jpg)Figure 6.15 The final version of this project |
|  |  |

| Form1.cs |
| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197198199200201202203204205206207208209210211212213214215216217218219220221222223224225226227228229230231232234235236237238239240241242243244245246247248249250251252253254255256257258259260261262263264265266267268269270271272273274275276277278279280281282283284285286287288289290291292293294295296297298299300301302303304305306307308309310322323324 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;namespace Tic_Tac_Toe{    public partial class FormTicTacToe : Form    {        Label[] LabelArr = new Label[9];        bool XTurn;        bool Clickable = false ;        int NumberOfClick;        String[] WinningArr = new String[8];        bool GameOver;        Random MyRandom = new Random();        System.Media.SoundPlayer DrawSound;        System.Media.SoundPlayer WinSound;        public FormTicTacToe ()        {            InitializeComponent();        }        private void FormTicTacToe_Load( object sender, EventArgs e)        {            // Fills array            LabelArr[0] = lblBox1;            LabelArr[1] = lblBox2;            LabelArr[2] = lblBox3;            LabelArr[3] = lblBox4;            LabelArr[4] = lblBox5;            LabelArr[5] = lblBox6;            LabelArr[6] = lblBox7;            LabelArr[7] = lblBox8;            LabelArr[8] = lblBox9;            // Possible winnings            WinningArr[0] = "012" ;            WinningArr[1] = "345" ;            WinningArr[2] = "678" ;            WinningArr[3] = "036" ;            WinningArr[4] = "147" ;            WinningArr[5] = "258" ;            WinningArr[6] = "048" ;            WinningArr[7] = "246" ;            // Clears labels            for ( int i = 0; i < 9; i++)                LabelArr[i].Text = "" ;            lblMessage.Text = "Game Stopped" ;            grpFirst.Enabled = false ;            grpComputer.Enabled = false ;            DrawSound = new System.Media.SoundPlayer(Application.StartupPath +                "\\draw.wav" );            WinSound = new System.Media.SoundPlayer(Application.StartupPath +                "\\win.wav" );        }        private void btnExit_Click( object sender, EventArgs e)        {            this .Close();        }        private void btnStartStop_Click( object sender, EventArgs e)        {            if (btnStartStop.Text == "Start Game" )            {                btnStartStop.Text = "Stop Game" ;                grpPlayer.Enabled = false ;                grpFirst.Enabled = false ;                grpComputer.Enabled = false ;                btnExit.Enabled = false ;                XTurn = true ;                lblMessage.Text = "X's Turn" ;                // Clears LabelArr                for ( int i = 0; i < 9; i++)                {                    LabelArr[i].Text = "" ;                    LabelArr[i].BackColor = Color.White;                }                Clickable = true ;                NumberOfClick = 0;                GameOver = false ;                if (rdoComputerFirst.Checked && rdoOnePlayer.Checked)                    ComputerTurn();            }            else            {                btnStartStop.Text = "Start Game" ;                if (!GameOver)                    lblMessage.Text = "Game Ends" ;                grpPlayer.Enabled = true ;                if (rdoOnePlayer.Checked)                {                    grpFirst.Enabled = true ;                    grpComputer.Enabled = true ;                }                btnExit.Enabled = true ;                Clickable = false ;            }        }        private void lblBox_Click( object sender, EventArgs e)        {            String WhoWin = "" ;            int i;            if (Clickable)            {                // See which box clicked                Label BoxClicked;                BoxClicked = (Label) sender;                // Last digit is the number extracted                i = Convert.ToInt32(                    BoxClicked.Name[BoxClicked.Name.Length - 1].ToString()) - 1;                // If it has been clicked, exit                if (LabelArr[i].Text != "" )                    return ;                NumberOfClick++;                if (XTurn)                {                    LabelArr[i].Text = "X" ;                    XTurn = false ;                    lblMessage.Text = "O's Turn" ;                }                else                {                    LabelArr[i].Text = "O" ;                    XTurn = true ;                    lblMessage.Text = "X's Turn" ;                }                // Who wins?                WhoWin = CheckWinning();                if (WhoWin != "" )                {                    WinSound.Play();                    lblMessage.Text = WhoWin + " wins" ;                    GameOver = true ;                    btnStartStop.PerformClick();                    return ;                }                else if (NumberOfClick == 9)                {                    // Draw                    DrawSound.Play();                    lblMessage.Text = "Game is draw!" ;                    GameOver = true ;                    btnStartStop.PerformClick();                    return ;                }                if (rdoOnePlayer.Checked)                    if ((XTurn && rdoComputerFirst.Checked) &#124;&#124;                           (!XTurn && rdoYouFirst.Checked))                        ComputerTurn();            }        }        private String CheckWinning()        {            String Winner = "" ;            int [] BoxNumber = new int [3];            String[] Symbol = new String[3];            // Checks all possible winning            for ( int i = 0; i < 8; i++)            {                for ( int j = 0; j < 3; j++)                {                    BoxNumber[j] = Convert.ToInt32(WinningArr[i][j].ToString());                    Symbol[j] = LabelArr[BoxNumber[j]].Text;                }                if (Symbol[0] == Symbol[1] && Symbol[0] == Symbol[2] &&                    Symbol[1] == Symbol[2] && Symbol[0] != "" )                {                    // There is a winner                    Winner = Symbol[0];                    for ( int j = 0; j < 3; j++)                        LabelArr[BoxNumber[j]].BackColor = Color.Red;                }            }            return (Winner);        }        private void rdoSatuPemain_Click( object sender, EventArgs e)        {            grpFirst.Enabled = true ;            grpComputer.Enabled = true ;        }        private void rdoDuaPemain_CheckedChanged( object sender, EventArgs e)        {            grpFirst.Enabled = false ;            grpComputer.Enabled = false ;        }        private void ComputerTurn()        {            int BoxSelected;            int i, n;            int j, k;            String ComputerSymbol, PlayerSymbol, WhichSymbol;            int [] BoxNumber = new int [3];            String[] Symbols = new String[3];            int EmptyBox;            int [] BestMove = { 4, 0, 2, 6, 8, 1, 3, 5, 7 };            if (rdoRandom.Checked)            {                // Random logic                // Put symbol on N-th empty box                n = MyRandom.Next(9 - NumberOfClick) + 1;                i = 0;                for (BoxSelected = 0; BoxSelected < 9; BoxSelected++)                {                    if (LabelArr[BoxSelected].Text == "" )                        i++;                    if (i == n)                        break ;                }                // Put symbol on BoxSelected                lblBox_Click(LabelArr[BoxSelected], null );            }            else            {                // Smart computer                // Determines who has what symbol                if (rdoComputerFirst.Checked)                {                    ComputerSymbol = "X" ;                    PlayerSymbol = "O" ;                }                else                {                    ComputerSymbol = "O" ;                    PlayerSymbol = "X" ;                }                //Step 1 (K = 1) - checks winning: if there is one line with                //two Symbols given by the computer And an empty box                //Step 2 (K = 2) - checks blocking: if there is a line with                //two Symbols given by human And an empty box                for (k = 1; k <= 2; k++)                {                    if (k == 1)                        WhichSymbol = ComputerSymbol;                    else                        WhichSymbol = PlayerSymbol;                    for (i = 0; i < 8; i++)                    {                        n = 0;                        EmptyBox = 0;                        for (j = 0; j < 3; j++)                        {                            BoxNumber[j] =                                Convert.ToInt32(WinningArr[i][j].ToString());                            Symbols[j] = LabelArr[BoxNumber[j]].Text;                            if (Symbols[j] == WhichSymbol)                                n++;                            else if (Symbols[j] == "" )                                EmptyBox = BoxNumber[j];                        }                        if (n == 2 && EmptyBox != 0)                        {                            //Give symbol on empty box to win                            //(K = 1) or to block(K = 2)                            lblBox_Click(LabelArr[EmptyBox], null );                            return ;                        }                    }                }                // Step 3: Find the best movement                for (i = 0; i < 9; i++)                {                    if (LabelArr[BestMove[i]].Text == "" )                    {                        lblBox_Click(LabelArr[BestMove[i]], null );                        return ;                    }                }            }        }    }} |
|  |  |

TUTORIAL 7

FIGHTING PLANE

In this tutorial, you will build Fighting Plane program. This program can be played by two human players or human player versus computer.

| Description |
| Start Visual C# and open the project and press <F5> to run it, you will see:![](Image00066.jpg)Figure 7.1 Fighting Plane game startsNext, press Options button. Choose One . With one player, you can also choose the level of difficulty of the game, as shown in Figure 7.1.Click OK and then click New Game button. Game will start, as shown in Figure 7.2.The controls of the player are done via the keyboard. Player 1 presses A key to move up, Z key to move down, and S key to throw rudal.When you choose Two players from the Options button, this game can be played by two human players. Player 1 presses the same keys, while player 2 presses key K to move up, M to move down, and key J to throw rudal, as shown in Figure 7.3.![](Image00067.jpg)Figure 7.2 User chooses one player and hard difficulty level![](Image00068.jpg)Figure 7.3 User play against computer![](Image00069.jpg)Figure 7.4 Human versus human |
| Tutorial Steps |
| Step 1 | You will start building Fighting Plane game project. Start a new project in Visual C#. Place 12 labels, a large control panel, and three control buttons on the form. In the control panel, place a smaller panel with two group box controls and a button control. In the first group box, place 2 radio buttons; in the second box group, place 4 radio buttons. Add two timer controls to the project. Change the size and position of each control so that the form is now as shown in Figure 7.5.All label controls are used for titles and provide scoring and game information. The large panel ( Panel1 ) is the playing field. Three button controls are used to start / stop a program, set options, and exit the program. One timer control is used to control game animation and another is used to represent the computer's decision process. The second control panel ( Panel2 ) is used to select game options. One group box contains radio buttons which are used to select number of players. A group box contains radio buttons to select the level of difficulty of the game, when playing against a computer. A small button is used to close the options panel. The default properties are set for one-player games with the easiest game difficulty. |
| Step 2 | Set control properties using the Properties window:![](Image00070.jpg)Figure 2.5 All controls user in Fighting Plane game project 

&#124; A number of properties of the Form1 object &#124;
&#124; Name &#124; FormFightingPlane &#124;
&#124; BackColor &#124; Red &#124;
&#124; FormBorderStyle &#124; FixedSingle &#124;
&#124; KeyPreview &#124; True &#124;
&#124; StartPosition &#124; CenterScreen &#124;
&#124; Text &#124; Fighting Plane &#124;
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
&#124; BackColor &#124; Yellow &#124;
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
&#124; BackColor &#124; Yellow &#124;
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
&#124; BackColor &#124; Yellow &#124;
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
&#124; BackColor &#124; Yellow &#124;
&#124; BorderStyle &#124; Fixed3D &#124;
&#124; Tex &#124; 20 &#124;
&#124; TextAlign &#124; MiddleCenter &#124;
&#124; Font &#124; Arial Narrow, Bold, Size 14 &#124;
&#124;  &#124;  &#124;

&#124; A number of properties of the Panel1 object &#124;
&#124; Name &#124; pnlGame &#124;
&#124; BackColor &#124; Blue &#124;
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
&#124; BackColor &#124; Crimson &#124;
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

When finished, the form will look like in the figure below.![](Image00071.jpg)Figure 7.6 Form after properties setting done |
| Step 3 | Run the project (press <F5>), the game is displayed as shwon in Figure 7.7\. You will now start writing project code. You first write the code that sets the status of the game based on the selected game options. |
| Step 4 | When the game starts, user will choose the options (number of players and the difficulty level of the game). Based on these choices, the form will display different information.When the user clicks Options button ( btnOption ), the following things occur: 
*   Disable btnGame .
*   Disable btnOption .
*   Disable Exit button.
*   Make pnlOption visible.

![](Image00072.jpg)Figure 7.7 The form first startsThe code to implement these steps is placed in the Click event of the btnOption button:

&#124; 1234567 &#124; private void btnOption_Click( object sender, EventArgs e){    btnGame.Enabled = false ;    btnOption.Enabled = false ;    btnExit.Enabled = false ;    pnlOption.Visible = true ;} &#124;

Add this procedure to your project. When the project is run and the user clicks on the Options button, the form will be displayed as shown in Figure 7.8. |
| Step 5 | After the options panel is displayed, the user can choose one or two players and select game difficulty (if playing against computer). You will use an Integer variable named NumberOfPlayer to save number of players and an Integer variable with the name Difficulty to save the selected difficulty level. Add the following two form-level variable declarations to the project: 

&#124; 1 &#124; int NumberOfPlayer, Difficulty; &#124;

![](Image00073.jpg)Figure 2.8 When user clicks Options button |
| Step 6 | Add a Load event of FormFightingPlane to the project to initialize these variables to their default values: 

&#124; 12345 &#124; private void FormFightingPlane_Load( object sender, EventArgs e){    NumberOfPlayer = 1;    Difficulty = 1;} &#124;

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

Add this procedure to your project.![](Image00073.jpg)Figure 7.9 The game display will appear with default values ​​(one player, easiest difficulty level) |
| Step 9 | After the user selects options he wants, he clicks the OK button ( btnOK ) to close the options panel. The code in the Click event of the btnOK control is the opposite of the code in the Click event of the btnOption : 

&#124; 1234567 &#124; private void btnOK_Click( object sender, EventArgs e){    btnGame.Enabled = true ;    btnOption.Enabled = true ;    btnExit.Enabled = true ;    pnlOption.Visible = false ;} &#124;

Add this procedure to your project. At this point, game can begin. |
| Step 10 | Save and run the project. The game display will appear with default values ​​(one player, easiest difficulty level). Click Options button to bring up the options panel, as shown in Figure 7.9.Changing the level of difficulty will not change the appearance of the form. Changing number of players will change the form display. Select two players, the header information will change and the Difficulty group box will be disabled:![](Image00074.jpg)Figure 7.10 Changing number of players will change the form display |
| Step 11 | The configuration file will contain two pieces of information: number of players ( NumberOfPlayer ) and difficulty level ( Difficulty ). First, you will develop code to write the configuration file when the program ends. This code is placed into the FormClosing event: 

&#124; 12345678 &#124; private void FormFightingPlane_FormClosing( object sender, FormClosingEventArgs e){    StreamWriter FileOutput =        new StreamWriter(Application.StartupPath + "\\plane.ini" );    FileOutput.WriteLine(NumberOfPlayer);    FileOutput.WriteLine(Difficulty);    FileOutput.Close();} &#124;

As always, the configuration file is in bin\Debug folder. Add this procedure to your project. |
| Step 12 | Add this code to the Click event procedure of btnExit , so you can stop the project and write configuration file: 

&#124; 1234 &#124; private void btnExit_Click( object sender, EventArgs e){    this .Close();} &#124;

 |
| Step 13 | The configuration file is opened and read in the Load procedure of the form. Based on the values ​​read, you then simulate clicks on the radio buttons to select options. The hardest part of this procedure is that you can only simulate these clicks if the buttons are visible and enabled. You will do this in this code. The modified Load procedure of the form that opens the configuration file and selects the radio buttons is given below: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637 &#124; private void FormFightingplane_Load( object sender, EventArgs e){    try    {        StreamReader fileInput =            new StreamReader(Application.StartupPath +            "\\plane.ini" );        NumberOfPlayer = Convert. ToInt32( fileInput .ReadLine());        Difficulty = Convert.ToInt32(fileInput.ReadLine());        fileInput.Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;} &#124;

![](Image00075.jpg)Figure 7.11 The project is first displayed with default optionsNote that you use the default values ​​if the configuration file cannot be opened. Also note that you make the form ( this ) and panel ( pnlOption ) appear before selecting options. You choose the difficulty option first, because this option is not enabled if two players are selected. After the option is selected, the Visible property of the panel returnes to False . |
| Step 14 | Save and run the project. The project is first displayed with default options (one player and easiest difficulty level) as shown in Figure 7.11.Choose several options. For example, say you choose the number of players two. Then, click the OK button and the Exit button to stop the project. Run the project again and click the Options button to see that the last selected option is still saved in the form: |
| Step 15 | You will have a number of animated images on this project (players, rudal, and ufos). This is a good place to test object-oriented programming skills. You will build a class named TwoPlayer to represent the two player objects and its default constructor: 

&#124; 1234567 &#124; class TwoPlayer{    public TwoPlayer ()    {    }} &#124;

![](Image00076.jpg)Figure 7.12 The last selected options are saved in the formYou will use three properties to describe a TwoPlayer object: MyImage ( Image data type), Location (type of Rectangle that describes size and location), an IsVisible (Boolean type that tells whether the object is visible or not). Add these declarations to the class file, which initializes IsVisible to False :

&#124; 12345678910 &#124; class TwoPlayer{    public TwoPlayer ()    {    }    public Image MyImage;    public Rectangle Location;    public bool IsVisible = false ;} &#124;

 |
| Step 16 | You will expand the class definition by adding several methods to help with the animation work. Class methods are used so that objects can do certain jobs. The method is written as a Visual C# method. You will write three methods for the TwoPlayer object, one method that places it on a graphical object, one method that moves it to a new location, and another method that removes it. These three methods are added to the class definition just like the general method when added to the form code file. To add a method to the class description, you choose the name and data type of information that will be generated as a return value. In addition, you specify the arguments required by the method.The Place method places a TwoPlayer object into a graphical object named g (passed as argument): 

&#124; 12345 &#124; public void Place(Graphics g){    g.DrawImage( this .MyImage, this .Location);    this .IsVisible = true ;} &#124;

Note the use of this keyword to refer to the current object or the calling object. After the object is placed on g , you set IsVisible property to True .The Move method moves a TwoPlayer object to a new location. The arguments needed are g ( Graphics object), bc ( Brush object) to delete the previous location, dx (change in location x), and dy (change in location y):

&#124; 1234567 &#124; public void Move(Graphics g, Brush bc, int dx, int dy){    g.FillRectangle(bc, this .Location);    this .Location.X += dx;    this .Location.Y += dy;    g.DrawImage( this .MyImage, this .Location);} &#124;

The object was deleted first. The location is then updated and the object is redrawn.The Remove method removes a TwoPlayer object from a graphical object (using bc brush):

&#124; 12345 &#124; public void Remove(Graphics g, Brush bc){    g.FillRectangle(bc, this .Location);    this .IsVisible = false ;} &#124;

Add these three methods ( Place , Move , Remove ) to te TwoPlayer class file to create the latest version:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940 &#124; using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;namespace FiringRudal{    class TwoPlayer    {        public TwoPlayer ()        {        }        public Image MyImage;        public Rectangle Location;        public bool IsVisible = false ;        public void Place(Graphics g)        {            g.DrawImage( this .MyImage, this .Location);            this .IsVisible = true ;        }        public void Move(Graphics g, Brush bc, int dx, int dy)        {            g.FillRectangle(bc, this .Location);            this .Location.X += dx;            this .Location.Y += dy;            g.DrawImage( this .MyImage, this .Location);        }        public void Remove(Graphics g, Brush bc)        {            g.FillRectangle(bc, this .Location);            this .IsVisible = false ;        }    }} &#124;

Using this class, a TwoPlayer object variable can be created using:

&#124; 1 &#124; TwoPlayer MyPlayer &#124;

The variable then is used to reference new TwoPlayer player:

&#124; 1 &#124; MyPlayer = new TwoPlayer() &#124;

Once created, the MyImage property can be specified using Image.FromFile method and the Location property can be assigned a Rectangle structure.TwoPlayer object is placed on a graphical object ( MyImage ) using: MyPlayer.Place (MyImage) . The TwoPlayer object is moved using: MyPlayer.Move(MyImage, MyBrush, dx, dy) , where MyBrush is a solid brush that has the same color as the background color of the graphical object, dx is how far you want to move the object horizontally, and dy is how far you want to move the object vertically. |
| Step 17 | You will now write the code to start and stop the game. You first need to define form-level variables to play and control the game. Return to the code of the form, add declarations to the project: 

&#124; 12345 &#124; Graphics MyGraphics;Brush MyBrush;TwoPlayer Player1, Player2;int Player1Hit, Player2Hit, Player1Rem, Player2Rem;const int RudalMax = 20; &#124;

MyGraphics is the region of graphics used to play game and MyBrush will be used to erase images. Two TwoPlayer objects ( Player1 and Player2 ) represent two planes. Player1Hit and Player2Hit will track how many successful firing rudal for each player. Players1Rem and Players2Rem will track how many fires each player still has. A RudalMax constant (you can change it if you like) sets the number of initial rudals each player has. |
| Step 18 | Add code to Load of FormFightingPlane to initialize each of these variables. The modified procedure is given as follows: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152 &#124; private void FormFightingPlane_Load( object sender, EventArgs e){    try    {        StreamReader fileInput =            new StreamReader(Application.StartupPath +            "\\plane.ini" );        NumberOfPlayer = Convert. ToInt32(fileInput.ReadLine());        Difficulty = Convert.ToInt32( fileInput .ReadLine());        fileInput .Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;    Player1Rem = RudalMax;    Player2Rem = RudalMax;    lblRemPlayer1.Text = Player1Rem.ToString();    lblRemPlayer2.Text = Player2Rem.ToString();    // Creates TwoPlayer objects    MyGraphics = pnlGame.CreateGraphics();    MyBrush = new SolidBrush(pnlGame.BackColor);    Player1 = new TwoPlayer();    Player2 = new TwoPlayer();    Player1.MyImage = Image.FromFile(Application.StartupPath +        "\\bomber1.png" );    Player2.MyImage = Image.FromFile(Application.StartupPath +        "\\bomber2.png" );} &#124;

Pay attention to the code to create two TwoPlayer objects and initialize MyImage property. Copy the bomber1.png and bomber2.png graphic files into bin\Debug folder. |
| Step 19 | At this point, the user can click on New Game ( btnGame ) to start the game. The following steps will be added: 
*   Remove all graphic objects.
*   Change the Text property from btnGame to Stop Game .
*   Disable btnOption .
*   Disable Exit button.
*   Reset Player1Hit and Player2Hit to 0.
*   Reset Player1Rem and Player2Rem to RudalMax .
*   Place Player1 and Player2 objects to the starting position (using Place method of TwoPlayer class).

The code for these steps is quite simple. The Player1 object will be centered vertically on pnlGame near the left edge. The Player2 object will be centered vertically on pnlGame near the right edge.The btnGame button is also used to stop the game. When the user clicks btnGame button (when its Text property is Stop Game ), the following things need to be done:

*   Delete Player1 and Player2 objects (using Remove method of TwoPlayer class).
*   Change Text property from btnGame to Start Game .
*   Enable btnOption .
*   Enable Exit button.
*   Display “Game Over” message.

The code for all of these steps is placed in the Click event procedure of btnGame . The code is given as follows:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839 &#124; private void btnGame_Click( object sender, EventArgs e){    if (btnGame.Text == "New Game" )    {        MyGraphics.Clear(pnlGame.BackColor);        btnGame.Text = "Stop Game" ;        btnOption.Enabled = false ;        btnExit.Enabled = false ;        Player1Hit = 0;        Player2Hit = 0;        lblHitPlayer1.Text = "0" ;        lblHitPlayer2.Text = "0" ;        Player1Rem = RudalMax;        Player2Rem = RudalMax;        lblRemPlayer1.Text = Player1Rem.ToString();        lblRemPlayer2.Text = Player2Rem.ToString();        Player1.Location = new Rectangle(5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player1.MyImage.Height), Player1.MyImage.Width,            Player1.MyImage.Height);        Player2.Location = new Rectangle(pnlGame.ClientSize.Width –            Player2.MyImage.Width - 5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player2.MyImage.Height), Player2.MyImage.Width,            Player2.MyImage.Height);        Player1.Place(MyGraphics);        Player2.Place(MyGraphics);    }    else    {        Player1.Remove(MyGraphics, MyBrush);        Player2.Remove(MyGraphics, MyBrush);        btnGame.Text = "New Game" ;        btnOption.Enabled = true ;        btnExit.Enabled = true ;        MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),            Brushes.Yellow, 530, 210);    }} &#124;

Add this procedure to your project. Positioning “Game Over” message is obtained by trial and error. Save and run project. Click on New Game button and both players will appear as shown in Figure 7.13.Before quit the game, click Stop Game button to make sure the procedure is working properly and “Game Over” message is displayed, as shown in Figure 7.14.At this point, the user has the option to start a new game, change options or exit the program. |
| Step 20 | You need the capability to move player up and down the graphics region. If you choose to use the keyboard to control, use the KeyDown event. This event is the same as the KeyPress event that has been used before, but is more flexible. This event can be used to detect keys that are pressed, along with control keys such as Alt, Ctrl, Shift, cursor control, and other control keys. The form of the KeyDown event procedure of form is: 

&#124; 123 &#124; private void FormFightingPlane_KeyDown( object sender, KeyEventArgs e){} &#124;

The KeyCode property is a member of the Keys class. There are a number of values ​​for each key that can be pressed. The Intellisense feature of the Visual C# IDE will provide KeyCode values ​​when needed. KeyDown event generally have a Select Case structure with a Case clause for each possible key (or key combination).In this game, you choose the following keys to control the player's movement and to throw rudal (selected from the keyboard):

&#124; Player 1 &#124; A – Up, Z – Down, S – Throw rudal &#124;
&#124; Player 2 &#124; K – Up, M – Down, J – Throw rudal &#124;

You can change it yourself if you like.![](Image00077.jpg)Figure 7.13 The Player1 object is centered vertically on pnlGame near the left edge and the Player2 object is centered vertically on pnlGame near the right edge.![](Image00078.jpg)Figure 7.14 “Game Over” message appear when user clicks Stop Game buttonEach time the movement key is pressed, you will move the player (using Move method of PlayerTwo class) as far as PlayerIncrement (a value that you can change if needed) if you want to move it down and as far as - PlayerIncrement if you want to move it up. Add a form-level constant declaration to this value:

&#124; 1 &#124; const int PlayerIncrement = 5; &#124;

The code to move the player is placed into the KeyDown event procedure of the form:

&#124; 123456789101112131415161718192021222324252627282930313233 &#124; private void FormFightingPlane_KeyDown( object sender, KeyEventArgs e){    if (btnGame.Text == "New Game" )        return ;    switch (e.KeyCode)    {        case Keys.A:            Player1.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player1.Location.Y < 0)                Player1.Location.Y = 0;            break ;        case Keys.Z:            Player1.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player1.Location.Y > pnlGame.ClientSize.Height –                Player1.Location.Height)                Player1.Location.Y = pnlGame.ClientSize.Height –                    Player1.Location.Height;            break ;        case Keys.K:            Player2.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player2.Location.Y < 0)                Player2.Location.Y = 0;            break ;        case Keys.M:            Player2.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player2.Location.Y > pnlGame.ClientSize.Height –                Player2.Location.Height)                Player2.Location.Y = pnlGame.ClientSize.Height –                    Player2.Location.Height;            break ;    }} &#124;

Note that you do not allow KeyDown events to occur if the user has not started a game (that is, if btnGame still says New Game ). Add this procedure to your project.You need to make sure that form always has the focus to intercept the keys to move players. To be sure, add this line: this.Focus() at the end of the Click procedure on btnGame which is used to start a new game.![](Image00079.jpg)Figure 7.15 Both players now can move up and down. |
| Step 21 | Save and run the project. Select Two option in grpPlayer so you can see whether both players can move. Click New Game . Press A and Z to move player 1 and press K and M to move player 2\. Make sure both players do not move past the upper or lower limit of the control panel as shown in Figure 7.15. |
| Step 22 | In this project, you will give players the ability to throw rudal at each other. Rudal will be represented by Image object just like player. The only difference here is that when rudal is fired, it moves without user interaction at a predetermined speed and its position is updated by the timer control. And, you need to constantly check if the rudal collides with another object. TwoPlayer class does not have properties for speed, or methods that check collisions. So, you need a new class to define rudal.You will explain rudal using MovingRudal class. This class will have a number of properties and methods from TwoPlayer class (using inheritance), plus the speed properties and a method for checking collision. To build this class, you can start from scratch, with all new properties and new methods. Or, you can take advantage of the concept of inheritance in object-oriented programming. Inheritance is a concept where you can build an existing class-based class, by adding its own properties and/or methods. This will save work.You will see how inheritance is used. You will add the collision checking method later. Now, just focus on class properties. Add a class to the project, name it MovinRudal . Use the following class code: 

&#124; 123456789 &#124; class MovingRudal : TwoPlayer{    public MovingRudal ()    {    }    public int XSpeed;    public int YSpeed;} &#124;

This will make all the properties and methods of TwoPlayer class available to the new class ( MovingRudal ). Other lines of code add speed properties ( XSpeed , speed in the horizontal direction; YSpeed , speed in the vertical direction). These two properties represent how far the MovingRudal will move in a certain direction. |
| Step 23 | Rudals are represented by two MovingRudal objects ( Rudal1 is rudal fired by player 1, while Rudal2 is rudal fired by player 2). Horizontal speed is determined by the rudal speed constant with zero vertical speed. Add the following level-form declarations to your project: 

&#124; 12 &#124; MovingRudal Rudal1, Rudal2;const int RudalSpeed = 30; &#124;

Speed ​​is another parameter that you can change yourself as you like with the value that you think is best. |
| Step 24 | Snowballs are created in the Load procedure from the form. Add the following four lines to the procedure (after the lines of code that specify the TwoPlayer objects): 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061 &#124; private void FormFightingPlane_Load( object sender, EventArgs e){    try    {        StreamReader fileInput =            new StreamReader(Application.StartupPath +            "\\plane.ini" );        NumberOfPlayer = Convert. ToInt32(fileInput.ReadLine());        Difficulty = Convert.ToInt32(fileInput.ReadLine());        fileInput.Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;    Player1Rem = RudalMax;    Player2Rem = RudalMax;    lblRemPlayer1.Text = Player1Rem.ToString();    lblRemPlayer2.Text = Player2Rem.ToString();    // Creates TwoPlayer objects    MyGraphics = pnlGame.CreateGraphics();    MyBrush = new SolidBrush(pnlGame.BackColor);    Player1 = new TwoPlayer();    Player2 = new TwoPlayer();    Player1.MyImage = Image.FromFile(Application.StartupPath +        "\\bomber1.png" );    Player2.MyImage = Image.FromFile(Application.StartupPath +        "\\bomber2.png" );    Rudal1 = new MovingRudal();    Rudal2 = new MovingRudal();    Rudal1.MyImage = Image.FromFile(Application.StartupPath +        "\\rudal1.png" );    Rudal2.MyImage = Image.FromFile(Application.StartupPath +        "\\rudal2.png" );    btnGame.Focus();} &#124;

 |
| Step 25 | Player 1 fires rudal by pressing the S key. Player 2 fires rudal by pressing the J key. You set a number of rules in firing the rudal. First, you will only allow one rudal from each player to be displayed on the screen at a time (no multi pitching). Second, the player cannot throw rudal if he runs out of rations. If these conditions are met, when the player fires rudal, these steps are carried out: 
*   Decrease the remaining rudals.
*   Update the remaining rudals.
*   Position the rudal to the side of the player (in the right of player 1, in the left of player 2).
*   Place rudal snowballs on graphic objects using Place method of TwoPlayer class.

This code for firing rudal is placed in the existing KeyDown event procedure. Here is the modified code:

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960 &#124; private void FormFightingPlane_KeyDown( object sender, KeyEventArgs e){    if (btnGame.Text == "New Game" )        return ;    switch (e.KeyCode)    {        case Keys.A:            Player1.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player1.Location.Y < 0)                Player1.Location.Y = 0;            break ;        case Keys.Z:            Player1.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player1.Location.Y > pnlGame.ClientSize.Height –                Player1.Location.Height)                Player1.Location.Y = pnlGame.ClientSize.Height –                    Player1.Location.Height;            break ;        case Keys.S:            if (!Rudal1.IsVisible && Player1Rem > 0)            {                Player1Rem--;                lblRemPlayer1.Text = Player1Rem.ToString();                                 Rudal1.Location = new                    Rectangle(Player1.Location.X +                     Player1.Location.Width, Player1.Location.Y,                    Rudal1.MyImage.Width, Rudal1.MyImage.Height);                Rudal1.Place(MyGraphics);            }            break ;        case Keys.K:            Player2.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player2.Location.Y < 0)                Player2.Location.Y = 0;            break ;        case Keys.M:            Player2.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player2.Location.Y > pnlGame.ClientSize.Height –                Player2.Location.Height)                Player2.Location.Y = pnlGame.ClientSize.Height –                    Player2.Location.Height;            break ;        case Keys.J:            if (!Rudal2.IsVisible && Player2Rem > 0)            {                Player2Rem--;                lblRemPlayer2.Text = Player2Rem.ToString();                Rudal2.Location = new                    Rectangle(Player2.Location.X –                    Player2.Location.Width, Player2.Location.Y,                    Rudal1.MyImage.Width, Rudal1.MyImage.Height);                Rudal2.Place(MyGraphics);            }            break ;    }} &#124;

 |
| Step 26 | Save and run the project. Now, after the user presses S key and J key, the two rudals are displayed.![](Image00080.jpg)Figure 7.16 The two rudals appear when user press J and K keys |
| Step 27 | Once fired, the movement or displacement of the rudal is updated by the timGame control. You need the Click event code of btnGame to enable the timer (when a New Game is clicked) and to stop the timer (when Stop Game is clicked). You also need to clear the rudal when the Stop Game is clicked. A modified version of the Click procedure of btnGame is given as follows: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445 &#124; private void btnGame_Click( object sender, EventArgs e){    if (btnGame.Text == "New Game" )    {        MyGraphics.Clear(pnlGame.BackColor);        btnGame.Text = "Stop Game" ;        btnOption.Enabled = false ;        btnExit.Enabled = false ;        Player1Hit = 0;        Player2Hit = 0;        lblHitPlayer1.Text = "0" ;        lblHitPlayer2.Text = "0" ;        Player1Rem = RudalMax;        Player2Rem = RudalMax;        lblRemPlayer1.Text = Player1Rem.ToString();        lblRemPlayer2.Text = Player2Rem.ToString();        Player1.Location = new Rectangle(5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player1.MyImage.Height), Player1.MyImage.Width,            Player1.MyImage.Height);        Player2.Location = new Rectangle(pnlGame.ClientSize.Width –            Player2.MyImage.Width - 5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player2.MyImage.Height), Player2.MyImage.Width,            Player2.MyImage.Height);        Player1.Place(MyGraphics);        Player2.Place(MyGraphics);        timGame.Enabled = true ;        this .Focus();    }    else    {        timGame.Enabled = false ;        Player1.Remove(MyGraphics, MyBrush);        Player2.Remove(MyGraphics, MyBrush);        Rudal1.Remove(MyGraphics, MyBrush);        Rudal2.Remove(MyGraphics, MyBrush);        btnGame.Text = "New Game" ;        btnOption.Enabled = true ;        btnExit.Enabled = true ;        MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),            Brushes.Yellow, 530, 210);    }} &#124;

 |
| Step 28 | In the Tick event procedure timGame , you update the position of the rudal fired using the horizontal speed value and Move method. You also check whether rudal is past the edge of the panel. If so, you need to delete it from the panel to allow another throw. You also check the end of the game (both players are out of rudals and both players are not visible). When the game ends, btnGame button will be clicked: 

&#124; 12345678910111213141516171819202122232425 &#124; private void timGame_Tick( object sender, EventArgs e){    // status of rudal fired by player 1    if (Rudal1.IsVisible)    {        Rudal1.Move(MyGraphics, MyBrush, RudalSpeed, 0);        if (Rudal1.Location.X > pnlGame.ClientSize.Width)            // past the edge of the panel            Rudal1.Remove(MyGraphics, MyBrush);    }    //status of rudal fired by player 2    if (Rudal2.IsVisible)    {        Rudal2.Move(MyGraphics, MyBrush, -RudalSpeed, 0);        if (Rudal2.Location.X < 0)            // past the edge of the panel            Rudal2.Remove(MyGraphics, MyBrush);    }    // Checks game status    if (!Rudal1.IsVisible && Player1Rem == 0 && !Rudal2.IsVisible &&          Player2Rem == 0)        btnGame.PerformClick();} &#124;

Add this procedure to your project. In the code, you select the Interval property of the timer control by 50 milliseconds. This is a parameter that you can change as you like. |
| Step 29 | Save and run project. Make sure you still use the two player option. Click New Game . Click the S and J keys to throw rudal. Make sure the labels reflect the exact value of the remaining rudals. If rudal hits the player, the player's graphics will disappear. To bring it up again press one of the keys that move it up and down the panel, as shown in Figure 7.17. |
| Step 30 | If rudal is fired at or hits a player, another player will get point (a hit). You need a way to check for such collision. Because rectangular region defines moving object here, you need to know what if two rectangular regions intersect. In Visual C#, this test can be performed using ItersectsWith method of Rectangle structure.To see whether the two rectangular regions ( Rectangular1 and Rectangular2 ) intersect, you need to check the Boolean value of Rectangular1.IntersectsWith (Rectangular2) . If the value is True , then an intersection or collision occurs. If False , then there is no collision.![](Image00081.jpg)Figure 7.17 Both players now throw rudal at each otherTo use it on this project, you will add a method, Collide , to MovingRudal class. Open MovingRudal.cs file and add the following change: 

&#124; 123456789101112131415161718192021222324 &#124; using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;namespace FiringRudal{    class MovingRudal : TwoPlayer    {        public MovingRudal ()        {        }        public int XSpeed;        public int YSpeed;        public bool Collide(Rectangle r)        {            return ( this .Location.IntersectsWith(r));        }    }} &#124;

This method has a rectangular structural argument (r) for checking collision on the MovingRudal object.As an example of using this method, you can check whether Rudal1 collides with Player2 . The resulting Boolean value: Rudal1.Collide(Player2. Location) will be True if a collision occurs. If a collision occurs, you need to clear the rudal and update the thrower's score. |
| Step 31 | You check for collision between rudal and player in the Click event procedure of timGame . Modified code for checking collision and updating score are given as follows: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637 &#124; private void timGame_Tick( object sender, EventArgs e){    // status of rudal fired by player 1    if (Rudal1.IsVisible)    {        Rudal1.Move(MyGraphics, MyBrush, RudalSpeed, 0);        if (Rudal1.Location.X > pnlGame.ClientSize.Width)            // past the edge of the panel            Rudal1.Remove(MyGraphics, MyBrush);        else if (Rudal1.Collide(Player2.Location))        {            Player1Hit++;            lblHitPlayer1.Text = Player1Hit.ToString();            Rudal1.Remove(MyGraphics, MyBrush);        }    }    //status of rudal fired by player 2    if (Rudal2.IsVisible)    {        Rudal2.Move(MyGraphics, MyBrush, -RudalSpeed, 0);        if (Rudal2.Location.X < 0)            // past the edge of the panel            Rudal2.Remove(MyGraphics, MyBrush);        else if (Rudal2.Collide(Player1.Location))        {            Player2Hit++;            lblHitPlayer2.Text = Player2Hit.ToString();            Rudal2.Remove(MyGraphics, MyBrush);        }    }    // Checks game status    if (!Rudal1.IsVisible && Player1Rem == 0 && !Rudal2.IsVisible &&          Player2Rem == 0)        btnGame.PerformClick();} &#124;

 |
| Step 32 | Save and run project. Now if user fires rudal and hits another player, the rudal will disappear, but the player remains. You can now try it:![](Image00082.jpg)Figure 7.18 User fires rudal and hits another player, the rudal will disappear, but the player remains. |
| Step 33 | As designed, the players have no protection from rudal except for their ability to go up and down. You will change it. You will create two ufos roaming the playing field. This ufo will stop rudal fired.You will have two ufos, each represented by a MovingRudal object ( Ufo1 and Ufo2 ). The movements will be random, with few restrictions. Add the following form level declarations to your form to declare ufo objects and random number object: 

&#124; 12 &#124; MovingRudal Ufo1, Ufo2;Random MyRandom = new Random(); &#124;

Ufo will follow some rules. Ufo1 will only move vertically on the left side of the playing field, while Ufo2 will only move vertically on the right side of the playing field. The vertical speed will be random between values ​​1 and 4 (you can change it yourself). Ufo can move up and down. If it moves up, it will start from the bottom side of the playing field. If it moves down, it will start from the top side of the playing field. |
| Step 34 | Ufo is constructed in the Load procedure of form. Add the following four lines to this Load procedure to specify the creation of the MovingRudal objects for two ufos: 

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768 &#124; private void FormFightingPlane_Load( object sender, EventArgs e){    try    {        StreamReader fileInput =            new StreamReader(Application.StartupPath +            "\\plane.ini" );        NumberOfPlayer = Convert. ToInt32(fileInput.ReadLine());        Difficulty = Convert.ToInt32(fileInput.ReadLine());        fileInput.Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;    Player1Rem = RudalMax;    Player2Rem = RudalMax;    lblRemPlayer1.Text = Player1Rem.ToString();    lblRemPlayer2.Text = Player2Rem.ToString();    // Creates TwoPlayer objects    MyGraphics = pnlGame.CreateGraphics();    MyBrush = new SolidBrush(pnlGame.BackColor);    Player1 = new TwoPlayer();    Player2 = new TwoPlayer();    Player1.MyImage = Image.FromFile(Application.StartupPath +        "\\bomber1.png" );    Player2.MyImage = Image.FromFile(Application.StartupPath +        "\\bomber2.png" );    Rudal1 = new MovingRudal();    Rudal2 = new MovingRudal();    Rudal1.MyImage = Image.FromFile(Application.StartupPath +        "\\rudal1.png" );    Rudal2.MyImage = Image.FromFile(Application.StartupPath +        "\\rudal2.png" );    Ufo1 = new MovingRudal();    Ufo2 = new MovingRudal();    Ufo1.MyImage = Image.FromFile(Application.StartupPath +        "\\ufo.png" );    Ufo2.MyImage = Image.FromFile(Application.StartupPath +        "\\ufo.png" );    btnGame.Focus();} &#124;

 |
| Step 35 | Ufos are initially placed in the game field when New Game button is clicked. When this happens, the two ufos are randomly placed in the vertical restraints of the graphic object. And, both are assigned random speeds. The two ufos will be removed when Stop Game button is clicked. The Click procedure of the modified btnGame that does this job is given below: 

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960 &#124; private void btnGame_Click( object sender, EventArgs e){    if (btnGame.Text == "New Game" )    {        MyGraphics.Clear(pnlGame.BackColor);        btnGame.Text = "Stop Game" ;        btnOption.Enabled = false ;        btnExit.Enabled = false ;        Player1Hit = 0;        Player2Hit = 0;        lblHitPlayer1.Text = "0" ;        lblHitPlayer2.Text = "0" ;        Player1Rem = RudalMax;        Player2Rem = RudalMax;        lblRemPlayer1.Text = Player1Rem.ToString();        lblRemPlayer2.Text = Player2Rem.ToString();        Player1.Location = new Rectangle(5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player1.MyImage.Height), Player1.MyImage.Width,            Player1.MyImage.Height);        Player2.Location = new Rectangle(pnlGame.ClientSize.Width –            Player2.MyImage.Width - 5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player2.MyImage.Height), Player2.MyImage.Width,            Player2.MyImage.Height);        Player1.Place(MyGraphics);        Player2.Place(MyGraphics);        Ufo1.Location = new Rectangle(( int )(0.5 *            pnlGame.ClientSize.Width - Ufo1.MyImage.Width),            MyRandom.Next(pnlGame.ClientSize.Height),            Ufo1.MyImage.Width, Ufo1.MyImage.Height);        Ufo2.Location = new Rectangle(( int )(0.5 *            pnlGame.ClientSize.Width),            MyRandom.Next(pnlGame.ClientSize.Height),            Ufo2.MyImage.Width, Ufo2.MyImage.Height);        Ufo1.YSpeed = UfoSpeed();        Ufo2.YSpeed = UfoSpeed();        Ufo1.Place(MyGraphics);        Ufo2.Place(MyGraphics);        timGame.Enabled = true ;        this .Focus();    }    else    {        timGame.Enabled = false ;        Player1.Remove(MyGraphics, MyBrush);        Player2.Remove(MyGraphics, MyBrush);        Rudal1.Remove(MyGraphics, MyBrush);        Rudal2.Remove(MyGraphics, MyBrush);        Ufo1.Remove(MyGraphics, MyBrush);        Ufo2.Remove(MyGraphics, MyBrush);        btnGame.Text = "New Game" ;        btnOption.Enabled = true ;        btnExit.Enabled = true ;        MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),            Brushes.Yellow, 280, 160);    }} &#124;

Ufo1 is placed just to the left of the center of the panel control, while Ufo2 is to the right of the center of the panel control.Notice how both ufos are randomly positioned vertically. |
| Step 36 | The speed of the ufo is assigned using a general function, UfoSpeed . As mentioned, you choose this value randomly, between 1 and 4\. Speed ​​can be positive (for downward movement) or negative (for upward movement): 

&#124; 1234567891011 &#124; private int UfoSpeed(){    const int SpeedMin = 1;    const int SpeedMax = 4;    int Speed;    Speed = MyRandom.Next(SpeedMax - SpeedMin + 1) + SpeedMin;    if (MyRandom.Next(2) == 0)        Speed = -Speed;    return (Speed);} &#124;

 |
| Step 37 | The movement of the ufo is updated on the Tick event of timGame timer. For each update, for each ufo, you need to do these steps: 
*   Move ufo using YSpeed ​​property.
*   Check whether ufo has come out of the boundary of the game field.
*   If ufo goes out of the boundary of the game field, do this: Calculate new speed; If the speed is positive, position ufo to the top edge of the playing field so that it can move down; If the speed is negative, position ufo to the bottom edge of the playing field so that it can move up;
*   After moving or repositioning the ufo, check whether the fired rudal collides with it. If there is a collision, remove the rudal from the game field.

The Tick event procedure of the modified timGame control is given as follows:

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273747576 &#124; private void timGame_Tick( object sender, EventArgs e){    // Moves ufo    Ufo1.Move(MyGraphics, MyBrush, 0, Ufo1.YSpeed);    if (Ufo1.Location.Y < -Ufo1.MyImage.Height &#124;&#124;        Ufo1.Location.Y > pnlGame.ClientSize.Height)    {        // Recalculates speed        Ufo1.YSpeed = UfoSpeed();        if (Ufo1.YSpeed > 0)            Ufo1.Location.Y = -Ufo1.MyImage.Height;        else            Ufo1.Location.Y = pnlGame.ClientSize.Height;    }    Ufo2.Move(MyGraphics, MyBrush, 0, Ufo2.YSpeed);    if (Ufo2.Location.Y < -Ufo2.MyImage.Height &#124;&#124;        Ufo2.Location.Y > pnlGame.ClientSize.Height)    {        // Recalculates speed        Ufo2.YSpeed = UfoSpeed();        if (Ufo2.YSpeed > 0)            Ufo2.Location.Y = -Ufo2.MyImage.Height;        else            Ufo2.Location.Y = pnlGame.ClientSize.Height;    }    // status of rudal fired by player 1    if (Rudal1.IsVisible)    {        Rudal1.Move(MyGraphics, MyBrush, RudalSpeed, 0);        if (Rudal1.Location.X > pnlGame.ClientSize.Width)            // past the edge of the panel            Rudal1.Remove(MyGraphics, MyBrush);        else if (Rudal1.Collide(Player2.Location))        {            Player1Hit++;            lblHitPlayer1.Text = Player1Hit.ToString();            Rudal1.Remove(MyGraphics, MyBrush);        }        else if (Rudal1.Collide(Ufo1.Location) &#124;&#124;            Rudal1.Collide(Ufo2.Location))        {            Rudal1.Remove(MyGraphics, MyBrush);        }    }    //status of rudal fired by player 2    if (Rudal2.IsVisible)    {        Rudal2.Move(MyGraphics, MyBrush, -RudalSpeed, 0);        if (Rudal2.Location.X < 0)            // past the edge of the panel            Rudal2.Remove(MyGraphics, MyBrush);        else if (Rudal2.Collide(Player1.Location))        {            Player2Hit++;            lblHitPlayer2.Text = Player2Hit.ToString();            Rudal2.Remove(MyGraphics, MyBrush);        }        else if (Rudal2.Collide(Ufo1.Location) &#124;&#124;            Rudal2.Collide(Ufo2.Location))        {            Rudal2.Remove(MyGraphics, MyBrush);        }    }    // Checks game status    if (!Rudal1.IsVisible && Player1Rem == 0 && !Rudal2.IsVisible &&          Player2Rem == 0)        btnGame.PerformClick();} &#124;

 |
| Step 38 | Save and run project. The two ufos move up and down and can block rudals fired by players:![](Image00083.jpg)Figure 2.18 The two ufos randomly move up and down and can block rudals fired by players |
| Step 39 | By using SoundPlayer class, which is located in the using System.Media namespace, you can add sound to this game.The SoundPlayer class is used to play sound represented by wav file. There are a number of wav files provided in the bin\Debug folder in your project: 

&#124; throw.wav &#124; Sound is played when the rudal is fired. &#124;
&#124; hit.wav &#124; Sound is played when rudal hits a ufo. &#124;
&#124; ouch.wav &#124; Sound is played when rudal hits a player. &#124;
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

&#124; 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950515253545556575859606162636465666768697071727374757677787980 &#124; private void FormFightingPlane_Load( object sender, EventArgs e){    try    {        StreamReader fileInput =            new StreamReader(Application.StartupPath +            "\\plane.ini" );        NumberOfPlayer = Convert. ToInt32(fileInput.ReadLine());        Difficulty = Convert.ToInt32(fileInput.ReadLine());        fileInput.Close();    }    catch    {         NumberOfPlayer = 1;         Difficulty = 1;    }    // Makes form visible so options can be clicked    this .Show();    pnlOption.Visible = true ;    if (Difficulty == 1)        rdoEasiest.PerformClick();    else if (Difficulty == 2)        rdoEasy.PerformClick();    else if (Difficulty == 3)        rdoHard.PerformClick();    else        rdoHardest.PerformClick();    if (NumberOfPlayer == 1)        rdoOnePlayer.PerformClick();    else        rdoTwoPlayers.PerformClick();    pnlOption.Visible = false ;    Player1Rem = RudalMax;    Player2Rem = RudalMax;    lblRemPlayer1.Text = Player1Rem.ToString();    lblRemPlayer2.Text = Player2Rem.ToString();    // Creates TwoPlayer objects    MyGraphics = pnlGame.CreateGraphics();    MyBrush = new SolidBrush(pnlGame.BackColor);    Player1 = new TwoPlayer();    Player2 = new TwoPlayer();    Player1.MyImage = Image.FromFile(Application.StartupPath +        "\\bomber1.png" );    Player2.MyImage = Image.FromFile(Application.StartupPath +        "\\bomber2.png" );    Rudal1 = new MovingRudal();    Rudal2 = new MovingRudal();    Rudal1.MyImage = Image.FromFile(Application.StartupPath +        "\\rudal1.png" );    Rudal2.MyImage = Image.FromFile(Application.StartupPath +        "\\rudal2.png" );    Ufo1 = new MovingRudal();    Ufo2 = new MovingRudal();    Ufo1.MyImage = Image.FromFile(Application.StartupPath +        "\\ufo.png" );    Ufo2.MyImage = Image.FromFile(Application.StartupPath +        "\\ufo.png" );    SoundThrow = new SoundPlayer(Application.StartupPath +        "\\throw.wav" );    SoundHit = new SoundPlayer(Application.StartupPath +        "\\hit.wav" );    SoundOuch = new SoundPlayer(Application.StartupPath +        "\\ouch.wav" );    SoundGameOver = new SoundPlayer(Application.StartupPath +        "\\gameover.wav" );    SoundThrow.Load();    SoundHit.Load();    SoundOuch.Load();    btnGame.Focus();} &#124;

 |
| Step 41 | SoundThrow will be played when rudal is fired. This occurs in the KeyDown event procedure of the form. The modified code is given the following: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061 &#124; private void FormFightingPlane_KeyDown( object sender, KeyEventArgs e){    if (btnGame.Text == "New Game" )        return ;    switch (e.KeyCode)    {        case Keys.A:            Player1.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player1.Location.Y < 0)                Player1.Location.Y = 0;            break ;        case Keys.Z:            Player1.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player1.Location.Y > pnlGame.ClientSize.Height –                Player1.Location.Height)                Player1.Location.Y = pnlGame.ClientSize.Height –                    Player1.Location.Height;            break ;        case Keys.S:            if (!Rudal1.IsVisible && Player1Rem > 0)            {                SoundThrow.Play();                Player1Rem--;                lblRemPlayer1.Text = Player1Rem.ToString();                                 Rudal1.Location = new                    Rectangle(Player1.Location.X +                     Player1.Location.Width, Player1.Location.Y,                    Rudal1.MyImage.Width, Rudal1.MyImage.Height);                Rudal1.Place(MyGraphics);            }            break ;        case Keys.K:            Player2.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player2.Location.Y < 0)                Player2.Location.Y = 0;            break ;        case Keys.M:            Player2.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player2.Location.Y > pnlGame.ClientSize.Height –                Player2.Location.Height)                Player2.Location.Y = pnlGame.ClientSize.Height –                    Player2.Location.Height;            break ;        case Keys.J:            if (!Rudal2.IsVisible && Player2Rem > 0)            {                SoundThrow.Play();                Player2Rem--;                lblRemPlayer2.Text = Player2Rem.ToString();                Rudal2.Location = new                    Rectangle(Player2.Location.X –                    Player2.Location.Width, Player2.Location.Y,                    Rudal1.MyImage.Width, Rudal1.MyImage.Height);                Rudal2.Place(MyGraphics);            }            break ;    }} &#124;

 |
| Step 42 | SoundHit will be played when a ufo is hit by rudal throw. SoundOuch will be played when a player is hit by rudal throw and SoundGameOver will be played when both players run out of rudals. All this happened at the Tick event of timGame timer: 

&#124; 12345678910111213141516171819202122232425262728293031323334353637383940414243444546474849505152535455565758596061626364656667686970717273747576777879808182 &#124; private void timGame_Tick( object sender, EventArgs e){    // Moves ufo    Ufo1.Move(MyGraphics, MyBrush, 0, Ufo1.YSpeed);    if (Ufo1.Location.Y < -Ufo1.MyImage.Height &#124;&#124;        Ufo1.Location.Y > pnlGame.ClientSize.Height)    {        // Recalculates speed        Ufo1.YSpeed = UfoSpeed();        if (Ufo1.YSpeed > 0)            Ufo1.Location.Y = -Ufo1.MyImage.Height;        else            Ufo1.Location.Y = pnlGame.ClientSize.Height;    }    Ufo2.Move(MyGraphics, MyBrush, 0, Ufo2.YSpeed);    if (Ufo2.Location.Y < -Ufo2.MyImage.Height &#124;&#124;        Ufo2.Location.Y > pnlGame.ClientSize.Height)    {        // Recalculates speed        Ufo2.YSpeed = UfoSpeed();        if (Ufo2.YSpeed > 0)            Ufo2.Location.Y = -Ufo2.MyImage.Height;        else            Ufo2.Location.Y = pnlGame.ClientSize.Height;    }    // status of rudal fired by player 1    if (Rudal1.IsVisible)    {        Rudal1.Move(MyGraphics, MyBrush, RudalSpeed, 0);        if (Rudal1.Location.X > pnlGame.ClientSize.Width)            // past the edge of the panel            Rudal1.Remove(MyGraphics, MyBrush);        else if (Rudal1.Collide(Player2.Location))        {            SoundOuch.Play();            Player1Hit++;            lblHitPlayer1.Text = Player1Hit.ToString();            Rudal1.Remove(MyGraphics, MyBrush);        }        else if (Rudal1.Collide(Ufo1.Location) &#124;&#124;            Rudal1.Collide(Ufo2.Location))        {            SoundHit.Play();            Rudal1.Remove(MyGraphics, MyBrush);        }    }    //status of rudal fired by player 2    if (Rudal2.IsVisible)    {        Rudal2.Move(MyGraphics, MyBrush, -RudalSpeed, 0);        if (Rudal2.Location.X < 0)            // past the edge of the panel            Rudal2.Remove(MyGraphics, MyBrush);        else if (Rudal2.Collide(Player1.Location))        {            SoundOuch.Play();            Player2Hit++;            lblHitPlayer2.Text = Player2Hit.ToString();            Rudal2.Remove(MyGraphics, MyBrush);        }        else if (Rudal2.Collide(Ufo1.Location) &#124;&#124;            Rudal2.Collide(Ufo2.Location))        {            SoundHit.Play();            Rudal2.Remove(MyGraphics, MyBrush);        }    }    // Checks game status    if (!Rudal1.IsVisible && Player1Rem == 0 && !Rudal2.IsVisible &&          Player2Rem == 0)        SoundGameOver.PlaySync();        btnGame.PerformClick();} &#124;

 |
| Step 43 | Save and run project. Play the two player game. You can now listen to the sounds of firing, hitting and ouch. And, play until the rudal is zero for both players so that the gameover sound is played. |
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

&#124; 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566 &#124; private void btnGame_Click( object sender, EventArgs e){    if (btnGame.Text == "New Game" )    {        MyGraphics.Clear(pnlGame.BackColor);        btnGame.Text = "Stop Game" ;        btnOption.Enabled = false ;        btnExit.Enabled = false ;        Player1Hit = 0;        Player2Hit = 0;        lblHitPlayer1.Text = "0" ;        lblHitPlayer2.Text = "0" ;        Player1Rem = RudalMax;        Player2Rem = RudalMax;        lblRemPlayer1.Text = Player1Rem.ToString();        lblRemPlayer2.Text = Player2Rem.ToString();        Player1.Location = new Rectangle(5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player1.MyImage.Height), Player1.MyImage.Width,            Player1.MyImage.Height);        Player2.Location = new Rectangle(pnlGame.ClientSize.Width –            Player2.MyImage.Width - 5, ( int )(0.5 *            pnlGame.ClientSize.Height - 0.5 *            Player2.MyImage.Height), Player2.MyImage.Width,            Player2.MyImage.Height);        Player1.Place(MyGraphics);        Player2.Place(MyGraphics);        Ufo1.Location = new Rectangle(( int )(0.5 *            pnlGame.ClientSize.Width - Ufo1.MyImage.Width),            MyRandom.Next(pnlGame.ClientSize.Height),            Ufo1.MyImage.Width, Ufo1.MyImage.Height);        Ufo2.Location = new Rectangle(( int )(0.5 *            pnlGame.ClientSize.Width),            MyRandom.Next(pnlGame.ClientSize.Height),            Ufo2.MyImage.Width, Ufo2.MyImage.Height);        Ufo1.YSpeed = UfoSpeed();        Ufo2.YSpeed = UfoSpeed();        Ufo1.Place(MyGraphics);        Ufo2.Place(MyGraphics);        timGame.Enabled = true ;        if (NumberOfPlayer == 1)            timComputer.Enabled = true ;        this .Focus();    }    else    {        timGame.Enabled = false ;        timComputer.Enabled = false ;        Player1.Remove(MyGraphics, MyBrush);        Player2.Remove(MyGraphics, MyBrush);        Rudal1.Remove(MyGraphics, MyBrush);        Rudal2.Remove(MyGraphics, MyBrush);        Ufo1.Remove(MyGraphics, MyBrush);        Ufo2.Remove(MyGraphics, MyBrush);        btnGame.Text = "New Game" ;        btnOption.Enabled = true ;        btnExit.Enabled = true ;        MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),            Brushes.Yellow, 280, 160);    }} &#124;

 |
| Step 46 | Now, you will write down the rules of the computer game. You will start with a simple random rule. In this rule, the computer will only move up and down in the game field, and occasionally throw rudal. The only non-random element added is that the computer can only throw rudal if it has at least as many rudals as the player has. This is to prevent the computer from firing all the rudals and becoming an easy target for human. The rules used are: 
*   Generate a random value from 0 to 4.
*   If the random value is 0, throw rudal, if computer has at least as many as the remaining rudals owned by the player.
*   If the random value is 1 or 2, move up.
*   If the random value is 3 or 4, make down.

With this rule, rudals are fired one by one in five up or down movements. The computer will move up 2 movements of 5 movements and move down 2 movements from 5 movements.In detailed (smart) logic game rules, you only need to think about how you want to win the game. The smart rule is to throw if other players are "within a certain range". And, avoid human player if he fires rudal. In the rules given here, "in range" means that the vertical difference between two players is not more than 80 percent of the player's height:

*   If it is "in range" and the computer has at least as many rudals as the player has, the computer will throw rudal.
*   If the human player fires rudal or the computer no longer has the remaining rudals, the computer will make a defensive move: If human player is above the computer player, the computer will move down; If the human player is below the computer player, the computer will move up.
*   Otherwise, the computer will make an attacking move: If the human player is above the computer player, the computer will move up; If the human player is under the computer player, the computer will move down.

Note that the computer can only throw rudal when it has at least as many rudals left as the player has. You certainly don't want a computer to run out of rudals before a human player.The code for both of these logic is placed in the Tick event procedure of timComputer control. Before writing this code, you need to overcome the problem of how you make computer player throw, move up, or move down. With human as the second player, pressing J key will make player 2 throw, K key pressing will make player 2 move up and pressing M key will make player 2 move down. It would be better if there was a way to make the computer press the same key for the job.Fortunately, Visual C# has a procedure named SendKeys that can be used to simulate key presses on the keyboard. To press J key, the code is: SendKeys.Send("K") . Therefore, for computer player, you will use SendKeys procedure to implement computer actions.The Tick event procedure of timComputer control which implements computer player logic is given as follows:

&#124; 1234567891011121314151617181920212223242526272829303132333435363738 &#124; private void timComputer_Tick( object sender, EventArgs e){    int i;    if (MyRandom.Next(100) < RandComputer)    {        i = MyRandom.Next(5); // Moves randomly        if (i == 0)        {            if (Player2Rem >= Player1Rem)                SendKeys.Send( "J" ); // Fires rudal        }        else if (i <= 2)            SendKeys.Send( "K" ); // Moves up        else            SendKeys.Send( "M" ); // Moves down    }    else    {        if (Math.Abs(Player1.Location.Y - Player2.Location.Y) <            ( int )(0.8 * Player1.MyImage.Height) && Player2Rem >=            Player1Rem)            SendKeys.Send( "J" ); // Fires rudal        if (Rudal1.IsVisible &#124;&#124; Player2Rem == 0)        {            if (Player1.Location.Y - Player2.Location.Y < 0)                SendKeys.Send( "M" ); // Moves up            else                SendKeys.Send( "K" ); // Moves down        }        else        {            if (Player1.Location.Y - Player2.Location.Y < 0)                SendKeys.Send( "K" ); // Moves up            else                SendKeys.Send( "M" ); // Moves down        }    }} &#124;

 |
| Step 47 | Save and run project. Click Options button, choose one player. Then, choose one level of difficulty. Click OK , then New Game . Now your opponent is a computer. |
|  |  |

| TwoPlayer.cs |
| 12345678910111213141516171819202122232425262728293031323334353637383940 | using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;namespace FiringRudal{    class TwoPlayer    {        public TwoPlayer ()        {        }        public Image MyImage;        public Rectangle Location;        public bool IsVisible = false ;        public void Place(Graphics g)        {            g.DrawImage( this .MyImage, this .Location);            this .IsVisible = true ;        }        public void Move(Graphics g, Brush bc, int dx, int dy)        {            g.FillRectangle(bc, this .Location);            this .Location.X += dx;            this .Location.Y += dy;            g.DrawImage( this .MyImage, this .Location);        }        public void Remove(Graphics g, Brush bc)        {            g.FillRectangle(bc, this .Location);            this .IsVisible = false ;        }    }} |
|  |  |

| MovingRudal.cs |
| 123456789101112131415161718192021222324 | using System;using System.Collections.Generic;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Drawing;namespace FiringRudal{    class MovingRudal : TwoPlayer    {        public MovingRudal ()        {        }        public int XSpeed;        public int YSpeed;        public bool Collide(Rectangle r)        {            return ( this .Location.IntersectsWith(r));        }    }} |
|  |  |

| FormFightingPlane.cs |
| 123456789101112131415161718192021222324252627282930313233343536373839404142434445464748495051525354555657585960616263646566676869707172737475767778798081828384858687888990919293949596979899100101102103104105106107108109110111112113114115116117118119120121122123124125126127128129130131132133134135136137138139140141142143144145146147148149150151152153154155156157158159160161162163164165166167168169170171172173174175176177178179180181182183184185186187188189190191192193194195196197198199200201202203204205206207208209210211212213214215216217218219220221222223224225226227228229230231232234235236237238239240241242243244245246247248249250251252253254255256257258259260261262263264265266267268269270271272273274275276277278279280281282283284285286287288289290291292293294295296297298299300301302303304305306307308309310311312313314315316317318319320321322323324325326327328329330331332333334335336337338339340341342343344345346347348349350351352353354355356357358359360361362363364365366367368369370371372373374375376377378379380381382383384385386387388389390391392393394395396397398399400401402403404405406407408409410411412413414415416417418419420421422423424425426427428429430431432433434435436437438439440441442443444445446447448448450451452453454455456457458459460461462463464465466467468469470471472473474475476477478479480481482483484485486487488489490491492493494495496497498499500501502503504505506507508 | using System;using System.Collections.Generic;using System.ComponentModel;using System.Data;using System.Drawing;using System.Linq;using System.Text;using System.Threading.Tasks;using System.Windows.Forms;using System.IO;using System.Media;namespace FiringRudal{    public partial class FormFightingPlane : Form    {        int NumberOfPlayer, Difficulty;        Graphics MyGraphics;        Brush MyBrush;        TwoPlayer Player1, Player2;        int Player1Hit, Player2Hit, Player1Rem, Player2Rem;        const int RudalMax = 20;        const int PlayerIncrement = 10;        MovingFire Rudal1, Rudal2;        const int RudalSpeed = 30;        MovingFire Ufo1, Ufo2;        Random MyRandom = new Random();        SoundPlayer SoundFire, SoundHit, SoundOuch, SoundGameOver;        int RandComputer, TimeComputer;        public FormFightingPlane ()        {            InitializeComponent();        }        private void btnOption_Click( object sender, EventArgs e)        {            btnGame.Enabled = false ;            btnOption.Enabled = false ;            btnExit.Enabled = false ;            pnlOption.Visible = true ;            lblInstructionPlayer2.Visible = false ;        }        private void btnUp_Click( object sender, EventArgs e)        {            SendKeys.Send( "A" ); // Moves up        }        private void btnDown_Click( object sender, EventArgs e)        {            SendKeys.Send( "Z" ); // Moves down        }        private void btnFire_Click( object sender, EventArgs e)        {            SendKeys.Send( "S" ); // Fires        }        private void btnUp2_Click( object sender, EventArgs e)        {            Player2.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);            if (Player2.Location.Y < 0)                Player2.Location.Y = 0;        }        private void btnDown2_Click( object sender, EventArgs e)        {            Player2.Move(MyGraphics, MyBrush, 0, PlayerIncrement);            if (Player2.Location.Y >                    pnlGame.ClientSize.Height - Player2.Location.Height)                Player2.Location.Y =                    pnlGame.ClientSize.Height - Player2.Location.Height;        }        private void btnFire2_Click( object sender, EventArgs e)        {            if (!Rudal2.IsVisible && Player2Rem > 0)            {                SoundFire.Play();                Player2Rem--;                lblRemPlayer2.Text = Player2Rem.ToString();                Rudal2.Location =                    new Rectangle(Player2.Location.X - Player2.Location.Width,                    Player2.Location.Y, Rudal1.MyImage.Width,                    Rudal1.MyImage.Height);                Rudal2.Place(MyGraphics);            }        }        private void FormFightingPlane_Load( object sender, EventArgs e)        {            try            {                StreamReader fileInput = new                    StreamReader(Application.StartupPath                    + "\\plane.ini" );                NumberOfPlayer = Convert.ToInt32(fileInput.ReadLine());                Difficulty = Convert.ToInt32(fileInput.ReadLine());                fileInput.Close();                          }            catch            {                NumberOfPlayer = 1;                Difficulty = 1;            }            // Makes form visible so options can be clicked            this .Show();            pnlOption.Visible = true ;            if (Difficulty == 1)                rdoEasiest.PerformClick();            else if (Difficulty == 2)                rdoEasy.PerformClick();            else if (Difficulty == 3)                rdoHard.PerformClick();            else                rdoHardest.PerformClick();            if (NumberOfPlayer == 1)                rdoOnePlayer.PerformClick();            else                rdoTwoPlayers.PerformClick();            pnlOption.Visible = false ;            Player1Rem = RudalMax;            Player2Rem = RudalMax;            lblRemPlayer1.Text = Player1Rem.ToString();            lblRemPlayer2.Text = Player2Rem.ToString();            // Creates TwoPlayer objects            MyGraphics = pnlGame.CreateGraphics();            MyBrush = new SolidBrush(pnlGame.BackColor);            Player1 = new TwoPlayer();            Player2 = new TwoPlayer();            Player1.MyImage = Image.FromFile(Application.StartupPath +                "\\bomber1.png" );            Player2.MyImage = Image.FromFile(Application.StartupPath +                "\\bomber2.png" );            Rudal1 = new MovingFire();            Rudal2 = new MovingFire();            Rudal1.MyImage = Image.FromFile(Application.StartupPath +                "\\rudal4.png" );            Rudal2.MyImage = Image.FromFile(Application.StartupPath +                "\\rudal2.png" );            Ufo1 = new MovingFire();            Ufo2 = new MovingFire();            Ufo1.MyImage = Image.FromFile(Application.StartupPath +                "\\ufo2.png" );            Ufo2.MyImage = Image.FromFile(Application.StartupPath +                "\\ufo4.png" );            SoundFire = new SoundPlayer(Application.StartupPath +                "\\throw.wav" );            SoundHit = new SoundPlayer(Application.StartupPath + "\\hit.wav" );            SoundOuch = new SoundPlayer(Application.StartupPath + "\\ouch.wav" );            SoundGameOver = new SoundPlayer(Application.StartupPath +                "\\gameover.wav" );            SoundFire.Load();            SoundHit.Load();            SoundOuch.Load();            btnGame.Focus();        }        private void rdoPlayer_Click( object sender, EventArgs e)        {            RadioButton ButtonClicked;            ButtonClicked = (RadioButton) sender;            if (ButtonClicked.Text == "One" )            {                NumberOfPlayer = 1;                lblPlayer1.Text = "You:" ;                lblPlayer2.Text = "Computer:" ;                lblInstructionPlayer2.Visible = false ;                grpDifficulty.Enabled = true ;            }            else            {                NumberOfPlayer = 2;                lblPlayer1.Text = "Player 1:" ;                lblPlayer2.Text = "Player 2:" ;                lblInstructionPlayer2.Visible = true ;                grpDifficulty.Enabled = false ;            }        }        private void rdoDifficulty_Click( object sender, EventArgs e)        {            RadioButton ButtonClicked;            ButtonClicked = (RadioButton)sender;            switch (ButtonClicked.Text)            {                case "Easiest" :                    Difficulty = 1;                    RandComputer = 100;                    TimeComputer = 1000;                    break ;                case "Easy" :                    Difficulty = 2;                    RandComputer = 75;                    TimeComputer = 750;                    break ;                case "Hard" :                    Difficulty = 3;                    RandComputer = 50;                    TimeComputer = 500;                    break ;                case "Hardest" :                    Difficulty = 4;                    RandComputer = 25;                    TimeComputer = 250;                    break ;            }            timComputer.Interval = TimeComputer;        }        private void btnOK_Click( object sender, EventArgs e)        {            btnGame.Enabled = true ;            btnOption.Enabled = true ;            btnExit.Enabled = true ;            pnlOption.Visible = false ;        }        private void FormFightingPlane_FormClosing( object sender, FormClosingEventArgs e)        {            StreamWriter FileOutput = new StreamWriter(Application.StartupPath +                "\\plane.ini" );            FileOutput.WriteLine(NumberOfPlayer);            FileOutput.WriteLine(Difficulty);            FileOutput.Close();        }        private void btnExit_Click( object sender, EventArgs e)        {            this .Close();        }        private void btnGame_Click( object sender, EventArgs e)        {            if (btnGame.Text == "New Game" )            {                MyGraphics.Clear(pnlGame.BackColor);                btnGame.Text = "Stop Game" ;                btnOption.Enabled = false ;                btnExit.Enabled = false ;                Player1Hit = 0;                Player2Hit = 0;                lblHitPlayer1.Text = "0" ;                lblHitPlayer2.Text = "0" ;                Player1Rem = RudalMax;                Player2Rem = RudalMax;                lblRemPlayer1.Text = Player1Rem.ToString();                lblRemPlayer2.Text = Player2Rem.ToString();                Player1.Location =                    new Rectangle(5, ( int )(0.5 * pnlGame.ClientSize.Height - 0.5 *                    Player1.MyImage.Height), Player1.MyImage.Width,                    Player1.MyImage.Height);                Player2.Location =                   new Rectangle(pnlGame.ClientSize.Width –                   Player2.MyImage.Width - 5,                   ( int )(0.5 * pnlGame.ClientSize.Height - 0.5 *                   Player2.MyImage.Height), Player2.MyImage.Width,                   Player2.MyImage.Height);                Player1.Place(MyGraphics);                Player2.Place(MyGraphics);                Ufo1.Location =                    new Rectangle(( int )(0.5 * pnlGame.ClientSize.Width –                    Ufo1.MyImage.Width),                    MyRandom.Next(pnlGame.ClientSize.Height),                    Ufo1.MyImage.Width, Ufo1.MyImage.Height);                Ufo2.Location = new Rectangle(( int )(0.5 *                    pnlGame.ClientSize.Width),                    MyRandom.Next(pnlGame.ClientSize.Height),                    Ufo2.MyImage.Width,                    Ufo2.MyImage.Height);                Ufo1.YSpeed = UfoSpeed();                Ufo2.YSpeed = UfoSpeed();                Ufo1.Place(MyGraphics);                Ufo2.Place(MyGraphics);                timGame.Enabled = true ;                if (NumberOfPlayer == 1)                    timComputer.Enabled = true ;                this .Focus();            }            else            {                timComputer.Enabled = false ;                timGame.Enabled = false ;                Player1.Remove(MyGraphics, MyBrush);                Player2.Remove(MyGraphics, MyBrush);                Rudal1.Remove(MyGraphics, MyBrush);                Rudal2.Remove(MyGraphics, MyBrush);                Ufo1.Remove(MyGraphics, MyBrush);                Ufo2.Remove(MyGraphics, MyBrush);                btnGame.Text = "New Game" ;                btnOption.Enabled = true ;                btnExit.Enabled = true ;                MyGraphics.DrawString( "Game Over" , new Font( "Arial" , 24),                    Brushes.Yellow, 530, 210);            }        }        private int UfoSpeed()        {            const int SpeedMin = 1;            const int SpeedMax = 4;            int Speed;            Speed = MyRandom.Next(SpeedMax - SpeedMin + 1) + SpeedMin;            if (MyRandom.Next(2) == 0)                Speed = -Speed;            return (Speed);        }        private void FormFightingPlane_KeyDown( object sender, KeyEventArgs e)        {            if (btnGame.Text == "New Game" )                return ;            switch (e.KeyCode)            {                case Keys.A:                    Player1.Move(MyGraphics, MyBrush, 0, -PlayerIncrement);                    if (Player1.Location.Y < 0)                        Player1.Location.Y = 0;                    break ;                case Keys.Z:                    Player1.Move(MyGraphics, MyBrush, 0, PlayerIncrement);                    if (Player1.Location.Y >                            pnlGame.ClientSize.Height - Player1.Location.Height)                        Player1.Location.Y =                            pnlGame.ClientSize.Height - Player1.Location.Height;                    break ;                case Keys.S:                    if (!Rudal1.IsVisible && Player1Rem > 0)                    {                        SoundFire.Play();                        Player1Rem--;                        lblRemPlayer1.Text = Player1Rem.ToString();                        Rudal1.Location =                            new Rectangle(Player1.Location.X +                            Player1.Location.Width,                            Player1.Location.Y, Rudal1.MyImage.Width,                            Rudal1.MyImage.Height);                        Rudal1.Place(MyGraphics);                    }                    break ;                case Keys.K:                    btnUp2.PerformClick();                    break ;                case Keys.M:                    btnDown2.PerformClick();                    break ;                case Keys.J:                    btnFire2.PerformClick();                    break ;            }        }        private void timGame_Tick( object sender, EventArgs e)        {            // Moves shield            Ufo1.Move(MyGraphics, MyBrush, 0, Ufo1.YSpeed);            if (Ufo1.Location.Y < -Ufo1.MyImage.Height &#124;&#124;                Ufo1.Location.Y > pnlGame.ClientSize.Height)            {                // Recalculates speed                Ufo1.YSpeed = UfoSpeed();                if (Ufo1.YSpeed > 0)                {                    Ufo1.Location.Y = -Ufo1.MyImage.Height;                }                else                    Ufo1.Location.Y = pnlGame.ClientSize.Height;            }            Ufo2.Move(MyGraphics, MyBrush, 0, Ufo2.YSpeed);            if (Ufo2.Location.Y < -Ufo2.MyImage.Height &#124;&#124;                Ufo2.Location.Y > pnlGame.ClientSize.Height)            {                // Recalculates speed                Ufo2.YSpeed = UfoSpeed();                if (Ufo2.YSpeed > 0)                    Ufo2.Location.Y = -Ufo2.MyImage.Height;                else                    Ufo2.Location.Y = pnlGame.ClientSize.Height;            }            // status of fire thrown by player 1            if (Rudal1.IsVisible)            {                Rudal1.Move(MyGraphics, MyBrush, RudalSpeed, 0);                if (Rudal1.Location.X > pnlGame.ClientSize.Width)                    // past the edge of the panel                    Rudal1.Remove(MyGraphics, MyBrush);                else if (Rudal1.Collide(Player2.Location))                {                    SoundOuch.Play();                    Player1Hit++;                    lblHitPlayer1.Text = Player1Hit.ToString();                    Rudal1.Remove(MyGraphics, MyBrush);                }                else if (Rudal1.Collide(Ufo1.Location) &#124;&#124;                    Rudal1.Collide(Ufo2.Location))                {                    SoundHit.Play();                    Rudal1.Remove(MyGraphics, MyBrush);                }            }            //status of fire thrown fby player 2            if (Rudal2.IsVisible)            {                Rudal2.Move(MyGraphics, MyBrush, -RudalSpeed, 0);                if (Rudal2.Location.X < 0)                    // past the edge of the panel                    Rudal2.Remove(MyGraphics, MyBrush);                else if (Rudal2.Collide(Player1.Location))                {                    SoundOuch.Play();                    Player2Hit++;                    lblHitPlayer2.Text = Player2Hit.ToString();                    Rudal2.Remove(MyGraphics, MyBrush);                }                else if (Rudal2.Collide(Ufo1.Location) &#124;&#124;                    Rudal2.Collide(Ufo2.Location))                {                    SoundHit.Play();                    Rudal2.Remove(MyGraphics, MyBrush);                }            }            // Checks game status            if (!Rudal1.IsVisible && Player1Rem == 0 && !Rudal2.IsVisible &&                Player2Rem == 0)            {                SoundGameOver.PlaySync();                btnGame.PerformClick();            }        }        private void timComputer_Tick( object sender, EventArgs e)        {            int i;            if (MyRandom.Next(100) < RandComputer)            {                i = MyRandom.Next(5); // Moves randomly                if (i == 0)                {                    if (Player2Rem >= Player1Rem)                        btnFire2.PerformClick(); // Fires rudal                }                else if (i <= 2)                    btnUp2.PerformClick(); // Moves up                else                    btnDown2.PerformClick(); // Moves down            }            else            {                if (Math.Abs(Player1.Location.Y - Player2.Location.Y) <                       ( int )(0.8 * Player1.MyImage.Height) &&                       Player2Rem >= Player1Rem)                    btnFire2.PerformClick(); // Fires rudal                if (Rudal1.IsVisible &#124;&#124; Player2Rem == 0)                {                    if (Player1.Location.Y - Player2.Location.Y < 0)                        btnUp2.PerformClick(); // Moves up                    else                        btnDown2.PerformClick(); // Moves down                }                else                {                    if (Player1.Location.Y - Player2.Location.Y < 0)                        btnUp2.PerformClick(); // Moves up                    else                        btnDown2.PerformClick(); // Moves down                }            }        }    }} |
|  |  |