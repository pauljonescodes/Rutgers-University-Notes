# Software Methodology Notes 

## Description 

This course teaches essential principles, techniques, tools, and methods used to develop large software programs in Java. These include object-oriented programming and design, Unified Modeling Language (UML), testing and debugging, using and documenting APIs, asynchronous (event-driven) programming in a Graphical Use Interface (GUI) framework, code maintenance and version management using CVS, software development using Eclipse, introduction to building software on mobile platforms, introduction to multithreading, network programming, and object persistence.

+ Topics:
    - Inheritance, interfaces, abstract classes, polymorphism
    - Unified Modeling Language (UML)
    - Essential design patterns, including Singleton, Model-View-Controller (MVC),
     Template Method, State
    - Black-box unit testing, debugging, developing large applications in Eclipse
    - Object persistence, serialization
    - Code management using CVS
    - Designing and implementing GUIs using Java Swing and AWT
    - Frames, dialogs, panels, widgets, tables, layouts, colors, fonts, drawing, painting
    - The Swing MVC architecture and working with data models
    - Event handling
    - Introduction to software development on mobile platforms
    - Introduction to multithreading
    - Introduction to network programming

## Syllabus

- Topics
	1. Overview of software methodology. Object-oriented programming. Iterative development. Testing. Documentation. Source code management with Mercurial.
	2. Object-Oriented Design with Java. Class design, interfaces, inheritance, abstract classes, polymorphism.
	3. UML class diagrams to represent object-oriented design. Classes, generalizations, associations, dependencies.
	4. Event-driven Graphical User Interface (GUI) programming. Event registration, listeners, handling events. Java Swing and AWT. Components and containers. Frames, dialogs, panels, layouts, colors, fonts, drawing, painting.
	5. Model-View-Controller (MVC) design pattern. The Swing MVC architecture and working with data models.
	6. State-based programming. State design pattern.
	7. Iterative development - feature extension, code reuse, versioning, backward compatibility, object serialization.
	8. Block-box unit testing. Boundary values. Equivalence Classes. Debugging in Eclipse.
	9. Multithreading and synchronization on shared resources.
	10. Developing Android apps in Eclipse. Device emulators. Structure of Android apps. Java source code, resources, manifest file, xml layout, density independent pixels.
	11. App lifecycle, activities, passing information between activities. Layouts, views, widgets, menus, context menus, dialogs, inflating views from xml.
	12. Implementing search with search bar. I/O. Icons and drawables.
	13. Packaging an app for publishing to the Android Market.
	14. Introduction to network programming. Java networking API. Client-server programming with TCP/IP sockets and server sockets.
- Grading
	+ Recitation attendance: 50 (5%)
	+ Homework assignments: 150 (15%)
	+ Object-oriented GUI project: 300 (30%) 
	+ Android project: 200 (20%)
	+ Quizzes: 100 (10%)
	+ Final exam: 200 (20%)

## January 22nd, 2012 - Lecture

- Many things that you use when building a Java GUI, you'll be using widgets from Swing API.
- With JButtons, the simplest way to have something in the button is tompass text to the constructor.
- With JFrames, you want to display content in a certain arragement, using something called a layout manager.
- With different LayoutManagers, you get different arrangments.
- Other LayoutManagers include BorderLayout, GridLayout, ...
- For any frame and any window, you can set a size.
- Alyways set your frame to being visible.
- For every button or widget that sets off an action, you're going to need an event listener.
- Before Swing, there was AWT. And if you thought Swing was bad, well, AWT was worse.
- ActionListeners are interfaces - a la Comparable, Iterable, etc ...
- LayoutManagers can handle resizing of windows and other unexpected happenings.
- If you set the location relative to `null`, then you get a centered window.

## January 24th, 2013 - Lecture

- `ActionListener` is an interface - you need to define a class.
- In the package `jwt.java.event`, `ActionListener` is a subclass of the subclass of all interfaces.
- You will localize interface definitions if you will never need the code again, generalize it otherwise.
- We defined another class called `ButtonListener` which is in the same source file as `FC.java`.
- You can have multiple classes in the same source, but only one of them can be public.
- If you define a class that implements an interface after an instantion, it is called an "anonymous class."
- Whenever you add a listener, it sets in motion a mechanism within Java to handle the action.
- With `ActionListener`, all the information about the widget that the action was performed on is included.
	+ For example, you can get the text from a text button.
- If you add a class to listen to an action, it must implement `ActionPerformed(ActionEvent e)`.
- If you have multiple classes defined in the same source code, and you want to import one of them, you'll need to `import [filename].[classname]`.
- When you program in static, you working outside of the object oriented framework.
- You are only limited to one public class when the classes are defined at the same level.
- Java is meant to be platform independant.
- An `Object` reference does not "know" what type of object it is.

## January 28th, 2013 - Recitation: Problem Set 1 (GUI, Javadoc, Inheritence)

1. Write a program that creates a frame with two buttons on it: OK and Quit. When OK is clicked, nothing will happen. When Quit is clicked, the application will exit. The application window (frame) should be launched in the center of the screen, and should NOT be closed when the user clicks on the 'x' button in the title bar. (In other words, the only way to close the window is to click on the 'Quit' button.)

		package recitation;
		import java.awt.FlowLayout;
		import java.awt.event.ActionEvent;
		import java.awt.event.ActionListener;
		import javax.swing.JButton;
		import javax.swing.JFrame;
		
		public class OKQuit extends JFrame {

        private JButton ok, quit;
        
        public OKQuit() {
                ok = new JButton("OK");
                quit = new JButton("Quit");
                setLayout(new FlowLayout(FlowLayout.LEFT,15,15));
                add(ok);
                add(quit);
                
                quit.addActionListener(new ActionListener() {
                        public void actionPerformed(ActionEvent e) {
                                System.exit(1);
                        }
                });
        }
        
        /**
         * @param args
         */
        public static void main(String[] args) {
                // TODO Auto-generated method stub
                OKQuit okquit = new OKQuit();
                okquit.setDefaultCloseOperation(DO_NOTHING_ON_CLOSE);
                okquit.setSize(200,80);
                okquit.setLocationRelativeTo(null);
                okquit.setVisible(true);
        }
		}
		
2. Redesign the Fahrenheit-Celsius GUI we did in the first lecture to do away with the buttons to convert between F and C. Instead, when the user types something in one of the text fields, the converted value shows up immediately in the other. So your GUI looks like this:

		        Fahrenheit       Celsius
		        ----------     ----------
		       |          |   |          |
		        ----------     ----------
Also, give the frame a title (that appears in the title bar) and make the text right-aligned in both text fields (digits are displayed right to left). Read the documentation for JTextField in the Java API to see how to right-align text. You can register an action listener directly on a text field to receive an event when the user hits enter after entering text in the text field.

			package recitation;
		    import javax.swing.*;
		    import java.awt.*;
		    import java.awt.event.*;
			public class FCNoButtons extends JFrame {
		        JLabel f,c;
		        JTextField F,C;
        
				public FCNoButtons(String title) {
              	  super(title);
                	f = new JLabel(" Fahrenheit");
                	c = new JLabel("   Celsius");
                	F = new JTextField(5);
                	C = new JTextField(5);
                	F.setHorizontalAlignment(JTextField.RIGHT);
                	C.setHorizontalAlignment(JTextField.RIGHT);
                
                	setLayout(new FlowLayout(FlowLayout.LEFT, 15, 15));
                
                	add(f);
                	add(c);
                	add(F);
                	add(C);
                
                F.addActionListener(new ActionListener() { 
                        public void actionPerformed(ActionEvent e) { 
                                float fval = Float.parseFloat(F.getText());
                                float cval = (fval-32)*5.0f/9.0f;
                                String cstr = String.format("%5.1f", cval);
                                C.setText(cstr);
                        }
                });
                
                C.addActionListener(new ActionListener() { // anonymous class
                        public void actionPerformed(ActionEvent e) { 
                                float cval = Float.parseFloat(C.getText());
                                float fval = 9.0f/5.0f*cval + 32f;
                                String fstr = String.format("%5.1f", fval);
                                F.setText(fstr);
            		            }
                		});
       		 }
        
        
			/**
			* @param args
			 */
       		 public static void main(String[] args) {
            		    FCNoButtons fc = new FCNoButtons("F-C Converter");
                		fc.setSize(200,120);
                		fc.setResizable(false); 
                		fc.setVisible(true);
                		fc.setLocationRelativeTo(null);
                		fc.setDefaultCloseOperation(EXIT_ON_CLOSE);
   		     }
				}
	- This problem requires only labels and text fields.
	- Think of this as a "project description", a very simple one.
	- Give the frame a title.
3. Documenting with Javadoc
	- Make a comment which begins with two stars 
	- Then hit "generate javadoc" in Eclipse to create a generic website based on that information.
	- Can include fields such as `@see`, `@author`, `@version`, and `@since`
4. What is the output of this code? Why?

		   class GrandParent { }
		   class Parent extends GrandParent{ }
		   class Child extends Parent { }

		   class Foo {
		      public void bar(GrandParent p) {
		         System.out.println("called with type GrandParent");
		      }
 		     public void bar(Parent p) {
		         System.out.println("called with type Parent");
		      }
		   }

		   public class Test {
		      public static void main(String[] args) {
		         new Foo().bar(new Child());
		    }
The output is:
			
			called with type Parent
The method call matches the argument type (`Child`) with the closest matching parameter type (`Parent`). So the method `Foo.bar(Parent)` is called.

## January 29th, 2013 - Lecture

- It's one thing to write code that hacks through a GUI, it's wholly another to write an extensible, usuable GUI.
- How can we write code that is easily extensible?
- Inheritence simply means that the code you've written in the parent need not be rewritten.
- You have to initialize the superclass portion first, and then then the subclass portion afterwards.
- The constructors are not inherited.
- The name of the constructor is taken from the name of the class, so they're not inherited.
- Static vs. dynamic type
	+ There is a difference between compile time and run time types.
	
				Point p1 = new Point(2,3);

		* Compile time type: `Point p1`
		* Run time type: `2,3`
		
				Point p2 = new ColoredPoint(3,4,"red");

		* Compile time type: `Point p2`
		* Run time type: `ColoredPoint 3,4,"red"`
	+ Dynamic binding: at runtime, the actual method being called is bound to that call.
	+ You can't initialize a child as a parent, and every parent 
	+ If an object is statically declared to be of a certain type, it can only calls those methods in that type.
	+ However, at runtime, it can call whatever it is dynamically assigned to be.
	+ Typecasting tells the compiler to ignore the declared type and use this "typecast" type instead. Example:

			(ColoredPoint)p2.getColor();
	+ Typecasting usually is indicative of not following design intent or having poor design.
- You cannot access private variables through the object.
- A subclass inherits the subclasses private fields.	
- It's a beginner's mistake to write an `equals` method like this:

		public boolean equals (Point p) {
			return x == p.x && y = p.y;
		}
- Here's an instance where typecasting is fine, and a good `equals` method:

		public boolean equals (Object o) {
			if (o == null || !(o instanceof Point))
				return null;
			Point p = (Point) o;
			return x == p.x && y = p.y;
		}
- Writing code banking on equals being there
	- Because the `Object` class defines `equals`, you can indepentadly write code to compare two objects.

### Announcements

- iclicker test quiz on Thursday
- Quizzes in recitation will be "design based."

## January 31st, 2013 - Lecture

- Dynamic binding happens when at runtime a certain method happens when a call is bound to a subclasses version.
- A lot of times you'll do things with things with `static`. What *is* `static`?
	+ If you make something `static`, you're making it "not object oriented."
	+ `static` is the non-OO portion of Java.
	+ Say, for instance, you need a program that just repeats whatever is typed in?
	+ You don't need an echo object for this – there's no object anywhere here. 
	+ `Math.java`, for instance, is a `static` class, and it is what's called a "utility" class.
- `static` variables
	+ There are two static constant fields in `Math.java` – `E` and `PI`.
	+ A classic example of a `static` non-`constant` variable is a counter that keeps track of how many objects are in existence.
- `static` methods

## February 6th, 2013 - Lecture

- When you make UI, the first thing you should do is draw the mockup, every window, every scheme.
- This way you fine tune the UI before you write code.
- When you have more complex layouts, you need the `JPanel` class to put in your `JFrame`.
- A `JPanel` goes into a top level `JFrame`.
- Generally, you should not allow the user to make mistakes.
- For our project, we will have to make a storyboard.
- You can use Eclipse to make a `JPanel` visually.
- It doesn't do this as well as Xcode. Nowhere near.
- `Color` is a class in `awt`.
- You can make your own colors.
	+ You can set themesee in 
- `setEditable(boolean)` makes a panel read only (to the user).
- `setForeground(Color)` and `setBackground(Color)` set the color of the interface.
- `setFont(Font)` ... sets the font ...
- A text field can have its horitniztonal alignment set with `setHorizontalAlignment()`
- A `GridLayout` creates ... a grid for you to put UI elements in.
- The difference between default and no argument constructors is that the compiler gives you no argument for free.
- Make sure to always to ... `setVisible(boolean)`
- `pack()` will make your `JFrame` as small as possible given your UI elements.
- `protected` makes the scope of a variable visible to every class in the same package and any subclasses.

## February 7th, 2013 - Lecture: GridBagLayout

- Example
	+ Fours buttons are added to a fram, constraints are all default values.
	On enlarging the fram, notice how the buttons *maintain their sizes* and stay centered within the container.
	- `gridx` and `gridy`
		- leftmost colum has `gridx = 0` and topmost row has `gridy= 0`
		- Defult value is `GridBagConstraints.RELATIVE` - component is placed to the right of (if `gridx`) or in the row immediately below,
	+ `gridwidth` and `gridheight`
			* Number of columns and row in the compnents display area.
			* Note: Component may r5dftnot always fill its desplay area.
			* Default value is one.

## February 7th, 2013 - Assignment 1: Song Library GUI Design and Implementation

### Description

Design and implement an application with a graphical user interface to add and display a library of songs. No two songs should have the same name and artist (case insensitive match.) Your application should have a SINGLE FRAME with three interfaces:

- A song list interface, with the ability to select ONE song from the list. The list will only display the names of the songs
- A song detail interface, with name, artist, album, and year, of the song that is selected in the song list area.
- An add/delete/edit interface, for adding new songs, deleting selected song, and editing selected song information:
	- When adding a new song, the song name and artist should be entered at the very least. Year and album are optional.
	- For editing, any of the fields can be changed.

There should be NO other windows in your application. While these three interfaces should be easy to interpret and access, they need not necessarily be three distinct containers. It is completely up to you as to how you want to best design the interface, but you will be responsible for making it clear and complete in functionality. (More below.)

When your program is started, it should show the current list of songs in the library, in the song list area, with the first song selected by default. (The first time the program is run, there should be nothing in the display, of course.)

The data should be persistent across different sessions of your program. You can save the song list in a file in whatever format you like, and then read it into your program when it starts up.

Your application is NOT required to play a song when it is selected.

The application frame should be resizable, and should appropriately resize/not resize the constituent areas, according to what you think would be best for the user experience.

Many of the aspects of design (frames, panels, layouts) and implementation (event handling) you need to do this assignment have been covered in class. However, you may need to add other aspects from Swing/AWT, and you are expected to discover these for yourself. You may find these links useful:

- [How to Use Various Components](http://docs.oracle.com/javase/tutorial/uiswing/components/componentlist.html)
- [A Visual Guide to Layout Managers](http://docs.oracle.com/javase/tutorial/uiswing/layout/visual.html)

### Grading


	GUI Component			Points
	Song list+selection		8
	Details display			7
	Add/Delete/Edit			20
	Persistence				5

(No Javadoc documentation needed, save for the @author tag - see Submission Instructions below.)
For the first three components, the grade will be depend on correctness and compleletness of functionality, as well as effective/appropriate use of Swing/AWT widgets. For the last part (persistence), grading is on correctness, and on ensuring this is transparent to the user, i.e. the user should not have to be concerned with where and how the song list is stored between sessions.

Effective/appropriate means the UI should be clear, the user should know exactly what to expect when events are triggered, the user should know exactly what to do to achieve their objective. If you need to explain to someone how to use the interface, then it's not a good enough interface.

Along these lines, your UI should not use widgets that are an overkill for the task at hand because if a complex widget is used for a simple task, it will confuse the user. (So, for instance, do NOT use a JTable to show song details because the specification does not require you to arrange/rearrange details in any particular order, or be able to sort on any particular aspect of the details.)

Finally, your UI is not required to be aesthetically pleasing (no points for this because it's highly subjective), but you can certainly try to impress us with your creativity (just for the heck of it!) as long as it does not get in the way of functionality.

### Submission Instructions

Call your main class SongLib (If you don't do this we will have to first find which of your classes has the main method so we can run your program. Points will be deducted!)

Make sure you add the Javadoc @author tag with your name to all the classes you implement. No other Javadoc comments are required.

Export your project to a zip file called songlib.zip Make sure you have done this correctly by importing it back as a project into Eclipse (points will be deducted if we get a zip file that is not legit).

Submit your songlib.zip file.

## February 11th, 2013 - Recitation: Problem Set 3 (Tokenizing, GridBagLayout, Interfaces)

1. Write a program to accept a string and extract tokens from it. A token (string) is any sequence of non-whitespace characters, unless it is enclosed in double quotes, in which case everything inside double quotes (including whitespaces if any) is a token.

2. Create a GUI application using a GridBagLayout. There should be 4 buttons (one each for north, south, east, and west). Each button should have a visible amount of spacing between itself and other components. At the center of the application create a label. This label's text should initially read "default." When one of the buttons is pressed, the label's text should read one of north, south, east, or west as appropriate. When the window is resized, the buttons should continue to hug the borders, and the label should continue to be centered.

3. Suppose you built a Java library of sorting algorithms:  insertion sort, quicksort, and heapsort.  You want to sell this library.  How would you package your library so users could use any of these algorithms in their applications, and switch from using one to another (plug-n-play) with the least amount of code rewrite? Come up with the most appropriate design.

4. Examine the following classes, then answer the questions below.

		public class Thing implements Comparable <Thing> {
			int a; 
			Thing() {
         		a = getThingValue(); // assume getThingValue() is properly implemented.
     		}

    	 		public int compareTo(Thing x) {
         		return -1; 
        			// assume this return value is correct for part (a)
        			// implement a proper return value for part (b)
     		}
		}

		public class Contraption extends Thing implements Comparable<Contraption> {

     		int b; 

     		Contraption() {
          		super();
          		b = getContraptionValue(); // assume getContraptionValue() is properly implemented.
     		}

		     public int compareTo(Thing x) {
        			  return 1;
          		// assume this return value is correct for part (a)
          		// implement a proper return value for part (b)
    			 }
		}
	1. As implemented above, these classes contain an error which will prevent them from compiling. Find and describe the error. Note that you should assume getThingValue() and getContraptionValue() are properly implemented. Do not change the compareTo() methods for this part.
	2. Re-implement the two classes so that two instantiations of Contraption can be compared via one of their compareTo methods. You will need to fully implement the two compareTo methods, however you may not change either compareTo methods' signature. Be sure to i) remove the compareTo methods' current return values and ii) correct the error from part (a). Assume that getThingValue() and getContraptionValue() are properly implemented. Use the following ordering rules for implementing the compareTo functions:
		+ Comparing two instantiations of Thing: 
		+ Compare the "a" values. Return -1, 0, or 1 as appropriate for a compareTo function.
		+ Comparing two instantiations of Contraption: 
	A Contraption's "a" value has a higher precedence than its "b" value. First compare the "a" values. If possible, return either -1 or 1. If an ordering cannot be established using only "a" values, compare the "b" values. This function should return -1, 0, or 1 as appropriate for a compareTo function.

	3. Which classes' compareTo method will line 3 of the following code execute? Why?

			Thing myThing = new Thing();
			Contraption myContraption = new Contraption();
			int result = myThing.compareTo(myContraption);
			System.out.println(result);

## February 12th, 2013 - Lecture: Interfaces

### Using interfaces

- Take a stack, for instance

		public class Stack<T> {
			private ArrayList<T> items;
			public Stack() { ... }
			public void push (T t) { ... }
			....
		}
- Look at this alternate code:

		public class LLStack<T> {
			private ArrayList<T> items;
			public Stack() { ... }
			public void llpush (T t) { ... }
			....
		}
		
	+ Had this been production code, and you go from using `Stack` to `LLStack`, the client has to do a lot of work to convert everything from one to the other.

- Solution:

		public interface Stack<T> {
			void push(T t);
			T pop();
			...
		}
		
- And:

		public class ALStack<T> implements Stack<T>
			private ArrayList<T> items;
			public ALStack() {...}
			public void push (T t) { ... }
			public T pop();
			
	- This allows for plug and play.
	
### Interface and Polymorophism

		public class Point {
			int x,y;
			...
			public String toString() {
				return x + " " + y;
			}
		}
		
		public class ColoredPoint extends Point {
			String color;
			...
			public String toString() {
				return x + " " + y + " " + color;
			}
		}
		
		// in some main method
		
		Point[] pts = new Point[n ]
		pts[0] = new Point(2, 3);
		pts[1] = new ColoredPoint(3,4,"red");
		...
		
		for (int i = 0; i < pts.length; i++) {
			System.out.println(pts[i].toString());
		}

## February 14th, 2013 - Project Part 1: Photo Album (Design and Implementation I)

### The Model-View-Controller (MVC) Architecture

For this first part of the project, your team will create the model and
control parts of a **Model-View-Control** architecture for a **Photo
Album** application.

A system using the MVC architecture has three main components:

-   **Model** - The representation and management of the systems data
-   **View** - The user's interface to the system
-   **Control** - The algorithmic logic, decision making and data
    manipulation processes

Breaking up a system into these three components is beneficial for a
number of reasons. The most obvious reason is for modularity. Properly
coded, a system using MVC should be able to change the way any of the
components is implemented without breaking the others. For instance, the
model could store data in flat files. Later, if there is a reason to
move to a database storage scheme, then the model can be reimplemented,
but the view and controller can be left untouched, **if the model had
been implemented to an interface, and the view and controller interacted
with the model solely through this interface**. (Here the word
"interface" is used to refer broadly to one or more interfaces.)

Another motivation for using the MVC architecture is ease of testing. If
the model talks to the control and view only through a known interface,
the invocations of that interface can be scripted to run a set of
diagnostics, isolating any problems with data the tester is seeing
either in or out of the model.

For this first part, you will be writing a "simple" text-based view that
is operated from the command line for the purpose of bug testing the
control and model components. Assuming this first part is done
correctly, the text-based view can be plugged out and a graphical user
interface plugged in without wondering if the weird text that is being
displayed on the screen comes from the model (it doesn't, you tested
that in the first part) or some nuance of object references in the view.

**IMPORTANT**:

In your implementation, the **control** should connect the **view** to
the **model**. The only parts of the **model** that the **view** may
interact with are the ones which get or set data without any
manipulation. (For example, getting the view can directly get the id of
a user from the model, and display it. But things such as sorting a list
of users should be done in the control.)

### Project Structure

-   Name your project `PhotoAlbumXX`, where XX is the two digit group
    number (ie 1 becomes 01).
-   The **model** component should be in its own package
    `cs213.photoAlbum.model`
-   The simple command line **view** client should be in the package
    `cs213.photoAlbum.simpleview` and have a main class `CmdView`
-   The **control** should be in package `cs213.photoAlbum.control`
-   Any utility classes shared by the MVC components can go in the
    package `cs213.photoAlbum.util`
-   Data (users, albums, information about the photos except the actual
    files) should be stored in a folder called `data` directly under the
    `PhotoAlbumXX` folder. (The actual photos can be anywhere in the
    local filesystem.)
-   All documentation (PDFS, HTMLs) should be in a folder called `docs`
    directly under the `PhotoAlbumXX` folder.

NOTE: In Eclipse, create packages with the complete name, such as
`cs213.photoAlbum.model`. DO NOT separate this into a 3-package
hierarchy. It should show up as a single package "folder" in the Eclipse
package explorer view, but when you look at the directory structure in
your computer's filesystem, you will see that it has been automatically
expanded into the hierarchy `cs213 --> photoAlbum --> model`

### Model

The model has four main components: photo, album, user, and a backend.
The photo, album, and user objects are simply data containers.

#### Photo specification

-   A unique (per user) file name.
-   A caption
-   A `java.util.Calendar` instance for the date and time the photo was
    taken/file was created\

    **Note:** When you set a date and time in a `Calendar` instance,
    also make sure you set milliseconds to zero, as in:

             
             cal.set(Calendar.MILLISECOND,0);

    Otherwise your equality checks won't work correctly.

-   List of different tags:

    -   Location of where the photo was taken (unspecified or one)
    -   Names of the people in the photo (zero or more)
    -   Other tags, as you may see fit

    **Note**: A tag is a combination of tag type and tag value, e.g.
    ("location","New Brunswick"), and each tag (type, value pair) for a
    photo is unique. For instance, the people who appear in a photo will
    appear in multiple tags, one tag per person. However, you can't have
    two tags with the same person tag type and same person name value.

-   Functionality to edit the attributes of the photo

#### Album specification

-   A unique (per user) album name
-   Zero or more photos
-   Functionality to add and delete photos to/from albums, and to
    recaption photos\

**Note**: A photo may appear in multiple albums of a user.

#### User specification

-   The user's unique ID (string, used to log in)
-   The user's full name
-   The user's albums, stored efficiently
-   Functionality to add, delete and rename albums

#### Backend specification

The backend refers to functionality that will allow for the storage and
retrieval from the `data` directory, and the photo files pointed to by
file name information in the data directory. (See [Project
structure](#structure)). The backend functionality includes:

-   Read a user (including all constituent user data, see **User
    Specification** above) identified by user ID from storage into
    memory
-   Write a user (including all constituent user data) to storage from
    memory
-   Delete a user, identified by user ID
-   Get a list of existing users, identified by user IDs

#### Model Versions

Different version of the model may be used, depending on whether and at
what time state changes in the user/photo data are written to disk. Here
are two contrasting models:

-   **Session Persistence**: This model does not store anything to disk
    when the program is running, but stores all data when the program
    terminates. Every program run is a session. When a session starts
    up, data from the previous session is read from disk - this is the
    start state. This model version is sufficient for a single-user mode
    where users cannot see each other's albums.
-   **Write Persistence**: This model stores state changes to disk every
    time a command that updates the state is executed, i.e. the state
    change is a "write". For instance, if a user adds a photo, the new
    photo information will be immediately written to disk. That is, at
    any time, the user/photo data on disk would be a copy of the
    corresponding data in memory. (As in the session persistence model,
    when a session starts up, data resulting from the previous session
    is read from disk.) This version is required for a program that runs
    in multi-user mode, where users can see each other's albums (think
    of a web-based shared photo album such as Flickr).
-   **Your Model Version Implementation**

    For your project, you will need to implement **session persistence**
    only.

    You **are required** to use the `java.io.Serializable` interface,
    and the `java.io.ObjectOutputStream`/`java.io.ObjectInputStream`
    classes to store and retrieve data.

    Although you are only required to implement one model (flat file,
    session persistence), part of the credit will be based on how easy
    it would be to replace session persistence with a different model
    version. Use interfaces to make swapping different model
    implementations easy (plug-n-play, interface polymorphism), with
    minimal change to the other parts (view/control) of the program. See
    the [API Driven Coding](#api) section for more information.


### View


For this first stage of the project, you will implement a simple
text-based view with two modes of input - a command line mode, and an
interactive mode.

#### Command Line Mode 

-   To list existing users: \
    `java cs213.photoAlbum.simpleview.CmdView listusers` \
    Output: \
    `<userId1>` \
    `<userId2>` \
    `...` \
    Or: \
    `no users exist`

-   To add a new user: \
    `java cs213.photoAlbum.simpleview.CmdView adduser <user id> "<user name>"`
    \
    Output: \
    `created user <user id> with name <user name>` \
    Or: \
    `user <user id> already exists with name <user name>`

-   To delete a user: \
    `java cs213.photoAlbum.simpleview.CmdView deleteuser <user id>` \
    Output: \
    `deleted user <user id>` \
    Or: \
    `user <user id> does not exist `

-   To login as an existing user: \
    `java cs213.photoAlbum.simpleview.CmdView login <user id>` \
    (*view now goes into interactive mode*) \
    Or: \
    `user <user id> does not exist `

**Note**: You can run these from inside Eclipse by changing the program
arguments every time (See the Eclipse page for how to set program
arguments). However, this can get cumbersome. Instead, you can work in a
command window/shell, by going to the bin directory inside the project,
and running the **java** command from there.

**Interactive Mode**

-   To create an album: \
     `createAlbum "<name>"` \
    Output: \
    `created album for user <user id>:` \
    `<name>` \
    Or: \
    `album exists for user <user id>:` \
    `<name>`
-   To delete an album: \
     `deleteAlbum "<name>"` \
    Output: \
    `deleted album from user <user id>:` \
    `<name>` \
    Or: \
    `album does not exist for user <user id>:` \
    `<name>`
-   To list all albums, with their number of photos and the range of
    dates that the photos were taken: \
     `listAlbums` \
    Output: \
    `Albums for user <user id>: ` \
    `<name> number of photos: <numberOfPhotos>,  <start date> - <end date>`
    \
    `... ` \
    Or: \
    `No albums exist for user <user id>`
-   To list the photos in an album: \
    `listPhotos "<name>"` \
    Output: \
    `Photos for album <name>:` \
    `<fileName> - <date>` \
    `...`
-   To add a photo to an album: \
    `addPhoto "<fileName>" "<caption>" "<albumName>"` \
    Output: \
    `Added photo <fileName>:` \
    `<caption> - Album: <albumName>` \
    Or: \
    `Photo <fileName> already exists in album <albumName>` \
    Or: \
    `File <fileName> does not exist`

    **Notes**:

    -   The date and time for the photo should be obtained from the
        properties of the photo file.
    -   The caption is a property of the photo, not the album. This
        means if you add a photo to more than one album, you specify the
        caption when adding to the first album. Then, when adding to
        subsequent albums, you specify an empty string for the caption,
        meaning that the caption is retained from the first add. The
        output message for the subsequent adds however should have the
        original caption, so it's clear that the caption has been
        retained.

-   To move a photo from one album to another: \
    `movePhoto "<fileName>" "<oldAlbumName>" "<newAlbumName>"` \
    Output: \
    `Moved photo <fileName>:` \
    `<fileName> - From album <oldAlbumName> to album <newAlbumName>` \
    Or: \
    `Photo <fileName> does not exist in <oldAlbumName>`

    **Note**: If the photo already exists in the new album, the command
    should return silently without doing anything.

-   To remove a photo from an album: \
    `removePhoto "<fileName>" "<albumName>"` \
    Output: \
    `Removed photo:` \
    `<fileName> - From album <albumName>` \
    Or: \
    `Photo <fileName> is not in album <albumName>`
-   To add a tag to a photo: \
    `addTag "&ltfileName>" <tagType>:"<tagValue>"` \
    Output: \
    `Added tag:` \
    `<fileName> <tagType>:<tagValue>` \
    Or: \
    `Tag already exists for <fileName> <tagType>:<tagValue>`
-   To delete a tag from a photo: \
    `deleteTag "&ltfileName>" <tagType>:"<tagValue>"` \
    Output: \
    `Deleted tag:` \
    `<fileName> <tagType>:<tagValue>` \
    Or: \
    `Tag does not exist for <fileName> <tagType>:<tagValue>`
-   To list photo info: \
    `listPhotoInfo "&ltfileName>"` \
    Output: \
    `Photo file name: <fileName>` \
    `Album: <albumName>[,<albumName>]...` \
    `Date: <date>` \
    `Caption: <caption>` \
    `Tags:` \
    `<tagType>:<tagValue>` \
    `...` \
    (grouped by tag type, in the order location first, then people, and
    then others, sorted by tag value within each type) \
    Or: \
    `Photo <fileName> does not exist`
-   To retrieve all photos taken within a given range of dates, in
    chronological order: \
    `getPhotosByDate <start date> <end date>` \
    Output: \
    `Photos for user <user id> in range <start date> to <end date>:` \
    `<caption> - Album:   <albumName>[,<albumName>]... - Date: <date>` \
    `...`
-   To retrieve all photos that have all the given tags, in
    chronological order. Tags can be specified with or without their
    types: \
    `getPhotosByTag [<tagType>:]"<tagValue>" [,[<tagType>:]"<tagValue>"]...`
    \
    Output: \
    `Photos for user <user id> with tags <search string>:` \
    `<caption> - Album: <albumName>[,<albumName>]... - Date: <date>` \
    `...`
-   To end the interactive mode (and the session): \
     `logout` \
    Output: none

Any errors (illegal parameters, invalid dates) should be handled
gracefully. No stack traces should be printed out (the user shouldn't
have to know what an exception is). Instead, a one sentence description
of what exactly went wrong should be printed. The format is as follows:
\
`Error: <description of error>`

**Important:**

-   All names (such as user names, file names, etc.) in the commands are
    contained within quotes. The reason is you can have spaces in any of
    these, but the whole thing needs to be treated as a single quantity
    (token). So if a picture location is Busch Campus, say, it should
    not be read as two tokens, which necessitates typing in "Busch
    Campus", within double quotes.

-   Quantities in angle brackets stand for corresponding *values*. That
    is, anything contained in an angle bracket should be replaced with
    an actual value. The angle brackets themselves should not be typed.
-   Quantities in square brackets are optional.
-   `...` stands for repetition.

-   If you use a `java.io.BufferedReader` or `java.util.Scanner` to read
    input from `System.in`, be sure you do not instantiate a new one for
    every single input. This causes problems when the graders copy a
    larger set of commands into your program at once. Instantiate the
    reader/scanner *once* and re-use it for each read.

-   Stick to the input and output guidelines exactly. Any deviation from
    the specified formats will be penalized. **This means no ascii art
    or clever intros at the beginning!** (The graders do not care about
    what "version" you think the code is at, nor do they appreciate the
    carefully drawn box of roses surrounding said information...)

### Control

The control (or controller) does all manipulation/processing of data
within the program including the creation (but not storage) and deletion
of new objects, sorting/filtering data on various dimensions, and
checking data validity that goes beyond syntactic correctness of input
commands. (For instance, checking dates for validity.)

As mentioned earlier, the view can directly interact with the model only
for direct access of data that is not processed in any way. Note that
the user specification in the model includes storing albums in efficient
data structures.

The control can know about a single user at a time. Then all operations
on the control apply to that user.

The control should not be tied to any one particular model
implementation, so it should interact with the model interface(s).

### API Driven Coding

API (Application Programming Interface) refers to explicit and implicit
interfaces that serve as "contracts", enabling different parts of an
application to be built independenly. For instance, if the two of you in
a group know what all the `interface`s are (explicit interfaces), as
well as what the public/package/protected members of all classes are
(implicit interfaces), you can then divide up the work and fill in the
code for all the classes you are responsible for.

For each of the main components for this first part--model and
control--you will need to provide an API, which should be in the form of
a set of **documented interfaces and public/package/protected class
fields, constructors, and methods**. (Private fields, constructors,
inner classes, and methods need not be documented for sharing, but you
will document them all by the time you finish coding the entire part 1.)

Documentation should be done through `javadoc` and UML diagrams. (Note:
not all classes you build will necessarily implement an interface.)

The UML diagrams will most likely not be complex. It should include all
classes that the group writes in the model and control, but none from
the view and none from the standard library (the graders know what a
`String` is, no need to diagram it).

For javadoc, in addition to comments about the nature of the code, the
javadoc for each class and interface must name the primary author for
that class (use the `@author` field), and where applicable the javadoc
for a particular method should also name its author.

The interfaces should be as *general* as possible. Ideally, one should
be able to swap out your implementation of these interfaces for another
with minimal code rewriting and no errors (assuming the other
implementation is bug-free).

An example of making a generic interface comes from `java.util.List`.
You saw in lecture how interface polymorphism is useful for swapping two
different implementations of the `List` interface, the `LinkedList` and
`ArrayList` classes, depending on need. Similarly, if you design the
model and control interfaces well, it should be possible to swap
different model or control implementations without changing any code
that uses these interfaces.


### Development Instructions

#### Development/Testing

Development may take place anywhere, as long as your code is compilable
with Java Version 6. You can develop with a higher version installation,
but make sure your code compiles and runs under Java 6. It should, if
you are not using features that are specific to the higher versions. If
the graders are unable to compile/run your program on their machine,
running Java 6, you will lose credit.

Also, you may only use the standard Java API. No external libraries!

#### Mercurial

Each group will access its Mercurial repository on BitBucket, which you
will set up according to the instructions given in the
Mercurial/Bitbucket walkthrough page in Sakai. The repository name for
your group will be `photoAlbumXX`, where `XX` is your two digit group
number.

### Submission

#### Friday, Feb 20, by 11 PM

-   HTML documentation (generated by javadocs) of all explicit and
    implicit interfaces as described in the [API Driven Coding](#api)
    section. This should be in the `docs` directory as described in the
    [Project Structure](#structure) section, committed to your Mercurial
    repository in BitBucket.

    Important: All interfaces and classes should have authorship, so
    that it is clear as to who will be developing what parts of the
    code.

Submitting this will significantly help you (a) plan ahead and build the
application in a professional manner, working independently for the most
part, and synchronizing when you need to build the "glue" between parts,
(b) protect against trouble if one of you complains because the other
does too much work (takes charge and doesn't work together), or too
little work.

If you are having trouble making this submission, it means you are not
able to work together as a team, and should contact Prof. Venugopal to
get the issue resolved. After this point, you are assumed to be working
well together, and complaints about the partnership will only be
entertained if one partner has dropped the class.

#### Fri, Mar 8, by 11 PM

-   Complete code, UML diagram (PDF ONLY), updated javadoc generated
    HTML (if you have updated the javadocs after the February 22
    submission), sample user data in the `data` directory, all committed
    to your Mercurial repository in BitBucket.

Any changes made to the repository after the deadline will not be graded
- the grader will pull the project in its state at the deadline, not the
most recent version.

Be sure that there are no hard coded file paths. The grader should not
have to do anything other than check out your project and run an
appropriate (and generic except for your group numer) test script.
Anything else will result in a deduction from the score.

### Grading

The project will be graded on the following criteria:

**Good design:** How well the project conforms to the MVC pattern, how
well your submission of February 22 anticipated the completed
implementation, and how well your UML diagram represents the code. \
\
**Implementation**: Everyting described in the the **Model**, **View**,
and **Control** specifications. \
\
**Documentation:** Appropriately detailed javadocs \
\
**Specification Adherence:** How well your project conforms to the
guidelines in this document

### Sample Run


Here is a sample test run. Your program should work on this test (and we
will check!), but also others. You might find it convenient to make your
own test runs. The following test run assumes the existence of a user
"testuser".

Note: You can run the program in Eclipse, but you will need to keep
changing the program arguments frequently for the command line mode,
which can get annoying. It may be easier to position youseelf in the
eclipse workspace project `bin` directory, and run the program from
there.

If you get a `ClassNotFoundError` from this, try adding `-cp .` to the
command line, right after `java` as in: \
 `java -cp . <stuff> `

The following sample works with this assumption. (And when we test your
program, we will run java outside Eclipse.)

    java cs213.photoAlbum.simpleview.CmdView login testuser 

    createAlbum "Fall colors"

    createAlbum "Colorado Springs"

    addPhoto "DSC_001.jpg" "DSC_001" "Fall colors"

    addPhoto "DSC_005.jpg" "DSC_005" "Fall colors"

    addPhoto "DSC_007.jpg" "DSC_007" "Colorado Springs"

    listAlbums

    movePhoto "DSC_001.jpg" "Colorado Springs"

    addTag "DSC_001.jpg" person:"Alex Buschman"

    addTag "DSC_001.jpg" location:"Colorado"

    addTag "DSC_005.jpg" person:"Alex Buschman"

    listPhotos "Fall colors"

    searchPhotosByTags person:"Alex Buschman"

    logout

This run should produce the following output:

    created album for user testuser: 
    Fall colors
    created album for user testuser: 
    Colorado Springs

    Added photo DSC_001.JPG: 
    DSC_001 - Album: Fall Colors

    Added photo DSC_005.JPG: 
    DSC_005 - Album: Fall Colors

    Added photo DSC_007.JPG: 
    DSC_007 - Album: Colorado Springs

    Albums for user testuser: 
    Colorado Springs number of photos: 1, 02/12/2012-09:23:00 - 02/12/2012-09:23:00
    Fall Colors number of photos: 2, 02/12/2012-10:15:00 - 02/12/2012-15:42:00

    Moved photo DSC_001.JPG: 
    DSC_001.JPG - From album Fall Colors to album Colorado Springs

    Added tag:
    DSC_001.jpg person:"Alex Buschman"

    Added tag:
    DSC_001.jpg location:"Colorado"

    Added tag:
    DSC_005.jpg person:"Alex Buschman"

    Photos for album Fall Colors: 
    DSC_005.JPG - 02/12/2012-15:42:00

    Photos for user testuser containing person:Alex Buschman
    DSC_001 - Album: Colorado Springs - Date: 02/12/2012-09:23:00
    DSC_005 - Album: Fall Colors - Date: 02/12/2012-15:42:00


## February 18th, 2013 - Recitation 4: Project Q&A, Debugging in Eclipse, Polymorphism

1.  Project Q&A

2.  Debugging in Eclipse

    Download the (buggy) code in [HeapSort.java](Heapsort.java) and
    import it into Eclipse. Use the debugger to track down the bug(s)
    and fix the code.

3.  There is an application that defines a `Person` class and a
    `Student` class. The `Student` class is defined as a subclass of
    `Person`. Every person has a home address, while every student has a
    school address as well.

    Consider printing addresses of all people in the application,
    assuming there is a single array list that stores all `Person` and
    `Student` objects. How would the address that is printed for
    students depend on the way the `Student` class address methods are
    designed/implemented? What alternatives in design can you think of,
    and what are the pros and cons of these alternatives in printing the
    addresses?

4.  In class we saw how you could write code to print a collection of
    mixed `Point` and `ColoredPoint` objects:

           Point[] pts = new Point[n];
           pts[0] = new Point(2,3);
           pts[1] = new ColoredPoint(3,4,"black");
           ...
           for (int i=0; i < pts.length; i++) {
              System.out.println(pts[i]);
           }

    1.  Where is the *polymorphic* behavior in this code?
    2.  Give an example of code using the `pts` array that is NOT
        polymorphic, and explain why it is not polymorphic.

5.  Suppose classes `A` and `B` are in package `ab`, and classes `C` and
    `D` are in package `cd`. Furthermore, both `C` and `B` extend `A`,
    and `D` extends `B`. Assume all classes are declared to be `public`.

    1.  Are `protected` members of `A` accessible in `C`?  If yes,
        explain how. If not, explain why.
    2.  Are `protected` members of `A` accessible in `D`?  If yes, how?
        If not, why?
    3.  Answer the same question as in 1. replacing `A` with `B`
    4.  Answer the same question as in 2. replacing `A` with `B`

6.  You are given the followig `Employee` class:

        public class Employee {
          private String name;
          private double salary;
          
          public Employee(String aName) {
             name = aName; 
          }
          
          public void setSalary(double aSalary) {
             salary = aSalary; 
          }
          
          public String getName() {
             return name; 
          }
          
          public double getSalary() {
             return salary; 
          }
        }

    Write subclasses `HourlyEmployee` and `SalariedEmployee` of the
    `Employee` class.  Provide the constructors listed below:

        HourlyEmployee(String aName, double anHourlySalary)

        SalariedEmployee(String aName, double anAnnualSalary)

    Add, in the appropriate place(s), the method:

        double getWeeklySalary()

    (You can modify the `Employee` class if needed.)

    Assume that hourly employees work 40 hours per week, and salaried
    employees are paid 1/52 of their annual salary every week.

7.  (Adapted from an example in Interface Oriented Design by Ken Pugh,
    sec. 4.2)
    Suppose you want to create a printing subsystem for several
    different printers, each with different capabilities/features (e.g.
    color printing, high-resolution, duplex, multiple trays, etc.).  How
    could you place the different capabilities into an interface? 
    Should you use a single interface or multiple interfaces (e.g.
    ColorPrinter, DuplexPrinter, MultiTrayPrinter)?  Describe the
    advantages and disadvantages of both approaches.



