# Expo Linking.getInitialURL() Inconsistent Null Return

This repository demonstrates a bug where Expo's `Linking.getInitialURL()` method inconsistently returns `null`, even when a deep link was used to launch the application.  This can lead to deep link handling failures in your application.

## Problem

The `Linking.getInitialURL()` method is crucial for handling deep links when your application is launched. However, in some cases, it unpredictably returns `null`, preventing your application from properly processing the intended deep link.

## Reproduction

The `handleDeepLinkBug.js` file provides a minimal reproducible example demonstrating this issue.  The inconsistency makes consistent reproduction challenging; however, multiple instances have been observed on various devices and Android versions.

## Solution

The `handleDeepLinkSolution.js` file showcases a potential solution by implementing a retry mechanism using `setTimeout`.  While this doesn't address the root cause, it provides a workaround to improve reliability.

## Further investigation:

This issue warrants further investigation into the Expo `Linking` API implementation to identify and fix the root cause of the inconsistent `null` return. Contributions and insights are welcome.