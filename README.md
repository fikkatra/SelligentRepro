# Selligent Android build error

## Code Repro

This code repro is nothing more than:
* A blank React Native project, following instructions on [React Native - Environment Setup](https://reactnative.dev/docs/environment-setup)
* Adding environments dev, tst, prd via Android variants (product flavors). They each have a different app id.
* Adding Selligent React Native SDK, following instructions on [SelligentMarketingCloud - MobileSDK-ReactNative](https://github.com/SelligentMarketingCloud/MobileSDK-ReactNative)

## To reproduce the build error

* Add ./android/app/google-services.json file contents (omitted for security reasons)
* Add ./selligent.json file contents (omitted for security reasons)

Then start the Android build:

```bash
npm run android
```

This produces a build error:

> FAILURE: Build failed with an exception.
> 
> Where:
> Build file '/Users/sophietraen/Projects/POCS/kpnwe/node_modules/@selligent-marketing-cloud/selligent-react-native/android/build.gradle' line: 101
> 
> What went wrong:
> A problem occurred configuring project ':selligent-marketing-cloud_selligent-react-native'.
> org.gradle.api.InvalidUserDataException: The selligent.json file could not be found. Please make sure you provide this file in the root of this project.
