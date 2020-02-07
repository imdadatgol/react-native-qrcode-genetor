
# react-native-qrcode-genetor
A react-native component to generate [QRcode](http://en.wikipedia.org/wiki/QR_code), note only support English.


Based on react-native-qrcode, for react-native version > 0.59 react-native-qrcode was using webview from 'react-native'. I removed webview from 'react-native' and added webview from 'react-native-webview'.
## Installation
by using yarn

```sh
yarn add react-native-qrcode-genetor
```
by using npm
```sh
npm install react-native-generator --save
```
## Usage
```jsx

import React, { Component } from 'react'
import QRCode from 'react-native-qrcode';

import {
    AppRegistry,
    StyleSheet,
    View,
    TextInput
} from 'react-native';

class HelloWorld extends Component {
  state = {
    text: 'http://facebook.github.io/react-native/',
  };

  render() {
    return (
      <View style={styles.container}>
        <TextInput
          style={styles.input}
          onChangeText={(text) => this.setState({text: text})}
          value={this.state.text}
        />
        <QRCode
          value={this.state.text}
          size={200}
          bgColor='purple'
          fgColor='white'/>
      </View>
    );
  };
}

const styles = StyleSheet.create({
    container: {
        flex: 1,
        backgroundColor: 'white',
        alignItems: 'center',
        justifyContent: 'center'
    },

    input: {
        height: 40,
        borderColor: 'gray',
        borderWidth: 1,
        margin: 10,
        borderRadius: 5,
        padding: 5,
    }
});

AppRegistry.registerComponent('HelloWorld', () => HelloWorld);

module.exports = HelloWorld;
```
## Available Props

prop          | type                 | default value
----------    |----------------------|--------------
`value`       | `string`             | `http://facebook.github.io/react-native/`
`size`        | `number`             | `128`
`bgColor`     | `string` (CSS color) | `"#000"`
`fgColor`     | `string` (CSS color) | `"#FFF"`
`Canvas_size` | `number`             | `1000`
![picture](qrcode.png)

# Licenses

All source code is licensed under the [MIT License] 
