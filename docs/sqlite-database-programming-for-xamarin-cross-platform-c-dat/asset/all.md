![](Image00011.jpg)

SQLite Database Programming for Xamarin

Anthony Serpico

Table of Contents

[About this book](#text00000.html_filepos0000021182)

> [Acknowledgements](#text00000.html_filepos0000021290)

> [Conventions used in this book](#text00000.html_filepos0000022002)

> [Code formatting](#text00000.html_filepos0000027830)

> [Who this book is for](#text00000.html_filepos0000028612)

> [How to use this book](#text00000.html_filepos0000029605)

> [About the author](#text00000.html_filepos0000031571)

> [Personal note](#text00000.html_filepos0000032976)

> [Feedback](#text00000.html_filepos0000034261)

[Part 1\. Data persistence for mobile apps](#text00000.html_filepos0000034885)

> [The nature of mobile applications](#text00000.html_filepos0000035025)

> > [SQLite](#text00000.html_filepos0000037150)

> > [Offline, online, and occasionally connected apps](#text00000.html_filepos0000039039)

> > [Is this some kind of joke?](#text00000.html_filepos0000043768)

> > [Do I really need all of this?](#text00000.html_filepos0000054691)

> [Understanding Where HotRiot fits in](#text00000.html_filepos0000055268)

> [Database design considerations](#text00000.html_filepos0000056873)

> > [Designing for SQLite](#text00000.html_filepos0000062371)

> > > [Primary keys and foreign keys](#text00000.html_filepos0000063519)

> > > [Structuring your database](#text00000.html_filepos0000066093)

> > > [Defining fields](#text00000.html_filepos0000069947)

> > > [Including primary keys](#text00000.html_filepos0000071576)

> > > [Linking tables](#text00000.html_filepos0000072149)

> > [Searching a relational database](#text00000.html_filepos0000075031)

> > [Designing for Mongo synching](#text00000.html_filepos0000076360)

> > [Suggestions for designing your SQL](#text00000.html_filepos0000077756)

> > > [Storing dates and times in SQLite](#text00000.html_filepos0000081790)

> [Getting SQLite.XM](#text00000.html_filepos0000084233)

> [Creating an application skeleton](#text00000.html_filepos0000085112)

> [Platform specific code](#text00000.html_filepos0000089533)

[Part 2\. Data storage on the device](#text00000.html_filepos0000091119)

> [Describing your apps databases](#text00000.html_filepos0000091245)

> [Schema initialization](#text00000.html_filepos0000110589)

> > [Including a SQL statements properties file in Android](#text00000.html_filepos0000113410)

> > [Including a SQL statements properties file in iOS](#text00000.html_filepos0000114288)

> > [Parameterized queries](#text00000.html_filepos0000115959)

> > [Understanding the SQL statements properties file](#text00000.html_filepos0000118367)

> > > [Defining table statements](#text00000.html_filepos0000120734)

> > > [Defining insert statements](#text00000.html_filepos0000123775)

> > > [Defining alter table statements](#text00000.html_filepos0000128118)

> > > [Defining index statements](#text00000.html_filepos0000130354)

> > > [Defining select, update, and delete statements](#text00000.html_filepos0000132623)

> > [Creating tables](#text00000.html_filepos0000134739)

> > [SQLite naming constraints](#text00000.html_filepos0000141830)

> > [Initializing the database](#text00000.html_filepos0000142886)

> [Using the SxmTransaction class](#text00001.html)

> > [Inserting records into the database](#text00001.html_filepos0000165730)

> > > [Committing transactions](#text00001.html_filepos0000188493)

> > > [The insertResponse object](#text00001.html_filepos0000189589)

> > > [Saving file attachments](#text00001.html_filepos0000191538)

> > [Updating records](#text00001.html_filepos0000197500)

> > [Deleting records](#text00001.html_filepos0000207304)

> > [Error Processing](#text00001.html_filepos0000213092)

> > > [Initialization error processing](#text00001.html_filepos0000214220)

> > > [The SxmException object](#text00001.html_filepos0000227718)

> > > [Transaction error processing](#text00001.html_filepos0000230397)

> > > [Programming for errors](#text00001.html_filepos0000256231)

> > > [Some final thoughts regarding errors](#text00001.html_filepos0000263678)

> > [Searching the database](#text00001.html_filepos0000265131)

> > > [Processing record data in-line](#text00001.html_filepos0000282273)

> > [Embedding SQL in your code](#text00001.html_filepos0000294967)

> [Multi-database statement processing](#text00001.html_filepos0000297667)

> [Understanding transactions](#text00001.html_filepos0000300456)

> [Transaction visibility](#text00001.html_filepos0000310491)

> [Performing joins across databases](#text00001.html_filepos0000324109)

> [Locking and concurrency](#text00001.html_filepos0000341500)

> > [Deadlock conditions](#text00001.html_filepos0000362697)

> > [Nesting connections](#text00001.html_filepos0000364092)

> [Serializing transactions using the SxmSTransaction class](#text00001.html_filepos0000393767)

> [Dynamic Queries](#text00002.html)

> > [Using parameterized placeholders](#text00002.html_filepos0000409414)

> > [SQL Injection dangers](#text00002.html_filepos0000426210)

> > [Directly inserting query parameters](#text00002.html_filepos0000431568)

> [Making schema changes](#text00002.html_filepos0000439022)

> > [Adding/Modifying tables](#text00002.html_filepos0000440050)

> > [Creating/Deleting indexes](#text00002.html_filepos0000445953)

> > [Dropping tables](#text00002.html_filepos0000451497)

> [The SxmConnection class](#text00002.html_filepos0000452253)

> > [Creating an SxmConnection](#text00002.html_filepos0000454681)

> > [Using an SxmConnection](#text00002.html_filepos0000466309)

[Part 3\. Data synchronization to the cloud](#text00002.html_filepos0000475119)

> [Understanding SQLite.XM synchronization](#text00002.html_filepos0000478055)

> [Setting-up a server-side infrastructure](#text00002.html_filepos0000485954)

> > [Creating the replication database tables](#text00002.html_filepos0000488539)

> > [Activating synchronization in SQLite.XM](#text00002.html_filepos0000495620)

> [Synchronization details](#text00002.html_filepos0000497740)

> [Synchronizing files](#text00002.html_filepos0000502579)

> [Coordinating synchronization](#text00002.html_filepos0000506845)

> [Customizing synchronization](#text00002.html_filepos0000512290)

> > [Pre-synchronization processing](#text00002.html_filepos0000514012)

> > > [Writing a pre-synchronization delegate](#text00002.html_filepos0000528424)

> > > [Pre-synchronization abort conditions](#text00002.html_filepos0000562249)

> > > [Multi-table synchronizations error processing](#text00002.html_filepos0000564324)

> > [Synchronization error processing](#text00002.html_filepos0000569461)

> > > [Handling exception synchronization errors](#text00002.html_filepos0000579430)

> > > [Handling processing synchronization errors](#text00002.html_filepos0000583403)

> > > [Invalid data errors and non-unique data errors](#text00002.html_filepos0000587601)

> > > [Writing a synchronization error handler](#text00002.html_filepos0000632899)

> > [Post-synchronization processing](#text00003.html)

> > > [Writing a post-synchronization delegate](#text00003.html_filepos0000656671)

> [Synchronizing to your own private back-end server](#text00003.html_filepos0000665866)

> > [How custom synchronization works](#text00003.html_filepos0000674515)

> > [Designing for custom synchronization](#text00003.html_filepos0000676107)

> > [Writing a custom synchronization delegate](#text00003.html_filepos0000679674)

[Appendix A - SQLite Error Codes](#text00003.html_filepos0000710459)

SQLite Database Programming for Xamarin

© 2015 Anthony Serpico

All rights reserved. No part of this book may be reproduced, stored in a retrieval system, or transmitted in any form or by any means without the prior written consent of the author, except in the case of short quotations embedded in critical articles or reviews or certain other non-commercial uses permitted by copyright law.

Every effort has been made in the writing of this book to ensure the accuracy of the information presented herein.  However, the information in this book is without warranty, either express or implied. Neither the author, publisher, dealers, nor distributors of this book will be held liable for any damages caused or alleged, either directly or indirectly by this book.

About this book

Acknowledgements

I am grateful for the considerable time and effort put forward by Dr. Raoul Salazar as a technical editor and in providing me with guidance and support in writing this book.

Dr. Salazar is an innovative, results driven CTO and Educator whose career incorporates both industry and academia. His unique blend of technical expertise, combined with his software development, problem solving and teaching skills has earned him the respect of his colleagues in industry, academia, and from corporations to whom he provides his services. He created over 150 training courses.

Conventions used in this book

The following typographical conventions are used.

`Fixed width:` Used for code listings, including SQL statements. Also used inside paragraphs when referring to program elements such as function names, variable names, environment settings, and keywords.

**Bold** : Is used (sparingly) to highlight or emphasize some important point or to enhance readability.

*`Fixed width italic`* `:` Used to show text that is to be replaced with user supplied values.

An example code listing is shown below.

 `public`  `void` ` executeQuery (` `string` ` command, ` `ArrayList` ` parameterValues)`

`  {`

 `try`

`    {`

 `if` ` (command == ` `null` `)`

 `throw`  `new`  `Exception` ` (` `ErrorMessages` `.error [` `"missingSQL"` `]);`

 `if` ` (connCommand == ` `null` `)`

`          connCommand = dbConn.CreateCommand ();`

 `else`

`          releaseDataReader();`

**`1`** `     connCommand.CommandText = command;`

 `connCommand.CommandType = System.Data.` `CommandType` `.Text;`

**`2`** `     addCommandParameters (parameterValues);`

**`3`** `     connDataReader = connCommand.ExecuteReader ();`

`    }`

 `catch` ` (System.` `Exception` ` ex) `

`    {`

`      logger.log (ex, System.Reflection.` `MethodBase` `.GetCurrentMethod ().ToString ());`

`    }`

` }`

Code listings are shown with the default color coding used by Xamarin Studio at the time of writing. Paragraphs that explain listings will reference line numbers that are shown in the left column of the listing. Referencing line numbers do not necessarily start on the first line of code. Code listings are mostly devoid of basic error checking, error processing, rudimentary optimizations or anything else that might increase their length or otherwise detract from their primary purpose.

Code formatting

I’ve worked hard to make the code examples as easy to read as possible. Most are very short, so that helps a lot. Unfortunately, the myriad of screen sizes and devices for eBooks makes formatting uncertain at best. Code that displays nicely for one configuration may prove unreadable for others.

It has been my experience that reading this book from a tablet in landscape orientation provides the best view. If you find the code examples difficult to follow due to formatting, you can try changing the font size to see if that helps. Often times, this is enough to set things right.

Who this book is for

This book is designed to be read by mobile app developers that are using or intend to use the Xamarin framework and want to learn how to use the SQLite.XM library. In order to get the most out of this book, you’ll need a basic understanding of C# and have at least some general knowledge of SQL. There is no complex SQL or C# in this book, so a basic understanding of each is sufficient to get you through. Of course, the more you know the better. If you’re a Java developer, you should have no problem with the C# examples. Having a basic understanding of Android or iOS development concepts will also be helpful. Again, there isn’t any complex Android or iOS employed by any of the sample code. For the most part, it’s pretty simple stuff. I try and stay on point and focused on SQLite, SQLite.XM and the best database practices for mobile development.

How to use this book

This book is intended to be more than a simple guide to using SQLite.XM. I try and give advice and make suggestions, and, where appropriate, provide you with a rational for making certain engineering choices. Every project is different, and the choices you make may very well differ from my advice. My hope is that by providing insight into my thinking, I will help you with questioning your own decisions. Sometimes you’ll agree with my advice and suggestions and other times you won’t. Either way, it doesn’t really matter, so long as I promote critical thinking in weighing your own design options, I will have done my job. There is rarely one right way when it comes to coding.

In Part 1 of this book, I spend some time talking in general terms about data persistence along with issues specific to mobile app development. I also spend a bit of time going over the various technologies used in the book to build our data persistence layer. I then go on to discuss database design and challenges specific to designing for mobile apps.

Part 2 is dedicated to explaining how to use SQLite.XM for data persistence on the device. This is the heart of the book. If you have some experience with mobile app development, and know a bit about relational database design, you may choose to skip Part 1 and jump to this section to get right into the specifics of SQLite.XM. If you do decide to skip ahead, be sure to first read the section ‘Platform specific code’ as it has some instructions that you need to be aware of.

Part 3 is where I explain SQLite.XM and cloud replication; how to set up a server-side database and how to get data moved, or copied, from the device to your cloud server. If you don’t need to replicate to a server, you can skip this section.

About the author

I have been a professional software developer since 1986 doing work at IBM, The Nuclear Regulatory Commission, for Bell Laboratories and at a host of smaller firms, including the startup Sezme. I have had the opportunity to work a broad spectrum of computing, from low level embedded systems development in assembler to JVM and .net CLR virtual machine programming in Java and C#. I even had the opportunity to dabble in microcode for a brief period of time. My early career was focused on computer graphics, including OpenGL, digital image processing, and image compression. I developed a proprietary spatial domain compression algorithm intended to be used where traditional cosine transforms proved computationally too expensive. A bit later I was the lead developer for SPG in the creation of the image editor ColorWorks, which was delivered on the OS/2 and Windows platforms. ColorWorks was one of NASAs favored tools for color correcting/enhancing images taken with the Hubble telescope. I later focused my attention on database and Web work for the creation of HotRiot. HotRiot is an SaaS that provides back-end services for mobile and Web applications. I am currently the technical lead in the development of a mobile messaging app for Android and iOS using Xamarin and SignalR.

Personal note

This is my first foray into publishing. I opted to self-publish because I wanted to provide detailed subject matter coverage beyond what is possible in a blog or other shorter venue, but still offer my writing free of charge. This would not have been possible with a publisher. I have been asked a number of times; why free?  It’s true that writing a book take a considerable amount of time and energy. Not to mention the work put in by proof readers and tech reviewers. I was surprised by how hard it was to get to a first revision. I have a new appreciation for what authors go through in getting their works published. But I wanted to contribute back into the tech community. Over the years, I have benefited from countless resources made available by others; including blogs, programming help, and open source code. This was an opportunity for me to make a contribution back. If this book is well received, I will follow-up with another. I have learned a lot about mobile messaging with SignalR that I would like to share. If I publish again, I will try to continue to offer my books for free. Thanks for choosing to read this book and I hope you learn and enjoy.

Feedback

If you have any feedback related to this book, for example, errors, suggestions etc., please let me know. I will continuously update the online manuscript as I make edits, this should improve the experience for future readers. Your help with this is greatly appreciated. I’m always happy to assist with SQLite.XM. If you need some help or advice or need something clarified, please drop me a line I’ll do my best to help.

ajserpicoj@gmail.com

Part 1\. Data persistence for mobile apps

The nature of mobile applications

In traditional client-server computing, a client normally connects to a central database server, often through a front-end proxy, for data storage/processing services. If that connection cannot be established, the application is normally unable to run. For the most part, this is okay. The way these applications are designed, packaged, and distributed, this makes sense. This traditional model relies on a continuous connection to a middle tier. For the type of tasks these applications perform, this is all well enough and it helps to simplify their design. Think of any Web based application of significance or any typical enterprise application. It’s true that HTML 5 offers a number of offline storage options, but these are not widely used. The storage technologies that are available are somewhat limited in their capabilities and browser support is non-uniform. Having to deal with the myriad of browser combinations is enough to dissuade most developers from using one of the structured storage solutions offered in HTML.

For mobile applications, a more flexible model is needed. First, network connectivity for mobile devices is much less certain. Not only do connections go in-and-out with much greater frequency, their quality and speed can vary greatly. So, relying on an external database can be sketchy. Also, the type of tasks that mobile apps are called on to perform, along with user expectations, require that they have much more autonomy than their Web or enterprise counterparts. Users will not tolerate spotty service from their mobile apps. With this in mind, mobile applications should be designed to operate without a network connection to the fullest extent possible. This will almost always require some kind of structured data storage solution on the device. Fortunately, a database infrastructure is present on the most popular mobile operating systems. Both iOS and Android ship with a relational database pre-installed: SQLite.

SQLite

SQLite is the most widely deployed relational database in the world, by far. It is included in virtually every iOS and Android device. If you count the number of active devices as measured by Google and Apple, this adds up to several billion. No other database comes close.

Unless the data storage requirements for your app are extremely simple, you’re going to need a storage solution beyond what you can easily implement yourself in a simple key/value structure or basic properties file. SQLite is a very attractive option as there’s no setup required for iOS or Android and its presence is guaranteed on both OS’. This simplifies packaging, deployment and installation for your app, removing any friction that might be caused by installing and managing a separate, embedded database server. Also, knowing that SQLite will be available, allows you to write a common, shared data persistence layer that will work across platforms when using Xamarin. While it is unfortunate that Microsoft doesn’t include SQLite as part of Windows Phone, it is, nonetheless, easy enough to install using NuGet.

Now, you might get the sense that I’m enthusiastic about SQLite simply because it’s convenient. While it is convenient to use, SQLite qualifies as full featured relational database, putting all of the power of a traditional transactional database engine at the disposal of your app. You would be hard pressed to find a better datastore for your mobile application.

I’m not going to go into detail about SQLite beyond what is needed to use our persistence layer, SQLite.XM. However, I encourage you to explore SQLite in more detail. Their website, *sqlite.org* , has a wealth of information.

Offline, online, and occasionally connected apps

Mobile applications generally follow one of three models:

*   Pure Offline Application
*   Pure Online Application
*   Occasionally Connected Application (OCA)

Pure offline applications don’t require any network connectivity in order to operate. The datastore is local on the device and all data and application logic resides locally. Data that’s generated by the application is not synched with an external or back-end server. These type of mobile application are entirely self-contained and self-supported, and are a bit rare. It is somewhat unusual to see pure offline mobile applications.

In contrast, pure online applications require a network connection in order to function. These apps may include a local database, but this is not a requirement. Even if a local datastore is used, it’s generally limited to such things as configuration information or other metadata. These apps establish regular or continuous communications with a remote server that may, in addition to providing database services, also provide supporting application logic.

An Occasionally Connected Application (OCA) represents a middle ground between the offline and online model. These apps can operate for extended periods without a network connection but eventually need connectivity in order to complete their processing cycle. They almost always include a local database and normally synch their local data with a back-end server. Even though these apps synch their local data, OCAs don’t rely on a remote datastore in order to function. These types of apps are designed to provide a base level of functionality when disconnected with full functionality made available when connectivity is established. OCAs may also rely on a back-end server for supporting application logic. Of the three models, OCA is the most flexible and complex to design and code.

With respect to which of the three models you should choose, the answer is easy if your application truly qualifies as an offline app. In this case, simply use the offline model. This is the easiest of the three to develop and there is little benefit to complicating things. Consider yourself lucky, you don’t need to deal with intermittent connectivity issues, remote communications, synching or any of a host of problems that come along with client server computing.

Unfortunately, it is much more likely that you’re creating an app that follows the online or OCA model. In this case, things can get a bit murky. In most instances, an online mobile application can be designed as an OCA, and vice versa. Actually, I think it would be more accurate to say that most online mobile apps are really misidentified OCAs.

Let us look at an example. Imagine you are creating an app for a specialty merchant that’s similar to the Amazon price comparison application. The app searches for items in inventory via a barcode scan and displays price comparisons. For this example, let’s say this is the only feature in our application. This would seem to be an online application, as the app needs to communicate with a back-end server in order to locate the scanned product information. This is true. But what are you going to do if there is no connectivity? You could simply error out of a price check request by displaying some status message to the user. Not such a great outcome. The other option is to offer to save the request locally until network connectivity is reestablished, at which time, the app will perform the search and present the results to the user. Much better! Our seemingly online application, when thought through, is really an OCA. When there is no network connectivity, it still allows users to perform product scans. The app completes its processing cycle, searching and displaying price comparisons, when connectivity is reestablished.

As a general rule, it’s better to choose the OCA model whenever possible. If you think your app qualifies as a pure online application, think again. Really think through the various use case scenarios. In most instances, you will find your application is better designed as an OCA. While this does add complexity, it also provides for the best user experience.

Is this some kind of joke?

A complete cross-platform data storage solution for a typical OCA requires a number of technologies working together. The reason for this traces back to the need for OCAs to function offline and online and to be able to synch. This requires an infrastructure that can support a “store and forward” architecture for the application data. This, in turn, necessitates a database on the device, a server-side database, and a middleware tier to link the two. In our case, we want our solution to be cross platform, so we’ll also need a cross platform development framework. Admittedly, the reasons for choosing a cross-platform solution goes beyond the data layer, but this is nonetheless a requirement. It would also be nice to have an abstraction layer that simplifies working with SQLite and that include the logic for performing synching. If you put this all together, you end up with a list that looks like the one below

*   **SQLite** : Our local device datastore.
*   **SQLite.XM** : Our SQLite abstraction layer, which includes support for data synching.
*   **A server-side middle tier** : For the examples in this book, we’re using HotRiot.com.
*   **A server side database** : Either a traditional relational database, for example, MySQL, or a NoSQL document datastore, such as MongoDB.
*   **Xamarin** : Our cross-platform framework.

The list above is quite a combination of technologies. It includes a device-side and server-side database, a cross-platform development framework, a SQLite abstraction layer with synching logic, and a server-side middle tier. That might seem like a bit much just to support data persistence. But it turns out, to fully implement a cross-platform OCA, they are all needed.

Let’s have a look at where each of these components fits in.

**SQLite** is light weight, server-less traditional relational database. By “traditional”, I mean a database that supports transactions with ACID compliance, joins, triggers, implements standard SQL, etc. As the name implies, SQLite is a database implementation designed as a light weight solution with a small footprint intended to run on devices with limited resources.

iOS and Android both have a SQLite database engine built in as part of their platform. So there’s nothing you need to do to make SQLite available to your application for these two OS’. Windows Phone offers SQLite as an extension that’s simple to install from Visual Studio. Most mobile applications need to save at least some data locally. SQLite is a natural choice as it is readily available for mobile and very capable.

**SQLite.XM** is a SQLite abstraction layer written in C# and designed to be used with apps developed using Xamarin.  It makes using SQLite with Xamarin a snap. It shields your application from the details of working directly with SQLite. Instead, you app interfaces with a high level, cross-platform layer that provides database CRUD functionality. In addition to providing an abstraction layer that greatly simplifies database searching and record retrieval. SQLite.XM also takes care of organizing your SQL, initializing your apps schema, performing schema updates, and synchronizing data to a server-side database.

At this point, the obvious question is: where does SQLite.XM synch device data? SQLite.XM comes out of the box ready to synch with HotRiot.com. HotRiot is a hosted server-side platform for mobile application; see the next section for more details. SQLite.XM is also capable of communicating with any server for the purpose of data synching. It allows you to insert your own delegate method into the synchronization processing chain for the purpose of writing an interface to any cloud based server of your choosing. I go into detail explaining this is part 3 of the book; “Data synchronization to the cloud.”

**A server-side middle tier:** An OCA needs to synch its device data to a server side datastore. This is taken care of by SQLite.XM on the device side. However, a middleware server is needed in order to actually write the data into to the database. As a general rule, you never let the device connect directly to the server database. Instead, requests are made to a middle tier which then performs the database operation on behalf of the client. However, there is more to this. We don’t just synch data to the server for the sake of synching. We do it to get information over to the server in order to support functionality needed by the app, which requires the support of a back-end.

Just reading and writing to a back-end database such as MySQL or Mongo will require middleware support. But there is a host of other services that many apps also require, for instance:

*   Push notifications through Apple Push Notification Service or Google Cloud Messaging.
*   Provide a central repository for apps that need to share data generated between devices’
*   Document management support. Such as generating thumbnails or moving file attachments to a key/value store such as AWS S3.
*   Support for event triggers. For example, contacting a user when a record is stored in the database that includes some information of interest.
*   Bulk email processing for contacting all of users by email.
*   Managing permissions for security.
*   Sending email confirmations, for example when a user registers with an application.

This is not an exhaustive list by any means but it highlights a number of services requiring a back-end infrastructure. Now, there are several ways to approach this. You could build out your own server-side infrastructure. However, this is a lot of work to do correctly and adds little to differentiate your application. The back-end, while critical, is largely invisible to end users. Your users are never going to love your app because you did a great job developing the server-side. They will only notice when it doesn’t perform. It is a ton of work to write the code, deploy servers and provide ongoing support. Not to mention all of the time this adds to your development cycle. This can really get expensive. There is a better way. Find a good hosted service and use it!

SQLite.XM comes ready to work with HotRiot.com. To reiterate, HotRiot is a hosted server-side platform for mobile applications. It includes support for all of the bulleted items listed above and more. The HotRiot C# Xamarin API is built into SQLite.XM, so there is nothing you need to do in order to use SQLite.XM with HotRiot. Of course, SQLite.XM doesn’t just work with HotRiot, it is designed to work with any back-end. I show you how to do this in part 3 of the book.

**A server-side database:** We are going to need a server-side database where we can synchronize the local device data. This can be either a traditional relational database or a NoSQL document database. You are probably wondering why I specifically state that the server datastore should be either a relational or a NoSQL document database. The reason is simple. SQLite is a traditional relational database. Synching with another relational database or a NoSQL document database such as MongoDB, will provide the best device-to-server translation. While SQLite.XM will support synching to any back-end, a server-side database whose data model is significantly different from the data model on the device can make synching difficult. It is not unusual to have a schema on the server that is different from the schema on the device, and SQLite.XM fully supports synching to different schemas. However, when the fundamental data models between the device and the server get too far apart, it becomes difficult to perform a rational, workable translation. For example, as a generally rule, it would be less than ideal to try and synch your apps data with a key/value datastore. Of course, depending on the particulars of your app and what you intend to with your data once it is synched, there are may be legitimate reasons for breaking this rule. But it would be unusual.

HotRiot includes support for MySQL and MongoDB.

It would be fair to ask why include two server-side database options when they perform a similar function. The short answer is that each of these two databases have strengths and weaknesses. To only support a relational database or only a NoSQL document database would limit us to trying to fit a solution where it might not be best suited.

**Xamarin** is our cross platform development framework of choice. It allows us to create native Android, iOS, and Windows apps using a mostly shared C# code base. Xamarin lets you to write the vast majority of the non UI application logic using shared code. The platform specific layer is typically much smaller and generally encompasses the user interface code. According to Xamarin, the average application written using Xamarin shares about 65% to 70% of the app code across all three development platforms. This greatly reduces the programming effort needed to support the most popular mobile devices. Given these strengths, Xamarin is a natural choice for creating a cross platform persistence layer.  The other option is to create a separate data layer for each of the platforms we wish to support. That would require coding in Objective-C, Java and C# in order to support iOS, Android and Windows. Using one language to create a single shared persistence layer allows us to focus on the problem we wish to solve, without having to spend too much time on platform related issues.

This is not a book intended to detail Xamarin development. There are other good resources for that. I explain how to use Xamarin to the extent needed to create our data persistence layer. Beyond that, Xamarin is largely ignored. This allows us to stay focused on our data persistence solution. You don’t need to be a Xamarin developer to follow along. We will explain enough Xamarin to get you through.

Do I really need all of this?

The short answer is; probably. If you are developing an OCA, then definitely. For a pure offline application, you may only need local database support, and depending on what you build, you may not even need that. For pure online applications, you will probably need the entire stack except the synchronization logic. However this is all highly dependent on what you’re building.

Understanding Where HotRiot fits in

We are going to be synching local data generated by our application to a central back-end database provided to us through HotRiot. This database could be used for a variety of purposes, but this really needs to be thought of in broader terms. When you synch, whether to HotRiot or some other back-end, you’re not just synching to a database, what you’re really doing is synching with a server-side platform that provides support services to your application.

As stated earlier, HotRiot provides mobile applications with a server-side platform in the cloud. HotRiot includes a set of graphical tools that are used to create an infrastructure for the server side portion of your application, making it a breeze to create tables or collections, design queries, set-up permissions, create triggers, etc.

For the moment, the most interesting aspect of our choice for a back-end server solution is the fact that all HotRiot accounts come with a provisioned SQL (MySQL) and NoSQL (MongoDB) database. This allows you to choose which type of server-side datastore best fits your needs. Another interesting feature of HotRiot is that it can use your own personal MySQL or Mongo database for storing your data; this is instead of using a HotRiot managed database server. More on this later.

Database design considerations

The database on the local device is SQLite. This is a traditional relational database. From a data modeling perspective, the most influential feature of a relational database is their support for joins. This single feature, more than any other, dictates the fundamental structure of the data for a relational database. The device side database should be designed independent from the database used on the back-end server where the local data will be synched. But this presents a potential problem. If we wish to use MongoDB or some other NoSQL database as our back-end datastore, instead of relational database, how do we deal with the fact that most NoSQL databases do not support joins. And, as a result, require a fundamentally different structure from our local database?

Unfortunately, there is no easy answer but that doesn’t mean the problem cannot be managed. One of the factors that works in our favor is that the local datastore for mobile apps tend to be relatively simple when compared to larger enterprise applications. Although this is not always the case this does generally hold true, and can help to make the translation from a relational model to a document model easier.

Let’s take a moment to discuss MongoDB, MySQL, and HotRiot.

When you create your back-end database in HotRiot for the purposes of synching, you are given the option to use either MySQL or MongoDB for the underlying storage engine. MySQL and MongoDB are both very capable databases, each offers features that might make one or the other more appropriate in any particular circumstance. HotRiot allows you to use both Mongo and MySQL simultaneously, although I generally don’t recommend this. While HotRiot has done a lot of work to smooth out the differences between these databases so that you have a very similar user experience, these are, nonetheless, different database technologies. Thus, intermingling them within the same application is generally not recommended.

MySQL and Mongo are fundamentally different, one being a document store and the other using the traditional relational model. Even so, for the vast majority of mobile application, either one is fully capable of meeting design requirements. While there are many subtle and not so subtle differences between MySQL and Mongo, most of them are not significant to the point where they render one or the other unusable for most mobile apps. However, there are few significant differentiators that should carefully be considered when deciding which one to use. I highlight the ones I think are important, this list is surprisingly short.

**Transactions** : If your application requires transactions, then MySQL is realistically your only choice. This is a true requirement less often than you might think. However, for money transfers and some other complex operations, transactions can be indispensable.

**Joins** : If you think your data model can benefit from joins, then MySQL is your better choice. Mongo does not support joins and performing them in your code is not recommended. Do not attempt to do the job of the database, instead, select right database. I know that joins have fallen out of favor lately, especially with the rise in popularity of NoSQL databases. I will tell you without hesitation, I really like the capabilities that joins bring to the table, especially the flexibility in data modeling that joins permit. The problem with joins is in how they are used, not with joins themselves. When used correctly, joins are performant and flexible.

**Scalability** : If you’re expecting to generate huge amounts of data that needs to be part of the apps transactional data set, then Mongo may be your better choice. Mongo is designed from the ground up to support horizontal scaling. If you expect your data set to grow beyond what can be supported by a single database server, then Mongo could have some features that tip in its favor. But this is not the usual case. I know that it is popular these days to talk of supporting “Web scale,” but when looked at objectively, only a very small percentage of apps require anything near this level of scalability. You would be amazed at what a single, powerful database server can handle. For example, I have a good friend that is part owner of one of the more popular dating sites on the net. At any one time, his site can have tens of thousands of users online. Even with a site this large, his database hovers around 80 GB, not including file attachments, which are stored outside the database. Now, he doesn’t allow junk to accumulate in his database, otherwise it would grow to an unmanageable size. So he regularly culls the data in order to keep the working set down. This is smart. There is no point in keeping garbage in your transactional datastore; either delete it or move it to offline storage. His site uses MySQL hosted on AWS.

Here is my advice: Use a relational database such as MySQL unless you have a specific, articulable reason for using Mongo or some other NoSQL solution. For example, if you expect to need horizontal scaling. Traditional relational databases are unmatched in their power and flexibility.

Designing for SQLite

Okay, let us get back to discussing how to design your local database. I will show you how to do a design that can be used for synching to either a traditional SQL database or a NoSQL database.

Any application of significance is going to require a database design that is composed of multiple tables. Remember, were designing for the device, which uses a traditional SQL database. The information in different tables is usually related in some way and needs to be linked in order to effectively process the data produced and consumed by your application. The term relational, the way it is being used here, refers to the fact that the information between tables is connected in some way. The data in one record can be used to find additional related information in other records that exist in other tables. This is usually done using key fields. This allows you to create complex interrelationships between tables that can be used to accommodate a wide variety of requirements.

**Primary keys and foreign keys**

Before we go any further, we need to explain the concept of primary keys and foreign keys. A primary key is a field which uniquely identifies a record in a table. A foreign key is a field which identifies a record in some other table. A foreign key field contains the primary key value of the record it references in the "foreign" table, thus providing a direct link to the record. A table can have multiple foreign keys but only one primary key.

For example, consider the two tables below:

*   Registration Table
*   Job Posting Table

Both the Registration and Job Posting tables contain primary key fields. In this example, the primary keys are named ‘Registration PK’ and ‘Job Posting PK.’ I like to use a naming convention where I append ‘PK’ to a primary key field name. This makes it easy to identify the field. The job posting table also contains a foreign key named ‘Registration FK.’ As with primary key fields, I like to append ‘FK’ to the name of a foreign key field. This field is the key that connects the records in each table. A record in the registration table can be used to find all jobs posted by a company by searching the job posting table on the Registration FK field. Conversely, you can locate the registration profile associated with a job record by searching the registration table on the Registration PK field.

Let's have a look at the internals of what these two tables look like:

![](Image00018.jpg)

As you can see in the tables above, the values in the ‘Registration FK’ column of the job postings database correspond to the ‘Registration PK’ values in the registration table. This primary key / foreign key relationship provides a bi-directional link between the records in the two tables, allowing a lookup of one from the other.

We don't want to get too far ahead of ourselves. The purpose here is to get you to consider ways in which you can structure your tables, and how you can use primary keys and foreign keys to establish relationships.

**Structuring your database**

There is no clear cut correct way to structure a database. However, there are some general guidelines you should consider. Let's take a look at an example database for a simple job search app.

In the illustration below, we have defined six tables that comprise the database for a simple job search application. Notice each table contains a primary key field, which is used to uniquely identify records. In addition, most of the tables also contain foreign keys, which are used to link records between the tables. For example, the Job Postings table contains the foreign key ‘Co Registration FK.’  This can be used to easily locate all jobs posted by a particular company by simply searching the Job Postings table on this field. Alternatively, this can be used to look up the registration details of the company that posted the job by searching the company registration table on the ‘Co Registration PK’ field.

![](Image00021.jpg)

As you can see from this diagram, things can start to get complicated as you create more complex interrelationships. Therefore, you need to take time to properly plan things out. Nonetheless, linking tables through primary key/foreign key relationships allows you to create sophisticated and flexible designs with relative ease.

At this point, do not concern yourself with the mechanics of how you are going to create the tables. Right now, just think about the database structure in a broad sense. On paper, write out the name of each table and the information it will store. Try to follow our example above — identify the tables you will need, and include a couple of the fields they will contain.  Follow the general guidelines below.

*   Each table should only store related information. For example, it would be a mistake to include job posting information in the Company Registration table. It is far better to simply create another table to hold the job posting information and then link the two tables using key fields.

*   Include a primary key field in every table you create, even if you think it will never get used. You should almost never break this rule. It is better to have a primary key and not use it, than to need it and not have it.

*   When records in two tables are related, link them using a primary key / foreign key relationship. This is the foundation upon which relational databases are built.  Sometimes a table is linked to more than one other table, as in the ‘Job Seeker Favorites’ above. As you can see, the records in this table include three foreign keys that link to records in three table, including:

    The Job Seeker Registration Table

    The Company Registration Table

    The Job Postings Table

When you link related tables in this way, you greatly enhance your ability to create searches that can locate related records. For example, the ‘Co Registration FK’ field in the Job Seeker Favorites table can be used to create a search that can locate the registration information of the company that posted the job. Similarly, the 'Job Posting FK' link can be used to create a search that can locate the complete job listing. This is the real power behind using linked key fields.

Let's take a closer look at the three basic principles described above.

**Defining fields**

Once you have identified the tables required by your application, the next step is to decide the specific information each table will store. This should be fairly easy. For example, if your app includes a registration table, you must decide the information you would like to collect as part of the registration process. This can be whatever you want. However, in defining your table fields, consider the three guidelines below:

*   Only include fields you really need. You do not want to carry around useless information in your tables; it only serves to bog things down. Don't worry if you miss some fields in your initial design. You can always go back and add them.

*   Each table should only store related information. We mentioned this earlier, however it is worth reiterating.

*   Registration tables represent a special case — these tables often include an email address field and a password field. Together, these fields represent a user's login credentials. You can use some other combination of fields if appropriate, which, when combined are unique. Normally, applications that have a registration will also include a login; this allows registered users returning to the application to enter. You can set up a registration in any number of ways, but this is one typical way of doing this.

**Including primary keys**

It is almost universally accepted that it is good database design to include a primary key field in all tables, even if you are not sure that you will ever use the key. Experience has shown that primary keys wind up being used extensively in most applications, especially those that include registrations. And creating a primary key is easy! The rule here is: it’s betters to have a primary key and not need it, than need it and not have it.

**Linking tables**

The ability to link related tables is the payoff you get for properly designing your database and including key fields. Let's go back and use the job search example to help us understand how tables are linked. Below is copy of the job search database we presented earlier.

![](Image00021.jpg)

This is a database for an imaginary job search Application. This site allows registered companies to post job listings in the job postings database. Registered job seekers can search the job postings table. When they find a job they are interested in, they can save a record of the job in the job seeker favorites table. This allows them to easily go back and find all jobs in which they were previously interested. Job seekers can also send emails to a company through the company email database. This functionality would have been difficult if not impossible provide if we had not created primary keys and foreign keys that link these related tables.

Let us go step by step and see how we linked these tables. Let's start with the company registration table. This table includes a primary key named 'Co Registration PK,' which is automatically created when a company registers with our application. At some point, a registered company is going to post a job to the 'Job Postings' table. Naturally, we will want to include the primary key value from their registration, as a foreign key, in the job postings record. In keeping with database design principal #2, our job postings table also includes a primary key field named 'Job Postings PK.'

Now let's look at how job seekers interact with our site. Job seekers must register before they can search the job postings table. Naturally, our registration table includes a primary key. This key is stored in the 'JS Registration PK' field. Once job seekers have submitted their registrations, they can start searching the job postings table. One of the features of our application is that we allow job seekers to maintain records of their favorite jobs.

As you can see from the diagram above, the job seeker favorites' table includes three foreign key fields:

*   JS Registration FK
*   Co Registration FK
*   Job Postings FK

These foreign keys reference records in their respective tables, which is what creates the link between records in the ‘Job Seeker Favorites’ table and records in the three foreign tables.

Searching a relational database

We are going to get into this in detail later, but let’s just touch on it. Another benefit you get from a good database design is flexibility in searching. The critical feature of the design in the diagram above is the fact that it contains key fields that link related tables to each other. This greatly enhances your ability to create secondary searches that can locate related records. For example, the ‘Co Registration FK' field in the ‘Job Seeker Favorites’ table can be used to create a search that can locate the registration information of the company that posted the job. Similarly, the ‘Job Posting FK’ key can be used to create a search that can locate the complete job listing from the job posting table. Along with maintainability, this is the real power behind a good design.

Another option, is to use the more advanced technique of searching by using joins. A join can be thought of as a multi-table or multi-database search. It allows you to perform searches that include record data from two or more tables, including tables in different databases. This is covered in more detail later. For more information, see the section ’Performing joins across databases.’

Designing for Mongo synching

Earlier, I said I was going to show you how to design a local database schema for the device which would work well even if you intend to synch with a NoSQL datastore on the back-end. Well, if you look at the database we designed for our example job posting application, what you see is a VERY traditional relational schema. Even our design guidelines are really targeted towards a traditional relational database model. This is all just fine when synching with a relational database but what about when synching to a NoSQL datastore, what gives? It turns out that trying to create a schema that will work for both a traditional relational database and a NoSQL database is a fool’s folly. You will almost certainly end up with a design that works well with neither. The answer to this problem is to create a traditional relational design on the device and create a flattened, denormalized design on the Mongo back-end, performing the required translation in code when synching. However, in order for this to work, the device schema must be done right, especially with respect to creating primary keys and foreign keys. It is these keys that are used to perform the translation from the relational schema to a document schema. We cover this in detail later when we discuss synching.

Suggestions for designing your SQL

I have some thoughts and suggestions I would like to share with you regarding SQL for mobile apps.

Generally speaking, the rules and principals that you follow in order to write good SQL for non-mobile apps also apply to mobile applications. So, there really isn’t a bunch of new stuff that needs to be learned. The major differentiator is the environment and context in which SQLite runs is quite different from a traditional database server. As a result, some well-known and accepted rules are less applicable when using SQLite in a mobile environment. SQLite is a server-less database that runs in the address space of the application, or, at the very least, on the same CPU. Either way, the affect is the same.

There are different schools of thought over whether to use fewer complex queries as opposed to more simple queries in order to accomplish a given task.  I have heard compelling arguments to support both. And to be perfectly candid, I’m not really sure that I have formulated a strong opinion of my own on this. Although, I seem to gravitate towards writing simpler queries. In any case, when writing SQL for SQLite on mobile, I believe that as a general rule, simpler queries are better. Let me explain why.

There are four primary reasons for writing complex SQL, including stored procedures.

*   Stored procedures are often written in order to centralize business logic. Due to their very nature, these queries tend to be complex. While there is nothing that requires a stored procedure to be complex, they nonetheless encourage complexity due to the flexibility they provide.
*   Writing complex SQL, including stored procedures, allows some processing to be offloaded to the database server. Sharing load in this way can provide performance benefits.
*   Fewer complex queries can significantly reduce the number of over-the-wire trips that need to be made to the database. Network traffic is often times more of a performance bottleneck that processing power.
*   A single complex SQL statement is found to be more efficient than multiple simple statements.

None of these, except the last one, apply to SQLite in a mobile environment. There are no stored procedures, no offloading of processing to a separate server, and no over-the-wire network communication between the app and the database. Gains offered by the first three are largely nullified by the context in which SQLite runs.

Simple right? Well, as is usually the case with software engineering, nothing is that simple. While it is true that the first three reasons don’t really apply to SQLite, it is possible that the fourth might be more or less applicable than usual. Simpler queries might be more appropriate for apps that are multithreaded and requires concurrent database access; for more details, see the section ‘Locking and concurrency.’ Also, because there is no over-the-wire traffic generated by SQLite, the normal issues associated with higher velocity database workloads, such as network latency and traffic bottlenecks, don’t exist. If your apps read load is much higher than its write load, you might choose fewer complex queries, even if your database access is highly concurrent. The reason for this is reads execute with the highest level of concurrency in SQLite. I realize that this just muddies the waters, so I am going to give you a concrete recommendation.

If you have the choice to use a single complex query or multiple simple queries, and don’t want to go through the work of performance profiling, go with multiple simple queries.

**Storing dates and times in SQLite**

“SQLite does not have a storage class set aside for storing dates and/or times.“ That sentence was copied directly from the SQLite documentation. In SQLite, dates and times are stored in the following formats.

*   **TEXT** as ISO8601 strings ("YYYY-MM-DD HH:MM:SS.SSS").
*   **INTEGER** as Unix Time, the number of seconds since 1970-01-01 00:00:00 UTC.
*   **REAL** as Julian day numbers, the number of days since noon in Greenwich on November 24, 4714 B.C. according to the proleptic Gregorian calendar.

You can then use the built in SQLite date and time functions to perform conversions. If you don’t need to synchronize the device database to a server-side datastore, then it really doesn’t matter which format you select. Just choose the one you are most comfortable working with in your app. Otherwise, it’s easiest to choose a format that will be readily accepted by the target replication server. For example, SQLite.XM’s default replication synchronizes with HotRiot. HotRiot has a dedicated date and time data type that accepts a date/time in the ISO8601format, so the text format would work just fine. This also has the advantage of storing the date/time on the server using an actual date/time field. HotRiot also includes both integer and real number data types, so using an integer or real for date/time would also be okay. Of course, you would need to perform a conversion in order to print the output in a human readable form.

What if you want to use one format for storing dates/times on the device database and a different format for storing them on the server? This is not a problem, but it requires extra work on your part. Synchronization includes the ability for you modify record data before sending it up to the server. You could use this capability to convert from one format to another. This feature is known as pre-synchronization processing and is covered in detail in the section ‘Customizing synchronization’.

Getting SQLite.XM

SQLite.XM is available on GitHub, here is a direct link: [https://github.com/HotRiot/SQLite.XM-Xamarin](https://github.com/HotRiot/SQLite.XM-Xamarin) . Just include the SQLite.XM project into your solution. If you’re not sure how this is done, I go through an example in the next section.

For creating iOS based applications, SQLite.XM requires Xamarin iOS 5.2 or later and an iOS version that supports multithreading. It is very unlikely that you wouldn’t meet these minimum requirements. You would have to indeed be working with an old version of Xamarin and testing with a very outdated version of iOS.

Creating an application skeleton

In this section I’ll explain how to create an application skeleton that includes SQLite.XM. If your comfortable doing this on your own, just skip ahead to the next section. The examples in the book do not depend on your having a project that exactly matches the one I create here. Just as long as you have some project with SQLite.XM, you’ll be fine.

I decided to use Xamarin Studio as it provides a fairly consistent and uniform interface between Windows and OSX. If you haven’t already done so, go to the following URI to install Xamarin: [http://xamarin.com/download](http://xamarin.com/download) .

![](Image00015.jpg)

Once installed, start Xamarin Studio and select *New Solution* on the opening screen, or select *File->New->Solution* . This will open the *New Solutions* dialog, see the screenshot below. We’re going to start by creating a basic Android application, that is, an Android project with a single activity.

In the *New Solutions* dialog, select *Android* then *Android Application* . I named the project JSearch, short for Job Search.

![](Image00035.jpg)

Once created, our solution should show up in Xamarin Studio similar to the screenshot below.

![](Image00007.jpg)

Now, we are going to add SQLite.XM to our newly created solution. SQLite.XM is a shared project that can be used by all platforms targeted by Xamarin, including iOS, Android, and Windows. Right click on the JSearch solution and navigate to the *Add->Add Existing Project* , see the screenshot below.

![](Image00013.jpg)

This will bring up the open project dialog, see the next screenshot. Navigate to the folder where you placed the SQLite.XM project that you downloaded from GitHub and add it to the solution.

![](Image00009.jpg)

Next, we need to add several references which are required by SQLite.XM. Right click on the *References* folder listed under your project heading. This will display the references menu, see the screenshot below. Select the *Edit References* menu item.

![](Image00025.jpg)

The *Edit Referenced* dialog will display, see the next screenshot. Begin by selecting the *Packages* tab, then add the following four packages.

*   Mono.Data.Sqlite
*   System.Data
*   System.Web.Services
*   System.Xml.Linq

![](Image00008.jpg)

Next, select the *Projects* tab of the edit *References* dialog, then select the SQLite.XM project. See the screenshot below. Select the *OK* button to add the references.

![](Image00023.jpg)

Next, select *Project->Add NuGet* Package.

![](Image00039.jpg)

This will open the *Add Packages* dialog; see the next screenshot.

![](Image00000.jpg)

Add the package Json.NET to your project. At this point, we have fully created our project skeleton and we’re ready to get started!

Platform specific code

SQLite.XM was designed to be a cross-platform solution for your iOS and Android applications. There is almost no platform specific code. At worst, you will need to add one additional line of code to the Android SQLite.XM initialization sequence that is not needed in iOS. I will show you this latter. That’s all the platform specific code you will need to deal with, everything else in SQLite.XM is consistent between Android and iOS.

Internally however, SQLite.XM has some platform specific code. Two files in SQLite.XM include conditional compilation directives used for selecting the correct code depending on the target platform for which you are compiling. At the top of the following two files are two *#ifdef* statements, one for Android and one for iOS.

*   *HotRiot->HotRiot_CS.cs*
*   *Synchronize.cs*

Uncomment the statement that references the platform for which you are compiling. A screenshot showing the top of the *Synchronize.cs* file is shown below, it has the Android directive uncommented.

![](Image00003.jpg)

Part 2\. Data storage on the device

Describing your apps databases

The first step to building a data persistence layer is to create a descriptor for each database used by your application. Descriptors provide basic information about the databases your app will be using. Below is a partial listing of the database descriptor class.

`public`  `class`  `DatabaseDescriptor`

`{   `

 `private`  `string` ` databaseName;`

 `private`  `Environment` `.` `SpecialFolder` ` databaseFolder;`

 `public`  `Environment` `.` `SpecialFolder` ` DatabaseFolder`

`    {`

 `get` ` { ` `return` ` databaseFolder; }`

`    }`

 `public`  `bool` ` noLog =` `false` `;`

 `public`  `string` ` logfileName;`

 `public`  `int` ` logfileMaxSize = ` `1024` ` * ` `1024` `;`

 `public`  `Environment` `.` `SpecialFolder` ` logfileFolder =`

 `Environment` `.` `SpecialFolder` `.Personal; `

`    +` `public`  `DatabaseDescriptor` `(` `string` ` databaseName,`

 `Environment` `.` `SpecialFolder` ` databaseFolder =` `Environment` `.` `SpecialFolder` `.ApplicationData)…`

`    +` `public`  `static`  `DatabaseDescriptor` ` getDescriptor(` `string` ` databaseName)…`

 `+` `public`  `static`  `ArrayList` ` getDatabaseNames()…`

`}`

The `DatabaseDescriptor` constructor takes a single required parameter; the name of the database you wish to create/connect. It also accepts an optional folder location for the database. By default, databases are located in the *ApplicationData* folder. This path is the value of the environment variable `XDG_CONFIG_HOME` , if it is set, otherwise, it is in the ‘.config’ directory of the current user's home directory, which, in Android, translates to the following location:

 `/data/data/<application name>/files/.config`

and in iOS:

 `<application base>/documents/`

DO NOT name your database ‘main’ or ‘temp’, these names are used by SQLite internally and using them may cause problems.

The `DatabaseDescriptor` class has reasonable defaults for its control parameters. Of course, if you don’t like any of the default values, you can change them. In the example below, the location where the database will be created is set to the *Personal* folder.

`try`

`{`

 `new`  `DatabaseDescriptor` `(` `"jSearch",` `Environment` `.` `SpecialFolder` `.Personal); `

`}`

`catch` `( System.` `Exception` ` ex)`

`{`

 `string` ` message = ex.Message;`

`}`

Once created, the database name and folder location in the descriptor cannot be changed. This is reasonable; it’s hard to imagine a circumstance where this would make sense. Anyway, changing either of these effectively changes the database being referenced by the descriptor. Each database descriptor also includes properties for a log file. What this means is, each database can, and should, have its own separate log. This may seem like overkill; why not simply share a log file between all databases. The reason is twofold; this provides flexibility in managing logs and visually parsing a single file shared between databases is more difficult than having separate database logs.

The log file is automatically assigned the same name as the database with the extension ‘.log’ and its default size is 1MB. By default, log files are placed in the `Personal` folder. This is the personal or home directory for the current user, which, in Android, translates to the following location:

 `/data/data/<application name>/files`

Of course, you can change any of these defaults. In the example below, we change the maximum log file size from its default 1MB to 5MB and the log file name to `jSearch-log` .

`try`

`{`

 `DatabaseDescriptor` ` dd = ` `new`  `DatabaseDescriptor` `(` `"jSearch"` `);`

`    dd.logfileMaxSize` `= 1024 * 1024 * 5;`

`    dd.` `logfileName =` `"jSearch-log"` `;`

`}`

`catch` `( System.` `Exception` ` ex)`

`{`

 `string` ` message = ex.Message;`

`}`

When a log file reaches its maximum size, it is renamed from `<` *`logfile name`* `>.log` to `<` *`logfile name`* `>.old.log` and a new log file is started. If there was an existing old log file, it is replaced. If you don’t want logging, set `noLog` to `false` .

Database descriptors are used by the persistence layer as needed; this is all automatic and under the covers. As part of your apps initialization, you must create a descriptor for each database. Only create one per database. SQLite.XM will quietly ignore attempts to initialize a descriptor for the same database more than once. You do not need to keep the instances of the descriptor objects that you create since the persistence layer automatically manages descriptors. Once created, descriptors can safely be forgotten about. However, if you need to get a descriptor, use the static method:

`public`  `static`  `DatabaseDescriptor` ` getDescriptor(` `string` ` databaseName)`

This method will return the descriptor for the named database, or null of the descriptor could not be found.

In the example below, we create three database descriptors. The first two use the defaults for all of the control parameters. In the third descriptor, logging is turned off.

`try`

`{`

 `new`  `DatabaseDescriptor` `(` `"user"` `);`

 `new`  `DatabaseDescriptor` `(` `"records"` `);`

 `DatabaseDescriptor` ` dd = ` `new`  `DatabaseDescriptor` `(` `"report"` `);`

`    dd.noLog =` `true` `;`

`}`

`catch` `( System.` `Exception` ` ex)`

`{`

 `string` ` message = ex.Message;`

`}`

While you can create as many databases as your app requires, as a practical matter, the vast majority of mobile applications really only need a single database. This is the simplest approach and works well in most cases. I would recommend this as the default unless you have a compelling reason to do otherwise. Multiple databases can add complexity. For example, joins across databases require that the joined databases be attached using the `attachDatabase` method; explained in detail later. This introduces potential concurrency issues, such as when trying to attach a currently locked database. There is also additional system overhead when working with multiple databases. While this generally not a serious concern, mobile devices are limited in resources and efficiency should always be considered in your design. That being said, there are times when multiple databases are the right choice.

Schema initialization

Once the database descriptors have been initialized, the next step is to create the tables and indexes required by your schema.

One feature not present in SQLite, is stored procedures, so writing common callable SQL that is stored in the database is not an option. Which is well enough, it doesn’t really seem to make much sense to support stored procedures in a server-less, embedded database like SQLite. So, we have to decide where to put our SQL statements. We have a few choices:

*   Put the SQL statements in the database.
*   Imbed the SQL statements in the code.
*   Place the SQL statements in a properties file.

When not using stored procedures, I generally prefer putting SQL statements in a centralized datastore, usually the database. It organizes the SQL in one location and makes it easy to find, read and modify independent of the code base. I prefer this solution when building applications that use a traditional database server, such as MySQL or SQL Server.  In these cases, the database is almost always running on a server managed by a DBA. But for SQLite, this doesn’t seem to make much sense given how it would need to be implemented.

We could place the SQL directly in the code, in a single class. This is probably is the most efficient solution but it requires users to make code modifications. We definitely want to keep that to a minimum, even if only entering SQL text. The other possibility is to embed the SQL statements directly in the SQLite.XM database calls. I really don’t like peppering SQL throughout the code base. It is just a mess. It makes it more difficult to locate your SQL, which can cause other problems; for example, missing indexing opportunities or increasing the likelihood that you will duplicate code.

The best solution is to place our SQL statements in a properties file. This allows us to keep our SQL in a central location that makes it easy to read and modify without messing with the code. This is not the most efficient solution, as it requires the SQL statements properties file to be read and processed when initializing the app. But that really shouldn’t cause a significant delay and the tradeoff seems worth it. This solution is implemented slightly different on Android and iOS. So we need to deal with some application specific issues. As with most engineering design decisions, selecting one solution over another is really a balancing of tradeoffs.

Including a SQL statements properties file in Android

All Android applications include an *Assets* folder. This is the location where you place arbitrary files that need to be processed by your app as raw data, for example, the SQL statements properties file. You can find this folder in your project, it is created automatically by Xamarin. Create an empty file and place it in this folder.

![](Image00027.jpg)

You can name the file whatever you like, for the examples in this book, we call it *SqlStatements.txt* . This will be our SQL statements properties file. This is all that’s needed in order to include a statements file in an Android project. Later on, I’ll show you how to access the file.

Including a SQL statements properties file in iOS

Xamarin based iOS application include a *Resources* folder. This is the location where you place arbitrary files that need to be processed by your app, for example, the SQL statements properties file. You can find this folder in your project, it is created automatically by Xamarin. Create an empty file and place it in this folder. If you like, you can place it within a subfolder of the *Resources* folder. This can help to organize things even further.

![](Image00019.jpg)

You can name the file whatever you like. In the screenshot above and for the iOS examples later in the book, we call it *SqlStatements.txt* and we placed in in the subfolder *sqlProperties.* This will be our SQL statements properties file. This is all that’s needed in order to include a statements file in an iOS project. Later on, I’ll show you how to access the file.

As a side note, iOS requires that application resource files be placed in the application's root directory. Unfortunately, this can get a bit messy. To clean things up, Xamarin has this notion of a *BundledResource* build action, which lets you put files in the *Resources* directory instead of in the root. The contents of the *Resources* directory gets mapped to the root of the application during the build process. This is done automatically by Xamarin. I find this to be a really nice feature that helps to organize your project a bit better.

Parameterized queries

Before explaining the structural details of the SQL statements properties file, we need to understand how queries should be written for SQLite.XM. All queries that require user supplied data must be written as a parameterized query. Parameterized queries are also known as prepared statements. A parameterized query is a query that is written where place holders are put in the query where user supplied data would normally appear; see the example below.

`INSERT INTO companyReg (companyRegPK, coName, hrContact, email, password) VALUES(?, ?, ?, ?, ?)`

This query uses question marks at the location in the query where the record data would normally go. We do it this way for a number of reasons. First, parameterized queries are much easier to work with in code. Manually assembling a query that contains the actual record data is quite a bit more work than using the parameterized form. Parameterized queries are virtually immune to SQL injection attacks. SQL injection is a type of malicious hack that can be used to access or destroy your database. Finally, parameterized queries can me more performant. The way parameterized queries are implemented, the database can skip several complex preparatory steps when the same statement is used more than once. This can amount to a significant time savings for certain queries that are used repeatedly.

Let’s get a better understanding of the performance benefits offered by parameterized statements. Prepared statements provide the best performance gains when being used to execute a large number of identical queries (the user supplied data can vary). The performance gains will be particularly significant when executing complex queries. If a statement is relatively simple, the performance advantage of a prepared statement will be less noticeable.

Parameterized statements only last for the life of a connection. When a connection ends, all associated prepared statements are also terminated, so they must be recreated for any new connections. This also means that a prepared statement cannot be used by multiple connections; however, each connection can create their own prepared statements.

Understanding the SQL statements properties file

Let’s start by having a look at the structure of the SQL statements properties file.

![](Image00004.jpg)

The SQL statements properties file is divided into seven sections:

*   `TABLE`
*   `INDEX`
*   `INSERT`
*   `SELECT`
*   `UPDATE`
*   `ALTER`
*   `DELETE`

Each section starts with a header name that is placed between opening and closing brackets and ends with an empty set of brackets. These are the opening and closing markers for a section. The sections can be in any order, however, they all must be present in the file, even sections that are empty. Anything that is not between opening and closing brackets is considered a comment and is ignored by SQLite.XM. Do not use the brackets symbol in any of your comments; these are used exclusively as a delimiter. The SQL statements for each section are placed between the opening and closing section markers. Each section should only include statements relevant to the section.

The `TABLE` section should only include create/drop table SQL statements.

The `INDEX` section should only include create/drop index SQL statements.

The `INSERT` section should only include record insert SQL statements.

The `SELECT` section should only include select SQL statements.

The `UPDATE` section should only include update SQL statements.

The `ALTER` section should only include alter table statements

The `DELETE` sections should only include record delete SQL statements.

Let’s take a closer look at each section of the SQL statements properties file.

**Defining table statements**

The `TABLE` section of the SQL statements file should only include create table or drop table statements. Putting any other data definition or data manipulation statements in this section will result in a runtime error. Each create table statement is composed of three fields.

`[` *`database_name`* ***`.`*** *`table_name`* `] [` *`create/drop table statement`* `] [` *`synch_key`* `]`

Each field is placed inside opening and closing brackets. The fields must appear in the order shown above. However, you can format them on separate lines or include white spaces in order to enhance readability. The first field is the fully qualified name of the table being created, that is, the database name followed by a period followed by the table name. The second field is the actual create table SQL statement. The last field is the synchronization key. This tells SQLite.XM how to synchronize the table data. There are currently three options.

*   **no_synch** : Do not synchronize the table data.
*   **synch** : Synchronize the table data with the server.
*   **copy** : Copy the table data to the server. However, do not execute record deletes on the server.

This field is not case sensitive. Below is an example `TABLE` section with two create table statements and a comment.

**`[TABLE]`**

**`Create the database tables “People” and “Places”.`**

`[jSearch.People] [CREATE TABLE People (id INTEGER PRIMARY KEY AUTOINCREMENT, FName TEXT, LName TEXT)] [synch]`

`[jSearch.Places] [CREATE TABLE Places (id INTEGER PRIMARY KEY AUTOINCREMENT, loc TEXT, reason TEXT)] [synch]`

**`[]`**

SQLite.XM adds a text field to every table that’s used for coordinating synching. The field name is `systemSynchID` . This field is completely managed by the SQLite.XM code, so it can safely be ignored. That being said, this is a reserved name so you cannot use this field name in any of your tables.

**Defining insert statements**

The `INSERT` section of the SQL statements file should only include record insert statements. Each insert statement is composed of three fields.

`[` *`statement name`* `] [` *`table name`* `] [` *`insert record statement`* `]`

Each field is placed inside opening and closing brackets. The fields must appear in the order shown above. However, you can format them on separate lines or include white spaces in order to enhance readability. The first field is the name of the insert statement. This can be any name of your choosing, however, it must be unique from all other insert statement names. We suggest you choose a name that is short but descriptive. The second field is the name of the insert table. The last field is the actual SQL insert statement.

Below is an example `INSERT` section with two insert statements.

**`[INSERT]`**

`[registerCompany]`

`[companyReg] `

`[INSERT INTO companyReg (companyRegPK, coName, hrContact, email, password) VALUES(?, ?, ?, ?, ?)]`

`[insertJobPosting] `

`[jobPosting] `

`[INSERT INTO jobPosting (jobPostingPK, companyRegFK, jobTitle, description, pay) VALUES(?, ?, ?, ?, ?)]`

**`[]`**

Earlier, I mentioned that SQLite.XM adds a field named `systemSynchID` to every table and that this field can safely be ignored as it is managed by the system automatically. All that is true, however, there is one side effect caused by this that must be taken into consideration when writing INSERT statements.

There are two basic forms for the INSERT INTO statement:

*   `INSERT INTO table_name (column1, column2, column3, ...columnN) VALUES (?, ?, ?, ...?)`
*   `INSERT INTO table_name VALUES (?, ?, ?, ...?)`

In the first form, the column names and the corresponding values being inserted are explicitly delineated. For example, column1 will get the value from parameter 1, column2 will get value from parameter 2, and so forth. In the second form, the columns being inserted are implied by the SQL statement. For example, the first column in the table will get value from parameter 1, the second column in the table will get value from parameter 2, and so forth.

When writing your INSERT statements, you must use the first form. The reason for this is when a table is first created, the `systemSynchID` field is known to be the last column in the table, as in the sample registration table below.

![](Image00020.jpg)

However, if you alter a table by adding fields, the new fields will now come after the `systemSynchID` field.

![](Image00005.jpg)

In this case, trying to perform updates using the implicit insert syntax may have problems. This is due to the fact that the `systemSynchID` field will now be located somewhere in the middle of the table.

**Defining alter table statements**

The `ALTER` section of the SQL statements file should only include alter table statements. The alter table statement in SQLite supports a limited subset of commands. You can rename a table or you can add a new column to an existing table. DO NOT rename tables. The reason for this is when a table is created, SQLite.XM creates corresponding triggers needed for synchronization. When a table is renamed, the triggers do not automatically update.  This will render the triggers inoperative and synchronization will start to fail. A future version of SQLite.XM may support table renames by automatically dropping and recreating triggers, but for now, do not rename tables.

Each alter table statement is composed of three fields.

`[` *`database_name`* ***`.`*** *`table_name`* `] [` *`column name`* `] [` *`alter table statement`* `]`

Each field is placed inside opening and closing brackets. The fields must appear in the order shown above. However, you can format them on separate lines or include white spaces in order to enhance readability. The first field is the fully qualified name of the table being altered, that is, the database name followed by a period followed by the table name. The second field is the name of the column being added to the table. The last field is the actual SQL alter table statement.

Below is an example `ALTER` section with one alter statement.

**`[ALTER]`**

`[jsearch.companyReg] [president] [ALTER TABLE companyReg ADD president TEXT]`

**`[]`**

**Defining index statements**

Unlike some other databases, index definitions are not part of the SQLite create table syntax. Therefore, indexes need to be created independently. This is not problem and in no way puts SQLite at a disadvantage, it’s just how they do things. The `INDEX` section of the SQL statements file should only include CREATE INDEX or DROP INDXED statements. Each index statement is composed of three fields.

`[` *`database_name`* ***`.`*** *`table_name`* `] [` *`index name`* `] [` *`index statement`* `]`

Each field is placed inside opening and closing brackets. The fields must appear in the order shown above. However, you can format them on separate lines or include white spaces in order to enhance readability. The first field is the fully qualified name of the table being indexed, that is, the database name followed by a period followed by the table name.  The second field is the name of the index that is being created or dropped. The last field is the actual SQL index statement.

Below is an example `INDEX` section with two index statements.

**`[INDEX]`**

`[jsearch.companyReg] [coNameIDX] [DROP INDEX coNameIDX]`

`[jsearch.companyReg] [newCoNameIDX] [CREATE INDEX newCoNameIDX ON companyReg (hrContact, coName)]`

**`[]`**

Drop index and create index statements can appear in any order, intermingling them is okay. Having more than one drop or one create for the same index will cause an error. However, you can have one create and one drop statement for the same index.

**Defining select, update, and delete statements**

The `SELECT` , `UPDATE` and `DELETE` sections of the SQL statements file should only include their respective select, update, or delete SQL statements. Each of these statements is composed of two fields.

`[` *`statement name`* `] [` *`SQL statement`* `]`

Each field is placed inside opening and closing brackets. The fields must appear in the order shown above. However, you can format them on separate lines or include white spaces in order to enhance readability. The first field is the name of the statement. This can be any name of your choosing, however, it must be unique from all other statement names in the same section. We suggest you choose a name that is short but descriptive. The second field is the actual SQL statement.

Below are several example statements.

**`[SELECT]`**

`[findCompany] [SELECT * FROM companyReg WHERE coName = ?]`

**`[]`**

**`[UPDATE]`**

`[updateCompanyReg] [UPDATE companyReg SET hrContact = ? WHERE coName = ?]`

**`[]`**

**`[DELETE]`**

`[deleteCompany] [DELETE companyReg WHERE coName = ?]`

**`[]`**

Creating tables

Now that we understand the structure of the SQL statement properties file and how to include it in a project, the next step is to populate the `TABLE` section. Below is the table portion of our example job search site.

**`[TABLE]`**

**`Create the company registration table.`**

`[jsearch.companyReg] `

`[CREATE TABLE companyReg (id INTEGER PRIMARY KEY AUTOINCREMENT, `

`companyRegPK TEXT, coName TEXT, hrContact TEXT, email TEXT, password TEXT)] `

`[synch]`

**`Create the job postings table.`**

`[jsearch.jobPosting] `

`[CREATE TABLE jobPosting (id INTEGER PRIMARY KEY AUTOINCREMENT,`

`jobPostingPK TEXT, companyRegFK TEXT, jobTitle TEXT, description TEXT, pay INTEGER)]`

`[synch]`

**`Create the company email table.`**

`[jsearch.companyEmail] `

`[CREATE TABLE companyEmail (id INTEGER PRIMARY KEY AUTOINCREMENT,`

`companyEmailPK TEXT, jobPostingFK TEXT, companyRegFK TEXT, subject TEXT, body INTEGER)]`

`[synch]`

**`Create the job seeker registration table.`**

`[jsearch.seekerReg] `

`[CREATE TABLE seekerReg (id INTEGER PRIMARY KEY AUTOINCREMENT,`

`seekerRegPK TEXT, fName TEXT, lName TEXT, email TEXT, password INTEGER)]`

`[synch]`

**`Create the job seeker favorites table.`**

`[jsearch.seekerFavorites] `

`[CREATE TABLE seekerFavorites (id INTEGER PRIMARY KEY AUTOINCREMENT,`

`seekerFavoritesPK TEXT, seekerRegFK TEXT, companyRegFK TEXT, jobPostingFK TEXT, password INTEGER)]`

`[synch]`

**`Create the job seeker email table.`**

`[jsearch.seekerEmail] `

`[CREATE TABLE seekerEmail (id INTEGER PRIMARY KEY AUTOINCREMENT,`

`seekerEmailPK TEXT, seekerRegFK TEXT, companyRegFK TEXT, subject TEXT, body INTEGER)]`

`[synch]`

**`[]`**

There are a few things worth noting in the example above. First, the use of comments. Anything not between brackets is considered a comment. I recommend you include a many comments as necessary in order to clarify what you are doing. Also, notice how the statements are formatted for readability. Finally, you will notice that every table includes an *id* field, which is defined as follows:

*   `id INTEGER PRIMARY KEY AUTOINCREMENT`

Every table you create must include this field. Other than these basic formatting options and this one structural requirement, you are free to create your tables however you like. In the example above, I have made extensive use of primary keys and foreign keys. I suggest you do the same.

If you look closely at the primary key fields and foreign key fields you will notice they are all defined as type text. While this is not unheard of, it is a bit unusual. Key fields are normally defined as a number, or, more specifically, as a 64 bit long. However, when you define your tables, all key fields must also be created as text fields, similar to the way I have done in the example above.

Why is this so?

The answer is simple. As I stated above, key fields are typically defined as 64 bit auto increment values. However, this poses a problem when synchronizing data from multiple devices with each running an independent database instance. In this case, you are sure to have duplicate key values generated on the different devices. When you then try an synchronize, you will encounter either duplicate key errors or simply create other problems due to the fact that you have duplicate keys, which, by definition, are expected to be unique. The graphic below depicts this condition. We see that records from two different devices with the same record ID (27) are being synchronized to the server database. This, of course, is unacceptable. Fortunately, the solution to this problem is fairly simple.

![](Image00036.jpg)

Instead of creating a key field as a traditional auto increment value, you define it as a text field. You then populate the field with a Globally Unique Identifier (GUID) sometimes referred to as a Universally Unique Identifier (UUID). Put simply, a GUID can be thought of as a random number that is virtually guaranteed to be unique from all other GUIDs. It would be fair to ask how we can be so sure that we won’t have the same duplicate key problem with GUIDs that we would have with auto increment keys. I won’t go into details, but given how GUIDs are generated and their enormous size (typically 128 bits), it is generally accepted that it’s safe to rely on them being unique. Later, I will show you how to generate a GUID.

SQLite naming constraints

In SQLite, table names, index names, column names, or any other named object should only include alphanumeric characters, including underscores, and must not start with a digit. Avoid all other special characters, including spaces. This is the safest way to go. That being said, SQLite will allow special characters in a named object provided it is quoted using one of the mechanisms below.

1.  Use double quotes, as in the following: **"keyword"**
2.  Use brackets, as in the following: **[keyword]**
3.  Use grave accents (ASCII code 96), as in the following: **`keyword`**

Another rule you might choose to follow when selecting names, is to avoid English words. The reason for this is to avoid any conflicts with SQL keywords.

Initializing the database

We now have everything in place to successfully initialize our database. So let us take a look at an example that puts all of the pieces together. Below is a code snippet for an Android main activity class. In the example below, it is assumed that you have already created a SQL statements properties file by the name *SqlStatements.txt* and have populated it with create table statements, and, optionally, any required index statements.

`public`  `class`  `MainActivity` ` : ` `Activity`

`{`

 `protected`  `override`  `void` ` OnCreate (` `Bundle` ` bundle)`

`    {`

 `base` `.OnCreate (bundle);`

`      SetContentView (` `Resource` `.` `Layout` `.Main);`

 `try` `{`

**`1`**   `new`  `DatabaseDescriptor` `(` `"jsearch"` `);`

  *`// Read the SQL statements properties file that we placed in the Assets folder.`*

**`2`**  `using` ` (` `StreamReader` ` sr = ` `new`  `StreamReader` ` (Assets.Open (` `"SqlStatements.txt"` `))){`

**`3`**   `ProcessSQLStatements` `.Parse (sr);`

 `}`

**`4`**   `SxmInit.` `initialize();`

**`5`**   `using` ` (` `SxmTransaction` ` sxmTrans = ` `new`  `SxmTransaction` `(` `"jsearch"` `))`

 `{`

 `}`

`      }`

 `catch` `( System.` `Exception` ` ex){`

  `string` ` message = ex.Message;`

 `}`

 `}`

`}`

The first step in initializing the database is to create a database descriptor for each database needed by your app, see line 1\. Our example app only requires one database, this is typical for mobile applications. Once this is done, the next step is to process the SQL statements properties file. Have a look at lines 2 and 3\. Line 2 creates a new stream reader for the file. The file stream is then processed on line 3. Once these two steps are complete, it’s time to actually perform the initialization. This is done on line 4\. Line 5 creates a transaction for the newly initialized database. This step is not actually part of the initialization process and is only shown here for illustration. I explain transactions in detail in a later section. It doesn’t really matter when you actually initialize the database. In our example, we are doing it in the main activity. The only rule is that you must initialize the database before trying to establish a connection or create a transaction object. This seems obvious enough.

Below is an example of how this initialization might be done for iOS.

 `public`  `class`  `Application` ` {`

  *`// This is the main entry point of the application.`*

 `static`  `void` ` Main (` `string` `[] args)`

`    {`

 `Thread` ` synchThread = ` `new`  `Thread` `(` `new`  `ThreadStart` `(initDB));`

`      synchThread.Start ();`

 *`// If you want to use a different Application Delegate `*

 *`// class from "AppDelegate" you can specify it here.`*

 `UIApplication` `.Main (args, ` `null` `, ` `"AppDelegate"` `);`

`    }`

 `private`  `static`  `void` ` initDB ()`

`    {`

 `new`  `DatabaseDescriptor` ` (` `"jsearch"` `, System.` `Environment` `.` `SpecialFolder` `.Personal);`

 *`// Read the SQL statements properties file that we placed in the Resources folder.`*

 `using` ` (` `StreamReader` ` sr = ` `new`  `StreamReader` ` (` `"sqlProperties/SqlStatements.txt"` `)){`

 `ProcessSQLStatements` `.Parse (sr);`

`      }`

 `SxmInit` `.initialize (` `)` `;`

`    }`

 `}` 

As you can see, the Android initialization and the iOS initialization are virtually identical. The main difference is we performed the iOS initialization on a separate thread. Strictly speaking, this is probably not necessary and you could always do it this way for Android also. The other, minor difference, is the way we pass the path for the SQL statements properties file to the *`StreamReader`* . This is done differently to account for the fact that in Android the SQL statements properties file is placed in the *Assets* folder and in iOS it is placed in the *Resources* folder.

Now, you might look at the initialization sequence and think that it is rather inefficient to do this for each startup cycle. However, looking closely at the code, you see that it’s really quite efficient. Parsing the SQL statements properties file is pretty light weight, and besides, even a file with a lot of statements is not going to be very large, possibly 100 kB. The create schema code is also very efficient. For each database used by your app, typically one, a single query is made to get the names of the existing tables. The create table statements are compared to this list and those already existing in the database are skipped. The alter table statements are only executed against tables that already exist in the database. This allows you to make schema changes to tables without having to execute both create and alter SQL commands. Index and alter table statements are only executed after their corresponding index or table field is first checked to verify that the statement needs to run. More about this later.

One more important point. It is perfectly safe to execute the initialization sequence multiple times for each run of an application, the sequence is idempotent. This might, under certain circumstances, ease dealing with application state transitions. For example, the code below would work just fine.

 `for` `(` `int` ` i=` `0` `; i<` `4` `; i++)`

`  {`

 `new`  `DatabaseDescriptor` `(` `"jsearch"` `);`

 `using` ` (` `StreamReader` ` sr = ` `new`  `StreamReader` ` (Assets.Open (` `"SqlStatements.txt"` `))){`

 `ProcessSQLStatements` `.Parse (sr);`

`    }`

 `SxmInit.` `initialize();`

`  }`

While this is not something that you would necessarily want to do, no harm will come if you do.

Using the SxmTransaction class

Once the database has been fully initialized, it is ready to be used. The `SxmTransaction` class is the easiest and most direct way to interact with your database. It dynamically creates connections to the database and manages all associated resources automatically. For most applications, this is the best way to work with the database; you just instantiate an instance of the class inside a `using` statement and use it. All of the resource cleanup is taken care of automatically.  Your other option is to manually create your database connections, reusing them as needed. I explain this in a later section. For more information, see the section ‘The `SxmConnection` class.’

Although the `SxmTransaction` class is a bit less efficient than managing connections manually, for many apps, the performance difference is not significant enough to warrant the extra effort of dealing with connections directly. Other than the cost of establishing new connections, the main performance disadvantage of the `SxmTransaction` class is that prepared statements are lost when the transaction object is destroyed. With that said, I would like to point out that these are not really as costly as you might think.

When interacting with a traditional database server, developers usually make an effort to minimize connection workload. This makes sense, since connecting to a database typically requires a remote network connection to a database server. This is costly and should be kept to a minimum. Connection reuse through pooling is the strategy most used to do this. But requirements are different for mobile apps. The cost of establishing a new connection to a local SQLite database is very low. There is no over-the-wire network involved. Mobile environments have limited resources, so managing a pool of open connections is probably worse than just creating and tearing down connections as needed. Also, while SQLite does have good concurrency, it is not up to the level of a full-fledged database server. Fewer active connections minimizes the potential for conflicts due to locking.

Prepared statements offer their greatest benefit when executing complex queries repetitively. This condition is the exception rather than the rule for mobile applications. For most mobile apps, queries tend to be simple and are generally not executed so often that the cost savings of prepared statements is so significant.  It is important to understand that the advantage of prepared statements are not entirely lost when using the `SxmTransaction` class. The `SxmTransaction` class does create and use prepared statements for the life of a transaction, which can span many statement executions. However, all prepared statement that are created are lost when a transaction is completed, therefore they cannot be carried over and reused by another transaction object.

Inserting records into the database

Let’s start with a simple example that posts a record to a database. Below is a screenshot of the company registration page of our job search application. This is a very basic input form used to register a company with our app. When the submit button is selected, the registration is processed.

![](Image00006.jpg)

Below is the company registration activity class for our registration form. It’s pretty simple, it submits a registration record to the database. We are most interested in the `processSubmitHandler` method. This method is called when the submit registration button is selected, it is responsible for inserting the registration record. Before we pick this method apart, let’s have a look at the insert statement in the SQL statements properties file that is used to actually save the registration record.

`[registerCompany]`

`[companyReg]`

`[INSERT INTO companyReg (companyRegPK, coName, hrContact, email, password) VALUES(?, ?, ?, ?, ?)]`

The first field in the definition is the name of the statement; `registerCompany` . The second field is the name of the table being inserted by the insert statement; `companyReg` . And lastly, we have the actual insert statement itself. This is the SQL statement that is used to actually save the registration. As you can see, it is a simple parameterized insert statement. Okay, back to the code below.

`  [` `Activity` ` (Label = ` `"CoRegistrationActivity"` `)]            `

 `public`  `class`  `CoRegistrationActivity` ` : ` `Activity`

`  {`

 `protected`  `override`  `void` ` OnCreate (` `Bundle` ` bundle)`

`    {`

 `base` `.OnCreate (bundle);`

`      SetContentView (` `Resource` `.` `Layout` `.CoRegistration);`

 `Button` ` submitCoRegButton = FindViewById<` `Button` `> (` `Resource` `.` `Id` `.submitCoRegButton);`

`      submitCoRegButton.Click += ` `delegate` ` { processSubmitHandler(); };`

`    }`

 `private`  `void` ` processSubmitHandler()`

`    {`

 `ArrayList` ` parameterValues = ` `new`  `ArrayList` ` ();`

**`1`**  `string` ` registrationPK = ` `Guid` `.NewGuid ().ToString ();`

**`2`** `     parameterValues.Add (registrationPK);`

**`3`** `     parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegName).Text);`

**`4`** `     parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegContact).Text);`

**`5`** `    parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegEmail).Text);`

**`6`** `     parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegPassword).Text);`

**`7`**  `using` `(` `SxmTransaction` ` sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`8`**   `InsertResponse` ` ir = sxmTransaction.executeInsert(` `"registerCompany"` `, `

 `parameterValues);`

**`9`**  `if` `(sxmTransaction.commitTransaction () !=` `SQLiteErrorCode` `.Ok` `)`

`          throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Commit error."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

`      }`

`    }`

`  }`

Let’s take a detailed look at the `processSubmitHandler` method.

*   On line 1, we create a new GUID. Earlier, I explained how GUIDs would be used as the primary key, instead of the traditional auto-increment integer.

*   On lines 2 through 6, an `ArrayList` is populated with our newly created GUID along with the registration values entered in the company registration form. The values must be entered into the ArrayList in the same order they are named in the insert statement used to save the record.

*   On line 7, we instantiate an `SxmTransaction` object. The `SxmTransaction` constructor takes one parameter, the name of database for which you wish to interact. As a convenience, you can omit the database name parameter provided your app only uses one database, i.e., only defines one database descriptor. In this case, the constructor could be written as:

    `sxmTransaction = ` `new`  `SxmTransaction` `();`

*   On line 8, we execute the insert command that performs the actual insert of the record into the database. The method `executeInsert` takes two parameters; the name of the insert statement from the SQL statements properties file and the `ArrayList` that holds the record data to be inserted into the database.

*   On line 9, the transaction is committed. At this point, the record will be been inserted into the database. If you exit the `using` block without committing the transaction, the cleanup code will perform a rollback. The `commitTransaction` method returns a `SqliteErrorCode` , defined in the assembly `Mono.Data.Sqlite` . See the next section, ‘Committing transaction.’

Most of the code above is very simple and self-explanatory. However, there are a few things worth noting. Always instantiate an `SxmTransaction` inside a `using` statement. This is necessary in order to guarantee proper clean-up. You should perform as little work as possible inside of an `SxmTransaction using` block. This is to limit the life of the transaction object. For example, don’t do things similar to the following.

 `using` `(` `SxmTransaction` ` sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

 `ArrayList` ` parameterValues = ` `new`  `ArrayList` ` ();`

 `string` ` registrationPK = ` `Guid` `.NewGuid ().ToString ();`

`   parameterValues.Add (registrationPK);`

`   parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegName).Text);`

`   parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegContact).Text);`

`   parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegEmail).Text);`

`   parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegPassword).Text);`

 `InsertResponse` ` ir = sxmTransaction.executeInsert(` `"registerCompany"` `, `

`                                                     parameterValues);`

 `SQLiteErrorCode` `SqliteErrorCode = sxmTransaction.commitTransaction ();`

`  }`

In the coded fragment above, we are building the parameter values array inside the `using` block. This causes us to hold onto database resources longer than necessary. DO NOT pass an `SxmTransaction` object to other threads. Depending on the state of the transaction, this could cause problems.

The `executeInsert` method locates the insert statement from the SQL statements properties file that matches the statement name passed in as the first parameter. In our example, this would be the entry below.

`INSERT INTO companyReg (companyRegPK, coName, hrContact, email, password) VALUES(?, ?, ?, ?, ?)`

The values in the `ArrayList` passed in as the second parameter replace the parameter placeholders in the SQL statement. The statement is then executed. If you have been following along closely, you are probably wondering why an insert definition must include the name of the table being inserted. As a refresher, the format of an insert definition in the SQL statements properties file is as follows:

`[` *`statement name`* `][` *`table name`* `][` *`insert SQL statement`* `]`

The purpose for the statement name and the insert SQL statement is obvious, but why the table name? Earlier I mentioned that an ID field used for synching records is added to every table. After an insert is performed, an immediate update to the record is then executed in order to add the synched ID.  The table name is used by this update code. The table name could be extracted from the insert statement, but it is more efficient to have it as an explicit field rather than parsing the statement field.

**Committing transactions**

The `SxmTransaction` object performs a true transaction. That is, all SQL commands executed by an instance of `SxmTransaction` that modify the database are applied or discarded atomically by the `commitTransaction` or `rollbackTransaction` methods`. commitTransaction` returns a `SQLiteErrorCode` . If the commit is successful, the return value is `SQLiteErrorCode.Ok` . Any other return value indicates an error that occurred in the SQLite engine. A list of SQLite error codes can be found in Appendix A. Other errors encountered during the execution of `commitTransaction` will result in an exception. Modifications to the database will not be visible to other transaction objects until the changes are committed. A transaction object can see its own changes as they are occurring, before a commit. For more details, see the sections ‘Understanding Transactions’ and ‘Transaction Visibility.’

**The insertResponse object**

The `executeInsert` method returns an `InsertResponse` object.

`InsertResponse` ` ir = sxmTransaction.executeInsert (` `"registerCompany"` `, parameterValues);`

This object contains the auto increment ID and the `systemSynchID` for the newly inserted record. Remember, the `systemSynchID` is a system managed field which is added to every table and is used for synching to the cloud. For the most part, these values are not really all that important for your application code. While the increment ID can be used to uniquely identify a record locally, this is really not a good idea. ID’s are not unique across devices and relying on them can cause problems. You are far better off using GUIDS as unique identifiers, I explained this earlier. The record ID and the synch ID are both properties with getters that can easily be accessed.

`string` ` synchID = ir.SynchID;`

`int` ` recordID = ir.RecordID;`

If the record ID is -1 or the synch ID is null, then a problem occurred with the insert that didn’t result in an exception being thrown. This should be a very rare condition indeed. The `systemSynchID` is a system managed field and unless you have some compelling reason to do otherwise, it is best left alone.

**Saving file attachments**

File attachments can be saved directly in the database as a BLOB or as an external file with a pointer stored in the database. There are legitimate reasons for choosing one or the other. As a practical matter, unless you intend to store a large number of files or you expect the files to be rather large, it probably doesn’t make a huge difference which option you choose.

According to the SQLite documentation:

“For BLOBs smaller than 100KB, reads are faster when the BLOBs are stored directly in the database file. For BLOBs larger than 100KB, reads from a separate file are faster.”

But processing speed should not be the only consideration or even the primary consideration. I find storing files outside the database to be more flexibility. Often times, it can be very difficult to know in advance the direction a project will take over time. Trying to predict future requirements is a fool’s errand. For this reason, when presented with the option of flexibility over performance or convenience, I almost always opt for a more flexible engineering solution. For example, one application I wrote ended up having a requirement to share file data between records without duplicating the file data. This particular requirement didn’t show up until 5 years after the initial release. This would have been very difficult to implement had we not chosen to store attachments as external files. I worked on another app which included support to save file attachments in virtually unlimited numbers. Initially, we stored the files on dedicated servers that were separate from the database server. This was before AWS S3 and other similar services. When S3 was introduced, we decided to move our all file from our servers into S3 storage. In this case, storing the files outside the database simplified the transition to S3\. In both these cases, flexibility served us well as requirements changed in ways we could not have predicted when initially designing our application.

Storing inside the database allows for file attachments to automatically participate in transactions and makes backups and some other database operations easier. And don’t forget, external files means there’s one more item that needs to be managed as part of every record. This can complicate your design significantly; for example, you’ll need to include exception processing in your app to deal with synching failures, such as when a record delete succeeds but the associated file delete fails.

Let’s dig deeper into this to see what I’m talking about. Imagine you delete a database record that includes an external file attachment, but when you try and delete the associated file, you get some sort of failure. Now what do you do?

1.  Acknowledge the failure by performing a rollback on the record delete. If this was an automated delete, try it again later, otherwise, alert the user that a failure occurred and ask them to try the selected operation again later.
2.  Allow the record delete to fully process by issuing a commit. The file is marked somehow in order to permit automatic removal at some later date.
3.  Allow the record delete to fully process by issuing a commit. The file failure is ignored and the file is simply left orphaned.

You can only make the “right” choice after considering the specifics of the particular application. Even so, none of these are particularly attractive options. It would be best if this problem were solved by not allowing the problem to occur in the first place. And you can do that by storing the file in the database.

Exception processing is an ever-present fact of life, however, it almost always injects complexity into your design. So, as a general rule, you should design you code/application with as few failure points as possible. This seems obvious but you would be surprised how often this simple rule is ignored. We have considered competing file storage options each with strengths and weaknesses. Let us try and boil them down to a single sentence and provide some concrete advice.

*   Storing files outside the database is likely to be more flexible, but it usually create additional points of failure and is normally more complicated to implement.
*   Storing files inside the database is normally less flexible but easier to design and implement.

I prefer to store files outside the database, that’s the advice I almost always give. That being said, every app is different and only you know what’s best given your particular requirements. It might seem strange that after I delineate the pitfalls of external file storage that I would, as a general rule, recommend this solution. I believe, all things considered, it is usually the better choice.

So, that’s it? Unfortunately, no. There is still one more consideration. If the tables where you store files are going to be replicated, you should consider the specifics of how file transfers are performed between your app and the cloud server. In our case, we’ve decided to use HotRiot as our cloud storage solution. The HotRiot API performs file transfers expecting the file data to be an actual file on disk (SSD). This doesn’t necessarily mean you can’t store files inside the database, but in our case, it provide one more reason to use an external file instead.

Updating records

The way records are updated is very similar to the way they are inserted. Let’s take the record insert example from earlier and modify it in order to perform an update.

`  [` `Activity` ` (Label = ` `"UpdateHRActivity"` `)]            `

 `public`  `class`  `UpdateHRActivity` ` : ` `Activity`

`  {`

 `protected`  `override`  `void` ` OnCreate (` `Bundle` ` bundle)`

`    {`

 `base` `.OnCreate (bundle);`

`      SetContentView (` `Resource` `.` `Layout` `.CoRegistration);`

 `Button` ` submitCoRegButton = FindViewById<` `Button` `> (` `Resource` `.` `Id` `.submitCoRegButton);`

`      submitCoRegButton.Click += ` `delegate` ` { updateHRContactSubmitHandler (); };`

`    }`

 `private`  `void` ` updateHRContactSubmitHandler()`

`    {`

 `ArrayList` ` updateValues = ` `new`  `ArrayList` ` ();`

`     updateValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegContact).Text);`

`     updateValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegName).Text`

 `using` `(` `SxmTransaction` ` sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`1`** `       sxmTransaction` `.executeUpdate(` `"updateHRContact"` `updateValues);`

**`2`**  `if` `(sxmTransaction.commitTransaction () !=` `SQLiteErrorCode` `.Ok` `)`

`          throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Commit error."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

`      }`

`    }`

`  }`

Everything here should look pretty familiar. Line 1 is where the actual call is made to perform the update. As you can see, this is very similar to the insert example. The `executeUpdate` method locates the update statement from the SQL statements properties file that matches the statement name passed in as the first parameter. In our example, this would be the entry below.

`[updateHRContact] [UPDATE companyReg SET hrContact = ? WHERE coName = ?]`

The values in the `ArrayList` that’s passed in as the second parameter replace the placeholders in the SQL statement. The statement is then executed. Of course, update operations modify the database, they therefore require a commit, which is done on line 2.

Deleting records

The method below performs a record delete on the company registration table.

 `private`  `void` ` deleteCoRegistration (` `string` ` registrationRecordPK)`

`  {`

 `ArrayList` ` deleteKey = ` `new`  `ArrayList` ` ();`

`   deleteKey.Add (registrationRecordPK);`

 `using` `(` `SxmTransaction` ` sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`1`** `     sxmTransaction` `.executeDelete(` `"deleteCompanyReg"` `deleteKey);`

**`2`**  `if` `(sxmTransaction.commitTransaction () !=` `SQLiteErrorCode` `.Ok` `)`

`        throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Commit error."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

`    }`

`  }`

At this point, everything should look pretty familiar. Insert, update, and delete operations are all invoked in a very similar manner. Line 1 is where the actual call is made that performs the delete. As you can see, this is very similar to the insert and update examples. The `executeDelete` method locates the delete statement from the SQL statements properties file that matches the statement name passed in as the first parameter. In our example, this would be the entry below.

`[DELETE]`

`[deleteCompanyReg] [DELETE FROM companyReg WHERE companyRegPK=?]`

`[]`

The values in the `ArrayList` that’s passed in as the second parameter replace the placeholders in the SQL statement; this can be a null or an empty list. The statement is then executed. Of course, a delete operations modify the database, they therefore require a commit, which is done on line 2.

Error Processing

Errors are a fact of life for any app of significance, so I suppose it goes without saying that proper error handling is critical. But you’d be surprised how often I see error processing implemented as an afterthought. Often what you see is the main line of the code implemented first and then the exception processing grafted on at some later point. It is natural to set aside error handling; it’s mostly mundane work that feels somewhat unproductive, and it can be difficult to do well. But don’t wait. The sooner you start dealing with exception conditions the better. It will prompt you to think about your code in a deeper more critical way and probably get you to implement more robust solutions. However, to get real benefit from this, it needs to be done while you are writing the main line of code. Enough said, for now. Let’s have a look at a two examples. The first will show exception processing during database initialization. The second example will show error processing for an `SxmTransaction` .

**Initialization error processing**

The `initDB` method below initializes the database, preparing it for use. It performs the basic tasks required by SQLite.XM. The interesting dilemma with initializations, is that you often can’t proceed if they fail. This is certainly almost always the case with database initialization. It’s kind of hard to recover from errors rooted in the foundation of an app. For example, if database schema initialization fails, how can you really expect to run your app with any confidence? The answer is, you can’t. That’s the bad news. The good news is, once you get initialization working, it would be unusual for it to fail. So, for the most part, error processing on initialization is used more during development than for recovery. That being said, should initialization fail in production, you need to process the error in a sane manner; don’t just let it go. It’s better to proactively deal with an unrecoverable condition rather than let it manifest into something worse. Let’s get on with the code below

`  protected`  `void` ` initDB ()`

`  {`

**`1`**  `DatabaseDescriptor` ` jsDD = ` `null` `;`

 `string` `errorMessage =` `null` `;`

**`2`**  `bool` ` parsed = ` `false` `;`

**`3`**  `bool` ` init = ` `false` `;`

 `try` `{`

**`4`** `     jsDD  = ` `new`  `DatabaseDescriptor` `(` `"jsearch"` `);`

 *`// For Android apps.`*

 `using` ` (` `StreamReader` ` sr = ` `new`  `StreamReader` ` (Assets.Open (` `"SqlStatements.txt"` `))){`

 *`// For iOS apps.`*

 `using` ` (` `StreamReader` ` sr = ` `new`  `StreamReader` ` (` `”sqlProperties/SqlStatements.txt"` `)){`

**`5`** `       parsed = ` `ProcessSQLStatements` `.Parse (sr);`

`      }`

**`6`** `     init = ` `SxmInit.` `initialize ();`

`    }`

 `catch` ` (` `SxmException` ` sxmEx){`

 `Exception` ` iex = ` `SxmException` `.getInnermostException (sxmEx);`

`      errorMessage = ie` `x.Message;`

`    }`

 `catch` ` (System.` `Exception` ` ex){`

`      errorMessage = ex.Message;`

`    }`

 `finally` `{`

 `if` `(errorMessage != null){`

  `string` ` initResult = ` `String` `.Format (` `"jsDD: ` `{0}` `, ` `Parsed: ` `{2}` `,`

 `  Init: ` `{3},` `Error:` `{4}` `"` `, `

 `jsDD, parsed, init,`

 `errorMessage);`

  `Log` `.Debug(` `"initDB"` `, initResult);`

`     }`

`    }`

`  }`

Lines 4 through 6 is where the database is initialized. Initialization should always be wrapped in a try-catch with an accompanying finally block. The methods `parse` and `initialize` will throw an `SxmException` on error. An error instantiating a `DatabaseDescriptor` will also result in an `SxmException` . In our example, we catch the `SxmException` and the base `System.Exception` . The vast majority of exceptions that occur in the SQLite.XM library are re-thrown as `SxmExceptions` . In fact, all try-catch blocks in the library re-throw an `SxmException` . The only time you would see another exception coming out of the library is for something that’s uncaught. However, this is unusual and is only allowed for really oddball conditions. You should always catch both the `SxmException` and the base `System.Exception` . Often times, the base exception catch won’t be needed but it won’t hurt to include it and it will serve as a safety. Really, all of your try-catches should catch the base exception. 

Inside the `SxmException` handler, you will see a call to `getInnermostException` . This method returns the root exception. SQLite.XM will set an inner exception when appropriate. This can be helpful for tracing errors, however, often times you are only interested in getting at the root cause. If there is no inner exception, `getInnermostException` will just return the top-level exception.

The methods `parse` and `initialize` return *true* upon successful completion. Of course, the *new* statement on line 4 returns a `DatabaseDescriptor` instance. We can use this knowledge to help us more easily identify the source of an error. By initializing the return values to *null* and *false* (see lines 1, 2 and 3), we can then inspect the state of these values inside the finally block to see where an exception occurred. For example, if we fall into the finally block and see that `jsDD` is non-null but `parsed` and `init` are false, we can reasonably deduce that the error occurred in the call to `Parse` . The exception message will usually point you to the offending code and you can always look at the stack trace to find the source of an error. But this does provide a level of convenience and can simplify things a bit when an error occurs in a method that is shared.

**The SxmException object**

Below is the output from an `SxmException` object for a database timeout error I intentionally caused.

![](Image00024.jpg)

The *Data* property of all SxmExceptions include an `SxmErrorCode` key, which returns the enum value of the error. Of course, an error message is also always set. You can have a look at all possible SxmErrorCodes by inspecting the enum `Defines.SxmErrorCode` located in *Defines.cs* . If the `SxmErrorCode` is set to `sqliteException` , then this tells you that the error originated inside SQLite. In that case, there will be another key in the *Data* property field named `sqliteErrorCode` . This is the SQLite assigned error code for the error. See Appendix A for a list of all SQLite error codes. You can find a list of all SQLite.XM errors in the *ErrorMessages.cs* source file. When there is an inner exception, the `sxmErrorCode` will be set to `innerException.` Of course, the `InnerException` property will be also be set.

You can throw your own user defined `SxmException` using the following line of code.

 `throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Some error message."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

**Transaction error processing**

Let’s have a look at an error processing example for an `SxmTransaction` . The code below performs a simple insert followed by a search. The search results are then retrieved and the transaction committed. I won’t bother going through the code, this is stuff you have already seen.  Let’s just focus on the error handling.

`  private`  `void` ` processInsert()`

`  {`

 `List` `<` `Hashtable` `>` `allRows = ` `null` `;`

 `InsertResponse` ` ir = ` `null` `;`

 `ArrayList` ` parameterValues = ` `new`  `ArrayList` ` ();`

`    parameterValues.Add (` `Guid` `.NewGuid ().ToString ());`

`    parameterValues.Add (` `"testCoName"` `);`

`    parameterValues.Add (` `"testContact"` `);`

`    parameterValues.Add (` `"testemail@testCoName.com"` `);`

`    parameterValues.Add (` `"testPassword"` `);`

 `try` `{`

 `using` ` (` `SxmTransaction` `sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

 `ir = sxmTransaction.executeInsert(` `"registerCompany"` `, parameterValues);`

  `if` ` (ir.SynchID == ` `null` ` || ir.RecordID == -` `1L` ` )`

  `throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Insert error @ processInsert."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

  `sxmTransaction.executeQuery (` `"findCompany"` `, ` `null` `);`

  `allRows = sxmTransaction.getAllRows ();`

**`1`**  `if` `(sxmTransaction.commitTransaction () ==` `SQLiteErrorCode` `.Busy` `){`

 `Thread` `.Sleep (` `50` `);`

`           sxmTransaction.commitTransaction ();` `// Try again.`

`        }`

`      }`

`   }`

 `catch` ` (` `SxmException` ` sxmEx){`

 `throw` `SxmException` `.getInnermostException (sxmEx);`

`    }`

 `catch` ` (System.` `Exception` ` ex){`

 `throw` ` ex;`

`    }`

`  }`

An `SxmTransaction` object should always be instantiated within a `using` statement. This is important in order to guarantee that database resources are properly released. The transaction cleanup code, which is automatically called when exiting the `using` block, has a no-throw guarantee. The reason for this, is that even if cleanup encounters an error it makes a best effort to complete processing and release all resources. We don’t want to leave the database in an indeterminate state by interrupting cleanup midway through. The transaction cleanup code has one additional behavior you need to be aware of;

*   If a transaction that performed a database update is being cleaned-up, and the transaction is still active, i.e., a call to `commitTransaction` or `rollbackTransaction` was not successfully executed, then the cleanup code will automatically roll back the transaction.

This is important to understand. Exiting a `using` block with an active transaction is essentially considered an error condition by the cleanup code and will result in a rollback. As far as dealing with errors inside the using block, there are a variety of try-catch combinations that you could use, but they all basically boil down to three options.

*   Place a try-catch around the `using` block.
*   Place a try-catch inside the `using` block that encloses all statements.
*   Place a try-catch around the `using` block and around specific statements inside the `using` block.

There is no “right” choice. Any one of these may be more or less appropriate given different circumstances. By using the first option, you are essentially saying that ANY exception that occurs while a transaction is active should result in a rollback. The reason for this, is that all exceptions will exit the `using` block. Remember our earlier rule: exiting a `using` block with an active transaction will result in a rollback. This is the error processing strategy that I use most. I feel that it best fits the spirit of transactions and how they are meant to be used.

The second try-catch option allows you to examine an exception and take some remedial action before exiting the `using` block. You could, presumably, decide to commit the currently active transaction or retry a failed operation or execute other intermediate operations. This could be useful if you have some cleanup of your own that you need to perform first before exiting the `using` block, or if you wish to be able to commit a partially successful transaction. I generally don’t find this strategy to be very useful. Generally speaking, transactions are meant to be short-lived operations that either succeed or fail in their entirety. And it is best to not perform other work inside a transaction that needs its own cleanup.

The last try-catch option gives you fine grained control over how to process individual exceptions that occur inside the `using` block. You might choose to use this strategy if you’re performing multiple independent transactions using a single transaction object. See the code fragment below.

`try` `{`

`  using` ` (` `SxmTransaction` `sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

 `try` `{`

 `ir = sxmTransaction.executeInsert(` `"registerCompany"` `, parameterValues);`

 `if` ` (ir.SynchID == ` `null` ` || ir.RecordID == -` `1L` ` )`

 `throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Insert error @ processInsert."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

 `if` `(sxmTransaction.commitTransaction () !=` `SQLiteErrorCode` `.Ok` `)`

`        throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Commit error @ processInsert."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

`    }`

 `catch` ` (System.` `Exception` ` ex){`

`      sxmTransaction` `.rollba` `ckTransaction ()                           `

`    }`

 `try` `{`

 `ir = sxmTransaction.executeInsert(` `"newRegistration"` `, parameterValues);`

 `if` ` (ir.SynchID == ` `null` ` || ir.RecordID == -` `1L` ` )`

 `throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Insert error @ processInsert."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

 `if` `(sxmTransaction.commitTransaction () !=` `SQLiteErrorCode` `.Ok` `)`

`        throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Commit error @ processInsert."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

`    }`

 `catch` ` (System.` `Exception` ` ex){`

`      sxmTransaction.rollbackTransaction ()                           `

`    }`

`    sxmTransaction.executeQuery (` `"findCompany"` `, ` `null` `);`

 `return` `sxmTransaction.getAllRows ();`

`  }`

`}`

The transaction object above is used to execute two independent transactions. If the first transaction fails, the second is still permitted to execute. If the second transaction fails, the query statement is still permitted to run. If you have independent transaction, you might decide to process exceptions inside the `using` block in this manner. This sequence leaves one unanswered question: what happens if the rollback fails? If there is an error executing a rollback, an exception is thrown. This is true unless the rollback is being executed by the `using` block cleanup code.  The reason for throwing an exception, is a rollback is a pretty robust operation and a failure indicates a likely serious problem, at that point, it is probably best to exit the transaction and allow the cleanup code to run.

**Programming for errors**

Now I’m going to say something really silly; the best way to deal with errors is to write your code in such a way that they can’t occur. I know what you’re thinking; that’s not possible, and for the most part, I agree. However, approaching your code with that mind-set will cause you to seek out solutions with a minimal error profile and get you to deal with potential errors proactively. What do I mean by this? Let’s use the `SxmTransaction` class as an example.

Before the `SxmTransaction` class was designed to be used with a `using` statement, the typical usage pattern was as follows.

`  SxmTransaction` `sxmTransaction = null;`

 `try` `{`

`    sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `);`

 `// Do database work.`

`    sxmTransaction.commitTransaction ();`

`  }`

 `catch` ` (System.` `Exception` ` ex){`

 `if` ` (sxmTransaction != ` `null)` 

`        sxmTransaction.rollbackTransaction ();`

`  }`

 `finally` `{`

 `try` `{`

 `if` ` (sxmTransaction != ` `null)` 

 `sxmTransaction.completeTransaction ();`

`    }`

 `catch` ` (System.` `Exception` ` doNothing) {} `

`  }`

The transaction object and its accompanying statements are executed within a try-catch. The call to `completeTransaction` in the finally block cleans up the transaction. But looking at this, you see too many opportunities for problems.

*   Users might not wrap the transaction in a try-catch.
*   The finally clause might be omitted from the try-catch.
*   Users might forget to make the call to `completeTransaction` or place the call outside of a finally block or they might fail to include the null check. 
*   Users might forget to wrap the call to `completeTransaction` in a try-catch.
*   Users might forget to perform a rollback in the catch or they might fail to include the null check. 

Could this be rewritten to eliminate these potential problems and shrink the error footprint? Well, it turns out we could do much better. We made four modifications that significantly improved code.

*   The `SxmTransaction` object was fitted to work with the `using` statement.
*   The cleanup performed by the `completeTransaction` method was redesigned to have a no-throw guarantee. The rational being, that if an error occurred during cleanup, the cleanup code would be in the best position to deal with the problem. There is no advantage to pushing the error up the stack.
*   A rollback was incorporated into the cleanup code for an active transaction.
*   A finalize method was added to the `SxmTransaction` class in order to perform cleanup in the event a user failed to instantiate the transaction inside of a `using` statement.

So, what was the result of these changes? We reduced the five potential problems listed above to a single problem; a user might fail to instantiate a transaction inside a `using` statement. But even this was mitigated by adding a finalizer. In the process of tightening up the code, we also improved resource usage. How, you ask. The `SxmTransaction` object automatically goes out of scope when it exits the using block, making it immediately available for garbage collection. By simply taking a critical look at our original design, we found a few simple openings where we could improve usability. The net result is not only more robust, resource efficient code but code that is easier to read, write and harder to get wrong. This is what I mean when talking about minimizing your codes error profile.

When looking at your own code, ask this question; how can this fail and what can I do to make failure less likely.

**Some final thoughts regarding errors**

“ Any error that can occur, given enough time, will occur.”

While the probability of any particular error occurring might be very low, from a design philosophy, I try to following the statement above like a maxim. Now, as a practical matter you will probably end up bending this rule a bit, otherwise error processing could wind up consuming your app. Some errors are so remote that they don’t warrant checking or indicate a much deeper problem that an application is unequipped to handle even if caught. But for the most part, I recommend that you stick to this as a guiding principal.

An error reporting subsystem is as much about helping you, the developer identify and fix problems with efficiency as it is about providing your app with the information necessary for it to rationally manage errors in the wild. This is especially true when writing code that will be consumed by other developers. When designing your error management system, strive to always report with as much specificity as possible and try to provide both machine friendly and human friendly identifiers for all errors. Machine identifiers are typically numbers, preferably enums, humans, of course, do better with text messages.

Searching the database

Let’s perform a simple search of our database. In this example, we are going to search for records in the job postings database that were submitted by the currently logged in company user. Below is a screenshot of the search page.

![](Image00017.jpg)

When the *Get Jobs* button is selected, a search of the job postings database is initiated using the primary key from the company registration as the search parameter. Below is the entry in the SQL statements properties file for this search.

`[getCompanyJobs] [SELECT * FROM jobPosting WHERE companyRegFK = ?]`

The `GetJobs` method shown below is called when the *Get Jobs* button is selected.

 `private`  `ArrayList` ` GetJobs (` `string` ` registrationPK)`

 `{`

  `ArrayList` ` parameterValues = ` `new`  `ArrayList` ` ();`

 `  parameterValues.Add (registrationPK);`

  `List` `<` `Hashtable` `>` `postedJobs = ` `new`  `List` `<` `Hashtable` `>` `();`

  `Hashtable` ` postedJob = ` `null` `;`

  `using` `(` `SxmTransaction` `sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`1`**   `sxmTransaction.executeQuery (` `"getCompanyJobs"` `, parameterValues);`

**`2`**   `while` ` ((postedJob = sxmTransaction.getNextRow ()) != ` `null` `)`

**`3`**   `postedJobs.Add (postedJob);`

 `  }`

**`4`** `   buildTable (` `postedJobs` `);`

  `return` ` postedJobs;`

 `}`

We execute our query on line 1\. Then, on lines 2 and 3, we extract each row from the record set and place it in an array list. Each row is represented as a hash table, where the field names from the database table are the keys. We can extract the field data from the hash table using a simple key lookup. Lines 2 and 3 from our example are shown below.  The are used to retrieve the row data.

**`2`** `  while` ` ((postedJob = sxmTransaction.getNextRow ()) != ` `null` `)`

**`3`** `    postedJobs.Add (postedJob);`

As an alternative, we could have called the following method instead.

 `postedJobs = sxmTransaction.getAllRows ()`

This is an even easier way of getting the selected record data. The method `getAllRows` performs roughly the equivalent of lines 2 and 3 above. `getAllRows` always returns a valid `ArrayList` , however, the list will be empty if the record set is empty.

You will notice that we don’t call `commitTransaction` anywhere in the `using` block`.` There were no database update commands processed during the transaction, so there is nothing to commit. When a transaction only includes select statements, it doesn’t need to be committed.

As a general rule, you should free database resources as quickly as possible. You do this by limiting the amount of work you do within a transactions `using` block. As you can see, the record data is moved from the database into a collection and is then processed outside the using block. This allows us to complete the transaction early, releasing any resources used by the database. On line 4, the data selected by the query is passed to the `BuildTable` method. But by this time, the transaction object has already been released so we can spend whatever time we need processing the search results without having to concern ourselves about database resources. Now let’s take a look at the `BuildTable` method.

 `private`  `void` ` BuildTable (` `List` `<` `Hashtable` `>` `postedJobs) `

`  {`

 `TableLayout` ` jobsTable = (` `TableLayout` `)FindViewById(` `Resource` `.` `Id` `.coJobsTable);`

 `string` ` [] fieldData = ` `new`  `string` ` [` `3` `];`

`    jobsTable.RemoveAllViews ();`

**`1`**  `foreach` ` (` `Hashtable` ` job ` `in` ` postedJobs)`

`    {`

**`2`** `     fieldData[` `2` `] = job [` `"pay"` `].ToString ();`

**`3`** `     fieldData[` `0` `] = (` `string` `)job [` `"jobTitle"` `];`

**`4`** `     fieldData[` `1` `] = (` `string` `)job [` `"description"` `];`

 `TableRow` ` row = ` `new`  `TableRow` ` (` `this` `);`

 `foreach` ` (` `string` ` fieldValue ` `in` ` fieldData) `

`      {`

 `TextView` ` tv = ` `new`  `TextView` ` (` `this` `);`

`        tv.SetPadding (` `8` `, ` `10` `, ` `8` `, ` `10` `);`

`        tv.SetText (fieldValue, ` `TextView` `.` `BufferType` `.Normal);`

`        row.AddView (tv);`

`      }`

`      jobsTable.AddView(row);`

`    }`

`  }`

This method processes the search results by outputting the row data to a table that is dynamically created. Lines 1 thru 4 show how the individual field data for each row is accessed. The screenshot below shows the output for a search that located three job postings. This is basic stuff that’s pretty self-explanatory.

![](Image00022.jpg)

**Processing record data in-line**

In the example above, the selected record data was first moved out of the database and into a collection before being processed by the `BuildTable` method. There are times when this pattern makes sense, for example.

*   When handing off the record data to another thread for processing.
*   If you expect to perform some time consuming processing of the result set.
*   If you need to access the data multiple times or if you need to hold on to the data for other reasons.
*   Resource usage is not an issue and you wish to use the simplest design pattern.

As an alternative, you can, instead, process the selected records as they are read from the result set. Below is the `GetJobs` and `BuildTable` methods rewritten to show how this is done.

`  private`  `void` ` GetJobs (` `string` ` registrationPK)`

`  {`

 `ArrayList` ` parameterValues = ` `new`  `ArrayList` ` ();`

`    parameterValues.Add (registrationPK);`

 `using` `(` `SxmTransaction` `sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

  `sxmTransaction.executeQuery (` `"getCompanyJobs"` `, parameterValues);`

`      BuildTable (sxmTransaction);`

`    }`

`  }`

 `private`  `void` ` BuildTable (` `SxmTransaction` ` sxmTransaction) `

`  {`

 `TableLayout` ` jobsTable = (` `TableLayout` `)FindViewById(` `Resource` `.` `Id` `.coJobsTable);`

 `string` ` [] fieldData = ` `new`  `string` ` [` `3` `];`

`    jobsTable.RemoveAllViews ();`

**`1`**  `while` ` (sxmTransaction.nextRow () == ` `true` `)`

`    {`

**`2`** `     fieldData[` `0` `] = (` `string` `)sxmTransaction.getValue (` `"jobTitle"` `);`

**`3`** `     fieldData[` `1` `] = (` `string` `)sxmTransaction.getValue (` `"description"` `);`

**`4`**  `Type` ` payType = sxmTransaction.getType (` `"pay"` `);`

**`5`** `     fieldData[` `2` `] = ((System.` `Int64` `)sxmTransaction.getValue (` `"pay"` `)).ToString ();`

 `TableRow` ` row = ` `new`  `TableRow` ` (` `this` `);`

 `foreach` ` (` `string` ` fieldValue ` `in` ` fieldData) `

`      {`

 `TextView` ` tv = ` `new`  `TextView` ` (` `this` `);`

`        tv.SetPadding (` `8` `, ` `10` `, ` `8` `, ` `10` `);`

`        tv.SetText (fieldValue, ` `TextView` `.` `BufferType` `.Normal);`

`        row.AddView (tv);`

`      }`

`      jobsTable.AddView(row);`

`    }`

`  }`

Line 1 selects the next row for processing. The rows are iterated in the order they are returned by the query. The `nextRow` method will return false when there are no more records to process. Lines 2, 3,  and 5 retrieve the actual row data by calling the `getValue` method. We are selecting the job title, description, and pay. `getValue` returns a generic object, so it may be necessary to cast the return object to its actual type, as we are doing here. For example, on lines 2 and 3, the return values are cast to a string. On line 4, we are get the data type information for the value returned in the `pay` field. Normally this isn’t necessary as you usually know the data type for a field in advance. However, if you need to dynamically get a field’s type information, this is how you do it. The `nextRow` method only allows you to move forward in the result set; sometimes this is a problem and other times it isn’t. If you need to iterate over the results more than once or you need to be able to freely move forward and backward through the search results, first pull the records from the result set and place them into a collection.

Embedding SQL in your code

Let me say right from the start that I don’t recommend you embed SQL directly in your code unless you have a very good reason. SQL statements should be placed in the SQL statements properties file. That being said, there may be legitimate circumstances which call for imbedded SQL. SQLite.XM includes variations of the `executeUpdate` , `executeDelete` , and `executeQuery` methods that accept a SQL string. They are listed below.

*   `executeDeleteDirect (` `string` ` sqlStatement, ` `ArrayList` ` ParameterValues)`
*   `executeUpdateDirect (` `string` ` sqlStatement, ` `ArrayList` ` ParameterValues)`
*   `executeQueryDirect (` `string` ` sqlStatement, ` `ArrayList` ` ParameterValues)`

These are drop-in replacements for the `executeUpdate` , `executeDelete` , and `executeQuery` methods that we have been using thus far. The first parameter to all three of these methods is the actual SQL statement that you wish to execute. You can design your SQL any way you like, however, it must use the parameterized form that is used throughout this book and required by SQLite.XM. The second parameter is the usual `ArrayList` of values that replaces the placeholders in the SQL statement; this can be a null or an empty list.

Multi-database statement processing

This concept is explored in more detail a bit later; however, I need to provide a brief introduction to the notion of attaching and detaching databases. When an `SxmTransaction` object is created, it is for a particular named database. In the line of code below, we instantiate a transaction for the `jsearch` database. This is referred to as the transactions primary database.

`sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `);`

There is nothing unusual here, we’ve already seen this in numerous examples. Once created, SQL statements that are executed by a transaction object are executed on the database associated with the particular transaction. However, what if you want to execute statements that need to access tables in two or more databases? In order to do that, you need to “attach” the other secondary databases to the transaction, at which point, they can participate in queries executed by the transaction. Below is an example

`sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `);`

`sxmTransaction.attachDatabase (` `"anotherDatabase"` `);`

Once attached, you can execute SQL statements that require the participation the attached database. Attached databases remain accessible and part of a transaction object until detached. This is explored in more detail in the section ‘Performing joins across databases.’ I just wanted to introduce this concept to you as I make reference to it in the following section.

Understanding transactions

A transaction is a series of SQL statements that are applied to a database as one atomic operation that either succeeds or fails in its entirety. Do not confuse an `SxmTransaction` object with a transaction. Not all `SxmTransaction` objects implement a genuine database transaction. Let me explain. An underlying database transaction is only created by an `SxmTransaction` object when it executes a SQL statement that modifies a database in some way, i.e., any statement other than a select statement. The following are some points to keep in mind with respect to transactions.

*   An `SxmTransaction` object that only executes select statements will never create an underlying database transaction. There is really no need to wrap a series of select statements in a transaction, as there is nothing to commit.
*   An underlying database transaction is started by an `SxmTransaction` object only at the point that it executes a statement other than a select statement.  The reason for using this lazy initialization tactic, is that transactions acquire database locks, which can block other operations; for example, other databases updates. As a general rule of computing, you endeavor to minimize blocking.
*   Attached databases fully participate in transactions. If you attach a database to an `SxmTransaction` object and process a SQL statement that modifies the attached database, the call to `commitTransaction` will commit all updates made to both the primary and attached databases.
*   You cannot attach or detach a database once an underlying database transaction has started.
*   A single `SxmTransaction` object can host multiple transactions, serially, of course.

The last bullet point requires some elaboration; consider the code below. We instantiate a single `SxmTransaction` object and then use it to perform two independent transactions. In this example, we allow the second transaction to execute even if the first one fails. This is fine so long as the transactions are independent. The point to keep in mind, is you must complete one transaction before starting another. Now, I know this seems obvious, however, if you fail to successfully call either `commitTransaction` or `rollbackTransaction` , the transaction will remain active. In such a case, additional database operations will be appended to the unfinished, active transaction, obviously not what you would want.

`  using` ` (` `SxmTransaction` `sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

 `try` `{`

`      sxmTransaction.executeInsert(` `"registerCompany"` `, parameterValues);`

 `if` `(sxmTransaction.commitTransaction () !=` `SQLiteErrorCode` `.Ok` `)`

`        throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"registerCompany commit error."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

`    }`

 `catch` ` (System.` `Exception` ` ex){`

`      sxmTransaction.rollbackTransaction ()                           `

`    }`

 `try` `{`

`      sxmTransaction.executeInsert(` `"newRegistration"` `, parameterValues);`

 `if` `(sxmTransaction.commitTransaction () !=` `SQLiteErrorCode` `.Ok` `)`

`        throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"newRegistration commit error."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

`    }`

 `catch` ` (System.` `Exception` ` ex){`

`      sxmTransaction.rollbackTransaction ()                           `

`    }`

`    sxmTransaction.executeQuery (` `"findCompany"` `, ` `null` `);`

 `return` `sxmTransaction.getAllRows ();`

`  }`

Transaction visibility

Let’s take a closer look at how actions performed by one transaction are “seen” by other transactions. This concept is known as transaction isolation.

When there are multiple transaction objects active at the same time, operations that modify the database that are performed by one transaction are not visible to other transactions until they are committed. This can seem a bit strange at first. You really need to understand how this works, otherwise you can wind up with seemingly inexplicable behavior. The `processSubmitHandler` method below is from our earlier example, rewritten to illustrate transaction isolation.

 `private`  `void` ` processSubmitHandler()`

`  {`

 `ArrayList` ` parameterValues = ` `new`  `ArrayList` ` ();`

 `string` ` registrationPK = ` `Guid` `.NewGuid ().ToString ();`

 `string` ` companyName = FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegName).Text;`

`    parameterValues.Add (registrationPK);`

`    parameterValues.Add (companyName);`

`    parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegContact).Text);`

`    parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegEmail).Text);`

`    parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegPassword).Text);`

**`1`**  `using` `(` `SxmTransaction` `sxmTransaction1 = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`2`**   `InsertResponse` ` ir = sxmTransaction1.executeInsert(` `"registerCompany"` `, parameterValues);`

**`3`**   `using` `(` `SxmTransaction` ` sxmTransaction2 = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

  `parameterValues.Clear();`

  `parameterValues.Add (companyName);`

**`4`**  `    sxmTransaction2` `.executeQuery(` `"findCompany"` `, parameterValues);`

**`5`**   `List` `<` `Hashtable` `>` `rows = sxmTransaction2.getAllRows();`

**`6`**   `sxmTransaction1.commitTransaction ();`

**`7`**  `    sxmTransaction2` `.executeQuery(` `"findCompany"` `, parameterValues);`

**`8`**   `rows = sxmTransaction2.getAllRows();`

`      } `

`    }`

`  }`

This example shows how a record written to the database by one `SxmTransaction` object is invisible to another `SxmTransaction` object until the first object commits its transaction. For this example, assume we are starting with a database that has no records. Let’s pick apart the method.

*   On line 1, we instantiate an `SxmTransaction` object.

*   On line 2, a record is written to the `registration` table using our newly created transaction object.

*   On line 3, another `SxmTransaction` object is created.

*   On line 4, a query is executed using the transaction object created on line 3\. This query searches for all records in the `registration` table.

*   On line 5, we attempt to get the record data returned from the query executed on line 4\. However, because the insert that was executed on line 2 has not yet been committed, the result set is empty.

*   On line 6, the transaction object created on line 1 commits all of its updates. This transaction object is no longer usable.

*   On line 7, a query is executed using the transaction object created on line 3\. This query searches for all records in the `registration` table.

*   On line 8, we attempt to get the record data returned from the query executed on line 7\. Because a commit was performed by the transaction object that insert the record, the record is found.

A few things that should be noted from the sequence above. First, the obvious; be careful not to write your code in a such way that you wind up expecting to see updates to the database made by other transactions before they are committed. One simple way to avoid this problem altogether, is to have only one transaction object active at any given time. This may or may not be an acceptable solution given your particular application requirements.

Another, more subtle side effect that you need to be aware of, is that when working with multiple concurrent transaction, you can wind up with inconsistent results from database reads for which the reason may not be obvious. In the example above, we execute the exact same query on line 4 and line 7, and get different results each time, from the same transaction object. When working with an enterprise database, this would hardly be worth mentioning; as reads, writes, and deletes coming from multiple independent connections is the norm. But, this behavior might be less expected when running a single app against a dedicated database.

Assuming a result set is not empty, from the point that a select has executed, other `SxmTransaction` objects will be blocked from performing commits until the result set is fully iterated or until the `SxmTransaction` object associated with the select exits its `using` block. This guarantees that the contents of a result set will remain unchanged while being processed.

SQLite does have the ability for transactions to have a “snapshot” view of the database. The way this works is at the time a transaction object performs a read operation, the view of the data is conceptually snapshotted so that it remains consistent throughout the life of the transaction, regardless of updates committed by other transactions. Unfortunately, I have not been able to get this to work using the `Mono.Data.Sqlite` assembly. If something changes, I will post an update.

Performing joins across databases

For the vast majority of mobile applications, a single database is all that is needed and if your app falls into that category, you can safely skip this section. Of course, there are exceptions, and some developers may feel that their requirements are better met having more than one database. I am not going to go into detail discussing the merits of single-database verses multi-database designs. If you’re seriously considering multiple databases for your app, I assume you have good reasons and understand the pros and cons. Here, I am simply going to explain the mechanics of processing queries that include joins across multiple databases. You can skip this section if don’t have any queries that join tables between databases.

This example is going to be a bit contrived, but it will, nonetheless, serve to illustrate our how joins across databases are performed. Image your app creates the following two databases.

`try`

`{`

 `new`  `DatabaseDescriptor` `(` `"user"` `); `

 `new`  `DatabaseDescriptor` `(` `"transaction"` `); `

`}`

`catch` `( System.` `Exception` ` ex)`

`{`

 `string` ` message = ex.Message;`

`}`

The `user` database stores user registrations and related information while the `transaction` database stores user purchases and related information. The following tables appear in each database.

![](Image00014.jpg)

Our databases include other tables but we do not need to consider them in order to illustrate this example. Every time a user purchases a product, an entry is made into the `purchase` table that records the primary key of the user that made the purchase along with other product specific information. We would like to run a query that joins these two tables and returns all of the purchases made by a specific user along with the user’s registration information.

Let’s write a function to do this. For readability, I have opted to include the SQL query as part of the method rather than defining it inside the SQL statements properties file.

 `private`  `ArrayList` ` GetUserPurchases (` `string` `userPK` `)`

`  {`

 `ArrayList` ` transactions = ` `new`  `ArrayList` `();`

 `ArrayList` ` searchCriterion = ` `new`  `ArrayList` `();`

`    searchCriterion.Add (` `userPK` `);`

**`1`**  `using` `(` `SxmTransaction` ` sxmTransaction = ` `new`  `SxmTransaction` ` (` `"user"` `)){`

**`2`**   `  sxmTransaction.attachDatabase (` `"transaction"` `);`

**`3`**  `string` `selectStmt` `=` `“` `SELECT` ` reg.*, ` **`pur.name`** **`AS`** **`purName`** `,`

 `        pur.productPK, pur.purchasePrice`

  `FROM` `registration ` `AS` ` reg `

 `        JOIN`  **`transaction.purchase `** **`AS`** **` pur`** 

 `       ON` ` pur.registrationFK == reg.registrationPK `

  `WHERE` ` reg.registrationPK = ?”;`

  `sxmTransaction.executeQueryDirect (` `selectStmt` `, searchCriterion);`

   `Hashtable` ` transaction = ` `null` `;`

  `while` ` ((transaction = sxmTransaction.getNextRow ()) != ` `null` `)`

  `transactions.Add (transaction);`

**`4`**   *`// sxmTransaction.detachDatabase ();`*

`    }`

 `return` ` transactions;`

`  }`

On line 1 a transaction object is created on the `user` database. Nothing unusual here. On line 2 the `transaction` database is attached to our newly created transaction object. In order to include a database in a transaction, it must be attached using the `attachDatabase` method. You can call `attachDatabase` multiple times in order to attach more than one database to a transaction. As an alternative, you can call `attachDatabase` without any parameters and SQLite.XM will attach all of your databases to the current transaction.

The actual SQL select statement is defined on line 3\. There are a few things in the query that are worth pointing out. First, notice the join clause uses the fully qualified name for the `purchase` table. However, when aliasing the `registration` table, we used the shorthand notation that only includes the table name. Why is this? In a SQLite, when referencing tables in attached databases, the table name must be qualified with the database name where it is defined. In our example, the `transaction` database is the attached database. Full Disclosure: There are exemptions to this rule that allow you to omit the database name. However, I suggest you not bother learning these exemptions and just adhere to this rule. I’ll give you five reasons.

*   You will never get in trouble using the full qualified table name. It’s just a bit more typing.
*   More specificity in your SQL requires you to think more about what you are doing.
*   Including more information in your queries makes them self-documenting, making it easier for others to read. For example, by simply reading a query you will be able to identify the attached databases.
*   Always including the fully qualified name for attached databases, whether required or not, supports code consistency.
*   If you inadvertently misapply any of the exemptions, you could wind up with inconsistent, difficult to find bugs. Here is why, according to the SQLite documentation:

    “If two or more tables in different databases have the same name and the database-name prefix is not used on a table reference, then the table chosen is the one in the database that was least recently attached.”

    Therefore, if your code is written in a way where databases could be attached in different order, bugs may appear and disappear for no obvious reason.

Also, notice that the `pur.name` field is aliased as `purName` . The reason we needed to alias this field is because the `registration` table also includes a `name` field and had we not aliased one of these fields we would have gotten an ambiguous field name error when trying to execute this query.

You will notice on line 4 the commented call to `detatchDatabase` . I put it there to show you what we could have done. However, it turns out that the way in which we are using the transaction makes this call unnecessary, so I removed it. Below are rules for attaching and detaching databases that will clarify this.

*   If you don’t care about resource usage, concurrency, or efficiency, make things easy on yourself; ignore the rules below and just perform the attach immediately after creating the `SxmTransaction` object. Then forget about it, and let the detach automatically happen when the transaction object exits the `using` block. Otherwise, follow the rules below.
*   Attach a database as late as possible, preferably right before you intend to execute a statement that requires the attachment. One caveat: a database must be attached before any statement is executed that modifies a database, i.e., a statement other than a select. The reason for this is an underlying database transaction is started when a database is modified and you cannot attach a database after the start of a transaction.
*   Detach databases as soon as you are done using them. For example, if you intend to execute multiple select queries but only one of them uses the attached database, detach the database as soon as you are done iterating through the results of the query, but not before, otherwise you will lose the result set.
*   Exiting the `using` block for a transaction object will automatically detach any attached database. So in our example, it was unnecessary to explicitly detach the database, we just let it automatic happen.
*   Do not explicitly detach a database that is part of a transaction that performs an update until after you have called the `commitTransaction` method. The reason for this, is you cannot detach a database while in the middle of a transaction.

Locking and concurrency

If your application is guaranteed to only have a single transaction object active at any one time, for example, it performs database processing on a single thread and does not nest open transactions, then issues associated with locking and concurrency can largely be ignored. However, if your app creates multiple `SxmTransaction` objects simultaneously, you will need to understand locking and concurrency.

NOTE: This explanation of locking and concurrency is intended to provide you the practical knowledge necessary to manage concurrent connections. This is a somewhat complicated subject and I want to avoid getting bogged down in details that do not add to this goal. Some operational details are skipped over in order simplify this discussion and focus on presenting the core request information. For example, SQLite has a notion of PENDING locks, which I do not cover. I don’t believe you need to be concerned with this in order to properly manage concurrent connections.

Locks are used by SQLite in order to signal the operational state of a database. When multiple connections try and access a database concurrently, the database examines the lock state in order to ascertain which operations are permissible. Depending on the current lock state along with the requested operation, SQLite will either allow an operation to continue or block the operation until the lock state changes or a timeout occurs. The following locks can be acquired on a database.

*   **Shared** – Multiple transaction objects can have a shared lock simultaneously.
*   **Reserved** – Only one transaction object can have a reserved lock at any one time, however, a reserved lock can coexist with shared locks.
*   **Exclusive** – Only one transaction can have an exclusive lock. All other locks must be disposed of before a transaction can acquire an exclusive lock. Once acquired, no other locks may be acquired until the exclusive lock is disposed.

When an `SxmTransaction` object is first created, it holds no lock on the database. An attempt to acquire a lock only occurs when performing an operation. Let’s see which locks are acquired by which operations.

*   SQL select statements attempt to acquire shared locks. A shared lock is used to tell SQLite that the connection is currently reading from the database.
*   Operations that modify a database, i.e., insert, update, and delete, attempt to acquire reserved locks. A reserved lock tells SQLite that at some point this connection may update the database by committing its transaction.
*   A connection attempts to acquire an exclusive lock when it wishes to write to the database, i.e., commit its transaction. In SQLite.XM, a commit is executed by the `commitTransaction` method`.`

The rules are fairly simple, but there are operational details that are best shown with an example; please see below. This code is a bit contrived, but the goal here is to explain concurrency in a way that is easy to understand. Rather than create a multi-threaded example, which might be a bit difficult to follow, I chose to nest the transaction instead. For our purposes, the effect is the same. For this example, assume no other `SxmTransaction` objects exist anywhere else in our app.

 `public`  `ArrayList` ` deleteRegistration (` `int` `deleteRegPK)`

`  {`

 `ArrayList` ` regList =` `null` `;`

**`1`**  `using` `(SxmTransaction` ` sxmTransactionSearch = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`2`**   `sxmTransactionSearch.executeQuery (` `"getAllCompanies"` `, ` `null` `);`

**`3`**   `deleteRegistration (deleteRegPK);`

  `while` ` ((company = sxmTransactionSearch.getNextRow ()) != ` `null` `) `

  `{`

  `if` ` (company [` `"name"` `].Equals(` `""` `) ==` `true` `) `

  `{`

**`4`**   `deleteRegistration (company.companyPK); `

**`5`**  `regList = searchRegistrations ();`

  `}`

  `}`

**`6`**   `deleteRegistration (deleteRegPK);`

`    }`

 `return` ` regList;`

`  }`

 `public`  `void` ` deleteRegistration (` `int` `companyPK)`

`  {`

 `ArrayList` ` paramVaues =` `new` ` ArrayList();`

`    paramVaues.Add(companyPK);`

 `using` `(` `SxmTransaction` ` sxmTransactionDelete = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`7`**   `sxmTransactionDelete.executeDelete (` `"deleteCompanyReg"` `, paramVaues);`

**`8`**  `  sxmTransactionDelete.commit` `Transaction ();`

`    }`

`  }`

 `public`  `ArrayList` `searchRegistrations ()`

`  {`

 `using` `(` `SxmTransaction` ` sxmTransactionSearch = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`9`**   `sxmTransactionSearch.executeQuery (` `"getAllCompanies"` `, ` `null` `);`

**`10`**   `List` `<` `Hashtable` `>` `searchResults = sxmTransactionSearch.getAllRows ();`

`    }`

 `return` ` searchResults;`

`  }`

The `deleteRegistration` method does two things; it deletes the registration record associated with the passed in primary key and it attempts to delete any registrations in the company registration table where the ‘name’ field is blank. Coming into this method, the `jsearch` database lock status is as follows:

Locks: NONE

On line 1, a new `SxmTransaction` object is created. On line 2, the newly created transaction object executes a query to locate all registration in the company registration table. The select statement for this query, as it appears in the SQL statements properties file, is shown below.

`[getAllCompanies] [SELECT * FROM companyReg]`

The `executeQuery` call successfully acquires a read lock on the database. The database lock status is now as follows:

Locks: READ

On line 3, a call to the method `deleteRegistration` is made. If you look at this method, you will see that it attempts to delete the record associated with the passed in primary key. On line 7, a call to

`executeDelete` is made. The SQL statement for this delete, as it appears in the SQL statements properties file, is shown below.

`[deleteCompanyReg] [DELETE FROM companyReg WHERE companyPK = ?]`

The `executeDelete` call successfully acquires a reserved lock. The database lock status is now as follows:

Locks: READ, RESERVED

On line 8, a call to `commitTransaction` is made, where it will attempt to commit the delete that was executed on line 7. Unfortunately, this call will fail with a timeout, as it will be unable to acquire an exclusive lock because the read lock has not yet been disposed; the read is still active. What happens here, is the transaction attempts to convert the reserved lock it currently holds, into an exclusive lock, but the currently active read lock causes the commit to block until it times out. SQLite.XM will rollback the transaction as part of its cleanup when existing the using block; the reserved lock held by this transaction object is disposed as part of the cleanup. The database lock status is now as follows:

Locks: READ

On line 4, a call to `deleteRegistration` is made inside the loop that iterates through the search results returned from the search performed on line 2\. This call fails for the same reason it failed when called from line 3.

On line 5, a call is made to `searchRegistrations` . As you can see, this method performs a search of the registration table. After executing the query on line 9, the database lock status will be:

Locks: READ, READ

After retrieving the search results on line 10, the database lock status will be as follows:

Locks: READ

Let’s pause a moment to consider what just happened. The `executeQuery` method successfully acquired a read lock, while the call to `getAllRows` disposed of that lock. Assuming a result set is not empty; from the point that a select is executed, it will hold a read lock until the result set is fully iterated or until the `SxmTransaction` object associated with the select is cleaned up by the `using` statement. This is important to fully appreciate. A long running select or failing to fully iterate through a result set quickly, will block other connections from acquiring an exclusive lock. If the result set is empty, no read lock will be acquired.

On line 6, another call to the `deleteRegistration` method is made. However, unlike our previous attempts, this one will succeed.  When this call is made, the database lock status is as follows:

Locks: NONE

Even though the connection is still active, the read lock acquired by the query on line 2 has already been disposed of by the time we get to line 6\. This is because the search results have been fully iterated. The call to `executeDelete` on line 7 will successfully acquire a reserved lock. The call to `commitTransaction` , which is made on line 8, will quickly acquire an exclusive lock and then immediately dispose of the lock once the transaction is committed. Returning from call on line 6, the database lock status is as follows:

Locks: NONE

There are some things to consider. For example, if a database update operation times out due to blocking on acquiring a reserved lock, an exception will be thrown. No exception is thrown if the exclusive lock cannot be acquired on a commit and the commit times out; in this case, a `SQLiteErrorCode` is returned. For details, see the sections ‘Committing transactions’ and ‘Error processing.’ Be careful of long running selects and not quickly iterating through result sets; they both block exclusive locks.

Blocking trying to acquire an exclusive lock during a commit should be limited to the length of time needed to execute the longest currently running read operation. Remember, their can be multiple concurrent read operations in play at any one time. If you’re careful to not have any long-running queries, this delay should be short lived. Once acquired, a commit normally only holds an exclusive lock for a few milliseconds. Exclusive locks block everything.

Deadlock conditions

Consider the following: two connections are reading from the database and they each hold a shared lock. Then, at about the same time, they both try to perform a write operation, requiring them to obtain a reserved lock. We know from our earlier discussion that only one connection can hold a reserved lock at any one time. So, one of the connections is handed the lock while the other blocks, waiting for the lock to come available. Now the connection that holds the shared lock wants to commit its writes. So it tries to acquire an exclusive lock. However, it can’t get the exclusive lock because the blocked connection is holding a shared lock. We are now in a deadlock condition, where each connection is waiting on the other. The blocked connection is waiting on the reserved lock to come available while the connection holding the reserved lock is waiting for the shared lock to be disposed so it can get the exclusive lock.

The question is, how does SQLite handle such a condition? SQLite doesn’t allow deadlock condition to persist. The lock manager either grants a request for a lock or returns an error without blocking the requester. Therefore, in this example, the connection trying to acquire the reserved lock will eventually return with a database lock error.

Nesting connections

I don’t believe nested connections are too prevalent or even all that useful in most circumstances. Consequently, this wasn’t something I was initially intending to discuss. However, using them to explain locking revealed an opportunity to present some additional nesting examples that you might find interesting.

It is acceptable to nest connections so long as you are careful about what you are doing. If you need the results of one query as an input to another transaction object that is performing an update, pull all of the results out of the result set first, do not try to process them in-line with connection nesting. The reason for this depends upon the specifics of your implementation, in-line processing may not work, as the update may block trying to acquire an exclusive lock. Let’s take a look at four different ways of doing this.

The update in the code fragment below will fail because the `commitTransaction` method on line 3 times out trying to acquire an exclusive lock. The reason for the timeout, is the `sxmTransactionSearch` object is holding a read lock. Admittedly, even if this could work, it is a rather inefficient way of doing this anyway. Let me explain why. Lines 1 through 3 represent a single update transaction. Due to the way transactions are processed by SQLite, they generally take two full rotations of a disk platter in order to complete. So, for a disk spinning at 10,000 RPM, the theoretical write limit is ~83 updates per second. Of course, the actual limit is somewhat less. Certainly, there are also inefficiencies associated with creating and tearing down a connection inside a loop, not good.

 `using` ` (` `SxmTransaction` ` sxmTransactionSearch = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

  `sxmTransactionSearch.executeQuery (` `"getAllCompanies"` `, ` `null` `);`

 `ArrayList` ` paramVaues =` `new` ` ArrayList();`

  `while` ` ((company = sxmTransactionSearch.getNextRow ()) != ` `null` `) `

  `{`

  `if` ` (company [` `"name"` `].Equals(` `""` `) ==` `true` `) `

  `{`

 `paramVaues.Clear ();`

 `paramVaues.Add(company [` `"companyPK"` `]);`

**`1`**  `using` ` (` `SxmTransaction` ` sxmTransactionDelete = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`2`**  `sxmTransactionDelete.executeDelete (` `"deleteCompanyReg"` `, paramVaues);`

**`3`**  `sxmTransactionDelete.commitTransaction ();`

`      }`

`    }`

`  }`

The update operation in the code fragment below will succeed. By the time we get to the `commitTransaction` call on line 1, the read lock acquired by the `sxmTransactionSearch` object will have already been disposed as a result of all rows in the result set having been processed. From a database performance perspective, this is an efficient way of doing this.

 `ArrayList` ` paramVaues =` `new` ` ArrayList();`

 `using` ` (` `SxmTransaction` ` sxmTransactionSearch = ` `new`  `SxmTransaction` ` (` `"jsearch"` `),`

 `sxmTransactionDelete = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

`    sxmTransactionSearch.executeQuery (` `"getAllCompanies"` `, ` `null` `);`

 `while` ` ((company = sxmTransactionSearch.getNextRow ()) != ` `null` `) `

 `if` ` (company [` `"name"` `].Equals(` `""` `) ==` `true` `) `

`      {`

`        paramVaues.Clear ();`

`        paramVaues.Add(company [` `"companyPK"` `]);`

`        sxmTransactionDelete.executeDelete (` `"deleteCompanyReg"` `, paramVaues);`

`      }`

**`1`** `   sxmTransactionDelete.com` `mitTransaction ();`

**`  }`**

The update operation in the code fragment below will also succeed. The records are first read from the result set and placed in a collection before being processed by the `SxmTransactionDelete` object. The read lock is released by the `getAllRows` method on line 1\. Of course, the `SxmTransactionSearch` object is cleaned up when it exits the `using` block. Either of these will dispose of the read lock. If the result set is really huge, consider paginating the search in order to break it down into more manageable chunks.

From a database performance perspective, this is also an efficient way of doing this. In the example above, we maintain two transaction objects simultaneously. In this example, we only have a one transaction object active at any time, but we need to allocate a collection for storing the result set. When comparing the examples, we are trading resource usage needed to support two transaction objects with resource usage needed for the record set collection.

 `ArrayList` ` paramVaues =` `new` ` ArrayList();`

 `using` ` (` `SxmTransaction` ` sxmTransactionSearch = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

  `sxmTransactionSearch.executeQuery (` `"getAllCompanies"` `, ` `null` `);`

**`1`**  `List` `<` `Hashtable` `>` `allRecords = sxmTransactionSearch.getAllRows ();`

**`2`**  `}`

 `using` ` (` `SxmTransaction` ` sxmTransactionDelete = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

  `foreach` ` (` `Hashtable` ` company ` `in` ` allRecords) `

    `if` ` (company [` `"name"` `].Equals(` `""` `) ==` `true` `) `

 `{`

 `paramVaues.Clear ();`

`          paramVaues.Add(company [` `"companyPK"` `]);`

`          sxmTransactionDelete.executeDelete (` `"deleteCompanyReg"` `, paramVaues);`

 `}`

  `sxmTransactionDelete.commitTransaction ();`

`    }`

Now for our final example. I have shown you three ways of processing the output from one transaction as the input to another. One of these was a non-working solution. You might have looked at the solution above and thought there is a better way of doing this, and you would be right. Creating a second `SxmTransaction` object in order to perform the delete was unnecessary.

 `ArrayList` ` paramVaues =` `new` ` ArrayList();`

 `using` ` (` `SxmTransaction` ` sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

  `sxmTransaction.executeQuery (` `"getAllCompanies"` `, ` `null` `);`

 `List` `<` `Hashtable` `>` `allRecords = sxmTransaction.getAllRows ();`

  `foreach` ` (` `Hashtable` ` company ` `in` ` allRecords) `

  `if` ` (company [` `"name"` `].Equals(` `""` `) ==` `true` `) `

 `{`

 `paramVaues.Clear ();`

 `paramVaues.Add(company [` `"companyPK"` `]);`

 `sxmTransaction.executeDelete (` `"deleteCompanyReg"` `, paramVaues);`

 `}`

 `sxmTransaction.commitTransaction ();`

`  }`

The example above works just fine. However, the slightly modified example below will fail. Actually, it won’t fail; it just won’t do what you expect. The `executeDelete` statement will clear the transaction’s data reader, which, in effect, clears the result set. This will cause to code to exit from the while statement. As a result, the delete can only execute a maximum of one time.

 `ArrayList` ` paramVaues =` `new` ` ArrayList();`

 `using` ` (` `SxmTransaction` ` sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

`    sxmTransaction.executeQuery (` `"getAllCompanies"` `, ` `null` `);`

 `while` ` ((company = sxmTransaction.getNextRow ()) != ` `null` `) `

 `if` ` (company [` `"name"` `].Equals(` `""` `) ==` `true` `) `

`      {`

`        paramVaues.Clear ();`

`        paramVaues.Add(company [` `"companyPK"` `]);`

`        sxmTransaction.executeDelete (` `"deleteCompanyReg"` `, paramVaues);`

`      }`

`     sxmTransaction.com` `mitTransaction ();`

`  }`

This probably needs some clarification. Executing a database update operation using an `SxmTransaction` object with an active result set, will cause the data reader for the result set to be closed so that the update can proceed. If the data reader is not closed, the update operation, in this example a delete, will fail with an *InvalidOperationException* ; ”*Cannot set CommandText while data reader is active.* ” A decision was made that it was better to close the data reader and allow the update to proceed rather than to let the update fail. If this does not work for your particular requirements, the workaround is very simple.

*   Either read the entire results set into a collection using the `getAllRows` method and then iterate through the collection. We did this in the second to last example above.
*   Or, use a separate `SxmTransaction` for performing the update.

Below is a list of operations that acquire locks.

*   `excuteInsert :` RESERVED
*   `executeQuery :` READ
*   `executeQueryDirect :` READ
*   `executeUpdate` `  :` RESERVED
*   `executeUpdateDirect` `:` RESERVED
*   `executeDelete :` RESERVED
*   `executeDeleteDirect` `:` RESERVED
*   `commitTransaction :` EXCLUSIVE, then disposes all locks

Serializing transactions using the SxmSTransaction class

In the last section, we explained how the lock state of the database is affected by various operations and how the database uses the lock state for managing concurrency. To reiterate, if your application is guaranteed to only have a single transaction object active at any one time, then issues associated with locking and concurrency can largely be ignored. However, if your app performs database operations on multiple threads, then concurrency is an issue that needs to be considered.

In the ‘Locking and concurrency’ section, we nested transactions in order to artificially create conditions that would cause blocking and, ultimately, some timeouts. This was done, of course, to illustrate how locking and concurrency works. In an actual application, you probably wouldn’t nest transactions. In all likelihood, an app will be executing multiple transactions on different threads. So, how does this difference affect locking and concurrency? It actually works to our favor. When lock contention occurs, for example, when trying to acquire an exclusive lock while there are active read locks, SQLite will block the thread trying to acquire the lock for a period of time while waiting for the lock state to change. If the lock state changes before the timeout period elapses, the blocked operation will be allowed to proceed.

Generally speaking, SQLite provides very good concurrency. Provided you don’t hold on to locks for extended periods of time, timeouts due to locking shouldn’t be a problem. However, timeouts are the extreme condition; you really need to do better than simply not pass a timeout threshold. You should strive to avoid any delays that are likely to annoy users. So, how can we do this?

*   The first rule for successful concurrent database processing is to always strive to minimize the amount of time you spend in the `using` block of an `SxmTransaction` . This is your best, first-line defense against blocking. While it doesn’t eliminate blocking, it helps to reduce it. The more concurrency you require, the more important this rule becomes.

For the majority of applications, it is more critical that database reads proceed unhindered than writes. With the exception of certain operations such as registrations, many write operations can be delayed. For example, when submitting a job posting to a job search site, it’s probably okay if the actual post occurs sometime in the future. What’s the difference whether a job posting appears in the jobs database immediately or within a few seconds? What I am trying to get at, is that in many instances it is perfectly fine to delay inserts. If you “meter” inserts, you will effectively be freeing the database to process other commands. One way to do this is to serialize all transactions that update the database; processing them one at a time. And, as luck would have it, the SQLite.XM library includes a class that performs transaction serialization. The class is `SxmSTransaction` and it inherits from the `SxmTransaction` class. Below is a code fragment from one of our earlier examples rewritten to use the `SxmSTransaction` class.

 `ArrayList` ` paramVaues =` `new` ` ArrayList();`

**`1`** `using` ` (` `SxmTransaction` ` sxmTransaction = ` `new`  **`SxmSTransaction`** ` (` `"jsearch"` `)){`

`    sxmTransaction.executeQuery (` `"getAllCompanies"` `, ` `null` `);`

 `while` ` ((company = sxmTransaction.getNextRow ()) != ` `null` `) `

 `if` ` (company [` `"name"` `].Equals(` `""` `) ==` `true` `) `

`      {`

`        paramVaues.Clear ();`

`        paramVaues.Add(company [` `"companyPK"` `]);`

`        sxmTransaction.executeDelete (` `"deleteCompanyReg"` `, paramVaues);`

`      }`

`     sxmTransaction.commitTransaction ();`

`  }`

The only difference from the earlier example is that an `SxmSTransaction` is instantiated in the `using` block instead of an `SxmTransaction` , see line 1\. Other than this one minor difference, everything else remains the same. The default behavior for the `SxmSTransaction` class is to block indefinitely waiting for its turn to execute. You can modify this behavior by including a milliseconds timeout value in the call to the constructor; see below.

`SxmTransaction` ` sxmTransaction = ` `new`  `SxmSTransaction` ` (` `"jsearch", 10000` `)`

In the line above, the `SxmSTransaction` constructor will wait 10 seconds before throwing an `sxmSTransactionTimeout` `SxmException` . The `SxmSTransaction` class will serialize any transaction, not just transactions that update the database. A fair question would be; do I really need to go through all this trouble? If you do not execute a lot of concurrent writes transactions and don’t hold onto read locks for long periods of time, then I would say no. You can just let the database block any operations as needed until the lock state changes and the blocked operations are permitted to proceed. However, if you perform numerous concurrent write transactions mixed with database reads that must be serviced quickly, then you might consider this strategy.

If you do decide to delay write operations, you should perform them on a worker thread not the UI thread. The reason for this is pretty obvious. It makes little sense to serialize some transactions in order to free the processor to perform other work and then block the user interface waiting on the serialized transactions.

Dynamic Queries

Up to this point, all of our queries have been statically defined in the SQL statements properties file.  By static, I am referring to parameterized queries where only the user supplied data in the query changes; the logic of the query remains constant. Many applications require that some of their queries be more flexibility. These apps need to be able to create queries on-the-fly where the query logic can differ in ways that may not be known in advance. These are often referred to as dynamic or ah-hoc queries. I classify two levels of dynamic queries.

*   Fully dynamic. These are queries that are fully assembled in code.
*   Partial dynamic. These are queries that are partially static and partially dynamic.

Let’s take a look at these individually.

Fully dynamic queries are normally used for searches where the combination of search constraints is not known in advance. For example, imagine you visit a real estate Web site that allows you to search for a home based on several dozen user selectable criteria, such as

*   Sq. footage
*   Number of  bathrooms
*   Number of bedrooms
*   Pool
*   etc…

The problem with trying to create a static query to satisfy such a search, is that you do not know in advance the combination of criteria any particular user is going to select. The way this is handled is to allow users to select the constraints that they wish to search and then to dynamically build a query to satisfy their selections. As you can imagine, this can get somewhat complex. And, to make matters worse, there is an issue with indexes. I am not going to get into this in detail, but the order in which fields are defined in a compound index affects its usability for any particular query. It’s not realistic to formulate indexes for all possible query combinations for a fully dynamic query. In order to solve this problem, you need to apply some crafty schema definition techniques to the table being queried. Processing of fully dynamic queries is beyond the scope of this book. So I don’t go into them in any additional detail.

Partially dynamic queries are queries where only part of the query logic is dynamically constructed. These queries are mostly static with select portions that are variable. First, I should probably explain why you would even need partially dynamic queries. Imagine your app includes a search that could return several thousand records. You would not want to let such a query execute without some constraint on the number of selected records. What you want to do is to paginate the search results. That is, return the records in some limited way, for example, 20 per page. To do this, your query needs to include a LIMIT and OFFSET clause. These SQL constructs tell the database how many records to select and from where in the record set to start selecting. Below is a rewritten version of our job selection query.

`SELECT * FROM jobPosting WHERE companyRegFK = ? LIMIT n OFFSET m`

In order to select the first 20 records, the statement would be: 

`SELECT * FROM jobPosting WHERE companyRegFK = ? LIMIT 20 OFFSET 0`

To select the next 20 records:

`SELECT * FROM jobPosting WHERE companyRegFK = ? LIMIT 20 OFFSET 20`

As you can see, the offset value needs to change in order to paginate the search results. In this example, we set the record read limit to 20 records. But this could also be a variable, for example, if you allow the number of returned records to be user selectable.

Let’s take a look at another example. Imagine we want to include the following query as part of our job search application.

`SELECT * FROM jobPosting WHERE companyRegFK IN (?)`

The problem with this query as it is written, is that you cannot parameterize an IN clause for a variable number of criterion. In order for this query to work for more than a single input parameter, it will need to be modified dynamically.

Let’s rewrite our job select query from earlier to include an IN clause and a limit/offset. Below is our new query as it appears in the SQL statements properties file. This query is intended to selects all jobs posted by all companies.

`[getAllCompanyJobs]` 

`[SELECT * FROM jobPosting WHERE companyRegFK IN ({0}) LIMIT {1} OFFSET {2}]`

There are actually two ways you can dynamically modify this query.

*   For each search parameter, insert a placeholder in the IN clause.
*   Insert the actual search parameters in the IN clause.

I’ll provide an example for each of these options, but I can tell you, the first option is your better choice. Here’s why:

*   It is much easier to send query parameters to a query rather than trying to construct a query string.
*   Sticking with parameterized queries keeps your code consistent whether using static or partially dynamic queries. 
*   Parameterized queries are much less prone to SQL injection attacks. When used correctly, they are probably immune to this sort of attack.

Using parameterized placeholders

Let’s start with inserting placeholders for the search parameters. For this search, we will be inserting a placeholder for each primary key value that is passed as a query parameter. Below is a screenshot of the administrators get jobs search page.

![](Image00016.jpg)

The `OnCreate` method for this activity is pretty basic. The method `getAllCompaniesPK` , which is called on line 1, performs a search of the company registration table, retrieving the primary key values for each registration.

 `private`  `static`  `int` ` pageNumber;`

 `private`  `static`  `int` ` recordCount = ` `10` `;`

`  protected`  `override`  `void` ` OnCreate (` `Bundle` ` bundle)`

`  {`

`    pageNumber = ` `0`

 `base` `.OnCreate (bundle);`

`    SetContentView (` `Resource` `.` `Layout` `.AdminGetAllJobs);`

**`1`**  `ArrayList` ` companiesList = getAllCompaniesPK (); `

 `Button` ` cancelGetAllJobsButton = ` `null` `;`

`    cancelGetAllJobsButton = FindViewById<` `Button` `> (` `Resource` `.` `Id` `.cancelGetAllJobsButton);`

`    cancelGetAllJobsButton.Click += ` `delegate` ` { finishActivity (); };`

 `Button` ` getJobsNextButton = FindViewById<` `Button` `> (` `Resource` `.` `Id` `.getJobsNextButton);`

**`2`** `   getJobsNextButton.Click += ` `delegate` ` { GetJobs (companiesList); ++pageNumber;};`

 `Button` ` getJobsPreviousButton = FindViewById<` `Button` `> (` `Resource` `.` `Id` `.getJobsPreviousButton);`

**`3`** `   getJobsPreviousButton.Click += ` `delegate` ` { if(pageNumber > ` `0` `) --pageNumber;`

`                                              GetJobs (` `companiesList); };`

`  }`

These values are placed in an array list. The select statement used for this search is shown below. For brevity, the `getAllCompaniesPK` method is not shown.

`[getAllCompaniesPK] [SELECT companyRegPK FROM companyReg]`

When the *Next Jobs* button is selected, a call to `GetJobs` is made from line 2 followed by an increment of the `pageNumber` parameter. When the *Previous Jobs* button is selected, the `pageNumber` parameter is decremented and a call to `GetJobs` is made from line 3\. The `GetJobs` method is shown below.

 `private`  `void` ` GetJobs (` `ArrayList` ` companiesList)`

`  {`

 `int` `recordCount =` `10` `;`

 `SxmTransaction` ` sxmTransaction = ` `null` `;`

**`1`**  `string` ` [] paramPlaceHolders = ` `Enumerable` `.Repeat<` `string` `>(` `"?"` `, `

 `companiesList.Count).ToArray();`

**`2`**  `string` ` csvParamPlaceHolders = ` `string` `.Join (` `","` `, paramPlaceHolders); `

 `try`

`    {      `

**`3`**  `string` `rawSelect =` `SqlStatements` `.selectStatements [` `"getAllCompanyJobs"` `];`

**`4`**  `string` ` selectStatement = ` `String` `.Format (rawSelect, ` **`csvParamPlaceHolders,`**

 **`recordCount`** `, ` **`recordCount*pageNumber`** `);`

 `using` ` (` `SxmTransaction` `sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

**`5`**   `sxmTransaction.executeQueryDirect (selectStatement, companiesList);`

  `BuildTableInline (sxmTransaction);   `

`      }` 

 `}`

 `catch` ` (` `Exception` ` ex)`

`    {`

 *`// Exception processing here.`*

`    }`

`  }`

This method retrieves records from the job postings database. The select statement for this query as it appears in the SQL statements properties file is shown below.

`[getAllCompanyJobs]`

`[SELECT * FROM jobPosting WHERE companyRegFK IN ({0}) LIMIT {1} OFFSET {2}]`

As you can see, the query string is designed to be processed by `String.Format` . The string includes three format items. The first, {0}, is where the query parameter placeholders will go. The other two format items are where the limit and offset values go. The placeholder string is constructed on lines 1 and 2.

On line 3, the unprocessed query string is retrieved from the SQL statements properties file. This is passed to the `String.Format` method on line 4, where the format items are replaced with their respective values. A fully constructed query string that is ready to execute is returned.

The `recordCount` and `pageNumber` variables are used to control the limit and offset for the search. `recordCount` is hard coded to 10 and never changes. However, the page number is incremented or decremented based on whether the next or previous button is selected. On line 5, the actual call is made to execute the query. Normally, you would call `executeQuery` , passing in the name of the query in the SQL statements properties file that you wish to execute. However, in this example, we dynamically constructed our query so we will be calling the `executeQueryDirect` method instead, passing in the fully constructed SQL statement. The method `executeQuery` should be used whenever executing a static select statement. The method `executeQueryDirect` is used when executing a dynamic query.

SQL Injection dangers

In this example, I did something that I warned you earlier not to do, which is: modify a SQL statement by directly editing the SQL string. I am not talking about the placeholders that we inserted, that was safe. I am referring to the query control values of the limit and offset clause. However small this change, it represents an alteration to the SQL string in a potentially unsafe manner. In this case, I allow the exception for two reasons:

*   In our example, the offset number supplied to the offset clause is not an input that is taken directly from the user. It is calculated in code based on whether the previous or next button is selected. Therefore, with proper bounds checking, the possibility of using an errant, or to be more accurate, malicious input is very low.
*   The inputs are very easy to accurately validate. Only a number should be supplied to the limit and offset clauses.

But don’t get too comfortable with this and repeat this in other ways without really thinking things through. Let me go through an example to show how this seemingly simple alteration can run afoul. Below is our query string from earlier. It is rewritten with the limit hard coded to 10, of course, the offset is still dynamic.

`SELECT * FROM jobPosting WHERE companyRegFK IN ({0}) LIMIT 10 OFFSET {1}`

Now, for this example, assume the offset value is a user supplied input and that there is an error in our code with validation. Further, assume a malicious user supplies the following offset value.

 `1;DROP TABLE jobPosting`

When we construct our query, the final query string will look something like.

 `SELECT * FROM jobPosting WHERE companyRegFK IN (?) `

 `LIMIT 10 OFFSET ` `1;DROP TABLE jobPosting`

You can probably guess what will happen when we execute this nifty little bit of SQL; the entire `jobPosting` table will be deleted. So, as you can see, things can get ugly very easily when dynamically constructing queries.

As an alternative to setting query control values directly using `String.Format` , you could use parameterized values. To do this, you would append the limit and offset onto the parameter array that is passed to the `executeQueryDirect` method. However, you would first need to change the query to the following.

`[getAllCompanyJobs]`

`[SELECT * FROM jobPosting WHERE companyRegFK IN ({0}) LIMIT ? OFFSET ?]`

The `String.Format` statement would be modified to the following.

`string` ` selectStatement = ` `String` `.Format (rawSelect,` **`csvParamPlaceHolders`** `);`

Finally, you would need to append the limit and offset values to the parameter array list.

**`companyList.Add(recordCount);`**

**`companyList.Add(recordCount*pageNumber);`**

I didn’t use this approach for our example for the reasons I stated earlier; I felt the way in which we were modifying the query was safe. That being said, there are many circumstances where this is the preferred solution. The general rules that I follow are:

*   Ask yourself: Can the insertion values easily and accurately be validated? If the answer is yes, as in our example, then you can consider further whether it is appropriate to modify the query control values directly.
*   If you are taking SQL inputs directly from users of your app, be very suspicious of any answer to the question above other than NO!
*   If you are altering the SQL string with anything that could be misidentified as “safe”, then modify the query using the parameterized method. It’s much more secure.
*   If in doubt, use the parameterized method.

Directly inserting query parameters

Now that we’ve shown how to modify a query using parameterized placeholders, let’s have a look at how we would modify a query by inserting the search parameters directly into the query string.

A new listing of the `GetJobs` method is shown below. Instead of constructing a placeholder string as in our earlier example, it builds an actual parameter string; see lines 1 thru 3\. This parameter string is then inserted into the query string on line 4.

`private`  `void` ` GetJobs (` `ArrayList` ` companiesList)`

`{`

 `SxmTransaction` ` sxmTransaction = ` `null` `;`

**`1`**  `for` `(` `int` `i=0; i< companiesList.Count; i++)`

**`2`** `   companiesList [i] =` `"’"` `+ companiesList [i] +` `"’"` `;`

**`3`**  `string` ` paramString = ` `string` `.Join (` `","` `, ` `(` `string` `[])` `companiesList` `.ToArray(typeof(` `string` `))` `); `

 `try`

`   {      `

 `string` `rawSelect =` `SqlStatements` `.selectStatements [` `"getAllCompanyJobs"` `];`

**`4`**  `string` ` selectStatement = ` `String` `.Format (rawSelect, paramString` **`,`**

`                                            recordCount, recordCount*pageNumber);`

 `using` ` (` `SxmTransaction` `sxmTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `)){`

  `sxmTransaction.executeQueryDirect (selectStatement, ` `null` `);`

`       BuildTableInline (sxmTransaction);   `

`     }` 

`  }`

 `catch` ` (` `Exception` ` ex)`

`   {`

 *`// Exception processing here.`*

`  }`

`}`

I do not recommend using this approach for constructing a query unless you have some compelling reason. This method can create real security problems in all but the simplest cases. If you have any doubt about this, go back and reread the section on SQL injection dangers.

Making schema changes

It’s inevitable that you are going to need to make schema changes between releases of your app. With SQLite, there are four types of changes that can be made to a schema:

*   Creating new tables
*   Updating existing tables with a new fields
*   Creating/deleting indexes
*   Dropping tables

There are conceivable other changes that you might make, however, the alter table statement in SQLite supports a limited subset of commands. So modifying a table beyond what is supported would require you to engineer a solution of your own. Index definitions are not supported by the SQLite create table statement, as these are managed independently.

Adding/Modifying tables

Adding a new table is easy, you simply include a new create table statement in the `TABLE` section of the SQL statements properties file. What happens when you need to make a change to an existing table? In this case, you need to create the table for new users and modify the table for existing users. These are inherently different operations. Let’s go through an example.

Imagine that the first release of your application includes a create table statement like the one below.

`CREATE TABLE companyReg (id INTEGER PRIMARY KEY AUTOINCREMENT, `

`companyRegPK TEXT, coName TEXT, hrContact TEXT, email TEXT, password TEXT)`

This is simple enough, it creates a company registration table that includes a few basic fields. Now imagine that in the next version of your application you decide to include the name of the CEO in the registration table. The new create table statement is shown below.

`CREATE TABLE companyReg (id INTEGER PRIMARY KEY AUTOINCREMENT, `

`companyRegPK TEXT, coName TEXT, hrContact TEXT, email TEXT,`

`password TEXT, ceo TEXT)`

Alright, the new statement is the same as the old one with the addition of the CEO field. For new users installing your app, everything seems just fine, but what about existing users that are upgrading to the new release? The way SQLite.XM works, is it only executes a create table statement if the table being created doesn’t already exist in the database. If it does, the statement is skipped. What you need to do is include an alter table statement in the ALTER section of the SQL statements properties file that adds the new field to the table. SQLite.XM will only execute alter table statements against tables that already exist in the database. So, the rules for creating and altering tables are as follows:

*   A create table statement will execute only if the table being created does not already exist in the database, otherwise the statement is skipped.
*   An alter table statement will execute only if the table that it alters already exists in the database, otherwise the statement is skipped.
*   An alter statement will only execute if the field being added to the table doesn’t already exist.

Given these rules, the proper way to modify our company registration table is to include both a create table statement and an alter table statement in the SQL statements properties file. Depending on whether a user is installing for the first time or upgrading an existing installation, only one of the statements will execute. The two example statements are shown below.

`[TABLE]`

`CREATE TABLE companyReg (id INTEGER PRIMARY KEY AUTOINCREMENT, `

`companyRegPK TEXT, coName TEXT, hrContact TEXT, email TEXT,`

`password TEXT, ceo TEXT)`

`[]`

`[ALTER]`

`[jsearch.companyReg][ceo][ALTER TABLE companyReg ADD ceo TEXT]`

`[]`

The create table statements for each new version of your app should create tables as they are required by the newest version. You should also include all of the alter table statements needed in order to upgrade tables from your apps first release to the latest. Do not remove alter statements between releases of your app, otherwise updates may not correctly apply. For users that are upgrading, SQLite.XM will execute the alter table statements needed in order to upgrade tables from their current state to the latest version. For new users, only the create table statement will be executed.

An alter table statement that adds a field is only executed if the table does not already include the field. For each table in your database, a single query is made to get the names of the existing fields.  Fields being added by alter table commands are compared to this list and those that already exist are skipped.

This entire discussion sidesteps the issue of deleting fields from a table or making other more complex structural changes. Unfortunately, SQLite does not support these operations. If you have a field you no longer need, I suggest you simply remove all of the field data from the table rather than going through the pain of simulating a drop column statement. Unless you have a good reason to do otherwise, it’s probably better to just carry around the unneeded field. If you must make unsupported table changes, you will need to perform them manually. You can create a new table and then manually copy the data from the old table to the new one performing the translation in code. This solution has potential problems, especially when dealing with large data sets.

Creating/Deleting indexes

Table indexes can be changed in the following ways:

*   Drop an existing index
*   Create a new index

That’s about it, there is no way to modify an existing index. If you have an index that you wish to change, the process is to first delete the index and then recreate it with the new structure using a new index name. As I mentioned earlier, create index and drop index statements go in the `INDEX` section of the SQL statements properties file. The statements can appear in any order.

Let’s have a look at how we would update indexes for new releases of an app. It’s very likely that the first revision of your app will include at least some indexes, although this is not a requirement. However, for the purposes of our example, we are going to assume our app shipped with two index definitions. Below is the `INDEX` section of the SQL statements properties file for our example.

`[INDEX]`

`[jsearch.companyReg][coRegNameIDX]`

`[CREATE INDEX coRegNameIDX ON companyReg (coName)]`

`[jsearch.jobPosting][jobTtileIDX]`

`[CREATE INDEX jobTtileIDX ON jobPosting (jobTitle)]`

`[]`

We have two indexes, one on the `companyReg` table and one on the `jobPosting` table. Now, imagine that for our next release we decide that the `jobTitleIDX` index needs to change so that it includes the `pay` field. Also, we want to create a new index on the job seeker registration table. Below is our modified SQL statements `INDEX` section.

`[INDEX]`

`[jsearch.companyReg][coRegNameIDX]`

`[CREATE INDEX coRegNameIDX ON companyReg (coName)]`

`[jsearch.jobPosting][jobTtileIDX]`

`[CREATE INDEX jobTtileIDX ON jobPosting (jobTitle)]`

**`[jsearch.jobPosting][jobTtileIDX]`**

**`[DROP INDEX jobTtileIDX]`**

**`[jsearch.jobPosting][jobTtilePayIDX]`**

**`[CREATE INDEX jobTtilePayIDX ON jobPosting (jobTitle, pay)]`**

**`[jsearch.seekerReg][seekerNameIDX]`**

**`[CREATE INDEX seekerNameIDX ON seekerReg (fName, lName)]`**

`[]`

The new entries in the table are highlighted in bold. We now have three active indexes: `coRegNameIDX` , `jobTitlePayIDX` , and `seekerNameIDX` . The `jobTitleIDX` index that was part of our apps first release, has been dropped. The drop statement could have appeared anywhere, it just happens that I placed it right after the corresponding create statement. SQLite.XM applies the following rules when processing the `INDEX` section of the SQL statements file.

*   The create table statements in the `TABLE` section of the SQL statements properties file execute before any statements in the `INDEX` section.
*   The alter table statements in the `ALTER` section of the SQL statements properties file also execute before any statements in the `INDEX` section.
*   An alter statement will only execute if the field being added to the table doesn’t already exist.
*   A create index statement is only executed if the index does not already exist AND there is no drop index statement present for the index.
*   A drop index statement will only execute if the index exists.

Do not remove index statements between releases of your app, otherwise updates may not correctly apply. Once an index has been dropped, you cannot reuse the dropped index name again. If you drop an index, be mindful to modify any SQL statements that use the INDEXED BY clause on the dropped index. The INDEXED BY phrase forces the SQLite query planner to use a particular named index on a DELETE, SELECT, or UPDATE statement.

Dropping tables

To drop a table, do the following.

*   Replace the create table statement in the TABLE section of the SQL statements properties with a drop table statement.
*   Remove all statements in the `ALTER` and `INDEX` sections of the SQL statements properties file that reference the table you wish to delete.

That’s about it. Do not remove drop table statements between releases of your app, otherwise updates may not correctly apply.

The SxmConnection class

As an alternative to having the `SxmTransaction` class mange connections, you can create and manage connections directly using the `SxmConnection` class. However, before I show you how this is done, let’s take a moment to look at the design of this class.

If you take a look at the `SxmConnection` code you will notice that it does not inherit from the `SqliteConnection` class. This is a bit strange, as it would be reasonable to consider the `SxmConnection` to be a specialization of the `SqliteConnection` . It turns out the `SqliteConnection` class is sealed and therefore cannot be used as a base class. I am not sure why this was done that way but it leaves us with few options except to have the `SxmConnection` class contain a `SqliteConnection` object. This works just fine but it would seem a more appropriate to use inheritance rather than containment.

The `SxmConnection` class does quite a bit more than simply establish a connection. It acts as a wrapper around all things related to processing database SQL commands. For example, it maintains the connection command object, includes a data reader for accessing record data from the last query and it manages error logging. It is also responsible for some resource management. As you would expect, this all has advantages and disadvantages. The `SxmConnection` class is very easy to use and removes much of the burden associated with dealing with the database. However, it is a bit less flexible than managing a connection directly using custom code. The compromises are relatively minor. The main issue is the `SxmConnection` class only maintains a single command object, as a result, it only supports a single data reader. What this means is, only the record data from the last executed query is accessible. This is generally not an issue as you are normally only interested in reading the results from the last query. If you need access to the result set of multiple queries simultaneously, the workaround is very easy, you simply create multiple connection objects or you pull the data from the first query out of the record set and into a collection and then issue a second query on the same connection.

Creating an SxmConnection

Creating a connection is very easy, you simply instantiate an `SxmConnection` object.

`SxmConnection` `Conn = ` `new`  `SxmConnection` `(` `"jsearch"` `);`

The `SxmConnection` constructor takes one required parameter, the name of database for which you wish to establish a connection. It’s safe to create multiple connections to the same database. In fact, it’s one of the strategies you can use in order to allow multiple threads to access the same database. You do not need to synchronize the creation of connection objects, even when connecting to the same database. As a convenience, you can omit the database name parameter provided your app only uses one database, i.e., only defines one database descriptor. In this case, the constructor would be written as:

`SxmConnection` `Conn = ` `new`  `SxmConnection` ` ();`

There is one interesting thing to note regarding the creation of connections. Before instantiating a connection, you can modify the database descriptor associated with the database you wish to connect. This allows you to alter descriptor details when connecting to the same database multiple times. Let’s have a look at an example.

 `try`

`  {`

**`1`**  `new`  `DatabaseDescriptor` `(` `"jsearch"` `);`

 *`// For Android apps.`*

 `using` ` (` `StreamReader` ` sr = ` `new`  `StreamReader` ` (Assets.Open(` `"SqlStatements.txt"` `))){` 

 *`// For iOS apps.`*

 `using` ` (` `StreamReader` ` sr = ` `new`  `StreamReader` ` (` `”sqlProperties/SqlStatements.txt"` `)){`

 `ProcessSQLStatements` `.Parse (sr);`

`   }`

 `SxmInit.` `initialize ();`

**`2`**  `SxmConnection` `conn1 = ` `new`  `SxmConnection` `(` `"jsearch"` `);`

 `}`

The code snippet above initializes the database *jsearch* . The database descriptor that is instantiated on line 1 uses the descriptors default settings. This means that the error log is going to be named *jsearch* . On line 2, a connection to the database is established. The connection, `conn1` , is going to log all errors to *jsearch.log* . Now have a look at the code snippet below.

 `DatabaseDescriptor` `jsearchDD =` `null` `;`

 `try`

`  {`

**`1`** `   jsearchDD =` `DatabaseDescriptor` `.getDescriptor (` `"jsearch"` `);`

`    if (` `jsearchDD != null )`

`    {`

**`2`**  `jsearchDD` `.lockDescriptor ();`

**`3`**  `jsearchDD.logfileName =` `"jsearch-log1";`

**`4`**   `jsearchDD.logfileMaxSize = 1024 * 1024 * 5` `;`

**`5`**   `SxmConnection` `conn2 = ` `new`  `SxmConnection` `(` `"jsearch"` `);`

`    }`

`  }`

`  finally`

`  {`

 `if (` `jsearchDD != null )`

**`6`**  `jsearchDD` `.unlockDescriptor ();`

`  }`

On line 1, we get the descriptor associated with the *jsearch* database that we initialized earlier. Then, on line 3, we change the name of the log file to *jsearch-log* . We also changed the maximum size of the log file to 5 MB, this is done on line 4\. On line 5, a connection to the database is established. The connection, `conn2` , is going to log all errors to *jsearch-log.log* . The log file will be allowed to grow to a maximum size of 5 MB.

These two connections, `conn1` and `conn2` , can be used simultaneously with each one logging errors to a different error log.

Looking at the code above, you will see we lock and unlock the database descriptor on lines 2 and 6 respectively. This is to ensure that while we are creating the new connection with the modified settings, no other thread will sneak in and make unexpected changes to the descriptor. You won’t need to do this if you do all of your database work on a single thread. Also, you don’t need to lock a database descriptor simply to instantiate an `SxmConnection` object, unless, of course, you code is designed in such a way that the descriptor could be modified by another thread. Changing a descriptor for a particular connection is a bit unusual anyway. You normally just create a database descriptor and leave it alone. Another thing to keep in mind, is that changes made to a descriptor remain in effect for all future `SxmConnection` objects.

Using an SxmConnection

Once a connection object has been created, it can be used by an `SxmTransaction` . Below is one of our earlier examples modified so that the `SxmTransaction` is instantiated with an `SxmConnection` .

 `private`  `void` ` processSubmitHandler (SxmConnection sxmConnection)`

`  {`

 `ArrayList` ` parameterValues = ` `new`  `ArrayList` ` ();`

 `string` ` registrationPK = ` `Guid` `.NewGuid ().ToString ();`

`   parameterValues.Add (registrationPK);`

`   parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegName).Text);`

`   parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegContact).Text);`

 `parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegEmail).Text);`

`   parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegPassword).Text);`

**`1`**  `using` `(` `SxmTransaction` ` sxmTransaction = ` `new`  `SxmTransaction` ` (sxmConnection)){`

 `InsertResponse` ` ir = sxmTransaction.executeInsert(` `"registerCompany"` `, `

`                                                        parameterValues);`

 `if` `(sxmTransaction.commitTransaction () !=` `SQLiteErrorCode` `.Ok` `)`

 `throw`  `new`  `SxmException` ` ( ` `new`  `ErrorMessage` ` (` `"Commit error."` `, `

 `Defines` `.` `SxmErrorCode` `.userDefined));`

`    }`

`  }`

You have seen this method before, so I’m not going to go through it in detail. However, I would like to point out the `using` statement on line 1\. The `SxmTransaction` constructor takes an instance of an `SxmConnection` as its only parameter. In all of our earlier examples, an `SxmTransaction` object was created using the name of the database. This difference has no effect on its usage. Once created, the `SxmTransaction` object behaves exactly as previously explained. Upon exiting the `using` block, the `SxmTransaction` will no longer be useable. However, the `SxmConnection` object will still be active and available for further use by other transactions.

A connection object cannot be used by multiple transactions at the same time. If you try to use a connection while it is attached to a transaction, it will throw a `lockDB SxmException` . You can safely pass a connection object to another thread as long as it is not currently in use by an `SxmTransaction` .

When you are finished with a connection, call the `destroyConection` method. Once called, the connection object will no longer be useable.

Part 3\. Data synchronization to the cloud

Before getting too far into this, we should probably first understand what it is we are trying to do. Our goal with cloud synchronization is to either copy or move the record data from the local SQLite database to a server side datastore; presumably this is an enterprise database server, but there is no requirement imposed by SQLite.XM that this is the case. SQLite.XM comes out of the box ready to work with HotRiot.com, which uses both MySQL and MongoDB for its datastore. However, SQLite.XM can work with any back-end database or middleware of your choosing. I’ll show you how this is done a bit later, but it essentially entails writing a custom delegate method that is inserted into the synchronization processing chain. When present, your delegate will be called on to transfer record data from the device to wherever it is you wish it to be saved. This transfer can be done in any manner and to any server of your choosing. You have complete flexibility. We will get into this later. Most of the remainder of this part of the book is dedicated to using the built-in HotRiot synchronization.

The graphic below depicts how data is aggregated to from the individual devices to the cloud server. 

![](Image00010.jpg)

This is a one way process that is ongoing and asynchronous. By that I mean, each device synchronizes independent of all other devices; there is no coordination between devices and there are no prescribed times for synchronization.

Let me make a few comments regarding the term synchronization. Some might object to my using this term, as synchronization strongly implies two or more copies of data that are being kept up-to date or in synch. This is not what we are doing, we are copying data from the devices to a central database server. This activity might better be described as replication. But even that term doesn’t exactly fit, as there is no requirement to truly replicate. SQLite.XM is perfectly happy to allow you to perform a transform on the source data before moving it up to the server. Not only that, the server side datastore can be a completely different storage technology from that used by the local device, SQLite.XM doesn’t care. The whole activity might be more accurately described as an ETL (Extract, Transform, Load) process, but that just depends on how it is implemented. So we just settled on the term synchronization. For those that disagree, I would ask for some wiggle room. Also, I use the term synchronization and replication interchangeable.

Understanding SQLite.XM synchronization

Generally speaking, there are two methods for performing database synchronization

*   Statement based synchronization (SBS)
*   Row based synchronization (RBS).

With SBS, the SQL statements that are executed on the source database are copied and executed on the destination database. With RBS, the actual record data is copied from the source to the destination database. SQLite.XM uses RBS. Each method has advantages and disadvantages, however due to the nature of synchronization with SQLite.XM, SBS is just not practical. SBS is difficult enough to successfully perform using identical versions of the same database. It is simply unrealistic to expect to use SBS between heterogeneous database technologies, which is permitted by SQLite.XM. Not only that, SQLite.XM synchronization allows for transforming of the source data before propagating it to the server. In this case, SBS really has no meaning.

Normally with RBS, the modified record data is copied to a synchronization log where it is held temporarily until it is moved to the target datastore. Each new insert or record update results in a new entry in the log. As you can imagine, depending the velocity of the inserts and/or updates and the frequency with which data is synchronized, you could wind up a very large log file. This is also a bit complicated to implement as the integrity of the synchronization log file must be assured as part of every transaction. This can get quite involved and it can be very difficult to create a reliable solution when managing the log from outside the actual database.

SQLite.XM uses a slightly different approach to RBS that works just fine for the vast majority of applications. That being said, it’s important for you to understand the details in order for you to make a decision as to whether it is appropriate for your particular app. SQLite.XM does not maintain a synchronization log in the traditional sense. While a log does exist, the log only includes the replication key for the records that needs to be synchronized. The key is used to query the record in order to send the entire record data as part of the synchronization operation. As you might expect, this has advantages and disadvantages.

The log is populated as part of the normal insert, update, and delete transaction processing performed by SQLite. This is part of the ACID compliance that is enforced by SQLite. This helps to ensure the integrity of the replication log. Therefore, if a record is successfully inserted, updated, or deleted, we can be certain that a corresponding entry into the replication log will also be properly made.  Conversely, if a database insert, update, or delete should fail, we can be sure that no entry will be inserted into the replication log. This is important, as proper synchronization starts with a replication log that accurately reflects database activity.

SQLite.XM queries entries in the replication log in the order in which they are inserted; First In First Out (FIFO). The replication key from each log entry is used to query the record referenced by the entry.  The entire record data is then sent to the replication server, where a new entry is made in the database or the existing record is updated or deleted. SQLite.XM does not track the individual fields modified by an update, it simply updates the entire record with the current record data. This greatly simplifies the synchronization process, which helps to make it more reliable. However, it has the side effect of potentially increasing network traffic over what would be needed if synchronization only updated modified fields. If your app performs many partial modifications to existing records, this could represent a significant increase over what is actually required. Of course, this depends on the particulars of you application.

The other issue to be aware of, is that fields in a record can be synchronized earlier in the replication process than when they were actually modified. The results of this are no different from what you could get with a traditional statement or row based replication. Let’s go through an example.

![](Image00028.jpg)

The table above represents a replication log with four entries. The synchronization ID is the link to the actual record in the database. As you can see, there are two entries in the table for record 2764\. Assume for this discussion that the widget table has 7 fields. Further, assume that two of the fields in record 2764 were updated by log entry 167 and three other fields in the same record were updated by entry 169\. As I stated earlier, the replication log entries are processed sequentially in FIFO order. So, the first entry to be processed will be log record 167\. When log entry 167 is processed, all of the fields for the associated record will be synchronized, that includes the two fields updated by log entry 167 and the three fields updated by log entry 169.

This does not generally present a problem, however, there are times where it can introduce side affects you need to be aware of. Consider the following set of circumstances:

*   The record update referenced by log entry 169 included an ID pointer to the record inserted into the *project* table by log entry 170. Imagine this is a GUID foreign key field.
*   Because of a network failure, synchronization was interrupted after successfully synchronizing entry 167.

Because of the network interruption, the record represented by synchronization ID 2764 on the server will include a foreign key to a record in the *project* table which has not yet been synchronized; i.e., the record does not yet exist on the server. Now, this is no different from what you would get with traditional RBR or SBR if synchronization failed on log entry 170, it just has the potential to happen earlier in the synchronization cycle.  Normally all you need to do is to design the code that accesses the data on the server to handle these conditions, which you should be doing anyway.

Another issue to be aware of with early field replication is with counters. If entry 169 included an update to a counter field, that update would appear on the server when log entry 167 is synchronized. However, even these types of inconsistencies are rarely show stoppers. Synchronization in SQLite.XM is event driven, when an entry is made to the local database, synchronization is immediately triggered. This helps to maintain consistency between the local store and the remote server. Of course, this provides no guarantee; for example, your app could be making modifications to the local database while there is an extended network outage. In which case, synchronization will have to wait until connectivity is reestablished. But when it is, all records in the replication log will get synchronized fairly quickly, sans some other problem.

Depending on the particulars of you application, there may be other issues you need to be cognizant of when dealing with replication. When thinking this through, keep in mind that a record is synchronized in its entirety when the first replication log entry for the record is processed.

Setting-up a server-side infrastructure

We need to set-up our server side infrastructure before we can begin replicating. SQLite.XM comes out of the box ready to work with HotRiot.com. But it’s not required that you use HotRiot for replication. SQLite.XM replication can be made to work with any server side datastore of your choosing. I’ll show you how this is done a bit later. The real difficulty with synchronizing with your own server, is in writing the code that performs the actual work of moving the data over the wire to the server. This can get a bit complicated, especially if you need support for document storage. Fortunately, all of that code has already been written for HotRiot and is included as part of SQLite.XM.

At this point, you might be asking why HotRiot? The answer is simple, and comes in three parts:

*   HotRiot is perfectly suited to this task. It provides a robust server-side platform for mobile applications. It includes a provisioned relational and NoSQL database, rich document support, push notifications, proximity searching and a whole lot more.
*   HotRiot includes a comprehensive C# API designed to work with Xamarin.
*   I was one of the lead developers on HotRiot, so it’s natural for me to use the service I know best.

But again, and I want to reiterate, you don’t have to use HotRiot in order to use SQLite.XM synchronization. Although you will need to write the supporting code, you’re free to use any back-end of your choosing. As another option, you can start your development using HotRiot and then switch over to your own cloud server later. This provides a path of least resistance during the development phase. HotRiot provides a no credit card signup and is free to use for 30 days. And if you need more time, the cost to use HotRiot during development is nominal. Most apps can be developed on HotRiot for a grand total of $15\. So you have plenty of time to perform a switch-over to your own server-side infrastructure without spending a whole lot of money.

Let me say one other thing regarding HotRiot. HotRiot is a very comprehensive product that does a lot. I only cover what’s needed in order to support data synchronization from SQLite.XM.

Creating the replication database tables

As stated earlier, before we can begin replicating, we need to set-up the server side datastore. We need to create our cloud database along with the tables that will be used for replication. Fortunately, with HotRiot this is a breeze. You build and manage your application's infrastructure using graphical tools from within the HotRiot Web application. HotRiot includes fairly comprehensive documentation, so I’m not going to attempt to duplicate it here. However, I will provide clarification when I believe it will be helpful.

Start by going to *HotRiot.com* and create a new account. Upon registering, you will be forwarded to your applications *Main Console* page. Please see the screenshot below.

![](Image00030.jpg)

Your new HotRiot account comes with a provisioned MySQL and MongoDB database. This is done for you automatically. All you need to do is to create the tables that will be used for replication. Earlier, in the section ‘Defining table statements’, I showed you how to create table definition entries for the SQL statements properties file. As a reminder, each create table statement is composed of three fields.

`[` *`database_name`* ***`.`*** *`table_name`* `] [` *`create/drop table statement`* `] [` *`synch_key`* `]`

The last field, the synch key, controls if/how a table is synched to the cloud. There are currently three options.

*   **no_synch** : Do not synchronize the table data.
*   **synch** : Synchronize the table data with the server.
*   **copy** : Copy the table data to the server. However, do not execute record deletes on the server.

The record data for every table with a synch key that is set to *synch* or *copy* will get synchronized. These tables require a corresponding table on the replication server, in our case, HotRiot. To create a table, select the *Create Database* link on the HotRiot *Main Console* page. And follow the instructions. HotRiot uses the term database and table interchangeably; I know, this is a bit strange, but that’s how it is. When creating your tables, keep in mind the following:

*   HotRiot give you the option to create a table manually or to create a table from a CSV file. For now, choose the manual option.
*   HotRiot gives you the option to create MySQL tables or MongoDB collections. For now, only create MySQL tables.
*   Table names are case sensitive and must exactly match the table names used in the SQL statements properties file.
*   Field names are case sensitive and must exactly match the field names used in the table definitions in the SQL statements properties file.
*   If you don’t want a particular field replicated, simply omit it from the table you define in HotRiot.
*   It’s perfectly fine to create fields in the tables that you define in HotRiot that don’t exist in the corresponding SQLite table.
*   EVERY replication table must include a field by the name *systemSynchID* . The field must be defined as type *Tex* t with a length of 50.
*   Set the data types for the fields you define in HotRiot to match the data types for the corresponding fields defined in the SQL statements properties file. This is important. HotRiot performs data validation on all incoming data and will reject mismatches. For example, if you set a field to number and try to insert text, HotRiot will reject the insert.

Below is a screenshot of Step 3 of the HotRiot *Create Database* wizard. This is where you define the table fields, along with the data types and field sizes. If you followed my earlier advice, all of your SQLite tables include a primary key, and this key is a text field populated with a GUID. In HotRiot, GUIDs are simply text fields with a minimum size of 40\. You will also see that the table includes the required *systemSynchID* field.

You will also notice that the data type for the *email* field is set to *Email Address* . For this table, the HotRiot validator will reject any insert where the value for the *email* field is anything other than a valid email address. SQLite does not have an email address data type; as far as I know, no database has this. In SQLite, an email address is simply a text field. It is the responsibility of the application to perform the required data validation. HotRiot has many data type options that are not in SQLite.  For example, phone number, zip code, and year; just to name a few. HotRiot validates all incoming data whenever inserting or updating a record. Any mismatches will result in the insert/update being rejected. This is important for you to bear in mind as you develop your application. The truth is, you should always validate the data that is processed by your app. This helps to ensure the integrity of your data. However, when synchronizing with HotRiot, this becomes mandatory.

![](Image00034.jpg)

There is one other required setting for replication with HotRiot. The *systemSynchID* field must be set to an *Edit Key* , this is done on Step 5 of the *Create Database* wizard. Below is a partial screenshot of this step. Start by setting the special property for the *systemSynchID* field to ‘*Value must be unique* .’ A check box will appear by the name *Edit Key* ; select this check box.

![](Image00026.jpg)

Once all of the tables that are required for synchronization have been created, you’re ready to activate the synchronization process in SQLite.XM.

Activating synchronization in SQLite.XM

Earlier, I showed you how to initialize the SQLite.XM library using the following method call.

`SxmInit.` `initialize();`

When the library is initialized in this manner, synchronization is inactive. That is to say, the SQLite.XM library will not attempt to perform data synchronization. In order to activate synchronization to your HotRiot account, you will need to perform initialization like this.

`SxmInit.` `initialize(“YOUR HotRiot APPLICATION NAME”);`

`this` `.StartService (` `new`  `Intent` ` (` `this` `, ` `typeof` `(` `SynchronizeService` `)));` `  //` `For Android only.`

Replace `“` *`YOUR HotRiot APPLICATION NAME`* `”` with the application name you entered when you registered with HotRiot. You can look-up your application name by selecting the edit registration icon on the HotRiot *Main Console* page.

Synchronization details

When SQLite.XM starts, it immediately checks the replication log for any existing entries. Any records that are in the log are immediately synchronized, if possible. If synchronization succeeds and all outstanding records are synchronized, synchronization goes into a wait state waiting for an event notification. A notification is triggered whenever a record is inserted, updated, or deleted that needs to be synchronized. The notification immediately sets off the synchronization process, where the outstanding record or records are synchronized. That’s how it goes when everything works as planned.

Of course, things never go as planned all of the time and errors are to be expected. Errors encountered by synchronization fall into two categories:

*   Recoverable
*   Non-recoverable

While this seems simple enough, there are details that you need to be aware of. Recoverable errors are errors encountered by synchronization which prevented replication from successfully processing but which are expected to correct themselves. These types of errors cause synchronization to pause for a brief period of time while, hopefully, the error condition clears up. After pausing, synchronization will again attempt to perform replication. If the error persists, synchronization will again pause. It will perform this cycle until it successfully synchronizes or the app is shutdown. If the app is terminated, SQLite.XM will attempt to synchronize all outstanding records the next time it is restarted. Examples of recoverable errors are:

*   Web exceptions
*   IO exceptions
*   Out of memory exceptions
*   Unexpected exceptions

A non-recoverable error is, as its name implies, an error which prevents synchronization from processing and has little or no chance of correcting itself. When SQLite.XM encounters this type of error, it removes the synchronization log entry that triggered the error, it then continues processing with the next record in the log. The offending record that is associated with the deleted log entry is not synchronized.  Examples of non-recoverable errors are:

*   Validation errors in HotRiot. For example, you define a field in HotRiot to expect a number and the corresponding field in the record being synchronized contains text. In such a case, the HotRiot validator will always to reject the insert/update for the record in question. Synchronization has little choice but to skip over the offending record. There are other types of validation errors that can occur. For example, if you define a field in HotRiot as *required* and the field in the record being synchronized is missing, or is null.

These types of validation errors are the primary source of unrecoverable errors. Fortunately, they are easy to prevent by simply including validation code in your app.

The following is another interesting unrecoverable synchronization error. Actually it would be more proper to consider this a replication side effect rather than an error.

![](Image00031.jpg)

Consider the log file above. The record represented by synchronization ID 2764 is updated by log entry 167 and delete by log entry 169\. When synchronization tries to process the update from entry 167, it will be unable to locate the record in the SQLite database due to it being deleted. The logical course of action for synchronization to follow is to simply remove log entry 167 and continue processing. 

Inserting, updating, and deleting of records while synchronization is in the running state, i.e., not waiting, is perfectly fine; there is no coordination that you need to perform. You’re free to modify the device database independent of synchronization. If a record is inserted, updated, or deleted while synchronization is in progress, the resulting replication log entry will be processed as part of the currently running synchronization cycle. Of course, if synchronization is in a wait state, the new log entry will trigger a synchronize event.

Synchronizing files

Earlier, in the section ’Saving file attachments’, I discuss the pros and cons of storing files inside the database verses storing them outside the database. I won’t bore you with a rehash of that material. However, we need to go over some specifics regarding how file attachments are processed by synchronization. This is important for applications that include files as part of their database records and that intend to synchronize with a server-side datastore.

The choice as to whether to store files inside or outside the database can depend heavily on the back-end server with which you intend to synchronize. If you use SQLiteXM’s default synchronization, you will, of course, be synchronizing to HotRiot. HotRiot does not include a BLOB data type. So there is no way to store a file inside a record. In HotRiot, all files are stored externally, in AWS S3\. The database simply includes a pointer to the file. Now, this does not mean that you can’t choose to store files inside the database on the device if this is what you want. But if you do, you will need to write a pre-processing delegate in order to transfer the file data to an actual file on disk and then include the fully qualified path to the newly created file in the record. This is quite a bit of work that increases the complexity and memory footprint of your application. Depending on the size of the files being processed and the capabilities of the device, the memory overhead can be anywhere from insignificant to downright burdensome. There is also one other consideration. Because you will be creating files as part of synchronization, you will need to clean these files from disk. SQLite.XM synchronization includes post-synchronization processing, which would provide you a mechanism for performing the deletes. But this is one more bit of customization that you would need to add to the synchronization process. My advice is this; unless there is some compelling reason to do otherwise, when synchronizing with HotRiot, store files outside the database on the device and simply include a file pointer in the record.

If you synchronize with a server that does support BLOBs, then you might choose to store files inside the SQLite database. That decision may depend on a number of factors, including how records are managed by the server. In any case, in order to make a fully informed decision, you need to be aware of how records that are being synchronized are processed. When a record is selected for synchronization, the entire record data is read from the device database and handed off to the SQLite.XM synchronization processing engine. The first thing synchronization does, is check to see if a pre-processing delegate has been registered with the system, if one has, the record is passed to the delegate for additional processing. Otherwise, the record is sent “as-is” to the server for synchronization. The pre-processing delegate will do whatever it does, possibly creating additional records from the input record. The return record list from the pre-processing delegate will then be synchronized to the server. Finally, if a post-synchronization delegate was registered, it will be called. The thing to keep in mind, is that the entire record is read and passed through the synchronization processing chain. If the files being stored in the database are very large, this could, depending on the constraints of the device, create memory issues. Of course, when synchronizing with a back-end other than HotRiot, you will need to write the code that performs the actual data transfer to the cloud. In this case you have complete control over the synchronization processing. You could choose to store files outside the database on the device and then store them inside the database on the server. The sky’s the limit. In any case, my advice remains the same; unless there is some compelling reason to do otherwise, when synchronizing with a custom back-end, store files outside the device database and simply include a file pointer in the record.

Coordinating synchronization

Earlier, in the section ’Synchronization details’ I said the following:

“Inserting, updating, and deleting of records while synchronization is in the running state, i.e., not waiting, is perfectly fine; there is no coordination that you need to perform. “

So it would be understandable if you’re feeling a bit confused. For the most part, it is safe for your app to operate independent of synchronization. So the quote from above is generally applicable. However, there is one circumstance where you will need to coordinate your apps activities with synchronization.

When synchronization is in the running state, you cannot safely delete files that are part of any records that could be in the process of being synchronized. You will recall from our earlier discussion regarding synchronizing files, that HotRiot requires file attachments to be stored outside the database. This could cause a potential conflict. Your app could attempt to delete a file that SQLite.XM is in the process of uploading to the HotRiot server. Of course, this is not acceptable and needs to be avoided. The solution is simple, before deleting any files that are part of any records that could be in the process of being synchronized, get the synchronization lock for the database where the records reside. You do this using the static `getSynchMonitor` method in the `SxmInit` class; see the method signature below.

`public`  `static`  `bool` ` getSynchMonitor (` `string` ` databaseName, ` `int` ` millisecondsTimeout)`

This method accepts two arguments:

*   The name of the database for which you would like to get the synchronization lock.
*   The number of milliseconds that you would like to wait trying to acquire the lock. The method returns immediately upon acquiring the lock or after the specified wait time has elapsed. Sending the value `Timeout.Infinite` wall cause the method to wait indefinitely until the lock is acquired.

The `getSynchMonitor` method returns *true* if the lock was acquired, otherwise it returns *false* . The SQLite.XM synchronization code could wind up holding a synch lock for quite a long time if the records/files being replicated are very large or the connection quality is poor. This is something that you need to consider in your design. You definitely do not want to block for long periods of time on the user interface thread trying to acquire a lock. Either perform file deletes on a worker thread or set the timeout for acquiring locks to a very brief period of time and design your delete logic to survive failures acquiring locks.

It’s important for your app to not hold a synchronization lock for any longer than absolutely necessary. While your app holds the lock, synchronization will block. You release the lock by calling the static `releaseSynchMonitor` method of the `SxmInit` class; see the method signature below.

`public`  `static`  `void` ` releaseSynchMonitor (` `string` ` databaseName)`

This method accepts as its only parameter the name of the database for which you would like to release the synchronization lock. This method MUST be called for every corresponding `getSynchMonitor` call that returns *true* . Failure to do so will cause synchronization to block indefinitely.

In order to maximize concurrency with lock requests being made by your app, SQLite.XM acquires and releases the synch lock for each record being synchronized. For example, if there were ten records in the replication log, the lock would be acquired and then released for each record. That cycle would repeat ten times, giving your app an opportunity to interleave a lock acquisition of its own in the middle of the synchronization processing.

Customizing synchronization

Up to this point, I have shown you how to setup and perform what I would describe as a standard synchronization. Where each table that is marked for synchronization on the local SQLite database has a corresponding table in HotRiot where the record data is propagated. In addition, error handling is fully managed by the synchronization process as described earlier. This is very easy to setup and for many applications, all that’s needed. However, there are times when more flexibility is required. For example, there may be times when synchronizing using a one-to-one relationship between tables on the device database and tables on the replication server might not be ideal. It may make more sense to transform the source data and save the resulting transformed data to a schema different from the one on the device. Or, you might wish to bypass the default synchronization error processing and instead insert your own custom error handling. And finally, there may be some processing that you would like to perform after a record is synchronized.

In order to accommodate these requirements, SQLite.XM allows you to insert your own custom delegate methods at the following points along the replication processing cycle:

*   Pre-synchronization
*   Post-synchronization
*   Error processing

You can choose to write a delegate for any or all of these.

Pre-synchronization processing

A pre-synchronization delegate allows you to customize replication in order to synchronize with a non-matching server-side schema. Actually, a pre-synchronization delegate can be used to perform any processing that you wish to execute before replicating a record. However, it is intended to be used for non-matching server side replication.

In our earlier synchronization example, each table marked for replication on the local SQLite database had a corresponding table in HotRiot. This standard synchronization only allows you to make minor tweaks to the replication process. For example, you can choose to not replicate specific fields from a device tables by omitting them from the corresponding tables you define in HotRiot. You can also include fields in the HotRiot tables that are not present in the device tables. While these kinds of changes can be useful, they are relatively minor. The fundamental schema between the device and the server datastore remains largely intact, at least for those tables marked for synchronization.

It’s not at all unusual for the schema on the replication server to be dramatically different from the schema found on the device. In fact, I have found this to often be the case. Let’s have a look at an example. Going back to our job search application; imagine we have a registration form for businesses that collects the typical contact information. Because this is a job search app, we also want to collect The human resources contact information, including a picture of the HR contact person. In addition, as part of registering, our app also creates an Android devices ID or an iOS device token; depending on which OS the app is being run. For performance reasons, we’ve decided to flatten the database schema on the device and store all of this information in a single table; the *company_registration* table. This table, as it is structured on the device, is shown below.

![](Image00001.jpg)

On the server-side datastore, we would like a more traditional schema. The figure below shows what the normalized, server-side schema looks like. As you can see, this is quite different from the company registration table on the device. There are four notable changes.

*   First, for the obvious, the original company registration table has been split into three individual tables that are linked to a registration table using foreign keys.
*   The *company_registration* table name is not used as the name for any of the tables on the server-side datastore.
*   New fields have been added to each of the tables which are not present in the company registration table on the device.
*   The fields from the *company_registration* table have not only been moved to different tables on the server, but they have also been renamed.

![](Image00002.jpg)

The question is; how can we transform the original single table registration into a format that will synchronize with the modified schema on the server. In the following discussion, it is assumed that these tables have already been created in HotRiot and that they include all of the fields show above. And that the data types for the fields have been properly set. Just to reiterate from our earlier discussion regarding primary keys, the data type for all primary key fields on the server-side database must be text. In addition, every table must include a `systemSynchID` field. Without this field, SQLite.XM is unable perform replication; for a refresher, see the section ‘Creating the replication database tables’. To keep this example a bit interesting, we have included a picture field in the devices *company_registration* table that needs to be stored in the *hrContact* table on the server.

What we need to do is create a pre-synchronization processing delegate that can perform this transformation. The delegate method signature is shown below.

`public`  `delegate`  `Task` `<` `List` `<` `SynchDescriptor` `>> ` `SynchPreProcessDel` ` (` `SynchDescriptor` ` sd);`

To insert a pre-processing delegate into the SQLite.XM synchronization processing chain, do the following.

*   Create an instance of the *`SynchOptions`* class.
*   Set the `SynchPreProcessDel` field to your error delegate.
*   Pass the `SynchOptions` class to the *`SxmInit.initialize`* method. 

See the first three lines of code below.

`  SynchOptions` ` synchOptions = ` `new`  `SynchOptions` `();`

`  s` `ynchOptions.SynchPreProcessDel = mySynchPreProcessDel;`

 `SxmInit.` `initialize(“YOUR HotRiot APPLICATION NAME”, synchOptions);`

 `this` `.StartService (` `new`  `Intent` ` (` `this` `, ` `typeof` `(` `SynchronizeService` `)));` `  //` `For Android only.`

As you can see, the pre-processing delegate method is passed in a `SynchDescriptor` and it returns a list of `SynchDescriptors` . A `SynchDescriptor` is an object that represents a record that is to be replicated to the server. It contains all of the information needed to perform the replication. The passed in `SynchDescriptor` represents the next record that SQLite.XM found in the replication log. The returned `SynchDescriptor` list, is a list of `SynchDescriptors` that is the output from transforming the input `SynchDescriptor` . This is the list of descriptors that SQLite.XM will actually replicated. A partial listing of the `SynchDescriptor` class is shown below.

 `public`  `class`  `SynchDescriptor`

`  {`

 `public`  `string` ` action;`

 `public`  `string` ` dbName;`

 `public`  `string` ` tableName;`

 `public`  `SynchResponse` `synchResponse;`

 `public`  `Hashtable` ` recordDataToSynch;`

 `public`  `SynchDescriptor` ` (` `string` ` action, ` `string` ` dbName, ` `string` ` tableName)`

`    {`

 `this` `.action = action;`

`      ...`

`    }`

`  }`

The class variables are pretty self-explanatory but we should to go over them anyway.

*   `string` ` action` : this is the synchronization action. It will be *insert* when inserting a new record, *delete* when deleting a record, and *update* when updating a record.
*   `string` ` dbName` : this is the database on the device from where this record was retreived.
*   `string` ` tableName` : this is the table from where this record was  retreived.
*   `SynchResponse` ` synchResponse` : this is the response result of synchronizing the record associated with this `SynchDescriptor` . This is explained in detail in the section ‘Post-synchronization delegate processing’.
*   `Hashtable` ` recordDataToSynch` : this is the actual record data. The keys in the hash contain the field names while the value contains the actual field data.

There is one interesting question regarding the `SynchDescriptor` . If a descriptor is passed to your delegate with an *action* that is *delete* , then what is passed in the `recordDataToSynch` field? In this case, there will only be one entry in the this field; the *systemSynchID* . As you know, the synch ID uniquely identifies a record, and as such, provides all the information that’s needed in order to perform a delete.

**Writing a pre-synchronization delegate**

A pre-synchronization delegate can transform the record represented by the input `SynchDescriptor` in any manner whatsoever. In our example, we are making some fairly extensive changes. The delegate method below performs this transformation, converting from a single table schema on the device to our multi-table server-side schema. It looks like a lot of code, but it is really quite simple.

 `public`  `static`  `async`  `Task` `<` `List` `<` `SynchDescriptor` `>> mySynchPreProcessDel(` `SynchDescriptor` ` sd)`

`  {`

 `List` `<` `SynchDescriptor` `> processList = ` `null` `;`

 `try`

`    {`

**`1`**  `if` ` ((sd.action.Equals (` `"insert"` `) == ` `true` `  || `

 `sd.action.Equals (` `"update"` `) == ` `true` `)  &&`

 `sd.dbName.Equals (` `"jsearch"` `) == ` `true` `  &&`

 `sd.tableName.Equals (` `"company_registration"` `) == ` `true` `)`

`      {`

`          processList = transformCompanyReg (sd);`

`      } `

 `else` 

`      {`

`        processList = ` `new`  `List` `<` `SynchDescriptor` `> ();`

`        processList.Add (sd);`

`      }`

`    }`

 `catch` ` (` `Exception` ` doNothing) {}`

 `return` ` processList;`

`  }`

The method above is the actual pre-processing delegate. It checks if the action for the record being synchronized is either an insert or an update and that the record came from the *`company_registration`* table; see line number 1\. If all of this is true, then the record needs to be transformed, otherwise the record can be synchronized without any modification. The *`transformCompanyReg`* method below performs the actual transformation from the device schema to the server-side schema. A complete explanation follows the code listing.

 `private`  `static`  `List` `<` `SynchDescriptor` `> transformCompanyReg (` `SynchDescriptor` ` sourceSD)`

`  {`

 `List` `<` `SynchDescriptor` `> processList = ` `new`  `List` `<` `SynchDescriptor` `> ();`

**`1`**  `SynchDescriptor` ` companyRegSD = ` `new`  `SynchDescriptor` ` (sourceSD.action,`

 `sourceSD.dbName, ` `"companyReg"` `);`

**`2`**  `SynchDescriptor` ` hrContactSD = ` `new`  `SynchDescriptor` ` (sourceSD.action,`

 `sourceSD.dbName, ` `"hrContact"` `);`

**`3`**  `SynchDescriptor` ` pushConnectionIDSD = ` `new`  `SynchDescriptor` ` (sourceSD.action,`

 `sourceSD.dbName,` `"gcmApnsID"` `);`

 `if` ` (sourceSD.recordDataToSynch.ContainsKey (` `"systemSynchID"` `) == ` `true` `) `

`    {`

 `object` ` dataObject = sourceSD.recordDataToSynch [` `"systemSynchID"` `]; `

**`4`** `     companyRegSD.recordDataToSynch.Add (` `"systemSynchID"` `, dataObject);`

**`5`** `     hrContactSD.recordDataToSynch.Add (` `"systemSynchID"` `, dataObject);`

**`6`** `    pushConnectionIDSD.recordDataToSynch.Add (` `"systemSynchID"` `, dataObject);`

`    } `

 `else`

 *`// This should not happen!`*

 `throw`  `new`  `Exception` ` (` `"Error, missing systemSynchID. This record cannot be synchronized."` `);`

 `Dictionary` `<` `string` `,` `string` `> translate = ` `new`  `Dictionary` `<` `string` `, ` `string` `> ();`

 *`// Set the source to destination field name translations for the companyReg table.`*

**`7`** `   translate.Add (` `"coRegName"` `, ` `"name"` `); `

**`8`** `   translate.Add (` `"coRegAddress"` `, ` `"address"` `); `

**`9`** `   translate.Add (` `"coRegCity"` `, ` `"city"` `); `

**`10`** ` translate.Add (` `"coRegState"` `, ` `"state"` `); `

**`11`** `  translate.Add (` `"coRegZipcode"` `, ` `"zip_code"` `); `

**`12`** `  translate.Add (` `"coRegEmail"` `, ` `"email"` `); `

**`13`** `  translate.Add (` `"coRegPhone"` `, ` `"phone"` `); `

**`14`** `  translate.Add (` `"coRegPassword"` `, ` `"password"` `); `

**`15`** `  translate.Add (` `"coRegPrimaryKey"` `, ` `"primary_key"` `);`

**`16`** `  translateSynchDescriptor (sourceSD, companyRegSD, translate);`

 `TimeSpan` ` elapsedSpan = ` `new`  `TimeSpan` `(` `DateTime` `.UtcNow.Ticks - `

 `new`  `DateTime` `(` `1970` `, ` `1` `, ` `1` `).Ticks);`

**`17`** `  companyRegSD.recordDataToSynch.Add (` `"time"` `, ` `Convert` `.ToInt64(elapsedSpan.TotalSeconds));`

 *`// Set the source to destination field name translations for the hrContact table.`*

`    translate.Clear ();`

`    translate.Add (` `"hrContact"` `, ` `"name"` `); `

`    translate.Add (` `"hrEmail"` `, ` `"email"` `); `

`    translate.Add (` `"hrPhone"` `, ` `"phone"` `); `

`    translate.Add (` `"hrPicture"` `, ` `"picture"` `); `

`    translate.Add (` `"coRegPrimaryKey"` `, ` `"registration_fk"` `); `

`    translateSynchDescriptor (sourceSD, hrContactSD, translate);`

**`18`** `  hrContactSD.recordDataToSynch.Add (` `"primary_key"` `, ` `Guid` `.NewGuid ().ToString ());`

 *`// Set the source to destination field name translations for the gcmApnsID table.`* 

`    translate.Clear ();`

`    translate.Add (` `"coIOSToken"` `, ` `"ios_device_token"` `); `

`    translate.Add (` `"coAndroidToken"` `, ` `"android_device_id"` `); `

`    translate.Add (` `"coRegPrimaryKey"` `, ` `"registration_fk"` `); `

`    translateSynchDescriptor (sourceSD, pushConnectionIDSD, translate);`

**`19`** `  pushConnectionIDSD.recordDataToSynch.Add (` `"primary_key"` `, ` `Guid` `.NewGuid ().ToString ());`

**`20`** `  processList.Add (companyRegSD);`

**`21`** `  processList.Add (hrContactSD);`

**`22`** `  processList.Add (pushConnectionIDSD);`

  `return` ` processList;`

`  }`

 `private`  `static`  `void` ` translateSynchDescriptor (` `SynchDescriptor` ` sourceSD, `

 `SynchDescriptor` ` transformedSD, `

 `Dictionary` `<` `string` `,` `string` `> translate)`

`  {`

 `foreach` ` (` `KeyValuePair` `<` `string` `, ` `string` `> pair ` `in` ` translate)`

 `if` ` (sourceSD.recordDataToSynch.ContainsKey (pair.Key) == ` `true` `)`

`        transformedSD.recordDataToSynch.Add (pair.Value, `

 `sourceSD.recordDataToSynch [pair.Key]);`

`  }`

The first thing that we need to do is create a `SynchDescriptor` for each of the server-side tables that will be written to as part of the synchronization. This is done on lines 1 thru 3\. As you can see, we use the same action and database name from the source descriptor when instantiating the new descriptors. The table name however, is set to the name of the server-side table. The database name is currently not used by replication, but we set it anyway.

On lines 4 thru 6 we add a `systemSynchID` field to each record. SQLite.XM uses this ID to identify the record on the server that is being synchronized. For example, if the synchronization action is update or delete, then the synch ID would be used to locate the record on the server being updated or deleted. In this example, we are setting the synch IDs to the `systemSynchID` from the source `SynchDescriptor` . Using this value works just fine in most cases and is by far the easiest solution. However, if for some reason you need a different synch ID for each record, you can choose to compute a unique hash using the `systemSynchID` from the source `SynchDescriptor` . A computed hash value MUST be unique and the output MUST be repeatable given the same input, i.e., deterministic.

On lines 7 thru 15 we are setting the field translation dictionary. The dictionary keys contain the field names from the input `SynchDescriptor` . The dictionary values contain the translated field names, i.e., the corresponding field names on the server-side table. For example, on line 7 the data from the *`coRegName`* field from the *`company_registration`* table on the device will be copied to the *`name`* field in the *`companyReg`* table on the server.

On line 16 we call the method *`translateSynchDescriptor`* , which copies the record data from the source synch descriptor to the *`companyReg`* synch descriptor. The *`companyReg`* table on the server includes a *`time`* field which is not present in *`company_registration`* table on the device. On line 17 we set this field to the number of seconds which have elapsed since 1970-01-01.

The logic from lines 7 thru 16 is repeated for the *`hrContact`* and *`gcmApnsID`* tables. These tables also include a primary key field, which are set on lines 18 and 19\. The synch descriptor list is populated on lines 20 thru 22 and is returned in the last statement of the listing. SQLite.XM will synchronized the records in the order that they appear in the list.

In the code above, I show one way to convert an input `SynchDescriptor` that represents a single record on the device to multiple `SynchDescriptors` , each representing a row to be synchronized to the server. This is just one example of what can be done using pre-synchronization processing. The ways in which you can perform a source-to-destination transformation using pre-synchronization is virtually unlimited and provides you with the flexibility to design the server datastore independent from the device database.

**Pre-synchronization abort conditions**

How you choose to handle errors within your pre-synchronization delegate is entirely up to you. Processing that is internal to the delegate method does not affect synchronization, however, what you return from a delegate does.

If the SQLite.XM synchronization engine determines that it cannot synchronize what is returned by your delegate, it will simply abort replication for the record that initiated the synchronization operation; removing it from the synchronization log. Any of the following would cause such a condition.

*   Throwing an exception from the delegate.
*   Returning an empty `SynchDescriptor` list.
*   Returning null.
*   Returning a record in the `SynchDescriptor` list that does not include a `systemSynchID` field.

These trigger an automatic unrecoverable replication failure, leaving synchronization with little choice but to abort replication for the current record.

You could use this knowledge to force the disposal of an entry in the replication log without performing replication. For example, if your pre-processing delegate were to experience some failure that rendered the log entry useless for replication, you could choose to throw an exception in order to remove the record from the log. In fact, this is exactly what we do in our pre-processing delegate example from earlier. If you look at the code, you will see that we throw an exception if the input synch descriptor does not include a `systemSynchID` . In this case, the pre-processing delegate realizes there is no hope of replicating this entry, so it just throws an exception in order to remove the record from the log.

**Multi-table synchronizations error processing**

Basic synchronization, i.e., replication that does not include a pre-processing delegate, replicates one record at a time. If an error is encountered, the replication operation fails in an atomic manner; there are no partial synchronizations or partial failures. Depending on whether an error is recoverable or non-recoverable, a failed operation may be retried at a later time. But still, it either succeeds or fails. Failures from a synchronization operation that includes a pre-processing delegate can get more involved.

If the output from a pre-processing delegate is a single synchronization operation, i.e., only one `SynchDescriptor` is returned in the synch descriptor list, then a synchronization error will be processed in the manner described above. However, if a pre-processing delegate generates multiple `SynchDescriptors` , then things get a bit more complicated. But before we try to understand how, we need to first to consider the kinds of synchronization operations that are typically generated by pre-processing delegates.

*   If the *action* in a source `SynchDescriptor` is an insert, then a pre-processing delegate will normally transform the single record insert into a multi-record insert. This fits the description of our earlier example.
*   If the *action* in a source `SynchDescriptor` is a delete, then a pre-processing delegate will normally transform the single record delete into a multi-record delete.
*   If the *action* in a source `SynchDescriptor` is an update, then a pre-processing delegate will normally transform the single record update into multi-record update.

This is pretty typical. For example, it would be a bit unusual for an insert synchronization action to be transformed by a pre-processing delegate to include, say, a delete. The same is true for a delete action and an update action. Mixing different actions in the same synchronization operation is unusual. That being said, there is nothing in SQLite.XM that would disqualify such a transform.

Let’s use our earlier pre-synchronization example to help us to understand error processing for a multi-table synchronization operation. The figure below shows a single record on the device transformed into three records that are to be replicated to HotRiot.

![](Image00029.jpg)

The records are synchronized in the following order: `companyReg, hrContact, gcmApnsID` . With respect to error processing, there are several questions that need to be answered:

*   What happens if a recoverable error is encountered after successfully replicating at least one entry in a replication list?

    **Answer** : The entry in the replication log that triggered the replication operation will not be deleted and will get re-synchronized during the next replication cycle. Recoverable errors are fully recoverable; it doesn’t matter what mix of entries are in the replication list or which entries in the list were successfully posted, the HotRiot server is capable of successfully reprocessing entries. While it is unusual to mix entries, for recoverable errors, it makes no difference.

*   What happens if a non-recoverable error is encountered after successfully replicating at least one entry in a replication list?

    **Answer** : An attempt will be made to delete all of the *insert* operations that were successfully posted to HotRiot. If a non-recoverable error is encountered trying to perform the deletes, the newly inserted records are simply orphaned. If a recoverable error is encountered processing the deletes, the entry in the replication log that triggered the replication operation will not be deleted and will get reprocessed during the next replication cycle. Presumably, the same failure will occur and the cleanup code will re-run. If the error does not reappear, then fine, the synchronization will successfully process.

    For *update* and *delete* operations, things are handled a bit differently. No attempt is made to rollback any *update* or *delete* operations which are successfully posted to HotRiot before a non-recoverable error is encountered. These cannot be reversed.

> > Non-recoverable errors should be a very rare occurrence, provided you properly validate all data being sent to the server.

Synchronization error processing

A synchronization error delegate is a method that is inserted into the synchronization processing chain that is called when an error is encountered synchronizing a record. It allows you to insert your own custom error processing. The signature for the error delegate method is shown below.

`public`  `delegate`  `Task`  `SynchErrorDel` ` (` `SynchDescriptor` ` synchDescriptor` `, SynchResponse` ` synchResponse);`

To insert your own handler into the SQLite.XM synchronization processing chain, do the following.

*   Create an instance of the *`SynchOptions`* class.
*   Set the `SynchErrorDel` field to your error delegate.
*   Pass the `SynchOptions` class to the *`SxmInit.initialize`* method. 

See the first four lines of code below.

`  SynchOptions` ` synchOptions = ` `new`  `SynchOptions` `();`

`  synchOptions.SynchErrorDel = mySynch` `ErrorDel;`

`  synchOptions.SynchPreProcessDel = mySynchPreProcessDel;`

`  SxmInit.` `initialize(“YOUR HotRiot APPLICATION NAME”, synchOptions);`

`  this` `.StartService (` `new`  `Intent` ` (` `this` `, ` `typeof` `(` `SynchronizeService` `)));  //` `For Android only.`

In this short code fragment, we set both the error delegate and the pre-processing delegate. Synchronization delegates are not interdependent in any way. They can be set individually or with other delegates. We did this just to show how you could set multiple delegates.

As you can see, the error delegate method returns a void and is passed the following two parameters.

*   `SynchDescriptor` `synchDescriptor` - This is the synch descriptor for the record being synchronized which triggered the error.
*   `SynchResponse` `synchResponse` - This is the response result that was returned from synchronizing the record.

Synch descriptors were explained earlier in the section ‘Post-synchronization delegate processing.’ So I won’t bore you rehashing that material. The `SynchResponse` object contains the results of synchronizing the record in the `SynchDescriptor` . A partial listing of this class is shown below.

 `public`  `class`  `SynchResponse`

`  {`

  `public` ` SQLiteXM.` `Defines` `.` `SynchErrorTypes` ` synchErrorType;`

 `public`  `ProcessingSynchError` ` processingSynchError;`

 `public`  `ExceptionSynchError` ` exceptionSynchError;`

 `public`  `bool` ` removeFlag = ` `true` `;`

 `...`

A description of each instance variable follows.

*   `SynchErrorTypes` `synchErrorType` - This field is the success or error response value. It will indicate either success or the category of error that occurred. Synchronization errors fall into two general categories; exception errors and processing errors. It will be set to one of the following two enums.

    `Defines` `.` `SynchErrorTypes.` `exception` - These are failures that occur trying to post a synchronization request to HotRiot. As a general rule, an exception error indicates that HotRiot never received the synchronization request or failed to send back a response. They include such things as IOExceptions, WebExceptions, etc. You will need to inspect the `exceptionSynchError` object for details.

    `Defines` `.` `SynchErrorTypes.` `processing` - These are failures that occur in HotRiot trying to fulfill a synchronization request. You will need to inspect the `processingSynchError` object for details.

*   `ProcessingSynchError` - If a processing error occurred, this object will provide details regarding the error. Otherwise it will be null.

*   `ExceptionSynchError` - If an exception error occurred, this object will provide details regarding the exception. Otherwise it will be null.

*   `Bool` `removeFlag` - This indicates whether the record in the replication log that triggered this error should be deleted. If *true* , the entry will be removed, otherwise it will be retained. The default value for this field is *true* . Your handler should set this field to *false* for recoverable errors and *true* for non-recoverable errors. This will be explained in more detail a bit later.

**Handling exception synchronization errors**

Exception errors indicate a failure posting a synchronization request to HotRiot, that is to say, HotRiot never received the request. It can also indicate a failure by HotRiot to respond to a request before a timeout occurred. A partial listing of the `ExceptionSynchError` class is shown below.

 `public`  `class`  `ExceptionSynchError`

`  {`

 `public`  `Exception` ` exception;`

 `public`  `string` ` exceptionType;`

 `public`  `string` ` exceptionMessage;`

`  . . .`

A description of each instance variable follows

*   `Exception` `exception` - This is the actual exception object for the exception.
*   `String` `exceptionType` - This is the type of exception that was encountered. For example, WebException, OutOfMemoryException, IOException, etc.
*   `String` `exceptionMessage` - This is the error message for this exception.

The screenshot below shows the output from an error response object for an `exception` type error. As you can see, the `synchErrorType` is set to `exception` and the `exceptionSynchError` object contains the details about the exception. This particular exception is a WebException which was thrown due to a timeout waiting on a response from HotRiot. The default SQLite.XM error handler considers a server timeout a recoverable error. It therefore set the `removeFlag` to *false* . As you will recall, recoverable errors are errors that are expected to correct themselves. From the perspective of the device, a server timeout is considered a temporary condition.

![](Image00033.jpg)

The table below lists the possible exception types returned in the `exceptionType` field.

![](Image00037.jpg)

**Handling processing synchronization errors**

Processing errors are errors that occur within HotRiot trying to fulfill a synchronization request. They indicates an error condition trying to process the request which prevented it from being successfully completed. A partial listing of the `ProcessingSynchError` class is shown below.

 `public`  `class`  `ProcessingSynchError`

`  {`

 `public`  `int` ` resultCode;`

 `public`  `string` ` resultTex;`

 `public`  `string` ` resultMessage;`

`  . . .`

A description of each instance variable follows

*   `int` `resultCode` - This is the numeric error code for the processing error.
*   `String` `resultText` - This is the general error message for the processing error.
*   `String` `resultMessage` - This is the specific error message.

The screenshot below shows the output from an error response object for a `processing` type error. As you can see, the `synchErrorType` is set to `processing` and the `processingSynchError` object contains the details about the error. The `resultText` field tells us the general type of processing error that occurred. This particular error was an invalid data exception. The `resultMessage` gives us a more detailed reason as to what caused the error, which in this case, was due to sending incorrectly formatted data to an email address field. The default SQLite.XM error handler considers invalid data exception errors non-recoverable. It therefore set the `removeFlag` to *true* . As you will recall, non-recoverable errors are errors that have little hope of correcting themselves. No matter how many attempts are made to replicate this record, the server is going to return the same error response, unless, of course, the error is somehow corrected.

![](Image00038.jpg)

The table below lists the possible values returned in the `resultCode` and `resultText` fields.

![](Image00032.jpg)

**Invalid data errors and non-unique data errors**

You’ll most likely encounter a synchronization processing error due to an invalid data error or a non-unique data error; error codes 3 and 4 respectively. Invalid data errors can occur for two reasons.

*   Incorrectly formatted data being posted to a field. For example, if you define a field in HotRiot to hold a number (done on step 3 of the HotRiot create database wizard) and try posting text data to the field.
*   You define a field in HotRiot as “Required” (also done on step 3 of the create database wizard) but the data field is missing in a record that SQLite.XM tries to synchronize.

Both of these are easily avoided by simply including data validation logic in your app. This is something you should always be doing anyway.

Non-unique data exception errors are a bit more complicated to manage, or, to be more accurate, prevent from occurring in the first place. These errors are caused by posting non-unique data to a data field that requires unique data. If you define a field in a HotRiot table as unique, HotRiot will reject any record insert or update request where the data being posted to the unique field already exists in the database. Nothing unusual here, this what you would expect. The problem is, in a distributed environment how can you be sure the data that’s being generated on the device is, in fact, unique across all other devices? This is very similar to the problem we faced generating unique primary keys. The solution there, was to simply use GUIDs instead of the typical auto-increment value. Unfortunately, for user generated data, such as passwords, this is not a viable option. Even for application generated data, this will often times be an unworkable solution. So, what are we to do? This problem is complicated by several factors.

*   Mobile apps operate in the context of an unreliable distributed environment. It may not be feasible at any particular point in time to check data generated on the device against data already on the replication server.

*   Data generated on one device cannot realistically be checked against the data on all other devices waiting to synchronize.
*   The app may be online or offline at any given moment.
*   Replication is a deferred process. And even if we designed for immediate replication, given the transient nature of connections, there is really no way to guarantee real-time or even near real-time synchronization.

So, how can we ensure unique data given an environment with the constraints listed above? To show how this is done, we will be revisiting the registration example from earlier.

![](Image00029.jpg)

You’ve seen the figure above. It shows a single registration table on the device that’s synchronized with three tables on the server. For this discussion, imagine that the registration password field must be populated with a password that is unique from all passwords that have been entered by other users. How can we ensure a unique password? The easy solution is to “cheat” and only allow users to register when the device/app has network connectivity. In many instances, this is the preferred solution and it’s the easiest to implement. Here’s one way to do it.

For this discussion, we assume that the three tables in HotRiot needed to hold the registration information have already been created. And that the password field in the `companyReg` table has been defined as unique. When a user submits a registration, don’t immediately save it to the local device database as you normally would, instead, first try and save the record to HotRiot. Of the three tables in HotRiot that make up the aggregate registration, you will only need to post the `companyReg` table information, as this is the only table that includes a unique field. If the record successfully posts to HotRiot, then you know the password field is unique. The newly created record in HotRiot will serve as a placeholder effectively reserving the password for this user. You now need to post the entire `company_registration` record to the local device database. Once you have completed this step, you’re done. SQLite.XM will take care of synchronizing the two other tables; `hrContact` and `gcmApnsID` . Of course, if the post to HotRiot fails, you will need to inspect the cause of the failure, and if it was due to a non-unique data exception, you’ll need to ask the user to reenter their password. The code listing below shows how to perform the operation just described.

This is a very simple company registration Android activity. The `registrationSubmitHandler` method attempts to save the registration record to HotRiot. If it succeeds, it calls the method `postRegistrationLocal` , which saves the registration to the device database. A detailed explanation follows the listing.

 `[` `Activity` ` (Label = ` `"CoRegistrationActivity"` `)]            `

 `public`  `class`  `CoRegistrationActivity` ` : ` `Activity`

`  {`

 `protected`  `override`  `void` ` OnCreate (` `Bundle` ` bundle)`

`    {`

 `base` `.OnCreate (bundle);`

`      SetContentView (` `Resource` `.` `Layout` `.CoRegistration);`

 `Button` ` submitCoRegButton = FindViewById<` `Button` `> (` `Resource` `.` `Id` `.submitCoRegButton);`

**`1`** `     submitCoRegButton.Click += ` `async`  `delegate` ` { ` `await` ` registrationSubmitHandler (); };`

`    }`

 `private`  `async`  `Task` ` registrationSubmitHandler ()`

`    {`

**`2`**  `NameValueCollection` ` hrRecord = ` `new`  `NameValueCollection` ` ();`

 `string` ` systemSynchID = ` `Guid` `.NewGuid ().ToString ();`

**`3`** `     hrRecord.Add (` `"systemSynchID"` `, systemSynchID);`

 `string` ` registrationPK = ` `Guid` `.NewGuid ().ToString ();`

`     hrRecord.Add (` `"primary_key"` `, registrationPK);`

`      hrRecord.Add (` `"name"` `, FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegName).Text);`

`      hrRecord.Add (` `"address"` `, FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegAddress).Text);`

`      hrRecord.Add (` `"city"` `, FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegCity).Text);`

`      hrRecord.Add (` `"state"` `, FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegState).Text);`

`      hrRecord.Add (` `"zip_code"` `, FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegZipcode).Text);`

`      hrRecord.Add (` `"email"` `, FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegEmail).Text);`

`      hrRecord.Add (` `"phone"` `, FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegPhone).Text);`

`      hrRecord.Add (` `"password"` `, FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegPassword).Text);`

 `TimeSpan` ` elapsedSpan = ` `new`  `TimeSpan` ` (` `DateTime` `.UtcNow.Ticks - `

 `new`  `DateTime` ` (` `1970` `, ` `1` `, ` `1` `).Ticks);`

`      hrRecord.Add (` `"time"` `, ` `Convert` `.ToInt64 (elapsedSpan.TotalSeconds).ToString());`

 *`// This is the table in HotRiot where the record will be saved.`*

 `string` ` tableName = ` `"companyReg"` `;`

 `string` ` editKey = ` `"systemSynchID"` `;`

 `HRInsertResponse` ` hrInsertResponse = ` `null` `;`

 `try`

`      {`

**`4`** `       hrInsertResponse = ` `await`  `HotRiot` `.getHotRiotInstance.submitKeyUpdateInsertRecord (tableName, editKey,  `

 `systemSynchID, hrRecord, ` `null` `);`

`        int resultCode =` `hrInsertResponse.getResultCode ();`

**`5`**  `if` `(resultCode == ` `HotRiot` `.SUCCESS) `

 `await` ` postRegistrationLocal (registrationPK, systemSynchID);`

 `else`

`        {`

**`6`**  `if` ` (resultCode == ` `HotRiot` `.NOT_UNIQUE_DATA_EXCEPTION)`

`          {`

 `string` ` resultMessage = hrInsertResponse.getResultMessage ();`

 *`// Was it the password field that caused the failure.`*

**`7`**  `if` ` (resultMessage.StartsWith (` `"password:"` `) == ` `true` `) `

`            {`

 *`// Alert the user that their password is not unique.`*

`            }`

 `else`

`            {`

 *`// Some other field cause the non-unique error. Do something.`*

`            } `

`          }`

 `else`

`          {`

 *`// Some other error occurred. Do something.`*

`          } `

`        } `

`      }`

 `catch` ` (` `HotRiotException` ` hex) `

`      {`

 `string` ` exType = (` `string` `)hex.Data [` `"exceptionType"` `];`

 *`// Some kind of connection problem.`*

 `if` ` (exType.Equals (` `"WebException"` `) == ` `true` ` || exType.Equals (` `"IOException"` `) == ` `true` `) `

`        {`

 *`// Alert user their is a connection problem and can't save registration.`*

`        }`

 `else`

`        {`

 *`// Some other exception occurred. Do something.`*

`        }`

`      }`

  `}`

 `private`  `async`  `Task` ` postRegistrationLocal (` `string` ` registrationPK, ` `string` ` systemSynchID)`

`    {`

 `ArrayList` ` parameterValues = ` `new`  `ArrayList` ` ();`

`      parameterValues.Add (registrationPK);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegName).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegAddress).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegCity).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegState).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegZipcode).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegEmail).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegPhone).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.hrContact).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.hrEmail).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.hrPhone).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.hrPicture).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coIOSToken).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coAndroidToken).Text);`

`      parameterValues.Add (FindViewById<` `EditText` `> (` `Resource` `.` `Id` `.coRegPassword).Text);`

`      parameterValues.Add (systemSynchID);`

 `try`

`      {`

 `using` `(` `SxmTransaction` ` sqlTransaction = ` `new`  `SxmTransaction` ` (` `"jsearch"` `))`

`        {`

 `InsertResponse` ` ir = sqlTransaction.executeInsert(` `"registerCompany"` `, `

 `parameterValues);`

`          sqlTransaction.commitTransaction ();`

`        }`

`      }`

 `finally`

`      {`

 `Intent` ` CoHomeActivity = ` `new`  `Intent` ` (` `this` `, ` `typeof` `(` `CoHomeActivity` `));`

`        CoHomeActivity.PutExtra (` `"registrationPK"` `, registrationPK);`

`        StartActivity (CoHomeActivity);`

`      }`

`    }`

`  }`

*   Line 1 sets the handler for the submit button to the `registrationSubmitHandler` method. This method takes care of posting the `companyReg` portion of the registration to HotRiot. Remember, a registration is saved to three tables on the server, this method only posts to the `companyReg` table.
*   Line 2 instantiates a name value collection. This holds the company registration record data that will be saved to HotRiot.
*   On lines 3, the record’s `systemSynchID` is set. As you know, the `systemSynchID` is a required field that’s used by synchronization to uniquely identify a record. When manually creating a new record in HotRiot, this field must be set to a GUID. The next several lines of code set remaining fields for the record.
*   On line 4, the record is posted to HotRiot. I don’t want to turn this into a tutorial on HotRiot, so I won’t explain this further. Please look to the HotRiot C# documentation for details. Here’s the URL: https://hotriot.com/hrCSAPI/hotriot_c__interface_guide.htm
*   Line 5 checks the result code from the record post that was performed on line 4\. If successful, the `postRegistrationlocal` method is called, where the registration record is saved to the device database, otherwise the result code is examined further.
*   Line 6 checks to see if the failure was caused by a non-unique data error. If it was, the result message is retrieved.
*   Line 7 checks the result message to see if the password field was the cause of the non-unique data error. This check is only needed if more than one field in a record could have caused this error. I added this to the code just to illustrate how it’s done.

    As a side note, you might be interested as to what’s returned in the `resultMessage` field for invalid data errors and non-unique data errors. The validation error text that you enter on step 4 of the HotRiot create database wizard is returned for invalid data errors and the validation text you enter in step 5 is returned for non-unique data errors. By inspecting the result message, you can easily determine the field that triggered the error. When I set the validation text, I always start with the field name followed by a colon. This makes it really easy to identify the offending field.

It’s okay to check for the existence of a connection before doing some operation that requires connectivity. But it’s not something you can really rely on. You could check and find that a connection exists and then a fraction of a millisecond later it’s gone. Regardless of whether you think a connection exists, you will need to put in place the logic to handle connectivity errors. A connection check is really only useful when you receive a negative response. In such a case, you might decide to skip a connection-based operation or take some alternate action, such as alerting the use.

If your app is designed to allow users to perform offline inserts into tables that include unique fields, for example, registering while in airplane mode. Then there will be no way to be sure at the time of the insert that a particular fields is unique from all other values saved by other users. You will be left with little choice but to design some mechanism where a user can be asked to modify their entry if a unique filed is later found to be non-unique.

**Writing a synchronization error handler**

The task of a synchronization error handler should be limited to determining whether the entry in the replication log which triggered the synchronization failure should or should not be removed. That’s it! This is done by setting the `removeFlag` of the `SynchResponse` object to either *true* of *false* . Actual error correction should be handled by a post-synchronization delegate not the error handler; this is explained in the next section ‘Post-synchronization delegate processing.’ The default synchronization error handler is shown below.

 `internal`  `static`  `async`  `Task` ` myErrorDel(` `SynchDescriptor` ` synchDescriptor, `

 `SynchResponse` ` synchResponse)`

`  {`

**`1`**  `if` ` (synchResponse.synchErrorType == SQLiteXM.` `Defines` `.` `SynchErrorTypes` `.exception ) `

`    {`

**`2`**  `if` ` (synchResponse.exceptionSynchError.exceptionType.Equals (` `"WebException"` `) == ` `true` ` || `

`          synchResponse.exceptionSynchError.exceptionType.Equals (` `"IOException"` `)  == ` `true` ` || `

`          synchResponse.exceptionSynchError.exceptionType.Equals (` `"OutOfMemoryException"` `) == ` `true` `)`

`              synchResponse.removeFlag = ` `false` `;`

`    }`

 `else`

**`3`**  `if` ` (synchResponse.synchErrorType == SQLiteXM.` `Defines` `.` `SynchErrorTypes` `.processing) `

`      {`

**`4`**  `if` ` (synchResponse.processingSynchError.resultCode == ` `HotRiot` `.DB_FULL_EXCEPTION)`

`          synchResponse.removeFlag = ` `false` `;`

`      }`

 `}`

As you can see, this handler first checks to see whether it is dealing with an exception error or processing error; see lines 1 and 3. It then checks to see if the error is recoverable, if it is, it sets the `removeFlag` to *false* . Otherwise, the `removeFlag` is left to its default value of *true* ; see lines 2 and 4.

When writing your own handler, you’ll need to determine which errors are recoverable and which ones are non-recoverable. Non-recoverable errors should result in the current replication log entry being deleted, ending synchronization for that record. Of course, synchronization continues processing the next entry in the log, if one is present. Otherwise it goes into a wait state, waiting for a new entry.

Recoverable errors are a bit more involved. Returning *false* in the `removeFlag,` instructs SQLite.XM to leave the current replication log entry intact; to be re-processed at some later point. Replication then halts for a period of time and then restarts processing, beginning with the same record. Be careful not to put replication into an endless loop that blocks synchronization. Let me explain. The screenshot below shows an invalid data processing error.

![](Image00038.jpg)

This particular error was caused by sending incorrectly formatted data to an email address field. Unless the root cause of the error is corrected, trying to resynchronize this record will only result in HotRiot returning the same error response; putting replication into an endless loop that blocks all synchronization.

If you return *false* in the `removeFlag,` one of the following conditions MUST be true.

*   The condition that caused the error must be self-correcting. For example, a timeout from the HotRiot server, or a Web or IO exception caused by a connection failure. It must be some sort of error that you can be reasonably sure will correct itself when conditions change.
*   The cause of the error must be explicitly corrected.

Post-synchronization processing

A post-synchronization delegate is a method that is inserted into the synchronization processing chain that’s called after replication has completed. It’s called for each entry in the replication log that’s processed. And it is called regardless of whether processing is successful, or a recoverable or non-recoverable error is encountered. The post-processing delegate is not called for abort conditions; see the section ‘Synchronization abort conditions.’

The post-processing method signature is shown below.

`public`  `delegate`  `Task`  `SynchPostProcessDel` ` (` `SynchDescriptor` ` originalSD, `

 `List` `<` `SynchDescriptor` `> sdList, `

 `SynchResponse` ` synchResponse);`

To insert a post-processing delegate into the SQLite.XM synchronization processing chain, do the following.

*   Create an instance of the *`SynchOptions`* class.
*   Set the `SynchPostProcessDel` field to your error delegate.
*   Pass the `SynchOptions` class to the *`SxmInit.initialize`* method. 

See the first four lines of code below.

`  SynchOptions` ` synchOptions = ` `new`  `SynchOptions` `();`

`  s` `ynchOptions.SynchPostProcessDel = mySynchPostProcessDel;`

`  s` `ynchOptions.SynchPreProcessDel = mySynchPreProcessDel;`

 `SxmInit.` `initialize(“YOUR HotRiot APPLICATION NAME”, synchOptions);`

 `this` `.StartService (` `new`  `Intent` ` (` `this` `, ` `typeof` `(` `SynchronizeService` `)));` `  //` `For Android only.`

In this short code fragment, we set both the pre-processing delegate and the post-processing delegate. Synchronization delegates are not interdependent in any way. They can be set individually or with other delegates. We did this just to show how you could set multiple delegates.

As you can see, the post-processing delegate method returns a void and is passed the following three parameters.

*   `SynchDescriptor` `originalSD` - This is the synch descriptor for the record associated with the entry in the replication log being synchronized. This is the descriptor that is passed to the pre-processing delegate, if one is registered.
*   `List` `<` `SynchDescriptor` `> sdList` - This is the list of descriptors that SQLite.XM actually replicated to HotRiot. It is the output from the pre-processing delegate, if one is registered. Otherwise, this list will contain a single entry that points to the same object as the `originalSD` parameter.
*   `SynchResponse` ` synchResponse` - This is the response result that was returned from the last record in the `sdLis` t that was synchronized.

The `SynchResponse` parameter requires some additional clarification. The `SynchDescriptors` in the `sdList` are synchronized in the order that they appear in the list. A `SynchResponse` is returned for each entry processed and is put in the `SynchResponse` instance variable of the `SynchDescriptor` being synchronized. Synch descriptors were explained in detail in the ‘pre-synchronization delegate processing’ section. A partial listing of the `SynchDescriptor` class is shown below.

 `public`  `class`  `SynchDescriptor`

`  {`

 `public`  `string` ` action;`

 `public`  `string` ` dbName;`

 `public`  `string` ` tableName;`

 `public`  `SynchResponse` `synchResponse;`

 `public`  `Hashtable` ` recordDataToSynch;`

`  . . .`

The response from the last record processed in the list is returned as the last parameter to the post-processing delegate. This is done as a matter of convenience. You could easily iterate through the descriptors in the `sdList` and inspect each `SynchResponse` object individually. But this is unnecessary, as you are really only interested in the response from the last record in the `sdList` that was processed. If this is a success response, then replication succeeded, otherwise replication failed. Replication is immediately halted if an error is encountered. If there is more than one descriptor in the `sdList,` then you will need to iterate through the list to know which descriptor caused the failure. I show you how to do this a bit later.

The `SynchResponse` class was covered in detail in the ‘Synchronization error delegate processing’ section, so I’ll only do a quick overview. A partial listing of this class is shown below.

 `public`  `class`  `SynchResponse`

`  {`

  `public` ` SQLiteXM.` `Defines` `.` `SynchErrorTypes` ` synchErrorType;`

 `public`  `ProcessingSynchError` ` processingSynchError;`

 `public`  `ExceptionSynchError` ` exceptionSynchError;`

 `public`  `bool` ` removeFlag = ` `true` `;`

 `...`

A description of each instance variable follows.

*   `SynchErrorTypes` ` synchErrorType` - This is a general success or error response value. It will indicate either success or the type of error that occured. This will be set to one of the following three enums.

    `Defines` `.` `SynchErrorTypes.` **`success`** - Indicates success processing the `SynchDescriptor` associated with this `SynchResponse` object.

    `Defines` `.` `SynchErrorTypes.` **`exception`** - Indicates that an exception occurred processing the `SynchDescriptor` associated with this `SynchResponse` object. You will need to inspect the `exceptionSynchError` object for details.

    `Defines` `.` `SynchErrorTypes.` **`Processing`** - Indicates that a processing error occurred processing the `SynchDescriptor` associated with this `SynchResponse` object. You will need to inspect the `processingSynchError` object for details.
*   `ProcessingSynchError` ` processingSynchError` - If a processing type error occurred, this object will provide details describing the error. Otherwise it will be null.
*   `ExceptionSynchError` ` exceptionSynchError` - If an exception type error occurred, this object will provide details regarding the exception. Otherwise it will be null.
*   `bool` ` removeFlag`  - This indicates whether the replication entry in the replication log was deleted. If *true* , the entry was removed. The remove flag will be *true* whenever the the `synchErrorType` is success. Otherwise, it will be *true* for non-recoverable errors and *false* for recoverable errors.

**Writing a post-synchronization delegate**

A post-synchronization delegate can be used for any processing that you wish to perform. One typical use, is for correcting synchronization errors. As a general rule, I like to divide error processing and actual error correction between an error delegate and a post-processing delegate. By that I mean, an error delegate should only identify an error as recoverable or non-recoverable. The post-processing delegate should assume responsibility for taking action necessary to correct an error.

In the post-synchronization delegate example below, we start by checking to see if synchronization succeeded, this is done on line 1\. If `synchResponse.synchErrorType` is success, then synchronization worked. You know this because the `synchResponse` parameter passed to the delegate is the response returned from the last record in the `sdList` that was processed.

If synchronization failed, the code iterates through the `sdList` in order to find the `SynchDescriptor` that triggered the failure. This is done on line 2\. Line 3 then checks to see if the error is recoverable or non-recoverable.

Checking for success or failure, and then, if necessary, identifying the descriptor that caused an error, is very easy. What you decide to do with this information is specific to your particular application requirements.

 `public`  `static`  `async`  `Task` ` mySynchPostProcessDel(` `SynchDescriptor` ` originalSD, `

 `List` `<` `SynchDescriptor` `> sdList, `

  `SynchResponse` ` synchResponse)`

`  {`

**`1`**  `if` ` (synchResponse.synchErrorType == ` `Defines` `.` `SynchErrorTypes` `.success) `

`    {`

 *`// Do success Processsing here.`*

`    }`

 `else`

 `{`

 *`// Find the descriptor that failed.`*

 `foreach` ` (` `SynchDescriptor` ` sd ` `in` ` sdList)`

`      {`

**`2`**  `if` ` (sd.synchResponse.synchErrorType != ` `Defines` `.` `SynchErrorTypes` `.success) `

`        {`

 *`// Is this a recoverable error.`*

**`3`**    `if` ` (sd.synchResponse.removeFlag == ` `false` `) `

  `    {`

   *`// Recoverable error.`*

  `} `

  `else` 

  `      {`

   *`// Non-recoverable error.`*

  `  }`

 *`// Found. Get out after processing. Remaining response objects will be null.`*

 `break` `;`

`        }`

`      }`

`    }`

 `}`

Synchronizing to your own private back-end server

Up to this point, all of the synchronizing that we have done as been to HotRiot. While you have a lot of flexibility and control in designing how records should be synchronized, they are, nonetheless, still synchronized to the HotRiot system. This is by far the easiest and fastest way to get your app up and running, and in many instances, ideal. However, there are legitimate reasons for wanting to replicate your own private back-end. I’m not going to delineate why you might choose to do this. I assume if you’re seriously considering replicating to private server, that you have good reason. In order to support this requirement, SQLite.XM allows you to replace the default HotRiot synchronization with your own custom replication. This allows you to take over replication and synchronize to any server of your choosing.

The method signature for the custom synchronization delegate is shown below.

`public`  `delegate`  `Task` `<` `bool` `> ` `SynchDel` ` (` `List` `<` `SynchDescriptor` `> sdList);`

To replace the default HotRiot synchronization with your own replication, simply pass your synchronization delegate to the *`SxmInit.initialize`* method; see below.

`bool` `schema = ` `SxmInit` `.initialize(mySynchDel);`

`this` `.StartService (` `new`  `Intent` ` (` `this` `, ` `typeof` `(` `SynchronizeService` `)));` `  //` `For Android only.`

As you can see, the custom synchronization delegate returns a bool, and is passed the following parameter.

*   `List` `<` `SynchDescriptor` `> sdList` - This is the list of synch descriptors that need to be synchronized to your server. For the current version of SQLite.XM, this list will only contains a single entry, but that might change in future versions.

A partial listing of the `SynchDescriptor` class is shown below.

 `public`  `class`  `SynchDescriptor`

`  {`

 `public`  `string` ` action;`

 `public`  `string` ` dbName;`

 `public`  `string` ` tableName;`

 `public`  `SynchResponse` `synchResponse;`

 `public`  `Hashtable` ` recordDataToSynch;`

`  . . .`

A description of each instance variable follows.

*   `string` `action` -This is synchronization action that needs to be performed on this record. It will be *insert* when inserting a new record, *delete* when deleting a record, and *update* when updating or modifying a record.
*   `string` `dbName` -This is the name of the database on the device from where this record was retreived.
*   `string` `tableName` -This is the name of the database table from where this record was retreived.
*   `SynchResponse` `synchResponse` -This is the respons that is returned from synchronizing this descriptor. This can be ignored when performing a custom synchronization.
*   `Hashtable` ` recordDataToSynch` - This is the actual record data that needs to be synchronized to your server. The keys in the hash contain the field names while the value contains the actual field data.

If a descriptor is passed to your custom delegate with an *action* that is *delete* , then what is passed in the `recordDataToSynch` field? In this case, there will only be one entry in the hash table; the *systemSynchID* . As you know, the synch ID uniquely identifies a record, and as such, provides all the information that’s needed in order for a delegate to perform a delete.

How custom synchronization works

SQLite.XM starts by retrieving the first record in the replication log that needs to be processed. It then creates a `SynchDescriptor` based on this record. Your delegate is then called with the newly created descriptor passed in the `sdList` parameter. At this point, your delegate is in control and responsible for synchronizing the data in the descriptor. How and where you choose to replicate this data is entirely up to you.

Your delegate method returns either *true* or *false* , depending on whether it wants the record in the replication log that triggered this synchronization to be deleted or not. If it returns *true* , the entry is deleted. In this case, it’s assumed that replication for this log entry has finished to completion. SQLite.XM will then continue processing with the next entry in the replication log, if one exists. If *false* is returned, the log entry is retained. In this case, it’s assumed that the record did not replicate. Synchronization will then pause for a brief period of time. After pausing, it will again attempt to perform replication, starting with the record that failed to process.

This cycle is repeated for each entry in the log. When the last entry is successfully processed, synchronization goes into a wait state, waiting for an event notification. A notification is triggered whenever a record is inserted, updated, or deleted that needs to be synchronized.

Designing for custom synchronization

How and where you choose to replicate using a custom delegate is, of course, entirely up to you. However, there are few things to keep in mind as you prepare to engineer a design for custom synchronization. It’s entirely possible that certain type of errors will cause synchronization to send your delegate the same record multiple times. This could happen if your synchronization delegate sends a request to your server and the request is received and correctly processed but no answer is returned. This might occur because of a connection failure or because of some error in the server-side code. Not knowing whether or not a replication request was fully processed, your delegate will probably return *false* in order to ensure that the record is reprocess. Your server must be able to properly handle these types of conditions. For example, you server could be asked to delete the same record more than once or perform an insert of a record that already exists.

It’s strongly recommended that you include a `systemSynchID` field wherever you will be replication your device data, and that you replicate to this field. This is the only field sent in the `recordDataToSynch` hash table when an *action* is *delete* . So without it, you will be unable to fulfill a delete synchronization request.

We also recommend that you include robust error processing as part of your synchronization design. Replication needs to be viewed as an unreliable operation. This is mostly due to the transient nature and sporadic quality of network connections on mobile devices. Your error handler will be responsible for deciding which errors are recoverable and which are not. And it’s likely that some recoverable errors will need to be explicitly corrected. Now, I don’t want to get too deep into the specifics of a design, as that is highly dependent on the particulars of your synchronization. But you need to be careful not to design your error processing and correction logic in such a way that it could put replication into an endless cycle that prevents synchronization. For example, this could happen if your synchronization handler encounters an error that it considers recoverable but requires an explicit correction and that correction is never made

There is another, more insidious problem that you could encounter. It’s what I call a non-error timeout. It most often happens when trying to synchronize a large record with a poor connection. Imagine your delegate attempts to synch a record which includes a large video as a blob. Assume for this example, that the time it takes to transfer the record and synchronize the data exceeds the connection timeout interval. In this example, the synchronization request was successfully processed by your server but the code on the device received a WebException error with a timeout message. The error handler might rightly consider this a recoverable error that simply needs to be reprocessed. The problem, however, is not going away. Each time you try and replicate this record, your synchronization code receives the same result.

If your synchronization delegate throws an exception, the record from the replication log which triggered the exception will be removed from the log and will not be processed any further. Synchronization will continue with the next entry in the log, if one exists.

Writing a custom synchronization delegate

The listing below should help to get you going in writing your own custom synchronization delegate. It provides a skeleton and a workflow that can be used as the basis for building a handler. Naturally, it does not include the actual implementation specific synchronization logic. You would, of course, need to fill in these missing parts. This just presents one way you might go about structuring replication. It is entirely possible, given the specifics of your requirements, that there is another better design you might choose instead. But even so, this listing should be helpful in giving you some ideas as to how you might do things.

The `synchDelegate` method is the actual synchronization delegate. It starts by inspecting the *action* and calling the appropriate lower level action-specific routine. If an error or an exception is encountered during processing, it then calls the method `isErrorRecoverable` or `isExceptionRecoverable` . As their names imply, these methods determine if the error or exception is recoverable or not. If a recoverable error or exception is encountered, the overloaded method `performErrorCorrection` is called. This method is responsible for determining if an error requires an explicit correction, and if it does, for making the correction. Some errors may not require any action on the part of synchronization, for example, a connection error.

 `public`  `static`  `async`  `Task` `<` `bool` `> SynchDelegate (` `List` `<` `SynchDescriptor` `> sdList)`

`  {`

 `bool` ` removeSynchRecordFlag =` `true` `;`

 `SynchResponse`  `synchResponse =` `null` `;`

 `try`

`    {`

  `foreach` ` (` `SynchDescriptor` `synchDescriptor` `in` `sdList ) `

  `  {`

   `if` ` (synchDescriptor.action.Equals (` `"insert"` `) == ` `true` `)` 

  `  synchResponse = ` `await` ` synchInsert (synchDescriptor);`

  `if` ` (synchDescriptor.action.Equals (` `"update"` `) == ` `true` `)` 

  `      synchResponse = ` `await` ` synchUpdate (synchDescriptor);`

   `if` ` (synchDescriptor.action.Equals (` `"delete"` `) == ` `true` `)`

  `  synchResponse = ` `await` ` synchDelete (synchDescriptor);`

  `if` ` (synchResponse.synchErrorType != ` `Defines` `.` `SynchErrorTypes` `.success` `)`

`        {`

  `if` `(isErrorRecoverable (synchResponse) ==` `true` `)`

`           {`

`             removeSynchRecordFlag =` `false;`

 `performErrorCorrection (synchResponse); ` *`// Perform error correction.`*

 `break` `;`

 `}`

`        }`

`      }`

`    }`

 `catch` ` (System.` `Exception` ` ex) `

`    {`

  `if` `(isExceptionRecoverable (ex) ==` `true` `)`

`      {`

 `removeSynchRecordFlag =` `false` `;`

 `performErrorCorrection (ex); ` *`// Perform error correction, if necessary.`*

`      }`

`    }`

 `return` ` removeSynchRecordFlag;`

`  }`

 `public`  `static`  `bool` ` isErrorRecoverable (` `SynchResponse`  `synchResponse` `)` 

`  {`

 `bool` ` recoverableFlag =` `true` `;` *`// Default to recoverable.`*

  *`// Determine if the error is recoverable.`* 

*`    // Return true for recoverable and false for non-recoverable.`*

 `return` ` recoverableFlag;`

`  }`

 `public`  `static`  `bool` ` isExceptionRecoverable (` `Exception`  `ex` `)` 

`  {`

 `bool` ` recoverableFlag =` `true` `;` *`// Default to recoverable.`*

  *`// Determine if the exception is recoverable.`*

*`    // Return true for recoverable and false for non-recoverable.`*

 `return` ` recoverableFlag;`

`  }`

 `public`  `static`  `void` ` performErrorCorrection (` `SynchResponse`  `synchResponse` `)` 

`  {`

  *`// Examin the synchResponse and perform whatever`*

*`   //`* *`explicit errror correction that needs to be perofrmed.`*

`  }`

 `public`  `static`  `void` ` performErrorCorrection (` `Exception`  `ex` `)` 

`  {`

  *`// Examin the exception and perform whatever explicit`*

*`    //`* *`errror correction that needs to be perofrmed.`*

`  }`

The synchronization insert and update methods, `synchInsert` and `SynchUpdate` , are mostly blank. These methods need to be filled in with whatever code is needed to perform an insert and update synchronization operation. The synchronization delete method, `synchDelete` , is much more complete. It include logic that somewhat matches what is used by the default HotRiot delete synchronization handler. Of course, this will not work for you. It will need to be gutted and replaced with you own delete logic. We put the code there to help give you a feel for what a delete handler might look like.

 `private`  `static`  `async`  `Task` `<` `SynchResponse` `> synchInsert (` `SynchDescriptor` ` synchDescriptor)`

`  {`

  *`// Perform replication insert operation.`*

 `SynchResponse`  `synchResponse = replicateInsertRecord (synchDescriptor);`

 `return`  `synchResponse;`

`  }`

 `private`  `static`  `async`  `Task` `<` `SynchResponse` `> synchUpdate (` `SynchDescriptor` ` synchDescriptor)`

`  {`

  *`// Perform replication update operation.`*

 `SynchResponse` `synchResponse = replicateUpdateRecord (synchDescriptor);`

 `return`  `synchResponse;`

`  }`

 `private`  `static`  `async`  `Task` `<` `SynchResponse` `> synchDelete (` `SynchDescriptor` ` synchDescriptor)`

`  {`

 `SynchResponse` ` synchResponse = ` `null` `;`

 `NameValueCollection` ` recordData = ` `new`  `NameValueCollection` `();`

 `foreach` ` (` `DictionaryEntry` ` pair ` `in` ` synchDescriptor.recordDataToSynch) `

`    {`

 `if` ` (pair.Key.ToString ().Equals (` `"systemSynchID"` `) == ` `true` `) `

`      {`

`        recordData.Add (` `"systemSynchID"` `, pair.Value.ToString ());`

 `break` `;`

`      }`

`    }`

 `HRDeleteResponse` ` hrDeleteResponse = ` `null` `;`

 `hrDeleteResponse = ` `await`  `HotRiot` `.getHotRiotInstance.submitKeyDeleteRecord (`

 `synchDescriptor.tableName, `

 `recordData);`

 `if` ` (hrDeleteResponse.getResultCode () != ` `HotRiot` `.SUCCESS) `

`    {`

 `ResultDetails` ` rd = hrDeleteResponse.getResultDetails ();`

`      synchResponse = ` `new`  `SynchResponse` ` (SQLiteXM.` `Defines` `.` `SynchErrorTypes` `.processing, `

 `rd.ResultCode, `

 `rd.ResultText, rd.ResultMessage);`

`    }`

 `else`

`      synchResponse = ` `new`  `SynchResponse` ` (` `true` `, SQLiteXM.` `Defines` `.` `SynchErrorTypes` `.success);`

 `return` ` synchResponse;`

`  }`

Appendix A - SQLite Error Codes

**Error Name        **  **Description**

`Unknown         ` `The error code is unknown.`

`Ok             ` `Successful result`

`Error     ` `     SQL error or missing database`

`Internal` `         Internal logic error in SQLite`

`Perm             Access permission denied`

`Abort` `           Callback routine requested an abort`

`Busy           ` `The database file is locked`

`Locked           A table in the database is locked`

`NoMem            A malloc() failed`

`ReadOnly`  `      Attempt to write a readonly database`

`Interrupt`  `Operation terminated by sqlite3_interrupt()`

`IoErr      `  `Some kind of disk I/O error occurred`

`Corrupt` `          The database disk image is malformed`

`NotFound`  `Unknown opcode in sqlite3_file_control()`

`Full        `  `Insertion failed because database is full`

`CantOpen` `         Unable to open the database file`

`Protocol       ` `Database lock protocol error`

`Empty          ` `Database is empty`

`Schema`  `The database schema changed`

`TooBig          ` `String or BLOB exceeds size limit`

`Constraint`  `Abort due to constraint violation`

`Mismatch       ` `Data type mismatch`

`Misuse         ` `Library used incorrectly`

`NoLfs          ` `Uses OS features not supported on host`

`Auth           ` `Authorization denied`

`Format           Auxiliary database format error`

`Range    ` `      2nd parameter to sqlite3_bind out of range`

`NotADb` `           File opened that is not a database file`

`Notice           Notifications from sqlite3_log()`

`Warning          Warnings from sqlite3_log()`

`Row            ` `sqlite3_step() has another row ready`

`Done            ` `sqlite3_step() has finished executing`

`NonExtendedMask  Used to mask off extended result codes`

**Table of Contents**

[About this book](#text00000.html_filepos0000021182)

> > [Acknowledgements](#text00000.html_filepos0000021290)

> > [Conventions used in this book](#text00000.html_filepos0000022002)

> > [Code formatting](#text00000.html_filepos0000027830)

> > [Who this book is for](#text00000.html_filepos0000028612)

> > [How to use this book](#text00000.html_filepos0000029605)

> > [About the author](#text00000.html_filepos0000031571)

> > [Personal note](#text00000.html_filepos0000032976)

> > [Feedback](#text00000.html_filepos0000034261)

[Part 1\. Data persistence for mobile apps](#text00000.html_filepos0000034885)

> > [The nature of mobile applications](#text00000.html_filepos0000035025)

> > > > > > [SQLite](#text00000.html_filepos0000037150)

> > > > > > [Offline, online, and occasionally connected apps](#text00000.html_filepos0000039039)

> > > > > > [Is this some kind of joke?](#text00000.html_filepos0000043768)

> > > > > > [Do I really need all of this?](#text00000.html_filepos0000054691)

> > [Understanding Where HotRiot fits in](#text00000.html_filepos0000055268)

> > [Database design considerations](#text00000.html_filepos0000056873)

> > > > > > [Designing for SQLite](#text00000.html_filepos0000062371)

> > > > > > > > > > [Primary keys and foreign keys](#text00000.html_filepos0000063519)

> > > > > > > > > > [Structuring your database](#text00000.html_filepos0000066093)

> > > > > > > > > > [Defining fields](#text00000.html_filepos0000069947)

> > > > > > > > > > [Including primary keys](#text00000.html_filepos0000071576)

> > > > > > > > > > [Linking tables](#text00000.html_filepos0000072149)

> > > > > > [Searching a relational database](#text00000.html_filepos0000075031)

> > > > > > [Designing for Mongo synching](#text00000.html_filepos0000076360)

> > > > > > [Suggestions for designing your SQL](#text00000.html_filepos0000077756)

> > > > > > > > > > [Storing dates and times in SQLite](#text00000.html_filepos0000081790)

> > [Getting SQLite.XM](#text00000.html_filepos0000084233)

> > [Creating an application skeleton](#text00000.html_filepos0000085112)

> > [Platform specific code](#text00000.html_filepos0000089533)

[Part 2\. Data storage on the device](#text00000.html_filepos0000091119)

> > [Describing your apps databases](#text00000.html_filepos0000091245)

> > [Schema initialization](#text00000.html_filepos0000110589)

> > > > > > [Including a SQL statements properties file in Android](#text00000.html_filepos0000113410)

> > > > > > [Including a SQL statements properties file in iOS](#text00000.html_filepos0000114288)

> > > > > > [Parameterized queries](#text00000.html_filepos0000115959)

> > > > > > [Understanding the SQL statements properties file](#text00000.html_filepos0000118367)

> > > > > > > > > > [Defining table statements](#text00000.html_filepos0000120734)

> > > > > > > > > > [Defining insert statements](#text00000.html_filepos0000123775)

> > > > > > > > > > [Defining alter table statements](#text00000.html_filepos0000128118)

> > > > > > > > > > [Defining index statements](#text00000.html_filepos0000130354)

> > > > > > > > > > [Defining select, update, and delete statements](#text00000.html_filepos0000132623)

> > > > > > [Creating tables](#text00000.html_filepos0000134739)

> > > > > > [SQLite naming constraints](#text00000.html_filepos0000141830)

> > > > > > [Initializing the database](#text00000.html_filepos0000142886)

> > [Using the SxmTransaction class](#text00001.html)

> > > > > > [Inserting records into the database](#text00001.html_filepos0000165730)

> > > > > > > > > > [Committing transactions](#text00001.html_filepos0000188493)

> > > > > > > > > > [The insertResponse object](#text00001.html_filepos0000189589)

> > > > > > > > > > [Saving file attachments](#text00001.html_filepos0000191538)

> > > > > > [Updating records](#text00001.html_filepos0000197500)

> > > > > > [Deleting records](#text00001.html_filepos0000207304)

> > > > > > [Error Processing](#text00001.html_filepos0000213092)

> > > > > > > > > > [Initialization error processing](#text00001.html_filepos0000214220)

> > > > > > > > > > [The SxmException object](#text00001.html_filepos0000227718)

> > > > > > > > > > [Transaction error processing](#text00001.html_filepos0000230397)

> > > > > > > > > > [Programming for errors](#text00001.html_filepos0000256231)

> > > > > > > > > > [Some final thoughts regarding errors](#text00001.html_filepos0000263678)

> > > > > > [Searching the database](#text00001.html_filepos0000265131)

> > > > > > > > > > [Processing record data in-line](#text00001.html_filepos0000282273)

> > > > > > [Embedding SQL in your code](#text00001.html_filepos0000294967)

> > [Multi-database statement processing](#text00001.html_filepos0000297667)

> > [Understanding transactions](#text00001.html_filepos0000300456)

> > [Transaction visibility](#text00001.html_filepos0000310491)

> > [Performing joins across databases](#text00001.html_filepos0000324109)

> > [Locking and concurrency](#text00001.html_filepos0000341500)

> > > > > > [Deadlock conditions](#text00001.html_filepos0000362697)

> > > > > > [Nesting connections](#text00001.html_filepos0000364092)

> > [Serializing transactions using the SxmSTransaction class](#text00001.html_filepos0000393767)

> > [Dynamic Queries](#text00002.html)

> > > > > > [Using parameterized placeholders](#text00002.html_filepos0000409414)

> > > > > > [SQL Injection dangers](#text00002.html_filepos0000426210)

> > > > > > [Directly inserting query parameters](#text00002.html_filepos0000431568)

> > [Making schema changes](#text00002.html_filepos0000439022)

> > > > > > [Adding/Modifying tables](#text00002.html_filepos0000440050)

> > > > > > [Creating/Deleting indexes](#text00002.html_filepos0000445953)

> > > > > > [Dropping tables](#text00002.html_filepos0000451497)

> > [The SxmConnection class](#text00002.html_filepos0000452253)

> > > > > > [Creating an SxmConnection](#text00002.html_filepos0000454681)

> > > > > > [Using an SxmConnection](#text00002.html_filepos0000466309)

[Part 3\. Data synchronization to the cloud](#text00002.html_filepos0000475119)

> > [Understanding SQLite.XM synchronization](#text00002.html_filepos0000478055)

> > [Setting-up a server-side infrastructure](#text00002.html_filepos0000485954)

> > > > > > [Creating the replication database tables](#text00002.html_filepos0000488539)

> > > > > > [Activating synchronization in SQLite.XM](#text00002.html_filepos0000495620)

> > [Synchronization details](#text00002.html_filepos0000497740)

> > [Synchronizing files](#text00002.html_filepos0000502579)

> > [Coordinating synchronization](#text00002.html_filepos0000506845)

> > [Customizing synchronization](#text00002.html_filepos0000512290)

> > > > > > [Pre-synchronization processing](#text00002.html_filepos0000514012)

> > > > > > > > > > [Writing a pre-synchronization delegate](#text00002.html_filepos0000528424)

> > > > > > > > > > [Pre-synchronization abort conditions](#text00002.html_filepos0000562249)

> > > > > > > > > > [Multi-table synchronizations error processing](#text00002.html_filepos0000564324)

> > > > > > [Synchronization error processing](#text00002.html_filepos0000569461)

> > > > > > > > > > [Handling exception synchronization errors](#text00002.html_filepos0000579430)

> > > > > > > > > > [Handling processing synchronization errors](#text00002.html_filepos0000583403)

> > > > > > > > > > [Invalid data errors and non-unique data errors](#text00002.html_filepos0000587601)

> > > > > > > > > > [Writing a synchronization error handler](#text00002.html_filepos0000632899)

> > > > > > [Post-synchronization processing](#text00003.html)

> > > > > > > > > > [Writing a post-synchronization delegate](#text00003.html_filepos0000656671)

> > [Synchronizing to your own private back-end server](#text00003.html_filepos0000665866)

> > > > > > [How custom synchronization works](#text00003.html_filepos0000674515)

> > > > > > [Designing for custom synchronization](#text00003.html_filepos0000676107)

> > > > > > [Writing a custom synchronization delegate](#text00003.html_filepos0000679674)

[Appendix A - SQLite Error Codes](#text00003.html_filepos0000710459)