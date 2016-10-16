I am more frequently asked this question than anything else, maybe, since some of my work relates to building and using APIs. Often, beginners have the problem of understanding the concepts API, library, and a framework. This is not surprising at all, since some of these concepts are used interchangeably!

But i would like to make an effort here  to distinguish between these concepts and make it clear.

Let's say we are trying to build a web based application that we would like to record our parent's day to day health information, the medicines they are using and the food they are eating, the blood pressure levels and etc.

We want to log this information.

The first question we face is what languages/frameworks we would use?

Brilliant. Here we are forced to make some decisions.

There are two sides of a web application, the client side, referring to the user interface that users will interact with and the server side, where we probably store, fetch data from a database etc.. and probably do something else that cannot be easily done at the user interface level.

Client side choices are limited and set in stone for web applications.  HTML for content, CSS for presentation and JavaScript for behavior. But sooner or later, we might have to make some choices for frameworks and libraries. Let's say we chose Angular.js as one of our framework choices, and a couple of libraries to help us with that, such as Lo-Dash and jQuery.

Although many programming environment choices exist,on the server side, let's say we chose C#.

C# is one of the many .NET languages that can be used in the .NET world. The .NET Framework enables us to build many kinds of applications.

Usually people do not re-invent the wheel. They would like to use existing code and focus on the application requirements.

The .NET framework provides a huge set of libraries (pre-existing code) for application developers to use.

For example in our application, since we are doing a day to day logging of activities, we might want to know what day is today. So what do we do? We make use of an existing library and call one of it's behaviors.

For example, System.Date.Now would give us the current date and time, on the local computer.

Here we have not checked our system's clock and get the information from there. We don't care how System.Date.Now works. We just want to use it.

.NET calls it built-in library system as Base Class Libraries, referring to the huge list of pre-existing code to do stuff for us.

.NET also has the concepts of frameworks such as the ASP.NET framework, the WPF, the Web API, and so on.. These are a grouping of related libraries that help in developing in certain kind of applications. Also sometimes, these frameworks might have certain infrastructure to help execute our application. For example, the ASP.NET has an ASP.NET runtime, an engine that manages the lifecycle of an ASP.NET web application.

Sometimes however, we have very specific requirements. Let's say sometimes our application is crashing and we want to know where it's happening and log all such crashes.

We could write our own code to do that or use an existing library to do work for us.

A popular choice in the .NET world is the log4net library.

And then we code away, our server components.

Sometimes we might want some functionality, but that might not be present. So we may create our own library and share it across our teams and may be give it to the world, if it is a generic functionality, by starting an open source project on GitHub and people can then make use of our code in their applications.

Internal libraries are very common. Some teams might develop a library that does some business logic and takes care of a certain business concern and give it to other teams to use in their applications.

"API" is a 3 letter acronym that stands for Application Programming Interface. The key concept here is it is an interface and a way to interact for the application programmers.

So, a library being the actual code, and all the code that makes it a "library", when we interact with the library classes, functions, methods etc, we are said to access the API.

A call that can be made to the library is basically an API.

For example, when we are trying to develop our user interface, we frequently visit the jQuery API documentation.




The above is a snap shot from the jQuery site. Notice that jQuery is mentioned as a feature rich library, and yet we have the term API describing the behaviors that jQuery supports. For example, one behavior that jQuery supports is making AJAX calls.

A library is a set of behaviors and each behavior is an API and we make an API call when we use that behavior in our code. We do not need to understand how the actual implementation or inner workings of the call. We just make a call to one of the library's behaviors.

For example, the API call we would make use of to make AJAX requests is the $.ajax() and we would pass in necessary parameters.

Sometimes an API call returns us some data, some times it does something else, for example log something to a file etc..

It doesn't matter what programming language you use, or what environment you are coding against, re-usable code is available, in the form of libraries, modules, packages etc.

A framework on the other hand specifies how we are going to build our application. It provides us certain philosophy, and certain approach in our application development.

For example, the ASP.NET team has an MVC framework and ASP.NET traditional web framework. The philosophy behind these two frameworks are different. The MVC framework forces the application developer to think in terms of the MVC architectural pattern. These two frameworks work differently although they run on the same runtime. Each framework has it's own set of libraries that facilitate application development.

It's important to understand the concept of framework because what application we are trying to build provides us with many kinds of framework options.

An example is building a Web API.

What's a Web API?

A web api is also an API. You make calls/requests and some action is performed or data is returned. The only difference is you don't have a library that you download and import in your project.

You make HTTP requests on the network. They are http endpoints. Sometimes, you  have calls that make use of data.

For example in our application, let's say we have parent/log as a resource and we provide an http end point.

HTTP verbs are normally used to specify what we are doing with a resource.

Let's say we are just fetching yesterday's day.

So we might design our API in such a way that people can use our API.

We can say

Use the GET verb and make a request to

                       http://ourParentsHealthApi/user/parent/mom/log/4-10-14

and people can use that in their applications.

One benefit about web apis are they are not restricted to a specific programming language or environment.

People of the ruby world, python world or the node world can make use of this API by issuing http requests.
They can use it in their web, mobile, desktop, data, console applications. Where ever they want!

So that's the beauty of a web api.

