# React Native Reponsive UI

Building reponsive UIs in React Native.

![example](https://raw.githubusercontent.com/wcandillon/react-native-responsive-ui/4637085802323386110a6352929147d11e1ca83c/example/components/images/example.gif)

## What about existing packages?

* [react-native-responsive](https://github.com/adbayb/react-native-responsive): This library provides interesting APIs but it doesn't listen to changes in the app window.
This is problematic when changing the orientation of the device or when splitting screens.

* [react-native-responsive-styles](https://github.com/FormidableLabs/react-native-responsive-styles): This is a great library but it contains native depencies which prevents you to use it with expo for instance.
  
## What about the react-native-responsive package?

## Installation

```bash
npm install react-native-responsive-ui --save
```

## Usage

### Media Queries

```jsx
// @flow
import React, {Component} from "react";
import {MediaQuery, MediaQueryStyleSheet, ResponsiveComponent} from "react-native-responsive-ui";

export default class Login extends Component {
    render(): React$Element<*> {
        const style = this.getStyle();
        return <BackgroundImage source={Images.login}>
            <View style={mainStyle.container}>
                <MediaQuery minHeight={450}>
                    <Mark />
                </MediaQuery>
                <Field label="email" />
                <Field label="password" secureTextEntry last />
                <View >
                    <Button label="Login" />
                    <Button label="Sign Up" />
                </View>
            </View>
        </BackgroundImage>;
    }
}

```

#### Properties

| Name           | Type   | Description                                                                          |
|----------------|--------|--------------------------------------------------------------------------------------|
| minHeight      | dp     | Minimum height of the window.                                                        |
| maxHeight      | dp     | Maximum height of the window.                                                        |
| minWidth       | dp     | Minimum width of the window.                                                         |
| maxHeight      | dp     | Maximum height of the window.                                                        |
| minAspectRatio | number | Minimum aspect ration of the window (ratio of horizontal pixels to vertical pixels). |
| maxAspectRatio | number | Maximum aspect ration of the window (ratio of horizontal pixels to vertical pixels). |
| minPixelRatio  | number | Minimum device pixel density. See [PixelRatio](https://facebook.github.io/react-native/docs/pixelratio.html). |
| maxPixelRatio  | number | Maximum device pixel density. See [PixelRatio](https://facebook.github.io/react-native/docs/pixelratio.html). |
| orientation    | `portrait` or `landspace` | Indicates whether the viewport is in landscape (the display is wider than it is tall) or portrait (the display is square or taller than it is wide) mode. |
| platform       | string | Platform of the device.  See [Platform](https://facebook.github.io/react-native/docs/platform-specific-code.html#platform-module). |
| condition      | boolean | Abritrary boolean value that must be true for the media query to pass. |


### Responsive Component

### Responsive StyleSheet
