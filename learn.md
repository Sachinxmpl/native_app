import {Button , View , Stylesheet , Text , Alert}

<Text style = {styles.button}>

Stylesheet utility
const styles = Stylesheet.create({

    button : {}

})

Native wind ==> tailwind like

<view>==> similar to div , flexbox by default

Some interactive elements

//customizable buttons
Basic button
<Button title = "singup" onPress = {()=>{Alert.alert("This is native alert message ")}}

<TouchableOpacity> ==> creating buttons

<TouchableHighlight> ==> creawting buttons

<TouchableWithoutFeedback> ===> no feedback on touch , for links

//ActivityIndicator to show loading spinner
import {ActivityIndicator} from "react-native"

{

    isLoading? (<ActivityIndicator  size="large" color="#fff" />) : ( <View>  

                        <Text>  No loading state </Text>

    </View>)

}




### FlatList to render longlist with better performance than map 


FlastList for larget lists , especially when you want feature like laxy loading  , smooth scrolling and better optimization  . For smaller list map function works fine 

```
import {FlatLIst} from 'react-native'

const items = [
                        { id: '1', name: 'Item 1' },
                        { id: '2', name: 'Item 2' },
                        { id: '3', name: 'Item 3' },
                        
];

export derfault function App(){
        return (
                <Flastlist
                                data = {items}
                                renderItem = {({item}) = > {    
                                        <view>
                                                    <Text>{item.name}</Text>
                                        </view>
                                }}

                                keyExtractor = {(item)=> item.id}

                />
        )
}


```


### ScrollView to render large list , enable scoll feature 
Vertical and horizontal scrolling 
Shows a scrool indicator by default 
onScroll function 


```
import React from 'react';
import { View, ScrollView, Text, StyleSheet } from 'react-native';

export default function App() {
  return (
        <View style={styles.container}>
                        <View style={styles.header}><Text>Header</Text></View>
                                        <ScrollView style={styles.scrollView}>
                                                <Text>Scrollable Content</Text>
                                                {/* Add more scrollable content here */}
                                        </ScrollView>
                        <View style={styles.footer}><Text>Footer</Text></View>
        </View>
  );
}


```


### Image and ImageBackground  TextInput


```
import {ImageBackground , Image} from "react-native"

export default function App(){
        return (
                <View style = {styles.cotnainer}>
                                <ImageBackground 
                                                source = {{url : ""}}
                                >
                                                <Text>This is teh image backgrond </Text>
                                </ImageBackground>


                                <Image 
                                        source = {{url  : "" }}
                                        style = {styles.imageStyle }
                                        resizeMode = "cover"
                                />

                                <TextInput
                                        style = {{height : 40   , borderColor :  "black", borderWidth : 1}}
                                        defaultValue = "You fcan type in here "
                                />
                </View>



        )
}
```




### StatucBar alws to customize the topmost batter , time bar 

```
<View style={styles.container}>
                        {/* Customize StatusBar */}
                        <StatusBar barStyle="light-content" backgroundColor="#6a51ae" />
                        
                        <Text style={styles.text}>Hello, World!</Text>
    </View>
```