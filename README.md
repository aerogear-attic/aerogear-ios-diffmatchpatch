# DiffMatchPatch for iOS / MacOSX

![Maintenance](https://img.shields.io/maintenance/yes/2017.svg)
[![circle-ci](https://img.shields.io/circleci/project/github/aerogear/aerogear-ios-diffmatchpatch/master.svg)](https://circleci.com/gh/aerogear/aerogear-ios-diffmatchpatch)
[![License](https://img.shields.io/badge/-Apache%202.0-blue.svg)](https://opensource.org/s/Apache-2.0)
[![GitHub release](https://img.shields.io/github/release/aerogear/aerogear-ios-diffmatchpatch.svg)](https://github.com/aerogear/aerogear-ios-diffmatchpatch/releases)
[![CocoaPods](https://img.shields.io/cocoapods/v/DiffMatchPatch.svg)](https://cocoapods.org/pods/DiffMatchPatch)
[![Platform](https://img.shields.io/cocoapods/p/DiffMatchPatch.svg)](https://cocoapods.org/pods/DiffMatchPatch)

The project is a fork of [google-diff-match-patch](https://github.com/JanX2/google-diff-match-patch)
with modifications to get it to compile for iOS / MacOSX and Xcode 9

The speed test target and schema were removed to save time figuring out some issues but might
later on.

## Prerequisites
This project requires Xcode 9.0 to run.

## Building

Building can be done by opening the project in Xcode:

    open DiffMatchPatch.xcodeproj

    xcodebuild -scheme DiffMatchPatch build

    xcodebuild -scheme DiffMatchPatch-OSX build

## Testing
Tests can be run from with in Xcode using Product->Test menu option (CMD+U).  

You can also run test from the command:

    xcodebuild -scheme DiffMatchPatch -destination 'platform=iOS Simulator,name=iPhone 5s' test

    xcodebuild -scheme DiffMatchPatch-OSX  test


## CocoaPods
This project can be made into a [CocoaPods](http://www.cocoapods.org/):

First install the CocoaPods gem by running:

    sudo gem install cocoapods --pre

Then you can verify that the podspec is correct:

    pod spec lint DiffMatchPatch.podspec --verbose --allow-warnings

If all goes well you are ready to release. First, create a tag and push:

    git tag 'version'
    git push --tags

Once the tag is available you can send the library to the Specs repo. For this you'll have to follow the instructions in ["Getting Setup with Trunk"].

    pod trunk push DiffMatchPatch.podspec
