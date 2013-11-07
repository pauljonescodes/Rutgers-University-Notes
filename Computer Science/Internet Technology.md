Internet Technology <small>with John-Austen Francisco</small> {#internet-technology-with-john-austen-francisco}
=============================================================

Description {#description}
-----------

To provide a practical understanding of computer networks with respect
to system architectures, protocols, and client-server interaction. These
objectives are accomplished through extensive laboratory exercises.

### Topics {#topics}

-   Communication media;
    -   protocol layers,
    -   TCP/IP protocols,
    -   wireless protocols,
    -   high speed protocols,
    -   routing,
    -   and switching architectures.

-   Interprocess communication,
-   client-server interaction,
-   and socket programming.
-   Emerging trends and technologies such as:
    -   high speed asynchronous transfer mode (ATM) communication,
    -   wireless communication,
    -   and videoconferencing.

### Department Learning Goals {#department-learning-goals}

-   Computer Science majors ...
    -   will be prepared to contribute to a rapidly changing field by
        acquiring a thorough grounding in the core principles and
        foundations of computer science (e.g., techniques of program
        design, creation, and testing; key aspects of computer hardware;
        algorithmic principles).
    -   will acquire a deeper understanding on (elective) topics of more
        specialized interest, and be able to critically review, assess,
        and communicate current developments in the field.
    -   will be prepared for the next step in their careers, for
        example, by having done a research project (for those headed to
        graduate school), a programming project (for those going into
        the software industry), or some sort of business plan (for those
        going into startups).

Syllabus {#syllabus}
--------

### Instructor Info {#instructor-info}

-   **Instructor**: John-Austen Francisco
    -   **Office**: Room 335 (DATAMAN Lab), CoRE Building, Busch Campus
    -   **Phone**: (732) 445-6450 x9571
    -   **Email**: deymious@gmail.com
    -   **Office Hours**: Wednesdays 1530-1730

-   **Teaching Assistant**: Jeff Ames
    -   **Office**: Room 335 (DATAMAN Lab), CoRE Building, Busch Campus
    -   **Email**: jeff.ames@cs.rutgers.edu
    -   **Office Hours**: Wednesday 1300-1500

### Requirements {#requirements}

Students are expected to attend all lectures and perform all reading
assignments prior to lecture. Students will be evaluated according to
their performance on several course activities: classroom discussion,
programming assignments, mid-term examinations, and the final
examination. Programming projects will be assigned, and students are
required to complete them by the scheduled deadlines.

This course involves a very large, semester-long programming project,
and students should plan to spend 12-15 hours each week on the project,
depending on their programming ability. The project will be developed in
groups of 2-3 students, so it will be essential to have good
communication with your group partners. In addition, students needing
help outside of class should attend office hours, lab meetings, and
utilize the Discussion Board on Sakai to get additional assistance.

### Grading {#grading}

This course has 1 midterm exam, held during the normal lecture time, and
a cumulative final exam. There will be periodic homework assignments,
either online through Sakai or to be submitted before the beginning of
lectures. Finally, a course-long programming project, written in Java,
will introduce the concepts of network socket programming,
multi-threading, and protocol implementation.

<table class="table">
<tbody>
<tr>
<th markdown="1">
Assignment
</th>

<th markdown="1">
Weight
</th>
</tr>

<tr>
<td markdown="1">
Homework
</td>

<td markdown="1">
15%
</td>
</tr>

<tr>
<td markdown="1">
Midterm
</td>

<td markdown="1">
20%
</td>
</tr>

<tr>
<td markdown="1">
Final examination
</td>

<td markdown="1">
30%
</td>
</tr>

<tr>
<td markdown="1">
Project part 0
</td>

<td markdown="1">
10%
</td>
</tr>

<tr>
<td markdown="1">
Project part 1
</td>

<td markdown="1">
10%
</td>
</tr>

<tr>
<td markdown="1">
Project part 2
</td>

<td markdown="1">
15%
</td>
</tr>
</tbody>
</table>


### Important Dates {#important-dates}

<table class="table">
<tbody>
<tr>
<th markdown="1">
Date
</th>

<th markdown="1">
Event
</th>

<th markdown="1">
Notes
</th>
</tr>

<tr>
<td markdown="1">
7/15
</td>

<td markdown="1">
Project 0 Due
</td>

<td markdown="1">
Online submission through Sakai.
</td>
</tr>

<tr>
<td markdown="1">
7/17
</td>

<td markdown="1">
Midterm
</td>

<td markdown="1">
In-class exam.
</td>
</tr>

<tr>
<td markdown="1">
7/29
</td>

<td markdown="1">
Project 1 Due
</td>

<td markdown="1">
Online submission through Sakai.
</td>
</tr>

<tr>
<td markdown="1">
8/14
</td>

<td markdown="1">
Project 2 Due
</td>

<td markdown="1">
Online submission through Sakai.
</td>
</tr>

<tr>
<td markdown="1">
8/14
</td>

<td markdown="1">
Final Exam
</td>

<td markdown="1">
In-class exam.
</td>
</tr>
</tbody>
</table>

### Policy on Missed Examinations {#policy-on-missed-examinations}

You must have a pressing reason (such as a medical emergency or personal
crisis) to miss a scheduled mid-term or final examination. Make-up
examinations may be taken if you have notified the instructor at least
two weeks prior to the original examination that you will not be able to
attend. If you miss an examination due to an unforeseen emergency, you
may take a make-up examination only after providing written
documentation of an excuse that is acceptable to the instructor.

### Required Textbook {#required-textbook}

-   *Computer Networking*, 6th Edition
    -   **Authors**: James Kurose and Keith Ross
    -   **Publisher**: Addison Wesley
    -   **ISBN**: 0-13-285620-4

### Policy on Disability Accomodation {#policy-on-disability-accomodation}

Rutgers, the State University of New Jersey abides by the Americans with
Disabilities Act of 1990, the Americans with Disabilities Act Amendments
(ADAA) of 2008, and Sections 504 and 508 which mandate that reasonable
accommodations be provided for qualified students with disabilities and
accessibility of online information. If you have a disability and may
require some type of instructional and/or examination accommodation,
please contact me early in the semester so that I can provide or
facilitate in providing accommodations you may need.

If you have not already done so, you will need to register with the
Office of Disability Services, the designated office on campus to
provide services and administer exams with accommodations for students
with disabilities. The Office of Disability Services is located in Lucy
Stone Hall, Livingston Campus, 54 Joyce Kilmer Ave., Suite A145, phone
number 848-445-6800. I look forward to talking with you soon to learn
how I may be helpful in enhancing your academic success in this course.

June 24th, 2013 <small>Lecture: Socket Programming</small> {#june-24th-2013-lecture-socket-programming}
----------------------------------------------------------

-   What is a socket? An interface
    -   Transport level
    -   An interface from one machine to another.
    -   If you're going through the internet, you have ISP.
    -   If you're sending something, it's sockets.

-   When do you use one?
    -   Client sends a request
    -   Server interprets them
    -   Sends a response, webpage

-   How it works:
    1.  Client initiates connect, connection accpeted

    -   Connection is set up
    -   Send request, request received ..., send reponse
    -   Receive response

-   In "Java-ese"

        ServerSocket welcomeSocket = new ServerSocket(9000);
        // No one else can use this
        Socket connectionSocket = welcomeSocket.accept();
        // Blocking call (BOOM ... you stop.)

-   The `Java.net.Socket` class

        public InputStream getInputStream();
        // Returns an input stream for this socket

        public OutputStreem getOutputStream();
        // Returns an output stream for this socket

-   Wrapper class simplify the I/O

        DataOutputStream outToServer = new DataOutputStream(
                                        clientSocket.getOutputStream());

        DataInputStream outToServer = new DataInputStream(
                                        clientSocket.getOutputStream());

        outToServer.writeBytes("Hello, World!");

-   Close your socket, when you're done, exception code, catch and
    close!
    -   It can only help.

June 26th, 2013 <small>Recitation</small> {#june-26th-2013-recitation}
-----------------------------------------

### Threading and concurrency {#threading-and-concurrency}

-   When you run an application on your machine, on the OS level that is
    represented by a process.
    -   If I'm running Chrome, that's a process.
    -   There's only ever one process running.
    -   There's usually an interface for having multiple threads.

-   Lets say I'm writing a chat application.

        while (1) {
            inFromServer.readline();
            outToServer.writeBytes(msg + '\n');
        }

    -   This only allows for conversation where one person talks, then
        the other talks, then the other.
        -   This is odd.

    -   Whenever there is a message from either person, it'd be great to
        have that done on a seperate thread.
        -   You can also imagine you get a connection from a client, and
            you can send back some data, but 100 clients that also want
            to connect.
        -   A lot of servers have a feature where they're listening for
            new connections and for every new one, it spins a new
            thread.

-   Synchronization can be done with locks

        lock L;
            temp = a;
            temp = temp + 1;
            a = temp;
        unlock L; // allows others to start now

    -   There is a way to make an entire function synchronized, and,
        well, it's with the word `synchronized` in the method name after
        public.
    -   But you can also synchronize on a variable.

            public void increment() {

                synchronize(this) {

                    temp = a;
                    temp = temp + 1;
                    a = temp;
                }

                updateUI();
            }

-   There are some stipulations on locks
    -   Thread 1:

            lock A; // (1) executes, succeeds, switch
            lock B; // (3 .. ?) executes, fails, switch

            a = 2;
            b = 1;

    -   Thread 2:

            lock B; // (2) executes, succeeds, switch 
            lock A; // (4 .. ?) executes, fails, switch

            b = 1;
            a = 2;

June 26th, 2013 <small>Lecture: Network Switching Techniques</small> {#june-26th-2013-lecture-network-switching-techniques}
--------------------------------------------------------------------

-   Core networks are run by ISP
-   There are the big ones, medium ones, and small ones.
-   ISPs connect to ISPs
-   A packet has to pass through your local ISP, your Tier 3, Tier 2
    ISP, and finally to the root. Then back again.
    -   Seven used to be average, now 14.
    -   At Rutgers it's like 2-3.

-   Switch schemes:
    1.  Circuit switching
        -   A lot like a telephone network
        -   End-end resource reserved for transmission.
        -   Sounds like TCP, set up all resources before hand.
        -   Steps:
            1.  Control message sets up a path from origin to dest.
            2.  Return signal informs source that data transmission may
                proceed.
            3.  Data transmission begins.
            4.  Entire path remains allocated to the transmission
                (whether used or not).
            5.  When transmission is complete, source relerases the
                circuit.

    2.  Message switching
        -   Sends the whole peice of data into the ISPs.

    3.  Packet switching
        -   Messages are split into smaller pieces called packets.
        -   These packets are numbered and addressed and sent through
            the network one at a time.
        -   Allows pipelining.
        -   **Overlap sending**

-   Header overhead

        Circuit < Message < Packet

-   Transmission delay
    -   Short bursty messages

            Packet < Message < Circuit

    -   Long continuous messages

            Circuit < Message < Packet

June 30th, 2013 <small>Reading: <em>Chapter 1, Computer Networks and the Internet</em></small> {#june-30th-2013-reading-chapter-1-computer-networks-and-the-internet}
----------------------------------------------------------------------------------------------

### A Nuts-and-Bolts Description {#a-nuts-and-bolts-description}

-   The Internet is a computer network that interconnects hundreds of
    millions of computers.
    -   These use to be desktops
    -   All devices that are hooked up to the Internet are called
        **hosts** or **end systems**.

-   End systems are connected by a network of **communication links**
    and **packet switches**.
    -   Different links can transmit data at different rates, with the
        **transmission rate** of a link measured in bits per second.
    -   The resulting packages of information are known as **packets**.
        -   These are taken apart and reassembeled during this process.

-   Packet switches come in many shapes and flavors, the two most
    prominent bing **routers** and **link-layer switches**.
    -   **Link-layer switches** are typically used to access networks.
    -   **Routers** are using in the network core.
    -   The sequence of communication layers that information goes
        through to reach the end system is known as the **route** or
        **path**.

-   End system access to the internet is thourugh
    <abbr title="Internet Service Providers">ISPs</abbr>.
-   End systems, packet switches, and other pieces of the Internet run
    **protocols** that control the sending and receiving of information
    within in the Internet.
    -   The <abbr title="Transmission Control Protocol">TCP</abbr> and
        the <abbr title="Internet Protocol">IP</abbr> are two of the
        most important protocols on the Internet.
        -   IP protocol specifies the format of the packets that are
            sent and recieved among routers and other end systems.
        -   The Internet's pirncipal protocols are collectively known as
            **TCP/IP**.

### A Services Description {#a-services-description}

-   We can describe the Internet from an entirely different angle, that
    it's *an infrastructure that provides services to applications*.
    -   For example, here are some **distributed applications**,
        -   Email
        -   Web surfing
        -   Social networks
        -   Instant messaging
        -   <abbr title = "Peer to peer">P2P</abbr> file-sharing
        -   TV on the Internet
        -   Remote loging

-   End systems attached to the Intenet provide
    \*\*<abbr title="Application
                Programming Interfaces">APIs</abbr> that specify how a
    program on one end system asks the Internet infrastucture to deliver
    data to a specific destination.

### What Is a Protocol? {#what-is-a-protocol}

> A **protocol** defines the format and the order of messages exchanged
> between two or more communicating entities, as well as the actions
> taken on the trans- mission and/or receipt of a message or other
> event.

### The Network Edge {#the-network-edge}

-   Hosts are grouped into two categories:
    -   **Clients**, which tend to be desktops, mobile PCs, smartphones,
        etc.
    -   **Servers**, which tend to be more powerful machines that store
        and distribute Web pages, stream video, relay email, etc.
    -   **Data centers** have possibly thousands of servers.

#### Access Networks <small>Home Access: DSL, Cable, FTTH, Dial-Up and Stellite</small> {#access-networks-home-access-dsl-cable-ftth-dial-up-and-stellite}

-   <abbr title="Digital subscriber line">DSL</abbr> and cable are the
    two most prevelant types of broadband.
-   **Cable Internet access** makes use of cable television's existing
    cable television infrastructure.
-   <abbr title="Fiber to the home">FTTH</abbr> is growing.

### Physical media {#physical-media}

-   For each transmitter-receiver pain, a bit is sent by propagating
    electromagnetic waves or optical pulses across a **physical
    medium**. These have two categories:
    -   **Guided media**, which the waves are guided along a solid
        medium, such as:
        -   Fiber-optic cable
        -   Twisted-pair copper wire
        -   Coaxial cable

    -   **Unguided media**, where the waves propogate in the atmosphere
        and in outer-space, such as wireless LAN or a digital satellite
        channel.

#### Twisted-Pair Copper Wire {#twisted-pair-copper-wire}

-   This is the least expensive and most commonly used transmission
    medium.
    -   For hundreds of years, it has been used for telephones.
    -   99 percet of wired connections use twisted-pair copper wire.

-   <abbr title="Unshielded twisted pair">UTP</abbr> is commonly used
    for computer netowkrs withing a building, for LAN.

#### Coaxial Cable {#coaxial-cable}

-   Like twisted pair, coaxial consists of two copper conductors.
    -   But they're concentric rather than parallel.
    -   Used for television.

-   Coaxial cable can be used as a guided **shared medium**.
    -   A number of end systems can be connected directly to the cable.
    -   With each end receiving whatever is sent by the other end
        system.

#### Fiber Optics {#fiber-optics}

-   Thin, flexible medium that conducts pulses of light, each pulse
    representing a bit.
-   Long distance communication uses this.

### The Network Core {#the-network-core}

#### Packet Switching {#packet-switching}

-   End systems enchange **messages** with each other.
    -   These contain anything the application designer wants.
    -   To send a message from source end systems to destination end
        systems, the source breaks long messages into smaller chunks of
        data known as **packets**.
    -   **Packet switches** are where the information travels tbhrough.
        There are:
        -   **Routers**
        -   **Link-layer switches**

July 1st, 2013 <small>Assessment <em>Chapter 1</em></small> {#july-1st-2013-assessment-chapter-1}
-----------------------------------------------------------

### Question 1 <small>(5 points)</small> {#question-1-5-points}

> Write out the canonical OSI 7-layer stack from highest to lowest:

-   Layer 7: **Application**
-   Layer 6: **Presentation**
-   Layer 5: **Session**
-   Layer 4: **Transport**
-   Layer 3: **Network**
-   Layer 2: **Link**
-   Layer 1: **Physical**

### Question 2 <small>(5 points)</small> {#question-2-5-points}

> Consider an application that transmits data at a steady rate (for
> example, the sender generates an *N*-bit unit of data every *k* time
> units, where *k* is small and fixed). Also, when such an application
> starts, it will continue running for a relatively long period of time.
> Answer the following questions, briefly justifying your answer:

1.  Would a **packet-switched network** or a **circuit-switched
    network** be more appropriate for this application? Why?
    -   The benefit of using a packet-switched network for this
        application would be that it is inherently packet-based. Packets
        are fixed units of data.
    -   The benefit of using a circuit-switched network for this
        application would be that you wouldn't have the overhead of
        packet headers for each piece of data, which is small.
    -   The downside of using a packet-switched network would be exactly
        that, that because the data is sent very, very often, you have
        the overhead of a packet for each transmission.
    -   The downside of using a circuit-switched network is that there
        expensive up-front, because you actually have to establish a
        circuit between both locations you want to transmit data from,
        but you benefit from this if an application is truly
        long-running.
    -   Assuming that this is a long-running application and the
        organizer has enough funds, circuit based switching would be a
        better choice because you pay the cost once to establish a
        connection between the two nodes and you can then transmit all
        the data instantly for as long as you want. For example,
        landlines are exactly what this problem describes, and landlines
        use circuit-based switching. Furthermore, packet-based switching
        to optimize utilization of available link capacity, which is
        this case, it wouldn't fully utilize because of the small nature
        of the packets. If the information could be assumed to be larger
        and fewer between, packets would be perfect. Because the
        information is small and often, and with the assumption that it
        is possible to set up a dedicated circuit, circuit switching is
        a better idea.

2.  Suppose that a packet-switched network is used and the only traffic
    in this network comes from such applications as described above.
    Furthermore, assume that the sum of the application data rates is
    less than the capacities of each and every link. Is some form of
    congestion control needed? Why?

    -   Network congestion is what happens when there are so many
        requests for service put out that the queue is flooded and the
        quality of the connection suffers as a result. If
        packet-switched networking was implemented for a steady rate
        data stream with a short time regeneration, then yes,
        absolutely, you could use your knowledge in advance of
        application to implement congestion control. Furthermore, it
        would be wise to do it. Yes.

### Question 3 <small>(7 points)</small> {#question-3-7-points}

-   **Offline Application**: Runs as an application on the local host
    (computer), and does not require network access for its' primary
    functionality.
-   **Utilizes Network Access**: Runs as an application on the local
    host (computer) but uses the network for basic functionality.
-   **Software as a Service (SaaS)/Cloud Application**: Applications
    that operate either as a web service or otherwise run completely
    remotely on a computer other than the local host.

<table class="table">
<tbody>
    <tr>
        <th></th>
        <th markdown="1">
Offline Application
</th>
        <th markdown="1">
Utilizes Network Access
</th>
        <th markdown="1">
Software as a Service/Cloud Application
</th>
    </tr>
    <tr>
        <td markdown="1">
Google Maps
</td>
        <td></td>
        <td></td>
        <td markdown="1">
<i class="icon-ok"></i>
</td>
    </tr>
    <tr>
        <td markdown="1">
Bittorrent
</td>
        <td></td>
        <td markdown="1">
<i class="icon-ok"></i>
</td>
        <td></td>
    </tr>
    <tr>
        <td markdown="1">
Microsoft Office
</td>
        <td markdown="1">
<i class="icon-ok"></i>
</td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td markdown="1">
Mozilla Firefox
</td>
        <td></td>
        <td markdown="1">
<i class="icon-ok"></i>
</td>
        <td></td>
    </tr>
    <tr>
        <td markdown="1">
Solitaire
</td>
        <td markdown="1">
<i class="icon-ok"></i>
</td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td markdown="1">
Adobe Photoshop
</td>
        <td markdown="1">
<i class="icon-ok"></i>
</td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td markdown="1">
Yahoo! Mail
</td>
        <td></td>
        <td></td>
        <td markdown="1">
<i class="icon-ok">
</td>
    </tr>
</tbody>
</table>

### Question 4 <small>(3 points)</small> {#question-4-3-points}

The network core is defined as:

1.  The technicians and administrators in charge of the network's
    computers.
2.  The collection of routers, switches, and network links responsible
    for routing packets from host to host.<i class="icon-ok"></i>  
3.  The collection of web servers, email servers, and personal computers
    connected to the network.
4.  The telecommunication (telecom) companies responsible for the
    majority of the packet routing performed in the network.

### Question 5 <small>(10 points)</small> {#question-5-10-points}

> In this problem we consider sending real-time voice from Host A to
> Host B over a packet-switched network (VoIP). Host A converts analog
> voice to a digital 64kbps bit stream on the fly. Host A then groups
> the bits into 56-byte packets. There is one link between Host A and
> Host B; its transmission rate is 2 Mbps and its propagation delay is
> 10msec. As soon as Host A gathers a packet, it sends it to Host B. As
> soon as Host B receives an entire packet, it converts the packet's
> bits to an analog signal. How much time elapses from the time a bit is
> created (from the original analog signal at Host A) until the bit is
> decoded (as part of the analog signal at Host B)?

-   The analog data is digitized at 64kbps, and Host A will need to
    capture 56 bytes (448 bits) of data. 448/64,000 = .007 so this will
    take 7 msec.
-   Next, the 448-bit packet must be transmitted onto the link at 2
    Mbps. This will take an additional .224 msec (448/2,000,000 =
    .000224). So far it has taken 7.224 msec.
-   The last bit of the packet will arrive 10 msec later, bringing the
    total to 17.224 msec from analog to analog.

July 1st, 2013 <small>Homework: <em>Simple Socket Programming</em></small> {#july-1st-2013-homework-simple-socket-programming}
--------------------------------------------------------------------------

### Overview {#overview}

For this assignment you will need to create a simple network client that
communicates with an "echo" server.  The echo server will accept your
incoming socket connection, read a line from your client, and send the
line back to the client.  This assignment is intended as a very simple
primer to get you familiar with the concepts of network hosts, TCP
sockets, and ports.  Keep in mind that one third (30%) of your grade is
related to your source code, so make sure to create comments and use
small, well-defined methods when appropriate.

This assignment is expected to take around **2 hours** to complete,
though it may take more or less time depending on your abilities and
background. 

It is due **before class** on Monday, 1 July. You must submit via the
Sakai Assignments 2 tool.  Only on-time assignments submitted through
Sakai will be accepted.

### Specifics of Operation {#specifics-of-operation}

Your program MUST be completely contained in a file called
"EchoClient.java" without any Java packaging. This means that compiling
and running your program will be identical to the output below:

    javac -cp . EchoClient.java
    java -cp . EchoClient myhost.mydomain.com 3456

If you are unfamiliar with the concepts of Java packages or classpaths,
you should see the instructor during recitation or office hours. Within
your class, you should create multiple methods in addition to the
`static main(String[])` method. An example skeleton class has been
provided to assist you, though you do not need to use this file as long
as your class has the same name (`EchoClient`). To successfully complete
this assignment, your program must do the following:

1.  Accept the echo server hostname/IP address as `args[0]` and the port
    as `args[1]` in the main method.  The port should be parsed into an
    int or `Integer`.
2.  Construct a socket connected to the echo server based on the
    hostname/port specified in the command-line arguments.
3.  Read a single line of text from System.in and send it to the echo
    server including any newline characters (CR/LF).
4.  Read a single line response from the echo server and print it to
    System.out.
5.  Close the Socket to the echo server and any IOStreams that you may
    have opened during the program's lifetime.
6.  Exit your program.  At no point in your application should you call
    `System.exit(int)`.

Two resources are available to you: an example outline of a client and a
JAR archive containing an appropriate echo server.  The client example
is only an example, and you do not need to use it when coding.  In fact,
it will be better in the long run if you design your client from
scratch.  The JAR is executable using the following command:

    java -jar echo-server-1.0.0.jar 1234

In this case, "1234" is the port number for the server to listen on. You
may choose any port you wish, but be aware that ports below 1024 are
reserved for the "root" user in most operating systems.  To use the port
in the client example above (3456) you would execute:

    java -jar echo-server-1.0.0.jar 3456

### Grading Outline {#grading-outline}

-   Source code organization and comments: 30%
-   Reading command-line parameters: 10%
-   Establishing socket to the server based on parameters: 20%
-   Reading user input and sending it to the server: 15%
-   Reading server response and printing it to the user: 15%
-   Closing all Sockets/IOStreams before exit: 10%

### Hints and Suggestions {#hints-and-suggestions}

If this is your first time working directly with Sockets, IOStreams, and
Strings, you may find the following classes/resources helpful:

-   [Java Tutorials Lesson: Basic
    I/O](http://docs.oracle.com/javase/tutorial/essential/io/)
    (oracle.com)
-   [I/O From the Command
    Line](http://docs.oracle.com/javase/tutorial/essential/io/cl.html)
    (oracle.com)
-   [Java Tutorials Lesson: All About
    Sockets](http://docs.oracle.com/javase/tutorial/networking/sockets/)
    (oracle.com)
-   [Reading from and Writing to a
    Socket](http://docs.oracle.com/javase/tutorial/networking/sockets/readingWriting.html)
    (oracle.com)

July 1st, 2013 <small>Project \#0</small> {#july-1st-2013-project-0}
-----------------------------------------

### Updates {#updates}

Before jumping into the project I would like to mention one thing. Most
of the time your first attempt at a software project is either too slow,
too buggy, or is difficult to maintain/expand. Be prepared to throw away
the first versions of most of your code. You can even plan to have them
as throw-aways. You don't waste time doing this because you learn where
you can make improvements in your final version.

### Theory of Operation {#theory-of-operation}

In this project, you will build a simple BitTorrent(BT) client which
will serve as the foundation for a fully-featured BT client you will
build in later assignments. For project 1, your client will load a
.torrent file, interface with a tracker and a single peer and will
download a single file (JPEG) from that peer. When the file is finished
downloading, you will save it to the hard disk. All communication will
be done over TCP.

The file your program will read in is a .torrent file containing
metadata for the file to be downloaded.

### Assignment Specifics {#assignment-specifics}

Your assignment should basically do the following:

1.  Take as a command-line argument the name of the .torrent file to be
    loaded and the name of the file to save the data to. For example:

        java -cp . RUBTClient somefile.torrent picture.jpg

2.  Open the .torrent file and parse the data inside. You may use
    the `Bencoder2.java` class to decode the data.
3.  Send an HTTP GET request to the tracker at the IP address and port
    specified by the TorrentFile object. The java.net.URL class is very
    useful for this.
4.  Capture the response from the tracker and decode it in order to get
    the list of peers. From this list of peers, use only the peer at IP
    address 128.6.171.3. You must extract this IP from the list,
    hard-coding it is not acceptable.
5.  Open a TCP socket on the local machine and contact the peer using
    the BT peer protocol and request a piece of the file.
6.  Download the piece of the file and verify its SHA-1 hash against the
    hash stored in the metadata file. The first time you begin the
    download, you need to contact the tracker and let it know you are
    starting to download.
7.  After a piece is downloaded and verified, the peer is notified that
    you have completed the piece.
8.  Repeat steps 5-7 (using the same TCP connection) for the rest of the
    file.
9.  When the file is finished, you must contact the tracker and send it
    the completed event and properly close all TCP connections
10. Save the file to the hard disk according to the second command-line
    argument.

### Files Available {#files-available}

There are several files available in the Resources section of the site
in the folder "Project files."  The most important is the "Project 1
torrent file" (project1.torrent), which is the "testbed" torrent you can
use to develop your client.  The other files available are helpful, but
not necessary.  Be sure to check the resources section for updates or
changes as the semester progresses.

### Programming Style {#programming-style}

Writing maintainable code is just as important as writing correct code.
Consequently, you will be graded on your style. Below is a list of
suggestions to make your code easier to understand and maintain:

-   Comments - Comments for variables and for sections of code that do
    not have an obvious purpose. Please do not comment obvious
    statements or sections of code. For example,

        int i = 0;  //i is an integer and the initial value is 0        

    is not useful and unnecessarily clutters the code.

-   Naming - Names of classes, methods, and variables should be
    descriptive. For example, if a class has a field containing its hash
    value, naming the field hash\_value is much better than naming
    it hv .
-   Exceptions - Catch exceptions and do something useful with them. For
    example, print a statement describing what went wrong to System.err.
-   Easy to understand loops/recursion. When possible, it's best to
    avoid break statements whenever possible. When using recursion,
    tail-recursion is often preferable because "smart" compilers can
    often translate it into a loop.
-   Efficiency - Avoid being terribly inefficient. For example, if you
    have to sort 10M objects, it's better to sort them with
    a O(n\*lg(n)) algorithm than a O(n<sup>2</sup>) algorithm.
-   Encapsulation - Encapsulation is a useful feature of object-oriented
    languages, and so you should try to write classes that expose as
    little as possible. This way you can change the implementation of a
    class without affecting the rest of your program.

### Bencoding (Pronounced "Bee Encoding") {#bencoding-pronounced-bee-encoding}

Bencoding a method of encoding binary data. Tracker responses, and
interpeer communication will be bencoded. Below is how data types are
bencoded according to the BT protocol. [The following list is taken
from[http://www.bittorrent.org/beps/bep\_0003.html ](http://www.bittorrent.org/beps/bep_0003.html)]

-   Strings are length-prefixed base-10 followed by a colon and the
    string. They are encoded in UTF-8. For example 4:spam corresponds to
    'spam'.
-   Integers are represented by an 'i' followed by the number in ASCII
    base-10 followed by an 'e'. For example i3e corresponds to 3 and
    i-3e corresponds to -3. Integers have no size limitation. i-0e is
    invalid. All encodings with a leading zero, such as i03e, are
    invalid, other than i0e, which of course corresponds to 0.
-   Lists are encoded as an 'l' followed by their elements (also
    bencoded) followed by an 'e'. For example, l4:spam4:eggse
    corresponds to ['spam', 'eggs'].
-   Dictionaries are encoded as a 'd' followed by a list of alternating
    keys and their corresponding values followed by an 'e'. For example,
    d3:cow3:moo4:spam4:eggse corresponds to {'cow':'moo', 'spam':'eggs'}
    and d4:spaml1:a1:bee corresponds to {'spam': ['a', 'b']}. Keys must
    be strings and appear in sorted order (sorted as raw strings, not
    alphanumerics).

### Communication With the Tracker {#communication-with-the-tracker}

Your client must take the information supplied by the metadata file and
use it to communicate with the tracker. The tracker's IP address and
port number must be extracted from the metainfo dictionary, and your
program must then contact the tracker. Your program will send an HTTP
GET request to the tracker with the following key/value pairs. Note that
these are NOT bencoded, but must be properly escaped [this list is taken
from[http://www.bittorrent.org/beps/bep\_0003.html ](http://www.bittorrent.org/beps/bep_0003.html)]:

-   `info_hash` - The 20 byte(160-bit) SHA1 hash of the bencoded form of
    the info value from the metainfo file. This value will almost
    certainly have to be escaped.
-   `peer_id` - A string of length 20 which this downloader uses as its
    id. Each downloader generates its own id at random at the start of a
    new download. This value will almost certainly have to be escaped.
    You peer ID must NOT start with RUBT.
-   `port` - The port number this peer is listening on. Common behavior
    is for a downloader to try to listen on port 6881 and if that port
    is taken try 6882, then 6883, etc. and give up after 6889.
-   `uploaded` - The total amount uploaded so far, encoded in base-10
    ascii.
-   `downloaded` - The total amount downloaded so far, encoded in
    base-10 ascii.
-   `left` - The number of bytes this peer still has to downloaded,
    encoded in base-10 ascii. This key is important - If you do not
    specify how much you have left to download, the tracker assumes you
    are a seed and will not return any seeds in the peer list.
-   `event` - This is an optional key which maps
    to started , completed , or stopped (or empty , which is the same as
    not being present. If not present, this is one of the announcements
    done at regular intervals. An announcement using started is sent
    when a download first begins, and one using completed is sent when
    the download is complete. No completed is sent if the file was
    complete when started. Downloaders send an announcement
    using stopped when they cease downloading.

The response from the tracker is a bencoded dictionary and contains two
keys:

-   `interval` - Maps to the number of seconds the downloader should
    wait between regular rerequests.
-   `peers` - Maps to a list of dictionaries corresponding to peers,
    each of which contains the keys peer id , ip , and port , which map
    to the peer's self-selected ID, IP address or dns name as a string,
    and port number, respectively.

### Communicating With the Peer {#communicating-with-the-peer}

Handshaking between peers begins with byte nineteen followed by the
string 'BitTorrent protocol'. After the fixed headers are 8 reserved
bytes which are set to 0. Next is the 20-byte SHA-1 hash of the bencoded
form of the info value from the metainfo (.torrent) file. The next
20-bytes are the peer id generated by the client. The info\_hash should
be the same as sent to the tracker, and the peer\_id is the same as sent
to the tracker. If the info\_hash is different between two peers, then
the connection is dropped.

-   All integers are encoded as 4-bytes big-endian (e.g. 1,234 should be
    encoded as (hex) `00 00 04 d2`).
-   The `peer_id` should be randomly-generated for each process your
    program generates. (Meaning that it should probably change in some
    way each time the client is run.)  Stick to alphanumerics for easier
    debugging.

After the handshake, messages between peers take the form
of `<length prefix><message ID><payload>`, where length prefix is a
4-byte big-endian value and message ID is a single byte. The payload
depends on the message. Please consult either of the BT-related
resources for detailed information describing these messages. Below is a
list of messages that need to be implemented in the project.

-   keep-alive: `<length prefix>` is 0. There is no message ID and no
    payload. These should be sent around once every 2 minutes to prevent
    peers from closing connections. These only need to be sent if no
    other messages are sent within a 2-minute interval.
-   choke: `<length prefix>` is 1 and message ID is 0. There is no
    payload.
-   unchoke: `<length prefix>` is 1 and the message ID is 1. There is no
    payload.
-   interested: `<length prefix>` is 1 and message ID is 2. There is no
    payload.
-   uninterested: `<length prefix>` is 1 and message ID is 3. There is
    no payload.
-   have: `<length prefix>` is 5 and message ID is 4. The payload is a
    zero-based index of the piece that has just been downloaded and
    verified.
-   request: `<length prefix>` is 13 and message ID is 6. The payload is
    as follows:

        <index><begin><length> 

    Where `<index>` is an integer specifying the zero-based piece
    index, `<begin>` is an integer specifying the zero-based byte offset
    within the piece, and `<length>` is the integer specifying the
    requested length.`<length>` is typically 2\^14 (16384) bytes. A
    smaller piece should only be used if the piece length is not
    divisible by 16384. A peer may close the connection if a block
    larger than 2\^14 bytes is requested.
-   piece: `<length prefix>` is 9+X and message ID is 7. The payload is
    as follows:

        <index><begin><block> 

    Where `<index>` is an integer specifying the zero-based piece
    index, `<begin>` is an integer specifying the zero-based byte offset
    within the piece, and `<block>` which is a block of data, and is a
    subset of the piece specified by `<index>`.

Below is an example of what would take place between two peers
setting-up a connection and starting sharing.

1.  The local host opens a TCP Socket to the remote peer and sends the
    handshake message. The local host then listens for the remote peer
    to respond.
2.  Upon accepting the incoming connection, the remote peer responds
    with a similar handshake message (except with its peer\_id). Be sure
    to verify the relevant portions of the handshake message. 
3.  Upon receiving the handshake and verifying the info\_hash, the local
    host then (optionally) sends a bitfield message which tells the
    remote peer which pieces it has downloaded and verified so far.
4.  If the local host is interested in what the remote peer has
    downloaded, then it sends an interested message, otherwise it should
    simply await messages from the remote peer. If the remote peer is
    interested in what the local host has downloaded, then it sends an
    interested message.
5.  When the local host, or the remote peer, is ready to upload to the
    other, it will send an unchoke message.
6.  Once a peer is unchoked, it can send a request message for one of
    the pieces that the other peer announced it has completed.

Please note that clients will, and your client should, ignore any
request messages received while a remote peer is choked. A client should
only upload to another client if the connection is unchoked AND the
remote peer is interested. This means that a remote peer will not reply
to the local hosts's request messages unless you have expressed interest
AND the remote peer has sent an unchoke message. If the remote peer
sends a choke message during data transfer, any outstanding requests
will be discarded and unanswered - they should be re-requested after the
next unchoke message.

### The Write-Up {#the-write-up}

-   Include your name as it appears on the roster and your student ID.
-   A high-level description of how your program works. Specifically,
    describe the high-level interactions between the classes. This is a
    good way to make sure that your program doesn't have any classes
    depending on the implementations of other classes. Drawing a
    dependency diagram is a simple way to visualize these dependencies.
    If you know how to use LaTeX, this should be fairly easy to diagram.
    Also, OpenOffice.org's Draw program has an Export to PDF feature
    that is very simple to use.
-   A brief (about 1 paragraph) description of each class in the
    program.
-   Be sure the file is in PDF format.
-   Optionally, you may include a section on feedback about the program.
    Please only provide constructive/useful comments or insights. What
    parts of the project were the most challenging and which were the
    easiest? Did you have trouble finding resources for the project?
    Were any parts confusing to you?

### Submitting the Project {#submitting-the-project}

The project should be submitted through Sakai.

-   Make sure your name is in comments at the top of every file
    submitted.
-   The "main" method should be in a file called RUBTClient.java.
-   The write-up in HTML or PDF format saved as a writeup.
    <html markdown="1" pdf>

    .
-   All files should be submitted as a compressed archive. Acceptable
    formats are `.zip`, `.tgz`/`.tar.gz`, and `.tar.bz2`. This file
    should be named `<NetID>.<EXT>`, where `<NetID>` is your eden NetID
    and `<EXT>` is the file type extension.

### Grading {#grading-1}

-   Programming Style: 15%
-   Correctly setting up TCP sockets/connections: 15%
-   Correctly interfacing with the tracker: 20%
-   Correctly interfacing with the peer: 20%
-   Correctly downloading and verifying the file: 20%
-   Write-up 10%

### Resources {#resources}

It is strongly recommended that you bookmark or download the [Sun Java
1.6 API ](http://java.sun.com/javase/6/docs/api/), as well as read the
following pages:

-   The Main BT Protocol
    Explanation: <http://www.bittorrent.org/beps/bep_0003.html>
-   Another BT Protocol
    Explanation: <http://wiki.theory.org/BitTorrentSpecification>
-   Java Cryptography: [Java Cryptography Architecture (JCA) Reference
    Guide](http://java.sun.com/javase/6/docs/technotes/guides/security/crypto/CryptoSpec.html)
-   A Page on Maintainable Code: <http://advogato.org/article/258.html>
-   A Page on HTTP
    escaping: <http://www.blooberry.com/indexdot/html/topics/urlencoding.htm>
-   [Wireshark ](http://www.wireshark.org/)- A network traffic sniffing
    tool useful for watching network traffic between your client and the
    tracker/peer.

Any questions about the project in general should be posted to the
Discussion Board tool.  If you have a question that is specific to you
(*e.g.,* JVM install, Eclipse setup), send an email to your TA.

### Frequently Asked Questions {#frequently-asked-questions}

I've been getting a lot of similar questions lately, so I'll post
general forms of them as well as advice on how to solve the underlying
problems. As a bit of general advice, if you aren't sure what a packet
is supposed to look like, you can always fire up a working client (the
mainline BitTorrent client, for example) and then use a network packet
sniffing tool like Ethereal to capture the traffic and analyze it.

1.  I can't connect to the tracker. I've tried creating a Socket and
    sending the bytes through myself by grabbing the InputStream and
    OutputStream from the Socket, but I can't get a response from the
    tracker. What's going wrong?

    Contacting the tracker is a simple HTTP GET request. This type of
    operation is done by every web browser today and even some smaller
    programs. As a result, there exists a class `java.net.URL` that can
    easily handle this type of request. Whatever you're trying to do in
    Java has probably already been done a thousand times, so it's
    usually faster to find an existing implementation than to write one
    yourself.

July 1st, 2013 <small>Lecture</small> {#july-1st-2013-lecture}
-------------------------------------

-   In order to receive messages, a process must an identifier.
-   Each host device has a unique 32-bit IPv4 address.
-   Does the IP address of the host on which a process runs suffice for
    identifying the proces?
    -   No, *many* processes can be running on the same hosts.

July 3rd, 2013 <small>Lecture</small> {#july-3rd-2013-lecture}
-------------------------------------

### Transport layer {#transport-layer}

#### Transport-layer services {#transport-layer-services}

##### Transport Layer vs. Network layer {#transport-layer-vs.-network-layer}

-   *Network layer* is logical communication between hosts.
-   *Transport layer* logical communication between processes.
    -   Relies on, enhances, network layer services.

##### Internet Transport Layer Protocols {#internet-transport-layer-protocols}

-   reliable, in-order delivery (TCP)
    -   congestion control
    -   flow control
    -   connection setup

-   unreliable, unordered delivery: UDP
    -   no-frills extension of “best- effort” IP

-   services not available:
    -   delay guarantees
    -   bandwidth guarantees
    -   jitter (variance) guarantees

#### Multiplexing and demultiplexing {#multiplexing-and-demultiplexing}

##### General {#general}

-   Demultiplexing at receive host:
    -   delivering received segments to correct socket

-   Multiplexing at send host
    -   gathering data from multiple sockets, enveloping data with
        header (later used for demultiplexing)

##### How Demultiplexing Works {#how-demultiplexing-works}

-   host receives IP datagrams
    -   each datagram has source IP address, destination IP address
    -   each datagram carries 1 transport-layer segment
    -   each segment has source, destination port number
    -   host uses IP addresses & port numbers to direct segment to
        appropriate socket

                          32 bits
            +----------------+---------------+
            | source port #  |   dest port # |
            +----------------+---------------+
            |                                |
            |        other header fields     |
            |                                |
            +--------------------------------+
            |                                |
            |       application data msg     |
            |                                |
            +--------------------------------+

##### Connectionless Demultiplexing {#connectionless-demultiplexing}

-   When host receives UDP segment:
    -   checks destination port number in segment
    -   directs UDP segment to socket with that port number

-   IP datagrams with different source IP addresses and/or source port
    numbers directed to same socket

##### How Demultiplexing Works {#how-demultiplexing-works-1}

-   Host receives IP datagrames
    -   Each datagram has source IP, destination IP,
    -   Each datagram carries 1 tranpsot layer segment
    -   Each segment has source, destination, and port number

##### Connection-Oriented Demultiplexing {#connection-oriented-demultiplexing}

-   TCP socket identified by 4- tuple:
    -   source IP address
    -   source port number
    -   dest IP address
    -   dest port number

-   recv host uses all four values to direct segment to appropriate
    socket
-   Server host may support many simultaneous TCP sockets:
    -   each socket identified by its own 4-tuple

-   Web servers have different sockets for each connecting client
    -   non-persistent HTTP will have different socket for each request

#### Connectionless transport: UDP {#connectionless-transport-udp}

##### User Datagram Protocol [RFC 768] {#user-datagram-protocol-rfc-768}

-   no frills,” “bare bones” Internet transport protocol
    -   “best effort” service, UDP segments may be:
    -   lost
    -   delivered out of order to

-   app
    -   connectionless:no handshaking between UDP sender, receiver
    -   each UDP segment handled independently of others

-   Why is there UDP?

### TCP and UDP {#tcp-and-udp}

#### The Internet Transport Layer {#the-internet-transport-layer}

-   Two transport layer protocols supported by the Internet:
    -   Reliable: The Transmission Control Protocol (TCP)
    -   Unreliable: The Unreliable Datagram Protocol (UDP)

#### UDP {#udp}

-   UDP is an unreliable transport protocol that can be used in the
    Internet
-   UDP does not provide:
    -   connection management
    -   flow or error control
    -   guaranteed in-order packet delivery

-   UDP is almost a “null” transport layer

#### Retransmission Timeout (RTO) {#retransmission-timeout-rto}

-   The timeout value is then calculated by multiplying the smoothed RTT
    by some factor (greater than 1) called
    -   Timeout = SRTT
    -   This coefficient of is included to allow for some variation in
        the round trip times.

#### Karn’s Algorithm {#karns-algorithm}

-   Retransmission ambiguity
    -   Measure RTT from original data segment
    -   Measure RTT from most recent segment

-   Either way there is a problem in RTT estimate One solution
    -   Never update RTT measurements based on acknowledgements from
        retransmitted packets

-   Problem: Sudden change in RTT can cause system never to update RTT
    -   Primary path failure leads to a slower secondary path

-   Use back-off as part of RTT computation
-   Whenever packet loss, RTO is increased by a factor
-   Use this increased RTO as RTO estimate for the next segment (not
    from SRTT)
-   Only after an acknowledgment received for a successful transmission
    is the timer set to new RTT obtained from SRTT

#### Another Problem with RTT Calculation {#another-problem-with-rtt-calculation}

-   RTT measurements can sometimes fluctuate severely
    -   smoothed RTT (SRTT) is not a good reflection of round-trip time
        in these cases

-   Solution: Use Jacobson/Karels algorithm:
    -   Error =RTT - SRTT
    -   SRTT = SRTT + Error Dev = Dev + δ(|Error| - Dev) Timeout =
        SRTT+  Dev

July 8th, 2013 <small>Lecture: TCP and UDP Part 2</small> {#july-8th-2013-lecture-tcp-and-udp-part-2}
---------------------------------------------------------

### Principles of Congestion Control {#principles-of-congestion-control}

-   informally: “too many sources sending too much data too fast for
    network to handle”
-   different from flow control! manifestations:
    -   lost packets (buffer overflow at routers)
    -   long delays (queueing in router buffers)

-   a top-10 problem!

### TCP Congestion Control {#tcp-congestion-control}

-   Recall: Network layer is responsible for congestion control
-   However, TCP/IP blurs the distinction In TCP/IP:
    -   the network layer (IP) simply handles routing and packet
        forwarding
    -   congestion control is done end-to-end by TCP

-   Goal: fully (fairly) utilize the resource (bandwidth)
    -   Don’t over use - **congestion**
    -   Don’t under use - **waste**

-   Goal: achieve self-clocking state
    -   Even if don’t know bandwidth of bottleneck
    -   Bottleneck may change over time

July 15th, 2013 <small>Assessment <em>Chapter 2</em></small> {#july-15th-2013-assessment-chapter-2}
------------------------------------------------------------

### Question 1 <small>(20 points)</small> {#question-1-20-points}

> List at least four different applications that are naturally suitable
> for P2P architectures. For each application, provide a 1 to 2 sentence
> justification.

There are two varieties of applications well suited to P2P
architectures, the file distribution variety and the distributed hash
table variety. (1) Of the first, you can imagine just the vanilla
version being well suited to P2P. The reason file distribution is a good
manifestation of P2P is because it does not require an constant
connection to an always on server, file sharing can happen with many
disparate peers with different portions of the file over time. (2) By
extension, you can imagine a P2P architecture that is like file
distribution, but is for generating large, random, prime numbers and
sharing them or storing them. An example would be a peer group to
generate BitCoins. The reason it is a good application of the P2P
architecture is because not every peer needs to be connected to a
tracker all the time, for instance, when the peer is trying to generate
the large, random, prime number, it does not need that server
connection. (3) Of the file sharing variety, it's also possible to
imagine an apt application where the files distributed are not static,
pre-existing files, but files being streamed from a lot of peers. It's a
good use of P2P architecture because it requires the first initial
always-on server connection, and everything after that is talking to
peers and getting content. (4) Of the second variety, which is a P2P
database called a distributed hash table, it could be useful to have a
database stores the name of content and then the corresponding IP
addresses, which means when you query for the content name you're
returned it's IP address location. This is a good use of P2P DHT because
there is the initial talking to the tracker, but then you talk to peers,
who "know" what other peer has a given content in the case of a circular
DHT.

### Question 2 <small>(3 points)</small> {#question-2-3-points}

What information is used by a process running on one host to identify a
process running on another host?

1.  Username and Password  
2.  IP Address and Port Number  
3.  URL and Filename  
4.  Protocol and Filesize

### Question 3 <small>(0 points ?)</small> {#question-3-0-points}

Two distinct Web pages (for example www.mit.edu/research.html and
www.mit.edu/students.html) can be sent over the same persistent
connection.  
With nonpersistent connections between browser and origin server, it is
possible for a single TCP segment to carry two distinct HTTP request
messages.  
The Date: header in the HTTP response message indicates when the object
in the response was last modified.  
HTTP response messages never have an empty message body.

### Question 4 <small>(0 points ?)</small> {#question-4-0-points}

Given the classes of services provided by transport layers listed below,
indicate which are provided by TCP and UDP.

TCP UDP Both Neither Throughput  
Timing  
Security

### Question 5 <small>(3 points)</small> {#question-5-3-points}

Suppose you wanted to do a transaction from a remote client to a server
as fast as possible. Would you use UDP or TCP? Why?

1.  TCP
2.  UDP

### Question 6 <small>(4 points)</small> {#question-6-4-points}

Why is it said that FTP sends control information "out-of-band"?

1.  The data transfer protocol has a flexible speed parameter (like a
    rubber band), but it occasionally goes too fast and is
    "out-of-band".
2.  The control information is sent over a TCP connection separate from
    the data transfer.  
3.  It uses frequency division multiplexing and the control information
    is in a different frequency band than the data.

July 16th, 2013 <small>Reading <em>Chapter 2</em></small> {#july-16th-2013-reading-chapter-2}
---------------------------------------------------------

### Principles of Networking Applications {#principles-of-networking-applications}

-   The **application architecture** is designed by the application
    developer and dictates how the application is structured over the
    various end systems.
-   a **client-server architecture**, there is an always-on *host*,
    called the server, which services requests from many other hosts,
    called *clients*.
    -   Web,
    -   FTP,
    -   Telnet, and
    -   e-mail

-   In a **P2P architecture**, there is minimal (or no) reliance on
    dedicated servers in data centers.

-   Transport services can be:
    -   Reliable or not
    -   High or low throughput, transfer a lot or little data
    -   Time sensitive or not
    -   Secure or not, encryption

-   TCP is without error and in the proper order.
    -   There's handshaking and opening connections.

-   UDP is no-frills, lightweight, with minimal services.
    -   Connectionaless, no handshaking.

### The Web and HTTP {#the-web-and-http}

-   The web's application protocol is HTTP
-   TCP connections can be persistent or not, meaning a new one is
    opened each time or the same way is kept.
-   For non-persistent, -------------------

### File Transfer: FTP {#file-transfer-ftp}

### Electronic Mail in the Internet {#electronic-mail-in-the-internet}

### DNS {#dns}

### Peer-to-Peer Applcations {#peer-to-peer-applcations}

### Socket Programming: Creating Networking Applications {#socket-programming-creating-networking-applications}

July 16th, 2013 <small>Midterm study guide</small> {#july-16th-2013-midterm-study-guide}
--------------------------------------------------

### Practice Exam <small>Spring 2012</small> {#practice-exam-spring-2012}

#### TCP/IP {#tcpip}

> Name the five layers of the TCP/IP protocol stack from highest to
> lowest and given an example implementation.

1.  Physical
    -   How bits and bytes are physically represented
    -   RS-232

2.  Datalink
    -   This is how two connected nodes share information.
    -   Wireless and wired communication
    -   802.11

3.  Network
    -   This is how two end hosts connected.
    -   The only network protocol on the Internet is IP

4.  Transport
    -   "End to end abstraction" for hosts.
    -   TCP, UDP

5.  Application.
    -   This is what the user actually sees and interacts with
    -   HTTP, FTP

#### "Quickies" {#quickies}

1.  Packet-switching vs. message switching.

    > Briefly explain the difference(s) between packet switching and
    > message switching. Under what circumstances would packet switching
    > have an advantage over message switching?

    -   Message switching is where entire peices of unfied data are sent
        across a network at once.
    -   Packet switching is where all data is chopped up into packets at
        potentially every level of hopping between clients.
    -   The advantage of packet-swtiching is that if a message is
        dropped, it has to be retransmitted in bulk. Whereas dropping a
        packet is no big deal, you just ask for the small packet again.
    -   If you're likely to drop, use packets.

2.  Multi-threading

    > In 2-3 sentences, explain why networked applications inherently
    > benefit from a multi- threaded design. Assume that network
    > communication is a significant portion of the application.

    -   There are two reasons that multi-threading is suitable for
        networking:
        1.  Networking can be taking information from a user while
            transmitting data, putting the user on one thread and the
            transmission on the other.
        2.  Oftentimes it is important to both send and receive data
            concurrently, or being listening for data while sending
            data. Any of this would require threading.

3.  Classless inter-domain routing

    > Give two reasons why CIDR replaced the original class-based
    > approach to IP address allocation.

4.  HTTP

    > Describe one advantage and one disadvantage of persistent
    > connections in HTTP. Be sure to justify our answer for full
    > credit.

#### Delay Calculation {#delay-calculation}

> Two hosts communicate with each other via satellites positioned in a
> geosynchronous orbit, 35,000 km above the earth, the two satellites
> are 30,000 km apart. Each node (host/satellite) requires 20ms to
> process any messages. You may assume that any transmissions propagate
> at the speed of light (300,000 km/s), and that no other links are
> used. 1. The hosts allocate a channel with 1 Mbps of capacity. How
> long will it take one of the hosts to transmit a 125 KB message to the
> other. Assume message switching is used, and ignore any
> response/acknowledgement from the receiving host.

1.  Transmission delay: 125 KB \* 8 = 1Mb / 1 Mbps \* 3 = 3 sec (1 s
    each link)
2.  Propagation delay: 35000 + 35000 + 30000 = 100,000 km / 300,000 km =
    333 ms
3.  Protocol delay: 4\*20ms = 80 ms
4.  Total = 3.413 s

#### Distance-Vector Routing {#distance-vector-routing}

#### BitTorrent Project {#bittorrent-project}

> 1.  What exactly is the “info hash” of a metainfo file? What purpose
>     does it serve in the context of communication with trackers and
>     peers? What problems might arise if it was removed from the peer
>     handshake?
> 2.  Most contemporary BitTorrent clients are capable of utilizing a
>     distributed hash table (DHT). The DHT allows the clients to
>     identify other peers in the same swarm. Ignoring any legal issues
>     concerning file sharing networks, why would this be considered an
>     advantage for BitTorrent clients?

### Practice Exam <small>Summer 2011</small> {#practice-exam-summer-2011}

#### Quickies {#quickies-1}

> Differentiate between packet switching and message switching,
> specifically describing scenarios where each would be preferred over
> the other.

> Explain the difference between the recursive and iterative methods of
> resolving DNS queries.

> List the 5 layers of the IP stack and give a brief description of the
> purpose of each, including an existing implementation (protocol).

> Describe why the Internet moved from class-based subnetting to the
> CIDR approach.

#### Network performance {#network-performance}

> Calculate the total time required to transfer a 800KB file in the
> following cases. Assume an RTT (Round Trip Time) of 25ms, a packet
> size of 5KB, and an initial 2xRTT of handshaking before data is sent.
> Show your work for full credit; there is no packet header/overhead; 1
> KB = 1,000B.

1.  The bandwidth is 1Mbps, and data packets can be sent continuously.
    1.  Handshake
    2.  Propagation
    3.  Transmission
    4.  Total

July 26th, 2013 <small>Project \#1</small> {#july-26th-2013-project-1}
------------------------------------------

### Theory of Operation {#theory-of-operation-1}

The second project will expand upon what you did for the first. Your
client must now open a .torrent file, contact the tracker as well as
multiple peers and be able to upload and download to the peers
simultaneously. This means you will have to manage the state of several
connections and work with multiple threads. Your client should also
accept incoming connections from the peers at the IP addresses listed
below. The user should be able to suspend (quit) the program at any
time, and the client should NOT terminate until the user provides the
appropriate input.

If your code for project 1 was well thought-out, it should be easy to
expand your program for multiple downloads, and uploading should not be
much more difficult than listening for more types of messages and
sending new ones. You will not have to worry about choking any peers,
but like the first project, you will have to make sure to unchoke them
and keep them up to date on what pieces your client has downloaded.

Some of the peers you connect to may "misbehave," meaning that they may
not behave the way you expect them to.  The purpose of this is to help
you write code defensively, which means that your application will
likely be more robust than if you only had well-behaved peers to work
with.

### Assignment Overview {#assignment-overview}

Your assignment should basically do the following:

1.  Take as a command-line argument the name of the .torrent file to be
    loaded and the name of the file to save the data to. Your main class
    MUST be called "RUBTClient.java", but may reside in any package. For
    example:

        java RUBTClient somefile.torrent picture.jpg

2.  Open the .torrent file and parse the data inside. You may use the
    Bencoder2 or TorrentInfo classes to decode the data.
3.  Contact the tracker via the announce URL, including all of the
    necessary key/value pairs in the request.  The java.net.URL class is
    a convenient way to accomplish this.
4.  Tracker announces should be performed no more frequently than the
    value of "min\_interval" (or 1/2 "interval" if "min\_interval" is
    not present), and no less frequently than twice the value of
    "interval" returned by the tracker. 
5.  Your client must correctly publish its connection information and
    status to the tracker.  This includes the port, uploaded,
    downloaded, left, and event arguments, when applicable.  Your client
    must accept incoming connections from other peers.  It should not
    maintain more than one TCP connection with another peer.
6.  Capture the response from the tracker and decode it in order to get
    the list of peers. From this list of peers, use only the peers
    located at 128.6.171.3 and 128.6.171.4 . You must extract these IP
    addresses from the list, hard-coding it is not acceptable, except
    the comparison itself.
7.  Open TCP connections to the peers and be able to download and
    upload **simultaneously** from several at the same time.
8.  Download one or more pieces of the file and verify its SHA-1 hash
    against the hash stored in the .torrent file. 
9.  After a piece is downloaded and verified, the peers are notified
    that you have completed the piece.
10. Other peers should be able to request pieces from your client that
    you have verified, and your client should send those pieces to the
    peers, according to the protocol.  Remember that you should be able
    to serve multiple clients simultaneously.
11. Repeat steps 5-8 (using the same TCP connections) for the rest of
    the file.  The client should continue uploading until the user
    provides the appropriate input to shut down the client.
12. When the client has downloaded and verified the entire file, be sure
    to contact the tracker with the *completed* event (even if it is
    shorter than the *interval* value).
13. When the client exits, you must contact the tracker and send it
    the stopped event and properly close all connections.

In addition to the above basic run-through of your program's execution,
your program should be able to detect input from the user at any point
(you can decide what the input should be), and allow the user to close
the program, suspending download of the file. The user should be able to
restart the program at a later time and resume the download. Any
non-verified pieces/blocks should be discarded before suspending, and
the program should also keep track of how much it has uploaded and
downloaded for that torrent.

How you choose to implement saving the state of your program is up to
you, but an intuitive approach might be to allocate the total space to
disk before downloading, and then writing the appropriate pieces into
the file as they complete. 

### Files Available {#files-available-1}

There are several files available in the Resources section of the site
in the folder "Project Resources."  The most important is
"project2.torrent", which is the "testbed" torrent you can use to
develop your client.  The other files available are helpful, but not
necessary.  Be sure to check the resources section for updates or
changes as the course progresses.  Do not modify the provided
files/classes.  If you want to modify their behavior, subclass (extend)
them instead and provide the functionality there.

### Programming Style {#programming-style-1}

Writing maintainable code is just as important as writing correct code.
Consequently, you will be graded on your style. Below is a list of
suggestions to make your code easier to understand and maintain:

-   Javadoc - All classes, fields, and methods that are not private must
    be documented with Javadoc.  Supplying Javadoc comments for private
    classes, methods, and fields is encouraged but optional.
-   Comments - Comments for variables and for sections of code that does
    not have an obvious purpose. Please do not comment obvious
    statements or sections of code. For example,

        int i = 0; //i is an integer and the initial value is 0

    is not useful and unnecessarily clutters the code.

-   Naming - Names of classes, methods, and variables should be
    descriptive. For example, if a class has a field containing its hash
    value, naming the field hash\_value is much better than naming
    it hv .
-   Exceptions - Catch exceptions and do something useful with them. For
    example, print a statement describing what went wrong to System.err.
-   Easy to understand loops/recursion. When possible, it's best to
    avoid break statements whenever possible. When using recursion,
    tail-recursion is often preferable because "smart" compilers can
    often translate it into a loop. Return statements within an if/else
    clause should be avoided whenever possible.
-   Efficiency - Avoid being terribly inefficient. For example, if you
    have to sort 10M objects, it's better to sort them with
    a O(n\*lg(n)) algorithm than a O(n<sup>2</sup>) algorithm.
-   **Encapsulation/Objects** - Encapsulation is a useful feature of
    object-oriented languages, and because you are writing your program
    in an OO language, your program **must** separate the functionality
    into multiple classes. This way you can change the implementation of
    a class without affecting the rest of your program. An example of
    separation would be to have separate FileHandler, PeerInterface, and
    TrackerInterface classes to manipulate files, interface with peers
    and interface with the tracker, respectively. If you do not separate
    your program into functional units, you will lose points on the
    Style portion of the grading.

### Bencoding (Pronounced "Bee Encoding") {#bencoding-pronounced-bee-encoding-1}

Bencoding a method of encoding binary data. Tracker responses, and
interpeer communication will be bencoded. Below is how data types are
bencoded according to the BT protocol. [The following list is taken
from[http://www.bittorrent.org/beps/bep\_0003.html ](http://www.bittorrent.org/beps/bep_0003.html)]

-   Strings are length-prefixed base ten followed by a colon and the
    string. They are encoded in UTF-8. For example 4:spam corresponds to
    'spam'.
-   Integers are represented by an 'i' followed by the number in ASCII
    base 10 followed by an 'e'. For example i3e corresponds to 3 and
    i-3e corresponds to -3. Integers have no size limitation. i-0e is
    invalid. All encodings with a leading zero, such as i03e, are
    invalid, other than i0e, which of course corresponds to 0.
-   Lists are encoded as an 'l' followed by their elements (also
    bencoded) followed by an 'e'. For example, l4:spam4:egse corresponds
    to ['spam', 'eggs'].
-   Dictionaries are encoded as a 'd' followed by a list of alternating
    keys and their corresponding values followed by an 'e'. For example,
    d3:cow3:moo4:spam4:eggse corresponds to {'cow':'moo', 'spam':'eggs'}
    and d4:spaml1:a1:bee corresponds to {'spam': ['a', 'b']}. Keys must
    be strings and appear in sorted order (sorted as raw byte values,
    not alphanumerics).

### Communication With the Tracker {#communication-with-the-tracker-1}

Your client must take the information supplied by the TorrentFile object
and use it to communicate with the tracker. The tracker's IP address and
port number will be given to you by the TorrentFile object, and your
program must then contact the tracker. Your program will send an HTTP
GET request to the tracker with the following key/value pairs. Note that
these are NOT bencoded, but must be properly escaped [this list is taken
from [http://www.bittorrent.org/beps/bep\_0003.html ](http://www.bittorrent.org/beps/bep_0003.html)]:

-   info\_hash - The 20 byte(160-bit) SHA1 hash of the bencoded form of
    the info value from the metainfo file. This value will almost
    certainly have to be escaped.
-   peer\_id - A string of length 20 which this downloader uses as its
    id. Each downloader generates its own id at random at the start of a
    new download. This value will almost certainly have to be escaped.
      You peer ID must NOT start with RUBT.
-   port - The port number this peer is listening on. Common behavior is
    for a downloader to try to listen on port 6881 and if that port is
    taken try 6882, then 6883, etc. and give up after 6889.
-   uploaded - The total amount uploaded so far, encoded in base ten
    ascii.
-   downloaded - The total amount downloaded so far, encoded in base ten
    ascii.
-   left - The number of bytes this peer still has to downloaded,
    encoded in base ten ascii. This key is important - If you do not
    specify how much you have left to download, the tracker assumes you
    are a seed and will not return any seeds in the peer list.
-   event - This is an optional key which maps to started , completed ,
    or stopped (or empty , which is the same as not being present. If
    not present, this is one of the announcements done at regular
    intervals. An announcement using started is sent when a download
    first begins, and one using completed is sent when the download is
    complete. No completed is sent if the file was complete when
    started. Downloaders send an announcement using stopped when they
    cease downloading.

The response from the tracker is a bencoded dictionary and contains two
keys:

-   interval - Maps to the number of seconds the downloader should wait
    between regular rerequests.
-   peers - Maps to a list of dictionaries corresponding to peers, each
    of which contains the keys peer id , ip , and port , which map to
    the peer's self-selected ID, IP address or dns name as a string, and
    port number, respectively.

In addition to what your program did for the last project, your client
should also periodically update its status to the tracker. The update
period should be **no less** than the *interval* returned by the
tracker. This may change during execution, so it should be updated each
time the tracker is contacted. In the event that the *interval* value is
excessively large, you may cap it at 180 seconds.

### Communicating With the Peer {#communicating-with-the-peer-1}

Handshaking between peers begins with byte nineteen (decimal) followed
by the string 'BitTorrent protocol'. After the fixed headers are 8
reserved bytes which are set to 0. Next is the 20-byte SHA-1 hash of the
bencoded form of the info value from the metainfo (.torrent) file. The
next 20-bytes are the peer id generated by the client. The info\_hash
should be the same as sent to the tracker, and the peer\_id is the same
as sent to the tracker. If the info\_hash is different between two
peers, then the connection is dropped.

-   All integers are encoded as 4-bytes big-endian. e.g. 1,234 should be
    encoded as (hex) 00 00 04 d2
-   The peer\_id should be randomly generated each time the client
    starts.  If you keep the value limited to ASCII alphanumerics,
    debugging can be a lot easier.

After the handshake, messages between peers take the form
of ``` <length prefix>``<message ID>``<payload> ``` , where length
prefix is a 4-byte big-endian value and message ID is a single decimal
character. The payload depends on the message. Please consult either of
the BT-related resources for detailed information describing these
messages. Below is a list of messages that need to be implemented in the
project.

-   keep-alive: `<length prefix>` is 0. There is no message ID and no
    payload. These should be sent around once every 2 minutes to prevent
    peers from closing connections. These only need to be sent if no
    other messages are sent within a 2-minute interval.
-   choke: `<**length prefix**>` is 1 and message ID is 0. There is no
    payload.
-   unchoke: `<**length prefix**>` is 1 and the message ID is 1. There
    is no payload.
-   interested: `<length prefix>` is 1 and message ID is 2. There is no
    payload.
-   uninterested: `<length prefix>` is 1 and message ID is 3. There is
    no payload.
-   have: `<length prefix>` is 5 and message ID is 4. The payload is a
    zero-based index of the piece that has just been downloaded and
    verified.
-   bitfield: `<length prefix>` is 1+X (X is number of pieces/8) and
    message ID is 5. The payload is a byte[] containing a single bit for
    each piece in the torrent.  The most significant bit is piece index
    0, then piece index 1, and so on.
-   request: `<length prefix>` is 13 and message ID is 6. The payload is
    as follows: ``` <index>``<begin>``<length> ```  Where `<index>` is
    an integer specifying the zero-based piece index, `<begin>` is an
    integer specifying the zero-based byte offset within the piece,
    and `<length>` is the integer specifying the requested
    length.`<length>` is typically 2\^14 (16384) bytes. A smaller piece
    should only be used if the piece length is not divisible by 16384. A
    peer may close the connection if a block larger than 2\^14 bytes is
    requested.
-   piece: `<length prefix>` is 9+X and message ID is 7. The payload is
    as follows: ``` <index>``<begin>``<block> ```  Where `<index>` is an
    integer specifying the zero-based piece index, `<begin>` is an
    integer specifying the zero-based byte offset within the piece,
    and `<block>` which is a block of data, and is a subset of the piece
    specified by `<index>` .

During the first project, a lot of people were confused about the order
of messages after the handshake. Below is an example of what would take
place between two peers setting-up a connection and starting sharing.

1.  The local host opens a TCP Socket to the remote peer and sends the
    handshake message. The local host then listens for the remote peer
    to respond.
2.  Upon accepting the incoming connection, the remote peer immediately
    sends a handshake message (with its' own peer\_id). Be sure to
    verify the relevant portions of the handshake message. 
3.  Upon receiving the handshake and verifying the info\_hash, both
    hosts then (optionally) send a bitfield message that tells the
    remote peer which pieces it has downloaded and verified so far.
4.  If a host is interested in what the other peer has downloaded, then
    it sends an interested message, otherwise it should simply await
    messages from the other peer. 
5.  When either peer is ready to upload to the other, it will send an
    unchoke message.
6.  Once a peer is unchoked, it can send a request message for one of
    the pieces that the other peer announced previously.

Please note that clients will, and your client should, ignore any
request messages received while a remote peer is choked. A client should
only upload to another client if the connection is unchoked AND the
remote peer is interested. This means that a remote peer will not reply
to the local hosts's request messages unless you have expressed interest
AND the remote peer has sent an unchoke message. If the remote peer
sends a choke message during data transfer, any outstanding requests
will be discarded and unanswered - they should be re-requested after the
next unchoke message.

### The Write-Up {#the-write-up-1}

-   Include all group member names as they appear on the roster and your
    student ID.
-   A high-level written description of how your program works.
    Specifically, describe the high-level interactions between the
    classes. This is a good way to make sure that your program doesn't
    have any classes depending on the implementations of other classes.
    You may include diagrams or illustrations if you feel it would aid
    your explanation or if you have a hard time explaining how your
    program works. However, you MUST include some written description of
    your program. If you know how to use LaTeX, this should be fairly
    easy to diagram. Also, LibreOffice's Draw program has an Export to
    PDF feature that is very simple to use. This section should be
    around 100 words, or 2 paragraphs.
-   A brief (about 1 paragraph) description of each class in the
    program. Describe what it does in general, the main public methods
    it provides, and any public fields it exposes. Note that classes
    should generally NOT have public fields unless they are static final
    (e.g. constants).
-   Optionally, you may include a section on feedback about the program.
    Please only provide constructive/useful comments or insights. What
    parts of the project were the most challenging and which were the
    easiest? Did you have trouble finding resources for the project?
    Were any parts confusing to you? Including feedback will help shape
    the direction of the next project as well as help in pointing-out
    trouble spots to look at during grading.

### Submitting the Project {#submitting-the-project-1}

The project should be submitted through Sakai.

-   **UPDATE**: Your project MUST be managed by either Git or Mercurial
    (Hg) version control systems.  To submit your project, you may
    either submit the entire repository (not only your working
    directory), or you can give the instructor read-only access to your
    repository hosted on BitBucket.org or GitHub.com.  If you choose to
    submit, ensure the entire repository is available in the submitted
    archive (download it and check it).  If you want to grant  access
    and aren't sure how, please contact the instructor via email.
-   Make sure your names are in comments at the top of every file
    submitted.
-   The "main" starting method should be in a file called
    RUBTClient.java.
-   The write-up in HTML or PDF format saved as a writeup.`<html/pdf>`.
    Please do not submit a write-up in any other formats
-   All files should be submitted as a compressed archive. Acceptable
    formats are .zip, .tgz/.tar.gz, and .tar.bz2. This file should be
    named `<Group>`.`<EXT>`, where `<Group>` is your group and `<EXT>`
    is the file type extension.  For example, group 14 might submit
    "group14.zip" or "group14.tgz".
-   Late submissions will **not** be accepted. If you have not completed
    the project, submit what you have and you will be graded for partial
    credit.

### Grading {#grading-2}

-   Programming Style: 15%
-   Correctly interfacing with the tracker (retrieving peer list,
    periodic updates, after completing download): 10%
-   Correctly interfacing with the peers (handshaking, maintaining
    state, keep-alive): 10%
-   Correctly downloading from at least 2 peers **simultaneously**: 15%
-   Correctly uploading to at least 2 peers **simultaneously**: 15%
-   Stopping from user input and resuming correctly: 10%
-   Correctly downloading and verifying the file: 15%
-   Write-up 10%
-   **UPDATE:** To ensure everyone in the group contributes to the final
    submission, your individual grade will be weighted by how much you
    contributed, up to 50% of the project grade.  Contribution will be
    evaluated based on the repository commit logs (see above), so be
    sure to commit as often as practical.

### Resources {#resources-1}

It is strongly recommended that you bookmark or download the [Sun Java
1.6 API ](http://java.sun.com/javase/6/docs/api/), as well as read the
following pages:

-   The Main BT Protocol
    Explanation: <http://www.bittorrent.org/beps/bep_0003.html>
-   Another BT Protocol
    Explanation: <http://wiki.theory.org/BitTorrentSpecification>
-   Java Cryptography: [Java Cryptography Architecture (JCA) Reference
    Guide](http://java.sun.com/javase/6/docs/technotes/guides/security/crypto/CryptoSpec.html)
-   A Page on Maintainable Code: <http://advogato.org/article/258.html>
-   A Page on HTTP
    escaping: <http://www.blooberry.com/indexdot/html/topics/urlencoding.htm>
-   [Wireshark ](http://www.wireshark.org/)- A network traffic sniffing
    tool useful for watching network traffic between your client and the
    tracker/peer.

Any questions about the project in general should be posted to the
Discussion Board tool.  If you have a question that is specific to you
(*e.g.,* JVM install, Eclipse setup), send an email to your TA.

 

### Frequently Asked Questions {#frequently-asked-questions-1}

I've been getting a lot of similar questions lately, so I'll post
general forms of them as well as advice on how to solve the underlying
problems. As a bit of general advice, if you aren't sure what a message
is supposed to look like, you can always fire up a working client (the
mainline BitTorrent client, for example) and then use a network message
sniffing tool like Wireshark to capture the traffic and analyze it.

1.  I can't connect to the tracker. I've tried creating a Socket and
    sending the bytes through myself by grabbing the InputStream and
    OutputStream from the Socket, but I can't get a response from the
    tracker. What's going wrong?

    Contacting the tracker is a simple HTTP GET request. This type of
    operation is done by every web browser today and even some smaller
    programs. As a result, there exists a class `java.net.URL` that can
    easily handle this type of request. Whatever you're trying to do in
    Java has probably already been done a thousand times, so it's
    usually faster to find an existing implementation than to write one
    yourself.

August 5th, 2013 <small>Chapter 4 Review</small> {#august-5th-2013-chapter-4-review}
------------------------------------------------

### Question 1 {#question-1}

> What is the 32-bit binary equivalent of the IP address 192.168.1.55?

-   11000000101010000000000100110111

### Question 2 {#question-2}

> What are the two most important network-layer functions in a datagram
> network? [What third function is additionally important in a virtual
> circuit network?]
>
> -   <del markdown="1">
>         
>     Retransmission, Error Correction, [Connection Setup]</del>
> -   Forwarding, <del>Error Correction</del>, [Session Management]  
> -   **Forwarding, Routing, [Connection Setup]**
> -   Routing, Retransmission, [Reliability]

### Question 3 {#question-3}

> What is the difference between forwarding and routing?

*Forwarding* refers to the router-local action of transferring a packet
from an input link interface to the appropriate output link interface.

*Routing* refers to the network-wide process that determines the
end-to-end paths that packets take from source to destination.

### Question 4 {#question-4}

> Suppose an ISP owns the block of addresses of the form
> 128.119.40.64/25. Suppose it wants to create four subnets from this
> block, with each block having the same number of IP addresses. What
> are the prefixes (of form a.b.c.d/x) for the four subnets?

-   128.119.40.64/25
-   128.119.40.80/25
-   128.119.40.96/25
-   128.119.40.112/25

### Question 5 {#question-5}

> Identify the different types of data units at different levels of the
> network protocol stack. If no answer matches exactly, choose the best
> fit. (A) Frame, (B) Segment, (C) Packet, (D) Message
>
> 1.  Transport Layer Data Unit **(B)**
> 2.  Network Layer Data Unit **(C)**
> 3.  Application Layer Data Unit **(D)**
> 4.  Link Layer Data Unit **(A)**

August 7th, 2013 <small>Project \#2</small> {#august-7th-2013-project-2}
-------------------------------------------

### Theory of Operation {#theory-of-operation-2}

The third project will expand upon what you did for the first two. Your
client must be able to interface with multiple peers, upload and
download, accept incoming connections, publish appropriate information
to the tracker (port, uploaded, downloaded, left, events, etc.) to allow
remote peers to contact your client. 

The client must also use the rarest-piece-first algorithm for piece
selection; and perform choking and optimistic unchoking.  Throughput
measurement is necessary to accomplish correct (un)choking behavior. 
The client should be able to maintain connections to at least ten (10)
peers, though not all peers need to be uploading/downloading
simultaneously.

The user should be able to suspend (quit) the program at any time, and
the client should NOT terminate until the user provides the appropriate
input.

Extra credit will be available to groups that develop a Graphical User
Interface (GUI) for their client.  The GUI should have complete
functionality: displaying all relevant information about the client,
allowing user input, and be aesthetically pleasing.  The extra credit
GUI has a maximum value of 15% of the project grade (115% with full
credit).  To achieve the full 15%, the GUI will need to be very
well-designed and -implemented.

### Assignment Specifics {#assignment-specifics-1}

Your assignment should basically do the following:

1.  Take as a command-line argument the name of the .torrent file to be
    loaded and the name of the file to save the data to. For example:

        java my.package.RUBTClient somefile.torrent somepicture.jpg

2.  See Project Part 2 for the basics of how your client should behave.
3.  Your client must correctly publish its connection information and
    status to the tracker.  This includes the port, uploaded,
    downloaded, left, and event arguments.  Your client must accept
    incoming connections from other peers.  It should not maintain more
    than one TCP connection to another peer.
4.  Piece requests should be ordered based on piece rarity for all
    connected (not only unchoked) clients.  The rarest piece available
    from a peer should be requested first, and if there are more than
    one pieces with the same rarity available, a randomized selection
    scheme should be used.
5.  Every 30 seconds, the client should analyze the performance of the
    connected peers, choke the "worst" peer, and randomly unchoke a
    choked peer.  Priority should be given to peers with high upload
    speeds while downloading (you finish sooner), or peers with high
    download speeds while seeding (they finish sooner), in order to
    maximize swarm throughput.
6.  You may limit the number of unchoked connections to 3.  No more than
    6 connections should be active (unchoked) at any point. 
7.  Tracker scrapes should be performed no more frequently than the
    value of "min\_interval" (or 1/2 "interval" if "min\_interval" is
    not present), and no less frequently than twice the value of
    "interval" returned by the tracker. 

How you choose to implement saving the state of your program is up to
you, but an intuitive approach might be to allocate the total space to
disk before downloading, and then writing the appropriate pieces into
the file as they complete. It is recommended that you do not use
serialization of Java objects to save client state.

### Files Available {#files-available-2}

There are several files available in the Resources section of the site
in the folder "Project files."  The most important is project2.torrent,
which will continue to be used for part 3.  The other files available
are helpful, but not necessary.  Be sure to check the resources section
for updates or changes.

### Programming Style {#programming-style-2}

Writing maintainable code is just as important as writing correct code.
Consequently, you will be graded on your style. Below is a list of
suggestions to make your code easier to understand and maintain:

-   Javadoc - All classes, fields, and methods that are not private must
    be documented with Javadoc.  Supplying Javadoc comments for private
    classes, methods, and fields is encouraged but optional.
-   Comments - Comments for variables and for sections of code that does
    not have an obvious purpose. Please do not comment obvious
    statements or sections of code. For example,

        int i = 0;  //i is an integer and the initial value is 0

    is not useful and unnecessarily clutters the code.

-   Naming - Names of classes, methods, and variables should be
    descriptive. For example, if a class has a field containing its hash
    value, naming the field hash\_value is much better than naming
    it hv .
-   Exceptions - Catch exceptions and do something useful with them. For
    example, print a statement describing what went wrong to System.err.
-   Easy to understand loops/recursion. When possible, it's best to
    avoid break statements whenever possible. When using recursion,
    tail-recursion is often preferable because "smart" compilers can
    often translate it into a loop. Return statements within an if/else
    clause should be avoided whenever possible.
-   Efficiency - Avoid being terribly inefficient. For example, if you
    have to sort 10M objects, it's better to sort them with
    a O(n\*lg(n)) algorithm than a O(n<sup>2</sup>) algorithm.
-   **Encapsulation/Objects** - Encapsulation is a useful feature of
    object-oriented languages, and because you are writing your program
    in an OO language, your program **must** separate the functionality
    into multiple classes. This way you can change the implementation of
    a class without affecting the rest of your program. An example of
    separation would be to have separate FileHandler, PeerInterface, and
    TrackerInterface classes to manipulate files, interface with peers
    and interface with the tracker, respectively. If you do not separate
    your program into functional units, you will lose points on the
    Style portion of the grading.

### Bencoding (Pronounced "Bee Encoding") {#bencoding-pronounced-bee-encoding-2}

Bencoding a method of encoding binary data. Tracker responses, and
interpeer communication will be bencoded. Below is how data types are
bencoded according to the BT protocol. [The following list is taken
from[http://www.bittorrent.org/beps/bep\_0003.html ](http://www.bittorrent.org/beps/bep_0003.html)]

-   Strings are length-prefixed base ten followed by a colon and the
    string. They are encoded in UTF-8. For example 4:spam corresponds to
    'spam'.
-   Integers are represented by an 'i' followed by the number in ASCII
    base 10 followed by an 'e'. For example i3e corresponds to 3 and
    i-3e corresponds to -3. Integers have no size limitation. i-0e is
    invalid. All encodings with a leading zero, such as i03e, are
    invalid, other than i0e, which of course corresponds to 0.
-   Lists are encoded as an 'l' followed by their elements (also
    bencoded) followed by an 'e'. For example, l4:spam4:egse corresponds
    to ['spam', 'eggs'].
-   Dictionaries are encoded as a 'd' followed by a list of alternating
    keys and their corresponding values followed by an 'e'. For example,
    d3:cow3:moo4:spam4:eggse corresponds to {'cow':'moo', 'spam':'eggs'}
    and d4:spaml1:a1:bee corresponds to {'spam': ['a', 'b']}. Keys must
    be strings and appear in sorted order (sorted as raw strings, not
    alphanumerics).

### Communication With the Tracker {#communication-with-the-tracker-2}

Your client must take the information supplied by the TorrentFile object
and use it to communicate with the tracker. The tracker's IP address and
port number will be given to you by the TorrentFile object, and your
program must then contact the tracker. Your program will send an HTTP
GET request to the tracker with the following key/value pairs. Note that
these are NOT bencoded, but must be properly escaped [this list is taken
from [http://www.bittorrent.org/beps/bep\_0003.html ](http://www.bittorrent.org/beps/bep_0003.html)]:

-   info\_hash - The 20 byte(160-bit) SHA1 hash of the bencoded form of
    the info value from the metainfo file. This value will almost
    certainly have to be escaped.
-   peer\_id - A string of length 20 which this downloader uses as its
    id. Each downloader generates its own id at random at the start of a
    new download. This value will almost certainly have to be escaped.
-   port - The port number this peer is listening on. Common behavior is
    for a downloader to try to listen on port 6881 and if that port is
    taken try 6882, then 6883, etc. and give up after 6889.
-   uploaded - The total amount uploaded so far, encoded in base ten
    ascii.
-   downloaded - The total amount downloaded so far, encoded in base ten
    ascii.
-   left - The number of bytes this peer still has to downloaded,
    encoded in base ten ascii. This key is important - If you do not
    specify how much you have left to download, the tracker assumes you
    are a seed and will not return any seeds in the peer list.
-   event - This is an optional key which maps to started , completed ,
    or stopped (or empty , which is the same as not being present. If
    not present, this is one of the announcements done at regular
    intervals. An announcement using started is sent when a download
    first begins, and one using completed is sent when the download is
    complete. No completed is sent if the file was complete when
    started. Peers send an announcement using stopped when they exit.

The response from the tracker is a bencoded dictionary and contains two
keys:

-   interval - Maps to the number of seconds the downloader should wait
    between regular requests.  Scrapes should occur within (interval *
    .5, interval *2) seconds of the previous scrape.
-   peers - Maps to a list of dictionaries corresponding to peers, each
    of which contains the keys peer id , ip , and port , which map to
    the peer's self-selected ID, IP address or dns name as a string, and
    port number, respectively.

In addition to what your program did for the last project, your client
should also periodically update its status to the tracker. The update
period should be **no less** than the \*min\_\*\*interval* returned by
the tracker (or half of *interval*, if *min\_interval* is not present).
This may change during execution, so it should be updated each time the
tracker is contacted. In the event that the *interval\* value is
excessively large, you may cap it at 180 seconds.

### Communicating With the Peer {#communicating-with-the-peer-2}

Handshaking between peers begins with character nineteen (decimal)
followed by the string 'BitTorrent protocol'. After the fixed headers
are 8 reserved bytes which are set to 0. Next is the 20-byte SHA-1 hash
of the bencoded form of the info value from the metainfo (.torrent)
file. The next 20-bytes are the peer id generated by the client. The
info\_hash should be the same as sent to the tracker, and the peer\_id
is the same as sent to the tracker. If the info\_hash is different
between two peers, then the connection is dropped.  You must verify the
peer ID of the remote peer if it is available (e.g. from a tracker
scrape), if the connection is incoming and you have no information about
the connecting peer, you may omit checking the peer ID.

-   All integers are encoded as 4-bytes big-endian. e.g. 1,234 should be
    encoded as (hex) 00 00 04 d2
-   The peer\_id should simply be random bytes.  It is suggested that
    you make the peer ID ASCII-printable for compatibility with other
    peers and debugging purposes.

After the handshake, messages between peers take the form of <length
prefix><message ID><payload> , where length prefix is a 4-byte
big-endian value and message ID is a single decimal character. The
payload depends on the message. Please consult either of the BT-related
resources for detailed information describing these messages. Below is a
list of messages that need to be implemented in the project.

-   keep-alive: <length prefix> is 0. There is no message ID and no
    payload. These should be sent around once every 2 minutes to prevent
    peers from closing connections. These only need to be sent if no
    other packets are sent within a 2-minute interval.
-   choke: \<**length prefix**\> is 1 and message ID is 0. There is no
    payload.
-   unchoke: \<**length prefix**\> is 1 and the message ID is 1. There
    is no payload.
-   interested: <length prefix> is 1 and message ID is 2. There is no
    payload.
-   uninterested: <length prefix> is 1 and message ID is 3. There is no
    payload.
-   have: <length prefix> is 5 and message ID is 4. The payload is a
    zero-based index of the piece that has just been downloaded and
    verified.
-   bitfield: <length prefix> is 1+X and message ID is 5. The payload is
    a sequence of *X* bytes where each bit indicates whether the peer
    has the piece at the bit's index. 
-   request: <length prefix> is 13 and message ID is 6. The payload is
    as follows: <index><begin><length>  Where <index> is an integer
    specifying the zero-based piece index, <begin> is an integer
    specifying the zero-based byte offset within the piece,
    and <length> is the integer specifying the requested
    length.<length> is typically 2\^14 (16384) bytes. A smaller piece
    should only be used if the piece length is not divisible by 16384. A
    peer may close the connection if a block larger than 2\^14 bytes is
    requested.
-   piece: <length prefix> is 9+X and message ID is 7. The payload is as
    follows: <index><begin><block>  Where <index> is an integer
    specifying the zero-based piece index, <begin> is an integer
    specifying the zero-based byte offset within the piece,
    and <block> which is a block of data, and is a subset of the piece
    specified by <index> .

Below is an example of what would take place between two peers
setting-up a connection and starting sharing.

1.  The local host opens a TCP Socket to the remote peer and sends the
    handshake packet. The local host then listens for the remote peer to
    respond.
2.  Upon receiving the handshake packet and verifying the info\_hash,
    the remote peer responds with a similar handshake packet (except
    with its peer\_id). The remote peer then listens for the local host
    to send a bitfield or other packet. The remote host can send a
    bitfield packet to the local host at this time.
3.  Upon receiving the handshake and verifying the info\_hash, the local
    host then (optionally) sends a bitfield packet which tells the
    remote peer which pieces it has downloaded and verified so far.
4.  If the local host is interested in what the remote peer has
    downloaded, then it sends an interested packet, otherwise it sends
    an uninterested packet. If the remote peer is interested in what the
    local host has downloaded, then it sends an interested packet,
    otherwise it sends an uninterested packet.
5.  When the local host, or the remote peer, is ready to download/upload
    to the other, it will send an unchoke packet.

Please note that clients will, and your client should, ignore any
request messages received while a remote peer is choked. A client should
only upload to another client if the connection is unchoked AND the
remote peer is interested. This means that a remote peer will not reply
to the local hosts's request messages unless you have expressed interest
AND the remote peer has sent an unchoke packet. If the remote peer sends
a choke packet during data transfer, any outstanding requests will be
discarded and unanswered - they should be re-requested after the next
unchoke packet.

### The Write-Up {#the-write-up-2}

-   Include your name as it appears on the roster and your student ID.
-   A high-level written description of how your program works.
    Specifically, describe the high-level interactions between the
    classes. This is a good way to make sure that your program doesn't
    have any classes depending on the implementations of other classes.
    You may include diagrams or illustrations if you feel it would aid
    your explanation or if you have a hard time explaining how your
    program works. However, you MUST include some written description of
    your program. If you know how to use LaTeX, this should be fairly
    easy to diagram. Also, OpenOffice.org's Draw program has an Export
    to PDF feature that is very simple to use. This section should be
    around 100 words, or 2 paragraphs.
-   A brief (about 1 paragraph) description of each class in the
    program. Describe what it does in general, the main public methods
    it provides, and any public fields it exposes. Note that classes
    should generally NOT have public fields unless they are Static (e.g.
    constants).
-   Optionally, you may include a section on feedback about the program.
    Please only provide constructive/useful comments or insights. What
    parts of the project were the most challenging and which were the
    easiest? Did you have trouble finding resources for the project?
    Were any parts confusing to you? Including feedback will help shape
    the direction of the next project as well as help in pointing-out
    trouble spots to look at during grading.

### Submitting the Project {#submitting-the-project-2}

The project should be submitted through Sakai.

-   Your project MUST be managed by either Git or Mercurial (Hg) version
    control systems.  To submit your project, you may either submit the
    entire repository (not only your working directory), or you can give
    the instructor read-only access to your repository hosted on
    BitBucket.org or GitHub.com. 
-   Make sure your names are in comments at the top of every file
    submitted.
-   The "main" starting method should be in a file called
    RUBTClient.java.
-   The write-up in HTML or PDF format saved as a writeup.
    <html markdown="1" pdf>
        
    . Please do not submit a write-up in any other formats
-   All files should be submitted as a compressed archive. Acceptable
    formats are .zip, .tgz/.tar.gz, and .tar.bz2. This file should be
    named <NetID>.<EXT>, where <NetID> is your eden NetID and <EXT> is
    the file type extension.
-   Late submissions will **not** be accepted. If you have not completed
    the project, submit what you have and you will be graded for partial
    credit.

### Grading {#grading-3}

-   Programming Style: 15%
-   Correctly interfacing with the tracker (retrieving peer list,
    periodic updates, after completing download): 10%
-   Correctly interfacing with the peers (handshaking, maintaining
    state, keep-alive): 10%
-   Correctly downloading from at least 2 peers **simultaneously**: 10%
-   Correctly uploading to at least 2 peers **simultaneously**: 10%
-   Correctly downloading and verifying the file: 15%
-   Rarest-piece-first selection algorithm: 5%
-   Ability to maintain at least 10 peer connections: 5%
-   Optimistic choking/unchoking (includes rate measurement and
    throttling): 10%
-   Write-up 10%
-   To ensure everyone in the group contributes to the final submission,
    your individual grade will be weighted by how much you contributed,
    up to 50% of the project grade.  Contribution will be evaluated
    based on the repository commit logs (see above), so be sure to
    commit as often as practical.

### Resources {#resources-2}

It is strongly recommended that you bookmark or download the [Sun Java
1.6 API ](http://java.sun.com/javase/6/docs/api/), as well as read the
following pages:

-   The Main BT Protocol
    Explanation: <http://www.bittorrent.org/beps/bep_0003.html>
-   Another BT Protocol
    Explanation: <http://wiki.theory.org/BitTorrentSpecification>
-   Java Cryptography: [Java Cryptography Architecture (JCA) Reference
    Guide](http://java.sun.com/javase/6/docs/technotes/guides/security/crypto/CryptoSpec.html)
-   A Page on Maintainable Code: <http://advogato.org/article/258.html>
-   A Page on HTTP
    escaping: <http://www.blooberry.com/indexdot/html/topics/urlencoding.htm>
-   [Wireshark ](http://www.wireshark.org/)- A network traffic sniffing
    tool useful for watching network traffic between your client and the
    tracker/peer.

Any questions about the project in general should be posted to the
Discussion Board tool.  If you have a question that is specific to you
(*e.g.,* JVM install, Eclipse setup), send an email to your TA.

 

### Frequently Asked Questions {#frequently-asked-questions-2}

I've been getting a lot of similar questions lately, so I'll post
general forms of them as well as advice on how to solve the underlying
problems. As a bit of general advice, if you aren't sure what a packet
is supposed to look like, you can always fire up a working client (the
mainline BitTorrent client, for example) and then use a network packet
sniffing tool like Ethereal to capture the traffic and analyze it.

1.  I can't connect to the tracker. I've tried creating a Socket and
    sending the bytes through myself by grabbing the InputStream and
    OutputStream from the Socket, but I can't get a response from the
    tracker. What's going wrong?

    Contacting the tracker is a simple HTTP GET request. This type of
    operation is done by every web browser today and even some smaller
    programs. As a result, there exists a class `java.net.URL` that can
    easily handle this type of request. Whatever you're trying to do in
    Java has probably already been done a thousand times, so it's
    usually faster to find an existing implementation than to write one
    yourself.

August 12th, 2013 <small>Chapter 5 Review</small> {#august-12th-2013-chapter-5-review}
-------------------------------------------------

### Question 1 <small>(2 points)</small> {#question-1-2-points}

> How big is the MAC address space?
>
> -   8 bytes
> -   4 bytes
> -   **6 bytes**
> -   16 bytes

### Question 2 <small>(2 points)</small> {#question-2-2-points}

> How big is the IPv6 address space?
>
> -   8 bytes
> -   4 bytes
> -   **16 bytes**
> -   6 bytes

-   [The length of an IPv6 address is 128 bits, compared with 32 bits in
    IPv4.](http://en.wikipedia.org/wiki/IPv6#Larger_address_space)
-   128 bits is equal to 16 bytes.

### Question 3 <small>(2 points)</small> {#question-3-2-points}

> How big is the IPv4 address space?
>
> -   **4 bytes**
> -   6 bytes
> -   16 bytes
> -   6 bytes

### Question 4 <small>(5 points)</small> {#question-4-5-points}

> Consider the 5-bit generator, G=10011, and suppose that D has the
> value 1010101010. What is the value of R (in binary)?

`0100`

### Question 5 <small>(4 points)</small> {#question-5-4-points}

> Imagine are building your own NAT. What is the MINIMUM amount of
> information the NAT's internal TCP connection table needs to store in
> order to relay packets?
>
> -   LAN IP address, LAN port, Dst IP address, Dst port, WAN port  
> -   LAN IP address, Dst IP address, WAN port ???
> -   **LAN IP address, LAN port, WAN port**  
> -   LAN IP address, LAN port, Dst IP address, Dst port

### Question 6 <small>(8 points)</small> {#question-6-8-points}

> While wired link layer communication protocols are able to detect
> collisions, wireless links can not. What property of wireless
> communication prevents collision detection? Presume all nodes can hear
> each other.

Wireless communication prevents collision detection because, generally,
the sender cannot "hear" what the receiver actually receives. A single
antenna is used to send and receive. More specifically, because a single
antenna cannot send and receive at the same time, collision detection is
impossible.

August 13th, 2013 <small>Final Exam Study Guide</small> {#august-13th-2013-final-exam-study-guide}
-------------------------------------------------------

### Datalink layers <small>Part 1</small> {#datalink-layers-part-1}

-   hosts and routers are **nodes**
-   communication path are **links**
-   Link layers services:
    -   Framing
        -   encapsulate datagram into frame, adding header, trailer link
            access

    -   channel access if shared medium
    -   Reliable delivery between adjacent nodes
    -   Flow Control
    -   Error Detection
    -   Error Correction
    -   Half-duplex and full-duplex
        -   with half duplex, nodes at both ends of link can transmit,
            but not at same time

### Exam guesses and Questions {#exam-guesses-and-questions}

#### Question 0 {#question-0}

> If every node in a network has implemented **Hamming Codes** at the
> link layer to provide error detection and correction, why is it \_\_\_
> to have \_\_ \_\_ at \_\_\_\_\_?

-   Hamming codes correct all single bit errors with only `log(M)` extra
    bits and detect double bit errors
-   The question is about a layer other than the link, I think.
-   s othe receiver might deliver a corrupted datagram to the network
    layer, or be unaware that the contentf a field in the frame’s header
    has been corrupted.

#### Question 1 {#question-1-1}

> Presume you have written \_\_\_\_\_\_ . Would \_\_\_\_ in order to
> \_\_\_ ? (think carefully about the **HTTP messages** you've seen and
> how they operate)

#### Question 2 {#question-2-1}

> What is the \_\_ of the \_\_\_\_ at each of the following \_?

Presumably some sort of fill in the blank.

##### Sub-question 1 {#sub-question-1}

-   The five services:
    -   Confidentiality
    -   Non-repudiation
    -   Integrity
    -   Authorization

> 1.  Public/private key challenge mechanism does not provide
>     authentication. \_\_\_\_\_ how the \_\_\_ can be \_\_\_\_.
> 2.  Public key encryption by itself does not provide **. What can be
>     **\_\_\_ \_\_ \_\_ to provide \_\_\_\_. Explain why \_\_\_\_.
> 3.  Does public key encryption provide \_\_\_\_ without any
>     modification? Why or why not?
> 4.  How \_\_\_\_\_\_ \_ \_\_\_ a public key \_\_\_ \_\_\_ secure?

1.  Public key certification ------------------------

2.  Message integrity.

3.

##### Sub-question 2 {#sub-question-2}

-   Possible attacks:
    -   Man in the middle attack \> Bob receives everything that Alice
        sends, and vice versa. \> (e.g., so Bob, Alice can meet one week
        later and recall conversation) \> Problem to solve: key
        distribution

    -   playback attack
        -   To avoid playback, use a nonce.
        -   Send R, large number, and expect it back encrypted with the
            private key.

> 1.  \_ can be broken with a \_\_\_\_\_ attack. Explain what a \_\_\_\_
>     attack is. What is '\_\_'?
> 2.  What is a '\_\_\_\_”?
> 3.  What is \_\_\_\_\_?

##### Sub-question 3 {#sub-question-3}

### Richie {#richie}

1.  CRC
2.  Timing
3.  Routing table

