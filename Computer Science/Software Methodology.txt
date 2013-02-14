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
		
		

