A simple fastlane setup for submit to Apple Testflight.

## Pre-setup
Make sure dont have any issue regarding [distribution private key](https://stackoverflow.com/questions/16563364/how-can-i-add-private-key-to-the-distribution-certificate/16563683)

## Fastfile
Contains script to submit testflight only. Need to edit based on project name and scheme

## env.beta
A file contains environment variables to be loaded to shell before start executing. Otherwise, fastlane command will keep prompt to enter email, choose team id, etc.

Run `source env.beta` in Terminal in order to load.

## Finally
Sit down and wait. It usually take around 15 - 20 minutes to submit and wait for complete processing in email.

![][screenshot.png]

## Reference
For details, refer to [https://github.com/fastlane/fastlane/](https://github.com/fastlane/fastlane/)

