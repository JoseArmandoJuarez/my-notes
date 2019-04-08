## What is an Android??
* is an operative system for mobile devices
* Based on the linux kernel
* Powered by Dalvik
* Apps are written in Java

---

## Basic Architecture Of ANDROID!
### APPS
* Contacts, phone, browser….
### APPLICATION FRAMEWORK
* Provides the services that are needed by Android app to run
* Window manager, Telephone manger, Location manager, Resource manager
### LIBRARIES
* Provide API’s for various functionalities SQLite, Webkit, SSL, OpenGL
### ANDROID RUN TIME
* Used by Application and some systems services an android
### LINUX KERNEL
* Interacts with the hardware
---

## ANDROID APP
* Intents
    * Use to transfer data between Activities.
    * Action: the action to be performed, which is indicated as a string
    * Data: the data on which the action will operate
    * Example: A phone call intent
    * Call - action
    * Phone # - data
* Activity 
    * Is a single screen with or singular interface (a device or program enabling a user to communicate with a computer)
* Service 
    * Is an application component that performs a usually long running operation in the background while not interacting with the user
    * Example: A service for playing music
* Content Provider 
    * Provides a structure interface to a set of data.
    * Example: a set of pictures or media files in general 
    * Can also share data with other applications (an address book)
* Broadcast Receiver
    * Can be registered to receive system or application events.
    * Example: A music player can use a broadcast receiver to register for the event of incoming phone calls
* Manifest
    * Is what keeps an android application together
    * Is an XML file that declares, among other thing all of the steady components of the app. Activities, services and content providers.
    * It declares all the permissions required for the app to work
    * It also specifies the entry point of the application. That is which activity should be launched when the application is executed, that means when you click on app to start the app up the system will look into the manifest to see which activity has to be started
    * Declares the version
