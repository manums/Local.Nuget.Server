# local.nuget.server

This contains two projects:
  - Local.Nuget.Server.4.5.2
  - SharedLogger

Local.Nuget.Server.4.5.2 is a simple web application which creates a local nuget server using ASP.NET web application. Simple steps to follow are listed here:
http://www.hanselman.com/blog/HowToHostYourOwnNuGetServerAndPackageFeed.aspx

Before you can host a nuget store locally and enable publishing to that, you can create nuget package from you csproj or existing dll. Make sure you have necessary prerequisities, you can download Nuget CLI from here: https://dist.nuget.org/index.html

SharedLogger project is a simple C# class library which is packed as nuget package. Guide to create a nuget package from project\dll is explained here: http://docs.nuget.org/ndocs/quickstart/create-and-publish-a-package

You will have to modify packagesPath, apiKey while hosting nuget server locally to point to your local path and your api key (this key is used as security token to push nuget's to your locally hosted store).

## Note
Nuget.Server version 2.11.2 is not built for 4.6, if you're compiling your project with 4.5.2 and below use nuget.Server package version 2.10.3 and below.

Issue details are here: https://github.com/NuGet/NuGetGallery/issues/3072
