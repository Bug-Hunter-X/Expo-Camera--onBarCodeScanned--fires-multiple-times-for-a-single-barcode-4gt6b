# Expo Camera Barcode Scan Duplication Bug

This repository demonstrates a bug in Expo's Camera API where the `onBarCodeScanned` function fires multiple times for a single barcode scan. This issue is particularly noticeable when scanning fast-moving barcodes.

## Problem

The `onBarCodeScanned` callback within Expo's Camera API is unexpectedly triggered multiple times for a single barcode, leading to duplicated data in the application.

## Solution

The solution involves debouncing the `onBarCodeScanned` callback. By adding a delay, we prevent the callback from being executed multiple times within a short period.

## Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Point the camera at a barcode.  Observe the multiple barcode readings.