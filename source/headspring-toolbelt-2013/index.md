Here is the toolset that we consider the "happy path" at Headspring.  We get to choose the majority of tools on most projects and we are extremely efficient when we get to run with tools of our choosing.  

##Communication
HipChat - All of the developers actively communicate via HipChat.  If you are running into a challenging problem this is a great place to bounce ideas off other developers.  We create chat rooms for each project so we can easily update other team members of our status or current blocking issue.

##Source Control
Git has proven out to be the winner in version control.  Excellent Git support is provided by Github and BitBucket.

Github - One great advantage that GitHub adds to the mix is some features on top of Git. The ability to comment on lines and review code within pull requests gives us a flexible workflow, the ability to share knowledge, and most importantly a tool for getting things done.

BitBucket - BitBucket has  a more competitive pricing structure than Github so we often use them for client work.

##Project Management

Github Issues - Github issues, pull requests, and code reviews has worked wonderfully on our client projects.

JIRA - On larger projects with heavier documentation processes we use JIRA to manage tasks.

##ORM (Object Relational Mapper)

NHibernate - Headspring was an early proponent of NHibernate and continues to use NHibernate successfully on many projects.  NHibernate offers mapping to custom types (like our Enumeration class), global filtering for Multitenant databases, 2nd level caching out of the box, which makes it still one of the most powerful free ORMs out there.

PetaPoco - When you need a complex query to hydrate a collection of objects as quickly as possible this micro ORM is what we use.

##Database Tools

RoundhousE - We manage our database migration scripts using RoundhousE.

NHibernate Profiler - NHibernate profiler helps ensure you are not abusing NHibernate so it helps reduce surprises in production.

ExpressProfiler - A barebones, show-me-the-SQL tool for SQL Server.  An open source, free alternative to NH Profiler or the tooling built into SQL Server.  http://expressprofiler.codeplex.com/

Visual Studio Database Project - Begining with Visual Studio 2010 The database project provides a way to manage all aspects of a SQL server database.  The artifacts are all stored in files that allow the database to be versioned in source control.  Artifacts such as tables, views, procedures, and functions are defined in their current state.  This is the main difference when compared to RoundhousE which stores sequentual modification scripts that have to be applied in a specific order.  The deployment uses VSDBCMB.exe to generate a differential script that will synchronize any database target.  Then end result will update the target database to match the Database Project definitions for all objects.  A Pre and Post deployment script section is provided to customize how data can be updated.  This uses SQLCMD to execute TSQL scripts.

##Databases

SQL Server - 

Oracle - 

MongoDB - A very good open source document database. 

RavenDB - 

##Eventing/Messaging

NServiceBus - Our defacto technology for building distributed systems is NServiceBus.  We use it to do pub/sub where publishers send reliable asynchronous messages to subscribers which allows you to decouple services in your system.

##Validation

Fluent Validaiton - A great library for producing readable and testable validation code.

##IOC (Inversion of Control) Container

Structure Map - Using IOC and dependency injection allows us to make our code extremely testable and clearly state our dependencies via constructor injection.

##Test Tools  

NUnit - NUnit has evolved with the times and kept up as a good starting point for .NET projects.

XUnit - XUnit is becoming the preferred testing framework of many new projects.  XUnit has more flexibility and some plugins not found with NUnit.

Autofac - We use Autofac with XUnit to automatically populate test method parameters.  The auto population of test parameters saves you from lots of object setup code when creating tests.

Visual Studio - Load testing and automated web performance testing can be done in a snap using Visual Studio's web testing tools.  You need the Premium version of Visual Studio 2012 to do these tests.

##Logging

Elmah - 

Log4Net - This is the long running workhorse for doing logging for most .NET development.

NLog - NLog is comparable to Log4Net.  Some developers prefer NLog over Log4Net because it is easier to setup and manage the logging configuration files.

##Website Monitoring

Glimpse - 

New Relic - For production website monitoring you cannot go wrong with New Relic.

##JavaScript

We use lots of JavaScript tools at Headspring and I will highlight the major ones here.

Backbone - When the JavaScript on a page grows sufficiently that you need to start managing the client side logic more formally then we start using Backbone.  If the page is sufficiently complex then we will use Backbone and Marrionette.

RequireJS - Newer projects are managing JavaScript dependencies via RequireJS.

Kendo UI - 

D3 - 

##CSS Frameworks

Bootstrap - 

Foundation - 

##Excel File Manipulation

GemBox - 

##.NET Libraries
Automapper - 
Enumeration - 



