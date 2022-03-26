# 100 Days of Code Flutter Notes

## 1

Text

The Text widget lets you create a run of styled text within your application.

## 2
 
Row, Column

These flex widgets let you create flexible layouts in both the horizontal (Row) and vertical (Column) directions. The design of these objects is based on the web’s flexbox layout model.

## 3

Stack

Instead of being linearly oriented (either horizontally or vertically), a Stack widget lets you place widgets on top of each other in paint order. You can then use the Positioned widget on children of a Stack to position them relative to the top, right, bottom, or left edge of the stack. Stacks are based on the web’s absolute positioning layout model.

## 4

Container

The Container widget lets you create a rectangular visual element. A container can be decorated with a BoxDecoration, such as a background, a border, or a shadow. A Container can also have margins, padding, and constraints applied to its size. In addition, a Container can be transformed in three dimensional space using a matrix.

## 5

Flutter provides a number of widgets that help you build apps that follow Material Design. A Material app starts with the MaterialApp widget, which builds a number of useful widgets at the root of your app, including a Navigator, which manages a stack of widgets identified by strings, also known as “routes”. The Navigator lets you transition smoothly between screens of your application. Using the MaterialApp widget is entirely optional but a good practice.

## 6

All layout widgets have either of the following:

A child property if they take a single child—for example, Center or Container

A children property if they take a list of widgets—for example, Row, Column, ListView, or Stack.

## 7

Container: Adds padding, margins, borders, background color, or other decorations to a widget.

GridView: Lays widgets out as a scrollable grid.

ListView: Lays widgets out as a scrollable list.

Stack: Overlaps a widget on top of another.

## 8

Card: Organizes related info into a box with rounded corners and a drop shadow.

ListTile: Organizes up to 3 lines of text, and optional leading and trailing icons, into a row.

## 9

Use GridView to lay widgets out as a two-dimensional list.

GridView provides two pre-fabricated lists, or you can build your own custom grid. When a GridView detects that its contents are too long to fit the render box, it automatically scrolls.

## 10

ListView, a column-like widget, automatically provides scrolling when its content is too long for its render box.

## 11

Use Stack to arrange widgets on top of a base widget—often an image. The widgets can completely or partially overlap the base widget.

## 12

A Card, from the Material library, contains related nuggets of information and can be composed from almost any widget, but is often used with ListTile. Card has a single child, but its child can be a column, row, list, grid, or other widget that supports multiple children. By default, a Card shrinks its size to 0 by 0 pixels. You can use SizedBox to constrain the size of a card.

## 13

Use ListTile, a specialized row widget from the Material library, for an easy way to create a row containing up to 3 lines of text and optional leading and trailing icons. ListTile is most commonly used in Card or ListView, but can be used elsewhere.
