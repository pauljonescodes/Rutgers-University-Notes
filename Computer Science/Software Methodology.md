Software Methodology <small>with Professor Sesh Venugopal</small>
=================================================================

Description
-----------

This course teaches essential principles, techniques, tools, and methods
used to develop large software programs in Java. These include
object-oriented programming and design, Unified Modeling Language (UML),
testing and debugging, using and documenting APIs, asynchronous
(event-driven) programming in a Graphical Use Interface (GUI) framework,
code maintenance and version management using CVS, software development
using Eclipse, introduction to building software on mobile platforms,
introduction to multithreading, network programming, and object
persistence.

-   Topics:
    -   Inheritance, interfaces, abstract classes, polymorphism
    -   Unified Modeling Language (UML)
    -   Essential design patterns, including Singleton,
        Model-View-Controller (MVC), Template Method, State
    -   Black-box unit testing, debugging, developing large applications
        in Eclipse
    -   Object persistence, serialization
    -   Code management using CVS
    -   Designing and implementing GUIs using Java Swing and AWT
    -   Frames, dialogs, panels, widgets, tables, layouts, colors,
        fonts, drawing, painting
    -   The Swing MVC architecture and working with data models
    -   Event handling
    -   Introduction to software development on mobile platforms
    -   Introduction to multithreading
    -   Introduction to network programming

Syllabus
--------

-   Topics
    1.  Overview of software methodology. Object-oriented programming.
        Iterative development. Testing. Documentation. Source code
        management with Mercurial.
    2.  Object-Oriented Design with Java. Class design, interfaces,
        inheritance, abstract classes, polymorphism.
    3.  UML class diagrams to represent object-oriented design. Classes,
        generalizations, associations, dependencies.
    4.  Event-driven Graphical User Interface (GUI) programming. Event
        registration, listeners, handling events. Java Swing and AWT.
        Components and containers. Frames, dialogs, panels, layouts,
        colors, fonts, drawing, painting.
    5.  Model-View-Controller (MVC) design pattern. The Swing MVC
        architecture and working with data models.
    6.  State-based programming. State design pattern.
    7.  Iterative development - feature extension, code reuse,
        versioning, backward compatibility, object serialization.
    8.  Block-box unit testing. Boundary values. Equivalence Classes.
        Debugging in Eclipse.
    9.  Multithreading and synchronization on shared resources.
    10. Developing Android apps in Eclipse. Device emulators. Structure
        of Android apps. Java source code, resources, manifest file, xml
        layout, density independent pixels.
    11. App lifecycle, activities, passing information between
        activities. Layouts, views, widgets, menus, context menus,
        dialogs, inflating views from xml.
    12. Implementing search with search bar. I/O. Icons and drawables.
    13. Packaging an app for publishing to the Android Market.
    14. Introduction to network programming. Java networking API.
        Client-server programming with TCP/IP sockets and server
        sockets.

-   Grading
    -   Recitation attendance: 50 (5%)
    -   Homework assignments: 150 (15%)
    -   Object-oriented GUI project: 300 (30%)
    -   Android project: 200 (20%)
    -   Quizzes: 100 (10%)
    -   Final exam: 200 (20%)

January 22nd, 2012 - Lecture
----------------------------

-   Many things that you use when building a Java GUI, you'll be using
    widgets from Swing API.
-   With JButtons, the simplest way to have something in the button is
    tompass text to the constructor.
-   With JFrames, you want to display content in a certain arragement,
    using something called a layout manager.
-   With different LayoutManagers, you get different arrangments.
-   Other LayoutManagers include BorderLayout, GridLayout, ...
-   For any frame and any window, you can set a size.
-   Alyways set your frame to being visible.
-   For every button or widget that sets off an action, you're going to
    need an event listener.
-   Before Swing, there was AWT. And if you thought Swing was bad, well,
    AWT was worse.
-   ActionListeners are interfaces - a la Comparable, Iterable, etc ...
-   LayoutManagers can handle resizing of windows and other unexpected
    happenings.
-   If you set the location relative to `null`, then you get a centered
    window.

January 24th, 2013 - Lecture
----------------------------

-   `ActionListener` is an interface - you need to define a class.
-   In the package `jwt.java.event`, `ActionListener` is a subclass of
    the subclass of all interfaces.
-   You will localize interface definitions if you will never need the
    code again, generalize it otherwise.
-   We defined another class called `ButtonListener` which is in the
    same source file as `FC.java`.
-   You can have multiple classes in the same source, but only one of
    them can be public.
-   If you define a class that implements an interface after an
    instantion, it is called an "anonymous class."
-   Whenever you add a listener, it sets in motion a mechanism within
    Java to handle the action.
-   With `ActionListener`, all the information about the widget that the
    action was performed on is included.
    -   For example, you can get the text from a text button.

-   If you add a class to listen to an action, it must implement
    `ActionPerformed(ActionEvent e)`.
-   If you have multiple classes defined in the same source code, and
    you want to import one of them, you'll need to
    `import [filename].[classname]`.
-   When you program in static, you working outside of the object
    oriented framework.
-   You are only limited to one public class when the classes are
    defined at the same level.
-   Java is meant to be platform independant.
-   An `Object` reference does not "know" what type of object it is.

January 28th, 2013 - Recitation 1: GUI, Javadoc, Inheritence
------------------------------------------------------------

1.  Write a program that creates a frame with two buttons on it: OK and
    Quit. When OK is clicked, nothing will happen. When Quit is clicked,
    the application will exit. The application window (frame) should be
    launched in the center of the screen, and should NOT be closed when
    the user clicks on the 'x' button in the title bar. (In other words,
    the only way to close the window is to click on the 'Quit' button.)

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

2.  Redesign the Fahrenheit-Celsius GUI we did in the first lecture to
    do away with the buttons to convert between F and C. Instead, when
    the user types something in one of the text fields, the converted
    value shows up immediately in the other. So your GUI looks like
    this:

                Fahrenheit       Celsius
                ----------     ----------
               |          |   |          |
                ----------     ----------

    Also, give the frame a title (that appears in the title bar) and
    make the text right-aligned in both text fields (digits are
    displayed right to left). Read the documentation for JTextField in
    the Java API to see how to right-align text. You can register an
    action listener directly on a text field to receive an event when
    the user hits enter after entering text in the text field.

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

    -   This problem requires only labels and text fields.
    -   Think of this as a "project description", a very simple one.
    -   Give the frame a title.

3.  Documenting with Javadoc
    -   Make a comment which begins with two stars
    -   Then hit "generate javadoc" in Eclipse to create a generic
        website based on that information.
    -   Can include fields such as `@see`, `@author`, `@version`, and
        `@since`

4.  What is the output of this code? Why?

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

    The method call matches the argument type (`Child`) with the closest
    matching parameter type (`Parent`). So the method `Foo.bar(Parent)`
    is called.

January 29th, 2013 - Lecture
----------------------------

-   It's one thing to write code that hacks through a GUI, it's wholly
    another to write an extensible, usuable GUI.
-   How can we write code that is easily extensible?
-   Inheritence simply means that the code you've written in the parent
    need not be rewritten.
-   You have to initialize the superclass portion first, and then then
    the subclass portion afterwards.
-   The constructors are not inherited.
-   The name of the constructor is taken from the name of the class, so
    they're not inherited.
-   Static vs. dynamic type
    -   There is a difference between compile time and run time types.

                Point p1 = new Point(2,3);

        -   Compile time type: `Point p1`
        -   Run time type: `2,3`

                Point p2 = new ColoredPoint(3,4,"red");

        -   Compile time type: `Point p2`
        -   Run time type: `ColoredPoint 3,4,"red"`

    -   Dynamic binding: at runtime, the actual method being called is
        bound to that call.
    -   You can't initialize a child as a parent, and every parent
    -   If an object is statically declared to be of a certain type, it
        can only calls those methods in that type.
    -   However, at runtime, it can call whatever it is dynamically
        assigned to be.
    -   Typecasting tells the compiler to ignore the declared type and
        use this "typecast" type instead. Example:

            (ColoredPoint)p2.getColor();

    -   Typecasting usually is indicative of not following design intent
        or having poor design.

-   You cannot access private variables through the object.
-   A subclass inherits the subclasses private fields.  
-   It's a beginner's mistake to write an `equals` method like this:

        public boolean equals (Point p) {
            return x == p.x && y = p.y;
        }

-   Here's an instance where typecasting is fine, and a good `equals`
    method:

        public boolean equals (Object o) {
            if (o == null || !(o instanceof Point))
                return null;
            Point p = (Point) o;
            return x == p.x && y = p.y;
        }

-   Writing code banking on equals being there
    -   Because the `Object` class defines `equals`, you can
        indepentadly write code to compare two objects.

### Announcements

-   iclicker test quiz on Thursday
-   Quizzes in recitation will be "design based."

January 31st, 2013 - Lecture
----------------------------

-   Dynamic binding happens when at runtime a certain method happens
    when a call is bound to a subclasses version.
-   A lot of times you'll do things with things with `static`. What *is*
    `static`?
    -   If you make something `static`, you're making it "not object
        oriented."
    -   `static` is the non-OO portion of Java.
    -   Say, for instance, you need a program that just repeats whatever
        is typed in?
    -   You don't need an echo object for this – there's no object
        anywhere here.
    -   `Math.java`, for instance, is a `static` class, and it is what's
        called a "utility" class.

-   `static` variables
    -   There are two static constant fields in `Math.java` – `E` and
        `PI`.
    -   A classic example of a `static` non-`constant` variable is a
        counter that keeps track of how many objects are in existence.

-   `static` methods

February 4th, 2013 - Recitation 2: Inheritance, Interfaces
----------------------------------------------------------

1.  Consider the following class definition:

        public class A {
           public A () {}
           public A (int a, int b) {}
        }

        public class B extends A {
             public B (int r) {}
             public B (int r, int w) { 
                super (r, w);
             }
        }

    Which of the following are legitimate calls to construct instances
    of the B class?
    1.  `B c = new B();`
        -   Invalid - B does not have a no-arg constructor

    2.  `A s = new B(1);`
        -   Valid

    3.  `B c = new B(1, 9);`
        -   Valid

    4.  `A t = new B(1, 9, 4);`
        -   No 3-argument constructor defined

    5.  `B t = (new B(1)).new B(1);`
        -   gibberish

    6.  `B b = new A(1, 2);`
        -   b is of static type B, and cannot refer to object of dynamic
            type A since A is not a subclass of B

2.  In this exercise we will try to see how static and final methods
    work with inheritance.  Consider the two classes defined below,
    `Parent` and `Child`:

        public class Parent {
          /*
           public static final void printClassName() {
              System.out.println("I am in class Parent, static invocation.");
           }
          */

           public final void printName() {
              System.out.println("I am in class Parent, dynamic invocation.");
           }
        }

        public class Child extends Parent {
          /*
           public static void printClassName() {
              System.out.println("I am in class Child, static invocation.");
           }
          */

           public void printName() {
              System.out.println("I am in class Child, dynamic invocation.");
           }
        }

    1.  Compile both the classes.  What do you see?
        -   Compiling the classes results in the Java compiler printing
            the following error message:

                1. ERROR in Child.java (at line 10)
                public void printName()
                            ^^^^^^^^^^^
                Cannot override the final method from Parent

    2.  Now comment out the `printName()` method from the child class
        and uncomment the `printClassName()` method in both classes. 
        Compile both classes.  What do you see?  Is it different from
        part (A)?  Why?
        -   Compiling the classes results in the Java compiler printing
            the following error message:

                ERROR in Child.java (at line 3)
                public static void printClassName()
                                   ^^^^^^^^^^^^^^^^
                Cannot override the final method from Parent

            It is different from part (A), but in essence it is the same
            error—trying to override a `final` method in a subclass.

    3.  Uncomment the `Child.printName()` method and remove the `final`
        modifier from `Parent.printName()` and
        `Parent.printClassName()`.  Recompile both classes.
        -   It compiles successfully.

    4.  Compile and run the following class:

            class App {
              public static void main(String[] args) {
                 Parent p = new Child();
                 p.printName();      // WHAT IS PRINTED?
                 p.printClassName(); // WHAT IS PRINTED? 
              }
            }

        Explain the difference in *which* methods are invoked in these
        two method calls.
        -   The `App.java` program compiles, but the compiler issues a
            warning because `printClassName()` should be invoked on the
            class, not on an instance.  The `printName()` call invokes
            the `Child` class's implementation because `p` refers to an
            instance of `Child`.  The `printClassName()` call invokes
            the `Parent` class's implementation because `p` is a
            reference of type `Parent`

3.  Suppose you design a class, `Set`, whose members behave like finite,
    unordered mathematical sets of integers, and can support the
    operations of membership query, union of two sets, intersection of
    two sets, and difference of two sets. Consider the intersection
    operation.  There are at least two ways of declaring such an
    operation in the class `Set`:

        public Set intersect(Set otherSet)

    or

        public static Set intersect(Set firstSet, Set secondSet)

    Give one pro and one con for the static version.
    -   The static version of the method is semantically closer to the
        mathematical idea of set operations. The static approach makes
        it clear to programmers that the intersect method is a symmetric
        operation. The drawback of a static definition is that it cannot
        be overridden by subclasses if we wanted to extend the Set class
        and apply polymorphism.

4.  You know of the `java.lang.Comparable<T>` interface used for
    comparing objects of a class. The `java.util` package has an
    interface, `Comparator<T>` that may also be used to compare objects.
    What is the difference between these two interfaces, and how may
    this difference be usefully employed in applications?

    Here's an example of a simplified user-defined type:

        public class Customer {
          private String firstName;
          private String middleName;
          private String lastName;

          // setter & getter methods..
        }

    In the above class, the most commonly *natural ordering* would be by
    `lastName`. This can easily be implemented using the `Comparable`
    interface, i.e.

        public class Customer implements Comparable {
          // as shown previously..

          public int compareTo (Object o) {
            if (o == null || !(o instanceof Customer)) {
              throw new IllegalArgumentException ("...");
            }
            Customer c = (Customer) o;
            String cLastName = c.getLastName();

            if (lastName == null && cLastName == null) return 0;
            // assuming you want null values shown last
            if (lastName != null && cLastName == null) return -1;
            if (lastName == null && cLastName != null) return 1;
            return lastName.compareTo (cLastName);
          }
        }

    Sorting a `List` of `Customer` objects would be as simple as:

          Collections.sort (customerList);

    But, if we want to use a different ordering, e.g. order by the first
    name, then we cannot use the natural ordering as defined within the
    `Customer` class. Instead, we have to define an alternative
    ordering, in the form of a `Comparator` class.

        public class CustomerFirstNameComparator
        implements Comparator {
          // use singleton whenever possible..

          public int compare (Object o1, Object o2) {
            if (o1 == null && o2 == null) return 0;
            // assuming you want null values shown last
            if (o1 != null && o2 == null) return -1;
            if (o1 == null && o2 != null) return 1;
            if (!(o1 instanceof Customer) ||
                !(o2 instanceof Customer)) {
              throw new IllegalArgumentException ("...");
            }

            Customer c1 = (Customer) o1;
            Customer c2 = (Customer) o2;
            String firstName1 = c1.getFirstName();
            String firstName2 = c2.getFirstName();

            if (firstName1 == null && firstName2 == null) return 0;
            // assuming you want null values shown last
            if (firstName1 != null && firstName2 == null) return -1;
            if (firstName1 == null && firstName2 != null) return 1;
            return firstName1.compareTo (firstName2);
          }
        }

    Sorting a `List` of `Customer` objects by their first name, would
    be:

          // assuming you implement singleton..
          Comparator comparator =
            CustomerFirstNameComparator.getInstance();

          Collections.sort (customerList, comparator);

5.  Suppose we need to have the `Point` and `ColoredPoint` classes
    provide functionality to parse text representations of points and
    colored points (as would be returned by the `toString` method), and
    return `Point` and `ColoredPoint` objects, respectively.
    1.  Show how you would implement this functionality. In `Point`
        class:

               public static Point parsePoint(String pointStr) {
                  String[] tokens = pointStr.split(",");
                  if (tokens.length != 2) {
                     throw new IllegalArgumentException();
                  }
                  try {
                     int x = Integer.parseInt(tokens[0]);
                     int y = Integer.parseInt(tokens[1]);
                     return new Point(x,y);
                  } catch (Exception e) {
                     throw new IllegalArgumentException();
                  }
               }

    In `ColoredPoint` class:

           public static ColoredPoint parsePoint(String pointStr) {
              String[] tokens = pointStr.split(",");
              if (tokens.length != 3) {
                 throw new IllegalArgumentException();
              }
              try {
                 int x = Integer.parseInt(tokens[0]);
                 int y = Integer.parseInt(tokens[1]);
                 return new ColoredPoint(x,y,tokens[2]);
              } catch (Exception e) {
                 throw new IllegalArgumentException();
              }
           }

    1.  How much of the `Point` implementation of this functionality is
        reused in `ColoredPoint`? (Reuse meaning using code from `Point`
        by calling on it in `ColoredPoint`.) If yes, indicate which
        part, else explain why not.
        -   No code is reused. The only way to reuse code in
            `ColoredPoint.parsePoint` would be with a call to
            `Point.parsePoint`. However, the latter returns a `Point`
            object, which would not fit in the former's implementation
            because it has no use for a `Point` object. (The idea of
            reuse arises because parsing a colored point equals parsing
            a point, plus parsing the color part.)

    2.  Does your implementation give rise to dynamic binding of the
        parsing functionality? (Recall that dynamic binding means the
        subclass version of a method is "bound" to the call made via an
        object reference that is statically typed to the superclass.)
        -   No, there is no dynamic binding since the methods involved
            are both `static`. So, binding is done purely on the
            static/compile-time type of the reference variable, without
            regard to what object it is pointing to. This means if you
            have:

                Point ptest = new ColoredPoint(3,4,"orange");

        then a call such as `ptest.parsePoint(...)` would invoke the
        `Point` class' `parsePoint` method, not the `ColoredPoint`'s.

6.  Here's the `Widget` class that was used in lecture last Thursday:

        public class Widget {
         protected float mass;  // not visible to clients, but inherited by subclass

         private static float MAX_MASS = 20;

         public static final float G = 9.81f;    

         public Widget(float mass) {
            if (mass > MAX_MASS) {
               throw new IllegalArgumentException();
            }
            this.mass = mass;
         }

         public static float getMaxMass() {
            return MAX_MASS;
         }

         public float getWeight() {
            return mass*G;
         }
        }

    Now suppose there is a certain set of widgets that are "heavy", so
    their maximum mass is 40 instead of the usual 20. Write a class
    called `HeavyWidget`, as a subclass of `Widget`. Do you encounter
    any implementation issues when you do this? Can you get around these
    issues? If so, show how. If not, explain why.

    -   Here's the try to implement `HeavyWeight`:

            public class HeavyWidget extends Widget {

               private static float MAX_MASS = 40;

               public HeavyWidget(float mass) {
                   super(mass);
                   if (mass > MAX_MASS) {
                      throw new IllegalArgumentException();
                   }
                   this.mass = mass;
               }
               ...

        The problem is the call `super(mass)` in the constructor. This
        call needs to be made because the first statement in a subclass
        constructor must be a call to a superclass constructor. Since
        there is only one constructor in the superclass `Widget`, which
        accepts a float parameter, we have no choice but to write in the
        `super(mass)` call. However, the `Widget` constructor would
        throw an exception if the mass exceeds 20, even though
        `HeavyWeight` allows mass to be as much as 40. So this is an
        issue. We can try to get around the issue by putting in a
        try-catch like this:

            public HeavyWidget(float mass) {
               try {
                 super(mass);
               } catch (IllegalArgumentException e) {

               }
               if (mass > MAX_MASS) {
                  throw new IllegalArgumentException();
               }
               this.mass = mass;
            }

        But this does not compile because `try` is now taken to be the
        first statement, which makes the compiler throw in a `super()`
        call *before* the `try`. And the compiler complains that there
        isn't a no-arg constructor in the `Widget` class. Also, it
        complains that the `super(mass)` statement is not the first
        statement. This issue--for which there isn't any sensible
        workaround--suggests that there may be some flaw in the design.
        In particular, making `HeavyWidget` a subclass of `Widget` means
        that EVERY heavy widget is a widget. (Along the lines of every
        student is a person, or every tiger is an animal). But is this
        true? If it were true, then EVERY heavy widget must pass the
        widget test. Which won't happen for all heavy widgets that have
        mass greater than 20. So it must be that every heavy widget is
        NOT a widget. So then is it true that EVERY widget is a heavy
        widget? In other words, if you were to flip the implementation
        so that `Widget` is a subclass of `HeavyWidget`, could you come
        up with clean code that works? If so, then there is a discord
        between how our everday phrasing in English, and Java
        implementation.

February 6th, 2013 - Lecture
----------------------------

-   When you make UI, the first thing you should do is draw the mockup,
    every window, every scheme.
-   This way you fine tune the UI before you write code.
-   When you have more complex layouts, you need the `JPanel` class to
    put in your `JFrame`.
-   A `JPanel` goes into a top level `JFrame`.
-   Generally, you should not allow the user to make mistakes.
-   For our project, we will have to make a storyboard.
-   You can use Eclipse to make a `JPanel` visually.
-   It doesn't do this as well as Xcode. Nowhere near.
-   `Color` is a class in `awt`.
-   You can make your own colors.
    -   You can set themesee in

-   `setEditable(boolean)` makes a panel read only (to the user).
-   `setForeground(Color)` and `setBackground(Color)` set the color of
    the interface.
-   `setFont(Font)` ... sets the font ...
-   A text field can have its horitniztonal alignment set with
    `setHorizontalAlignment()`
-   A `GridLayout` creates ... a grid for you to put UI elements in.
-   The difference between default and no argument constructors is that
    the compiler gives you no argument for free.
-   Make sure to always to ... `setVisible(boolean)`
-   `pack()` will make your `JFrame` as small as possible given your UI
    elements.
-   `protected` makes the scope of a variable visible to every class in
    the same package and any subclasses.

February 7th, 2013 - Lecture: GridBagLayout
-------------------------------------------

-   Example
    -   Fours buttons are added to a fram, constraints are all default
        values. On enlarging the fram, notice how the buttons *maintain
        their sizes* and stay centered within the container.
    -   `gridx` and `gridy`
        -   leftmost colum has `gridx = 0` and topmost row has
            `gridy= 0`
        -   Defult value is `GridBagConstraints.RELATIVE` - component is
            placed to the right of (if `gridx`) or in the row
            immediately below,

    -   `gridwidth` and `gridheight` \* Number of columns and row in the
        compnents display area. \* Note: Component may r5dftnot always
        fill its desplay area. \* Default value is one.

February 7th, 2013 - Assignment 1: Song Library GUI Design and Implementation
-----------------------------------------------------------------------------

### Description

Design and implement an application with a graphical user interface to
add and display a library of songs. No two songs should have the same
name and artist (case insensitive match.) Your application should have a
SINGLE FRAME with three interfaces:

-   A song list interface, with the ability to select ONE song from the
    list. The list will only display the names of the songs
-   A song detail interface, with name, artist, album, and year, of the
    song that is selected in the song list area.
-   An add/delete/edit interface, for adding new songs, deleting
    selected song, and editing selected song information:
    -   When adding a new song, the song name and artist should be
        entered at the very least. Year and album are optional.
    -   For editing, any of the fields can be changed.

There should be NO other windows in your application. While these three
interfaces should be easy to interpret and access, they need not
necessarily be three distinct containers. It is completely up to you as
to how you want to best design the interface, but you will be
responsible for making it clear and complete in functionality. (More
below.)

When your program is started, it should show the current list of songs
in the library, in the song list area, with the first song selected by
default. (The first time the program is run, there should be nothing in
the display, of course.)

The data should be persistent across different sessions of your program.
You can save the song list in a file in whatever format you like, and
then read it into your program when it starts up.

Your application is NOT required to play a song when it is selected.

The application frame should be resizable, and should appropriately
resize/not resize the constituent areas, according to what you think
would be best for the user experience.

Many of the aspects of design (frames, panels, layouts) and
implementation (event handling) you need to do this assignment have been
covered in class. However, you may need to add other aspects from
Swing/AWT, and you are expected to discover these for yourself. You may
find these links useful:

-   [How to Use Various
    Components](http://docs.oracle.com/javase/tutorial/uiswing/components/componentlist.html)
-   [A Visual Guide to Layout
    Managers](http://docs.oracle.com/javase/tutorial/uiswing/layout/visual.html)

### Grading

    GUI Component           Points
    Song list+selection     8
    Details display         7
    Add/Delete/Edit         20
    Persistence             5

(No Javadoc documentation needed, save for the @author tag - see
Submission Instructions below.) For the first three components, the
grade will be depend on correctness and compleletness of functionality,
as well as effective/appropriate use of Swing/AWT widgets. For the last
part (persistence), grading is on correctness, and on ensuring this is
transparent to the user, i.e. the user should not have to be concerned
with where and how the song list is stored between sessions.

Effective/appropriate means the UI should be clear, the user should know
exactly what to expect when events are triggered, the user should know
exactly what to do to achieve their objective. If you need to explain to
someone how to use the interface, then it's not a good enough interface.

Along these lines, your UI should not use widgets that are an overkill
for the task at hand because if a complex widget is used for a simple
task, it will confuse the user. (So, for instance, do NOT use a JTable
to show song details because the specification does not require you to
arrange/rearrange details in any particular order, or be able to sort on
any particular aspect of the details.)

Finally, your UI is not required to be aesthetically pleasing (no points
for this because it's highly subjective), but you can certainly try to
impress us with your creativity (just for the heck of it!) as long as it
does not get in the way of functionality.

### Submission Instructions

Call your main class SongLib (If you don't do this we will have to first
find which of your classes has the main method so we can run your
program. Points will be deducted!)

Make sure you add the Javadoc @author tag with your name to all the
classes you implement. No other Javadoc comments are required.

Export your project to a zip file called songlib.zip Make sure you have
done this correctly by importing it back as a project into Eclipse
(points will be deducted if we get a zip file that is not legit).

Submit your songlib.zip file.

[Source](https://github.com/PLJNS/Rutgers-Soft-Meth-Spring-2013/tree/master/Song%20Library/src/songLibrary)

February 11th, 2013 - Recitation 3: Tokenizing, GridBagLayout, Interfaces
-------------------------------------------------------------------------

1.  Write a program to accept a string and extract tokens from it. A
    token (string) is any sequence of non-whitespace characters, unless
    it is enclosed in double quotes, in which case everything inside
    double quotes (including whitespaces if any) is a token.

2.  Create a GUI application using a GridBagLayout. There should be 4
    buttons (one each for north, south, east, and west). Each button
    should have a visible amount of spacing between itself and other
    components. At the center of the application create a label. This
    label's text should initially read "default." When one of the
    buttons is pressed, the label's text should read one of north,
    south, east, or west as appropriate. When the window is resized, the
    buttons should continue to hug the borders, and the label should
    continue to be centered.

        package rec3;

        import java.awt.GridBagConstraints;
        import java.awt.GridBagLayout;
        import java.awt.Insets;
        import java.awt.event.ActionEvent;
        import java.awt.event.ActionListener;

        import javax.swing.JButton;
        import javax.swing.JFrame;
        import javax.swing.JLabel;

        public class GridBagLayoutExample extends JFrame {

        JButton[] buttons = {
           new JButton("North"),
           new JButton("West"),
           null,
           new JButton("East"),
           new JButton("South")
        };

        public static final int[] widths = 
        {GridBagConstraints.REMAINDER,1,1,GridBagConstraints.REMAINDER,GridBagConstraints.REMAINDER};

        GridBagLayout gb = new GridBagLayout();
        GridBagConstraints gbc = new GridBagConstraints();

        ActionListener al = new ButtonListener();

        JLabel label = new JLabel("Default");

        public GridBagLayoutExample(String title) {
           super(title);
           setLayout(gb);
           for (int i=0; i < buttons.length; i++) {
            addComponent(i);
           }
        }

        protected void addComponent(int i) {
            gbc.gridwidth = widths[i];
            if (buttons[i] != null) {
              gb.setConstraints(buttons[i], gbc);
              add(buttons[i]);
              buttons[i].addActionListener(al);
            } else {
              gbc.weightx = 1;
              gbc.weighty = 1;
              gbc.insets = new Insets(20,20,20,20);
              gb.setConstraints(label, gbc);
              add(label);
              gbc.weightx = 0;
              gbc.weighty = 0;
              gbc.insets = new Insets(0,0,0,0);
            }
        }

        protected class ButtonListener implements ActionListener {
            public void actionPerformed(ActionEvent e) {
              label.setText(e.getActionCommand());
            }
        }

        public static void main(String[] args) {
          // TODO Auto-generated method stub
          JFrame gbex = new GridBagLayoutExample("GridBagLayouExample");
          gbex.setDefaultCloseOperation(EXIT_ON_CLOSE);
          gbex.setLocationRelativeTo(null);
          gbex.pack();
          gbex.setVisible(true);
        }
        }

3.  Suppose you built a Java library of sorting algorithms: insertion
    sort, quicksort, and heapsort. You want to sell this library. How
    would you package your library so users could use any of these
    algorithms in their applications, and switch from using one to
    another (plug-n-play) with the least amount of code rewrite? Come up
    with the most appropriate design.

    -   Write an interface called `SortingAlgorithm` with one or more
        methods called `sort`, and then write various sorting classes
        for the different sorting algorithms, that implement the
        `SortingAlgorithm` interface.

4.  Examine the following classes, then answer the questions below.

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

    1.  As implemented above, these classes contain an error which will
        prevent them from compiling. Find and describe the error. Note
        that you should assume getThingValue() and getContraptionValue()
        are properly implemented. Do not change the compareTo() methods
        for this part.

        -   Attempting to implement `Comparable` interface twice with
            different generic types. Not possible.  
        -   The problem encountered at compilation time is that
            `Comparable< >` has been implemented twice for the
            `Contraption`. Because `Contraption` extends `Thing`, it
            also implements the interfaces that `Thing` implements, i.e.
            `Comparable<Thing>`. So `Contraption` implements
            `Comparable<Thing>` due to inheritance. But the explicit
            declaration that `Contraption` implements
            `Comparable<Contraption>` conflicts with the
            `Comparable<Thing>` implementation. Java will only allow one
            implementation of `Comparable<someType>`. This is true for
            any interface: SomeInterface can only be implemented once
            regardless of what is.

    2.  Re-implement the two classes so that two instantiations of
        Contraption can be compared via one of their compareTo methods.
        You will need to fully implement the two compareTo methods,
        however you may not change either compareTo methods' signature.
        Be sure to i) remove the compareTo methods' current return
        values and ii) correct the error from part (a). Assume that
        getThingValue() and getContraptionValue() are properly
        implemented. Use the following ordering rules for implementing
        the compareTo functions:
        -   Comparing two instantiations of Thing:
            -   Compare the "a" values. Return -1, 0, or 1 as
                appropriate for a compareTo function.

        -   Compare the "a" values. Return -1, 0, or 1 as appropriate
            for a compareTo function.
        -   Comparing two instantiations of Contraption: A Contraption's
            "a" value has a higher precedence than its "b" value. First
            compare the "a" values. If possible, return either -1 or 1.
            If an ordering cannot be established using only "a" values,
            compare the "b" values. This function should return -1, 0,
            or 1 as appropriate for a compareTo function.
            -   A Contraption's "a" value has a higher precedence than
                its "b" value.

    3.  Which classes' compareTo method will line 3 of the following
        code execute? Why?

            Thing myThing = new Thing();
            Contraption myContraption = new Contraption();
            int result = myThing.compareTo(myContraption);
            System.out.println(result);

        Line 3 will call `Thing`'s `compareTo()` method. The static type
        of `myThing` is `Thing`, and so is the dynamic type. The
        argument type, `Contraption` will match the `Thing` parameters
        since `Contraption` is a subclass of `Thing`, i.e. all
        `Contraption` objects are `Thing` objects.

February 12th, 2013 - Lecture: Interfaces
-----------------------------------------

### Using interfaces

-   Take a stack, for instance

        public class Stack<T> {
            private ArrayList<T> items;
            public Stack() { ... }
            public void push (T t) { ... }
            ....
        }

-   Look at this alternate code:

        public class LLStack<T> {
            private ArrayList<T> items;
            public Stack() { ... }
            public void llpush (T t) { ... }
            ....
        }

    -   Had this been production code, and you go from using `Stack` to
        `LLStack`, the client has to do a lot of work to convert
        everything from one to the other.

-   Solution:

        public interface Stack<T> {
            void push(T t);
            T pop();
            ...
        }

-   And:

        public class ALStack<T> implements Stack<T>
            private ArrayList<T> items;
            public ALStack() {...}
            public void push (T t) { ... }
            public T pop();

    -   This allows for plug and play.

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

February 14th, 2013 - Project Part 1: Photo Album (Design and Implementation I)
-------------------------------------------------------------------------------

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
    taken/file was created  
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
    recaption photos

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

    You **are required** to use the java.io.Serializable interface, and
    the java.io.ObjectOutputStream java.io.ObjectInputStream classes to
    store and retrieve data.

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

-   To list existing users:

        java cs213.photoAlbum.simpleview.CmdView listusers

        Output:
            <userId1>
            <userId2>
            ...
        Or: 
            no users exist

-   To add a new user:

        java cs213.photoAlbum.simpleview.CmdView adduser <user id> <user name>

        Output: 
            created user <user id> with name <user name>
        Or: 
            user <user id> already exists with name <user name>

-   To delete a user:

        java cs213.photoAlbum.simpleview.CmdView deleteuser <user id>

        Output:
            deleted user <user id>
        Or:
            user <user id> does not exist 

-   To login as an existing user:

        java cs213.photoAlbum.simpleview.CmdView login <user id>` 
            (*view now goes into interactive mode*) 
        Or: 
            user <user id> does not exist `

**Note**: You can run these from inside Eclipse by changing the program
arguments every time (See the Eclipse page for how to set program
arguments). However, this can get cumbersome. Instead, you can work in a
command window/shell, by going to the bin directory inside the project,
and running the **java** command from there.

#### Interactive Mode

-   To create an album:

        createAlbum "<name>"

        Output: 
            created album for user <user id>: 
            <name>
        Or: 
            album exists for user <user id>: 
            <name>

-   To delete an album:

        deleteAlbum "<name>"

        Output:
            deleted album from user <user id>:
            <name>
        Or: 
            album does not exist for user <user id>: 
            <name>

-   To list all albums, with their number of photos and the range of
    dates that the photos were taken:

        listAlbums

        Output:
            Albums for user <user id>: 
            <name> number of photos: <numberOfPhotos>,  <start date> - <end date>`
            ... 
        Or:
            No albums exist for user <user id>

-   To list the photos in an album:

        listPhotos "<name>"

        Output: 
            Photos for album <name>:
            <fileName> - <date>
            ...

-   To add a photo to an album:

        addPhoto "<fileName>" "<caption>" "<albumName>"

        Output: 
            Added photo <fileName>:
            <caption> - Album: <albumName>
        Or:
            Photo <fileName> already exists in album <albumName>
        Or:
            File <fileName> does not exist

    -   Notes:
        -   The date and time for the photo should be obtained from the
            properties of the photo file.
        -   The caption is a property of the photo, not the album. This
            means if you add a photo to more than one album, you specify
            the caption when adding to the first album. Then, when
            adding to subsequent albums, you specify an empty string for
            the caption, meaning that the caption is retained from the
            first add. The output message for the subsequent adds
            however should have the original caption, so it's clear that
            the caption has been retained.

-   To move a photo from one album to another:

        movePhoto "<fileName>" "<oldAlbumName>" "<newAlbumName>"

        Output: 
            Moved photo <fileName>:
            <fileName> - From album <oldAlbumName> to album <newAlbumName>
        Or: 
            Photo <fileName> does not exist in <oldAlbumName>

    -   Note: If the photo already exists in the new album, the command
        should return silently without doing anything.

-   To remove a photo from an album:

        removePhoto "<fileName>" "<albumName>"

        Output:
            Removed photo:
            <fileName> - From album <albumName>
        Or: 
            Photo <fileName> is not in album <albumName>

-   To add a tag to a photo:

        addTag "<fileName>" <tagType>:"<tagValue>"

        Output:
            Added tag:
            <fileName> <tagType>:<tagValue>
        Or: 
            Tag already exists for <fileName> <tagType>:<tagValue>

-   To delete a tag from a photo:

        deleteTag "<fileName>" <tagType>:"<tagValue>"

        Output:
            Deleted tag:
            <fileName> <tagType>:<tagValue>
        Or: 
            Tag does not exist for <fileName> <tagType>:<tagValue>

-   To list photo info:

        listPhotoInfo "<fileName>"

        Output:
            Photo file name: <fileName>
            Album: <albumName>[,<albumName>]...
            Date: <date>
            Caption: <caption>
            Tags:<tagType>:<tagValue>
            ...
            (grouped by tag type, in the order location first, then people, and
            then others, sorted by tag value within each type)
        Or: 
            Photo <fileName> does not exist

-   To retrieve all photos taken within a given range of dates, in
    chronological order:  
     getPhotosByDate <start date> <end date>\`

        Output: 
            Photos for user <user id> in range <start date> to <end date>:
            <caption> - Album:   <albumName>[,<albumName>]... - Date: <date>
            ...

-   To retrieve all photos that have all the given tags, in
    chronological order. Tags can be specified with or without their
    types:

        getPhotosByTag [<tagType>:]"<tagValue>" [,[<tagType>:]"<tagValue>"]...

        Output:
            Photos for user <user id> with tags <search string>:`
            <caption> - Album: <albumName>[,<albumName>]... - Date: <date>
            ...

-   To end the interactive mode (and the session):

        logout
        Output: none

Any errors (illegal parameters, invalid dates) should be handled
gracefully. No stack traces should be printed out (the user shouldn't
have to know what an exception is). Instead, a one sentence description
of what exactly went wrong should be printed. The format is as follows:

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

-   **Good design:** How well the project conforms to the MVC pattern,
    how well your submission of February 22 anticipated the completed
    implementation, and how well your UML diagram represents the code.
-   **Implementation**: Everyting described in the the **Model**,
    **View**, and **Control** specifications.
-   **Documentation:** Appropriately detailed javadocs
-   **Specification Adherence:** How well your project conforms to the
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
command line, right after `java` as in:  
 `java -cp . <stuff>`

The following sample works with this assumption. (And when we test your
program, we will run java outside Eclipse.)

    java cs213.photoAlbum.simpleview.CmdView login testuser c.. 

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

February 18th, 2013 - Recitation 4: Project Q&A, Debugging in Eclipse, Polymorphism
-----------------------------------------------------------------------------------

1.  Project Q&A
    -   This friday we have to hand in the APIs, how we're going to
        design it.
    -   We have "work to do", we have to implement what we do this
        Friday.
    -   Making an API is what you do in the real world.
    -   This is not naive paper work.
    -   Minor changes are likely okay, but major changes will lead to
        deductions.
    -   Photo objects and data containers are only getters and setters?
        -   Basically, yes.

2.  Debugging in Eclipse

    Download the (buggy) code in `HeapSort.java` and import it into
    Eclipse. Use the debugger to track down the bug(s) and fix the code.

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

    -   Every Person is expected to have one default home address, but
        Student can have another address for school.
    -   There are two ways to think about this.
        1.  One way is to think purely from the polymorphism point of
            view. If you were to run a loop through all objects in a
            mixed collection of Person and Student objects to print
            address, you will statically type the stepping reference as
            Person, say like this:

                    for (Person p: ) {
                        System.out.println(p.getAddress());
                    }

            This means, you want to look at every entity, including a
            Student, as a Person, which then implies that all addresses
            printed should be home addresses. If you take this point of
            view, then the Student class should not override the
            inherited getAddress method from Person, and should have a
            new getSchoolAddress method.
        2.  The other way to think about this is from the point of view
            of class design independent of how applications might use
            objects at run time. In this case, the method getAddress for
            a Student would override the inherited-from-Person
            implementation to return the school address instead. And a
            new getHomeAddress method would be coded to return the home
            address.

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
        -   Every time the `System.out.println(pts[i])` is executed,
            either a `Point` object is printed, or a `ColoredPoint` is
            printed, depending on the run-time type of the object to
            which `pts[i]` (which is statically typed to `Point`)
            refers. So `pts[i]` exhibits polymorphic behavior because it
            *automatically* changes "shape" between `Point` and
            `ColoredPoint` objects without any programmer intervention.

    2.  Give an example of code using the `pts` array that is NOT
        polymorphic, and explain why it is not polymorphic.

            for (int i=0; i < pts.length; i++) {
                  if (pts[i] instanceof ColoredPoint) {
                     System.out.println(((ColoredPoint)pts[i]).getColor());
                  }
               }

        This code is not polymorphic because in every iteration, the
        run-time type of `pts[i]` is checked explicitly, then cast to
        `ColoredPoint` - there is not any automatic shape-shifting.

5.  Suppose classes `A` and `B` are in package `ab`, and classes `C` and
    `D` are in package `cd`. Furthermore, both `C` and `B` extend `A`,
    and `D` extends `B`. Assume all classes are declared to be `public`.

    1.  Are `protected` members of `A` accessible in `C`?  If yes,
        explain how. If not, explain why.
        -   Protected members of `A` are *inherited* by `C`, but not
            accessible in `C` via instances of `A`.

    2.  Are `protected` members of `A` accessible in `D`?  If yes, how?
        If not, why?
        -   Protected members of `A` are *inherited* by `D` via `B` (in
            other words, `B` inherits protected fields from `A`, and `D`
            from `B`), but as with `C` protected members in `A` are not
            visible in `D` via instance of `A`.

    3.  Answer the same question as in 1. replacing `A` with `B`
        -   Protected members of `B` are *NOT* inherited by `C`, nor are
            they accessible in `C` via instances of `A`, since `C` is in
            a different package than `B`, but does not extend `B`.

    4.  Answer the same question as in 2. replacing `A` with `B`
        -   `D` inherits protected members of `B` since it subclasses
            from `B`

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

          public double getWeeklySalary() {
             return salary/52; 
          }
        }

        public class HourlyEmployee extends Employee {
            public HourlyEmployee(String aName, double anHourlySalary) {
                super(name);
                setSalary(anHourlySalary*40*52);
            }
        }

        public class SalariedEmployee extends Employee {
            public SalariedEmployee(String aName, double anAnnualSalary) {
                super(name);
                setSalary(anAnnualSalary);
            }
        }

7.  (Adapted from an example in Interface Oriented Design by Ken Pugh,
    sec. 4.2) Suppose you want to create a printing subsystem for
    several different printers, each with different
    capabilities/features (e.g. color printing, high-resolution, duplex,
    multiple trays, etc.).  How could you place the different
    capabilities into an interface?  Should you use a single interface
    or multiple interfaces (e.g. ColorPrinter, DuplexPrinter,
    MultiTrayPrinter)?  Describe the advantages and disadvantages of
    both approaches.

    -   It is generally better to produce several interfaces that are
        more specific to the various types of printers than to produce
        one large interface that covers all possibilities. If the
        interface is modified, then only code utilizing the modified
        interface must be changed. Programming each separate interface
        can take place independently and in parallel, so that the tasks
        can be distributed to different programmers.
    -   Also, any printer that did not make use of certain features of a
        single, combined interface, would have to write method stubs
        (empty method bodies) for non-implemented features, and throw
        exceptions if those methods were called. This is bad design,
        since a class should support every single feature for which it
        has a public method (otherwise why is that method in the class?)

February 19th, 2013 - Lecture
-----------------------------

### Object input and output streams

-   Jave provides a convinient way to dump all data.

        public static final String dirName = "dat"
        public static final String fileName = "filename"

        public static void writeApp(GeomApp gapp) 
        throws IOException {
            ObjectOutputStream oos = new ObjectOutputStream(
                new FileOutputStream(
                    dirname + File.separator + filename));

            oos.writeObject(gapp);
            // It's really that simple. (TM)
        }

-   This takes the object and writes the definitions of the classes
    before it writes the instances.
-   It'll actually write the geomApp class and it has references to
    points and it'll write that stuff out.
-   When it gets to an instance it'll give it a serial number.
-   Serial numbers are given so that if there are multiple instances of
    a given class there is only one definition that they all refer to.

        public static GeomApp readApp() 
                throws IOException, ClassNotFoundException {
            ObjectInputStream oos = new ObjectInputStream(
                new FileInputStream(
                    dirname + File.separator + filename));

            this = (GeomApp)ois.readObject(filename);
        }

-   Say you have a class which you serialize and someone else has it and
    you share the data, but that other person changes the class.
    -   What do?

-   This means that version 1 data could be incompatible with version 2.
    How do you fix this.
-   You have to declare a serial version UID.
    -   This is a static variable.
    -   By default it is 1.
    -   When you serialize, it doesn't write out the generated UID, it
        makes the 1.
    -   So when you have new datatypes, it's compatible.
        -   This seems like magic.

### Abstract Classes

-   When several classes have a common conceptual foundation, they can
    be generalized into an abstract superclass.
-   In Java a class is defined abstract in the class header.
-   An abstract method is one that has no implementation
    -   An abstract class may have zero or more abstract method.

-   An abstract class may implement non default constractors.
-   An abstract class cannot be instatiated even if all the methods have
    been implemented.

#### Inheritancee Polymorphism

-   Dynamically binding to same functionality in classes at different
    levels of an inhertance hierarchy.
-   This is interesting because it allows to write code that allows you
    to change entire implementation usage with just one change in code,
    so long as it implements an abstract class.
-   Dynamically binding to same functionality in classes at different
    levels of an inhertance hirarchy using a "least common denominator"
    type.
    -   Applied more boradly than just to abstract classes.

February 20th, 2013 - Lecture
-----------------------------

### Abstract class vs. Interface

#### Compare and contrast

-   You cannot have multiple inheritance with abstract classes,
    interfaces can.
-   Interfaces do not have any implentation, abstract class can.
-   If you find yourself with an abstract class with little
    implementation, you likely want an interface.
    -   Abstract classes close of the option.
    -   Depends on the context.

### UML Class Diagram - I

-   UML stands for Unified Modellling Language.
-   Mail graphical notation used to express object-oriented designed.
-   Most of it is arrows.
-   Types:
    -   **Class interaction diagram**: Used to show classes and the
        relations between them.
        -   **State diagram**: Used to represent state based designs.

    -   **Sequence diagram**: Used to show sequences of activity when
        methods are invoked on classes.

-   Class diagram
    -   A class diagram shows classes and the realtions between them.
    -   The simplest way to draw a class is like this:

            +-----------------------+
            |   rectangle           |
            +-----------------------+

    -   An even reater level of detail can be adde by specifyin the type
        of each attribute, as well as type of each parameter.
    -   And the access level for each member

            +-----------------------+
            |Window                 |
            +-----------------------+
            +-----------------------+
            |open()                 |
            |close()                |
            |move()                 | -------> dependance
            |refresh()              |
            |handleEvent()          |
            +-----------------------+       

February 25th, 2013 - Recitation 5: Abstract Classes, Interfaces
----------------------------------------------------------------

1.  This problem gives an example where polymorphism is useful. Consider
    the class hierarchy given below :

         public abstract class Shape implements Comparable<Shape {

             public void print() {
                 System.out.println("Shape");
             }

             public abstract double getArea();

              public static final Shape biggest(Shape[] s) {
            if (s.length == 0) { return null; }
            Shape biggestShape = s[0];
            for (int i = 1; i < s.length; i++) {
                if (biggestShape.compareTo(s[i]) < 0) {
                    biggestShape = s[i];
                }
            }
            return biggestShape;
        }

            public int compareTo(Shape s) {
            double areaDifference = getArea() - s.getArea();
            if (areaDifference == 0) {
                return 0;
            }
            return areaDifference < 0 ? -1 : 1;
        }
         }

         public class Circle extends Shape {
             double radius;

             public Circle(double r) {
                 radius = r;
             }

             public void print() {
                 System.out.println("Circle");
             }

             public double getArea() {
                 return Math.PI*radius*radius;
             }
         }

         public class Rectangle extends Shape {

             double height;
             double length;

             public Rectangle(double l,double h) {
                 length = l;
                 height = h;
             }

             public void print() {
                 System.out.println("Rectangle");
             }

             public double getArea() {
                 return length*height;
             }
         }

         public class App {

             public static void main(String[] args) {
                 Shape[] s = new Shape[3];

                 s[0] = new Circle(7);
                 s[1] = new Rectangle(5,10);
                 s[2] = new Circle(4);

                 System.out.println("The maximum area of a shape in s is : "+Shape.maximum(s));
                 return;        
             }
         }

    Complete the method

            public static Shape biggest(Shape[] s)

    in the `Shape` class. This method should return the shape with the
    largest area. Note that `Shape` implements the `Comparable`
    interface. Different `Shape`s should be compared using their area.
    Now if we extend the Shape hierarchy to include more shapes, say
    rhombus, then will your method run without any problems?

2.  In a previous problem set, you packaged a Java library of sorting
    algorithms:  insertion sort, quicksort, and heapsort.  using
    interfaces so that users could use any of these algorithms in their
    applications, and switch from using one to another (plug-n-play).
    Redo the exercise using abstract classes instead of interfaces.

    This is the abstract superclass of all the sorting algorithms:

             public abstract class Sort<T extends Comparable<T>> {
                T[] list;
                public Sort(T[] list) {    // implemented constructor
                   this.list = list;  
                }
                public abstract void sort();  // abstract sort method
             }

    Here's an example of one of the sorting implementations (just the
    shell):

            public class InsertionSort<T extends Comparable<T>> extends Sort<T> { // note the syntax
               public InsertionSort(T[] list) {
                  super(list);
               }
                public void sort() {   // implement the overridden abstract method
                   // implementation goes here
                   ...
                }
            }

    And the usage in client code:

            String[] list = new String[n];
            // populate list with strings
            ...
            Sort<String> sorter = new InsertionSort<String>(list);
            sorter.sort();
            // list is now in sorted order

3.  Think of a board game in which there are two kinds of pieces:  a
    slow piece that moves only one square at a time, and a fast piece
    that moves any number of squares (as required by the player) at a
    time.  Each piece can also be either flexible or not:  a
    non-flexible piece can only move horizontally or vertically, while a
    flexible piece can also move diagonally.

    How would you write Java code for all these pieces?  You need to
    have one class for each kind of actual piece.  Use interfaces and
    abstract classes as needed.  You don't need to fill in code for all
    the methods—just sketch the essential fields, constructor headers,
    and method headers.

        public abstract class GamePiece {
            public static final int DIR_NORTH = 0;
            public static final int DIR_SOUTH = 1;
            public static final int DIR_EAST = 2; 
            public static final int DIR_WEST = 3;
            public static final int DIR_NORTHEAST = 4;
            public static final int DIR_NORTHWEST = 5;
            public static final int DIR_SOUTHWEST = 6;
            public static final int DIR_SOUTHEAST = 7;

            protected int xPosition;
            protected int yPosition;

            public boolean movePiece(int numSpaces, int direction) {
                if (direction > DIR_SOUTHEAST || direction < DIR_NORTH || numSpaces < 0) {
                    return false;
                }
                switch(direction) {
                case DIR_NORTH:
                    yPosition += numSpaces; return true;
                case DIR_SOUTH:
                    yPosition -= numSpaces; return true;
                case DIR_EAST:
                    xPosition += numSpaces; return true;
                case DIR_WEST:
                    xPosition -= numSpaces; return true;
                case DIR_NORTHEAST:
                    yPosition += numSpaces; xPosition += numSpaces; return true;
                case DIR_SOUTHWEST:
                    yPosition -= numSpaces; xPosition -= numSpaces; return true;
                case DIR_NORTHWEST:
                    yPosition += numSpaces; xPosition -= numSpaces; return true;
                case DIR_SOUTHEAST:
                    yPosition -= numSpaces; xPosition += numSpaces; return true;
                }
                return false;
            }

            public GamePiece(int xPosition, int yPosition) {
                this.xPosition = xPosition;
                this.yPosition = yPosition;
            }
        }

        public class FastFlexiblePiece extends GamePiece {
            public FastFlexiblePiece(int xPosition, int yPosition) {
                super(xPosition,yPosition);
            }
        }

        public class SlowFlexiblePiece extends GamePiece {
            public SlowFlexiblePiece(int xPosition, int yPosition) {
                super(xPosition,yPosition);
            }

            public boolean movePiece(int numSpaces, int direction) {
                if (numSpaces > 1) {
                    return false;
                }
                return super.movePiece(numSpaces,direction);
            }
        }

        public class FastInflexiblePiece extends GamePiece {
            public FastInflexiblePiece(int xPosition, int yPosition) {
                super(xPosition,yPosition);
            }

            public boolean movePiece(int numSpaces, int direction) {
                if (direction > DIR_WEST) {
                    return false;
                }
                return super.movePiece(numSpaces,direction);
            }
        }

        public class SlowInflexiblePiece extends GamePiece {
            public SlowInflexiblePiece(int xPosition, int yPosition) {
                super(xPosition,yPosition);
            }

            public boolean movePiece(int numSpaces, int direction) {
                if (direction > DIR_WEST || numSpaces >1) {
                    return false;
                }
                return super.movePiece(numSpaces,direction);
            }
        }

    **Example implementation 2**:

        public abstract class GamePiece {

            public static final int DIR_NORTH = 0;
            public static final int DIR_SOUTH = 1;
            public static final int DIR_EAST = 2; 
            public static final int DIR_WEST = 3;

            protected int xPosition;
            protected int yPosition;

            // all pieces can move 1 space horizontally or vertically
            public void move(int direction) {
                if (direction > DIR_WEST || direction < 0) {
                    throw new IllegalArgumentException("direction > DIR_WEST || direction < 0");
                }

                switch(direction) {
                case DIR_NORTH:
                    yPosition++; break;
                case DIR_SOUTH:
                    yPosition--; break;
                case DIR_EAST:
                    xPosition++; break;
                case DIR_WEST:
                    xPosition--; break;
                }
            }

            public GamePiece(int xPosition, int yPosition) {
                this.xPosition = xPosition;
                this.yPosition = yPosition;
            }
        }

        public class SlowPiece extends GamePiece {
            public SlowPiece(int xPosition, int yPosition) {
                super(xPosition,yPosition);
            }

            public void move(int direction) {
                super.move(direction);
            }
        }

        public class FastPiece extends GamePiece {
            public FastPiece(int xPosition, int yPosition) {
                super(xPosition,yPosition);
            }

            public void move(int numSpaces, int direction) {
                if (numSpaces < 0) {
                   throw new IllegalArgumentException("numSpaces < 0");
                }
                if (numSpaces == 1) {
                    super.move(direction);
                    return;
                } 
                if (direction > DIR_WEST || direction < 0) {
                    throw new IllegalArgumentException("direction > DIR_WEST or < 0");
                }

                switch(direction) {
                case DIR_NORTH:
                    yPosition += numSpaces; break;
                case DIR_SOUTH:
                    yPosition -= numSpaces; break;
                case DIR_EAST:
                    xPosition += numSpaces; break;
                case DIR_WEST:
                    xPosition -= numSpaces; break;
                }
            }
        }

        public interface Flexible {
            public static final int DIR_NORTHEAST = 4;
            public static final int DIR_NORTHWEST = 5;
            public static final int DIR_SOUTHWEST = 6;
            public static final int DIR_SOUTHEAST = 7;
        }

        public class SlowFlexiblePiece extends SlowPiece implements Flexible {
            public SlowFlexiblePiece(int xPosition, int yPosition) {
                super(xPosition,yPosition);
            }

            public void move(int direction) {
                if (direction > Flexible.DIR_SOUTHEAST || direction < 0) {
                   throw new IllegalArgumentException("direction > Flexible.DIR_SOUTHEAST or < 0");
                }
            if (direction <= DIR_WEST) {
                   super.move(direction);
                   return;
                }
                switch(direction) {
                case Flexible.DIR_NORTHEAST:
                    xPosition++; yPosition++; break;
                case Flexible.DIR_NORTHWEST:
                    xPosition--; yPosition++; break;
                case Flexible.DIR_SOUTHWEST:
                    xPosition--; yPosition--; break;
                case Flexible.DIR_SOUTHEAST:
                    xPosition++; yPosition--; break;
                }
            }
        }

        public class FastFlexiblePiece extends FastPiece implements Flexible {
            public FastFlexiblePiece(int xPosition, int yPosition) {
                super(xPosition,yPosition);
            }

            public void move(int numSpaces, int direction) {
                if (numSpaces < 0) {
                   throw new IllegalArgumentException("numSpaces < 0");
                }
                if (direction > Flexible.DIR_SOUTHEAST || direction < 0) {
                   throw new IllegalArgumentException("direction > Flexible.DIR_SOUTHEAST or < 0");
                }
                if (direction <= DIR_WEST) {
                super.move(numSpaces, direction);
                    return;
                }
                switch(direction) {
                case Flexible.DIR_NORTHEAST:
                    xPosition += numSpaces; yPosition += numSpaces; break;
                case Flexible.DIR_NORTHWEST:
                    xPosition -= numSpaces; yPosition += numSpaces; break;
                case Flexible.DIR_SOUTHWEST:
                    xPosition -= numSpaces; yPosition -= numSpaces; break;
                case Flexible.DIR_SOUTHEAST:
                    xPosition += numSpaces; yPosition -= numSpaces; break;
                }
            }
        }

    **Further Thoughts**:

    -   Is one implementation better than the other?
    -   Is there any code redundancy in the second implementation? If
        so, how can it be removed?
    -   Can you think of another possibility that does not involve any
        abstract classes?

4.  A game developer asks you to make a set of classes to represent the
    monsters in a game. There are at least two different types of
    monsters, those that walk and those that bounce, but the code you
    write needs to be easily expandable to different types.
    Specifically, the code to keep track of a monster's appearance and
    to draw the monster needs to be in only one place. You are given an
    interface to start out:

        public interface Monster {
            void drawMonster();
            void setMonsterImage(Image i);
            void updatePosition();
        }

    Create an abstract base class `MovingMonster` for all monsters, and
    one subclass for each of two types discussed, `WalkingMonster` and
    `BouncingMonster`. Each monster will need to keep track of its own
    position and update it when the `updatePosition()` method is
    invoked. Assume that the Image class has a method
    `draw(int x, int y)`. The contents of the `updatePosition()` method
    are not important, but it has to change the monster's position and
    be different for either monster.

        public abstract class MovingMonster implements Monster {
            protected Image image;
            protected int xPosition;
            protected int yPosition;

            public abstract void updatePosition();

            public void drawMonster() {
                // Some implementation here.
            }
            public void setMonsterImage(Image i) {
                image = i;
            }

            public MovingMonster(Image image) {
                this.image = image;
                xPosition = yPosition = 0;
            }
        }

        public class WalkingMonster extends MovingMonster {
            public void updatePosition() {
                xPosition++;
            }

            public WalkingMonster(Image image) {
                super(image);
            }
        }

        public class BouncingMonster extends MovingMonster {
            public void updatePosition() {
                xPosition++;
                yPosition = (yPosition + 1) % 2;
            }

            public BouncingMonster(Image image) {
                super(image);
            }
        }

February 26th, 2013 - Assignment 2: 2-Player Chess
--------------------------------------------------

-   For this assignment you will explore how to apply the design ideas
    learned in class to design and implement a board game.

-   You will work **individually** on this assignment. Read the [DCS
    Academic Integrity Policy for Programming
    Assignments](http://www.cs.rutgers.edu/policies/academicintegrity/index.php?page=3)
-   you are responsible for this. In particular, note that **"All
    Violations of the Academic Integrity Policy will be reported by the
    instructor to the appropriate Dean".**

-   You will implement the game of
    [Chess](http://en.wikipedia.org/wiki/Chess) for two players. Your
    program, when launched, should draw the board using the terminal and
    prompt whomever's turn it is (white or black) for a move. Once the
    move is executed, the move should be played and the new board drawn,
    and the other player queried.

### Output

-   The board should be drawn on the screen with with ascii art in some
    sort of grid. Everything should be easily viewable in a standard
    sized terminal with 80 columns and 24 rows. The identity of each
    piece, color and type, must be easily discernible from the display.
    If the player whose turn it is is in check, that must be reported.
    The details are left to you.

-   Every piece must know what moves are allowed on it. If a player
    attempts an illegal move on a piece, your program should not execute
    the move, but instead, print an explanatory message detailing all
    legal moves the piece can make from the current position.
-   When a move is made, and it puts the opponent's King under check,
    your program should print "Check" before asking for the opponent's
    move.
-   If a checkmate or stalemate is detected, your program should print
    "Checkmate" or "Stalemate".
-   The last thing before termination should be a display of "Black
    wins", "White wins" or "Draw".

### Input

-   Your program needs to accept input of the form "FileRank FileRank",
    where the first file (column) and rank (row) are the coordinates of
    the piece to be moved, and the second file and rank are the
    coordinates of where it should end up.

-   The figure immediately below should make it clear which rank and
    file combinations belong to which squares. The white pieces always
    initially occupy ranks 1 and 2. The black pieces always initially
    occupy ranks 7 and 8. The queen always starts on the d file.

-   As an example, advancing the white king's pawn two spaces would be
    input as "e2 e4".

-   A castling move is indicated by specifying where the king begins and
    ends. So, white castling king's side would be "e1 g1".

-   A pawn promotion is indicated by putting the piece to be promoted to
    after the move. So, promoting a pawn to a knight might be "g7 g8 N".
    If no promotion is indicated, it is assumed to be a queen.

        bR bN bB bQ bK bB bN bR 8
        bp bp bp bp bp bp bp bp 7
           ##    ##    ##    ## 6
        ##    ##    ##    ##    5
           ##    ##    ##    ## 4
        ##    ##    ##    ##    3 
        wp wp wp wp wp wp wp wp 2
        wR wN wB wQ wK wB wN wR 1
         a  b  c  d  e  f  g  h

        White's move: e2 e4

        bR bN bB bQ bK bB bN bR 8
        bp bp bp bp bp bp bp bp 7
           ##    ##    ##    ## 6
        ##    ##    ##    ##    5
           ##    ## wp ##    ## 4
        ##    ##    ##    ##    3
        wp wp wp wp    wp wp wp 2
        wR wN wB wQ wK wB wN wR 1
         a  b  c  d  e  f  g  h

        Black's move: e7 e5

        bR bN bB bQ bK bB bN bR 8
        bp bp bp bp ## bp bp bp 7
           ##    ##    ##    ## 6
        ##    ##    bp    ##    5
           ##    ## wp ##    ## 4
        ##    ##    ##    ##    3
        wp wp wp wp    wp wp wp 2
        wR wN wB wQ wK wB wN wR 1
         a  b  c  d  e  f  g  h

        White's move:

#### Ending the game

-   If checkmate occurs, the game shall end immediately with the result
    reported.

-   A player may resign by entering "resign".

-   A player may offer a draw by appending "draw?" to the end of an
    otherwise regular move. The draw may be accepted by the other player
    submitting "draws" as the entirety of his or her next move. There
    will be no automatic draws (due to unchanging positions over long
    periods of time, etc).

### Grading

-   Correctness, 75 pts: Implementation of all required functionality
    including drawing the board
-   Design, 5 pts: Appropriate application of object-oriented design
    ideas you have learned. Although design points are low, our
    experience is that if you design your solution badly, you will have
    a lot of trouble implementing/debugging it.

### Submission

-   Name your project `Chess`. Use packages as necessary. Name your main
    class `Chess`. Make sure you record your name in each Java file with
    the @author Javadoc tag.

-   Zip your project source into a zip archive called `chess.zip` (see
    Eclipse tab, under "Zipping up a Project") and submit this file to
    Sakai.

-   [Source](https://github.com/PLJNS/Rutgers-Soft-Meth-Spring-2013/tree/master/Chess/src)

February 25th, 2013 - Lecture
-----------------------------

### Quiz preparation

-   Implemented `equals`
    -   An example of good equals, according to Dr. Sesh:

            public boolean equals (Object o) {
                if (o == null || !(o instanceof Point))
                    return null;
                Point p = (Point) o;
                return x == p.x && y = p.y;
                }

-   Another example from
    [StackOverflow](http://stackoverflow.com/a/27609/1489522):

            public boolean equals(Object obj) {
              if (obj == null)
                  return false;
              if (obj == this)
                  return true;
              if (obj.getClass() != getClass())
                  return false;
              Person rhs = (Person) obj;
              return new EqualsBuilder().
                  // if deriving: appendSuper(super.equals(obj)).
                  append(name, rhs.name).
                  append(age, rhs.age).
                  isEquals();
            }

-   Should be:
    -   reflexive
    -   symmetric
    -   transitive
    -   consistent

-   [access
    levels](http://www.tutorialspoint.com/java/java_access_modifiers.htm)
    -   `private`
        -   Methods, Variables and Constructors that are declared
            private **can only be accessed within the declared class
            itself**.
        -   Private access modifier is the most restrictive access
            level. **Class and interfaces cannot be private**.
        -   Variables that are declared private *can be accessed outside
            the class if public getter methods are present in the
            class*.

    -   `package`
    -   `protected`
        -   Variables, methods and constructors which are declared
            protected in a superclass can be accessed only by the
            subclasses in other package or any class within the package
            of the protected members' class.
        -   The protected access modifier cannot be applied to class and
            interfaces. Methods, fields can be declared protected,
            however methods and fields in a interface cannot be declared
            protected.
        -   Protected access gives the subclass a chance to use the
            helper method or variable, while preventing a nonrelated
            class from trying to use it.

    -   `public`
        -   A class, method, constructor, interface etc declared public
            **can be accessed from any other class**. Therefore fields,
            methods, blocks declared inside a public class can be
            accessed from any class belonging to the Java Universe.
        -   However if the public class we are trying to access is in a
            different package, then the public class **still need to be
            imported**.
        -   Because of class inheritance, **all public methods and
            variables of a class are inherited by its subclasses**.

    -   [Awesome
        table](http://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html):
        <table class="table">
                            <tbody><tr>
                            <th markdown="1" id="h1">

        Modifier
        </th>
            <th markdown="1" id="h2">

        Class
        </th>
            <th markdown="1" id="h3">

        Package
        </th>
            <th markdown="1" id="h4">

        Subclass
        </th>
            <th markdown="1" id="h5">

        World
        </th>
            </tr>
            <tr>
            <td markdown="1" headers="h1">

        <code>public</code>
        </td>
            <td markdown="1" headers="h2">

        Y
        </td>
            <td markdown="1" headers="h3">

        Y
        </td>
            <td markdown="1" headers="h4">

        Y
        </td>
            <td markdown="1" headers="h5">

        Y
        </td>
            </tr>
            <tr>
            <td markdown="1" headers="h1">

        <code>protected</code>
        </td>
            <td markdown="1" headers="h2">

        Y
        </td>
            <td markdown="1" headers="h3">

        Y
        </td>
            <td markdown="1" headers="h4">

        Y
        </td>
            <td markdown="1" headers="h5">

        N
        </td>
            </tr>
            <tr>
            <td markdown="1" headers="h1">

        no modifier
        </td>
            <td markdown="1" headers="h2">

        Y
        </td>
            <td markdown="1" headers="h3">

        Y
        </td>
            <td markdown="1" headers="h4">

        N
        </td>
            <td markdown="1" headers="h5">

        N
        </td>
            </tr>
            <tr>
            <td markdown="1" headers="h1">

        <code>private</code>
        </td>
            <td markdown="1" headers="h2">

        Y
        </td>
            <td markdown="1" headers="h3">

        N
        </td>
            <td markdown="1" headers="h4">

        N
        </td>
            <td markdown="1" headers="h5">

        N
        </td>
            </tr>
            </tbody></table> 

-   `interface`
    -   an interface is a group of related methods with empty bodies
    -   Interfaces cannot be instantiated, but rather are implemented
    -   One benefit of using interfaces is that they simulate multiple
        inheritance

-   [`abstract`
    classes](http://docs.oracle.com/javase/tutorial/java/IandI/abstract.html)
    -   An abstract class is a class that is declared abstract - it may
        or may not include abstract methods. Abstract classes **cannot
        be instantiated**, but they **can be subclassed**.
    -   An abstract method is a method that is declared **without an
        implementation**
    -   When an abstract class is subclassed, the subclass usually
        provides implementations for all of the abstract methods in its
        parent class. However, if it does not, the subclass must also be
        declared abstract.

-   polymorphism
-   inheritance
-   `static`
-   dynamic binding

### UML Class Diagram II

-   Class A depends on class B if A **uses** B in such a way that a
    change in B will effect A
-   Say A depends on B. Typically, then, B would appear as a parameter,
    return type, or local variable in a method of A.

March 4th, 2013 - Recitation 6: UML
-----------------------------------

1.  Give one example UML each (not covered in class!) of a
    uni-directional association, a bi-directional association, and an
    association class. (We stopped just short of the association class
    in lecture on Feb 28, but look at the last three slides in the
    feb28-uml.pdf that was posted in Resources.) By writing minimal
    amount of code (class headers and fields only), show how the
    relationship information depicted by the UML shows up in the
    implementation.

2.  For each of the following pairs/groups of classes, show the most
    appropriate relationship between them using UML (include
    multiplicities, and relationship classes for associations):

    1.  `Document`-`Keyword` in a search engine
    2.  `Friend-Friend` on Facebook
    3.  `Entry-Contributor` on Wikipedia
    4.  `Item-Seller-Bidder` on Ebay
    5.  `Book-Author-Publisher` on Amazon

3.  You are on a project that is developing software to manage a
    hospital. In particular, you are working on a sub-system that will
    model the patient care aspect including doctors, patients, hospital
    rooms, and services for which patients are billed. Services include
    medical services such as x-rays, as well as room services such as
    bed, TV, etc.

    Draw a UML class diagram of your model, with key attributes and
    methods for every class. Pay particular attention to making decisons
    about whether some entity should be an attribute of an object with
    values to differentiate between instances of the entity, or whether
    the entity deserves to be in its own class (fully typed). You should
    be able to argue for your decision either way.

    Also, make sure you don't model relationship-specific data
    structures as attributes in either of the participating classes.
    Such data structures should only show up in the implementation,
    chosen according to the constraints of the language of
    implementation (e.g. choices in Java may differ from C++) and
    requirements of efficiency. (UML is implementation-language
    neutral).

    Implement your model with outline of code including class headers,
    interfaces (if applicable) with method specifications, fields in all
    classes, method headers in all classes

March 5th, 2013 - Lecture
-------------------------

-   An **association class**is used to model an association between two
    classes.
    -   For example, if you had a `Company` and an `Employee` object,
        then you'd have a `Job` class to stand for the relationship.

March 8th, 2013 - Project Part 2: Photo Album (Design and Implementation II)
----------------------------------------------------------------------------

### Dates

-   Posted Fri, Mar 8  
-   GUI Storyboard and Work Split Document Due Wed, Mar 27, 11 PM  
-   Complete Implementation and Test Cases Due Fri, Apr 12, 11 PM.

### Features

In Part 1, you built a simple view for your photo album. In this part,
you will replace the simple view with a Graphical User Interface (GUI).

Your GUI will implement the following single-user paradigm, using
session persistence:

-   When the application starts, a user logs in with username. Password
    implementation is optional. It makes for a "real" scenario, but is
    irrelevant to the essence of the project.

-   There must be a special username **admin** that will take
    application to an administration sub-system. The **admin** user can
    do the following:
    -   List users
    -   Create a new user
    -   Delete an existing user

The rest of the specification below pertains to **non-admin** users
only.

Once the user logs in successfully, all albums and photo information for
this user from a previous session (if any) are loaded from disk.
Initially, all the albums belonging to the user should be displayed. For
each album, its name, the number of photos in it, the date of the oldest
photo, and the range of dates (earliest and latest date) on which photos
were taken. Use your discretion on how to show this additional
information.

The user can then do the following:

Create albums

Delete albums

Rename albums

Open an album. Opening an album displays all photos, with their
*thumbnail* images and captions, inside that album. Once an album is
open the user can do the following:

-   Add a photo
-   Remove a photo
-   Recaption a photo
-   Display a photo. Displaying a photo should fit the image in its
    display area, and should also show caption, date-time of capture,
    and all the tags.
-   Add a tag to a photo
-   Delete a tag from a photo
-   Move a photo from one album to another
-   Go through photos in album in sequence forward or backward (manual
    slideshow)

Search for photos (Photos that match the search criteria should be
displayed in a similar way to how photos in an album are displayed).
Under this, you should provide the following specific features:

1.  Search for photos by a date range.
2.  Search for photos by tag type-value pairs. This should follow the
    same rules as the command line version, where not specifying the tag
    type implies it can match any tag type.

There should be functionality to make an album out of the result of
either of the above searches.

Whatever view you choose to implement, make sure that users have the
power and the flexibility to get at all the information they want with
as few clicks/selections as possible (usability), and are not
overwhelmed with too much information all at once (scalability).

The user logs out at the end of the session. All albums and photo
information for the user are stored to disk.

After a user logs out, the application is still running, allowing
another user to log in.

There should be a way to quit the application **safely** at any time.
Safely means that you should make sure that all updates that were made
to the system in the current user's session are recorded correctly as
required by the user.

In the application all errors and exceptions should be handled
gracefully within the GUI. (The console should NOT be used for any
input, output, or error.)

### GUI Storyboard

Your first task is to design the interface in the form of a
**storyboard**.

The storyboard is a sequence of screen diagrams that shows all paths of
flow through the interface. Here's a [sample storyboard](storyboard.pdf)
for a calculator application that gives you an idea of what you should
do. This is not a complete storyboard in that it does not show all
possible screens that are in the UI it describes, nor does it
necessarily show all possible transitions between screens. What it does
show is how to draw screens, how to label screen components, how to draw
transitions between screens, and how to label transitions.

It is important to have a first page that is an overview that shows all
screens and all transitions between them, without any details of the
components within the screens themselves. This is an overview that can
give the complete picture in one shot. The rest of the storyboard will
then draw each screen in detail.

Each screen must be drawn using some drawing package. **Screenshots that
you take off a program WILL NOT be accepted.** In other words, there
should be **no program code** written at this stage at all.

Each screen will represent one window of your GUI and will contain all
the widgets that go into that screen - text fields, buttons, etc. Be as
precise as you can about the selection and layout of the components in a
screen. **You must LABEL each component with the Swing class of which it
is an instance, as shown in the model storyboard.**

Each screen will show transitions to other screens and the events that
trigger these transitions. When all is said and done, you will have
effectively drawn up a storyboard of your entire GUI that shows all
screens and all inter-screen transitions.

**Note**: The title for each screen should be descriptive of what the
screen does. The sample storyboard says "Calculator" for all titles, but
for your storyboard, name every screen with an appropriate title. This
can serve as the title to be displayed in the titlebar when you
implement these screens in code.

**Special Note**: Credit for the storyboard will be based on how well it
anticipates (and determines) the implementation of the GUI. This portion
of the grade for your storyboard will be given **after** you finish the
implementation, and we can look at how useful your storyboard has been
for your implementation.

### Work Split Documentation

When you have finished designing the storyboard, you need to decide how
to split the work of implementing all the windows. Implementing a window
will also include all non-visual aspects associated with it, all event
handling, the connections to the other parts of the GUI, and the
connections to the control and model. The work split must be as equal as
you can make it.

Type up the work split documentation (plain text or PDF, no other format
will be accepted). Make a table with two columns: in one column list the
name of the window to be implemented, and in the second, the team member
who will implement it.

### GUI Implementation (With UML, Javadocs and Data Files)

Implement your GUI using Java AWT and Swing components **only**. (We
will test with the standard JRE so if you use any external packages,
your program will not run, and you will not get credit.) You must make
sure your program can compile and run under Java 6.

Document every class you implement with Javadoc tags, and be sure to
include authorship.

Extend the UML class diagram from Part 1 to include all the new classes
you built in Part 2. In your UML diagram, include classes for all Java
swing components that are used. Shade them as illustrated in this
[Hangman UML diagram](hangman_uml.png).

For each class you built, show all public fields and methods in the UML
representation.

Keep in mind that you will need classes that are not visually
represented, but perform data-management functions, as well as broker
between the visual classes and the backend. These should be in your UML
as well.

**Load the application with some sample data of users, albums, and
photos that can be used to test your code.** This data should be able to
drive all the tests you list in the test report, as described in the
**Testing** section that follows. Your program should be runnable
without any of the data files specified above (except for whatever
information is needed to log in the **admin** user.)

### Testing

Write down every test you performed or would have liked to perform on
your photo album code, *including tests for robustness*. Write your test
report with the following structure:

-   List all the "use cases" of your application. A use case is any
    single request-response functionality that is implemented. For
    instance, creating an album is a use case.

-   For each use case:
    -   Define the equivalence classes of tests for that use case,
        *including equivalence classes for error conditions*.
    -   For each equivalence class, list all the test cases you used.
        The test case should list the data exactly as entered into the
        interface. For each test, either list (if it is a small set) or
        describe (if it is a large set) the expected result.

Write your test report in a spreadsheet called **tests.xls** (If you
don't have a spreadsheet program on your computer, you can use Microsoft
Excel at any of the campus computing labs, or use Google documents
spreadsheet and export as Excel.)

Your spreadsheet should look like this:

    ------------------------------------------------------------- ------------------------------------------- -----
    **Group Members**: \< your names\>                                                                        
                                                                                                              
    **Use Case 1**: \<List the use case\>                                                                     
    **Equivalence Class 1**: \<Describe the equivalence class\>                                               
    **Test Case**                                                 **Expected result**                         
    \<List the test input data\>                                  \<List/Describe the expected result\>       
    ...                                                           ...                                         
    **Equivalence Class 2**: \<Describe the equivalence class\>                                               
    **Test Case**                                                 **Expected result**                         
    ...                                                           ...                                         
                                                                                                              
    **Use Case 2**: \<List the use case\>                                                                     
    ...                                                           ...                                         ...
    ------------------------------------------------------------- ------------------------------------------- -----

### Mercurial Contents

#### By Wednesday, March 27, 11 PM

(The **docs** and **data** directories mentioned below should be created
directly under the project, NOT under **src** or under any of the
packages).

-   **GUI Storyboard**: The final form of your storyboard should be a
    PDF file called **storyboard.pdf**, which should be placed in the
    **docs** directory (where you put your javadoc documents for Part
    1).
-   **Work Split Document**: The final form of this document should be a
    plain text (.txt) or PDF file, called **worksplit.txt** or
    **worksplit.pdf**, and must be in the **docs** directory.

#### By Friday, Apr 12, 11 PM

-   **GUI Implementation**: Arrange your code elements in your GUI
    implementation to be consistent with how your arranged the model and
    control code in Part 1.
-   **UML**: The complete UML class diagram (updated for this part) for
    the project should be a PDF file called **uml2.pdf**, placed in the
    **docs** directory.
-   **Javadocs**: The complete Javadocs documentation should be
    generated and placed in the **docs** directory.
-   **Sample Data**: Users, albums, and photos for testing, to be placed
    in a **data** directory.
-   **Test Cases**: The **tests.xls** spreadsheet, to be placed in the
    **docs** directory.

### Grading

Your project will be graded on the following, for 200 points:

    ---------------------------------------------------------------------- --------
    Category                                                               Points
    UML + Javadocs + Storyboard                                            30
    Features (listed in Features)                                          125
    Robustness/Error Handling                                              15
    Deployment (naming packages, doc and data directory with content)      5
    Test Report                                                            25
    Total                                                                  200
    ---------------------------------------------------------------------- --------

**EXTRA CREDIT**:

-   (Up to **25 points**) for exceptional user interface features.

**Penalties** (up to 25 points) will be assessed on the following:

-   Needing extra configuration on our part to test your project because
    you did not follow specifications: **upto 5 pts**
-   Usability is poor such as roundabout ways to get at data, and/or
    confusing interface: **upto 10 pts**
-   Lacks scalability i.e. doesn't display large amounts of data (e.g.
    many tens of photos or more) in a easily navigable way: **upto 10
    pts**

March 11th, 2013 - Recitation 7: Table/Model, Image Handling
------------------------------------------------------------

1.  UML Quiz

2.  You will learn how to create a GUI application for a simple
    spreadsheet. You are to use javax.swing.JTable,
    javax.swing.table.TableModel, and
    javax.swing.table.DefaultTableModel. The contents of each cell may
    be either a floating point number or one of four simple formulas:
    =sumcol, =sumrow, =avgcol, =avgrow.

3.  You will learn how to load, display, and resize images using
    javax.swing.Image, javax.swing.ImageIcon, javax.swing.JSlider,
    java.awt.BorderLayout, and javax.swing.JScrollPane.

March 28th, 2013 - Recitation 8: Testing, Design Patterns
---------------------------------------------------------

1.  Let `Tomorrow` be a function of three variables: `month`, `day`, and
    `year`. It returns the date of the next day that follows the given
    input date. You may assume that `year` is in the range 1901 through
    1.  Using equivalance classes and boundary values, determine the
        test cases you would use to test a software implementation of
        this function. Include robustness tests.

2.  A polynomial may be represented as a linked list as follows: for
    every term in the polynomial there is one entry in the linked list
    consisting of the term's coefficient and degree. (There will be
    exactly one term in any degree.) The entries are ordered according
    to ascending degrees, and zero-coefficient terms are not stored. An
    empty (zero) polynomial is represented by a linked list with no
    nodes in it.

    For example, the following polynomial (the symbol '\^' is used to
    mean 'raised to the power'):

    4*x*<sup>5</sup> − 2*x*<sup>3</sup> + 2*x* + 3

    can be represented as the linked list of terms:

              (3,0) -> (2,1) -> (-2,3) -> (4,5)

    where each term is a (coefficient,degree) pair.

    Now suppose there is a method that **adds** two polynomials and
    returns the result in a new polynomial - the input polynomials are
    not modified. You are asked to black-box test this method for
    correctness, using the equivalence classes/boundary values approach.
    Clearly specify how you will apply this approach to identify test
    cases, and write down each such test case pair of input polynomials.
    Also identify test cases for checking correct reporting of errors
    (robustness).

3.  Draw a state diagram that models a user's shopping session at
    amazon.com, starting with a search. Show the UML for an
    implementation using the state design pattern including key fields
    and headers for the methods in the states.

4.  Show how you would enhance the Singleton pattern to allow up to a
    maximum number of instances of an object. There should be a way for
    clients to recycle instances, i.e. when a client is finished with an
    instance, it gives it up, and this instance can be later dealt out
    in response to a new instance request.

March 29th, 2013 - Assignment 3 (Web Discussion Groups UML)
-----------------------------------------------------------

You will work **individually** on this assignment. Read the [DCS
Academic Integrity Policy for Programmming
Assignments](http://www.cs.rutgers.edu/policies/academicintegrity/index.php?page=3)
- you are responsible for this. In particular, note that **"All
Violations of the Academic Integrity Policy will be reported by the
instructor to the appropriate Dean".**

Develop an object-oriented design and draw UML for web discussion groups
(such as Google groups).

#### Discussion Groups

The discussion groups are a part of a website of which a person first
needs to be a user before they can participate in one or more groups.

-   Each group has one or more members.
-   Members of a group can:
    1.  post messages to the group
    2.  read messages posted by other members to the group sorted
        according to combinations of message author, thread, or date

-   Each message is part of a discussion thread. It can be the
    initiating message for a new thread, or a response to a previous
    message in a thread
-   Users of the website can:
    1.  create new groups
    2.  join an existing group as member
    3.  leave a group

-   Every group has a single owner, who is initially the creator of the
    group. (The creator of a group automatically becomes its first
    member.)
-   Each group has one moderator, who is initially the creator of the
    group. Only a member can be a moderator.
-   Owners can:
    1.  invite users to join their group by sending them an email
        invitation
    2.  invite a member (including self) to be the moderator - if the
        invitation is accepted, the new moderator replaces the current
        moderator
    3.  invite a member to take over ownership - if the invitation is
        accepted, the ownership is transferred to that member
    4.  delete the group

-   Moderators can:
    1.  Deny or pass through messages posted to the group by members
    2.  Resign as moderator by sending an email to the owner, at which
        point the owner becomes the moderator (by inviting self)

#### UML

Choose the most appropriate representation for each entity in the model.
(Entity here refers to class or interface.) Use interfaces and abstract
classes as needed. In each class, decide what key attributes and methods
are needed to flesh out the specification. Not all details are
explicitly mentioned in the specification above, but must be filled in
by inference. Such details include choice of attributes and their data
types, choice of operations with parameters return values, and choice of
access levels (public/protected/package/private) for attributes and
operations.

Pay special attention to the relationships between entities. Remember,
super-sub classes, and interface implementations are the strongest
connections between entities, followed by associations, followed by
dependencies. Make sure you are as specific as you can be with the
multiplicities in associations, and whether an association is a plain
old link or an aggregation or a composition, whether it is
bidirectional, unidirectional or reflexive. Note: Every association is
by definition bidirectional unless you explicitly show
unidirectionality. Make sure you show multiplicities for all
associations.

#### Supplement to the UML

For each association, list the data structure (full type definition in
Java) that will be used to implement that association, and name the
class to which it will belong. You don't have to outline any class, just
draw a table with two columns, one for the data structure type
definition, and the other for the class in which it will be defined. (If
it is a class that is neither end point of the association, then make
this fact explicit in the table.)

#### Grading

Your UML and supplement will be graded on completeness, appropriate
choices in class/interface/abstract class for entities, appropriate
choices in relationships between entities, and how well you have chosen
data structures to implement associations. "Appropriateness" speaks to
the best applicable/most precise design choices based on all the
object-oriented design issues we have covered in class, flexibility (how
easy it is to use your design for a range of functionality),
extensibility (how easily your design can be extended to add more
capabilities), maintainability (how easy it is to fix problems that may
be arise in implementation). Not all of these may apply with equal
importance (every model is different) but you want to use this as a
checklist against your design to spot, and correct obvious flaws.

#### Submission Instructions

Submit a single PDF file, called webgroups.pdf, to Sakai. (Whatever
software you use to draw the diagrams/write text, you MUST convert to
PDF.) The PDF document should have the UML as well as the supplementary
table of data structures. If you have trouble fitting the UML in one
page, draw the UML with only the class names and relationships between
them on one page, and then on other pages, draw the details for each
entity. Scanned hand-drawn and hand-written submissions will NOT be
accepted.

April 1st, 2013 - Recitation 9: Multithreading, Android
-------------------------------------------------------

1.  Use threads to implement a stop watch that displays, *once every
    five seconds*, the minutes and seconds that have passed since it was
    started. The display should be in the form `mm:ss` for minutes and
    seconds. When the clock reaches 15 minutes, it should wrap back and
    start at 0 minutes and 0 seconds. The user should be able to stop
    the watch at any time. Write the complete code for the application.
    (Not the most accurate stop watch, but the model is useful for
    animations in which slight inaccuracies in time would not be
    detrimental.)

2.  Write an Android app that can accept an order to make a sub. Have
    checkboxes to select (or unselect) items to add (lettuce, tomato,
    etc.) Have combo boxes or equivalent to select one out of many
    (exclusive) options like the type of cheese to put in the sub. When
    the user confirms the order (via a button), display a message in a
    text area that lists the sub contents. Your UI doesn't have to be
    pretty - just make it work correctly.

April 2nd, 2013 - Lecture: Android Development
----------------------------------------------

This document points you to the appropriate developer resources that
describe how to set up Eclipse for Android development on your personal
computer. It also points you to resources that show how to create a
mobile Android device emulator for testing your application in Eclipse,
as well as how to install and test your application on an Android
smartphone. Written by Sesh Venugopal, Rutgers University. For CS 213
Spring 2013.

It is assumed that you have already installed Java and Eclipse on your
machine before you do the Android setup. (Java and Eclipse are already
available on the ilab machines.)

### Android SDK

#### Step 1: Download the SDK

The first thing you will need to do is download the Android SDK
(software development toolkit), which has all the tools you will need to
develop Android programs.

Go to [Get the Android SDK](http://developer.android.com/sdk/index.html)
On that page, you will see USE AN EXISTING IDE toward the lower half.
Expand it, and you'll see this:

I am on a Mac, so it shows up a Mac download button. If you are on
Windows, you should a Windows download button. Click on the button,
agree to the terms, then download.

-   For the Mac, you will download a zip file called
    **android-sdk\_r21.0.1-macosx.zip**
-   For Windows, you will download an installer file,
    **installer\_r21.0.1-windows.exe**

(r21.0.1 is the latest version as of this writing).

### Step 2: Set up the SDK

The next phase is to install the ADT for Eclipse.

### ADT for Eclipse

ADT stands for Android Development Toolkit. It is a plug in for Eclipse
that comes with a full set of tools to build, test, and export Android
apps to the Android market. To plug the ADT into Eclipse, go to
[Installing the Eclipse
Plugin](http://developer.android.com/sdk/installing/installing-adt.html),
and execute the following two steps.

#### Step 1: Download the ADT Plugin

The first thing you will need to do is download the Android SDK
(software development toolkit), which has all the tools you will need to
develop Android programs.

Go to Get the Android SDK On that page, you will see USE AN EXISTING IDE
toward the lower half. Expand it, and you'll see this:

I am on a Mac, so it shows up a Mac download button. If you are on
Windows, you should a Windows download button. Click on the button,
agree to the terms, then download.

-   For the Mac, you will download a zip file called
    android-sdk\_r21.0.1-macosx.zip
-   For Windows, you will download an installer file,
    installer\_r21.0.1-windows.exe

#### Step 2: Point the ADT to the SDK

-   Follow the instructions. On my Mac, I unpacked the file, moved the
    resulting directory to directly under my home directory, and renamed
    it as android-sdk-macosx. Here are the contents of this directory:

### Adding Platforms and Packages

An Android platform is basically a version of the Android API on which
you can run your app.

Since there are so many Android devices on the market, when you build an
app, you need to know whether you are building for the largest possible
user base, or for a specific subset of devices. For instance, you might
build a simple app that you want to target to as many users as possible.
In this case you would want to build your app for the earliest possible
platform that will support its features, say, Android 2.3.3. Or, you
might want to build a sophisticated app that can only be run on tablets,
in which case you will need to go with a platform that supports tablets,
such as Android 3.2.

A platform is tied to a certain revision of the SDK tools, and before
you install a newer platform, you need to update the SDK tools to the
revision required by the platform. For instance, the Android 4.2
platform needs the SDK tool revision r20 or higher. The Android 3.2
platform needs SDK tool revision r12 of higher.

Once you have identified which platforms you want to install, it is an
easy matter to do it in Eclipse, with the Android SDK Manager.

### Downloading Platforms and SDK Tools with SDK Manager

After plugging in the ADT into Eclipse, when you start Eclipse, you
should see a set of extra icons in the task bar at the top.

Clicking on the SDK Manager icon brings up this window:

The manager displays all available versions of the platforms. Here I
have expanded and highlighted the versions that I installed: 4.2, 3.2,
and 2.2 (each of these is mapped to an API level.) I have superimposed a
snapshot of my filesystem where you see the corresponding platform
directories under android-mac-osx/platforms. If I were to expand any of
the other versions (such as Android 4.1.2), it would show nothing
installed. Also notice at the top that the SDK tools version r21 is
installed.

Now say I wanted to install Android 2.3.3. (The expansion of that
version in the SDK shows it is not installed):

I can install all packages under Android 2.3.3 by clicking on the
checkbox to its left. But here, I am choosing to install only the SDK
Platform (required at minimum), and Google APIs (required if you are
going to use Google tools such as maps), so I check only these two:

Clicking on the "Install 2 packages..." button brings up this dialog:

Choose "Accept all" and click "Install". After installation, you should
see this in the SDK manager:

### Creating an Emulator

When you write an app, you can test it on emulators for various device
sizes and pixel densities so you now that it works well on small and big
phones, with varying degrees of pixel resolution. You can set up
emulators using the Android Virtual Device Manager, shown earlier:

The device manager allows you to create an emulator according to need.
When you click on the icon, you see a wizard to create an emulator, or
to edit an existing emulator, shown on the left in the following figure.
Let's create a new emulator, by clicking on the **New...** button in the
right hand bar, which brings up a create wizard, shown on the right.

The important fields here are "Device" and "Target", at the top. If you
pull down the "Device" choices you will see a list of "skins",
corresponding to devices of various sizes and densities. The following
table, from the page [Supporting Multiple
Screens](http://developer.android.com/guide/practices/screens_support.html)
of the Android documentation site:

The "Device" pull down list in the new AVD creator lists many of these
skins. I generally pick HVGA (320 x 480) (second row, second column),
which is for a normal screen, medium density, with potentially the
broadest reach in terms of ownership.

The other important field, "Target", should list all the APIs installed.
The list will also include Google APIs, which you would choose if you
were to incorporate, say, Google Maps. I picked Android 2.3.3 as the
target.

Leaving all other fields at their default settings, here's the
configuration, to the left, and the resulting emulator list, to the
right:

### Writing a Simple App

You are ready to start writing Android apps! Here's a simple "hello
world" app to get you started.

#### Creating an Android Project

When you enter Hello World for the application name, the wizard will
automatically fill in HelloWorld for the project name, and
com.example.helloworld for the package name - see the filled in wizard
on the right. The yellow exclamation point next to the package name is
for the warning at the top of the window.

The next three fields are pull downs for various SDK settings. The first
one is the lowest SDK version on which this app will run, which we can
leave at the default setting of Android 2.2. The next is the target SDK
against which the app will be tested. Since we created a virtual device
earlier targeting 2.3.3, this is what we pick here. The app will be
compiled with the latest version of the compiler, which is 4.2.

The last field is a color theme that will be applied to the application.
Again, we can leave it at the default.

All of these settings can be changed later - we'll see how after we
write up the app.

Clicking next takes you to another settings window, where you can leave
things as they are.

Clicking next again takes you to a window that can be used to choose a
launcher icon. This icon will appear when the user lists all apps on
their device. The default icon is the Android, which we will leave in
for this application. Note that the window shows several versions of the
icon, one for each of four screen resolutions: ldpi, mdpi, hdpi, and
xhdpi. If you were to make your own icon, you will need to make four
versions. Typically you would make one version, usually the mdpi, and
then scale it down or up for the other versions.

Clicking next presents a create activity window. You can leave the
selection at Blank Activity.

Clicking next asks for the name of the activity class to create. Enter
HelloWorld for the name, and main for the layout. Leave Navigation type
at the default setting of "None".

Click next. If you see a window about a missing dependency, click on the
"Install/Upgrade" button and carry out the installtion process.

Click Finish.

#### App Project

In the left hand pane is the package explorer where you see the
HelloWorld project. It has several folders, one of which is res (for
"resources"). Under res is a folder called layout, which holds an XML
file called main.xml. (Recall that we had named the layout "main" in the
project wizard's activity class window, toward the end of the previous
section.)

The editor is in the right pane, with the main.xml file open in
"Graphical Layout" form (see the tab at the bottom left corner of the
pane). This is pretty much what the app would look like when it's
launched. So let's go ahead and run the app, then we'll come back to
take a tour of the app's code, and some of the immediately relevant
aspects of the project's framework.

#### Running the App

Right click on the HelloWorld project folder name in the package
explorer, then choose "Run As", and "Android Application". This should
start up the emulator which we have created earlier, called "hvga". This
will take a few moments, and after the emulator starts running, it will
set itself up and eventually show the app, which is the leftmost picture
in the following set of images:

You may have noticed that the layout of the app while running in the
emulator is identical to the graphical layout of the main.xml layot file
shown in Eclipse.

The emulator provides basic navgiational capability, as well as a
hardware search button. The middle image above shows the home screen,
and the rightmost shows all the apps on the emulated device. (From where
the Hello World app can be launched, of course - observe the Android
icon used as the launcher icon, because we set it up that way in the
project creation process.)

April 22nd, 2013 - Recitation 12: Multithreading, Design Patterns
-----------------------------------------------------------------

1.  Suppose you use a search engine to search for a word or phrase that
    results in a match with a large number (hundreds) of web pages.
    However, the browser will only display a list of n (some variable
    parameter) page links in one screenful. Implement a multi-threaded
    program with one thread for the browser display, and another for the
    search engine, and have the search engine deal out hits in batches
    of the max size the browser can display in one screenful. You may
    assume that a method called fetch has already been written in the
    search engine to fetch the next batch of hits, returned as a list of
    URL strings.

        public class Searcher implements Runnable {
              private Request req;   // search request
              private Buffer buf;    // to store hits for display
              public Searcher(Request req, Buffer buf) {
                 this.req = req;
                 this.buf = buf;
                 new Thread(this).start();
              }
              public void run() {
                 while (true) {
                    while ((List hits = fetchNext(req)) != null)  { // more
              results from fetch
                       buf.put(hits);
                 }
              }
           }

           public class Displayer implements Runnable {
              private Buffer buf;
              public Displayer(Buffer buf) {
                 this.buf = buf;
                 new Thread(this).start();
              }
              public void run() {
                 while (true) {
                    display(buf.get());
                 }
              }
           }

           public class Buffer {
              List hits;
              boolean available = false;
              public synchronized void put(List hits) {
                 while (available) {
                    try {
                        wait();
                    }
                    catch (Exception e) { }
                 }
                 available = true;
                 this.hits = hits;
                 notifyAll();
              }

              public synchronized List get() {
                 while (!available) {
                    try {
                        wait();
                    }
                 catch (Exception e) { }
              }
              available = false;
              notifyAll();
              return hits;
           }

2.  In class you saw how one prime producer synchronized with one prime
    consumer. Rewrite the `PrimeCentral` class with appropriate
    synchronization to handle 3 producers and 1 consumer. For a given
    bound (max number up to which primes need to be computed), each
    producer will generate primes for a third of the range 2..bound.
    (So, for instance, if bound is 9000 then the first producer will
    generate primes between 2 and 3000, the second between 3001 and
    6000, and the third, between 6001 and 9000). The consumer should be
    able to get at any available prime in any of the three ranges. Make
    sure that you do not over-synchronize, i.e. if a consumer is trying
    to get at a prime in one of the ranges, a producers that may be
    attempting to put a prime in one of the other ranges should not be
    locked out.

3.  You are asked to implement an application that can plot graphs of
    mathematical functions, each function being of the form `y = f(x)`.
    While there may be a choice of functions that can be plotted, only
    one function is plotted at a time on a given 2-D screen.

    How would you use the `Template Method` design pattern to build your
    code? Write the outline of each class in your design, including
    relevant fields, constructors, and methods - pick any two specific
    mathematical functions to demonstrate the pattern.

    -   The abstract class hosting the template method (NOT abstract)
        and the hook method (abstract):

            public abstract class Plotter {

               ... // constructor and methods to set up and manage drawing objects

               public void draw(double[] xlist) { // template method, NOT abstract
                    ...  // set up graphing tools
                    for (int i=0; i < xlist.length; i++) {
                        double y = computeY(xlist[i]);
                    }
               }

               protected abstract double computeY(double x);   // hook method
            }

    -   A specific line plotter, using the function of the form
        `y = mx + b`

            public class LinePlotter extends Plotter {

               double slope, yIntercept;

               public LinePlotter(double double slope, double yIntercept) {
                   this.slope = slope; this.yIntercept = yIntercept;
               }      

               protected double computeY(double x) {  // implement hook 
                   return slope*x + yIntercept; 
               }
            }

April 26th, 2013 - Final Exam Study Guide
-----------------------------------------

### Object-Oriented Design with Java.

#### Interfaces

-   An abstract type that is used to specify an interface that clases
    must implement.
-   Declared using the `interface` keyword.
-   May contain method signature and constant declarations.
-   May not be instantiated.
-   *A class that implements and interface must implement all of the
    methods described in the interface or be an abstract class.*
-   Can be used to simulate multiple inheritance.
-   An interface can extend any number of interfaces.
-   An interface may not implement an interface.
-   An interface is *generally* public.
-   An interface defines a new type name that is tracked by the
    compiler.
-   All fields in an interface are implicity `public`, `static`, and
    `final`.
-   All methods in an interface are implicity `public` and `abstract`.
-   When a class implements an interface, it *must implement every
    single method* that is prescribed in the interface.
-   An interface may be generic.

        public interface Comparable<T> {
            int compareTo(T o);
        }

#### Inheritance

-   A class that derived from another class is called a *subclass*.
-   The class from which the subclass is derived is called the
    *superclass*.
-   Except for `Object`, which has no superclass, every class has one
    and one only direct superclass (single inheritance).
-   In the absence of any other explicit superclass, every class is
    implicitiy a subclass of `Object`.
    -   From `Object`, every Java class has, and you have likely seen,
        -   `equals()` - compares address of objects
        -   `toString()` - returns address of object
        -   `hashCode()` - returns the hash code value for object

-   The design aspect of inheritance is to model the "is a" relationship
    between objects.
    -   A car is a motor vehicle.
    -   A motor cycle is a motor vehicle.
    -   A colored point is a point.
    -   A zebra is an animal.

#### Abstract classes

-   An abstract class is a class that is declared by `abstract`.
-   It may or may not include abstract methods.
-   *Abstract classes may not be instantiated, but they can be
    subclassed.*
-   Unlike interfaces, abstract classes *may contain values that are not
    static and final*, and they *may contain implemented methods.*
-   When several classes have a common conceptual foundation they can be
    **generalized** into an `abstract` superclass.
-   In Java, a class is defined `abstract` in the class header.
-   An `abstract` method is one that has no implementation.
-   An `abstract` class may have *zero or more* `abstract` methods.

#### Polymorphism

-   The ability to create a variable, function, or object that has more
    than one form.
-   Used to implement a style of programming called *message-passing* in
    the literature.
-   Dynamically binding to same functionality in classes at different
    levels of an inheritance hierarchy using a "least common
    denominator" type is known as **inheritance polymorphism**.

### UML

-   UML stands for Unified Modeling Language, which is a mainly
    graphical notation used to express object-oriented design.
-   There are three kinds of UML diagrams that are most useful in
    practice:
    -   **Class interaction diagram**, used to show classes and the
        relationships between them.
    -   **Sequence diagram**, used to show sequences of activity when
        methods are invoked on classes.
    -   **State diagram**, used to represent state based designs.

#### Class diagrams

-   The class diagram is the main building block of OO modelling.
-   It is used both for general conceptual modelling and for
    systematics.
-   Classes contain three parts:
    1.  The upper part holds the name of the class
    2.  The middle part contains the attributes of the class.
    3.  The bottom part gives the methods or operations the class can
        take or undertake.

-   To specify the visibility of a class member, these are the notations
    used before the name:

        +   Public
        -   Private
        #   Protected
        ~   Package
        /   Derived
        _   Static

-   UML allows you to specify a relationship of class members using
    external links.

        Association:    --------+> // solid line,  filled triangle
        Aggregation:    -------<=> // solid line,  empty diamond
        Composition:    -------<+> // solid line,  filled diamond
        Generalization: --------|> // solid line,  empty triangle
        Dependancy:     - - - - |> // jagged line, empty triagnle 

-   To specific the multiplicity of an association of at least two
    related classes is done with the **multiplicity** entity, which is
    defined as follows:

        0..1    No instances, or one instance (optional, may)
        1       Exactly one instance
        0..*    Zero or more instances (also *)
        1..*    One or more instances (at least one)

##### Association

-   An *association* is a family of links.
-   They are representing with simply a line.
-   It can be named.
-   At the both ends of the line, the members can have role names.
-   The four types are bi-directional, uni-directional, aggregation, and
    reflexive. (The first two are the most common.)
-   *Association defines a relationship between classes of objects that
    allows one object instance to cause another to perform an action on
    its behalf.*
-   "Sending a message" or "invoking a method" or "calling a member
    function."
-   An "owns a" relationship.

        1     Owns     1..1
        ------------------>
        Owner        Owned

-   Directed associations happen when the `Owner`, in this case, knows
    about what it `Owns`, but the `Owned` does not "know" about its
    `Owner`.
-   At time, an association between two classes itself has properties,
    an **association class** is used to model these properties.
    -   This is represented by a jagged line stemming from where one
        might usually put the title of the association.

##### Aggregation

-   This differs from ordinary composition in that it does not imply
    ownership.
-   In composition, when the owning object is destroyed, so are the
    contained objects.
-   In aggregation, this is not *necessarily* true.
-   For example, if a University closes, the departments it owns, like
    Computer Science, will likely close along with it. On the other
    hand, the Professors and Students will still exist.
-   A "has a" relationship.
-   Represented with an empty diamond and a line, an unfilled diamond.

        Pond <=>-------------- Duck
                0..1      0..*

-   Good examples of aggregation are states aggregating counties that
    aggregate townships, police stations aggregate police officers, and
    directories aggregate files.

##### Composition

-   This is a stronger variant of the "owns a" relationship.
-   Composition usualy has a strong *life cycle dependancy* between
    instances of the container class and instances of the contained
    classes.
-   It is a way to combine simple objects into more complex ones.
-   Compositions are a criticle building block of basic data structures.
-   Example: An automobile is composed from objects including steering
    wheel, seat, gearbox, and engine.
-   Represented with a filled diamond.

        Car<+>----------Carburetor
              0..1  1..1

-   Alternatively, one can represent composition by nesting a class
    within the class representation.

##### Generalization

-   The generalization relationship ("is a") indicates that one of the
    two related classes is considered to be a specialized form of the
    other and a superclass is considered a generalization of the
    subclass.
-   It means that any instances of the subclass is also an instance of
    the superclass.
-   The generalization relationship is also known as the inheritance or
    "is a" relationship.
-   This is almost synomymous with interface implementation.
-   The representation in UML is a hollow triangle.

        Student ----------|> Person

-   A good example of generalization is shape is a generalization of a
    polygon, which is a generalization of rectangles and triangles.

##### Dependancy

-   Class `A` depends on `B` if `A` *uses* `B` in such a way that a
    change in `B` will effect `A`.
-   Say `A` depends on `B`. Typically, `B` would appear as a parameter,
    return type, or local variable in a method of `A`.

#### State diagram.

-   A state diagram is a type of diagram used in computer science and
    related fields to describe the behavior of systems.
    -   State diagrams require that the system described is composed of
        a finite number of states.
        -   Sometimes this is the case, in other there is a reasonable
            abstraction.

    -   Many forms of state diagrams exists, which different slight and
        have different semantics.

-   The state diagram in the Unified Modelling Language is essentially a
    Harel statechart with standardized notation.
    -   This can be used to describe many systems, from computer
        programs to business processors.
    -   In UML 2 the name has been changed to *State Machine Diagram*.

-   The basic notational elements that can be used to make a diagram
    are:
    -   Filled circle, pointing to the initial state.
    -   Hollow circle, containing a smaller filled circle indicating the
        final state.
    -   Rounded rectangle, denoting a state. Top of the rectagnle
        contains a name of the state.
        -   Can contain a horizaontal line in the middle, below which
            the activities that can be done are indicated.

    -   Arrow, denoting transtion. The name of the event (if any)
        causing this transition labels the arrow bodyu.
        -   A guard expression may be added before a "/" and enclosed in
            square-brackets. Ex: `eventName[guardExpression]`.
        -   If an action is performed during this transition, it is
            added to the label following a "/".

    -   Thick horizontal line with wither \$ x 1 \$ lines entering and 1
        line leaving or 1 line entering and *x* \> 1 lines leaving.
        -   These denote join/fork respectively.

### Design patterns

#### Model-View-Controller (MVC)

-   A **model** notifies its associated views and controllers when there
    has been a change in its state.
-   A **view** requests from the model the information that needs to
    generate an output representation to the user.
-   A **controller** can send commands to associated view to change the
    view's presentation of the model.

#### State (Behavioral)

-   Allow an object to change its behavior when its internal state
    changes.
-   *The "object" is a subclass of an abstract class, polymorphism.*
-   Context (client code) has a state object that is one of the concrete
    instances.
-   The request method executes handle on this concrete instance
    dynamically binding the appropriate class method.

        +-----------+          +-----------+
        |  Context  |<>--------|   State   |
        +-----------+          +-----------+
        | request() |          | handle()  |
        +-----------+          +-----------+
                |                     ^
                |                     |
        +--------------+       +------+--------+-- ...
        |state.handle()|       |               |
        +--------------+  +----------------+ +----------------+
                          |ConcreteState A | |ConcreteState B |
                          +----------------+ +----------------+
                          | handle()       | | handle()       |
                          +----------------+ +----------------+

-   Psuedocode

        class AbstractTool is
             function moveTo(point) is
                 input:  the location point the mouse moved to
                 (this function must be implemented by subclasses)

             function mouseDown(point) is   
                  input:  the location point the mouse is at
                  (this function must be implemented by subclasses) 

             function mouseUp(point) is
                  input:  the location point the mouse is at
                  (this function must be implemented by subclasses)

#### Singleton (Creational)

-   *Ensure that a class has only one object or instance.*
-   Only one point of global access.
-   The single private constructor ensures that an instance of the class
    cannot be created with `new`.

        +----------------------+
        |       Singleton      |
        +----------------------+
        |- Singleton()         |
        |+ static getInstance()|
        +----------------------+

#### Iterator

-   An iterator is *used to traverse a container and access the
    containter's elements.*
-   This *decouples algorithms from containers.*
-   The alogirthm `SearchForElement` can be implemented generally using
    a specific type of iterator rather than implementing
    container-specific algorithm.
-   This allows `SearchForElement` to be used on any container that
    supports the required type of iterator. \> Provide a way to access
    the elements of an aggregate object \> sequentially without exposing
    its underlying representation.

-   Java has an `Iterator` interface that the Collections should
    implement in order to traverse the collection.
-   Classic implementations were using the `next()` method.
-   Java also supports `hasNext()` and `remove()` methods.

        public interface Iterator<T> {
            boolean hasNext();
            T next();
            void remove();
        }

-   Access the contents of a collection without exposing its internal
    representation.
-   Suppoer overlapping multiple traversals.
-   Provide a uniform interface for traversing different collections.
-   Polymorphic iteration.

                              +-------------------+
                              |      Iterator     |
                              +-------------------+
                              |hasNext()          |
                              |next()             |
                              +-------------------+
                                         ^
                                         |
        +---------------+     +-------------------+
        |   Collection  |     | ConcreteIterator  |
        +---------------+     +-------------------+
        | itertator() o |---->|hasNext()          |
        +-------------|-+     |next()             |
                      |       +-------------------+
        +-------------|----------------+
        | return new ConcreteIterator()|
        +------------------------------+

#### Template Method

-   Implements a set sequence of actions
-   Each action is a method, some of which are abstract because their
    implementation is specific to concrete subclasses.
-   The abstract metods are referred to as "hook" methods.
-   *The template method is hosted in an abstract class.*
-   The template method itself is *not abstract*.
-   Each specific algorithm can then extend this abstract host class,
    and provide its own specific version of the hook method.

        +-------------------+   +--------+  
        |   Template Host   |   | . . .  |
        +-------------------+   | hook1()| // Note: This is the method
        | templateMethod() o----| . . .  | // and it is non-abstract
        | hook1()           |   | hook2()|
        | hook2()           |   | . . .  |
        +-------------------+   +--------+
            ^
            |
        +-------------------+
        |   ConcreteClass   |
        +-------------------+
        | hook1()           |
        | hook2()           |
        +-------------------+

-   In software engineering, the *template design pattern* is a
    behavioral design pattern that defines the program skeleton of an
    algorithm in a method, called the *template method*, which defers
    some steps to subclasses.
    -   It lets one redefine certain steps of an algorithm without
        changing the algorithms structure.

-   In the template method of this design pattern, one or more
    algorithms can be overridden by subclasses to allow differing
    behaviors enusuring that the overarching algorithm is still
    followed.
    -   In object-oriented programming, first a class is created that
        provides the basic steps of an algorithm design.
    -   These steps are implemented using abstract methods.
    -   Later on, subclasses change the abstract methods to implement
        real actions.
        -   Thus, the general algorithm is saved in one place but the
            concrete steps may be changed by subclasses.

-   The template method pattern thus manages the larger picture of task
    semantics, and more refined implementation details of selection and
    sequence of methods.
    -   This larger picture calls abstract and non-abstract methods for
        the task at hand.
    -   The non-abstract methods are completely controlled by the
        template method, but the abstract methods, implemented by
        subclasses, are implemented by the concrete subclasses.
        -   These are called "hooks"

    -   The template method is not abstract!

### Black-box Unit Testing

#### Boundary Value Analysis

-   Consider `charAt(i)` in the `String` class. This method implements a
    function that takes as input an integer position, and returns the
    character at that position in the string.
-   The range of input, *i*, where *s* is the length of the string:

    0 ≤ *i* ≤ *s* − 1

-   To test that `charAt` works correctly for a given string of length
    s, we would need to build the following input test cases
    -   Lower boundary value *i* = 0.
    -   Upper boundary value *i* = *s* − 1.
    -   A small increment on the lower boundary value, *i* = 1.
    -   A small decrement on the upper boundary value, *i* = *s* − 2.
    -   A nominal valye of *i* that is somewhere in the range that is
        not any of the above. \$i = \\frac{s}{2}\$

-   This is the basic **boundary value analysis** approach.
-   In general, if a function has an integer input *i*, which is between
    *l* and *h* in value, then the boundary analysis of the function
    selects the test input values *l*, *l* + *ε*, *l* + *ε*,
    *i*<sub>*n*</sub>, *h* − *ε*, and *h*, where:
    -   *i*<sub>*n*</sub> is a nominal value of *i* somewhere in the
        range.
    -   *ε* is a small value, typically 1 for `int`.

#### Robustness testing

-   A simple extension of the basic boundary value analysis that
    includes two additional input values: *l* − *ε* *h* + *ε*

-   These value fall outside the range but are class to the end value.
    -   They should result in the function implementation returning
        gracefully, without computing a result.

-   A Java method such as `charAt` would handle thes einputs by throwing
    an exception.
    -   It is graceful exit because it gives the client the choice to
        hangle this situation how they see fit.

-   The test cases with robust testing of `charAt` would be:
    −1, 0, 1, *s* / 2, *s*−2, *s*−1, *s*

-   Robustness testing uses seven test cases on a single-variable input
    function.
-   The main focus of robustness is on exception handling.

#### Multi-variable boundary values

-   Suppose you wrote a function `addHour` that, given a day and a time
    in hours, adds one hour to the time and outputs the resulting day
    and time.
-   The input variables here are integer `d`, for day, and an interger
    `h` for hour. Ranges:

    1 ≤ *d* ≤ 6 0 ≤ *h* ≤ 23

-   To create the test cases, we follow the procedure for single
    variable boundary value analysis, except we repret for both
    variables.
    -   When we run through the gamut for one variable, we keep the
        value of the other fixed at the nominal value.

-   Then the list of test cases using (day, hour)

    (*d*<sub>*n*</sub>, 0), (*d*<sub>*n*</sub>, 1), (*d*<sub>*n*</sub>, *h*<sub>*n*</sub>), (*d*<sub>*n*</sub>, 22), (*d*<sub>*n*</sub>, 23), 
    (1, *h*<sub>*n*</sub>), (2, *h*<sub>*n*</sub>), (*d*<sub>*n*</sub>, *h*<sub>*n*</sub>), (6, *h*<sub>*n*</sub>), (7, *h*<sub>*n*</sub>)
    -   One test appears twice, so there are 9 distinct cases.

-   For the numbers 4 and 12 for day and hour, there are nine distinct
    test cases:

    (4, 0), (4, 1), (4, 12), (4, 22), (4, 23), (1, 12), (2, 12), (6, 12), (7, 12)

-   Robustness testing yields four more test cases:

    (*d*<sub>*n*</sub>, −1), (*d*<sub>*n*</sub>, 24), (0, *h*<sub>*n*</sub>), (8, *h*<sub>*n*</sub>)

-   However, this general approach does not capture the important test
    cases (1, 23) and (7, 23) mentioned at the beginning of this
    discussion.
-   The reason the general approach followed above only works if the
    variables are *independant*.
    -   That is, if there are *n* independant variables, then the test
        cases are built by varying each indepedant variable thorugh all
        its test values while holding all the other variables at their
        respective nominal values.

-   If the variables are dependant on each other, then we need to use
    all value tuples obtained by combining the test values of the
    variables in all possible ways.
-   For the `addHour` examples, this would mean all possible combination
    of *d* boundary values with those of *h* boundary values.
-   The test values for *d* are 1, 2, 3, 4, 5, 6, 7 and those for *h*
    are 0, 1, 12, 22, 23.
    -   So there are 25 combinations, each of which will be a test case.

-   These combinations will include 1, 23 and 7, 23, among others.
-   Robustness testing does not get affected due to inter-dependance
    unless there are particular legitimate indivudual values whose
    combination is not legitimate.

#### Equivalence classes

-   Divides the input data of a software into partitions of equivilent
    data from which test cases can be derived.
-   In principle, test cases are designed to cover each partition at
    least once.
-   This technique tries to define test cases that uncover *classes of
    errors*.
-   Equivilence partitioning is typically applied to the inputs of a
    tested component.
    -   May be applied to outputs in rare cases.

-   The fundamental concept of ECP comes from equivilence class, which
    in turn comes from equivilence relation.

        int safe_add( int a, int b ) {
            int c = a + b;
            if ( a >= 0 && b >= 0 && c < 0 )
            {
                fprintf ( stderr, "Overflow!\n" );
            } 
            if ( a < 0 && b < 0 && c >= 0 )
            {
                fprintf ( stderr, "Underflow!\n" );
            } 
            return c;
        }

-   The boundary values approach results in a lot of test cases, many of
    which are repetitious or redundant.

        +------+---+---+
        | Test | d | h |
        +------+---+---+
        | 1    | 1 | 0 |
        | 2    | 1 | 1 |
        | 3    | 1 | 12|
        | 4    | 1 | 22|
        | 5    | 1 | 23|
        | 6    | 2 | 0 |
        | 7    | 2 | 1 |
        | .    | . | . |
        | .    | . | . |
        | .    | . | . |
        | 24   | 7 | 22|
        | 25   | 7 | 23|
        +------+---+---+

-   Consider each group of tests with the same *d* and different *h*'s.
    -   In the first group of 5 tests, with *d* = 1, all tests except
        the last result in the same type of input.

-   Why not break these into categories? All tests in each category
    would produce similar successes or failures.
    -   Category 1: All tests for which output *d* is same as input *d*.
    -   Category 2: All tests for which the output *d* is different from
        input *d*, but not 1.
    -   Category 3: All tests for which the output *d* is different from
        the input *d*, and is 1.

-   Each category is called an *equivilence class* and the cetgorization
    is called *equivilence partitioning*
    -   Equivilence partitioning can also be done for test cases that
        are expected to result in errors, for robustness testing.

-   Consider the example of a rectangle, where you have a method called
    `pointInRectangle`. It returns `0` if the point is *on* the
    rectangle, `-1` if the point is *not* on or in the rectangle, and
    `1` if it is *in* the rectangle.
    -   This function does not have a continuum of results, insteads it
        partitions the results into three calses of outcomes.
    -   This then leads to partitioning the input into equvilence
        classes.
    -   Each equivilence class would comprise all inputs that result in
        one of the possible outcomes, or force one type of error.
    -   Since we are assuming all inputs are legal coordinates, to start
        with, we will build equvilance classes for the possible correct
        outcomes.

### Multithreading and synchronization on shared resources

#### Multithreading I/0 with Computation

-   The steps to make a program multithreaded:
    1.  Extend the `java.lang.Thread` class.

            public class Program extends Thread { ... }

    2.  Place code you want to execute indepedantly in the `run` method

            public void run() { ... }

    3.  Make any parameters you need static fields.
    4.  Define a constructor that starts up an independant thread for
        run.

            public ProgramThread() { start(); }

        -   This method is defined in the `Thread` class, calling it
            sets up the necessary resources to run an independant thread
            and starts up the thread to execute the run method.

        > Note: Calling run directly (instead of start) will *not* start
        > an independant thread.

    5.  Change the main method to set up and independant thread for your
        computation. When the user interupts your program, report the
        current computation.

-   Every time the user hits enter, the main thread fetches the current
    status of your computation and prints it out.
-   Meanwhile, the program thread continues its computation.
-   If the user types "quit", the program thread continues indepedantly
    until the end of the current conditional or whatever might be
    happening in there.

#### Why threads

-   A thread runs asynchronously, independant of the thread that created
    it.
-   A Java application or applet itself runs as a thread, and can spin
    off as many threads as needed.
-   A collection of asyncrhously running threads may communicate with
    each other via a buffer, or directly invoking methods on each other.
-   Asynchrous computing allows several tasks to be performed in
    parallel, resulting in:
    -   **improved executing time** for the application as a whole.
    -   **improved turn around time** seen by the user, for instance the
        consumer thread displays data on the fly as it comes from the
        server, instead of blocking until all data is available.

-   Asynchrounous computing places more onus on the programmer to ensure
    that the program:
    -   **avoids race conditions**, two threads trying to update a
        variable at the same time.
    -   **maintains consistency of data**, two transactions both
        withdraw money from an account, but the second does not see the
        withdrawal being made by the first.

#### Lifecycle of a thread

A thread is born, started, run, and then terminated.

-   **New**: A new thread begins its life cycle in the new state. It
    remains in this state until the program starts the thread.
-   **Runnable**: After a newly born thread is started, the thread
    becomes runnable. It is executing a task.
-   **Waiting**: Sometimes a thread transitions to the waiting state
    while the thread waits for another thread to perform a task. A
    thread transitions back to the runnable state only when another
    thread signals the waiting thread to continue executing.
-   **Timed waiting**: A runnable thread can enter the timed waiting
    state for a specified interal of time. A thread in this state
    transitions back to the runnable state when that time interval
    expires or when the event it is waiting for occurs.
-   **Terminated**: A runnable thread enters the terminated state when
    it completes the task or is otherwise terminated.

#### Thread priorities

-   Every Java thread has a priority that helps the operating system
    determine the order in which threads are scheduled.
-   Java priorities are in the range between `MIN_PRIORITY` (1) and
    `MAX_PRIORITY` (10),
    -   By default, every thread is `NORM_PRIORITY` (5).

-   Threads with higher priority are more important to a program and
    should be allocated processor time before lower-priority threads,
    -   However, this is very platform dependant.

#### A thread "Hello, World!"

    class NewThread implements Runnable {
       Thread t;
       NewThread() {
          // Create a new, second thread
          t = new Thread(this, "Demo Thread");
          System.out.println("Child thread: " + t);
          t.start(); // Start the thread
       }

       // This is the entry point for the second thread.
       public void run() {
          try {
             for(int i = 5; i > 0; i--) {
                System.out.println("Child Thread: " + i);
                // Let the thread sleep for a while.
                Thread.sleep(500);
             }
         } catch (InterruptedException e) {
             System.out.println("Child interrupted.");
        }
         System.out.println("Exiting child thread.");
       }
    }

    public class ThreadDemo {
       public static void main(String args[]) {
          new NewThread(); // create a new thread
          try {
            for(int i = 5; i > 0; i--) {
              System.out.println("Main Thread: " + i);
               Thread.sleep(1000);
             }
          } catch (InterruptedException e) {
             System.out.println("Main thread interrupted.");
          }
          System.out.println("Main thread exiting.");
      }
    }

#### Recitation 9, Question 1

> Use threads to implement a stop watch that displays, once every five
> seconds, the minutes and seconds that have passed since it was
> started. The display should be in the form mm:ss for minutes and
> seconds. When the clock reaches 15 minutes, it should wrap back and
> start at 0 minutes and 0 seconds. The user should be able to stop the
> watch at any time. Write the complete code for the application. (Not
> the most accurate stop watch, but the model is useful for animations
> in which slight inaccuracies in time would not be detrimental.)

-   `Watch` class

        class Watch {
            int mins;
            int secs;

            String allStr;

            public Watch() {
                mins = 0;
                secs = 0;
                allStr = " 00:00";
            }

            public void stepUp() {
                secs = secs + 5;
                if (secs == 60) { 
                    mins = (mins + 1) % 60;
                    secs = 0;
                }
                if (mins >= 15) mins = mins - 15;
                String minsStr = String.valueOf(mins);
                String secsStr = String.valueOf(secs);

                if (mins < 10) minsStr = "0" + minsStr;
                if (secs < 10) secsStr = "0" + secsStr;

                allStr = " " + minsStr + ":" + secsStr;
                System.out.println(allStr);
            }

            public void reset() {
                mins = 0;
                secs = 0;
                allStr = " 00:00";
                System.out.println(allStr);
            }
        }

-   `StopWatchThread`

        class StopWatchThread  implements Runnable {
            private Watch w;
            public boolean quit = false;
            public boolean start = true;
            public boolean reset = false;
            public long startTime; 
            // delay is five second
            int delay = 5000;
            public void run() {
                startTime = System.currentTimeMillis();
                w = new Watch();
                // animation loop
                while (true) {
                    if (quit)
                        break;
                    if (reset) {
                        w.reset();
                        startTime = System.currentTimeMillis();
                        reset = false;
                    }
                    if (start) {
                        try {
                            startTime += delay;
                            Thread.sleep(Math.max(0, startTime - System.cu  rrentTimeMillis()));
                            w.stepUp();
                        } catch (InterruptedException e) {

                        }               
                    }

                }
            }
        }

#### Recitation 12, Question 1

> Suppose you use a search engine to search for a word or phrase that
> results in a match with a large number (hundreds) of web pages.
> However, the browser will only display a list of n (some variable
> parameter) page links in one screenful. Implement a multi-threaded
> program with one thread for the browser display, and another for the
> search engine, and have the search engine deal \> out hits in batches
> of the max size the browser can display in one screenful. \> You may
> assume that a method called fetch has already been written in the
> search engine to fetch the next batch of hits, returned as a list of
> URL strings.

    public class Searcher implements Runnable {
          private Request req;   // search request
          private Buffer buf;    // to store hits for display
          public Searcher(Request req, Buffer buf) {
             this.req = req;
             this.buf = buf;
             new Thread(this).start();
          }
          public void run() {
             while (true) {
                while ((List hits = fetchNext(req)) != null)  { // more
          results from fetch
                   buf.put(hits);
             }
          }
       }

       public class Displayer implements Runnable {
          private Buffer buf;
          public Displayer(Buffer buf) {
             this.buf = buf;
             new Thread(this).start();
          }
          public void run() {
             while (true) {
                display(buf.get());
             }
          }
       }

       public class Buffer {
          List hits;
          boolean available = false;
          public synchronized void put(List hits) {
             while (available) {
                try {
                    wait();
                }
                catch (Exception e) { }
             }
             available = true;
             this.hits = hits;
             notifyAll();
          }

          public synchronized List get() {
             while (!available) {
                try {
                    wait();
                }
             catch (Exception e) { }
          }
          available = false;
          notifyAll();
          return hits;
       }

May 6th, 2013 - Android Project: Chess OR Photo Album OR Roll Your Own
----------------------------------------------------------------------

You will continue working in pairs. You are allowed to roll your own
project (RYO) but if you choose to do so, you must get approval from
Prof. Venugopal.

### Photo Album

You are not required to carry over all the functionality from the Swing
implementation. Instead, you will implement a smaller set, as described
below. You may reuse any of the code from your GUI project.

Since the app will run on a personal smart phone, there is only a single
user, who is the owner of the phone. So there is no logging in, and no
admin functionality. Also, explicit captions are not required for photos
(the filename will stand for the caption). Dates are not required
either.

Your app should implement the following features:

-   30 pts Home screen. When the app comes up, it should load album and
    photo data from the previous session, if any, and list all albums.
    Off this "home" screen, you should be able to do the following, in
    one or more navigational steps.
-   40 pts Open, create, delete, and rename albums as listed in the GUI
    project description. When opening an album, display all its photos,
    with their thumbnail images.
-   40 pts Once an album is open, you should be able to add, remove, or
    display a photo. Displaying a photo could trigger a manual
    slideshow, allowing you to go backward or forward in the album one
    photo at a time.
-   20 pts When a photo is displayed, you should be able to add a tag to
    a photo. Only person and location are valid tag types; there are no
    typeless tags. You should also be able to delete a tag from a photo.
    Note: When displaying a photo, tags (if any) should be visible.
-   20 pts You should be able to move a photo from one album to another
-   50 pts You should be able to search for photos by tag (person or
    location), and matches should allow completion. For instance, if a
    location "New" is typed, matches should include photos taken in New
    York, New Mexico, New Zealand, etc. Note: You are not required to
    implement functionality to save the matching photos in an album.

You may serialize the albums and photos, but are not required to do so -
you can use alternative formats for storage on the device. Also, because
the user may switch out of your app to do other things (text, phone,
etc.) at any time, there is no single exit point. This means your app
must save any update to the device as soon as the update is made by the
user (*write persistence/write through*).

### Chess

Following up on the terminal-based Chess program, create an android app
that lets two people play chess with each other on the phone. You may
reuse any code from your chess assignment that you like. You have to
implement all the moves for all the pieces, determination of check, and
illegal moves (including any that puts the mover's King in check), but
you are not required to implement checkmate and stalemate.

Your app should have a Home activity that lets you choose from the
following three other activities:

#### Playing chess (120 pts)

-   30 pts Two humans can use your app to play a game of Chess.
-   20 pts Your app must draw the board with icons and correctly shaded
    squares.
-   20 pts Players must move their pieces using touch input - either
    dragging a piece or touching first the piece's original square and
    then its destination.
-   10 pts Provide an 'undo' button that will undo the last move (but no
    farther).
-   10 pts Provide an 'AI' button that will choose a move for the
    current player. Choosing randomly from the set of legal moves is
    sufficient.
-   20 pts Provide functional 'draw' and 'resign' buttons.
-   10 pts When the game is over, report the outcome (but not in a
    popup).

#### Recording games (50 pts)

-   20 pts Record all games as they're being played.
-   10 pts At the conclusion of a game, offer to store it and prompt the
    user for a game title.
-   20 pts List all recorded games, sorted by both date and by title
    (user can select which view to choose).

#### Game playback (30 pts)

-   A button that allows the user to play a selected game one move at a
    time.

