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

## 16

StatefulWidgets are special widgets that know how to generate State objects, which are then used to hold state.

## 17

In Flutter, these two types of objects have different life cycles. Widgets are temporary objects, used to construct a presentation of the application in its current state. State objects, on the other hand, are persistent between calls to build(), allowing them to remember information.

## 18

In Flutter, change notifications flow “up” the widget hierarchy by way of callbacks, while current state flows “down” to the stateless widgets that do presentation. The common parent that redirects this flow is the State.

## 19

Responsive:

Typically, a responsive app has had its layout tuned for the available screen size. Often this means (for example), re-laying out the UI if the user resizes the window, or changes the device’s orientation. This is especially necessary when the same app can run on a variety of devices, from a watch, phone, tablet, to a laptop or desktop computer.

## 20

Adaptive:

Adapting an app to run on different device types, such as mobile and desktop, requires dealing with mouse and keyboard input, as well as touch input. It also means there are different expectations about the app’s visual density, how component selection works (cascading menus vs bottom sheets, for example), using platform-specific features (such as top-level windows), and more.

## 21

Use the LayoutBuilder class

From its builder property, you get a BoxConstraints object. Examine the constraint’s properties to decide what to display. For example, if your maxWidth is greater than your width breakpoint, return a Scaffold object with a row that has a list on the left. If it’s narrower, return a Scaffold object with a drawer containing that list. You can also adjust your display based on the device’s height, the aspect ratio, or some other property. When the constraints change (for example, the user rotates the phone, or puts your app into a tile UI in Nougat), the build function runs.

## 22

Use the MediaQuery.of() method in your build functions

This gives you the size, orientation, etc, of your current app. This is more useful if you want to make decisions based on the complete context rather than on just the size of your particular widget. Again, if you use this, then your build function automatically runs if the user somehow changes the app’s size.

## 23

AspectRatio class
A widget that attempts to size the child to a specific aspect ratio.

The widget first tries the largest width permitted by the layout constraints. The height of the widget is determined by applying the given aspect ratio to the width, expressed as a ratio of width to height.

## 24

OrientationBuilder class 
Builds a widget tree that can depend on the parent widget's orientation (distinct from the device orientation).


# Layout widgets

## 25 Single Child

Align — Aligns a child within itself. It takes a double value between -1 and 1, for both the vertical and horizontal alignment.

ConstrainedBox — Imposes size constraints on its child, offering control over the minimum or maximum size.

CustomSingleChildLayout — Uses a delegate function to position a single child. The delegate can determine the layout constraints and positioning for the child.

Expanded and Flexible — Allows a child of a Row or Column to shrink or grow to fill any available space.

FractionallySizedBox — Sizes its child to a fraction of the available space.

SingleChildScrollView — Adds scrolling to a single child. Often used with a Row or Column.


## 26 Multichild

Column, Row, and Flex — Lays out children in a single horizontal or vertical run. Both Column and Row extend the Flex widget.

CustomMultiChildLayout — Uses a delegate function to position multiple children during the layout phase.

Flow — Similar to CustomMultiChildLayout, but more efficient because it’s performed during the paint phase rather than the layout phase.

ListView, GridView, and CustomScrollView — Provides scrollable lists of children.

Stack — Layers and positions multiple children relative to the edges of the Stack. Functions similarly to position-fixed in CSS.

Table — Uses a classic table layout algorithm for its children, combining multiple rows and columns.

Wrap — Displays its children in multiple horizontal or vertical runs.


## 27 

Different input devices offer various levels of precision, which necessitate differently sized hit areas. Flutter’s VisualDensity class makes it easy to adjust the density of your views across the entire application, for example, by making a button larger (and therefore easier to tap) on a touch device.

When you change the VisualDensity for your MaterialApp, MaterialComponents that support it animate their densities to match. By default, both horizontal and vertical densities are set to 0.0, but you can set the densities to any negative or positive value that you want. By switching between different densities, you can easily adjust your UI:

## 28 

Screen-based breakpoints

The simplest form of procedural layouts uses screen-based breakpoints. In Flutter, this can be done with the MediaQuery API. There are no hard and fast rules for the sizes to use here, but these are general values:

class FormFactor {
  static double desktop = 900;
  static double tablet = 600;
  static double handset = 300;
}

## 29

Design to the strengths of each form factor

Beyond screen size, you should also spend time considering the unique strengths and weaknesses of different form factors. It isn’t always ideal for your multiplatform app to offer identical functionality everywhere. Consider whether it makes sense to focus on specific capabilities, or even remove certain features, on some device categories.

## 30

Use desktop build targets for rapid testing

One of the most effective ways to test adaptive interfaces is to take advantage of the desktop build targets.

When running on a desktop, you can easily resize the window while the app is running to preview various screen sizes. This, combined with hot reload, can greatly accelerate the development of a responsive UI.

## 31

Scroll wheel

Scrolling widgets like ScrollView or ListView support the scroll wheel by default, and because almost every scrollable custom widget is built using one of these, it works with them as well.

If you need to implement custom scroll behavior, you can use the Listener widget, which lets you customize how your UI reacts to the scroll wheel.

## 32 

The FavoriteWidget class manages its own state, so it overrides createState() to create a State object. The framework calls createState() when it wants to build the widget. In this example, createState() returns an instance of _FavoriteWidgetState

## 33

The _toggleFavorite() method, which is called when the IconButton is pressed, calls setState(). Calling setState() is critical, because this tells the framework that the widget’s state has changed and that the widget should be redrawn.

## 34

IconButton class

A material design icon button.

An icon button is a picture printed on a Material widget that reacts to touches by filling with color (ink).

Icon buttons are commonly used in the AppBar.actions field, but they can be used in many other places as well.

## 35

GestureDetector class

A widget that detects gestures.

Attempts to recognize gestures that correspond to its non-null callbacks.

If this widget has a child, it defers to that child for its sizing behavior. If it does not have a child, it grows to fit the parent instead.

## 36

Form class Null safety
An optional container for grouping together multiple form field widgets (e.g. TextField widgets).

Each individual form field should be wrapped in a FormField widget, with the Form widget as a common ancestor of all of those. Call methods on FormState to save, reset, or validate each FormField that is a descendant of this Form. To obtain the FormState, you may use Form.of with a context whose ancestor is the Form, or pass a GlobalKey to the Form constructor and call GlobalKey.currentState.

## 37

FormField<T> class Null safety
A single form field.

This widget maintains the current state of the form field, so that updates and validation errors are visually reflected in the UI.

When used inside a Form, you can use methods on FormState to query or manipulate the form data as a whole. For example, calling FormState.save will invoke each FormField's onSaved callback in turn.
  
## 38
  
Checkbox class Null safety
  
A material design checkbox.

The checkbox itself does not maintain any state. Instead, when the state of the checkbox changes, the widget calls the onChanged callback. Most widgets that use a checkbox will listen for the onChanged callback and rebuild the checkbox with a new value to update the visual appearance of the checkbox.
  
## 39
  
DropdownButton<T> class Null safety

A material design button for selecting from a list of items.

A dropdown button lets the user select from a number of items. The button shows the currently selected item as well as an arrow that opens a menu for selecting another item.

The type T is the type of the value that each dropdown item represents. All the entries in a given menu must represent values with consistent types. Typically, an enum is used. Each DropdownMenuItem in items must be specialized with that same type argument.

## 40
  
TextButton class Null safety
  
A Material Design "Text Button".

Use text buttons on toolbars, in dialogs, or inline with other content but offset from that content with padding so that the button's presence is obvious. Text buttons do not have visible borders and must therefore rely on their position relative to other content for context. In dialogs and cards, they should be grouped together in one of the bottom corners. Avoid using text buttons where they would blend in with other content, for example in the middle of lists.
  
## 41
  
FloatingActionButton class Null safety
  
A material design floating action button.

A floating action button is a circular icon button that hovers over content to promote a primary action in the application. Floating action buttons are most commonly used in the Scaffold.floatingActionButton field.

## 42
  
Radio<T> class Null safety
  
A material design radio button.

Used to select between a number of mutually exclusive values. When one radio button in a group is selected, the other radio buttons in the group cease to be selected. The values are of type T, the type parameter of the Radio class. Enums are commonly used for this purpose.
  
## 43 
  
ElevatedButton class Null safety
  
A Material Design "elevated button".

Use elevated buttons to add dimension to otherwise mostly flat layouts, e.g. in long busy lists of content, or in wide spaces. Avoid using elevated buttons on already-elevated content such as dialogs or cards.

An elevated button is a label child displayed on a Material widget whose Material.elevation increases when the button is pressed. The label's Text and Icon widgets are displayed in style's ButtonStyle.foregroundColor and the button's filled background is the ButtonStyle.backgroundColor.
  
## 44
  
Slider class Null safety
  
A Material Design slider.

A slider can be used to select from either a continuous or a discrete set of values. The default is to use a continuous range of values from min to max. To use discrete values, use a non-null value for divisions, which indicates the number of discrete intervals.
  
## 45
  
Switch class Null safety
  
A material design switch.

Used to toggle the on/off state of a single setting.

The switch itself does not maintain any state. Instead, when the state of the switch changes, the widget calls the onChanged callback. Most widgets that use a switch will listen for the onChanged callback and rebuild the switch with a new value to update the visual appearance of the switch.
Used to select from a range of values.
  
## 46
  
TextField class Null safety
A material design text field.

A text field lets the user enter text, either with hardware keyboard or with an onscreen keyboard.

The text field calls the onChanged callback whenever the user changes the text in the field. If the user indicates that they are done typing in the field (e.g., by pressing a button on the soft keyboard), the text field calls the onSubmitted callback.
