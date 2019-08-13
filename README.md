# React Native Elements Snippets README

Automatically adds React Native Elements snippets to your React Native Apps. 
+ Required Expo 32 and Above and React Native 0.59


## Features

Supported languages (file extensions)

JavaScript (.js)
JavaScript React (.jsx)
JavaScript React Native(.jsx)
TypeScript (.ts)
TypeScript React (.tsx)

## Snippets Info

Basic Methods

`!rneavatar` ===> <br>

```javascript
import { Avatar } from 'react-native-elements';

// Standard Avatar
<Avatar
  rounded
  source={{
    uri:
      'https://s3.amazonaws.com/uifaces/faces/twitter/ladylexy/128.jpg',
  }}
/>

// Avatar with Title
<Avatar rounded title="MD" />

// Avatar with Icon
<Avatar rounded icon={{ name: 'home' }} />

// Standard Avatar with edit button
<Avatar
  source={{
    uri:
      'https://s3.amazonaws.com/uifaces/faces/twitter/adhamdannaway/128.jpg',
  }}
  showEditButton
/>
```

`!rnebadge` ===> <br>

```javascript
import { Text, View } from 'react-native'
import { Avatar, Badge, Icon, withBadge } from 'react-native-elements'

<Badge value="99+" status="error" />
<Badge value={<Text>My Custom Badge</Text>}>

<Badge status="success" />
<Badge status="error" />
<Badge status="primary" />
<Badge status="warning" />

<View>
  <Avatar
    rounded
    source={{
      uri: 'https://randomuser.me/api/portraits/men/41.jpg',
    }}
    size="large"
  />

  <Badge
    status="success"
    containerStyle={{ position: 'absolute', top: -4, right: -4 }}
  />
</View>


const BadgedIcon = withBadge(1)(Icon)
<BadgedIcon type="ionicon" name="ios-chatbubbles" />

@connect(state => ({
  notifications: state.notifications,
}))
@withBadge(props => props.notifications.length)
export default class MyDecoratedIcon extends React.Component {
  render() {
    return (
      <Icon type="ionicon" name="md-cart" />
    );
  }
}
```

`!rnebutton` ===> <br>

```javascript
import { Button } from 'react-native-elements';
import Icon from 'react-native-vector-icons/FontAwesome';

<Button
  title="Solid Button"
/>

<Button
  title="Outline button"
  type="outline"
/>

<Button
  title="Clear button"
  type="clear"
/>

<Button
  icon={
    <Icon
      name="arrow-right"
      size={15}
      color="white"
    />
  }
  title="Button with icon component"
/>

<Button
  icon={{
    name: "arrow-right",
    size: 15,
    color: "white"
  }}
  title="Button with icon object"
/>

<Button
  icon={
    <Icon
      name="arrow-right"
      size={15}
      color="white"
    />
  }
  iconRight
  title="Button with right icon"
/>

<Button
  title="Loading button"
  loading
/>
```

`!rnecard` ===> <br>

```javascript
const users = [
 {
    name: 'brynn',
    avatar: 'https://s3.amazonaws.com/uifaces/faces/twitter/brynn/128.jpg'
 },
 ... // more users here
]

import { View, Text, Image } from 'react-native'
import { Card, ListItem, Button, Icon } from 'react-native-elements'

// implemented without image with header
<Card title="CARD WITH DIVIDER">
  {
    users.map((u, i) => {
      return (
        <View key={i} style={styles.user}>
          <Image
            style={styles.image}
            resizeMode="cover"
            source={{ uri: u.avatar }}
          />
          <Text style={styles.name}>{u.name}</Text>
        </View>
      );
    })
  }
</Card>
```

`!rnecheckbox` ===> <br>

```javascript
import { CheckBox } from 'react-native-elements'

<CheckBox
  title='Click Here'
  checked={this.state.checked}
/>
```

`!rneheader` ===> <br>

```javascript
<Header
  leftComponent={{ icon: 'menu', color: '#fff' }}
  centerComponent={{ text: 'MY TITLE', style: { color: '#fff' } }}
  rightComponent={{ icon: 'home', color: '#fff' }}
/>
```


`!rneinput` ===> <br>

```javascript
import Icon from 'react-native-vector-icons/FontAwesome';
import { Input } from 'react-native-elements';

<Input
  placeholder='BASIC INPUT'
/>
```

`!rnetooltip` ===> <br>

```javascript
import { Tooltip, Text } from 'react-native-elements';


<Tooltip popover={<Text>Info here</Text>}>
  <Text>Press me</Text>
</Tooltip>
```

`!rnetile` ===> <br>

```javascript
import { Tile } from 'react-native-elements';

<Tile
  imageSrc={require('./img/path')}
  title="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores dolore exercitationem"
  featured
  caption="Some Caption Text"
/>;
```

`!rnetext` ===> <br>

```html
<Text h1>Heading 1</Text>
<Text h2>Heading 2</Text>
<Text h3>Heading 3</Text>
<Text h4>Heading 4</Text>
```




## Extension Settings

Include if your extension adds any VS Code settings through the `contributes.configuration` extension point.

For example:

This extension contributes the following settings:

* `myExtension.enable`: enable/disable this extension
* `myExtension.thing`: set to `blah` to do something

## Known Issues

Calling out known issues can help limit users opening duplicate issues against your extension.

## Release Notes


### 1.0.0

Initial release of React Native Elements Snippets


-----------------------------------------------------------------------------------------------------------
**Enjoy!**
