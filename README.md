# react-native-qrcode-scanner

A QR code scanner component for React Native built on top of [react-native-camera by Lochlan Wansbrough](https://github.com/lwansbrough/react-native-camera)


Please note, this will also function as a generic barcode scanner by the virtue of the above module supporting barcode scanning, however, this module was initially built as a QR code scanner.


## Getting started

To install and begin using react-native-qrcode-scanner:

```
npm install react-native-qrcode-scanner
```
```
react-native link react-native-qrcode-scanner
```

## Usage
To use react-native-qrcode-scanner, `import` the `react-native-qrcode-scanner` module and use the <QRCodeScanner /> tag.


## Props

#### `onRead` (required)
propType: `func.isRequired`
default: `() => (console.log('QR code scanned!'))`

Will call this specified method when a QR code or a barcode is detected in the camera's view

#### `fadeIn`
propType: `bool`
default: `true`

When set to `true` this ensures that the camera view fades in after the initial load up instead of being rendered immediately.
Set this to false to prevent the animated fade in of the camera view.

#### `reactivate`
propType: `bool`
default: `false`

When set to `false`,  when a QR code is scanned, the `QRCodeScanner` will not scan another code until it is re-rendered.
When set to `true` this will reactivate the scanning ability of the component.

#### `reactivateTimeout`
propType: `number`
default: `0`

Use this to configure how long it should take before the `QRCodeScanner` should reactivate.

#### `topInfo`
propType: `oneOfType([
  PropTypes.element,
  PropTypes.string,
])`

Use this to render any additional content at the top of the camera view.

#### `bottomInfo`
propType: `oneOfType([
  PropTypes.element,
  PropTypes.string,
])`

Use this to render any additional content at the bottom of the camera view.

<!-- #### `showMarker` -->

<!-- #### `customMarker` -->

## License
See [License](LICENSE.md)

### Thanks
Thanks to [Lochlan Wansbrough](https://github.com/lwansbrough) for the [react-native-camera module](https://github.com/lwansbrough/react-native-camera) which provided me with an awesome example of how to set up this module.

This QR code scanner was inspired by the QR code scanner within [Whatsapp](https://www.whatsapp.com/).

### To do
- Add usage example to get started using it in the project
- Document other complex examples
- Document props
- Document default props