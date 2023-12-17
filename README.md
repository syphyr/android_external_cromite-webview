# android_external_cromite-webview
Prebuilt Android System Webview from https://github.com/uazo/cromite

Replaces the default Android System Webview with the 'Cromite' SystemWebView component in Custom ROM builds

## Credits
I have only taken the apk files (arm and arm64) from https://github.com/uazo/cromite/releases and created an 'Androik.mk' file around. 
All credits go to the Chromium project (https://www.chromium.org/Home) and the developers behind Cromite. Please visit the 
respective pages listed above for more information and the respective Copyright and License

## How to include into your Custom ROM build
- Include this repo into your local manifest (path does not matter, suggest external/cromite-webview)
- Specify `PRODUCT_PACKAGES += cromite-webview` in a 'product' .mk file (**not** in an Android.mk file)
- An 'elegant' way to do so without having to fork and track any specific device or vendor repository is to simply create an own product.mk file in directory vendor/extras (or to add the above statement into an existing one)
- It is not necessary to remove the default webview repo from the build tree
- Add the following directory structure to include Cromite WebView:

  prebuilt/arm64/SystemWebView.apk

  prebuilt/arm/SystemWebView.apk

