# Tobey [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

Tobey is an open source smart assistant completely implemented in .Net Core. it can run everywhere also on a Raspberry Pi running Windows IOT.

## Architecture

Tobey solution is organized into 2 main components.

### **Core (tobey-core)**
This is the main component which handles the STT functionality and orchestrates the interaction with the TTS engine, the NLP Engine and all skills registered into the system. Core is implemented as a UWP app which can potentially be extended to offer UI capabilities to the system.

### **Foundation (tobey-foundation)**
This is the component which exposes the NLP Engine and all other common methods and functionalities shared across all other components. This is a .Net Standard library. 

### Skills
Each skill needs to be implemented as a separate **.Net Standard library** to be referenced in the **Core** project as a Nuget package.
There is a set of preconfigured Skill already activated in the Core. Skills like Date and time, Weather, Search, Ip lookup, are all pre-loaded into the Core component.

## Building the DEV environment

The first thing to do to get Tobey on your local dev environment, is to clone/dowload the Core solution.
All dependancies that Core has have been implemented as .NetStandard libraries that can be cloned/downloaded from GitHub as well.
At the current moment, you need to compile any dependancy manually before being able to compile Core.

- Clone and compile Foundation. This is an isolated component which doesn't have explicit dependancy, hence why will compile without any issue.
- Pack Foundation and push the nuget package into your local Nuget feed. Thisstep if needed to share the library with the other components.
- Clone and compile the default Skills which are: tobey-skill-datetime, tobey-skill-weather, tobey-skill-search, tobey-skill-greetings.
Make sure to pack these libraries and store the nuget package in your selected local nuget feed.





**Foundation** is a .NetStandard library, hence why you need to pack the library and push it into you local Nuget feed which will be used by the **Core** solution to load the library and restore the packages.



## Tools needed

- Visual Studio 2017
- .Net Core 1.4 +
- Github Tools for Visual Studio



