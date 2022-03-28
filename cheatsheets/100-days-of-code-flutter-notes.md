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

## 14

The GestureDetector widget doesn’t have a visual representation but instead detects gestures made by the user. When the user taps the Container, the GestureDetector calls its onTap() callback, in this case printing a message to the console. You can use GestureDetector to detect a variety of input gestures, including taps, drags, and scales.

## 15

Stateless widgets receive arguments from their parent widget, which they store in final member variables. When a widget is asked to build(), it uses these stored values to derive new arguments for the widgets it creates.

## 15

StatefulWidgets are special widgets that know how to generate State objects, which are then used to hold state.

## 16

In Flutter, these two types of objects have different life cycles. Widgets are temporary objects, used to construct a presentation of the application in its current state. State objects, on the other hand, are persistent between calls to build(), allowing them to remember information.

## 17

In Flutter, change notifications flow “up” the widget hierarchy by way of callbacks, while current state flows “down” to the stateless widgets that do presentation. The common parent that redirects this flow is the State.

## 18

Responsive:

Typically, a responsive app has had its layout tuned for the available screen size. Often this means (for example), re-laying out the UI if the user resizes the window, or changes the device’s orientation. This is especially necessary when the same app can run on a variety of devices, from a watch, phone, tablet, to a laptop or desktop computer.

## 19

Adaptive:

Adapting an app to run on different device types, such as mobile and desktop, requires dealing with mouse and keyboard input, as well as touch input. It also means there are different expectations about the app’s visual density, how component selection works (cascading menus vs bottom sheets, for example), using platform-specific features (such as top-level windows), and more.

## 20

Use the LayoutBuilder class

From its builder property, you get a BoxConstraints object. Examine the constraint’s properties to decide what to display. For example, if your maxWidth is greater than your width breakpoint, return a Scaffold object with a row that has a list on the left. If it’s narrower, return a Scaffold object with a drawer containing that list. You can also adjust your display based on the device’s height, the aspect ratio, or some other property. When the constraints change (for example, the user rotates the phone, or puts your app into a tile UI in Nougat), the build function runs.
