![](cover.jpeg)

Arduino

Getting Started With Arduino: The Ultimate Beginner’s Guide

Steve Gold

Introduction

If are you fascinated by the simplest of technology, and often wonder about the inner workings of the electronic devices that are so ubiquitous in our daily lives, you are likely to find joy in experimenting and tinkering with Arduino.

At the core of everything that comes to life at a flick of a switch – the Christmas tree lights that blink in multiple colors, the apps that open up on a touch screen device, and the microwave oven that heats up your food etc. – is a micro-controller, programmed to perform certain feats when activated. Arduino is an open-source platform that consists of a micro-controller and programming software. Unlike most platforms, Arduino was geared towards non-electricians who want to get creative with electronics, while also being flexible enough to accommodate engineering experts. It is meant to be accessible, low cost and easy to learn, regardless of your previous knowledge in electronics and programming.

This guide will not make you an Arduino expert overnight – in fact, nothing can. What you will learn from this book however are the fundamentals of this amazingly versatile platform, and you’ll also have the opportunity to get a firsthand feel for what it can do. You will be guided through the key features of an Arduino circuit board, technical requirements to begin working, how to kick-start your first Arduino, important lingo you’ll need to know in order to get by, and how to proceed further in order to keep building upon what you have learnt.

The information here is intended for the absolute beginner in electronics, circuitry and programming. If you have always wanted to learn how to build cool stuff with electronics yet are completely at loss as to how to get started, you now have all the information you’ll need at your fingertips in order to make your entry into the exciting world of Arduino. The rest is up to you!

P.S. As a token of my appreciation, I have included a free surprise for you; no catch, no charge. Simply [click here](#part0001_split_006.html_b3) to find out more.

© Copyright 2015 by Eddington Publishing - All rights reserved.

This document is geared towards providing exact and reliable information in regards to the topic and issue covered. The publication is sold with the idea that the publisher is not required to render accounting, officially permitted, or otherwise, qualified services. If advice is necessary, legal or professional, a practiced individual in the profession should be ordered.

- From a Declaration of Principles which was accepted and approved equally by a Committee of the American Bar Association and a Committee of Publishers and Associations.

In no way is it legal to reproduce, duplicate, or transmit any part of this document in either electronic means or in printed format. Recording of this publication is strictly prohibited and any storage of this document is not allowed unless with written permission from the publisher. All rights reserved.

The information provided herein is stated to be truthful and consistent, in that any liability, in terms of inattention or otherwise, by any usage or abuse of any policies, processes, or directions contained within is the solitary and utter responsibility of the recipient reader. Under no circumstances will any legal responsibility or blame be held against the publisher for any reparation, damages, or monetary loss due to the information herein, either directly or indirectly.

Respective authors own all copyrights not held by the publisher.

The information herein is offered for informational purposes solely, and is universal as so. The presentation of the information is without contract or any type of guarantee assurance.

The trademarks that are used are without any consent, and the publication of the trademark is without permission or backing by the trademark owner. All trademarks and brands within this book are for clarifying purposes only and are the owned by the owners themselves, not affiliated with this document.

Table of contents

Introduction

Chapter 1: Understanding Arduino

Chapter 2: How To Get Started with Arduino

Chapter 3: Taking the first step!

Chapter 4: Arduino Survival Lingo

Chapter 5: Essential Resources & Further Reading

Conclusion

A message from the author, Steve Gold

Chapter 1

Understanding Arduino

In 2005, the Ivrea Interaction Design Institute in Italy started a project of creating an open-source platform to be used for building various electronic projects, known as Arduino. Originally geared towards students with little to no background in electronics or computer programming, the platform eventually gained worldwide popularity due to its accessibility and beginner-friendly features.

Over the years since its inception, Arduino has garnered the attention and enthusiasm of hobbyists, artists, programmers, students and even hackers from all levels of experience. Being an open-source platform, it continues to grow with contributions from a diverse community of users that keep pushing the limits of its capabilities. In fact, Arduino has been the backbone behind thousands of projects and applications, from everyday objects to complex scientific equipment.

The Arduino platform consists of two components:

1.The hardware – A physical programmable circuit board, also known as the microcontroller. There are different types of Arduino boards (more on this in Chapter 2).

2.The Software – The Integrated Development Environment (IDE) that runs on the computer, used for writing and uploading programming codes to the physical board.

Why Go Arduino?

Practically anyone can use Arduino. Experts are sure to have fun with building projects and sharing ideas with other users at online communities. For those with no experience with circuits and micro-controller programming, the platform is excellent for learning and experimenting. However, it is recommended that before exploring the wonders of Arduino, you should at least have a firm understanding of these fundamental concepts:

•The basics of electricity and circuitry

•Voltage, current, resistance and Ohm’s law

•Polarity

•Integrated circuits (ICs)

•Digital logic

•Analog versus Digital

•Basic computer programming

What makes Arduino a favorite among amateurs and experts alike is that, compared to other platforms and systems, it simplifies the process of working with micro-controllers. For a start, loading new codes to the board can simply be done with a USB cable, unlike previous programmable circuit boards where a separate piece of hardware has to be used. It is also a plus point that Arduino boards are relatively inexpensive compared to other micro-controller platforms, with some pre-assembled modules costing less than $50\. If those perks are not enough, here are some more reasons why Arduino is the platform to go for:

•Cross-platform – Arduino’s IDE runs on Windows, Macintosh OSX, and Linux operating systems, whereas most micro-controller systems are only compatible with Windows.

•Simple programming environment – The Arduino IDE uses a simplified version of C++, making it easier for beginner to learn how to program, yet flexible enough for advance users to get creative and ambitious with.

•Open source and extensible hardware – Arduino board plans are published under a Creative Common license, allowing circuit designers to create their own version of the module, extending it and improving upon it.

•Open source and extensible software – The Arduino IDE is published as open source tools that experienced programmers can expand on, through C++ libraries. You can also learn the AVR-C programming language from Arduino, just as you can also add AVR-C code directly into Arduino programs.

•Backed by a supportive community – If you are absolutely new to the platform and don’t know where to begin, there is a wealth of information to be found online due to the popularity of Arduino. You will never run out of resources to learn from, and you can even find pre-coded projects to work on right away (See Chapter 5 for Arduino resources).

What can Arduino do for You?

Arduino was designed with the creative and innovative in mind, regardless of experience level. Artists, designers, electricians, engineers, programmers and science enthusiasts can use it to create interactive objects and environments. Among the things Arduino can interact with include motors, speakers, LEDs, GPS units, cameras, TVs, smart-phones and even the internet.

With Arduino, one can build low cost scientific instruments, do programming for robotics, build interactive prototypes of architectural designs and create installations for musical instruments to experiment with sound, build new video game hardware – and this is just the tip of the iceberg! So, whether your project entails building a robot, a heating blanket, a festive lighting display or a fortune-telling machine, Arduino can serve as a base for your electronic projects.

Before You Continue...

As a token of appreciation, I’ve included a great, surprise for you, completely FREE!

Simply click the link below now to find out more.

[==> CLICK HERE<==](#part0001_split_006.html_b3)

I promise, this is not “spam”, and you can be back to this page in just a few seconds via a simple link.

Take action now to avoid missing out!

[==>CLICK HERE NOW!<==](#part0001_split_006.html_b3)

Enjoy!

Steve Gold

Chapter 2

Getting Started with Arduino

As the Arduino platform is ever expanding, continuous learning is necessary as there is always something new to discover. What you will learn in this chapter is the bare minimum you need to know in order to get your feet wet. You will be introduced to the basic Arduino components, what you will need and how to set them up. Obviously, you are going to need the two essentials: an Arduino board and the software installed (available free for download on the official Arduino website).

Anatomy of an Arduino Board

Before you start shopping around for hardware, you need to know some basics about Arduino boards and their features. There are several types of Arduino boards available for purchase, each with different capabilities. Although they may differ in look and capabilities, you will find most boards have the majority of these components in common:

1.USB and Barrel Jack – Every board will have a means for it to be connected to a power source. Almost all Arduino boards come with USB connection, since this is how you will be uploading codes onto them. You can also connect to a wall power supply via the barrel jack.

2\. Pins – The boards’ pins are where you construct circuits by connecting wires. There are several types of pins on Arduino boards, each meant for a specific functions. Here is what you will normally find:

•GND: Short for Ground, these pins are used to ground your circuit.

•5V and 3.3V: These pins supply 5 Volts and 3.3 Volts of power, respectively.

•Analog: You can identify this row of pins under the ‘Analog In’ label. They are used for reading signals from analog sensors, and convert those signals into digital values.

•Digital: Across from the analog pins, under the ‘Digital’ label, are the pins to be used for digital input and output. For example, telling when a button is pressed (input), so that an LED lights up (output).

•PWM: In a lot of Arduino boards, there is the label (PWM~) next to ‘Digital’. It means that the pins can be used as normal digital pins, and also for a type of signal called Pulse-Width Modulation (see the glossary of terms in Chapter 4 for explanation).

•AREF: A short form for Analog Reference, this is the pin which can be used to set an external voltage as the upper limit for the analog pins (between 0 and 5 Volts), although it is mostly left alone.

3\. Reset button – This button is self-explanatory; pushing it will connect the rest pin to ground, and restart any code loaded onto the board. This is useful for testing your programmed codes multiple times. It does not, however, functions to reset everything to a clean slate and wipe away any problems.

4\. Power LED Indicator – This is a tiny LED that can be identified with the word ‘ON’ next to it. It will light up when you plug the board into a power source, and if it doesn’t, it means you have to re-check your circuit because something is wrong.

5\. Transmit (TX) and Receive (RX) LEDs – Not to be confused with the TX and RX markings by the 0 and 1 digital pins, the LEDs with these markings will give you a visual indication whenever the board is transmitting or receiving data, such as when you load a new program onto the board.

6\. Main Integrated Circuit (IC) – This is the black piece with metal legs that is attached to every board. It is basically the brains of an Arduino board. The main IC differs from board to board, though most are from the ATmega line of IC’s by the ATMEL company. It is important to know the IC and board type before loading up a new program from the Arduino IDE. You can usually find this information written on the top side of the IC.

7\. Voltage regulator – As its name implies, this component controls the amount of voltage that is allowed into the Arduino board. It functions by turning away extra voltage let into the board. But it has its limits though; it cannot handle anything over 20 Volts. So, a word of caution: DO NOT use a power supply greater than 20 Volts! It will overpower and destroy your Arduino. The recommended voltage for most models is 6 to 12 Volts.

All in the Family

The Arduino board has gone through considerable changes since it was first introduced, in order to meet the various demands and challenges of its users. More than just the 8-bit boards, Arduino have boards built for various applications, from Internet of Things (IoT) applications to wearable items. All of them are, of course, open-source, which further empowers users to build derivatives and customize them to fit specific needs. The following are a few options that are considered most suitable for the Arduino novice:

•Arduino UNO (R3) – The UNO is often considered to be the definitive Arduino board. It is well-equipped with everything you need to get started, with 14c digital input/output pins – six of which can be used as Pulse Width Modulation (PWM) outputs – six analog inputs, a USB connection, a power jack and many more. Simply connect it to any power source, whether it is a computer with a USB cable, an AC-to-DC adapter or battery, and you are good to get started. Regardless of your Arduino expertise, you can never go wrong with the UNO.

•Arduino Mega (2560) – The Mega board is a few notches above the UNO; kind of like its big brother. It has an impressive 54 digital input/output pins, of which 14 can be used as PWM outputs, 16 analog inputs, plus everything else you can find on the UNO and also functions the same way. If you have a project that requires a lot of digital input/outputs, such as for a lot of LED lights or buttons, the Mega may be the board for the job.

•Arduino Leonardo – The Leonardo board offers a cheaper and simpler alternative, as it is the first Arduino development board to use one micro-controller with built-in USB. Because of its direct USB handling, code libraries are available that allows the board to emulate a computer keyboard, mouse and much more.

•Arduino Mega ADK – This board is basically a specialized version of the Arduino Mega board. It is specifically designed for interfacing with Android smartphones.

•LilyPad Arduino – Thinking about making a cat-suit that lights up? The LilyPad is the wearable e-textile board you need. Designed by Leah Buechley, engineer and co-author of the book, Sew Electric, the innovative board was created with a large connecting pad and flat back that allows it to be sewn into clothing with conductive thread. And it is even washable!

•Arduino NG, Diecimila and duemilanove – Collectively known as Legacy Versions of the UNO, these boards are basically the granddaddies of the Arduino. The legacy boards lack some key features of other newer boards. For instance, the Diecimila and NG have a jumper next to the USB port and require manual selection of either USB or battery power. The NG also requires holding down the Reset button for a few seconds before uploading a program. It should be noted, however, the legacy boards are still being tinkered and improved upon by Arduino enthusiasts. They are worth looking into once you gain more knowledge and experience with Arduino.

Genuino Who?!

If you are shopping for Arduino boards outside of America, you may find Genuino boards that look identical. Don’t worry; you are not being duped by an imitation product! Genuino is Arduino’s sister-brand, created by the same team, and used for boards and products sold outside of the US.

The Genuino brand certifies the authenticity of boards and products to be in line with Arduino’s philosophy of open-source hardware. The brand has alliances with market-leading manufacturers in Asia, Europe, South America, Canada and Africa, making the Arduino hardware available worldwide.

You can think of Genuino boards as the identical twins of Arduino boards that live in foreign countries. All Genuino boards have the similar quality, components and characteristics as their Arduino counterpart. So, depending on which part of the world you live, you may find a Genuino UNO board when looking to buy an Arduino UNO. That’s just fine; you’re still getting the real deal.

It should be noted though, that not all Arduino boards – especially lesser known ones – have a Genuino twin.

Other Stuff You could Use

An Arduino board cannot do much on its own, so you will need to hook it up with something. There are plenty of hardware options one can fix onto their Arduino boards that will be overwhelming for the beginner to learn (see Chapter 5 for further reading suggestions). Hence, we will only be introducing you to two handy items that are easy to hook onto an Arduino boards and bringing your projects to life – sensors and shields.

There is a lot of fun to be had with sensors. Hook one up to your Arduino board, and add some simple programming code, you can then make your board sense and measure practically anything – light, temperature, physical pressure, distance proximity, barometric pressure and radioactivity. You can also build devices to scan fingerprint, detect motions of animals or people, and signals from remote controls.

Additionally, you can do even more with shields, which are pre-built circuit boards that can fit on top of your Arduino boards. With shields, you can program your Arduino to connect to the internet, control LCD screens, control motors and provide cellular communication and lots of other cool stuff, limited only by your knowledge and imagination!

Set Up the Software

Once you have your hardware sorted out, the first thing to do is to install the Arduino IDE. This is the software where you will write the code for the micro-controller and attach the circuit components to make things happen. You can download the software at the official Arduino website: [www.arduino.cc](http://www.arduino.cc).

Once downloaded, unzip the folder into a choose a location on your computer hard drive, and then run the Arduino.EXE file to complete the installation. Now, you are ready to get things going with Arduino!

Chapter 3

Taking The First Steps!

You have an Arduino board and the software; it is time to get down to business! In the sections that follow, you will be guided in a step-by-step process to do a few things; you will test out the Arduino software and board with your first code, and do a simple project of lighting an LED. For the example given, an Arduino UNO (R3) board will be used. However, the instructions can be applied, with minor modifications, to any Arduino board of your choice.

Here are the four pieces of equipment you will need to begin your Arduino journey:

•A computer that runs on Windows (XP or above), Mac, or Linux operating system, with the Arduino IDE installed

•An Arduino micro-controller (a.k.a. the circuit board)

•A USB A-to-B cable for connecting your Arduino board to the computer, or one that fits your board of choice (be aware that some boards will require an A-to-Mini-B cable)

•An LED

Plug in the Board

Arduino boards are powered by either a USB connection to a computer (via the USB jack) or an external power supply (via the barrel jack). You will need to connect the board to a computer in order to program it using the Arduino IDE. Once you are done with the programming and don’t require it to be connected – depending on how you want to use the board for your project – you can then opt for powering it with a wall power supply.

To start off, you must connect your Arduino board to a computer using the USB cable. The moment you so that, you may notice the LED with the label ‘ON’ next to it starts blinking furiously; this is the default program stored in the board’s chip. What you will be doing to kick-start your Arduino is overriding this default program, and making the LED blink on and off slowly, at 2-second intervals.

Install the Drivers

This step is required if you are using Windows 7, Vista or XP with an Arduino board for the first time. If you are using another operating system, you can skip this section.

1.When you plug in the board, Windows will begin the driver installation process. After a few moments, the process will fail.

2.Click on the Start Menu, and open up the Control Panel.

3.In the Control Panel, go to System and Security and click on System.

4.Once the System window is up, open the Device Manager.

5.Look under Ports (COM & LPT). You should see an open port named Arduino UNO (COMxx). If there is no COM & LPT section, look under Other Devices for Unknown Device.

6.Right click on the Arduino UNO (COmxx) or Unknown Device port and choose the Update Driver Software option.

7.Next, choose the Browse my computer for driver software option.

8.Finally, navigate to and select the driver file named arduino.inf, located in the Drivers folder of the Arduino Software download (not the FTDI USB Drivers sub-directory). If you are using an old version of the IDE (1.0.3 or older), choose the Uno driver file named Arduino UNO.inf.

9.Windows will finish up the driver installation from there.

Launch and Sketch

Once you have the Arduino IDE properly installed, you are now ready to test drive your board with the first program. Before getting into that, there are some things you need to know about writing code for Arduino. The codes are known as sketches, written in C++.

Every sketch needs two void type functions that do not return any value,  setup()  and loop(). The setup() method is run once, just after the Arduino board is powered up and the loop() method is run continuously afterwards. The setup() is where you want to do any initialization steps, and loop() is for codes you want to run over and over again.

A basic sketch skeleton should look like this:

| void setup(){}void loop(){} |

Now, let’s give your first program a try:

1.Make sure your board is plugged in, and launch the Arduino application

2.Open the Blink example sketch by going to: File > Examples > 1.Basics > Blink

3.Select the type of Arduino board you’re using: Tools > Board > your board type

4.Select the serial/COM port that your Arduino is attached to: Tools > Port > COMxx

If you’re not sure which serial device is your Arduino, take a look at the available ports, then unplug your Arduino and look again. It should be the one that disappeared as soon as you unplug.

Upload and Make it Blink!

With your Arduino board connected, and the Blink sketch open, press the Upload button. Wait for a few seconds; you should see the RX and TX LEDs of the board flashing as the program is being uploaded. If the upload is successful, you will see the Done Uploading message in the status bar of the Blink sketch.

If the whole process is done correctly, the orange ‘ON’ LED should be blinking slowly. Congratulations! You have successfully programmed your first Arduino.

But it doesn’t Work!

If you followed all the steps above, but you can’t upload the sketch to your Arduino for it to launch, it could be due to problems with one of the processes. Try running through these troubleshooting measures:

1.Make sure you select the right board under the Tools > Board menu. In case you choose to use another board besides the UNO (as in the example), check the IC on the board. For instance, newer Arduino Duemilanove boards come with an ATmega328, while older ones have an ATmega168\. So, make sure you select the right option.

2.Check that the proper port is selected in the Tools > Serial Port menu.

3.Check to see if the drivers for your board are properly installed in the Tools > Serial Port menu in the Arduino IDE, with your board connected. There should be an additional item that wasn’t there when your board is not plugged in.

First Mission: Light an LED!

Having successfully activated your Arduino, let’s try doing a little bit more with it. The following is a common learning project suitable for complete beginners in circuitry. For this task, you will need an LED and your Arduino that has already been launched (following the previous instructions).

1.Plug in your board.

2.Open another example sketch: File > Examples > Basics > BareMinimum. This will open a new window with a simple sketch that acts as the framework for your program.  

3.Connect the LED’s anode (the longer pin) to pin 13 on the Arduino board, and the cathode (the shorter pin) to the adjacent GND pin.

4.Under the setup() section of the sketch, add the code: pinMode(13, OUTPUT);. This is the command that will run once to configure the board and get it ready to do as you program.

5.Add the following under the loop() section: digitalWrite(13, HIGH);. This sets the pin 13 as an output pin with high voltage level (5 Volt).

When complete, your sketch should look like this:

| void setup(){pinMode(13, OUTPUT);}void loop(){digitalWrite(13, HIGH);} |

Hit the Upload button and wait for the Done Uploading message to show in the status bar. Voila! The LED should light up.

Chapter 4

Arduino Survival Lingo

As you go about adding to your knowledge bank about all things Arduino, you are bound to encounter some frequently used jargon. This mini glossary of terms is by no means extensive, but it does help the beginner understand the terms people often mention when they talk about Arduino, so that you will not be totally at a loss.

8-bit – The term refers to a Central Processing Unit (CPU) that processes 8 bits of data as a single unit.

Analog – Describes devices or systems that represent changing values as continuously variable physical quantities. As humans, we perceive the world in analog, as everything we see and hear is a continuous transmission of information (data) to our senses. An example of an analog device is a record player, because it reads bumps and groves from a vinyl record as a continuous signal. Analog data is more accurate than digital data, but harder to manipulate and preserve. With Arduino boards, you can use the analog pins to convert analog data to digital values.

AVR – When you work with electronics, you will encounter several meanings for this acronym. In Arduino terms, it refers to the platforms environment, which is based on Atmel Atmega micro-controllers. The AVR micro-controller was developed by Atmel Corporation in 1996, by Alf-Egil Bogen andVegard Wollan. The AVR acronym derives from its developers and stands for Alf-Egil Bogen Vegard Wollan RISC micro-controller, and is also known as Advanced Virtual RISC.

C++ – Pronounced as ‘cee plus plus’, it is a general-purpose programming language. You program an Arduino board do stuff with C++, using the Arduino IDE.

CPU – Stands for Central Processing Unit and is also commonly referred to as the processor, a CPU is the electronic circuitry within a computer that carries out the instructions of a program.

Digital – Information in digital is stored using a series of 1s and 0s, known as binary code. Digital is the opposite of analog. Because digital devices read only 1s and 0s, they can only approximate audio and video signals. Unlike analog, digital data is easier to manipulate and store.

Driver – A software that allows a computer to connect and communicate with a hardware or device. Without the right driver, the hardware you connect to a computer will not work properly. Depending on the operating system you are using to work with your Arduino, you may need to install the driver for the board.

Environment – In computing jargon, the environment refers to a particular configuration of a hardware platform and the operating system that it runs on.

Ground – In electrical engineering, a ground is the reference point in an electrical circuit from which voltages are measured or the common wiring point. The term can also mean the literal earth where electrical circuits are connected to. On the Arduino board, the GND pin serves this purpose.

I/O – Short for input/output, which describes a program, operation or device that transfers data to or from a computer, to interact with the outside world. For example, if a button is pressed (input), a light bulb goes on (output).

LED – The acronym for Light-Emitting Diode, a two-lead semiconductor light source. LEDs have many advantages over other light sources, including smaller sizes, longer lifespan and lower energy consumption. On the Arduino board, you will notice some LEDs that indicate when the board is powered and codes are uploaded.

Micro-controller – A computer present in a single integrated circuit that is programmed to perform specific tasks. Micro-controllers are the brains behind automatically controlled electronic devices, from cell phones and cameras to washing machines and microwave ovens to robots.

Open-source – A program whose source code is made freely available to the public for use or modification. Open Source is a certification mark owned by the Open Source Initiative (OSI) that allows software developers to freely share their products with the public, so that it can be improved upon and redistributed. Unlike commercial software, where some sort of redistribution licensing is required, anyone can have a hand in developing and redistributing an open-source project.

Sensor – Electronic devices used to measure physical quantities, and then convert them into electronic signals. There are various different kinds of sensors for measuring things in the physical, such as temperature, pressure, distance, noise, motion etc. Sensors are normally components of more complex and sophisticated electronic systems. If you want to built a digital thermometer, for instance, you will need a temperature sensor that will go with your Arduino board.

Serial port – A connector that is used to send data to a device connected to a computer, such as modems, printers, and mice. An Arduino board must be connected to the right serial port for codes to be uploaded properly.

Sketch – A term used to mean an Arduino program. A chunk of code written to command an Arduino is called a ‘sketch’, rather than just a ‘program’, because the Arduino platform was designed to appeal to artists and creative individuals in addition to engineers. According to the founders, using the term ‘sketch’ would imply a rough idea that can be explored, refined and developed – much like an art or design sketch. As such, it will make using Arduino feel more encouraging and less daunting to those who are not from a tech background.

Shield – This is a circuit board that can be attached on top of an Arduino to accomplish a variety of purposes. They are called this because they fit over the top of an Arduino board like a protective shield.

IDE (Integrated Development Environment) – The software application that is run to provide you with the tools to program Arduino boards. It includes a source code editor, build automation and debugger. It is an open-source software available for download at the official Arduino website ([www.arduino.cc](http://www.arduino.cc)).

Pulse-Width Modulation (PWM) – A term describing a type of digital signal that is used in a variety of applications. It is mainly used to control the amount of power supplied to electrical devices.

Voltage – The amount of energy between two points of a circuit, measured with the standard unit, Volt (V).

Chapter 5

Essential Resources & Further Reading

You have learnt the basics of Arduino and – if you have actually been following along with the instructions – got a feel for what the platform can do firsthand. That was just the tip of the iceberg, though; Arduino mastery takes time and dedication to keep building upon what you have learnt. Furthermore, the open-source platform keeps on expanding as more people take to using it. Whatever brought you to Arduino, your journey with this exciting platform has just begun. Here is a list of useful materials, written by some of the most respected authorities on Arduino, to help you move ahead.

For Absolute Beginners

# Getting Started with Arduino: The Open Source Electronics Prototyping Platform

by Massimo Banzi and Michael Shiloh

ISBN-10: 1449363334 / ISBN-13: 978-1449363338

What better way to get more acquainted with Arduino than from one of the creators himself? Massimo Banzi is the platform’s co-founder. This beginner-friendly book is written based on his extensive experience in teaching, using, and building Arduino.

# Beginning C for Arduino, Second Edition: Learn C Programming for the Arduino Kindle Edition

by Jack Purdum Ph.D.

ISBN-10: 1484209419 / ISBN-13: 978-1484209417

Written for those who have no prior experience with micro-controllers or programming, this guide is ideal for those who are starting their journey into programming. You will get an introduction into C programming language, with a simple demonstration of how it can be used on the Arduino family of micro-controllers. Drawn from the author’s 20-plus years of university teaching, this book is perfect for the complete programming beginner. It is engaging to read and assumes no prior programming or hardware design experience of its readers, making learning enjoyable.

Take Your Skills to the Next Level

# Programming Arduino Next Steps: Going Further with Sketches

by Simon Monk

ISBN-10: 0071830251 / ISBN-13: 978-0071830256

#### Electronics guru, Simon Monk reveals professional programming secrets for Arduino in this practical guide for those who already have a firm grasp of programming micro-controllers. This book covers the Arduino Uno, Leonardo, and Due boards. Learn advanced ‘sketching’ techniques to take your Arduino to the next level, including programming for the internet, maximizing serial communications, managing memory, performing digital signal processing, and so much more. The book features over 75 example sketches, all available for download.

# Electronics from the Ground Up: Learn by Hacking, Designing, and Inventing

by Ronald Quan

ISBN-10: 0071837280 / ISBN-13: 978-0071837286

Are you fascinated by the complex circuits behind common electronic devices? This book guides you through step-by-step experiments that reveal how electronic circuits function. It also explains components, construction techniques, basic test equipment, circuit analysis, and troubleshooting. By the end of the book, you will not only be armed with the know-how to design customs circuits, but also the ability to hack and modify existing circuits to suit your needs.

# 30 Arduino Projects for the Evil Genius

by Simon Monk

ISBN-10: 0071817727 / ISBN-13: 978-0071817721

Ever want to build a Morse code translator? Pulse rate monitor? A Hypnotizer? How about a keyboard prank? You can unleash your evil genius with this do-it-yourself guide that shows you how to program and build fascinating projects with the Arduino Uno and Leonardo boards. You will learn from through guides with checklists of required parts for each project, step-by-step instructions with illustrations, and clear explanation of scientific principles behind the projects.

Fun Project Ideas

# Arduino Workshop: A Hands-On Introduction with 65 Projects

by John Boxall

ISBN-10: 1593274483 / ISBN-13: 860-1200651553

Think you’ve already got the hang of Arduino and are ready to try some fun projects? This book will get you started. You will learn the extensive range of Arduino’s input/output add-ons, sensors, indicators, displays, motors, and more. Each project is designed to reinforce what you have learnt, and they increase in complexity as you progress. So, what can you learn to build? A digital thermometer, battery checker, and a GPS logger, to name a few. There are also fun things to learn, like making a binary quiz game and an an electronic dice.

# Sew Electric Perfect

by Leah Buechley, Kanjun Qiu and Sonja de Boer

ISBN-10: 0989795608 / ISBN-13: 978-0989795609

Co-written by the creator of the LilyPad Arduino board, Leah Buechley, this book is a hands-on guide that combines crafting, electronics and programming to create fun projects. Learn to make interactive toys, light-up fashion accessories and many other cool things using the LilyPad Arduino board that can be shared with friends and family. This is also a great material for teachers to introduce practical electronics to young students.

# Textile Messages: Dispatches From the World of E-Textiles and Education

by Leah Buechley, Kylie Peppler, Michael Eisenberg and Yasmin Kafai

ISBN-10: 143311920X / ISBN-13: 978-1433119200

This book is a handy introduction to e-textiles – soft circuit boards that can be used to incorporate electronic elements into clothing and furniture. In the Arduino family, the LilyPad board is an e-textile, and this is a beginner to intermediate guide that can show you how to make the most of your LilyPad. You will be introduced to a collection of tools that enable anyone to learn and create with e-textiles, whether you are an educator, hobbyist or designer.

# Make: Wearable Electronics: Design, prototype, and wear your own interactive garments

by Kate Hartman

ISBN-10: 1449336515 / ISBN-13: 978-1449336516

For those with interest in computing, and fashion designers who want to build creative projects that fuse both disciplines, this book is a must read. You will be introduced to tools, materials and techniques for making interactive electronic circuits, and embedding them in articles of clothing with step-by-step instructions. Although the book does not specifically feature Arduino projects, it will equip you with knowledge that can be adapted to suit the Arduino platform. So, if you ever wanted to build clothing that changes color to complement your skin tone, a jacket that shows when the next bus is arriving, shoes that dynamically shift your height, and many other cool wearable items, now you can!

# Adventures in Arduino

by Becky Stewart

ISBN-10: 1118948475 / ISBN-13: 978-1118948477

If you know a kid who shows potential in electrical engineering and programming, give this book to him or her! Written specifically for the budding electrician, ages 11 to 15, this book is an excellent Arduino introductory source.

Online Resources

[https://www.arduino.cc/](https://www.arduino.cc/) - The official Arduino website for all your needs and the latest development news regarding the platform. Here is where you can find and join the Arduino forum to get help and share knowledge with other users from all around the world.

[http://www.cplusplus.com/](http://www.cplusplus.com/) - A comprehensive online library for all things C++. You can learn about the history, development and the A-to-Zs of the programming language that Arduino runs on.

[http://www.ladyada.net/](http://www.ladyada.net/) - A wonderful resource to learn about electronics and circuitry, with nearly all its content being open-sourced.

Conclusion

Congratulations on completing the Arduino basic apprenticeship and successfully navigating your first Arduino project! In this book, I hope I have managed to give you all the information you need to feel confident in your ability to move forward and try some more difficult Arduino projects. Good luck!

A message from the author, Steve Gold

Thank you for your purchase of this book. If you enjoyed what you read, please take the time to share your thoughts and post a review on Amazon. It will only take a couple of minutes and I’d be extremely grateful for your support.

Thank you again for your support.

Steve Gold

###### FREE BONUS NUMBER 1!

###### As a free bonus, I’ve included a preview of one of my other best-selling books, “Elon Musk - The Biography of a Modern Day Renaissance Man”! Scroll to the end of this book to read it.

###### FREE BONUS NUMBER 2!

###### As a special thank you to all my readers, I’ve included access to my select group. Sign up to stay informed of upcoming releases, including some heavily discounted and FREE books!

###### ALSO…

###### Be sure to check out my other books. Scroll to the back of this book for a list of other books written by me along with download links!

##### FREE BONUS!:  Preview Of “Elon Musk - The Biography of a Modern Day Renaissance Man”!

##### ![Elon Musk - Biography.jpg](images/00001.jpeg)

##### If you enjoyed this book, I have a little bonus for you; a preview of one of my other books “Elon Musk - The Biography of a Modern Day Renaissance Man”. In this book, I take a closer look at exactly who Elon Musk is as well as examining the truly extraordinary accomplishments he has managed to achieve. Enjoy the free sample, and feel free to click on the purchase link below if you would like to learn more about this truly incredible individual!

Introduction

When actor Robert Downey Jr. signed on to portray Tony Stark (a.k.a. Iron Man), he suggested to director John Favreau that they meet up with Elon Musk. They have a task of bringing to life a superhero, and Musk is the closest there ever is to Marvel’s genius, billionaire, philanthropist in real life. The meeting was set and some of Musk’s characteristics went into RDJ’s portrayal of Tony Stark on screen, thus creating the memorable character that people come to know and love.

In reality, there is far more to Musk’s life and person than can be personified by a fictional character. Sure, he does have a lot in common with Iron Man; he’s a prodigious tech genius and entrepreneur, with the capacity to make seemingly impossible ideas a reality. Like Tony Stark, he dreams, thinks and lives large, but that is where the similarity ends.

Unlike his comic book counterpart, Elon Musk was not born into a life of luxury and ease. Despite showing potential for greatness as early as his preteens, his childhood and young adult life was filled with adversaries. To this day, Musk credits his early life struggles in helping him cultivate the indomitable spirit he is known for.

Having made his mark in the field of IT, finance, sustainable energy, automotive, aerospace manufacturing and space exploration, it is an understatement to say that Musk has come a long way from his humble beginnings. He founded some of the most pioneering companies – Paypal, Tesla Motors, and SpaceX – and is almost single-handed responsible for each enterprise’s success. Whichever business he decided to dabble in, he brought with him a revolutionary idea which often ends up being a game-changer in the industry. Yet, he is far from done.

His brilliant mind never ceased to think up grander innovations, even after numerous repeated successful endeavors. His ample and wild ambitions, it seems, are driven by grand visions of changing the world we live in. His agenda for the future includes filling the roads with more electric cars, powering the world with solar energy, colonizing neighboring planets and enabling people to cover great distances with a futuristic high-speed public transportation system.

Most children would imagine of going outer space and travel to different cities in bullet-fast capsule pods, until those fantasies fade away in adulthood. Rarely are there individuals who dare to dream of living those fantasies that appropriately should stay within the realm of fiction. Elon Musk is among the exceptional few.

Chapter 1

The Beginnings Of Greatness

Almost every success story of high-achieving individuals contain episodes highlighting their extraordinary iron will, critical thinking, propensity for hard work, and an unwavering belief that the impossible is not out of their reach. As one of the most brilliant minds who help shaped the global economy after at the dawn of the information age and tech boom in the late 20^(th) century, it is hardly surprising that Elon Musk displayed such distinctive personality traits at an incredibly young age.

Elon Reeve Musk was born in June 28 of 1971, in Pretoria, Gauteng, South Africa. His father is a South African-born British electrical engineer, Errol Musk, and his mother is Canadian-English dietitian, Maye Musk. Elon is the eldest of their three children, followed by brother Kimbal and sister Tosca.

Growing up in Pretoria, Elon’s early years were far from a picture perfect childhood. His parents divorced when he was 9 years-old, after which he lived mostly with his demanding and emotionally abusive father. At school, he endured harsh bullying by his peers. In one notable instance, he ended up hospitalized after being pushed down a flight of stairs. Such ordeals led Elon to find solace in the safest company available; his own thoughts and imagination which resided in the deep recesses of his prodigious mind.

He would regularly immerse himself in reading as a means of escaping his troubles in the outside world. Encyclopedias and science fiction were among his favorite books; they added to his knowledge bank and encouraged his seemingly wild dreams of futuristic technology which had yet to become a reality. Often times, Elon would be caught daydreaming and lost in his own thoughts, ignoring the world around him in favor of the utopias in his imagination. Along with his innovative thoughts, Elon’s childhood experiences also contributed to him developing a high tolerance for hardship and an extraordinary work ethic; attributes which he is well known for and which have served him well in his life.

His aptitude for technological innovations and entrepreneurship was evident when he began teaching himself computer programming at the tender age of 10\. When he was just 12, he developed a spaceship shooter video game called, “Blastar", which he sold to a computer magazine for $500\. After his first brush with success, Elon and his younger brother, Kimbal, hatched a plan to open an arcade near their school. Unfortunately, their enterprising plan had to be scrapped when their parents refused to provide the legal consent to obtain a business permit.

In 1988, after graduating from Pretoria Boys High School at the age of 17, Elon made the momentous decision to leave his hometown for the United States, without the support of his parents. This would be the first step towards his hard-earned success. He was able to obtain Canadian citizenship through his mother a year later, and left South Africa for Montreal, Canada. There, he worked low-paying jobs and was living on the brink of poverty for a year.

At the age of 19, he was accepted into Queens University in Kingston, Ontario for undergraduate studies in science. It was during his studies that he met Canadian author, Justine Musk, whom he would marry in 2000 and end up having six sons with. Their marriage lasted for only eight years, and Elon got married for the second time to British actress Talulah Riley. This marriage ended in divorce in 2014.

Two years into his studies at Queens, Elon received a scholarship from The University of Pennsylvania (Penn) in America. He relocated to the US in 1992, following his transfer to Penn. In the following year, he earned his Bachelor of Science degree in Physics from Penn's College of Arts and Sciences, and stayed back a year at Penn's Wharton School to complete his studies for a Bachelor of Science degree in Economics.

Throughout his college years, alongside his scientific studies, Elon took a keen interest in philosophical and religious literature. It was stated that his all-time favorite book is The Hitchhiker’s Guide to the Galaxy by Douglas Adams. It is through this immersion in both science and personal studies of humanities that Elon found his calling; he had the lofty ambition of wanting to contribute to projects that would change the world for the better.

Consequently, his vision and entrepreneurial aspirations began taking shape, specifically in the areas of the internet, renewable energy and space exploration.

##### [Click here to check out the rest of “Elon Musk - The Biography of a Modern Day Renaissance Man” on Amazon.](http://amzn.to/1MBnmB9)

##### Or go to: [http://amzn.to/1MBnmB9](http://amzn.to/1MBnmB9)

# Check Out My Other Books!

![Elon Musk - Biography-1.jpg](images/00002.jpeg)

[Elon Musk - The Biography Of A Modern Day Renaissance Man](http://amzn.to/1MBnmB9)

![Elon Musk - Lessons.jpg](images/00003.jpeg)

[Elon Musk - The Business & Life Lessons Of A Modern Day Renaissance Man](http://amzn.to/1jpCQl7)

![Warren_Buffett_new.jpg](images/00004.jpeg)

[Warren Buffett - The Business And Life Lessons Of An Investment Genius, Magnate And Philanthropist](http://amzn.to/1LPu6kp)

![Steve Jobs Thumbnail.JPG](images/00005.jpeg)

Steve Jobs - The Biography & Lessons Of The Mastermind Behind Apple

![Management - .jpg](images/00006.jpeg)

[Management - Achieve Management Excellence & World Class Leadership Skills In 7 Simple Steps](http://amzn.to/1hFnU09)

![Sales_new.jpg](images/00007.jpeg)

[Sales - Easily Sell Anything To Anyone & Achieve Sales Excellence In 7 Simple Steps](http://amazon.com/dp/B018S70JLQ/ref=sr_1_1?s=digital-text&ie=UTF8&qid=6143351094&sr=1-1&keywords=sales)

![Arduino Thumbnail.JPG](images/00008.jpeg)

Arduino - Getting Started With Arduino: The Ultimate Beginner’s Guide

(If the links do not work, for whatever reason, you can simply search for these titles on the Amazon to find them. All books available as ebooks or printed books)

The following is a free gift for my readers.

Thank you for your support!

Steve Gold

Connect

Simple Steps to Instant Likability, Rapport, and a Great First Impression

Steve Gold

Table of contents

Introduction

Chapter 1: The 60-Second Guide to Instant Rapport

Chapter 2: Let Your Body Talk

Chapter 3: Be Liked in an Instant

Conclusion

A message from the author, Steve Gold

Introduction

This short book is a limited-time free gift for my readers as a show of my appreciation for your support. It contains proven steps and strategies on how to connect with others and create a great first impression and instant rapport with them.

In this ebook:

•You will learn how to establish immediate connection and rapport in the first 60 seconds of meeting someone.

•You will learn what not to do when meeting someone for the first time.

•You will learn how to use verbal and non-verbal techniques to project charisma and ultimately get people to feel a sense of connection with you.

Please note, I have largely used the male pronoun in this book. I could have just as easily used the female pronoun or a combination of the two, but went with the male pronoun for the sake of simplicity.

Thanks again for your support and I hope you enjoy the book!

Steve Gold

© Copyright 2015 by Eddington Publishing - All rights reserved.

This document is geared towards providing exact and reliable information in regards to the topic and issue covered. The publication is sold with the idea that the publisher is not required to render accounting, officially permitted, or otherwise, qualified services. If advice is necessary, legal or professional, a practiced individual in the profession should be ordered.

- From a Declaration of Principles which was accepted and approved equally by a Committee of the American Bar Association and a Committee of Publishers and Associations.

In no way is it legal to reproduce, duplicate, or transmit any part of this document in either electronic means or in printed format. Recording of this publication is strictly prohibited and any storage of this document is not allowed unless with written permission from the publisher. All rights reserved.

The information provided herein is stated to be truthful and consistent, in that any liability, in terms of inattention or otherwise, by any usage or abuse of any policies, processes, or directions contained within is the solitary and utter responsibility of the recipient reader. Under no circumstances will any legal responsibility or blame be held against the publisher for any reparation, damages, or monetary loss due to the information herein, either directly or indirectly.

Respective authors own all copyrights not held by the publisher.

The information herein is offered for informational purposes solely, and is universal as so. The presentation of the information is without contract or any type of guarantee assurance.

The trademarks that are used are without any consent, and the publication of the trademark is without permission or backing by the trademark owner. All trademarks and brands within this book are for clarifying purposes only and are the owned by the owners themselves, not affiliated with this document.

Chapter 1

The 60-Second Guide to Instant Rapport

Establishing a Great First Impression

Research indicates how important making a good impression is in effective communication and interpersonal relationships. All of us are hardwired to evaluate a person based on the first sixty seconds of interaction. This inherent inclination to immediately assess someone has its roots in evolution. In olden times, one had to be able to tell whether or not another person was friend or foe; giving off the wrong impression could result in tragic consequences.

Today, making a good first impression is still essential—even if the outcome may not exactly be a matter of life or death. All of us want to make a great first impression on other people. We barely have 60 seconds to do this, and once a first impression is made, it is extremely difficult to change it. For this reason, it pays to give every new encounter the best that you are capable of. You are not likely to get a second chance.

Some people say that all that is required to make a good first impression is a heavy dose of good old common sense. This may very well be true but because you are not likely to get a second chance at making a great first impression, it pays to be prepared and to give it some serious thought.

Making that Instant Spark and Improving Your Rapport Development

To create instant spark and rapport with another person, you have to be genuinely interested in the other person – and to demonstrate this interest to him or her. You have to be a good listener. This means that you need to listen attentively, not only to what the other person is saying – but also, and sometimes more importantly, to what they are not.

Pay close attention to their non-verbal behaviors. These will cue you in to what the person you’re conversing with is really feeling and will help you determine how you should proceed with the rest of the conversation. Active listening allows you to fully understand what the other person is saying and to maintain a strong focus.

When you listen intently to the other person, you make them feel important and special. They are likely to think well of you and if the person senses that you are sincerely interested in them, you create an instant spark and are able to develop immediate rapport. You make the person feel comfortable and happy to be spending time with you.

Chapter 2

Let Your Body Talk

How you behave is just as important as what you are saying. Your body language is just as effective as your words are in communicating your feelings. You tend to become better at establishing rapport when your body language signals your interest in people.

The Art of Body Language

It is not enough to tell people that you want to get to know them. Your words are useless if your actuations do not substantiate them. If you want to create a strong immediate connection with people, use your body language to effectively demonstrate your interest to connect with them.

There are many non-verbal cues that other people find appealing. Strengthen your winning ways by looking closely into these behaviors.

When you turn toward another person, cross your legs in his direction, or point your feet towards him, you tell him through your body language that you want to know him better. When your body stance is open, you indicate that you are receptive to him.

Try to cultivate a sincere and contagious laugh. People respond strongly to somebody who laughs at the right time -- and in a spontaneous, charming, child-like manner. In the same manner, be careful not to laugh in a loud or unpleasant way. Bray like a donkey or laugh in a strident manner – and people are certain to stay out of your way.

Let your voice echo your excitement or pleasure. An expressive and lively voice is very attractive, particularly if it resonates and sparkles with positive feelings. Learn to cultivate a voice that reflects changes in volume, speed, and pitch, depending on the changing emotions that are present. Let your voice reflect your excitement about a particular topic. Let it mirror the warm and cordial feelings you feel about making the acquaintance of the person you are talking to.

An inscrutable face tends to intimidate. A warm and open face draws people.

Allow your face to demonstrate your feelings. You will be able to communicate more effectively when you enable the other person to better understand what you are saying through the different expressions you show on your face. The person you are talking to looks at your face and understands not only the ideas that you are expressing verbally but the feelings behind your words, as well, through the different vivid expressions that flit across your face.

Use your body language to help others visualize what you are saying. You do not necessarily have to act out your narrative but hand gestures and other body movements – on top of facial expressions – will definitely help you captivate the other person with what you are saying. He is not only likely to be better able to grasp your meaning; he is likely to be enthralled by you as well.

The No-No’s of Non-verbal Behavior

There are certain non-verbal behaviors that undermine your ability to establish rapport. You have to look into these behaviors so you can turn them around to work to your advantage.

Be cautious about giving a fake smile.

Everybody responds well to a smile – but it has to be sincere smile, a smile that reflects genuine interest, a warm welcome, or positive feelings. A fake smile simply makes people wary of you. It is not likely to make people think favorably of you; it may even make them avoid you.

Be careful about making eye contact.

When you establish and maintain eye contact, this shows the other person that you are interested in him. When you look past the person you are talking to, or keep your eyes on other people or goings-on in the room, these actions tell him that you are simply not interested -- that you would rather be somewhere else or talk to someone else. Take care not to glare as this makes the other person feel uncomfortable. Do not roll your eyes, either, as this non-verbal behavior demonstrates frustration or annoyance.

Do not stand too close to the other person.

Understand and respect the concept of “personal space.” When you position yourself too close to another individual, that person can feel uncomfortable or vulnerable. He is likely to see you as pushy or aggressive.

On the other hand, do not stay too far away.

You are likely to come across as aloof, unfriendly, and distant – not at all interested in establishing a connection with the other person.

Do not always touch the side of your nose or scratch your head.

These gestures are non-verbal cues that signal that you are telling a lie, or hiding or exaggerating something. They also indicate that you are not sure about what you are saying.

Do not cross your arms over your chest – using them as a “barricade.”

This stance signals that you are defensive and reluctant to let the other person get to know you better. Putting your hands in your pocket all the time says the same thing. If you do these things often, you are likely to come across as cold and aloof, and possibly even condescending.

Do not move around too much.

If you constantly pace, shift in position, or sway, this may indicate boredom or restlessness. It shows the other person that you are not really interested in the conversation.

Do not look blank or impassive.

It is difficult to carry on a conversation with a person who shows very little change in facial expression. He seems uninterested, indifferent, and unresponsive. It is more stimulating to talk to someone who is expressive, lively, and animated.

Do not be inflexible.

Move your body expressively. Use hand gestures to make your point. Being too rigid gives the impression that you’re uncomfortable and unable to relax. Of course, don't overdo it either!

Do not play with your pen, tie, jewelry, or hair.

This is distracting behavior. It signals to the person you are talking to that you are not interested in the conversation or that you are nervous. Either way this behavior is best avoided.

Do not fuss.

Demonstrate your confidence through your body language – even if you really are a bit nervous. Do not constantly rub your palms together, slouch your shoulders, or twist your hair. All of these actuations show that you are edgy. They can make others feel uncomfortable and tense, too.

Chapter 3

Be Liked in an Instant

Small Talk Equals Instant Connection

The ability to make small talk is an essential skill if you want to make an instant connection. It is a way of starting a conversation in an easy and comfortable manner. You talk about things that people find generally interesting and easy to converse about – music, movies, food, travel, sports, and other topics that people can discuss with ease – without fear or anxiety.

If you are good at making small talk, it will be easy for you to make an instant connection with people. You can easily draw people out of their shell in an easy and casual interchange that makes for light-hearted and interesting conversation for both of you. You can get individuals who are usually shy to easily converse with you.

Small talk usually starts small – with just a casual exchange of ideas about topics which may even seem rather superficial at first. However, rapport is established through these small baby steps. You have to first get the other person to feel comfortable with you through easy conversations. If you start out strong, deep, and intimate, you are just likely to drive people away. However, if you start out small in a casual, non-intimidating manner, you will be able to establish rapport. You will get the other person to like you in those first few seconds of interaction. You will be able to create a good impression, to establish the fact that you are a likable and fun person to be with. By starting small and casual, you pave the way to cultivating a deeper relationship – if both of you are so inclined to do so.

Habits of Likable and Charismatic People

Charisma comes naturally to some privileged people. But for most, though, it is, happily, something that can be learned. Try to observe people whom you consider as charismatic. What is it in their person and behaviors that make other people think of them as charming and compelling? What is it that draws people to them? What is it that makes other people feel happy, comfortable and at ease in their presence?

What are the habits of likable and charismatic people that you, too, can develop?

Likable individuals know how to initiate a conversation to make the other person feel that he is interesting. They know how to make others feel comfortable enough to respond to small talk and to overtures of friendship. They know not only how to start a conversation but how to sustain it. They know how to keep the conversation going so that the other person soon feels enthusiastic about the interaction.

In this aspect, practice, indeed, makes perfect. If you find it difficult to converse with people, make it a point to approach people and exercise your conversational skills. You may feel uncomfortable at first. Just keep on going. You do not have to be brilliant. You just have to be nice, to be sincerely interested in the other person. In time, you get to be natural at it – able to sense what the other person will find interesting to talk about and knowing how to steer the talk towards more interesting and more rewarding channels.

A charismatic person shows sincere interest in the other person. He asks questions because he genuinely wants to find out more about how the other person thinks and feels. He is sensitive. He realizes that he cannot simply bombard intimate details out of the other person so he is willing to go slow and easy.

A person can sense your interest and he is likely to appreciate it. When you are able to effectively communicate this interest, people are likely to see you as likable and charismatic. Because of this they tend to open up to you, to feel comfortable with you, and to be willing to take the conversation into deeper ends.

Like and Be Liked Through Listening and Mirroring

When you interact with a person, you may be able to “mirror” some of his behavior – facial expressions, posture, gestures, and even words. Research shows that mirroring is an effective technique for making another person like you. If you effectively use this technique, you may also find yourself readily liking the other person in return.

You will find it easier to make an instant connection with another person when you act and talk like he does. He will then see you as somebody familiar and comfortable to be with. He will find it easier to trust you because you, after all, appear to be just like him! When he sees that you have many things in common with him, he is likely to feel an instant bond with you. He tends to see himself in you.

You can use this powerful technique to create instant rapport with other people. You can harness mirroring to like and be liked by people in just 60 seconds.

Be attentive and observant of the other person. Observe both his verbal and non-verbal behavior.

What is the quality of his speaking voice? Does he talk in a soft, gentle, and deliberate manner? Or is he more emphatic, speaking loudly and assertively? Try to get a grasp of the rhythm, cadence, and speed of his speech.

Look at how he carries himself. Pay attention to how he tilts his head. Does he often lean forward? Does he tend to slouch? Or does he keep himself erect all the time?

Does he smile often? Does he often widen his eyes or move his eyebrows to make a point?

People often communicate with their hands – deliberately or unconsciously. Does he do this? Does he use hand gestures to add emphasis or convey his emotions with flourish? Watch how he gestures with his hands.

Observe all of these aspects of his verbal and non-verbal behavior and try to mirror them as you see fit. Note that mirroring is not mimicry. It is more of empathy – actively listening to what the other person is saying – both in his words and behavior -- and responding to it by acting in a way that shows this. It entails responding intelligently and sensitively to the other person. For after all, if you are not listening intently, if you are not paying sufficient attention, you will not be able to “mirror” the other person. Mirroring the other person underscores the fact that you are, indeed, focused on the other person. What is not to like in that? When you try to mirror the energy level and physical mannerisms of the person you are talking to in a way that is natural, he is likely to respond well to it. Without necessarily agreeing to what he says, but merely acting the way he does to some degree, you are likely to make him see you in a positive light. He is likely to think of you as likable and charismatic.

If you use this technique for the right reasons – using it in the right manner and the right time, you will be able to easily make an instant connection with other people.

Conclusion

The impression you make on other people, particularly during the first 60 seconds of meeting them, determines to a great degree if you will be able to effectively connect with them. Use the easy steps presented here and you will be able to create a great first impression, develop instant likability and charisma, and establish rapport with other people.

When you speak of charisma, you may be inclined to think about appearing as someone “special” to other people. True charisma, however, is grounded on how you make others feel – particularly about themselves. If an interaction with you, no matter how short, results in making the other person feel lighter, happier, and better about himself – if he feels special and important because of your actuations, he is likely to see you as likable and charming. Use this guide and you will be on your way to connecting with people without difficulty.

Scroll down for a FREE preview of “Warren Buffett - The Business & Life Lessons Of An Investment Genius, Magnate & Philanthropist”!

Thank you again for your support.

Steve Gold

FREE BONUS!:  Preview Of “Warren Buffett - The Business & Life Lessons Of An Investment Genius, Magnate & Philanthropist”!

![Warren_Buffett_new-1.jpg](images/00009.jpeg)

If you enjoyed this book, I have a little bonus for you; a preview of one of my other books “Warren Buffett - The Business & Life Lessons Of An Investment Genius, Magnate & Philanthropist”. In this book, I take a closer look at exactly who Warren Buffett is as well as examining the truly extraordinary accomplishments he has managed to achieve in his life thus far. In the book I dig deeper into 7 of the major principles that have helped Buffett achieve such unbelievable success. Enjoy the free sample, and feel free to click on the purchase link below if you would like to learn more about this truly incredible individual!

# Introduction

It may be a bold statement, but I believe that no one in the world of investment who’s alive today understands success, wealth and, perhaps even happiness, the way that Warren Buffet does. Not only does the so-called “Sage of Omaha” know how to generate an immense fortune, he also has a solid comprehension of how finite and impermanent money actually is. He may have made a name for himself as an investment strategist, but Buffet often speaks of how loose and overrated the link between wealth and quality of life can be. He would even go as far as to stress – somewhat paradoxically – that the more money one has, the less free and unhappy one is likely to become.

Indeed, it can almost seem at times that despite his influential career in finance, Buffett does not place great importance on money and material possessions. His net worth may be up in the billions, but he lives in the least billionaire-like fashion. Buffett, who’s the antithesis of the typical image of a wealthy business magnate, owns a considerably modest amount of tangible assets compared to his nine-figure net worth peers, and he appears to be disinterested in the extravagant lifestyle of the rich and famous. He embraces the simplicity of daily life, reminding himself from the onset of his career that there are no greater assets one can possess than good health, as well as remembering that the key to happiness lies in the priceless bonds one creates with friends and family.

His impartiality to wealth could not be more evident than in his numerous philanthropic efforts, which includes record-breaking donations amounting to more than half of his accumulated wealth over time.

Regardless of where one stands in life and whatever one’s aspirations are, plenty can be learned by examining the core values that made Warren Buffett one of the most successful and wealthy individuals in the world.

In the chapters that follow, you will see that business and personal success is not so much a result of strategic investment decisions, but rather that it results from cultivating a number of personality traits essential for navigating the world of commerce. Additionally, as Buffett has continuously demonstrated, good character and adherence to moral principles goes a long way in ensuring long-term success, wealth and happiness.

Warren Buffet has made great contributions to the world in the form of a long-standing investment track-record along with his enormously generous philanthropic endeavors. As a business and investment magnate, Buffett’s approach to growing and managing wealth contains a certain humility that is so rarely given attention in a field that is predominantly about strategies and figures. Drawing from his own life experiences, Buffett acknowledges the human element that is often overlooked when it comes to accumulating and maintaining wealth. His philosophy and principles are simple, yet so powerful that they go beyond investment portfolios and apply to practically every aspect of our lives.

Buffett’s extensive career achievements, however, can never measure up to the impressive life he has led. Living by his beliefs and principles, he proves that with patience, perseverance, diligence and hard work, one can build a financially stable and fulfilling life. Most importantly, he has exemplifies that a quality life is one which is lived with generosity, integrity and modesty.

Chapter 1

Plan For The Future

“Someone's sitting in the shade today because someone planted a tree a long time ago.”

Warren Buffett

The path to financial and personal success is not lined with gold but with golden values.

Keeping your path straight, free from distractions or temptations, is the best vision anybody can take while planning their financial future. Investment strategists such as Warren Buffett suggest instilling in yourself from a young age the ability to stick with your plan following concrete steps to get to where you want to be.

Buffett had a vision from when he was a child that he would be rich by investing his money in himself instead of giving away his hard earned money to somebody else. That vision started when he was a young boy in Washington, D.C., where his father served four terms in the U.S. House of Representatives after moving the family from Omaha, Neb. His father was originally a stockbroker and Warren learned the trade of investing by being close to his father. As a teenager in D.C., Buffett invested in placing pinball machines in barbershops. He took the money from those pinball machines and invested in more machines.

He was fortunate from the beginning to have a father who stressed the importance of making sound financial decisions to improve his future. Every bit of his money was important to his development in becoming the second wealthiest person in America, behind business magnate Bill Gates.

Buffett, who was born on Aug. 30, 1930, stresses to young people today to grasp what they have and build on it before giving it away to credit card companies. He warns against spending sprees and living outlandishly. His message: Everything has a price and what you spend today will affect your savings for tomorrow, not only for yourself but for your children and grandchildren.

“Money doesn’t create man, but it is the man who created money,” Buffett said in a recent interview with CNBC.

Money does not define Buffett although he is worth billions. He has maintained his humble values from his modest upbringing in Omaha. He continues to live in the same home in Omaha that he bought in 1958 for $31,500\. The 6,000-square foot home in the Dundee-Happy Hollow Historic is valued today at $250,000, still a modest price for the mega-billionaire who is nicknamed the “Oracle of Omaha”.

It is the only house Buffett owns, which is another rarity for a billionaire who has more personal wealth than some third-world countries. He once also owned real estate in Laguna Beach, Calif., but sold that property in 2005 for $5.45 million, a profit of more than $4 million from when he purchased it in 1993 as a vacation spot for him and his wife. Even when he tried to live lavishly, he made a profit from it, although this was an isolated case where he strayed from his basic principles.

Buffett always had a clear vision of his future since his childhood. He became an investor when he was 11\. In his high school yearbook, he described himself as a “future stockbroker” although he was well on his way. From the start, he had the confidence to achieve his goals because he knew his path would be free of distractions or temptations. He was never consumed by excess to a fault.

 “I don’t think standard of living equates with cost of living beyond a certain point,” Buffett said about his modest home during a 2014 shareholder meeting for Berkshire Hathaway, an American multinational conglomerate holding company that he owns. “Good housing, good health, good food, good transport. There’s a point you start getting inverse correlation between wealth and quality of life. My life couldn’t be happier. In fact, it’d be worse if I had six or eight houses. So, I have everything I need to have, and I don’t need any more because it doesn’t make a difference after a point.”

Buffett is on record saying that having more wealth actually reduces the quality of life. In his opinion, the quality of life is based on basic needs. That includes having good health, adequate housing, nourishment and transportation. Not all who are afforded these needs are content or satisfied. People crave bigger homes, souped-up cars and meals at expensive restaurants. Many of us believe happiness comes from having an extravagant lifestyle.

Buffett’s clear vision of his future from the time he was raised in Omaha and Washington, D.C., has allowed him to become wealthier than even the greediest person can imagine. The invaluable plans from when Buffett was young that created his happy existence involved taking an inventory of his life, embracing the simplicity of his life and never straying from his core values.

When taking an inventory of his life during his formative years at the University of Nebraska and Columbia Business School, Buffett realized his greatest asset aside from his health was his association with his significant other, family and long-standing friends. His inherent assets – his personality, humor and education -- all played a part in his fruitful association with others. They carry no price tag. Those assets define him more than money ever will.

Buffett’s simple pleasures of life include keeping to himself, reading a book without interruption. His idea of a pleasurable evening since his high school years is not being out on the town but instead staying home to watch television and enjoy a hot cup of tea. Buffett believes that taking every opportunity to embrace your simple pleasures is the most valuable move you can make for your future.

Throughout the years, Buffett has stayed true to his core principles and values. He never takes a chance with his investments. He sticks with investing in the sectors he believes will produce the most profit. Maintaining a clear vision of the values needed to reach prosperity has allowed Buffett to stay atop the business world, never wavering.

[Click here to check out the rest of “Warren Buffett - The Business & Life Lessons Of An Investment Genius, Magnate & Philanthropist” on Amazon.](http://amzn.to/1LPu6kp)

Or go to: [http://amzn.to/1LPu6kp](http://amzn.to/1LPu6kp)

Check Out My Other Books!

![Elon Musk - Biography-1.jpg](images/00002.jpeg)

[Elon Musk - The Biography Of A Modern Day Renaissance Man](http://amzn.to/1MBnmB9)

![Elon Musk - Lessons.jpg](images/00003.jpeg)

[Elon Musk - The Business & Life Lessons Of A Modern Day Renaissance Man](http://amzn.to/1jpCQl7)

![Warren_Buffett_new.jpg](images/00004.jpeg)

[Warren Buffett - The Business And Life Lessons Of An Investment Genius, Magnate And Philanthropist](http://amzn.to/1LPu6kp)

![Steve Jobs Thumbnail.JPG](images/00005.jpeg)

Steve Jobs - The Biography & Lessons Of The Mastermind Behind Apple

![Management - .jpg](images/00006.jpeg)

[Management - Achieve Management Excellence & World Class Leadership Skills In 7 Simple Steps](http://amzn.to/1hFnU09)

![Sales_new.jpg](images/00007.jpeg)

[Sales - Easily Sell Anything To Anyone & Achieve Sales Excellence In 7 Simple Steps](http://amazon.com/dp/B018S70JLQ/ref=sr_1_1?s=digital-text&ie=UTF8&qid=6143351094&sr=1-1&keywords=sales)

![Arduino Thumbnail.JPG](images/00008.jpeg)

Arduino - Getting Started With Arduino: The Ultimate Beginner’s Guide

(If the links do not work, for whatever reason, you can simply search for these titles on the Amazon to find them. All books available as ebooks or printed books)

Claim Your Free Gift!

As a token of my appreciation, I have included a special invitation to my mailing list! Simply follow the link below to sign up.

Also, as a member of my mailing list, you’ll have the option of being kept informed of other releases from myself and my publishing house, including FREE access to advanced copies and heavily discounted prices!

For your peace of mind, let me assure you that we have a strict no-spam policy and you are free to unsubscribe at any time if you choose to.

[=>Click HERE to sign up now!<=](http://eepurl.com/bMxlLr)

And when you’re ready, simply click [here](#part0000_split_001.html_b1) to return to the introduction or [here](#part0000_split_005.html_b2) to return to the start of Chapter 2.