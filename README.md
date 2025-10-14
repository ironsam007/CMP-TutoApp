# Initial project setup:
Initial project could be generated from Kotlin Multiplatform Wizard and choosing shared UI with CMP UI framework

## Project Arch:
### Project files:
- ComposeApp: code that will be shared across CMP applications, contains:
  - androidMain: Kotlin code that will be compiled per android
  - desktopMain: Kotlin code that will be compiled per desktop
  - iosMain    : Kotlin code that will be compiled per ios
  - commonMain: Code that is common for all targets, Most of the code should be Here in such project
  NB: In each one of this you have full access to ptfm specific libraries, OS dep... example: android.context
  
- IosApp: contains iOS applications. needed as an entry point for ios app. SwiftUI code could be added here for more developpement


## Adopted Arch: 
This app is single feature[self cotained], with a clean arch data-domain-presentation
Dev: start with what the actual problem the app is solving[feat: fetching book list]: domain layer, then presentation then data sources

- Clean Arch :
  - This app is a single feature (book - //here: looks very much self contain)
  - each feature contains 3 clean arch layers: data, domain, presentation