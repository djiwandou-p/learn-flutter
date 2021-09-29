because evermos-flutter already using Jenkins - GitHub integration there is a specification, referring to the Jenkinsfile rules.<br>
referring to build [Flutter CI/CD](https://github.com/evermos/evermos-flutter/wiki/Flutter-CI-CD) wiki's, there is three-stage of the build process which depends on the what kind of trigger goes off. <br>
* Pull Request will trigger created new branch with name PR-* and that also triggers Jenkins to build debug apk
* After PR-* merged it will trigger branch master to change, so the Jenkins will trigger to build both debug apk & preview apk.
* Meanwhile, Tag creation with prefixes (start with v, example `v.1.0.0`) will trigger to build both preview apk & production aab.
### APK/AAB name format
* [Triggered by PR] APK/AAB name format will be  app-staging_`PR-ID`.apk
* [Triggered by merge to master] APK/AAB name format will be app-staging_`v.0.1.0`.apk & app-preview_`v.0.1.0`.apk
* [Triggered by Tag Creation] APK/AAB name format will be app-preview_`v.0.1.0`.apk & app-production_`v.0.1.0`.aab