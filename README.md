# Tobey [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

Tobey is an open source smart assistant completely implemented in .Net Core. It runs everywhere, on Desktops, Mobiles and also on a Raspberry Pi running Windows IOT.

## Architecture

Tobey solution is organized into two main components.

### **Core (tobey-core)**
This is the main component which handles the STT functionality and orchestrates the interaction with the TTS engine, the NLP Engine and all skills registered into the system. Core is implemented as a UWP app, which can potentially be extended to offer some additional UI capabilities to the app.

### **Foundation (tobey-foundation)**
This is the component which exposes the NLP Engine and all other Common methods and functionalities shared across all other components. This is a .Net Standard library, hence why it needs to be packed into a NuGet package in order to be used.

### Skills
Each skill needs to be implemented as a separate **.Net Standard library** to be referenced in the **Core** project as an additional Nuget package.
There is a set of preconfigured Skills already activated in the Core; Skills like Date and time, Weather, Search, are all pre-loaded into the Core component.

## Building the DEV environment

The first thing to do to get Tobey on your local dev environment, is to clone/dowload the Core solution.
All dependancies that Core has have been implemented as .NetStandard libraries that can be cloned/downloaded from GitHub as well.
At the current moment, you need to compile any dependancy manually before being able to compile Core.

Please follow these steps to get your DEV environment up and running:

- Create a local Nuget feed. To do so, You can follow this simple steps from the Official ["https://docs.microsoft.com/en-us/nuget/hosting-packages/local-feeds"](Visual Studio article).

- Clone and compile Foundation. This is an isolated component which doesn't have explicit dependancy, hence why will compile without any issue.
- Pack Foundation and push the nuget package into your local Nuget feed. This step if needed to share the library with all other components.
- Clone and compile the default Skills which are: **tobey-skill-datetime**, **tobey-skill-weather**, **tobey-skill-search**, **tobey-skill-greetings**.
Make sure to pack these libraries and store the resulting nuget packages in your selected local nuget feed.
- 





**Foundation** is a .NetStandard library, hence why you need to pack the library and push it into you local Nuget feed which will be used by the **Core** solution to load the library and restore the packages.



## Tools needed

- Visual Studio 2017
- .Net Core 1.4 +
- Github Tools for Visual Studio



