![](images/00385.jpeg)

![C:\Users\Michael\AppData\Local\Microsoft\Windows\INetCacheContent.Word\An Introduction to the Microsoft Bot Framework Cover.jpg](images/00001.jpeg)

An Introduction to the Microsoft Bot Framework

Create Facebook and Skype Chatbots using Microsoft Visual Studio and C#

(This book covers the Microsoft Bot Framework Preview Edition)

Copyright 2016

Published By

The Ai Help Website

http://AiHelpWebsite.com

# 
Copyright

Copyright © 2016 by Michael Washington

Cover and internal design © Michael Washington

Editing by Andrea Dickinson (www.QualityBookServices.com)

All rights reserved. No part of this book may be reproduced in any form or by any electronic or mechanical means including information storage and retrieval systems – except in the case of brief quotations in articles or reviews – without the permission in writing from its publisher, AiHelpWebsite.com.

All brand names and product names used in this book are trademarks, registered trademarks, or trade names of their respective holders. We are not associated with any product or vendor in this book.

Microsoft Visual Studio is a registered trademark of Microsoft Corporation. 

Skype is a registered trademark of Microsoft Corporation.

Facebook is a registered trademark of Facebook Inc.

# Table of Contents

[Copyright](#part0000_split_002.html__Toc466087336)

[Table of Contents](#part0000_split_003.html__Toc466087337)

[Dedication](#part0000_split_004.html__Toc466087338)

[Michael Washington](#part0000_split_005.html__Toc466087339)

[Thank  You](#part0000_split_006.html__Toc466087340)

[Microsoft](#part0000_split_006.html__Toc466087341)

[Community](#part0000_split_007.html__Toc466087342)

[Preface](#part0000_split_008.html__Toc466087343)

[Requirements](#part0000_split_009.html__Toc466087344)

[Chapter 1: Understanding the  Microsoft Bot Framework](#part0000_split_010.html__Toc466087345)

[What Is the Microsoft Bot Framework?](#part0000_split_011.html__Toc466087346)

[Chapter 2: Create a Hello World! Bot](#part0000_split_012.html__Toc466087347)

[Creating A Hello World! Bot](#part0000_split_013.html__Toc466087348)

[Using The Bot Emulator](#part0000_split_014.html__Toc466087349)

[Saving User Data](#part0000_split_015.html__Toc466087350)

[Publishing The Bot](#part0000_split_018.html__Toc466087351)

[Registering The Bot With The Microsoft Bot Framework Developer Portal](#part0000_split_019.html__Toc466087352)

[Chapter 3: Using FormFlow](#part0000_split_020.html__Toc466087353)

[A Walk Through](#part0000_split_021.html__Toc466087354)

[Creating The Project](#part0000_split_022.html__Toc466087355)

[Test The Application](#part0000_split_025.html__Toc466087356)

[Saving The Data](#part0000_split_026.html__Toc466087357)

[Chapter 4: Using Dialogs](#part0000_split_030.html__Toc466087358)

[Walk Through](#part0000_split_031.html__Toc466087359)

[Creating The Application](#part0000_split_032.html__Toc466087360)

[Test The Application](#part0000_split_036.html__Toc466087361)

[Dialog Prompts](#part0000_split_037.html__Toc466087362)

[Chapter 5: Using Images, Cards, Carousels, and Buttons](#part0000_split_039.html__Toc466087363)

[Hero Card](#part0000_split_040.html__Toc466087364)

[Carousel](#part0000_split_041.html__Toc466087365)

[Rich Card Attachments In Dialogs](#part0000_split_042.html__Toc466087366)

[Create The Hero Card In The Dialog Class](#part0000_split_043.html__Toc466087367)

[Creating A Re-Usable Hero Card](#part0000_split_047.html__Toc466087368)

[Chapter 6: Implementing A SQL Server Database With Your Bot](#part0000_split_050.html__Toc466087369)

[Create The SQL Server Database](#part0000_split_051.html__Toc466087370)

[Create An ADO.NET Entity Data Model](#part0000_split_054.html__Toc466087371)

[Log To The Database](#part0000_split_055.html__Toc466087372)

[Log Messages In The Dialog Class](#part0000_split_058.html__Toc466087373)

[Test The Database Logging Code](#part0000_split_061.html__Toc466087374)

[View The Data](#part0000_split_062.html__Toc466087375)

[Logging High Scores](#part0000_split_063.html__Toc466087376)

[Update ADO.NET Entity Data Model](#part0000_split_064.html__Toc466087377)

[Alter Code To Log High Scores](#part0000_split_065.html__Toc466087378)

[Display The High Scores](#part0000_split_066.html__Toc466087379)

[Test The Code](#part0000_split_068.html__Toc466087380)

[Publishing A Microsoft Bot Framework Application That Uses a Database](#part0000_split_069.html__Toc466087381)

[Chapter 7: Implementing Language Understanding Intelligent Service (LUIS)](#part0000_split_071.html__Toc466087382)

[Create The LUIS Application](#part0000_split_072.html__Toc466087383)

[Update The Bot Application](#part0000_split_073.html__Toc466087384)

[Implement High Scores](#part0000_split_078.html__Toc466087385)

[Chapter 8: Calling The Microsoft Bot Framework Using The Direct Line API](#part0000_split_081.html__Toc466087386)

[Configuring The Direct Line Connector](#part0000_split_082.html__Toc466087387)

[Create The Web Application](#part0000_split_084.html__Toc466087388)

[Complete The Web Application](#part0000_split_086.html__Toc466087389)

[Run The Application](#part0000_split_088.html__Toc466087390)

[Chapter 9: Using Application Insights To Monitor Your Bot](#part0000_split_090.html__Toc466087391)

[Enable Application Insights](#part0000_split_092.html__Toc466087392)

[Debug The Application](#part0000_split_094.html__Toc466087393)

[Using The Bot Emulator](#part0000_split_095.html__Toc466087394)

[Custom Telemetry](#part0000_split_097.html__Toc466087395)

[Application Insights API summary](#part0000_split_100.html__Toc466087396)

[Application Insights Portal](#part0000_split_101.html__Toc466087397)

[Monitoring A Published Application](#part0000_split_102.html__Toc466087398)

[Chapter 10: Creating a Skype Bot](#part0000_split_103.html__Toc466087399)

[Publishing The Bot](#part0000_split_104.html__Toc466087400)

[Registering The Bot With The Bot Connector](#part0000_split_105.html__Toc466087401)

[Configure Skype](#part0000_split_108.html__Toc466087402)

[Chapter 11: Creating A Facebook Messenger Bot](#part0000_split_109.html__Toc466087403)

[Set-Up Facebook](#part0000_split_110.html__Toc466087404)

[Create A Facebook Developer Account](#part0000_split_112.html__Toc466087405)

[Create A Facebook App](#part0000_split_113.html__Toc466087406)

[Configure The Callback URL and Verify Token](#part0000_split_114.html__Toc466087407)

[Get Page Token](#part0000_split_115.html__Toc466087408)

[Configure The Microsoft Bot Connector](#part0000_split_116.html__Toc466087409)

[Talking To Your Bot](#part0000_split_117.html__Toc466087410)

[About The Author](#part0000_split_119.html__Toc466087411)

# 
Dedication

## Michael Washington

As always, for Valerie and Zachary

# Thank  You

## Microsoft

Dan Driscoll

Jim Lewallen

Simon Michael

Anna Roth

Rebecca Duffy

Daniel Egan

## Community

Ezequiel Jadib

Joe Mayo

Robin Osborne

Gary Pretty 

Mahesh Chand 

Johnathan Lightfoot 

# 
Preface

## Requirements

You must have a computer running Microsoft Windows with Microsoft Visual Studio 2015 (or higher) with Update 3 (or higher) to create the applications described in this book.

You can download the free Visual Studio Community  Edition from https://www.visualstudio.com/vs/community/

You will also need to download and install the Visual Studio 2015  Bot template from http://aka.ms/bf-bc-vstemplate

# Chapter 1: Understanding the
Microsoft Bot Framework

This book covers using Visual Studio 2015 to create Chatbots using the Microsoft Bot Framework. The purpose of this book is to demonstrate, provide examples of, and to explain important concepts of the technology.

## What Is the Microsoft Bot Framework?

![image](images/00002.jpeg)

The [Microsoft Bot Framework](https://dev.botframework.com/) allows you to easily create Bots.

![image](images/00003.jpeg)

You can create bots that interact with your users naturally wherever they are, including Facebook, text, Skype, Office 365 email, and other popular services.

![image](images/00004.jpeg)

The Microsoft Bot Framework contains the following components:

*   Bot Framework Developer Portal – A service that connects your Bot to communication channels such as Facebook, Skype, and email.
*   Bot Builder SDK – A C# and Node.js library that provides a powerful framework for constructing bots that can handle freeform and guided interactions.
*   Bot Directory – A directory of Bots that you can connect to.

The Bot Framework Developer Portal helps you connect your Bot to communication channels. You can write a Bot and expose the Microsoft Bot Framework-compatible API on the Internet. The Bot Framework Developer Portal will forward messages to users, and will send the user messages back to your Bot.

The Bot Builder SDK is an open source SDK hosted on GitHub (https://github.com/Microsoft/BotBuilder-Samples) that provides everything you need to build dialogs. Bot developers at Microsoft created this library to encapsulate functionality required for conversational bots.

The Bot Directory (located at https://bots.botframework.com/) features Bots that you can communicate with through channels exposed through the Bot Connector. 

# Chapter 2: Create a Hello World! Bot

The sample code for this chapter can be obtained at the link “Creating a Hello World! Bot Using The Microsoft Bot Framework” at http://AiHelpWebsite.com/Downloads

The purpose of this chapter is to demonstrate how to get started using the Microsoft Bot Framework, how to create a simple Bot, and how to publish it to the Microsoft Bot Framework Developer Portal.

## Creating A Hello World! Bot

![image](images/00005.jpeg)

Download the Visual Studio 2015 template from http://aka.ms/bf-bc-vstemplate

Save the .zip file in the templates directory of your windows computer located at %USERPROFILE%\Documents\Visual Studio 2015\Templates\

ProjectTemplates\Visual C#

This creates a template that you can use in Visual Studio to create Bot projects.

![image](images/00006.jpeg)

Open Visual Studio.

![image](images/00007.jpeg)

Create a new Project.

![image](images/00008.jpeg)

Select the Bot Application template and name the project HelloWorldBot.

![image](images/00009.jpeg)

Open the MessagesController.cs file in the Controllers folder.

Change the Post method to the following: 

![](images/00010.jpeg)

![image](images/00011.jpeg)

Hit F5 to run the project.

![image](images/00012.jpeg)

Note the web address. You will need it in the next step.

## Using The Bot Emulator

![image](images/00013.jpeg)

Download, install, and run the Bot Framework Emulator from https://aka.ms/bf-bc-emulator

When the emulator starts, connect to the Bot by setting the address to the address indicated in the web browser. However, add /api/messages to the end.

![image](images/00014.jpeg)

In the Bot Emulator, enter Hello in the text box and click the send key (or press enter).

You will see the response in the Chat window and the JSON contents of the response in the JSON window.

## Saving User Data

An important part of any conversation is remembering what a user has previously said.

We can do this using GetPrivateConversationData andSetPrivateConversationData.

To demonstrate how this is handled, add the following to the top of the MessagesController.cs file in the Controllers folder:

![](images/00015.gif)

Next, change the Post method in the MessagesController.cs file to the following:

![](images/00016.jpeg)

![](images/00017.jpeg)

Finally, alter the following section in the HandleSystemMessagemethod (in the MessagesController.cs file) to the following:

![](images/00018.jpeg)

![image](images/00019.jpeg)

Now when we chat with the Bot, it can remember our name.

![image](images/00020.jpeg)

If we tell it to Delete User Data…

![image](images/00021.jpeg)

It will respect our wishes.

## Publishing The Bot

To connect your Bot through channels such as Skype and Facebook Messenger, you need to configure it on the Microsoft Bot Framework Developer Portal. To do that, you will first need to publish it in a publicly accessible location.

This can be any server; however, publishing to Azure is recommended because publishing to it has built-in support in Visual Studio.

First, go to [https://azure.microsoft.com](https://azure.microsoft.com/) and create an account and a subscription if you don’t already have one.

![image](images/00022.jpeg)

Next, Right-click on the Project node (not theSolution node) in Visual Studio and select Publish.

![image](images/00023.jpeg)

Select Microsoft Azure Web Apps.

![image](images/00024.jpeg)

Sign into your Azure account.

Select a subscription.

Then click the New button.

![image](images/00025.jpeg)

Enter a unique Web App name.

Select your subscription.

Select or create a service plan, resource group and region.

Then click the Create button.

![image](images/00026.jpeg)

After the web app has been created, click the Publish button.

![image](images/00027.jpeg)

The web app will open in the web browser.

Note the web address. You will need it in a later step.

## Registering The Bot With The Microsoft Bot Framework Developer Portal

![image](images/00028.jpeg)

Go to the Microsoft Bot Framework Developer Portal at [https://www.botframework.com](https://www.botframework.com/) and sign in with your[Microsoft Account](https://www.microsoft.com/en-us/account).

![image](images/00029.jpeg)

Select Register a bot.

![](images/00030.jpeg)

Fill in all of the fields.

Note:The end point web address is what you saw when the web browser opened in the previous step. However, remember you have to add “/api/messages” to the end of the address and use https:// rather than http://.

![image](images/00031.jpeg)

During the process, you will be prompted to click a link to go to [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/).

It is there that you will get an Application ID and a password.

Make a note of them because you will need to use them to update the Visual Studio project in later step.

![image](images/00032.jpeg)

Click the Register button.

![image](images/00033.jpeg)

The Bot registration will be created.

![image](images/00034.jpeg)

Copy the Bot ID, MicrosoftAppId, and MicrosoftAppPassword from the https://apps.dev.microsoft.com site to theweb.config of the Bot in Visual Studio.

Note: If you forgot to note the MicrosoftAppPassword in the earlier step, you can click the Generate New Password button to create another one.

![image](images/00035.jpeg)

Publish the Bot again.

You are doing this because the Bot Framework will pass the Bot ID, MicrosoftAppId, and MicrosoftAppPassword when it communicates with it.

![image](images/00036.jpeg)

You can now test your Bot using the Bot Framework Developer Portal web page.

![image](images/00037.jpeg)

If you desire, you can click the Publishbutton to submit your Bot to theBot Directory.

You can also [configure channels](http://docs.botframework.com/connector/getstarted/#configuring-channels) for your Bot.

Even if you do not publish your Bot to theBot Directory, you can still call it from your own applications and through any channels you configure.

Note: Chapters 10 and 11 cover how to use the Bot Framework Developer Portal to configure the Skype and Facebook Messenger channels to deploy your Bot on those networks.

# Chapter 3: Using FormFlow

The sample code for this chapter can be obtained at the link “Introduction To FormFlow With The Microsoft Bot Framework” at http://AiHelpWebsite.com/Downloads

![](images/00038.jpeg)

Using [FormFlow](https://docs.botframework.com/en-us/csharp/builder/sdkreference/forms.html) with the [Microsoft Bot Framework](https://dev.botframework.com/) allows you to quickly create a guided conversation to gather information from a user with the least amount of code. While it is less flexible than using Dialogs (Dialogs are covered in the next chapter), it can be combined with Dialogs to increase its functionality.

## A Walk Through

![](images/00039.jpeg)

When a user begins a conversation with the Bot, it introduces itself and asks the user’s name.

![](images/00040.jpeg)

The Bot proceeds to ask questions and gather the responses.

![](images/00041.jpeg)

A feature of FormFlow is that the user can type help at any time to obtain assistance with any question or the FormFlow itself.

As a developer, you get this functionality without the need to write any additional code.

![](images/00042.jpeg)

The FormFlow continues until the form is complete.

## Creating The Project

![image](images/00043.jpeg)

Open Visual Studio.

![image](images/00044.jpeg)

Create a new Project.

![image](images/00045.jpeg)

Select the Bot Application template and name the project HelloFormFlowBot.

![image](images/00046.jpeg)

The project will be created.

![image](images/00047.jpeg)

Right-click on the project. Select Add and then New Item.

We will now create the class that will contain the logic for our FormFlow.

![image](images/00048.jpeg)

Add a new C# class called ProfileForm.cs.

Replace all the code with the following code:

![](images/00049.jpeg)

This code indicates the fields we will gather with our FormFlow.

Notice that the class, as well as the Gender  enum that it consumes, is marked [Serializable].

The Microsoft Bot Framework requires that the classes must be serializable, so the Bot can be stateless.

Save the file.

![image](images/00050.jpeg)

Open the MessagesController.cs file.

Add the following using statements at the top of the file (to support the FormFlow code):

![](images/00051.gif) 

Add the following MakeRootDialog method to the MessagesController class to call the BuildForm method in the ProfileForm class we created earlier:

![](images/00052.jpeg)

Finally, alter the Post method in the MessagesController class to the following:

![](images/00053.jpeg)

Save the file.

## Test The Application

![image](images/00054.jpeg)

Hit F5 to run the application.

![image](images/00055.jpeg)

The web browser will open.

Note the port number and the web address.

![image](images/00056.jpeg)

Open and run the Microsoft  Bot Framework Emulator.

When the emulator starts, connect to the Bot by setting the address to the one indicted in the web browser; however, add /api/messages to the end.

![image](images/00057.jpeg)

Ensure that the Bot URL is connecting to the correct address.

![image](images/00058.jpeg)

Type a message and click the send key (or press Enter).

![image](images/00059.jpeg)

You can now converse with the Bot and fill out the FormFlow.

## Saving The Data

Currently the application does not save the responses from the user. In fact, after you fill the FormFlow out, it will simply ask you to fill it out again.

We can use the [Bot State Service](https://docs.botframework.com/en-us/csharp/builder/sdkreference/stateapi.html) to save and retrieve the values.

Alter the BuildForm method in the ProfileForm.cs file to the following to save the values entered into the form:

![](images/00060.gif)

We are not only storing the values provided by the user, but we are also setting a flag (ProfileComplete), so we don’t ask the user to fill out the form again.

Finally, alter the Post method in the MessagesController class to the following:

![](images/00061.jpeg)

![](images/00062.jpeg)

Now the application will only ask the user to fill in the form one time and display the values received using the Bot State Service.

The values will be persisted by the Microsoft Bot Framework keyed to that user in that conversation.

In our example, we used PrivateConversationData, but the Bot State Service exposes the following methods, each with a different scope:

| Method | Scoped | Description |
| SetUserData() | User | Remembering context object with a user |
| SetConversationData() | Conversation | Remembering context object with a conversation |
| SetPrivateConversationData() | User & Conversation | Remembering context object with a person in a conversation |

# Chapter 4: Using Dialogs

The sample code for this chapter can be obtained at the link “Introduction To Using Dialogs With The Microsoft Bot Framework” at http://AiHelpWebsite.com/Downloads

![image](images/00063.jpeg)

Using Dialogs with the Microsoft Bot Framework allows you to model a conversation with a user. While they are more flexible than using a FormFlow (covered in the preceding chapter), Dialogs require more code.

A Dialog is a class that implements the IDialog interface. Dialogs can be composed with other dialogs to maximize reuse.

A Dialog has a context that contains a stack of dialogs active in a conversation and will maintain the state of the conversation. A Dialog sends messages to a user and is suspended when it is waiting for a response from a user.

A Dialog uses a state stored in its context to resume a conversation. This state is stored in the state service provided by the Microsoft Bot Framework service.

## Walk Through

![image](images/00064.jpeg)

The conversation starts when the User types in a message.

The Bot responds with a greeting and the directions of the game, which is to guess a number from 1 to 10 (chosen at random).

![image](images/00065.jpeg)

The User guesses a number, and the Bot informs the User if they are correct or not.

![image](images/00066.jpeg)

When the User guesses the number correctly, they are offered a chance to play the game again.

If the User chooses not to play the game again, the Bot tells them goodbye.

## Creating The Application

![image](images/00067.jpeg)

Open Visual Studio.

![image](images/00068.jpeg)

Create a new Project.

![image](images/00069.jpeg)

Select the Bot Application template and name the project AiNumberGuesserBot.

![image](images/00070.jpeg)

The project will be created.

![image](images/00071.jpeg)

Right-click on the project. Select Add and then New Item.

We will now create the class that will contain the logic for the Dialog.

![image](images/00072.jpeg)

Add a new C# class called NumberGuesserDialog.cs.

Replace all the code with the following code:

![](images/00073.gif) 

A Dialog is a class that inherits from IDialog.

Note that we must decorate this class as [Serializable].

![image](images/00074.jpeg)

This requires you to implement a StartAsync method.

To implement this, hover the mouse over IDialog<object>, wait a few seconds, and the interface option window will appear.

![image](images/00075.jpeg)

Click the black arrow next to the light bulb and select Implement interface.

![image](images/00076.jpeg) 

The StartAsync method will be created.

This will be called when the Dialog is first instantiated.

![image](images/00077.jpeg)

We want the code to run asynchronously, so add async to the method signature.

Now, change the code inside the method, so the complete method is coded as follows:

![](images/00078.gif)

The last line in the method is context.Wait. This suspends the current Dialog until the user has sent a message to the Bot.

The Wait method takes a method as a parameter (in this case MessageReceivedAsync) to be called to resume the conversation when the response has been received.

![image](images/00079.jpeg)

To implement it, hover the mouse over MessageReceivedAsync, wait a few seconds, and the interface option window will appear.

Click the black arrow next to the light bulb and select Generate method ‘NumberGuesserDialog.MessageReceivedAsync.

![image](images/00080.jpeg)

The MessageReceivedAsync method will be created.

Notice it takes the context of the Dialog and an argument (result).

![image](images/00081.jpeg)

Change the type of the argument from object to IMessageActivity and change the name of the variable from result to argument.

Again, we want the code to run asynchronously, so add async to the method signature and mark it as [virtual](https://msdn.microsoft.com/en-us/library/9fkccyh4.aspx).

Alter the code in the method, so the complete method is coded as follows:

![](images/00082.jpeg) 

Notice the last line (context.Wait(MessageReceivedAsync)) simply calls the method the code is contained in again and again.

We are only doing this to make this example as simple as possible. We will explore a more realistic example in the next section when we add a PromptDialog.

![image](images/00083.jpeg)

Next, open the MessagesController.cs file at …\AiNumberGuesserBot\AiNumberGuesserBot\Controllers\

MessagesController.cs

Replace the default code in the code block that begins: 

![](images/00084.gif) 

With the code:

![](images/00085.jpeg)

This tells the Bot to direct any messages to the NumberGuesserDialog class.

Finally, add the following using statement to the top of the code file:

![](images/00086.gif) 

## Test The Application

![image](images/00087.jpeg)

Hit F5 to run the application.

![image](images/00088.jpeg)

The web browser will open. Note the port number and the web address.

![image](images/00089.jpeg)

Open and run the Microsoft Bot Framework Emulator.

When the emulator starts, connect to the Bot by setting the address to the one indicted in the web browser; however, add /api/messages to the end.

![image](images/00090.jpeg)

Ensure that the Bot URL is connecting to the correct address.

![image](images/00091.jpeg)

Type a message and click the send key (or press Enter).

![](images/00092.jpeg)

The Bot will respond.

This is all the Bot will do at this point; however, this example shows the minimal code to create and consume a Dialog class. 

## Dialog Prompts

A PromptDialog is essentially a Dialog factory for creating simple prompts. It allows you to ask the User for a response and indicate what code will run when the response is given. A PromptDialog spawns a sub-dialog that has its own private state. This sub-dialog is suspended by the Microsoft Bot Framework service while it waits for a response. When it gets a response, it resumes at the point in the code it was at when it was suspended.

This is the primary means of controlling program flow within a Dialog class.

A PromptDialog can be one of the following types:

*   Prompt for an attachment
*   Prompt for one of a set of choices
*   Ask a yes/no question
*   Prompt for a long
*   Prompt for a double
*   Prompt for a string

We will enhance our application to implement a PromptDialog that asks a yes/no question.

First, add the following code to the MessageReceivedAsync method:

![](images/00093.gif)

This code will simply keep looping and counting the guessing attempts if the user does not guess the random number.

If the user does guess the number, the code in the else block will be called.

Right now, the code is not complete. We need to add a PromptDialog under the line // Put PromptDialog here.

![image](images/00094.jpeg)

Type PromptDialog and press the period (.) key. The autocomplete options will show and we will see the option to implement the various types of PromptDialogs.

Choose the Confirm option.

![image](images/00095.jpeg)

We can look in the official documentation at https://docs.botframework.com/en-us/csharp/builder/sdkreference/ and see the method signature requires us to pass the current context, indicate the method to be called when we get a response (resume handler), provide a message to show the user (prompt), and provide a message to display if the response type is not correct (retry). The other parameters are optional.

The following shows the complete code for our implementation:

![](images/00096.gif)

We now need to implement the resume handler method to handle the response (PlayAgainAsync).

![image](images/00097.jpeg)

To implement it, hover the mouse over PlayAgainAsync, wait a few seconds, and the interface option window will appear.

Click the black arrow next to the light bulb and select Generate method ‘NumberGuesserDialog.PlayAgainAsync’.

![image](images/00098.jpeg)

The method will be created.

![image](images/00099.jpeg)

Add async to the method signature.

Alter the method, so the complete code is as follows:

![](images/00100.jpeg)

Hit F5 to run the program and connect to it, using the Bot Framework Emulator…

![image](images/00101.jpeg)

When we guess the correct number, the PromptDialog will appear. When we provide an answer, the PlayAgainAsync method will immediately run to process our answer.

We can spawn another PromptDialog inside the PlayAgainAsync method if we choose, effectively creating an endless chain of PromptDialogs to create branches of code for a conversation.

# Chapter 5: Using Images, Cards, Carousels, and Buttons

The sample code for this chapter can be obtained at the link “Using Images, Cards, Carousels, and Buttons In The Microsoft Bot Framework” at http://AiHelpWebsite.com/Downloads

![](images/00102.jpeg)

Note: The image above shows the Bot in Skype. Deploying a Bot to Skype is covered in Chapter Ten.

Implementing images in your Microsoft Bot Framework application adds a visual element to the interaction with your users.

You can easily pass a media attachment (image/audio/video/file) to a message using code such as this:

![](images/00103.jpeg)

Depending on the [channel](https://docs.botframework.com/en-us/csharp/builder/sdkreference/gettingstarted.html#channels) used and the media type, an image will be displayed or a link will be displayed for the user to download the media element.

However, real power is provided when you use [rich card attachments](https://docs.botframework.com/en-us/csharp/builder/sdkreference/attachments.html#richcards).

There are four card types:

| Card Type | Description | Single or Carousel/List(Multiple Cards) |
| Hero Card | A big image with text | Single or Carousel/List |
| Thumbnail Card  | A small image with text | Single or Carousel/List |
| Receipt Card  | An invoice or receipt | Single |
| Sign-In Card  | A user sign-in form | Single |

## Hero Card

![image](images/00104.jpeg)

In this chapter, we will cover Hero Card.

A Hero Card and a Thumbnail Card differ only in the size of their image and card.

Each consists of the following properties:

| Property | Description |
| Title | Title of the card |
| Text | Text to display on the card |
| Subtitle | A link for the title |
| Images | Actually, only a single image |
| Buttons | One or more buttons (In Skype, only 5 buttons will display on a card. If you have more buttons, it will create two cards.) |
| Tap | An action that is triggered when a user taps on the card (This does not work in some Skype clients, so for Skype, use a hyperlink for the Subtitle property.) |

![](images/00105.jpeg)

To demonstrate implementing a Hero Card, we will start with the code from the previous chapter.

Note: First, you will have to use Manage NuGet Packages in Visual Studio to update Microsoft.Bot.Builder to the latest stable version before you continue.

Also, we will make some small changes, such as making the number to guess from 1 to 5 rather than 1 to 10,  so it shows up well in Skype because Skype will only display 5 buttons on a single card.

Open the project in Visual Studio.

![image](images/00106.jpeg)

Add a new folder and call it Images.

Add the NumberGuesserOpeningCard.png file (you can get the code on the [Downloads page](http://aihelpwebsite.com/Downloads) of the AiHelpWebsite.com) to the Images folder.

Open the MessagesController.cs file (in the Controllers directory), and add the following using statement to the top of the file:

![](images/00107.gif)

![image](images/00108.jpeg)

Next, locate the else if (message.Type == ActivityTypes.ContactRelationUpdate) section in the HandleSystemMessage method.

This method fires when the Bot is added to the Contact list of a user.

Replace all the code in the section with the following code:

![](images/00109.jpeg) 

![image](images/00110.jpeg)

Save the file and hit F5 to run the application.

![image](images/00111.jpeg)

Open and run the Bot using the Microsoft Bot Framework Emulator.

![image](images/00112.jpeg)

In the Emulator, invoke the Contact Relation Update-add event.

![image](images/00113.jpeg)

The Hero Card will display.

Clicking on the card will take you to the AiHelpWebsite.com website.

## Carousel

![image](images/00114.jpeg)

A carousel displays multiple cards (either Hero Cards or Thumbnail Cards) horizontally.

A List (the default layout for multiple cards) displays the cards vertically.

The image above shows what a carousel of two Hero Cards looks like in the Skype client.

![image](images/00115.jpeg)

To implement this, first add the AiLogo_smallSquare.png file (you can get the code on the [Downloads page](http://aihelpwebsite.com/Downloads) of the AiHelpWebsite.com) to the Images folder.

Next, add the following code to the HandleSystemMessage method (above the var connector = new ConnectorClient(new Uri(message.ServiceUrl)); line):

![](images/00116.gif)

Save the file, run the application, and connect to it in the Emulator.

In the Emulator, invoke the Contact Relation Update-add event.

![](images/00117.jpeg)

The first card will show, but you will now see a slider.

Slide it to the right.

![](images/00118.jpeg)

You will then see the second Hero Card.

In Skype, the Subtitle property will display as a hyperlink and be clickable.

## Rich Card Attachments In Dialogs

There are additional challenges when implementing rich card attachments in Dialogs.

Primarily, the biggest challenge is that, inside the Dialog class, you do not have access to the base URL of the application to determine where your images are.

We can address this by using the Bot State Service.

Open the MessagesController.cs file:

![image](images/00119.jpeg) 

Add the following code to the top of the Post method:

![](images/00120.jpeg) 

This will store the CurrentBaseURL and the Recipient using the [Bot State Service](https://docs.botframework.com/en-us/csharp/builder/sdkreference/stateapi.html), so the values can later be retrieved in the Dialog class.

![image](images/00121.jpeg)

Open the NumberGuesserDialog.cs file.

Add the following code above the namespace:

![](images/00122.gif) 

Add this to the top of the class:

![](images/00123.gif)
This will provide a global variable that will be automatically [serialized and persisted](https://docs.botframework.com/en-us/csharp/builder/sdkreference/dialogs.html#echoBot) between calls to store the Base URL.

Add the following code to the top of the MessageReceivedAsync method:

![](images/00124.gif)

This will retrieve the value of CurrentBaseURL that was stored in Bot State Service in the MessagesController class and store it in the strBaseURL global variable.

Add the following Utility method to the class. This method will create 5 CardAction buttons that will be attached to the Hero Card (that we will create in a later step):

![](images/00125.gif)

The buttons are set to the Type “[imBack](https://docs.botframework.com/en-us/csharp/builder/sdkreference/attachments.html#cardaction)”, which makes the button (CardAction) simply post the value (in this case, the button number) back to the Bot.

## Create The Hero Card In The Dialog Class

![image](images/00126.jpeg)

We will now display a Hero Card with 5 buttons in the Dialog class.

First, add the NumberGuesserCard.png file (you can get the code on the [Downloads page](http://aihelpwebsite.com/Downloads) of the AiHelpWebsite.com) to the Images folder.

Next, find the following code in the MessageReceivedAsync method:

![](images/00127.jpeg) 

Replace it with the following code:

![](images/00128.gif)

Save the file, hit F5 to run the project, and connect to it in the Emulator.

![](images/00129.jpeg)

The Bot will now display an image and buttons.

We can either click one of the buttons or enter a number to play the game.

The following image shows what it looks like in Skype:

![image](images/00130.jpeg)

## Creating A Re-Usable Hero Card

If there are a few more places we need to display the Hero Card with the buttons,

we will want to create a re-usable Hero Card.

This Hero Card will not have an image, only buttons.

First, add the following utility method to the Dialog class:

![](images/00131.jpeg) 

Note that it calls the CreateButtons  utility method that we created earlier.

Now, locate the following code:

![](images/00132.gif)

Replace it with:

![](images/00133.gif)

The code will now call the ShowButtons method that will return the Hero Card.

Finally, find the following code:

![](images/00134.gif)

Replace it with:

![](images/00135.gif)

![](images/00136.jpeg)

The Bot will now display the Hero Card, with only the buttons, in each situation where we called the utility method.

# Chapter 6: Implementing A SQL Server Database With Your Bot

The sample code for this chapter can be obtained at the link “Implementing A SQL Server Database With The Microsoft Bot Framework” at http://AiHelpWebsite.com/Downloads

![](images/00137.jpeg)

Microsoft Bot Framework  Chatbot applications that require information to be stored, queried, and shared with multiple users will require a central storage repository.

Using Microsoft SQL Server and Microsoft Azure will allow you to easily implement this feature.

![image](images/00130.jpeg)

To demonstrate implementing a database with a Microsoft Bot Framework application, we will start with the code from the previous chapter.

## Create The SQL Server Database

We will start by creating a database and logging the messages sent to and from the Bot.

![image](images/00138.jpeg)

Open the project in Visual Studio.

![](images/00139.jpeg)

In the Solution Explorer in Visual Studio, right-click on the Project (not the Solution), and select Add, then Add ASP.NET Folder, then App_Data.

Note:  App_Data is a special folder that will contain the database we will create. We use this folder because we will have an option to not deploy this folder (and the database that it will contain) when we publish the application to Azure. This will be covered later.

![](images/00140.jpeg)

Right-click on the App_Data folder. Select Add and then New Item.

![image](images/00141.jpeg)

Add a SQL Server Database.

Name it BotData.mdf.

![image](images/00142.jpeg)

We will now create a table in the database to hold our data.

Right-click on the database and select Open.

![image](images/00143.jpeg)

Expand the database elements in the tree.

Right-click on Tables and select Add New Table.

![image](images/00144.jpeg)

Paste the following script in and click the Update button:

![](images/00145.gif) 

![](images/00146.jpeg)

Click Update Database.

![image](images/00147.jpeg)

The table will be created.

![image](images/00148.jpeg)

Right-click on the Tables node and select Refresh.

![image](images/00149.jpeg)

The table will show.

## Create An ADO.NET Entity Data Model

![image](images/00150.jpeg)

We will now create an Entity Data Model to allow programmatic access to the database.

Switch to Solution Explorer view.

![image](images/00151.jpeg)

Create a folder called Models.

Right-click on the Models folder. Select Add and then New Item.

![image](images/00152.jpeg)

Add an ADO.NET Entity Data Model and call it BotData.

![image](images/00153.jpeg)

When the Entity Data Model Wizard opens, select EF Designer from database.

Click Next.

![image](images/00154.jpeg)

Select BotData.mdf in the database dropdown (if it is not already selected).

Check the box next to Save connection settings in Web.Config.

Click Next.

![image](images/00155.jpeg)

Select Entity Framework 6.x.

Click Next.

![image](images/00156.jpeg)

Expand the tree to reveal the UserLog table and click the checkbox next to it.

Accept the other default values.

Click Finish.

![image](images/00157.jpeg)

The BotData.edmx an Entity Data Model will be created.

You can close the BotData.edmx for now.

## Log To The Database

We will now create code that will log (most of) the messages to and from the Bot to the database.

First, create a file called Utility.cs and use the following code:

![](images/00158.jpeg)

This creates a utility method to allow us to trim any text we store in the database. This ensures that no message is too long to be stored in the database. This would cause an error.

![image](images/00159.jpeg)

Next, find the following code in MessagesController.cs:

![](images/00160.gif)

Replace it with:

 ![](images/00161.gif)

This code logs the messages being sent from the user to the Bot.

## Log Messages In The Dialog Class

![image](images/00162.jpeg)

The [Dialog](https://docs.botframework.com/en-us/csharp/builder/sdkreference/dialogs.html) class creates a response to the user.

Find all code in the NumberGuessserDialog.cs file (there will be multiple places) that send a text response to the user, which contain these lines:

![](images/00163.gif)

Add the following code above the existing lines of code (again, there will be multiple places you will do this):

![](images/00164.gif)

When we have a PromptDialog, we don’t have a [reply  Activity](https://docs.botframework.com/en-us/csharp/builder/sdkreference/routing.html#replytoactivity). In this case, we need to make one, so we have the values we need to log to the database.

Find the following code in the Dialog class:

![](images/00165.gif)

Add the following code above the existing lines of code:

![](images/00166.gif)

Note: The CongratulationsStringPrompt is set by the existing code to indicate that the user has won the game.

## Test The Database Logging Code

![image](images/00167.jpeg)

Hit F5 to run the application.

![image](images/00168.jpeg)

The web browser will open.

Note the port number and the web address.

![image](images/00169.jpeg)

Open and run the Microsoft Bot Framework Emulator.

When the emulator starts, connect to the Bot by setting the address to the one indicted in the web browser; however, add /api/messages to the end.

![image](images/00170.jpeg)

Ensure that the Bot URL is connecting to the correct address.

![image](images/00171.jpeg)

Enter Helloand click the send button to start a conversation with the Bot.

![](images/00172.jpeg)

Play the game with the Bot.

Close the web browser to stop the application and return to Visual Studio.

## View The Data

![image](images/00173.jpeg)

We will now view the data that was logged to the database.

In the Solution Explorer in Visual Studio, right-click on BotData.mdf and select Open.

![image](images/00174.jpeg)

This will open the Server Explorer.

Right-click on the UserLog table and select Show Table Data.

![image](images/00175.jpeg)

The logged data will be displayed.

## Logging High Scores

![image](images/00176.jpeg)

We will now add code to log and display High Scores.

We have to alter the database first to store the number of turns required to win and the name of the winner.

In the Server Explorer, right-click on the UserLog table and select Open Table Definition.

Note: If you don’t have this option, install the latest SQL Server Data Tools (SSDT) from https://msdn.microsoft.com/library/mt204009.aspx

![](images/00177.jpeg)

Add the following fields:

*   CountOfTurnsToWin [int]
*   WinnerUserName [nvarchar(150)]

Click the Update button.

![](images/00178.jpeg)

When the Preview Database Updates box shows, click Update Database.

![image](images/00179.jpeg)

The Data Tools Operations window will indicate when the update is complete.

## Update ADO.NET Entity Data Model

![image](images/00180.jpeg)

We have to update the ADO.NET Entity Data Model to have programmatic access to the newly added fields.

In the Solution Explorer, click on BotData.edmx to open it in the designer.

In the designer, right-click on the UserLog table and select Update Model from Database.

![](images/00181.jpeg)

When the Update Wizard shows, select the Refresh tab and then select the UserLog table. Click Finish.

## Alter Code To Log High Scores

![image](images/00182.jpeg)

We will now alter the code in the Dialog class to log the winning user and the number of turns they required to win.

In the NumberGuesserDialog.cs file, locate the following code:

![](images/00183.gif)

Add the following lines of code below the code above:

![](images/00184.gif)

## Display The High Scores

![image](images/00185.jpeg)

We will now add code to display the High Scores whenever the user types High Scores.

Open the MessagesController.cs file and add the following method to the class:

![](images/00186.jpeg) 

We will now add the code that will call the ShowHighScores method we just added.

In the MessagesController.cs file, locate the following code:

![](images/00187.gif) 

Replace it with the following code:

![](images/00188.jpeg) 

Finally, to let the user know they can type High Scores to see the high scores, find the following code in the Dialog class:

![](images/00189.gif)

Change it to:

![](images/00190.jpeg)

## Test The Code

![](images/00191.jpeg)

Now when we type High Scores, we can see the high scores for the past day.

![image](images/00192.jpeg)

The image above shows what the high scores look like when the Bot is published and viewed through the Skype client.

## Publishing A Microsoft Bot Framework Application That Uses a Database

![image](images/00193.jpeg)

To publish the Bot, we can follow the directions in Chapter 2: Create a Hello World! Bot.

However, unlike this chapter, that chapter does not cover publishing a Bot that uses a database.

![image](images/00194.jpeg)

If you do not have a Microsoft Azure account, go to https://azure.microsoft.com and create an account and a subscription.

![image](images/00195.jpeg)

Log into the Azure  [web portal](https://portal.azure.com/) and select SQL databases.

![image](images/00196.jpeg)

Add a new database.

![](images/00197.jpeg)

Fill in the form to create a new database.

Note: If you do not already have a server to put the database on, you will be prompted to create one. At that time, you will create a user name and password. This is the user name and password you will use in the connection string to connect to the database when you use the deployment wizard in Visual Studio (covered later).

![image](images/00198.jpeg)

After you create the database, you can view the ADO.NET(SQL authentication) connection string for the database in the Overview section.

Note: The connection string will not have the username and password. You will use the username and password of the Azure server that contains the database.

![image](images/00199.jpeg)

In the Solution Explorer in Visual Studio, right-click on the project node and select Publish.

![image](images/00200.jpeg)

In the Publish wizard, fill out the fields to publish your Bot to Azure.

On the Settings tab:

1.  Select Exclude files from the App_Data folder.
    This will prevent the BotData.mdf database file from being published to Azure. You are doing this because the .mdf file cannot be used on Azure.
2.  Enter the connection string to the database (running on Azure) in BotDataEntities.
    You can get the ADO.NET(SQL authentication) connection string for the database in the Overview section for the database in the Azure portal. Use the “…” button to help you connect to the database and construct the connection string.
3.  Check Use this connection string at runtime.
    This will update the web.config of the published application, so the published application will connect to the database on Azure.
4.  Click the Publish button.

![image](images/00201.jpeg)

In the Server Explorer in Visual Studio, right-click on the database and select Open in SQL Server Object Explorer.

Note: If you don’t have this option, install the latest SQL Server Data Tools (SSDT) from https://msdn.microsoft.com/library/mt204009.aspx

![image](images/00202.jpeg)

This will open the SQL Server Object Explorer.

Right-click on the Tables node under the database and select Add New Table.

![](images/00203.jpeg)

Use the following script to create the required table and click the Update button:

![](images/00204.gif)

![image](images/00205.jpeg)

When the Preview Database Updates box shows, click Update Database.

Note: You can also use the [Cloud Explorer for Visual Studio 2015 extension](https://visualstudiogallery.msdn.microsoft.com/84e83a7c-9606-4f9f-83dd-0f6182f13add) to manage your Azure databases inside Visual Studio.

# Chapter 7: Implementing Language Understanding Intelligent Service (LUIS)

The sample code for this chapter can be obtained at the link “Implementing Language Understanding Intelligent Service (LUIS) In Microsoft Bot Framework” at http://AiHelpWebsite.com/Downloads

![](images/00206.jpeg)

Using Language Understanding Intelligent Service (LUIS) in your Microsoft Bot Framework application allows you to create chat bots that are easier for your end-users to interact with.

![image](images/00207.jpeg)

For this example, we will start with the code created in the previous chapter.

This chapter covers how to create a number guessing game and storing and displaying the high scores. In the previous chapter, the user is required to type in the exact words High Scores, and they could only see the high scores for the past day.

![image](images/00208.jpeg)

In this chapter, we will alter the code to allow the user to see the high scores for the past week, the past month, or the past days they specify (up to 30 days).

Most importantly, we will allow the user to type their request using normal language and then detect the intent of the user and the important related entities (such as the number of days).

We will do this by creating an application using the Language Understanding Intelligent Service (LUIS) and then interfacing that application with our existing Bot.

## Create The LUIS Application

![image](images/00209.jpeg)

The first step is to go to https://www.luis.ai/ and create an account on the Language Understanding Intelligent Service (LUIS) site and log in.

![image](images/00210.jpeg)

Create a New Application.

![image14](images/00211.jpeg)

We will call it HighScores, and after filling out the other fields, we click Add App.

![image](images/00212.jpeg)

Now we need to create Entities. These are elements we will need to identify and gather, so our Bot can perform operations based on their value. In our example, we want to create two Entities:

*   PeriodOfTime – Detect if the user entered a word describing the amount of days (but not the actual days), for example, week or month
*   Days – Detect if the user entered the actual days such as 3 or three

![image](images/00213.jpeg)

Click the plus button next to the Entities label (on the left-hand side of the editor) to open a box that will allow you to add each Entity (one at a time).

![image](images/00214.jpeg)

When you’re done, the Entities will be displayed.

![image](images/00215.jpeg)

Next, we will add an Intent.

Note: The “None” Intent, to be triggered when an utterance by the user does not match a programmed intent, will be automatically created)

Click the plus button next to the Intents label.

![image](images/00216.jpeg)

Enter HighScores for the Intent name.

Enter Show me the high scores for the past week for Enter an example of a command that triggers this intent. (This is also known as a sample utterance.)

Click Save.

![image](images/00217.jpeg)

The utterance will now display in the New utterances tab.

We want this utterance to trigger the HighScores  Intent, so select it from the dropdown.

![image](images/00218.jpeg)

We also want to detect the associated Entity.

Click on the word week, it will then be highlighted, and a popup box will appear.

Select PeriodOfTime.

![image](images/00219.jpeg)

Finally, click Submit.

![image](images/00220.jpeg)

Continue to enter and label additional utterances.

Note: Remember to label any Entities that indicate a number as Days.

![image](images/00221.jpeg)

Continue to train the service.

You will notice that eventually it will start detecting the Entities on its own.

However, many times you will still have to correct it.

Enter and correct at least ten different utterances.

![image](images/00222.jpeg)

Click the Train button in the bottom left-hand corner of the interface to train the model.

![image](images/00223.jpeg)

Next, click the Publish button.

![image](images/00224.jpeg)

Finally, click the Publish web service button.

![image](images/00225.jpeg)

The published end-point will be displayed.

Make note of the App ID and Subscription Key. You will need these later to be used in the Bot application.

Note: Starting 12/31/2016, App ID will no longer be used. You will only use a Subscription Key to connect to your LUIS application.

Note: For a production application, you will obtain your [subscription key from Azure](https://azure.microsoft.com/en-us/services/cognitive-services/language-understanding-intelligence-service/).

Now, we need to update the Bot to call the LUIS service…

## Update The Bot Application

![image](images/00226.jpeg)

Open the project from the previous chapter in Visual Studio.

Add a new file called LUISDialogClass.cs, using the following code:

![](images/00227.jpeg)  ![](images/00228.jpeg)

This code will pass text entered into the Bot to the LUIS application and trigger the None or HighScores methods based on what the LUIS application determines the Intent is, which the entered text matches.

We decorate each method with a LuisIntent decoration, setting the name of an Intent (for example, [LuisIntent("HighScores")]) to indicate which method should be triggered.

Note: The code is not complete at this point. We will complete the code in later steps.

![image](images/00229.jpeg)

Ensure that you enter the App ID and Subscription Key from your LUIS application in the LuisModel decoration at the top of the class.

This is how the code knows what LUIS application to connect to.

![image](images/00230.jpeg)

We now need to call the LUISDialogClass, instead of the previously configured NumberGuesserDialog class, when a user communicates with the Bot.

The new LUIS code (LUISDialogClass) will call the NumberGuesserDialog class when needed, for example, when the user has not triggered the HighScores intent.

Open the MessagesController.cs file in the Controllers folder.

Replace the following code:

![](images/00231.gif) 

With:

![](images/00232.gif)

![image](images/00233.jpeg)

There are places where the NumberGuesserDialog will need to call LUISDialogClass, for example, when the user has entered a response that is not a number being guessed as part of the game.

The NumberGuesserDialog class will need to return control back to the LUISDialogClass.

Replace the code in the NumberGuesserDialog class (encapsulated in the brackets) that begins like the text below:

![](images/00234.gif)

With the following code:

 ![](images/00235.jpeg) 

![image](images/00236.jpeg)

The NumberGuesserDialog class is no longer the root class, so we will need to alter it slightly again, so it starts up the game properly when it is triggered by the LUISDialogClass.

Locate the following code in the StartAsync method:

![](images/00237.gif)

Replace it with:

![](images/00238.gif)

This code shows the welcome screen to start the number guessing game.

## Implement High Scores

![](images/00239.jpeg)

At this point, if we run the application and connect to it in the Microsoft Bot Framework Emulator, we can play the game.

However, if we type anything that triggers the HighScores  LUIS Intent, we will receive an error because the code to handle this has not been implemented yet.

![image](images/00240.jpeg)

Open the LUISDialogClass.cs file and locate the following code:

![](images/00241.gif)

Replace it with:

![](images/00242.jpeg) 

This code will set the number of days the user is asking the high scores to include. It first tries to detect if a period of time was passed (in the PeriodOfTime entity). If it has been, the code converts a known period of time to a number of days.

If a number of days was passed (in the Days entity), the code tries to convert the days into a number. If it cannot, it assumes the number of days was passed as a word not a number. If this is the case, it passes the value to the ParseEnglish method that converts the word to a number.

Note: You can get the ParseEnglish method from http://stackoverflow.com/questions/11278081/convert-words-string-to-int

The number of days (and the current context) is then passed to the ShowHighScores method.

As the final step, enter the following code to implement the ShowHighScores method into the LUISDialogClass:

![](images/00243.jpeg)

# Chapter 8: Calling The Microsoft Bot Framework Using The Direct Line API

The sample code for this chapter can be obtained at the link “Calling The Microsoft Bot Framework Using The Direct Line API” at http://AiHelpWebsite.com/Downloads

![image](images/00244.jpeg)

You may need to call your Microsoft Bot Framework Bot directly from a custom application, a service, or a website. The Microsoft Bot Connector Direct Line REST API allows you to do this. In addition, it allows you to authenticate a user in your application and securely communicate with the Bot as that user.

![image](images/00245.jpeg)

The Direct Line API exposes a REST API that allows you to communicate with a single Bot that has been registered with the [Microsoft Bot Connector Service](https://docs.botframework.com/en-us/csharp/builder/sdkreference/connector.html).

This API is intended for developers who want to communicate with their Bot from their own client applications, such as mobile apps, a service, or even a [HoloLens](https://www.microsoft.com/microsoft-hololens/en-us).

![image](images/00246.jpeg)

The procedure for working with the API is:

1.  Register your Bot with the Bot Framework Developer Portal
2.  Configure the Direct Line Connector
3.  Use the credentials obtained from the Bot Framework Developer Portal to make REST based calls to communicate with the Bot
    In our example, we will use the Microsoft.Bot.Connector.DirectLine  Nuget package to help us make the calls.

![image](images/00247.jpeg)

Note: The rendering of the output will be the responsibility of the developer of the custom application that is calling the Direct Line API.

Media such an images, cards, and buttons will require custom code to render in a manner that is appropriate for the particular application.

![image](images/00248.jpeg)

The example application we will build will create a custom client that will allow a user to create an account, sign-in, and securely communicate with the Bot that was created in the previous chapter.

## Configuring The Direct Line Connector

![image](images/00249.jpeg)

We want to configure the Direct Line connector for our Bot.

Go to https://dev.botframework.com/, log in, and select My Bots.

Open a Bot that has been deployed to the Microsoft Bot Framework Developer Portal.

![image](images/00250.jpeg)

The first step is to make a note of the Bot handle you gave your Bot. You will need this later when you create the Web Application.

![image](images/00251.jpeg)

Under Add another channel, click the Add button next to Direct Line.

![](images/00252.jpeg)

When the Configure  Direct Line screen appears, click the Generate  Direct Line secret button.

![](images/00253.jpeg)

Copy the Secret code. You will need this later when you create the Web Application.

Click I’m done configuring Direct Line button.

The screen will close.

## Create The Web Application

![image](images/00254.jpeg)

Open Visual Studio.

![image](images/00255.jpeg)

From the toolbar in Visual Studio, select File, then New, and then Project.

![image](images/00256.jpeg)

Select Web and then ASP.NET Web Application (.Net Framework).

Enter DirectLineBot for the Name.

Select the Create directory for solution box.

Press OK.

![image](images/00257.jpeg)

When the application configuration box appears, select the MVC template.

Ensure that Individual User Accounts is selected for Authentication. If not, click the Change Authentication button and change it.

Press OK.

![image](images/00258.jpeg)

The application will be created.

We need to add the Microsoft.Bot.Connector.DirectLine  NuGet  Package that will allow us to easily communicate with the DirectLine API.

![image](images/00259.jpeg)

In the Solution Explorer, right-click on the DirectLineBot project node (not the Solution node), and select Manage NuGet Packages.

![image](images/00260.jpeg)

When the NuGet Package configuration window appears, click the Browse button.

Enter Microsoft.Bot.Connector.DirectLine in the search box to conduct the search.

When the Microsoft.Bot.Connector.DirectLine package shows up, click on it, so its properties appear in the window on the right.

Click the Install button to install the package.

![](images/00261.jpeg)

Click OK when the Preview window shows.

![](images/00262.jpeg)

Click the I Accept button when the License Acceptance window appears.

![image](images/00263.jpeg)

The Microsoft.Bot.Connector.DirectLine assembly will be installed.

![image](images/00264.jpeg)

Hit F5 to debug and run the application.

The application will open in the web browser.

![image](images/00265.jpeg)

You will see the default web application created by the MVC template.

We can click the Register button to create a new account.

We can also click the Log in button to log in using a registered account.

## Complete The Web Application

![image](images/00266.jpeg)

We will update the home page to show the chat box and the Bot response only if the user has created an account and logged in.

Stop debugging the application and open the Index.cshtml file in the Views/Home folder.

Replace all of the code with the following code:

![](images/00267.gif)

![image](images/00268.jpeg)

Open the HomeController.cs file in the Controllers folder, and replace all the code with the following code:

![](images/00269.jpeg)

At this point the code is not complete; however, it sets up the basic framework.

Replace ** INSERT YOUR SECRET CODE HERE ** and ** INSERT YOUR BOTID HERE ** with the values from you own published Bot.

When a logged in user loads the page or submits text to the Bot, the TalkToTheBot method is called.

To implement it, add the following method to the HomeController class:

![](images/00270.jpeg)

The TalkToTheBot method calls the ReadBotMessagesAsync method to read the response from the Bot.

To implement it, add the following method to the HomeController class:

![](images/00271.jpeg)

When there is an image that is returned by the Bot, the ReadBotMessagesAsync method calls the RenderImageHTML method.

To implement it, add the following method to the HomeController class:

![](images/00272.gif)

## Run The Application

![image](images/00273.jpeg)

Hit F5 to run the application.

The application will open in the web browser. Initially, we are not logged in, so we will be unable to communicate with the Bot.

![image](images/00274.jpeg)

Click the Register button to create an account.

![image](images/00275.jpeg)

Fill in the required information and click the Register button.

![image](images/00276.jpeg)

After you have created an account, you can click the Log in button to log in (if you are not already logged in).

![image](images/00277.jpeg)

You will know you are logged in when you see your email address in the menu bar and on the Home page.

![image](images/00278.jpeg)

You can now communicate with the Bot and run the same code that was created in the previous chapter.

![image](images/00279.jpeg)

When we look at the data in the database on Azure, we see the UserID and UserName for messages posted to the Bot are completely under the control of the following custom code:

![](images/00280.jpeg) 

# Chapter 9: Using Application Insights To Monitor Your Bot

The sample code for this chapter can be obtained at the link “Using Application Insights With Microsoft Bot Framework” at http://AiHelpWebsite.com/Downloads

![](images/00281.jpeg)

With Application Insights, you can insert a few lines of code in your Bot to find out what your users are doing.

When you install Application Insights, you are installing a small instrumentation package in your application. Next, you set up an Application Insights resource in the Microsoft Azure portal.

The instrumentation you install monitors your app and sends telemetry data to the Microsoft Azure portal. The Microsoft Azure portal shows statistical charts and has powerful search tools to help you monitor your application and diagnose any problems.

![](images/00282.jpeg)

To demonstrate this, we will start with the Bot created in Chapter Six.

![image](images/00283.jpeg)

This will require using Microsoft Azure. If you do not have a Microsoft Azure account, go to https://azure.microsoft.com and create an account and a subscription.

## Enable Application Insights

![image](images/00284.jpeg)

Open the AiNumberGuesserBot project in Visual Studio.

In the Solution Explorer, right-click on the Project (not the Solution), and select Add Application Insights Telemetry.

![image](images/00285.jpeg)

First, you will be required to log into your Microsoft Azure Account.

After doing so, you will be presented with a form to create an Application Insights resource (by choosing the New resource option in the Send telemetry to dropdown) or connect to an existing Application Insights resource (by selecting it in the Send telemetry to dropdown).

After selecting the configuration options, click the Add button to proceed.

![image](images/00286.jpeg)

Application Insights assemblies will be added to the project.

![image](images/00287.jpeg)

If you get an error, most likely you have components that need to be updated.

![image](images/00288.jpeg)

In the Solution Explorer in Visual Studio, right-click on the Project (not the Solution), and select Manage NuGet Packages.

![image](images/00289.jpeg)

Select Updates, select the components that the error message indicates need to be updated, and click the Update button.

![image](images/00290.jpeg)

When the Review Changes box shows, click the OK button.

Next, right-click on the Project and select Add Application Insights Telemetry again to re-start the process.

The Application Insights components should now install successfully.

## Debug The Application

![image](images/00291.jpeg)

Before you try to debug, clear any MicrosoftAppId and MicrosoftAppPassword settings there may be in the Web.config file and then save the file.

This is required, so you can easily debug locally.

Remember to replace any settings if you need to re-publish the application.

![image](images/00292.jpeg)

Hit F5 to run the project.

![image](images/00293.jpeg)

The application will open in the web browser.

Note the web address, as you will need it in the next step.

## Using The Bot Emulator

![](images/00294.jpeg)

Open and run the Microsoft Bot Framework Emulator.

When the emulator starts, connect to the Bot by setting the address to the one indicted in the web browser; however, add /api/messages to the end.

![](images/00295.jpeg)

In the Bot Emulator, enter Hello in the text box and click the send key (or press enter).

You will see the response in the Chat window and the JSON contents of the response in the JSON window.

![image](images/00296.jpeg)

You should see a window pop up that provides links to the telemetry data.

![image](images/00297.jpeg)

You can also access the data by clicking on the links in the ApplicationInsight.config section in the Solution Explorer of Visual Studio while the application is running.

![image](images/00298.jpeg)

Also, you can right-click on the Project and select Application Insights to show the menu that will provide all the options.

![image](images/00299.jpeg)

Selecting Search Live Telemetry or Search Debug Session Telemetry will open a window in Visual Studio that will display telemetry data.

Note: See Learn more about Application Insights tools in Visual Studio at https://azure.microsoft.com/en-us/documentation/articles/app-insights-visual-studio/ for more information on using these windows.

![image](images/00300.jpeg)

For full Telemetry Readiness, ensure all the green dots are checked. If any aren’t, click on them.

![image](images/00301.jpeg)

It will stop debugging to add components.

![image](images/00302.jpeg)

You will be able to click a button to add or configure the components.

![image](images/00303.jpeg)

The components will be added.

![image](images/00304.jpeg)

The result will be displayed.

## Custom Telemetry

![image](images/00305.jpeg)

One of the most powerful features of Application Insights is being able to use it to track your own custom telemetry.

We will now demonstrate using it to track when a game is started, completed, what number a user needed to guess, and how many attempts they required.

In the AiNumberGuesserBot project, open the NumberGuesserDialog.cs file and add the following using statements:

![](images/00306.gif)

Next, add the following line to the class:

![](images/00307.gif)

Finally, add the following lines to the StartAsync method:

![](images/00308.gif)

This will track a game being started and the number the user needs to guess.

Also, add the following code to track the game completed:

![](images/00309.gif)

There are a number of API calls we can use to track custom events as the following table illustrates:

## Application Insights API summary

From: https://azure.microsoft.com/en-us/documentation/articles/app-insights-api-custom-events-metrics/

| Method | Used for |
| [TrackPageView](https://azure.microsoft.com/en-us/documentation/articles/app-insights-api-custom-events-metrics/#page-views) | Pages, screens, blades, or forms |
| [TrackEvent](https://azure.microsoft.com/en-us/documentation/articles/app-insights-api-custom-events-metrics/#track-event) | User actions and other events. Used to track user behavior or to monitor performance. |
| [TrackMetric](https://azure.microsoft.com/en-us/documentation/articles/app-insights-api-custom-events-metrics/#track-metric) | Performance measurements such as queue lengths not related to specific events |
| [TrackException](https://azure.microsoft.com/en-us/documentation/articles/app-insights-api-custom-events-metrics/#track-exception) | Log exceptions for diagnosis. Trace where they occur in relation to other events and examine stack traces. |
| [TrackRequest](https://azure.microsoft.com/en-us/documentation/articles/app-insights-api-custom-events-metrics/#track-request) | Log the frequency and duration of server requests for performance analysis. |
| [TrackTrace](https://azure.microsoft.com/en-us/documentation/articles/app-insights-api-custom-events-metrics/#track-trace) | Diagnostic log messages. You can also capture 3rd-party logs. |
| [TrackDependency](https://azure.microsoft.com/en-us/documentation/articles/app-insights-api-custom-events-metrics/#track-dependency) | Log the duration and frequency of calls to external components on which your app depends. |

You can [attach properties and metrics](https://azure.microsoft.com/en-us/documentation/articles/app-insights-api-custom-events-metrics/#properties) to most of these telemetry calls.

![image](images/00310.jpeg)

Run the application and enter some sample data.

![image](images/00311.jpeg)

When you select the Application Insights menu in Visual Studio and select Explore Telemetry Trends…

![](images/00312.jpeg)

…you can then select Inspect your custom events.

![image](images/00313.jpeg)

Click the Analyze Telemetry button to process the latest data. You will see where the Properties and Metrics have been tracked.

Note: It will take a few minutes for your custom events to show.

You can double-click on a trend to drill into the data.

![image](images/00314.jpeg)

This will take you to the search screen where you can filter further and view the details of each individual event.

## Application Insights Portal

![image](images/00315.jpeg)

You can access the Application Insights Portal on the Microsoft Azure site by selecting it from the menu in Visual Studio.

![image](images/00316.jpeg)

It is there you can see and change your Pricing tier.

You can also obtain your Instrumentation Key.

## Monitoring A Published Application

![image](images/00317.jpeg)

You can monitor your published Bot.

Publish your Bot. (See Chapter 2 for directions on this.) After your Bot is published on the https://dev.botframework.com/ site, select My bots.

![](images/00318.jpeg)

Edit the Bot configuration.

![](images/00319.jpeg)

Enter the Instrumentation Key (from the Microsoft Azure site) and click Save changes.

This will enable additional properties and metrics to track.

![image](images/00320.jpeg)

Return to the Application Insights resource on the Microsoft Azure site.

You can now monitor your published application and create custom charts using default tracking data and your custom properties and metrics.

# Chapter 10: Creating a Skype Bot

The sample code for this chapter can be obtained at the link “Creating a Skype Bot Using The Microsoft Bot Framework” at http://AiHelpWebsite.com/Downloads

![](images/00321.jpeg)

You can easily create a Skype Bot and deploy it to Skype.

![](images/00282.jpeg)

To demonstrate this, we will start with the Bot created in Chapter Six.

Note: If you have not previously deployed your Bot, skip down to the section labeled “Register Skype”.

## Publishing The Bot

![image](images/00322.jpeg)

The first step is to connect the AiNumberGuesserBot to the Microsoft Bot Framework Developer Portal.

To do this, we need to publish it in a publically accessible location. This can be any server; however, publishing to Azure is recommended because publishing to it has built-in support in Visual Studio.

![image](images/00323.jpeg)

First, go to https://azure.microsoft.com and create an account and a subscription (if you don’t already have one).

![image](images/00324.jpeg)

Next, open the AiNumberGuesserBot project in Visual Studio and right-click on the Project node (not the Solution node), and select Publish.

![image](images/00325.jpeg)

Select Microsoft Azure App Service.

![image](images/00326.jpeg)

Sign into your Azure account and then click the New button.

![image](images/00327.jpeg)

Ensure the type is Web App.

Enter a unique Web App name, select your subscription, select or create a service plan and resource group and click the Create button.

![image](images/00328.jpeg)

After the web app has been created, click the Publish button.

![image](images/00329.jpeg)

The web app will open in the web browser.

Note the web address as you will need it in a later step.

## Registering The Bot With The Bot Connector

![image](images/00330.jpeg)

Go to the Microsoft Bot Framework portal at http://dev.botframework.com and sign in with your [Microsoft Account](https://www.microsoft.com/en-us/account).

![image](images/00331.jpeg)

Select Register a bot.

![image](images/00332.jpeg)

Fill in all of the fields.

![image](images/00333.jpeg)

Note: The end point web address is what you saw when the web browser opened in the previous step.

However, you have to add /api/messages  to the end of the address and use https:// rather than http://.

![image](images/00334.jpeg)

At one point in the form, you will see a link you will click to go to

https://apps.dev.microsoft.com

It is there that you will get an Application ID and a password.

![image](images/00335.jpeg)

Make a note of them because you will need to use them to update the web.config file in the Visual Studio project later.

![image](images/00336.jpeg)

Click the Register button.

![image](images/00337.jpeg)

The Bot registration will be created.

When you return to the http://dev.botframework.com page, you will see the Microsoft App ID from the https://apps.dev.microsoft.com site has been entered into your Bot’s configuration.

![image](images/00338.jpeg)

Copy the Bot ID (Bot handle) and MicrosoftAppId and MicrosoftAppPassword from http://dev.botframework.com and [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/) to the web.config of the Bot in Visual Studio.

Note: If you forgot to note the MicrosoftAppPassword in the earlier step, you can click the Generate New Password button at [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/) to create another one.

![image](images/00339.jpeg)

In Visual Studio, Publish the Bot again.

You are doing this because the Bot Connector will pass the Bot ID and MicrosoftAppId and MicrosoftAppPassword when it communicates with it.

![image](images/00340.jpeg)

Return to the Bot configuration page at http://dev.botframework.com.

You can now click the Test button on that page to test the connection to your Bot.

![image](images/00341.jpeg)

You can now [configure channels](http://docs.botframework.com/connector/getstarted/#configuring-channels) to your Bot.

When you have configured channels, if you desire, you can click the Publish button to submit your bot to the Bot Directory.

Even if you do not publish it to the Bot Directory, you can still call it from your own applications and through any channels you configure.

## Configure Skype

![image](images/00342.jpeg)

To add the Bot to Skype, click the Add to Skype button on the Bot configuration page at http://dev.botframework.com.

![](images/00343.jpeg)

You will be directed to a Skype configuration page for the Bot.

Click the button to Add to Contacts.

![image](images/00344.jpeg)

Click Allow in the popup box.

![image](images/00345.jpeg)

Skype will open, and you can select the Bot from your contacts and converse with it.

# Chapter 11: Creating A Facebook Messenger Bot

The sample code for this chapter can be obtained at the link “Creating A Facebook Bot Using Microsoft Bot Framework” at http://AiHelpWebsite.com/Downloads

![image](images/00346.jpeg)

You can easily create a Bot and deploy it on Facebook.

![image](images/00002.jpeg)

To demonstrate this, we will start with the Bot created in Chapter Two.

## Set-Up Facebook

![image](images/00347.jpeg)

The first step is to log into your Facebook.com account (or create one).

![image](images/00348.jpeg)

Select Create Page.

![image](images/00349.jpeg)

Select a template, fill in the required information, and click Get Started.

![image](images/00350.jpeg)

To get the Facebook Page ID, which you will need later, click on the About tab.

![image](images/00351.jpeg)

Locate the Facebook Page ID.

## Create A Facebook Developer Account

![image](images/00352.jpeg)

Go to https://developers.facebook.com/docs/apps/register and click the button to create a Facebook  Developer Account.

![image](images/00353.jpeg)

Click the slider to Yes to accept the policies and click Register.

## Create A Facebook App

![image](images/00354.jpeg)

Next, go to https://developers.facebook.com/ and log in again if needed.

![image](images/00355.jpeg)

Select Add a New App.

![image](images/00356.jpeg)

Select basic setup.

![image](images/00357.jpeg)

Fill in the information and click Create App ID.

![image](images/00358.jpeg)

Make a note of the App ID as you will need it in a later step.

Click the Show button to display the App Secret. Make a note of it as you will need it in a later step.

![image](images/00359.jpeg)

Now that the App is created, you need to configure it to use Facebook Messenger.

Click Add Product.

![image](images/00360.jpeg)

Select Messenger.

![image](images/00361.jpeg)

Select Get Started.

![image](images/00362.jpeg)

Facebook Messenger has been added.

You now need to configure it to talk to the Microsoft Bot Connector.

## Configure The Callback URL and Verify Token

![image](images/00363.jpeg)

Go to [https://dev.botframework.com/](https://dev.botframework.com/) and Sign in.

![image](images/00364.jpeg)

Select My bots.

![image](images/00365.jpeg)

Select a published bot. (See Chapter Two for directions on how to do this.)

![image](images/00366.jpeg)

Click the Add button next to the Facebook Messenger channel.

![](images/00367.jpeg)

Click the expander next to Set webhook callback url and verify token.

![image](images/00368.jpeg)

Use the Select buttons to individually select and copy the Callback Url and Verify Token.

![image](images/00369.jpeg)

Return to [https://developers.facebook.com](https://developers.facebook.com/), select your application, and in the settings for Messenger, click the Setup Webhooks button.

![image](images/00370.jpeg)

Enter the Callback URL and Verify Token you copied, check the Subscription  Fields indicated in the image above, and click the Verify and Save button.

![image](images/00371.jpeg)

After the Webhooks have been set, click the dropdown next to Select a Page.

![image](images/00372.jpeg)

Select the Facebook page you created earlier.

![image](images/00373.jpeg)

Next, click the Subscribe button.

## Get Page Token

![image](images/00374.jpeg)

In the Token Generation section, select the page that you previously created.

![image](images/00375.jpeg)

A Page Access Token will be created.

Copy the Page Access Token.

## Configure The Microsoft Bot Connector

![image](images/00376.jpeg)

Return to https://dev.botframework.com/ and select your Bot again. Then click the Edit button next to the Facebook Messenger channel.

Click the expander next to Enter your credentials.

Enter the information you gathered in the earlier steps and click the Resubmit button.

![image](images/00377.jpeg)

Check the box next to Enable this bot on Facebook Messenger.

Click I’m done configuring Facebook Messenger button.

## Talking To Your Bot

![image](images/00378.jpeg)

You can now talk to your Bot by navigating to

https://www.messenger.com/t/{Your Page ID}/

This will take you to Facebook Messenger, and after logging in with your Facebook  ID, it will allow you to converse with your Bot.

![image](images/00379.jpeg)

Until your App is approved and made public, only you can chat with your Bot.

To create accounts to test it, go to [https://developers.facebook.com/](https://developers.facebook.com/) s

Select the App and then select Roles and then Test Users.

Fill in the form that displays to create test users.

![image](images/00380.jpeg)

To allow real Facebook users to test it, select Roles and then Add Testers.

Fill in the form that displays to allow access for the users.

![image](images/00381.jpeg)

To make the Bot public, select App Review. Then click the slider to change it from No to Yes.

![image](images/00382.jpeg)

To request the needed permissions, select Settings under Messenger then click the Request Permissions button.

![image](images/00383.jpeg)

Select pages_messaging and then click the Add 1 Item button.

See this page for more information on the App review process

https://developers.facebook.com/docs/messenger-platform/app-review

About The Author

![MichaelWashingtonSmallRound](images/00384.jpeg)

Michael Washington is an ASP.NET, C#, and Visual Basic programmer. He has extensive knowledge in process improvement, billing systems, and student information systems. He is a Microsoft MVP. He has a son, Zachary, and resides in Los Angeles with his wife, Valerie.

He has written several tutorials that are posted at [http://AiHelpWebsite.com/Blog](http://AiHelpWebsite.com/Blog).

He is the author of six previous books:

*   Creating HTML 5 Websites and Cloud Business Apps Using LightSwitch In Visual Studio 2013-2015 (LightSwitchHelpWebsite.com)
*   Creating Web Pages Using the LightSwitch HTML Client In Visual Studio 2012 (LightSwitchHelpWebsite.com)
*   OData And Visual Studio LightSwitch (LightSwitchHelpWebsite.com)
*   Creating Visual Studio LightSwitch Custom Controls (Beginner to Intermediate) (LightSwitchHelpWebsite.com)
*   Building Websites with VB.NET and DotNetNuke 4 (Packt Publishing)
*   Building Websites with DotNetNuke 5 (Packt Publishing)