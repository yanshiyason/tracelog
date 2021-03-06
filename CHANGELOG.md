# Change Log
All significant changes to this project will be documented in this file.

## [4.0.1](https://github.com/tonystone/tracelog/tree/4.0.1)

#### Fixed
- Adding missing newline to `ConsoleWriter` output (issue #55).

## [4.0.0](https://github.com/tonystone/tracelog/tree/4.0.0)

#### Added
- Added mode to TraceLog.configuration to allow direct, async, or sync mode of operation. Sync & direct mode are useful for use cases that have short-lived processes (scripts) or require real-time logging.
- Added ability to set the concurrency mode individually for each Writer.
- Added `FileWriter` class for writing to local log files.
- Added `TestHarness` to assist developers in testing their own `Writer` types.
- Added `shell` utility to assist in testing `Writer` types.
- Added TraceLogTestTools module/library to allow use of new `TestHarness` and other Utilities.

#### Removed
- Removed all Xcode projects, Xcode projects are now generated using Swift Package Manager.
- Dropped iOS 8 support.

## [3.0.0](https://github.com/tonystone/tracelog/tree/3.0.0)

#### Updated
- Xcode projects to be swift 4.1 compatible.

#### Removed
- Removed deprecated `TLLogger.configure()`. Use TraceLog.configure in swift instead.
- Removed deprecated `TLLogger.configureWithEnvironment`.  Use TraceLog.configure in swift instead.


## [2.2.0](https://github.com/tonystone/tracelog/tree/2.2.0)

#### Updated
- Change build environment requirements to xcode9.2 / Swift 4.0.3 (note: this is just the build, targets are still the same).

## [2.1.0](https://github.com/tonystone/tracelog/tree/2.1.0)

#### Added
- Log level `OFF` to allow turning off logging for a specific level (global, prefix, tag).

## [2.0.2](https://github.com/tonystone/tracelog/tree/2.0.2)

#### Added
- Added required tests to bring coverage back to 100%.

#### Updated
- Deprecated TLLogger.configure and TLLogger.configureWithEnvironment.  Use TraceLog.configure in swift instead.
- Changed Vagrant file to include libpython2.7 required for Swift REPL.

#### Fixed
- Removed unnecessary String with formatters call that can result in a crash if the interpolated string includes formatter options that the String(format:) function will never have matching parameters for.

## [2.0.1](https://github.com/tonystone/tracelog/tree/2.0.1)
Released on 2016-10-16.

#### Added
- The `OS_ACTIVITY_MODE` environment variable to iOS and OSX Example.
- CHANGELOG.md

#### Updated
- Inline documentation for all public classes and functions.
- Combined TraceLog.configure func's into one with the same symantics as the 3 previous funcs.
- iOS example application converting it to Swift.

#### Fixed
- Cocoadocs documentation creation.

## [2.0.0](https://github.com/tonystone/tracelog/tree/2.0.0)
Released on 2016-10-15.

#### Added

- Installable Writers to allow custom writers to be used to write to various output devices/end points such as HTTP services, sys log, files, etc
- Ability to configure the environment statically at the beginning of the application
- **Swift 3** Compatibility
- **Swift Package Manager** support
- **Linux** support
- Now written in Swift 3
