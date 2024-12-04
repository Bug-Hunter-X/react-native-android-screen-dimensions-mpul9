# React Native: Inconsistent Screen Dimensions on Android

This repository demonstrates a common bug in React Native applications related to inconsistent screen dimensions obtained using the `Dimensions` API, particularly on Android devices. The issue stems from the asynchronous nature of dimension updates and can cause layout problems if not handled properly.

## Problem
The `Dimensions.get('window')` or `Dimensions.get('screen')` methods might not provide accurate dimensions immediately after the app starts or when the screen orientation changes.  This leads to misaligned elements and incorrect layouts.  The example provided shows a layout that breaks when the initial dimensions are inaccurate. 

## Solution
The solution involves using the `Dimensions` API in conjunction with the `useEffect` hook. This ensures that the layout updates after the dimensions have been reliably obtained.

## How to reproduce
1. Clone the repository.
2. Run `npm install` or `yarn install`.
3. Run the app on an Android emulator or device.
4. Observe the layout. Note how the dimensions might be slightly off initially, and then correctly set afterwards.

## License
MIT