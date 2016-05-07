
# Bar Collapsible React Native

It's a React Native bar component with different interactions: Text Only,
Clickable, Collapsible.

## Install

Install the package via npm:

```javascript
    npm i react-native-bar-collapsible --save
```

The [React Native Vector Icons](https://github.com/oblador/react-native-vector-icons)
package is a dependency of this component and it's needed to link it, as you can
read in its installation instructions.

In order to link it to the project first install [rnpm](https://github.com/rnpm/rnpm)

```javascript
    npm install rnpm -g
```

Then run the following command to link the react-native-vector-icons package

```javascript
    rnpm link react-native-vector-icons
```

## Usage

Import the component:

```javascript
    import Collapsible from 'react-native-bar-collapsible';
```

**Text Only**:

This is the default action, you just need to pass a "title" property with the text to show

```jsx
    <Collapsible title='My title'/>
```

#### Clickable:

You need to pass the properties:

- ***title:*** string
- ***clickable:*** boolean. If false or null is passed the bar will be rendered as text only.
- ***icon:*** string, a FontAwesome icon name. If no icon property is passed the
    default is 'angle-right'.
- ***onPressed:*** function

```jsx
<Collapsible
    title='My title'
    clickable={true}
    icon='rocket'
    onPressed={() => this._myFunction()}/>
```

#### Collapsible:

You need to pass the properties:

- ***title:*** string
- ***collapsible:*** boolean. If false or null is passed the bar will be rendered as text only.
- ***iconCollapsed:*** string, a FontAwesome icon name. If no icon property is passed the
    default is 'plus'.
- ***iconOpened:*** string, a FontAwesome icon name. If no icon property is passed the
    default is 'minus'.
- ***children:*** The View or component you want to rendered in the toggled view.

```jsx
<Collapsible
    title='My title'
    collapsible={true}
    iconCollapsed='chevron-right'
    iconOpened='chevron-down'
    children={<OtherComponent/>}/>
```

### Another properties for customization

Additional to the basic properties, you can pass:

- ***backgroundColor***
- ***iconSize***
- ***tintColor***

```jsx
<Collapsible
    title='My title'
    clickable={true}
    icon='rocket'
    backgroundColor='#BF5327'
    tintColor='#F2F2F2'
    iconSize={15}/>
```

### Icons

The component use Font Awesome Icons from
[React Native Vector Icons](https://github.com/oblador/react-native-vector-icons)
package. All the icons available can be found [here](http://fortawesome.github.io/Font-Awesome/icons/).




## License

```
   Copyright (C) 2016 Carolina Aguilar

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing,
   software distributed under the License is distributed on an
   "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
   KIND, either express or implied.  See the License for the
   specific language governing permissions and limitations
   under the License.
```
