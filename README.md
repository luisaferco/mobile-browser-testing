# mobile-browser-testing
A simple project with webdriverIO to test on mobile browsers 

## Description 📖
An example project to run Appium tests with WebdriverIO for iOS/Android Hybrid Apps

## Starting 🚀

### Prerequisites
You need to install:
- Node.js, a Long-Term Support (LTS) release version 16 or later - [download](https://nodejs.org/en/)
- Appium with npm install appium -g
- Appium on a local machine [download](https://github.com/appium/appium-desktop)
- Chrome web browser - [download](https://www.google.co.uk/chrome/)

# Preparación del ambiente

we will be working with Windows, therefore the installations that
we will see here will be on that operating system. It is important to mention,
however, *Appium* can be used both in macOS and in different Linux
distributions.

### Appium

1. Once nodeJS is installed, download appium through following command on proyect path:
    
    ```bash
    npm install -g appium
    appium
    ```
    
2. Appium also has a graphical interface that can be downloaded [here](https://bitbucket.org/appium/appium.app/downloads/) 

## How to configure capabilities 

<aside>
💡 Prerrequisites: must have installed adb
</aside>

Enable Developer Options and USB debugging in mobile device. Connect the device to desktop computer and make sure was correctly connected through following command via cmd: 

```bash
adb devices
```

A list of connected devices should be displayed 

Some crusial capabilities should be configure on <wdio.config.ts> with which Appium requesta a mobile device connection.

`PlatformVersion`: adb -s "deviceId" shell getprop ro.build.version.release
`DeviceName`: adb -s "deviceId" shell getprop ro.product.model
