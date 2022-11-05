# XcodeAndFastlaneHelp

##  Uplading to testflight
1. If Ipa upload is failing for Testflight
  - check if the current version and build is already in the Testflight.
  - check if the current version's any build is already live in appstore.

2. If the ITMSTRANSPORTER constantly fails to upload the ipa, put below line of code in .env file.
ITMSTRANSPORTER_FORCE_ITMS_PACKAGE_UPLOAD='true'

3. If ipa upload is failing even though above solutions, increase the build to abit higher eg. if build 3 is in TF use build 5. If even this doesnt solve the issue try changing the version as well. eg. 1.8.0 to 1.8.1.

## Archiving
1. If fastlane gym fails constantly with timeout error, put below line of code in .env file.
FASTLANE_XCODEBUILD_SETTINGS_TIMEOUT=60


## Setting in Xcode
1. If you are not able to change the provisioning profile from the Signing & Capabilities tab, go to Build Setting tab and search Signing and under signing header there must be a provisioning profile header, change the provisioning profile for the respective config.
