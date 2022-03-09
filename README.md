# Dolby.io Communications SDK for Android

## Documentation

The complete documentation for this product is available on Dolby.io, where you can find the product [overview](https://docs.dolby.io/communications-apis/docs/android-overview), [instructions](https://docs.dolby.io/communications-apis/docs/getting-started-with-android) how to create a basic audio conference application, and [reference documentation](https://docs.dolby.io/communications-apis/docs/android-reference). 

For additional information on Dolby.io Communications SDK for iOS releases, recent changes, and new features, see the Dolby.io Communications Client SDK [release notes](https://docs.dolby.io/communications-apis/changelog).

## Proguard integration

We recommend a wildcard configurations for our classes :

```
-keep class com.voxeet.** { *; }
-keep interface com.voxeet.** { *; }

-keep class org.webrtc.** { *; }
-keep interface org.webrtc.** { *; }

-keep class com.dolby.voice.** { *; }
-keep interface com.dolby.voice.** { *; }
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
