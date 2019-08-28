---
layout: post
title: 'PR1: MVC versus WPF - The rivalry that wasn't!'
author: Ashish
categories: [ Article ]
image: 
---
 
Apples and Oranges (with a caveat). <br/>They are very different technologies with a little bit of overlap. I have seen several people asking questions about these two over the past couple of years and there seems to exist some confusion.

<b>WPF</b>

Window Presentation Foundation is a successor of Windows Forms application development. Windows Forms has been around for a long time. Its current incarnation has been a part of the .NET stack from the beginning, and was spawned from Visual Basic form projects that came before. Unfortunately for WinForms developers, Windows Forms is in maintenance mode; no new development. It is just too old and is being retired.

WPF is taking over the mantle for graphical desktop client applications in .NET. Where WinForms was written from the standpoint that applications are fine if they are utilitarian but functional, WPF strives to make the application interactive and pleasing to the eye as well as functional. WPF offloads the majority of the rendering to the graphics hardware by leveraging DirectX. This allows the application to do more with the interface while freeing up CPU resources to process the logic.

WPF applications are typically written in two languages. XAML (eXtensible Application Markup Language) is an XML based markup that describes the layout of the page or the View. XAML incorporates the elements, styling information, transformation and animation. The other language is either a CLR language, VB.NET and C# primarily or more recently, Javascript.

WPF is also designed from the beginning with a more intelligent structure in mind. WinForms relied on the codebehind (a partial class that helped describe the form) to supply the logic. This tied the view directly to the logic so that when you press a button, a handler does something, and sets the color of this element, and changes the visibility of that element, and changes the mouse cursor, etc. For anything but the simplest forms, this became a huge mess very quickly (one can use a modified MVVM [more on that in a minute] format in WinForms, but it is not designed with that in mind, and there are severe limitations). WPF provides a more robust data binding mechanism to allow for the separation of the View and the Logic. The MVVM (Model-View-ViewModel) pattern promotes the separation of concerns that WPF is designed for.

WPF works best when your application is used inside the network. It runs in the user session so it can take advantage of Windows account credentials. Also, when you need lots of complex data displayed, it works very well with graphs and charts and dynamic hierarchy controls and so forth.

<b>MVC</b>

People talk about MVC, but they really mean ASP.NET MVC. MVC (Model View Controller) is similar to MVVM described above. It is a way of separating the UI (the View) from the data (the Model) with a layer that processes the data and gives the view what it needs to display.

ASP.NET MVC has some commonality in this regard to WPF. Both separate the View from the Data, both describe the view in a markup language (HTML in ASP.NET MVCs case). ASP.NET MVC has been gaining a lot of ground due to the rise in need of mobile applications. Where WPF applications must be run from a Windows machine, ASP.NET MVC web applications can be run on anything that uses a modern browser. Also applications are easily written so that the user can be nearly anywhere (in the local network, somewhere else on the internet) and can use the application.

By default, and without specialized controls for the page, ASP.NET MVC does not display large amounts of data in graphs and charts very well. It is not designed to. Additionally, it is not designed to be as smooth and interactive be default as WPF applications are. The vanilla ASP.NET MVC application is not a Single Page Application and thus page loads disrupt smooth application flow. Single Page Applications can be made, but they require extensive additional work.

So, ASP.NET MVC works well when you need your application mobile and available to users cross platform. It does not do well when moving large amounts of data around or displaying it on the screen.
Is WPF going away?

I have been hearing this questions since 2010 (not long after WPF came about in .NET 3.0). There is no indication that WPF is being phased out. Microsoft last year phased WinForms into maintenance mode. Unless they release a successor to WPF, there are unable to phase out WPF or they will be left with no viable desktop application authoring framework. WPF isn’t going anywhere. New features are continually being added to it, and Mark Twain would have some things to say about the rumor going around about its imminent demise.
Which should I use?

As with any technology conundrum, you use whichever most satisfies your needs. If you are writing an application that is customer facing, and those customers are expected to access the application from outside your network, you might consider ASP.NET. While Silverlight (WPFs web cousin) can handle things like that, I have not yet had enough experience with Silverlight to form a good opinion of it.

If your application is an internal tool for your company to use and you are displaying tons of data (and you would normally write it in Winforms) consider WPF.

Weigh the pros and cons, make a proof of concept to get a feel for how the application will work. These are not two competing technologies really, they are more like a wrench and a screwdriver. Both of these tools are used to turn something. What that something is determines which tool you use. Or you could use the hammer and just beat the offending something into a mash with WinForms.
