# react-native-countdown

React Native CountDown

## Installation

Run `npm install @orashidi/react-native-countdown-component`

## Preview

![React Native Countdown](https://media.giphy.com/media/xT0xeLWYNSaLerFGko/giphy.gif 'React Native Countdown')

## Code

```javascript
import CountDown from 'react-native-countdown-component'

render() {
    return (
      <CountDown
        until={10}
        onFinish={() => alert('finished')}
        onPress={() => alert('hello')}
        size={20}
      />
    )
}
```

## Props

| Name           | Description                                                  | Type                    |                    Default Value                    |
| :------------- | :----------------------------------------------------------- | :---------------------- | :-------------------------------------------------: |
| id             | Counter ID, to determine whether to reset the counter or not | string                  |                        null                         |
| style          | Override the component style                                 | `StyleProp<ViewStyle>`  |                         {}                          |
| digitStyle     | Digit style                                                  | `StyleProp<ViewStyle>`  |           {backgroundColor: `'#FAB913'`}            |
| digitTxtStyle  | Digit Text style                                             | `StyleProp<TextStyle>`  |                  {color: `'#000'`}                  |
| timeLabelStyle | Time Label style                                             | `StyleProp<TextStyle>`  |                  {color: `'#000'`}                  |
| separatorStyle | Separator style                                              | `StyleProp<TextStyle>`  |                  {color: `'#000'`}                  |
| size           | Size of the countdown component                              | number                  |                         15                          |
| until          | Number of seconds to countdown                               | number                  |                          0                          |
| onFinish       | What function should be invoked when the time is 0           | () => void              |                        null                         |
| onChange       | What function should be invoked when the timer is changing   | (until: number) => void |                        null                         |
| onPress        | What function should be invoked when clicking on the timer   | () => void              |                        null                         |
| timeToShow     | What Digits to show                                          | DigitType[]             |                ['D', 'H', 'M', 'S']                 |
| timeLabels     | Text to show in time label                                   | object                  | {d: 'Days', h: 'Hours', m: 'Minutes', s: 'Seconds'} |
| showSeparator  | Should show separator                                        | boolean                 |                        false                        |
| running        | A boolean to pause and resume the component                  | boolean                 |                        true                         |

## Custom Styling Example

![React Native Countdown](https://media.giphy.com/media/wIwc1dinsZhx6v2PxB/giphy.gif 'React Native Countdown')

## Code

```javascript
import CountDown from '@yakalexey/react-native-countdown-component'

render() {
    return (
      <CountDown
        until={60 * 10 + 30}
        size={30}
        onFinish={() => alert('Finished')}
        digitStyle={{backgroundColor: '#FFF'}}
        digitTxtStyle={{color: '#1CC625'}}
        timeToShow={['M', 'S']}
        timeLabels={{m: 'MM', s: 'SS'}}
      />
    )
}
```

## Separator Example

![React Native Countdown](https://media.giphy.com/media/4H7qQF4UPwQKEc0Qpx/giphy.gif 'React Native Countdown')

## Code

```javascript
import CountDown from '@yakalexey/react-native-countdown-component'

render() {
    return (
      <CountDown
        size={30}
        until={1000}
        onFinish={() => alert('Finished')}
        digitStyle={{backgroundColor: '#FFF', borderWidth: 2, borderColor: '#1CC625'}}
        digitTxtStyle={{color: '#1CC625'}}
        timeLabelStyle={{color: 'red', fontWeight: 'bold'}}
        separatorStyle={{color: '#1CC625'}}
        timeToShow={['H', 'M', 'S']}
        timeLabels={{m: null, s: null}}
        showSeparator
      />
    )
}
```
