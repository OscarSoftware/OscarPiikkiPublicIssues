# OscarPiikkiPublicIssues
Public repository for Oscar Piikki issues. Meant to be used by people who test and use Piikki mobile app. Testers can report bugfixes and imporovement suggestions through the issues page of this repository.

# Beta 4 release notes
  - Whats new:
    - OpenID Connect implementation to Piikki
      - User is now redirected to a separate login page provided by Oscar to sign in
      - Much better error handling for users signup errors
    - Payment methods are no longer hardcoded. They are now received from Cloud and ready to be used in Piikki
    - Target selection has been reworked and should work much more smoothly now
    - Receipts can now have negative values (https://github.com/OscarSoftware/OscarPiikkiPublicIssues/issues/19)
    - Navigation within the app has been fixed
    - Added new field "Lisäkuvaus" for receipt (https://github.com/OscarSoftware/OscarPiikkiPublicIssues/issues/16)
    - User related settings fixed
    - User can now perform "undo" when editing an image
      - This means whenever user crops an image multiple times and user chooses to undo the crop, it will undo the previous crop and not all the crops at once
    - UX improvements
  - Known issues:
    - In the photo review screen the "advanced" cropping, contrast and brightness features are not implemented
    - Statistics screen is not implemented
    - Offline mode not working properly
    - All open issues: https://github.com/OscarSoftware/OscarPiikkiPublicIssues/issues

# Alpha 3 release notes
  - Whats new:
    - User can now use a lot of filters when searching for receipts.
    - A lot of improvements to make Piikki work with Oscar Pro
    - More settings for user
      - Default values
      - Receipt synchronization period
      - Save images from Piikki to image gallery
    - Improvements to error handling
    - App version is now visible to the user in login screen and in the settings screen
    - More small stuff :D
    - More bugs
  - Known issues:
    - Payment methods are still hardcoded, and may not be working correctly
    - In the photo review screen the "advanced" cropping, contrast and brightness features are not implemented
    - The chart will not work if u close and reopen the app. Only works after login.. sigh
    - Settings screens design is poor and will be reworked later
    - User info in the settings screen is not implemented
    - Statistics screen is not implemented
    - (PRO) Image can be opened only once.. :D
