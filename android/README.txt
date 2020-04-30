1. Export Android Project, from unity
- open unity
- switch to Android platform
- export project check box
- Export to api\client\unity\androidBuild

2. Add Unity Module by modifying settings.gradle of android
- open Android Studio for android
- add to settings.gradle at the end of file, change path to {Exported project}\unityLibrary from step #1
include ':unityLibrary'
project(':unityLibrary').projectDir=new File('C:\\Projects\\UaaLExample\\unity\\Export\\unityLibrary')

3. Add dependency on :unityLibrary for :app
- add next to dependencies block in build.gradle for :app module
  implementation project(':unityLibrary')

Project prepared