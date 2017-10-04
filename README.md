# react-native-markdown-package
Package for implementing markdown syntax in React Native. Contribution, Pull Request, or anything else from you guys will be really appreciated. :)

## Getting started

1. add this line to your package.json `dependencies`

    `"react-native-markdown-package": "git+https://github.com/andangrd/react-native-markdown-package.git"`
    
2. run `npm install`

## Usage

What you need is to `import` the `react-native-markdown-package` module and then use the
`<Markdown/>` tag.

here is simple implementation :

```javascript
/**
 * Sample React Native App
 * https://github.com/facebook/react-native
 * @flow
 */

import React, { Component } from 'react';
import Markdown from 'react-native-markdown-package';
import {
  AppRegistry,
  StyleSheet,
  Text,
  View
} from 'react-native';

export default class AwesomeProject extends Component {
  render() {
    return (
      <View style={styles.container}>
        <Text style={styles.welcome}>
          Welcome to React Native!
        </Text>
        <Markdown styles={styles.markdown} >
          # This is Heading 1{'\n\n'}
          ## This is Heading 2{'\n\n'}
          1. List1 {'\n'}
          2. List2 {'\n'} 
          {'\t'}1. sublist1{'\n'}
          {'\t'}description sublist1.{'\n'}
          {'\t'}2. sublist2{'\t\t'}{'\n'}
          * List3{'\n'}
          * List4{'\n'}
          {'\t'}1. **bold text** {'\n'}
          {'\t'}2. this line contain * and should not be a new sublist{'\t\t'}{'\n'}
          5.  Last list{'\n\n'}
          Some *really* basic **Markdown**.{'\n\n'}


          ## this is header {'\n\n\n\n'}
          {'this is _italic_ '}
          {'this is **strong**'}

          {'\n\n'}
          | # | Name   | Age |{'\n'}
          |---|--------|-----|{'\n'}
          | 1 | John   | 19  |{'\n'}
          | 2 | Sally  | 18  |{'\n'}
          | 3 | Stream | 20  |{'\n'}
        </Markdown>
      </View>
    );
  }
}

const styles = {
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
  },
  welcome: {
    fontSize: 20,
    textAlign: 'center',
    margin: 10,
  },
  instructions: {
    textAlign: 'center',
    color: '#333333',
    marginBottom: 5,
  },
  markdown: {
    heading1: {
      color: 'red'
    },
    heading2: {
      color: 'green'
    },
    strong: {
      color: 'blue'
    },
    em: {
      color: 'cyan'
    },
    text: {
      color: 'magenta',
    }
  }
};

AppRegistry.registerComponent('AwesomeProject', () => AwesomeProject);

```

<img src="https://github.com/andangrd/rn-markdown-example/blob/master/assets/images/example.png" width="250">

## Properties

#### `styles`

Default style properties will be applied to the markdown. You will likely want to customize these styles, the following properties can be used to modify the rendered elements:

*Note: The text inside the parentheses denotes the element type.*

- `autolink` (`<Text>`) - WIP
- `blockQuote` (`<Text>`) - WIP
- `br` (`<Text>`)
- `codeBlock` (`<View>`) - WIP
- `del` (`<Text>`)
- `em` (`<Text>`)
- `heading` (`<Text>`) - Also `heading1` through `heading6`
- `hr` (`<View>`)
- `image` (`<Image>`) - Implemented but size is fixed to `50x50` until auto width is supported by React Native.
- `inlineCode` (`<Text>`)
- `link` (`<Text>`) - WIP
- `list` (`<View>`) - Also `sublist` (`<View>`), `listItem` (`<View>`), `listItemBullet` (`<Text>`) and `listItemNumber` (`<Text>`)
- `sublist` (`<View`) - Also `listItem` (`<View>`), `listItemBullet` (`<Text>`) and `listItemNumber` (`<Text>`)
- `mailto` (`<Text>`) - WIP
- `newline` (`<Text>`) - WIP
- `paragraph` (`<View>`)
- `plainText` (`<Text>`) - Use for styling text without any associated styles
- `strong` (`<Text>`)
- `table` (`<View>`)
- `tableHeader` (`<View>`)
- `tableHeaderCell` (`<Text>`)
- `tableRow` (`<View>`)
- `tableRowCell` (`<View>`)
- `tableRowLast` (`<View>`, inherits from `tableRow`)
- `text` (`<Text>`) - Inherited by all text based elements
- `u` (`<View>`)
- `url` (`<Text>`)
- `view` (`<View>`) - This is the container `View` that the Markdown is rendered in.

## Thanks To

Special thanks to: 

[lwansbrough](https://github.com/lwansbrough) , [gijoehosaphat](https://github.com/gijoehosaphat) , [Khan](https://github.com/Khan) 
