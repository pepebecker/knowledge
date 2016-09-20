# Install Android SDK on macOS

## Install the Android SDK

```
brew install android-sdk
```

## List all Packages

```
android list sdk --all
```

## Install a Package

```
android update sdk -u -a -t <package-number>
```

## Create Android Virtual Device

```
android create avd -n <name> -t <targetID>
```

## Start Emulator

```
emulator -avd <device-name>
```

[Go Back](README.md)