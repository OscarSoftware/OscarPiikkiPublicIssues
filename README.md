# OscarPiikkiPublicIssues
Public repository for Oscar Piikki issues. Meant to be used by people who test and use Piikki mobile app. Testers can report bugfixes and imporovement suggestions through the issues page of this repository.

# 20.1.0 Release notes
 - Push notifications functionality added
   - Disabled until real usage is added
 - Update splash screen for newer iPhone devices
 - Image upload quality tweaking
   - New attempt on "sweet spot" between quality and file size 
 - Bugfixes
   - Reduce image upload sizes for iPhone
   - Removing and updating photos now works correctly
   - Fix component states not resetting on sign out
   - Camera sound unloads on end, saving memory
   - Fix image resolution scaling
   - Fix crop inaccuracy on iOS
   - Fix scroll bar sometimes appearing in the middle in receipt editing screen
   - Fix image cache management
   - Safe areas added to components needing them
   - Fixed navigation issues
   - Updated dependencies

# 20.0.2 Release notes
 - Bugfixes
   - Updated dependencies to fix camera / gallery bug on Android SDK 21 and 22
   - Fix icon clipping in camera screen
   - Disable changing backend in camera and photo review screens

# 20.0.1 Release notes
 - What's new:
      - Multiple backends
        - Own settings for each backend
        - Save images seperately for each backend
        - New settings: Ask which company (backend) to use when signing in
      - On POST, send images only if they have been changed
      - Fix statistics with foreign currencies
        
# 20.0.0 Release notes
 - What's new:
      - Select default value on mandatory fields if only 1 value is present
      - Images now have a much higher quality
      - Users can now select default payment 
      - Unify number formatting
 - Bug fixes:
      - Fix alerts toasts appearing on top of each other
      - Fix data appearing on wrong month in statistics
      - Fix partially loaded images
      - Users now correctly stay logged in if chosen so
      - Possible fix for decimal point not appearing on Samsung keyboards

# 19.2.4 Release notes
 - What's new:
      - PDF viewer
        - PDFs are no longer converted to images in backend, and they can be viewed inside the app
      - Image manipulation
        - Perspective cropping
        - Black and white image

# 19.2.1 Release notes
 - What's new:
      - PDF Preview
        - User can preview PDFs as they are converted to images in cloud and fetched by the app.
      - Default screen on startup
        - User can select a default startup screen from settings. When the app starts it opens to this screen. 
      - General data updating logic improved
        - CRUD-operations more reliable as there are global providers and functions for state access/manipulation.
        - Data is always up to date as changes are reflected globally. 
      - Styling changes
        - Settings screen redesigned.
        - More loadingcomponents/toasts added and loading icon changed.
        - Toast component redesigned. Automatical stacking and onPress dismiss. Also removed buggy layoutanimation.
      - Permormance improvements
        - Receipt images were previously fetched individually for each receipt. Loading/updating of receipts is now much  
          quicker as images are bulk fetched.
        - User has quicker access to new data when switching between screens as the data is now updated in background
          when changes happen. 
      - iOS Logout works 
        - User couldn't logout without clearing cache. 
 - Known issues: 
     - PDFs can only be viewed individually
        - User cannot view PDFs and images simultaneously inside preview carousel. When user clicks on a PDF-icon, only 
          the PDF pages are shown. Normal images have to be viewed separately. 
     

# 19.2.0 Release notes
 - What's new:
      - Statistics screen added
        - User can see how many sent, unhandled and unsent receipts there are
        - User can browse costs by target 
      - Unhandled receipt status code change to "KASITTELEMATON"
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
     - If user data fetch fails (accounts, targets, payment methods and currencies) there is no way to update the data but to  reboot the app
     - As uploading receipt data and images don't happen on a single transaction, it is theoretically possible to manage
       to upload a receipt without images. 
     
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
      
        
        
