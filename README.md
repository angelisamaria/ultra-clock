# Purpose
The purpose of this app is to calculate statistics during a sunrise-to-sunset ultramarathon. Usually when
running the runner has plenty of time to do (bad) math in their head on how much further they have to
go, how fast they have to run to make it, how much slack they have, etc. This app does all that math
automatically.

This app was inspired by "Bryan's Soul Searching Solstice Run" on December 21, 2020 featured on the "How Was Your Run 
Today" Podcast (https://howwasyourruntoday.com/episodes/hwyrt-holiday-bonus-bryans-soul-searching-s1!b121d). My plan is 
to do this run on January 1, 2021 so I will be unlikely to maintain this app after that day. 

"We had to do lots of math to figure out how much longer we needed to go as it got later on in the afternoon because
there's no celestial indication that we're getting later in the day"
Podcast above at 23:45

# History
* v0.5.0 (01/18/2021) -- Add setting and saving of course information
* v0.4.5 (01/12/2021) -- Fix walk/rest calculations; added tons of unit tests
* v0.4.4 (12/29/2020) -- Hardcode to 12/30
* v0.4.3 (12/28/2020) -- Hardcode to 12/29
* v0.4.2 (12/28/2020) -- Fix skip-ahead bugs. Fix input spinner focus bugs. 
* v0.4.1 (12/27/2020) -- Fix NaN edge cases when "Now" is outside the race window
* v0.4.0 (12/27/2020) -- Add pace visualization. Many other minor things
* v0.3.0 (12/27/2020) -- Add progress circles to Distance and Time tabs
* v0.2.0 (12/26/2020) -- Make text bigger. Add tabs. Based upon feedback from run
* v0.1.0 (12/24/2020) -- MVP. Calculates basic statistics. Hard-coded dates for sunrise/sunset on 1/1/2021. 


# Developer information
This was developed on Windows 10 for a Samsung Galaxy S7 Edge using 
* IntelliJ 2017.2.1
* Android Studio 4.1.1  (Note this horrible bug: https://stackoverflow.com/a/64741229/5360912)

I use IntelliJ for all JS dev and open it from the project root. I use AS for Java development and open from the `android` folder

## iOS
This has not been tested on iOS, but it *should * run out of the box. The only issue I know of is the "VersionModule" 
which calls `git describe` on the command line. 

## To run unit tests
From the root:
```
npx jest
```
Note: I Have not yet successfully integrated with the old version of IntelliJ. I was successful back in 2017-2018 but it
appears incompatible now. 

## To run the app
### In one PowerShell window
```
npx react-native start --reset-cache
```

### In the other window

#### Debug
In debug (best for faster dev). Takes a few minutes the first time, then update immediately

```
npx react-native run-android
```

#### Release
To send a release (for faster execution). Takes ~5 minutes

```
npx react-native run-android --variant=release
```

### PLay store release
* Open Android Studio->Tools->Build->Generate Signed Bundle / APK->Press Next a lot

