# React Native Styling Properties

This document covers the styling properties available in React Native and includes examples for some key properties.

## Table of Contents

1. [Layout Properties](#layout-properties)
2. [Shadow Properties](#shadow-properties)
3. [Border Properties](#border-properties)
4. [Typography Properties](#typography-properties)
5. [Image Styling Properties](#image-styling-properties)
6. [Flexbox Properties](#flexbox-properties)
7. [Example Usage](#example-usage)

## Layout Properties

- **alignContent**: Aligns a flex container's lines within when there's extra space on the cross-axis.
- **alignItems**: Aligns children along the cross-axis.
- **alignSelf**: Aligns a single child within its flex container.
- **aspectRatio**: Defines the proportion between width and height of an element.
- **borderBottomWidth**: Width of the bottom border.
- **borderEndWidth**: Logical width of the border at the end.
- **borderLeftWidth**: Width of the left border.
- **borderRightWidth**: Width of the right border.
- **borderStartWidth**: Logical width of the border at the start.
- **borderTopWidth**: Width of the top border.
- **borderWidth**: Width of all borders.
- **bottom**: The position relative to the bottom of the parent container.
- **display**: Controls the display type (`flex` or `none`).
- **end**: Logical position at the end (RTL or LTR).
- **flex**: Specifies how a component should grow or shrink.
- **flexBasis**: Defines the default size of an element before the remaining space is distributed.
- **flexDirection**: Defines the primary axis (`row`, `row-reverse`, `column`, `column-reverse`).
- **flexGrow**: Defines the growth factor of a flex item.
- **flexShrink**: Defines the shrink factor of a flex item.
- **flexWrap**: Defines whether to wrap items onto multiple lines (`nowrap`, `wrap`).
- **height**: Sets the height of the component.
- **justifyContent**: Aligns children along the main axis (`flex-start`, `flex-end`, `center`, `space-between`, etc.).
- **left**: The position relative to the left of the parent container.
- **margin**: Sets the margin space around the component.
- **marginBottom**: Sets the bottom margin.
- **marginEnd**: Sets the end margin.
- **marginHorizontal**: Sets the horizontal margin (left and right).
- **marginLeft**: Sets the left margin.
- **marginRight**: Sets the right margin.
- **marginStart**: Sets the start margin.
- **marginTop**: Sets the top margin.
- **marginVertical**: Sets the vertical margin (top and bottom).
- **maxHeight**: Sets the maximum height for the component.
- **maxWidth**: Sets the maximum width for the component.
- **minHeight**: Sets the minimum height for the component.
- **minWidth**: Sets the minimum width for the component.
- **overflow**: Determines the behavior when content overflows (`visible`, `hidden`, `scroll`).
- **padding**: Sets the padding inside the component.
- **paddingBottom**: Sets the bottom padding.
- **paddingEnd**: Sets the end padding.
- **paddingHorizontal**: Sets the horizontal padding (left and right).
- **paddingLeft**: Sets the left padding.
- **paddingRight**: Sets the right padding.
- **paddingStart**: Sets the start padding.
- **paddingTop**: Sets the top padding.
- **paddingVertical**: Sets the vertical padding (top and bottom).
- **position**: Defines the position type (`relative`, `absolute`).
- **right**: The position relative to the right of the parent container.
- **start**: Logical position at the start (RTL or LTR).
- **top**: The position relative to the top of the parent container.
- **width**: Sets the width of the component.
- **zIndex**: Controls the stacking order of components.

## Shadow Properties

- **shadowColor**: Color of the shadow.
- **shadowOffset**: The offset of the shadow (`{width: number, height: number}`).
- **shadowOpacity**: Opacity of the shadow (0 to 1).
- **shadowRadius**: How blurred the shadow is.

## Border Properties

- **borderBottomColor**: Color of the bottom border.
- **borderBottomEndRadius**: Rounds the bottom end corner.
- **borderBottomLeftRadius**: Rounds the bottom left corner.
- **borderBottomRightRadius**: Rounds the bottom right corner.
- **borderBottomStartRadius**: Rounds the bottom start corner.
- **borderColor**: Color of all borders.
- **borderEndColor**: Logical color of the border at the end.
- **borderLeftColor**: Color of the left border.
- **borderRadius**: Rounds all corners.
- **borderRightColor**: Color of the right border.
- **borderStartColor**: Logical color of the border at the start.
- **borderStyle**: Style of the border (`solid`, `dotted`, `dashed`).
- **borderTopColor**: Color of the top border.
- **borderTopEndRadius**: Rounds the top end corner.
- **borderTopLeftRadius**: Rounds the top left corner.
- **borderTopRightRadius**: Rounds the top right corner.
- **borderTopStartRadius**: Rounds the top start corner.

## Typography Properties

- **color**: Sets the color of the text.
- **fontFamily**: Defines the font family.
- **fontSize**: Sets the size of the font.
- **fontStyle**: Defines the font style (`normal`, `italic`).
- **fontWeight**: Sets the weight of the font (`normal`, `bold`, `100` - `900`).
- **letterSpacing**: Adjusts the spacing between letters.
- **lineHeight**: Sets the height between lines.
- **textAlign**: Aligns text horizontally (`left`, `right`, `center`, `justify`).
- **textAlignVertical**: Aligns text vertically (`auto`, `top`, `bottom`, `center`).
- **textDecorationColor**: Color of the underline/strike-through text decoration.
- **textDecorationLine**: Adds an underline or strike-through (`none`, `underline`, `line-through`).
- **textDecorationStyle**: Defines the style of text decoration (`solid`, `double`, `dotted`, `dashed`).
- **textShadowColor**: Color of the text shadow.
- **textShadowOffset**: The offset of the text shadow (`{width: number, height: number}`).
- **textShadowRadius**: Blur radius of the text shadow.

## Image Styling Properties

- **resizeMode**: Defines how the image should be resized to fit the container (`cover`, `contain`, `stretch`, `repeat`, `center`).
- **tintColor**: Applies a color overlay to the image.

## Example Usage

Below is an example that demonstrates the usage of these properties in a `StyleSheet`:

```javascript
import React from 'react';
import { StyleSheet, Text, View, Image } from 'react-native';

export default function App() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Hello, World!</Text>
      <Image source={{ uri: 'https://example.com/image.jpg' }} style={styles.image} />
      <Text style={styles.text}>This is an example text.</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    padding: 20,
  },
  title: {
    fontSize: 24,
    fontWeight: 'bold',
    textAlign: 'center',
    color: '#333',
    marginBottom: 20,
  },
  text: {
    fontSize: 16,
    color: '#666',
    textAlign: 'left',
    marginVertical: 10,
  },
  image: {
    width: 100,
    height: 100,
    borderRadius: 50,
    resizeMode: 'cover',
    shadowColor: '#000',
    shadowOffset: { width: 0, height: 2 },
    shadowOpacity: 0.8,
    shadowRadius: 3,
  },
});
