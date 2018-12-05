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
All dependancies that **Core** has, have been implemented as .NetStandard libraries that can be cloned/downloaded from GitHub as well.
At the current moment, you need to compile any dependancy manually before being able to compile Core.

Please follow these steps to get your DEV environment up and running:

- Create a local Nuget feed. To do so, You can follow this simple steps from this [Official Visual Studio article](https://docs.microsoft.com/en-us/nuget/hosting-packages/local-feeds).

- Clone and compile the **Foundation** solution. This is an isolated component which doesn't have explicit dependancies with any other project, hence why it will compile without any issue.

- Pack **Foundation** and push the Nuget package into your local Nuget feed. This step is needed to share the library with all other components.

- Clone and compile the default Skills which are: **tobey-skill-datetime**, **tobey-skill-weather**, **tobey-skill-search**, **tobey-skill-greetings**. Keep in mind that each skill project has a dependancy with **Foundation**.

Make sure to pack these libraries and store the resulting Nuget packages in your selected local Nuget feed.
- Now you can finally restore the packages in the **Core** project and build it.

## Tools needed

- Visual Studio 2017
- .Net Core SDK 1.4 +
- Github Tools for Visual Studio

## Contributing

If you would like to help and be part of this project, Tobey is 100% open source which means you can start contributing right now.
Just please follow the [Contributing Guide](/.github/CONTRIBUTING.md) we prepared for you.
