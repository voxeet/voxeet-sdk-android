# Change Log

All notable changes to this project will be documented in this file.

## v3.x

Use of the dependencies for the SDK 3.0 and above are subject to the [Dolby Voice License agreement](LICENSE)

New repository and dependency to be used by the modules :

```
maven { url "https://android-sdk.voxeet.com/release" }
```

```
dependencies {
   ...
   implementation "com.voxeet.sdk:sdk:${version}"
}
```

### 3.1.4

Released on 2021-04-30.

- update embedded devices database to improve Crosscall compatibility

### 3.1.2

Released on 2021-04-14.

Fix stability issues related to the 3.1.0 and 3.1.1 versions :

- local screenshare can now be attached to be rendered on the presenter side
- calling multiple open(ParticipantInfo) could overwrite already negotiated information
- improved various internal calls

Deprecation :

- to push forward security inside our customer's applications, we have deprecated the initialize(appId, appSecret), this method won't be removed but it will be clear from the IDE itself that developers should move toward the initialize(accessToken, refreshCallback) implementation.

### 3.1.1

Released on 2021-03-11.

Fix stability issues related to the 3.1.0 version :

- join method is now properly resolving when being called
- screenshare calls could hang when used on Android 10
- OAuth callbacks now properly fires at various intervals before expiration of any previously obtained token

### 3.1.0

Released on 2021-03-01.

Introducing the Conference Access Token (CAT), Conference Capacity Limit (CCL) and Video Forwarding Strategy (VFS). Those set of 3 APIs alongside various improvements in the SDK will help achieve great feature quality as well as providing a better security and stability while being in conferences.



### v3.0.3

Released on 2020-12-9.

Fixed an issue where devices like the Google Pixel and others were showing distorted videos from local participants.
Fixed an issue where VideoPresentation controls where mixed up with the controls from the FilePresentation.

The VoxeetSDK instance is now already available to be used. The various services are enabled and a new `isInitialized()` method is available in the VoxeetSDK class. This method will return true if the `VoxeetSDK.initialize(...)` has been used. This change will provide a better support for anything related to the system while keeping ap consistency when using `@NonNull` and `@Nullable` checker accross the apps using the SDK.

It can be used as follow :

```
if(VoxeetSDK.instance().isInitialized()) {
  ...
}
```

### v3.0.2

Released on 2020-11-30.

- Fixed an issue preventing getting the audioLevel from participants either local or remote
- Improved internal reconnection to the proper websocket's endpoint

### v3.0.1
Released on 2020-11-16.

- Changed the logging level to decrease the number of received logs, reducing the affects on system performance.
- Fixed an issue which prevented getting the audio from non dvc conferences
- Fixed a crash which could happen during conferences

### v3.0.0

Released on 2020-10-29.

Focus on audio quality and new Dolby related integration :

- mute and participants audio related API deprecation
- audio improvement (using the dolbyVoice flag at conference creation)
- auto video adaptation
- internal service improvements

## v3.x Beta

Use of the dependencies for the SDK 3.0 and above are subject to the [Dolby Voice License agreement](LICENSE)

New repository and dependency to be used by the modules :

```
maven { url "https://android-sdk.voxeet.com/beta" }
```

```
dependencies {
   ...
   implementation "com.voxeet.sdk:sdk:${version}"
}
```


### v3.1.0-BETA2102041753

Released on 2021-02-02.

**Features**

- Introduced the Video Forwarding feature to allow participants to dynamically control the number of transmitted video streams. The [Video Forwarding](https://beta.dolby.io/developers/interactivity-apis/guides/video-forwarding) article describes in detail the changes to Interactivity APIs.
- Introduced updates to the client SDK to support the use of conference access tokens for limiting the scope of participant permissions. The [Enhanced Conference Access Control](https://beta.dolby.io/developers/interactivity-apis/guides/enhanced-conference-access-control) article describes in detail the changes to Interactivity APIs.
- Introduced the conference capacity limit, limiting the number of conference participants based on type, in order to preserve audio and video quality. The [Conference Capacity Limitations](https://beta.dolby.io/developers/interactivity-apis/guides/conference-capacity-limitations) article describes the capacity limits and [ConferenceAtMaxCapacityError](https://beta.dolby.io/developers/interactivity-apis/reference/client-sdk/reference-android/model/conferenceatmaxcapacityerror).

**Changes**

Modified the supported Android versions. The Dolby Interactivity APIs Android SDK is now compatible with Android 5.0 and later versions.

### v3.0.3-BETA2012071606

Released on 2020-12-07.

Fixed an issue where devices like the Google Pixel and others were showing distorted videos from local participants.
Fixed an issue where VideoPresentation controls where mixed up with the controls from the FilePresentation.

The VoxeetSDK instance is now already available to be used. The various services are enabled and a new `isInitialized()` method is available in the VoxeetSDK class. This method will return true if the `VoxeetSDK.initialize(...)` has been used. This change will provide a better support for anything related to the system while keeping ap consistency when using `@NonNull` and `@Nullable` checker accross the apps using the SDK.

It can be used as follow :

```
if(VoxeetSDK.instance().isInitialized()) {
  ...
}
```


### v3.0.0-BETA2010191520

Released on 2020-10-19.

Focus on audio quality and new Dolby related integration :

- mute and participants audio related API deprecation
- audio improvement (using the dolbyVoice flag at conference creation)
- auto video adaptation
- internal service improvements

## v2.x Releases

### [v2.4.2](https://bintray.com/voxeet/maven/com.voxeet.sdk/2.4.2)

Released on 2020-10-05.

Fix various issues with the SDK :

- authentication locked due to network issue preventing reconnection on new sessions
- fix telemetry upload causing crash on previous 2.4.x versions
- provided VideoView's rendering `scaleType` has been changed to `streamScaleType` to prevent conflict with third party libraries

## Proguard integration

We recommend a wildcard configurations for our classes :

```
-keep class com.voxeet.** { *; }
-keep interface com.voxeet.** { *; }

-keep class org.webrtc.** { *; }
-keep interface org.webrtc.** { *; }

-keep class com.dolbyvoice.** { *; }
-keep interface com.dolbyvoice.** { *; }
```

## License

**BEFORE DOWNLOADING THE SOFTWARE, PLEASE CAREFULLY READ THE FOLLOWING AGREEMENT. DO NOT DOWNLOAD, INSTALL, ACTIVATE OR USE THIS SOFTWARE IF YOU HAVE NOT
ENTERED INTO A COMMERCIAL AGREEMENT WITH DOLBY. BY DOWNLOADING, INSTALLING, ACTIVATING OR USING THE SOFTWARE, YOU ARE AGREEING TO BE BOUND BY THE TERMS
OF THIS AGREEMENT. IF PRIOR TO DOWNLOADING, INSTALLING, ACTIVATING OR USING THE SOFTWARE, YOU DECIDE YOU ARE UNWILLING TO AGREE TO THE TERMS OF THIS
AGREEMENT, YOU HAVE NO RIGHT TO USE THE SDK.**

```
This Dolby Software License Agreement (“Agreement”) is a legal agreement between you individually if you are agreeing to it in your own capacity, or if you are
authorized to acquire the Software on behalf of your company or organization, between the entity for whose benefit you act (“Licensee”) and **Dolby Laboratories
Licensing Corporation** , a New York corporation, **Dolby International AB** , a Swedish company residing in The Netherlands (collectively, “**Licensor**”). This
Agreement is governed by the terms in the commercial agreement separately entered into by Licensee and Licensor (the “Commercial Agreement”), the terms of
which are incorporated herein by reference. Defined terms in this Agreement and not otherwise defined herein, have the meanings given to them in the Commercial
Agreement.
```
