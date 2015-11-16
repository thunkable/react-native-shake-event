# ![react-native-shake-event-ios](media/promo.png)

[![npm package](https://img.shields.io/npm/v/react-native.svg?style=flat-square)](https://www.npmjs.org/package/gatsby)
[![react-native channel on discord](https://img.shields.io/badge/discord-react--native%40reactiflux-738bd7.svg?style=flat-square)](https://discord.gg/0ZcbPKXt5bXsb3os)

Add the shake event on your React Native app, giving users improved usability. Enjoy!

## Demo

*(Soon)*

*Run this example: [Example App](#).*


## Install

```
$ npm install react-native-shake-event-ios--save
```

#### Add to Xcode (required)

1. Add the `RNShakeEvent.xcodeproj` file to your Xcode project [Demo](https://facebook.github.io/react-native/img/AddToLibraries.png);
2. Add the `Products/libRNShakeEvent.a` file to **Build Settings**  [Demo](https://facebook.github.io/react-native/img/AddToBuildPhases.png).

This step is described here: [Linking Libraries](https://facebook.github.io/react-native/docs/linking-libraries-ios.html#content).

## Usage

```
import RNShakeEventIOS from 'react-native-shake-event-ios';

class MyComponent extends React.Component {
  componentWillMount() {
    RNShakeEventIOS.addEventListener('shake', () => {      
      console.log('Device shake!');
    });
  }

  componentWillUnmount() {
    RNShakeEventIOS.removeEventListener('shake');
  }
}
```

## API

### RNShakeEventIOS

#### addEventListener('shake', Function)
Start listening the shake event and handle a callback function.

#### removeEventListener('shake', Function)
Stop to listening the shake event, and is recommended to prevent memory leak.

## Issues
1. [Submit here](https://github.com/jadsonlourenco/react-native-shake-event-ios/issues);
2. iOS only - For Android version please create new module;
3. On *debug mode* this event also handle the **DevMenu**, but works fine on *production*.

## License

MIT © [Chessboard Radio Lab](https://chessboardradio.com)
