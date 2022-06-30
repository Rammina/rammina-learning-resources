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
  
## 47  
  
AnimatedWidget class 
  
A widget that rebuilds when the given Listenable changes value
  
AnimatedWidget is most commonly used with Animation objects, which are Listenable, but it can be used with any Listenable, including ChangeNotifier and ValueNotifier.

AnimatedWidget is most useful for widgets that are otherwise stateless. To use AnimatedWidget, simply subclass it and implement the build function.
  
## 48
  
The primary building block of the animation system is the Animation class. An animation represents a value of a specific type that can change over the lifetime of the animation. Most widgets that perform an animation receive an Animation object as a parameter, from which they read the current value of the animation and to which they listen for changes to that value.

## 49
  
AnimatedBuilder class 
A general-purpose widget for building animations.

AnimatedBuilder is useful for more complex widgets that wish to include an animation as part of a larger build function. To use AnimatedBuilder, simply construct the widget and pass it a builder function.

For simple cases without additional state, consider using AnimatedWidget.
  
## 50
  
Animations also provide an AnimationStatus, which indicates how the animation will evolve over time. Whenever the animation’s status changes, the animation notifies all the listeners added with addStatusListener. Typically, animations start out in the dismissed status, which means they’re at the beginning of their range.
  
## 51
  
AnimationController class 
A controller for an animation.

This class lets you perform tasks such as:

Play an animation forward or in reverse, or stop an animation.
Set the animation to a specific value.
Define the upperBound and lowerBound values of an animation.
Create a fling animation effect using a physics simulation.

## 52
  
TickerProvider class
  
An interface implemented by classes that can vend Ticker objects.

Tickers can be used by any object that wants to be notified whenever a frame triggers, but are most commonly used indirectly via an AnimationController.
  
## 54
  
WidgetTester class
  
Class that programmatically interacts with widgets and the test environment.

For convenience, instances of this class (such as the one provided by testWidgets) can be used as the vsync for AnimationController objects.
  
## 55
  
Tween<T extends Object?> class
A linear interpolation between a beginning and ending value.

Tween is useful if you want to interpolate across a range.

To use a Tween object with an animation, call the Tween object's animate method and pass it the Animation object that you want to modify.
  
## 56
  
ColorTween class
An interpolation between two colors.

This class specializes the interpolation of Tween<Color> to use Color.lerp.

The values can be null, representing no color (which is distinct to transparent black, as represented by Colors.transparent).
  
## 57
  
RectTween class 
An interpolation between two rectangles.

This class specializes the interpolation of Tween<Rect> to use Rect.lerp.

The values can be null, representing a zero-sized rectangle at the origin (Rect.zero).
  
## 58
  
ReverseAnimation class
  
An animation that is the reverse of another animation.

If the parent animation is running forward from 0.0 to 1.0, this animation is running in reverse from 1.0 to 0.0.

Using a ReverseAnimation is different from simply using a Tween with a begin of 1.0 and an end of 0.0 because the tween does not change the status or direction of the animation.
  
## 59
  
FlippedCurve class
  
A curve that is the reversed inversion of its given curve.

This curve evaluates the given curve in reverse (i.e., from 1.0 to 0.0 as t increases from 0.0 to 1.0) and returns the inverse of the given curve's value (i.e., 1.0 minus the given curve's value).
  
## 60
  
SchedulerBinding mixin 
Scheduler for running the following:

Transient callbacks, triggered by the system's dart:ui.PlatformDispatcher.onBeginFrame callback, for synchronizing the application's behavior to the system's display. For example, Tickers and AnimationControllers trigger from these.

Persistent callbacks, triggered by the system's dart:ui.PlatformDispatcher.onDrawFrame callback, for updating the system's display after transient callbacks have executed. For example, the rendering layer uses this to drive its rendering pipeline.

Post-frame callbacks, which are run after persistent callbacks, just before returning from the dart:ui.PlatformDispatcher.onDrawFrame callback.

Non-rendering tasks, to be run between frames. These are given a priority and are executed in priority order according to a schedulingStrategy.
  
## 61
  
Simulation class
The base class for all simulations.

A simulation models an object, in a one-dimensional space, on which particular forces are being applied, and exposes:

The object's position, x
The object's velocity, dx
Whether the simulation is "done", isDone
A simulation is generally "done" if the object has, to a given tolerance, come to a complete rest.
  
## 62
  
BouncingScrollSimulation class Null safety
An implementation of scroll physics that matches iOS.
 
ClampingScrollSimulation class Null safety
An implementation of scroll physics that matches Android.
  
## 63
  
Animatable<T> class
An object that can produce a value of type T given an Animation<double> as input.

Typically, the values of the input animation are nominally in the range 0.0 to 1.0. In principle, however, any value could be provided.

The main subclass of Animatable is Tween.
  
## 64
  
Curves
The Curve abstract class maps doubles nominally in the range 0.0-1.0 to doubles nominally in the range 0.0-1.0.

Curve classes are stateless and immutable.

## 65
 
Intent class 
An abstract class representing a particular configuration of an Action.

This class is what the Shortcuts.shortcuts map has as values, and is used by an ActionDispatcher to look up an action and invoke it, giving it this object to extract configuration information from.
  
## 66
  
Action<T extends Intent> class
Base class for actions.

As the name implies, an Action is an action or command to be performed. They are typically invoked as a result of a user action, such as a keyboard shortcut in a Shortcuts widget, which is used to look up an Intent, which is given to an ActionDispatcher to map the Intent to an Action and invoke it.

The ActionDispatcher can invoke an Action on the primary focus, or without regard for focus.
  
## 67
  
CallbackAction<T extends Intent> class
  
An Action that takes a callback in order to configure it without having to create an explicit Action subclass just to call a callback.
  
## 68
  
Shortcuts 
  
Are key bindings that activate by pressing a key or combination of keys. The key combinations reside in a table with their bound intent. When the Shortcuts widget invokes them, it sends their matching intent to the actions subsystem for fulfillment.
  
## 69
  
Flutter has an ActivateIntent widget that maps each type of control to its corresponding version of an ActivateAction (and that executes the code that activates the control). This code often needs fairly private access to do its work.
  
## 70
  
CallbackShortcuts class
A widget that provides an uncomplicated mechanism for binding a key combination to a specific callback.

This is similar to the functionality provided by the Shortcuts widget, but instead of requiring a mapping to an Intent, and an Actions widget somewhere in the widget tree to bind the Intent to, it just takes a set of bindings that bind the key combination directly to a VoidCallback.

## 71
  
Ephemeral state (sometimes called UI state or local state) is the state you can neatly contain in a single widget.

This is, intentionally, a vague definition, so here are a few examples.

current page in a PageView
current progress of a complex animation
current selected tab in a BottomNavigationBar
Other parts of the widget tree seldom need to access this kind of state. There is no need to serialize it, and it doesn’t change in complex ways.
  
## 72
  
App state
State that is not ephemeral, that you want to share across many parts of your app, and that you want to keep between user sessions, is what we call application state (sometimes also called shared state).

Examples of application state:

User preferences
Login info
Notifications in a social networking app
The shopping cart in an e-commerce app
Read/unread state of articles in a news app
For managing app state, you’ll want to research your options. Your choice depends on the complexity and nature of your app, your team’s previous experience, and many other aspects.
  
## 73
  
ChangeNotifier is a simple class included in the Flutter SDK which provides change notification to its listeners. In other words, if something is a ChangeNotifier, you can subscribe to its changes. (It is a form of Observable, for those familiar with the term.)
  
## 74
  
ChangeNotifierProvider is the widget that provides an instance of a ChangeNotifier to its descendants. It comes from the provider package.
  
## 75
  
By default, Flutter only provides US English localizations. To add support for other languages, an application must specify additional MaterialApp (or CupertinoApp) properties, and include a package called flutter_localizations.
  
## 76
  
scriptCode property
  
The script subtag of the Locale Identifier, null if absent.

It is syntactically valid and normalized (has correct case), but not necessarily valid (the script might not exist) because the list of valid scripts changes with time.
  
## 77
  
Locale class
  
An identifier used to select a user's language and formatting preferences.

This represents a Unicode Language Identifier (i.e. without Locale extensions), except variants are not supported.

Locales are canonicalized according to the "preferred value" entries in the IANA Language Subtag Registry. For example, const Locale('he') and const Locale('iw') are equal and both have the languageCode he, because iw is a deprecated language subtag that was replaced by the subtag he.
  
## 78
  
GlobalWidgetsLocalizations class
  
Localized values for widgets.

Currently this class just maps locale to textDirection. All locales are TextDirection.ltr except for locales with the following Locale.languageCode values, which are TextDirection.rtl:

ar - Arabic
fa - Farsi
he - Hebrew
ps - Pashto
sd - Sindhi
ur - Urdu
  
## 79
  
supportedLocales property
  
The list of locales that this app has been localized for.

By default only the American English locale is supported. Apps should configure this list to match the locales they support.

This list must not null. Its default value is just [const Locale('en', 'US')].
  
## 80
  
LocaleResolutionCallback typedef
  
The signature of WidgetsApp.localeResolutionCallback.

It is recommended to provide a LocaleListResolutionCallback instead of a LocaleResolutionCallback when possible, as LocaleResolutionCallback only receives a subset of the information provided in LocaleListResolutionCallback.

A LocaleResolutionCallback is responsible for computing the locale of the app's Localizations object when the app starts and when user changes the default locale for the device after LocaleListResolutionCallback fails or is not provided.
  
## 81
  
GlobalMaterialLocalizations class
  
Implementation of localized strings for the material widgets using the intl package for date and time formatting.
  
## 82
  
dart:convert library
  
Encoders and decoders for converting between different data representations, including JSON and UTF-8.

In addition to converters for common data representations, this library provides support for implementing converters in a way which makes them easy to chain and to use with streams.
  
## 83
  
Flutter supports using shared packages contributed by other developers to the Flutter and Dart ecosystems. This allows quickly building an app without having to develop everything from scratch.
 
## 84
  
Packages
  
At a minimum, a Dart package is a directory containing a pubspec file. Additionally, a package can contain dependencies (listed in the pubspec), Dart libraries, apps, resources, tests, images, and examples.
  
## 85
  
Federated plugins
  
Federated plugins are a way of splitting support for different platforms into separate packages. So, a federated plugin can use one package for iOS, another for Android, another for web, and yet another for a car (as an example of an IoT device).
  
## 86
  
Package versions
  
All packages have a version number, specified in the package’s pubspec.yaml file. The current version of a package is displayed next to its name (for example, see the url_launcher package), as well as a list of all prior versions (see url_launcher versions).
  
## 87
 
Updating package dependencies
  
When running flutter pub get (Packages get in IntelliJ or Android Studio) for the first time after adding a package, Flutter saves the concrete package version found in the pubspec.lock lockfile. This ensures that you get the same version again if you, or another developer on your team, run flutter pub get.
  
## 88
  
To upgrade to a new version of the package, for example to use new features in that package, run flutter pub upgrade (Upgrade dependencies in IntelliJ or Android Studio) to retrieve the highest available version of the package that is allowed by the version constraint specified in pubspec.yaml.
  
## 89
  
Dependencies on unpublished packages
  
Packages can be used even when not published on pub.dev. For private plugins, or for packages not ready for publishing, additional dependency options are available
  
## 90
  
Path dependency
  
A Flutter app can depend on a plugin via a file system path: dependency. The path can be either relative or absolute. Relative paths are evaluated relative to the directory containing pubspec.yaml.
  
## 91
  
If you are exclusively writing Flutter apps with Dart code and not using platform-specific libraries, or otherwise accessing platform-specific features, you can debug your code using your IDE’s debugger. 
  
## 92
  
If you’re writing a platform-specific plugin or using platform-specific libraries written in Swift, ObjectiveC, Java, or Kotlin, you can debug that portion of your code using Xcode (for iOS) or Android Gradle (for Android).
  
## 93
  
Flutter inspector
  
There are two other features provided by the Flutter plugin that you might find useful. The Flutter inspector is a tool for visualizing and exploring the Flutter widget tree and helps you:

Understand existing layouts
Diagnose layout issues
  
## 94  
  
Flutter outline
  
The Flutter Outline displays the build method in visual form. Note that this might be different than the widget tree for the build method. Toggle display of the outline using the vertical button to the right of the AS window.
  
## 95
  
Debug
In debug mode, the app is set up for debugging on the physical device, emulator, or simulator.

Debug mode for mobile apps mean that:

Assertions are enabled.
Service extensions are enabled.
Compilation is optimized for fast development and run cycles (but not for execution speed, binary size, or deployment).
Debugging is enabled, and tools supporting source level debugging (such as DevTools) can connect to the process.
  
## 96
  
Release
Use release mode for deploying the app, when you want maximum optimization and minimal footprint size. For mobile, release mode (which is not supported on the simulator or emulator), means that:

Assertions are disabled.
Debugging information is stripped out.
Debugging is disabled.
Compilation is optimized for fast startup, fast execution, and small package sizes.
Service extensions are disabled.
  
## 97
  
## 98
  
## 99
  
## 100
