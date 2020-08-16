---
layout: post
title: The choice between .NET Core and .NET Framework
---

I have a few friends (most are developers) who are starting a new project or even working on an existing project have encountered the following question:

## Should I choose .NET Core or .NET Framework?

![.NET Core]({{ site.url }}/images/posts/dotnet-core.PNG)

I would say that you should always go for .NET Core, if you can!

Actually, this shouldn't be a very hard question if you know the ecosystem and the technical environment of your company and fell confortable aswering 5 questions that will lead you to the final answer:

- Do you need and will you be able to share essencial codes, libraries, packages and data between the new project and the current ones?
- Does your application (web/service) need to run on multiple platforms (Windows, Linux, and macOS)?
- Does your system need the best possible performance and scalability?
- Does your team have experience and feel comfortable with .NET Core?
- Do you need a docker containers support?

So basically if you have answered YES for all the questions above, go for .NET Core... and don't forget that .NET 5 is coming soon!
