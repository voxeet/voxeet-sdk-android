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
