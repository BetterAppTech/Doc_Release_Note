# BetterApp Ad SDK Release Notes

## 2.9.3.2
- Added Calendar integration support for the Ad SDK
- Exposed `sInitReady` and `sAdConfigFetcher` in `MediaAdLoader`
- Provided global ad event listener: `MediaAdLoader.setAllAdListener` for unified handling of request, load, display, and click events

## 2.9.3.0
- Optimized ad initialization process with logging for individual ad network initialization results
- Improved DT Banner auto-refresh logic

## 2.9.2.1
- Added support for AdMob MREC carousel (auto-rotating) display

## 2.9.1.1
- Enabled ad value reporting for DT ad network

## 2.9.1.0
- Added support for dynamically removing dependencies on MAX SDK and DT SDK
- Enabled shared usage of Ad SDK across multiple apps or modules

## 2.8.4.3
- Handled potential crashes caused by multiple Ad SDK initializations

## 2.8.3.1
- Fixed banner display issues caused by background refresh
- Optimized banner event tracking and reporting logic

## 2.8.1
- Upgraded DT SDK to address policy compliance issues
