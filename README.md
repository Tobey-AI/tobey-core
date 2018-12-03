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

To build Tobey on your local dev environment, you need to clone/dowload the Core and the Foundation solutions.
**Foundation** is a .NetStandard library, hence why you need to pack the library and push it into you local Nuget feed which will be used by the **Core** solution to load the library and restore the packages.



## Tools needed

- Visual Studio 2017
- .Net Core 1.4 +
- Github Tools for Visual Studio



