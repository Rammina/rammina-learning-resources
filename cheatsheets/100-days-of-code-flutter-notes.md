# 100 Days of Code Flutter Notes

## 1 

Text  

The Text widget lets you create a run of styled text within your application.

Also, newlines can be done with either using triple quotes or single quotes.

![FOdCt7-VgAQ53hM](https://user-images.githubusercontent.com/49326578/179341284-6a5c43ee-6529-47e3-856d-e542344234a2.png)

## 2

Row & Column

These flex widgets let you create flexible layouts in both the horizontal (Row) and vertical (Column) directions. Their design is based on the web’s flexbox layout model.

![FOiOM3MVkAUJJXm](https://user-images.githubusercontent.com/49326578/179341306-4e18a11d-b911-45ee-971e-b79fcfabf8ac.png)

## 3

Stack

Instead of being linearly oriented (either horizontally or vertically), a Stack widget lets you place widgets on top of each other in paint order. Based on the web’s absolute positioning model.

![FOmlGBtVUAM_FCP](https://user-images.githubusercontent.com/49326578/179341318-6d3b8b26-be86-4f76-a241-5f3238680224.png)

## 4

Container

Learned about Container

The Container widget lets you create a rectangular visual element. A container can be decorated with a BoxDecoration, such as a background, a border, or a shadow. 

![FOsmAl-VkAAQm56](https://user-images.githubusercontent.com/49326578/179341332-32f03147-3a49-4d24-9d77-c7724fa8ea27.png)

A Container can also have margins, padding, and constraints applied to its size. In addition, a Container can be transformed in three dimensional space using a matrix.

![FOsmQ2sVQAQ9DpP](https://user-images.githubusercontent.com/49326578/179341335-0256e339-c685-43f9-8714-8c25ee48eae6.png)

## 5

Material Design

Flutter provides a number of widgets that follow Material Design. A Material app starts with the MaterialApp widget, which builds a number of useful widgets at the root of your app. 

![FOvd6nKUcAIuZM4](https://user-images.githubusercontent.com/49326578/179341348-abf7f43b-cc07-4dc6-a0cd-572e88a8c2ce.jpg)

One of them is a Navigator widget, which manages a stack of widgets identified by strings, also known as “routes”. The Navigator lets you transition smoothly between screens of your application. Using the MaterialApp widget is entirely optional but a good practice.

## 6

All layout widgets have either:

`child` prop if they take a single child (e.g. Center, Container)

`children` prop if they take a list of widgets, such as Row, Column, ListView, or Stack.

![FO0_632VsAMZ9kt](https://user-images.githubusercontent.com/49326578/179341361-f82453da-2101-46f0-a208-a65da1779b43.png)

## 7

GridView: Lays widgets out as a scrollable grid.

ListView: Lays widgets out as a scrollable list.

Stack: Overlaps a widget on top of another.

![FO6DByJUYAUeg5a](https://user-images.githubusercontent.com/49326578/179341366-4b686aa5-854a-49fe-b95d-bc9fe1f057a5.jpg)

## 8

Card and ListTile Widgets

Card: Organizes related info into a box with rounded corners and a drop shadow.

ListTile: Organizes up to 3 lines of text, and optional leading and trailing icons, into a row.

![FPNkTY5UcAEaiha](https://user-images.githubusercontent.com/49326578/179341378-1eba806b-6a27-410d-84a0-9a199453caa2.jpg)

## 9

Practiced using GridView to lay widgets out as a 2D list.

It's nice, GridView has two pre-fabricated lists, or you can build your own custom grid. If its contents don't fit, it automatically scrolls.

![FPTQpdPVEAAX8e7](https://user-images.githubusercontent.com/49326578/179341380-4cc44029-56fe-4388-89f3-1a923012cb30.png)

## 10

ListView, a column-like widget, automatically gives scrolling when its content is too long.

It differs from GridView in child layout. With ListView, layout can be either vertically or horizontally only. 

![FPXts3NVsAABj6G](https://user-images.githubusercontent.com/49326578/179341388-ee9a4c80-3733-4319-b310-e80d23ab8278.png)

With GridView, its a combination of both. It lays its children horizontally first.

## 11

Use Stack to arrange widgets on top of a base widget—often an image. The widgets can completely or partially overlap the base widget.

![FPeOwHNVIAYFEnp](https://user-images.githubusercontent.com/49326578/179341403-2e589cb9-372e-418a-88cd-59215c124ea5.png)

## 12

A Card, from the Material library, contains related nuggets of information and can be composed from almost any widget, but is often used with ListTile. 

![FPi2uc6VcAAehao](https://user-images.githubusercontent.com/49326578/179341407-120d85db-c452-43c6-8f81-f4dc1aa4aa50.png)

Card has a single child, but its child can be a column, row, list, grid, or other widget that supports multiple children. By default, a Card shrinks its size to 0 by 0 pixels. You can use SizedBox to constrain the size of a card.

## 13

Use ListTile, a specialized row widget from the Material library, for an easy way to create a row containing up to 3 lines of text and optional leading and trailing icons. 

![FPnjUELVcAIVUhj](https://user-images.githubusercontent.com/49326578/179341418-1aa10c5c-6d2d-4065-8ea6-13d1a5f2beb1.png)

ListTile is most commonly used in Card or ListView, but can be used elsewhere.

## 14

The GestureDetector widget doesn’t have a visual representation but instead detects gestures made by the user. It can detect a variety of input gestures, including taps, drags, and scales.

![FPze167VcAcilwq](https://user-images.githubusercontent.com/49326578/179341424-85543493-ff53-43b5-a828-ee008afebe61.jpg)

## 15

Stateless widgets receive arguments from their parent widget, which they store in final member variables. When a widget is asked to build(), it uses them to make new arguments for the widgets it creates.

![FP3ukK0VkAEpUpf](https://user-images.githubusercontent.com/49326578/179341430-bcd750e4-7aa8-431c-a81a-3c5002eb3e2a.png)

## 16

StatefulWidgets are special widgets that know how to generate State objects, which are then used to hold state.

![FP9k9-0aIAQ3vWe](https://user-images.githubusercontent.com/49326578/179341441-9e87fa9a-2b1c-450a-a10e-57fe72afacb0.jpg)

## 17

Widgets are temporary objects, used to construct a presentation of the application in its current state. 

State objects, are persistent between calls to build(), allowing them to remember information.

![FQCrgxlXsAEKPve](https://user-images.githubusercontent.com/49326578/179341447-72d33925-5de0-4b08-8317-447f4ddc88da.jpg)

## 18

Change notifications flow “up” the widget tree by way of callbacks, while current state flows “down” to the stateless widgets that do presentation. The State is the common parent that redirects this flow

![FQIbk56VcAMGU52](https://user-images.githubusercontent.com/49326578/179341457-374d0e7f-0b2d-4c24-baed-8d7503d04457.jpg)

## 19

Responsive:

Responsive vs Adaptive App (1/2)

Typically, a responsive app has had its layout tuned for the available screen size. Re-laying out the UI if the user resizes the window, or changes device orientation.

![FQMRYO2VgAMl1WB](https://user-images.githubusercontent.com/49326578/179341485-d5c98198-4d9a-4bb2-b012-46d0939ebab8.jpg)

This is especially necessary when the same app can run on a variety of devices, from a watch, phone, tablet, to a laptop or desktop computer.

## 20

Adaptive:

Responsive vs Adaptive App (2/2)

Adapting an app to run on different device types, such as mobile and desktop, requires dealing with mouse and keyboard input, as well as touch input.

![FQRZqJmVQAEzILQ](https://user-images.githubusercontent.com/49326578/179341493-c1463153-d42d-4d25-b895-73c7bcb4f488.jpg)

It also means there are different expectations about the app’s visual density, how component selection works (cascading menus vs bottom sheets, for example), using platform-specific features (such as top-level windows), and more.

## 21

LayoutBuilder class

From its builder property, you get a BoxConstraints object. Examine the constraint’s properties to decide what to display. 

![FQXSSBlVIAEbY2D](https://user-images.githubusercontent.com/49326578/179341524-8f78d97c-a44f-4eac-8e70-453147802e91.jpg)

For example, if your maxWidth is greater than your width breakpoint, return a Scaffold object with a row that has a list on the left. If it’s narrower, return a Scaffold object with a drawer containing that list.

You can also adjust your display based on the device’s height, the aspect ratio, or some other property. When the constraints change (for example, the user rotates the phone, or puts your app into a tile UI in Nougat), the build function runs.

## 22

Use the MediaQuery.of() method in your build functions

It gives you the size, orientation, etc, of your app. Helpful for logic based on the complete context rather than on a specific widget's size.

![FQccMjmVEAA_lIC](https://user-images.githubusercontent.com/49326578/179341545-6d7f9266-854f-423c-a3e5-91cd278bcdf0.png)

Again, if you use this, then your build function automatically runs if the user somehow changes the app’s size.

## 23

AspectRatio class

AspectRatio is a widget that attempts to size the child to a specific aspect ratio.

The widget first tries the largest width permitted by the layout constraints. Then, the height is adjusted based on it

![FQiSCcPVEAAh9ai](https://user-images.githubusercontent.com/49326578/179341554-f608c4ba-6413-4561-a3d7-2f21414bc7bd.jpg)

## 24

OrientationBuilder class 

OrientationBuilder class builds a widget tree that can depend on the parent widget's orientation (distinct from the device orientation).

![FQnUE6KVsAI16Uk](https://user-images.githubusercontent.com/49326578/179341574-bdc4d690-394f-4dc9-bb48-85f4a9c95d5c.jpg)

# Layout widgets

## 25 Single Child

Align — Aligns a child within itself. It takes a double value between -1 and 1, for both the vertical and horizontal alignment.

![FQstlDRVEAQmjm_](https://user-images.githubusercontent.com/49326578/179341704-52bf7206-0240-43eb-84b5-96c190aea95c.png)

ConstrainedBox — Imposes size constraints on its child, offering control over the minimum or maximum size.

![FQ0TOiyVcAA-4uv](https://user-images.githubusercontent.com/49326578/179341712-bbe34b81-3441-449d-bffa-ec882aca2bb8.png)

CustomSingleChildLayout — Uses a delegate function to position a single child. The delegate can determine the layout constraints and positioning for the child.

![FQ5YHM5VEAAB48A](https://user-images.githubusercontent.com/49326578/179341715-d40cfe7c-e828-41fe-92ac-3373759d0664.jpg)

Expanded and Flexible — Allows a child of a Row or Column to shrink or grow to fill any available space.

![FQ-xxYnVIAEkQXo](https://user-images.githubusercontent.com/49326578/179341722-be87df3b-550f-4d90-8b9e-b2b7688324df.png)

FractionallySizedBox — Sizes its child to a fraction of the available space.

![FREcEGYVEAACD_L](https://user-images.githubusercontent.com/49326578/179341729-a62bfa00-163c-43db-b422-ad7ac95d072e.png)

SingleChildScrollView — Adds scrolling to a single child. Often used with a Row or Column.

![FRJF4J5UUAAmNAu](https://user-images.githubusercontent.com/49326578/179341734-7598d5ae-00ab-4ff3-8eb0-4e57df62fcc8.jpg)


## 26 Multichild

Column, Row, and Flex — Lays out children in a single horizontal or vertical run. Both Column and Row extend the Flex widget.

![FRN-WAQUUAAQYep](https://user-images.githubusercontent.com/49326578/179341747-4cc7453a-ad12-48e3-8e87-84f21d5de5e5.png)

CustomMultiChildLayout — Uses a delegate function to position multiple children during the layout phase.

https://twitter.com/i/status/1519109306775265280

Flow — Similar to CustomMultiChildLayout, but more efficient because it’s performed during the paint phase rather than the layout phase.

![FRY8IfvVsAEReUK](https://user-images.githubusercontent.com/49326578/179341816-343159b8-8435-45b6-963f-cab812d5ca96.jpg)

ListView, GridView, and CustomScrollView — Provides scrollable lists of children.

![FRd5a56VUAA-UJE](https://user-images.githubusercontent.com/49326578/179341824-4e809942-fb81-4c81-b8f9-d49e48b7c7fb.jpg)

Stack — Layers and positions multiple children relative to the edges of the Stack. Functions similarly to position-fixed in CSS.

Table — Uses a classic table layout algorithm for its children, combining multiple rows and columns.

Wrap — Displays its children in multiple horizontal or vertical runs.

It's very similar to CSS' 
`flex-wrap: wrap;`

![FRjMWwyVsAAePtN](https://user-images.githubusercontent.com/49326578/179341835-5dd97913-1c94-4d1f-b4aa-e13e78b7a27b.png)

## 27 

Different input devices offer various levels of precision, which require differently sized hit areas. Flutter’s VisualDensity class makes it easy to adjust the density of your views across the entire app

For example, the VisualDensity class helps by making a button larger (and therefore easier to tap) on a touch device.

https://twitter.com/i/status/1520609529263579136

## 28 

Screen-based breakpointbs

Use the MediaQuery API to implement screen-based breakpoints

In Flutter, the simplest form of procedural layouts uses screen-based breakpoints. 

If you're familiar with CSS, it's similar to @media

![FRtsqHwUUAAqhKm](https://user-images.githubusercontent.com/49326578/179341881-6ab14c4a-b275-4b65-8eae-78ee4cff6c1a.jpg)

There are no hard and fast rules for the sizes to use here, but these are general values:

class FormFactor { static double desktop = 900; static double tablet = 600; static double handset = 300; }

## 29

Design to the strengths of each form factor

Beyond screen size, you should also spend time considering the unique strengths and weaknesses of different form factors. It isn’t always ideal for your multiplatform app to offer identical functionality everywhere. Consider whether it makes sense to focus on specific capabilities, or even remove certain features, on some device categories.

## 30

Beyond screen size, you should also spend time considering the unique strengths and weaknesses of different form factors. Your multiplatform app can't simply offer identical functionality everywhere

![FRzGeDoVcAAMGiD](https://user-images.githubusercontent.com/49326578/179341899-6c8e7769-ad6a-4f0c-af66-b5d0859ddbb9.jpg)

Consider whether it makes sense to focus on specific capabilities, or even remove certain features, on some device categories.

## 31

Scroll wheel

Scrolling widgets like ScrollView or ListView support the scroll wheel by default, and because almost every scrollable custom widget is built using one of these, it works with them as well.

![FR4vIR2VkAEJ2eQ](https://user-images.githubusercontent.com/49326578/179341906-485d82a6-60bc-42c2-b43c-e7e7f47438fe.png)

If you need to implement custom scroll behavior, you can use the Listener widget, which lets you customize how your UI reacts to the scroll wheel.

## 32 

The FavoriteWidget class manages its own state, so it overrides createState() to create a State object. The framework calls createState() when it wants to build the widget. 

![FR98oPHUUAI3V2B](https://user-images.githubusercontent.com/49326578/179341919-3606d5f1-209c-4b76-ad97-a8099a893f2b.png)

## 33

setState() tells the Flutter framework that the widget’s state has changed and that the widget should be redrawn.

![FSCUr82VgAAf_Ar](https://user-images.githubusercontent.com/49326578/179341931-dc7c35a8-8784-4fc1-aede-69df746d6a3a.png)

## 34

IconButton class

The IconButton class, which is a material design icon button.

An icon button is a picture printed on a Material widget that reacts to touches by filling with color (ink).

https://twitter.com/i/status/1522791825018265600

## 35

GestureDetector class

A widget that detects gestures.

Attempts to recognize gestures that correspond to its non-null callbacks.

If this widget has a child, it defers to that child for its sizing behavior. If it does not have a child, it grows to fit the parent instead.

## 36

Form class Null safety

Form class is an container for grouping together form field widgets (e.g. TextField)

Form fields should be wrapped in a FormField widget, with the Form widget as a common ancestor of all of those. 

https://twitter.com/i/status/1523112738737721345

Call methods on FormState to save, reset, or validate each FormField that is a descendant of this Form. 

To obtain the FormState, you may use Form.of with a context whose ancestor is the Form, or pass a GlobalKey to the Form constructor and call GlobalKey.currentState.

## 37

FormField<T> class Null safety
A single form field.

This widget maintains the current state of the form field, so that updates and validation errors are visually reflected in the UI.

When used inside a Form, you can use methods on FormState to query or manipulate the form data as a whole. For example, calling FormState.save will invoke each FormField's onSaved callback in turn.
  
## 38
  
Checkbox class Null safety
  
Checkbox class, which is a material design checkbox.

The checkbox itself does not maintain any state. Instead, when the state of the checkbox changes, the widget calls the onChanged callback. 
  
https://twitter.com/i/status/1523536163079737344
  
Most widgets that use a checkbox will listen for the onChanged callback and rebuild the checkbox with a new value to update the visual appearance of the checkbox.
  
## 39
  
DropdownButton<T> class

DropdownButton class is a material design button for selecting from a list of items.

A dropdown button lets the user select from a number of items. 
  
https://twitter.com/i/status/1523781087180165121
  
The button shows the currently selected item as well as an arrow that opens a menu for selecting another item

All the entries in a menu must represent values with consistent types. Typically, an enum is used. Each DropdownMenuItem must be specialized with that same type argument

## 40
  
TextButton class
  
TextButton class that can be used as text buttons on toolbars, in dialogs, or inline with other content but offset from that content with padding so that the button's presence is obvious. 
  
https://twitter.com/i/status/1524141826298368000
  
Text buttons do not have visible borders and must therefore rely on their position relative to other content for context. In dialogs and cards, they should be grouped together in one of the bottom corners. 

Avoid using text buttons where they would blend in with other content.
  
## 41
  
FloatingActionButton class
  
FloatingActionButton class is a material design floating action button.

A floating action button is a circular icon button that hovers over content to promote a primary action in the application. 
  
https://twitter.com/i/status/1524510100467052544
  
Floating action buttons are most commonly used in the Scaffold.floatingActionButton field.

## 42
  
Radio<T> class
  
Use the Radio class select between a number of mutually exclusive values. 

When one radio button in a group is selected, the other radio buttons in the group cease to be selected.
  
https://twitter.com/i/status/1524892084880019458
  
The values are of type T, the type parameter of the Radio class. Enums are commonly used for this purpose.
  
## 43 
  
ElevatedButton class
  
This adds dimension to flat layouts, e.g. in long busy lists of content, or in wide spaces. Avoid using them on already-elevated content such as dialogs or cards.
  
https://twitter.com/i/status/1525294823439093760
  
An elevated button is a label child displayed on a Material widget whose Material.elevation increases when you press it. 

The label's Text and Icon widgets are displayed in style's ButtonStyle.foregroundColor and the button's filled background is the ButtonStyle.backgroundColor.
  
## 44
  
Slider class
  
Use the Slider class to select from either a continuous or a discrete set of values. 

It defaults with continuous values, from min to max. 

With non-null value for divisions, it becomes discrete.
  
https://twitter.com/i/status/1525630370640584704
  
## 45
  
Switch class
  
Switch class is used to toggle the on/off state of a single setting.

It does not maintain any state. Instead, when the state of the switch changes, the widget calls the onChanged callback.
  
https://twitter.com/i/status/1526021764475588608
  
Most widgets that use a switch will listen for the onChanged callback and rebuild the switch with a new value to update the visual appearance of the switch. Used to select from a range of values.
  
## 46
  
TextField class

Use the TextField class to create a text field that lets the user enter text, either with hardware keyboard or with an onscreen keyboard.
  
https://twitter.com/i/status/1526339657142652928
  
The text field calls the onChanged callback whenever the user changes the text in the field. 

If the user indicates that they are done typing in the field (e.g., by pressing a button on the soft keyboard), the text field calls the onSubmitted callback.
  
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
  
DevTools is a suite of performance and debugging tools for Dart and Flutter.
  
## 98
  
Here are some of the things you can do with DevTools:

Inspect the UI layout and state of a Flutter app.
Diagnose UI jank performance issues in a Flutter app.
CPU profiling for a Flutter or Dart app.
Network profiling for a Flutter app.
Source-level debugging of a Flutter or Dart app.
Debug memory issues in a Flutter or Dart command-line app.
View general log and diagnostics information about a running Flutter or Dart command-line app.
Analyze code and app size.
  
## 99
  
## 100
