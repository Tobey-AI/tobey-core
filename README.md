# Tobey [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

Tobey is an open source smart assistant completely implemented in .Net Core. it can run everywhere also on a Raspberry Pi running Windows IOT.

## Getting Started

Tobey solution is organized into 2 main components.

### **Core component**
This is the main component which handles the STT functionality and orchestrates the interaction with the TTS engine, the NLP Engine and all skills registered into the system. Core is implemented as a UWP app which can potentially be extended to offer UI capabilities to the system.

### **Foundation component**
This is the component which exposes the NLP Engine and all other common methods and functionalities shared across all other components. This is a .Net Standard library. 

## Skills
Each skill needs to be implemented as a separate .Net Standard library to be referenced in the Core project as a separate Nuget package.

## Building the DEV environment

To build Tobey on your local dev environment, you need to setup a local Nuget feed.




## Tools needed

- Visual Studio 2017
- .Net Core 1.4 +
- Github Tools for Visual Studio



