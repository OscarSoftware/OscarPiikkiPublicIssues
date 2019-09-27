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
# Release 19.2.0 notes
    - What's new:
      - Statistics screen added
        - User can see how many sent, unhandled and unsent receipts there are
        - User can browse costs by target 
      - Unhandled receipt statuscode change to "KASITTELEMATON"
      - Default account can be selected from settings
      - Receipts in UI are mostly updated through SQLite
        - Receipts are synced from cloud to SQLite once during startup
        - When user slides to refresh, receipts are synced again from cloud to SQLite
        - Receipt updates, additions and deletions don't cause full cloud refresh, only individual sync to SQLite
      - Perfomance updates
        - Opening filters has no more lag
        - Receipt search view initially shows only 10 receipts but more receipts can be loaded from the button below the list
        - Changing of screens happens much faster as screen updates are only done when necessary
      - Camerascreen improvements
        - Transparent screen when taking picture
        - Shutter click sound on android
      - PDF upload support
        - As of now previewing PDF inside app not possible. Shows only an icon
      - Receipt can have negative price
      - Correct user account details shown in settings screen
    - Known issues: 
      - If a screen is loading something, user should wait for loading to finish before proceeding to next page
        - Can cause out of sync data -> slide to refresh to update again. 
      - If user data fetch fails (accounts, targets, etc) there is no way to update the data but to reboot the app
      
        
        
