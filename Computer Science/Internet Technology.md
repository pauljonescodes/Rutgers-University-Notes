Internet Technology <small>with John-Austen Francisco</small>
=============================================================

Description
-----------

To provide a practical understanding of computer networks with respect
to system architectures, protocols, and client-server interaction. These
objectives are accomplished through extensive laboratory exercises.

### Topics

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

### Department Learning Goals

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

Syllabus
--------

### Instructor Info

-   **Instructor**: John-Austen Francisco
    -   **Office**: Room 335 (DATAMAN Lab), CoRE Building, Busch Campus
    -   **Phone**: (732) 445-6450 x9571
    -   **Email**: deymious@gmail.com
    -   **Office Hours**: Wednesdays 1530-1730

-   **Teaching Assistant**: Jeff Ames
    -   **Office**: Room 335 (DATAMAN Lab), CoRE Building, Busch Campus
    -   **Email**: jeff.ames@cs.rutgers.edu
    -   **Office Hours**: Wednesday 1300-1500

### Requirements

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

### Grading

This course has 1 midterm exam, held during the normal lecture time, and
a cumulative final exam. There will be periodic homework assignments,
either online through Sakai or to be submitted before the beginning of
lectures. Finally, a course-long programming project, written in Java,
will introduce the concepts of network socket programming,
multi-threading, and protocol implementation.

<table class="table">
<tbody>
<tr>
<th>
Assignment
</th>

<th>
Weight
</th>
</tr>

<tr>
<td>
Homework
</td>

<td>
15%
</td>
</tr>

<tr>
<td>
Midterm
</td>

<td>
20%
</td>
</tr>

<tr>
<td>
Final examination
</td>

<td>
30%
</td>
</tr>

<tr>
<td>
Project part 0
</td>

<td>
10%
</td>
</tr>

<tr>
<td>
Project part 1
</td>

<td>
10%
</td>
</tr>

<tr>
<td>
Project part 2
</td>

<td>
15%
</td>
</tr>
</tbody>
</table>


### Important Dates

<table class="table">
<tbody>
<tr>
<th>
Date
</th>

<th>
Event
</th>

<th>
Notes
</th>
</tr>

<tr>
<td>
7/15
</td>

<td>
Project 0 Due
</td>

<td>
Online submission through Sakai.
</td>
</tr>

<tr>
<td>
7/17
</td>

<td>
Midterm
</td>

<td>
In-class exam.
</td>
</tr>

<tr>
<td>
7/29
</td>

<td>
Project 1 Due
</td>

<td>
Online submission through Sakai.
</td>
</tr>

<tr>
<td>
8/14
</td>

<td>
Project 2 Due
</td>

<td>
Online submission through Sakai.
</td>
</tr>

<tr>
<td>
8/14
</td>

<td>
Final Exam
</td>

<td>
In-class exam.
</td>
</tr>
</tbody>
</table>

### Policy on Missed Examinations

You must have a pressing reason (such as a medical emergency or personal
crisis) to miss a scheduled mid-term or final examination. Make-up
examinations may be taken if you have notified the instructor at least
two weeks prior to the original examination that you will not be able to
attend. If you miss an examination due to an unforeseen emergency, you
may take a make-up examination only after providing written
documentation of an excuse that is acceptable to the instructor.

### Required Textbook

-   *Computer Networking*, 6th Edition
    -   **Authors**: James Kurose and Keith Ross
    -   **Publisher**: Addison Wesley
    -   **ISBN**: 0-13-285620-4

### Policy on Disability Accomodation

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

June 24th, 2013 <small>Lecture: Socket Programming</small>
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

June 26th, 2013 <small>Recitation</small>
-----------------------------------------

### Threading and concurrency

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

June 26th, 2013 <small>Lecture: Network Switching Techniques</small>
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

June 30th, 2013 <small>Reading: <em>Chapter 1, Computer Networks and the Internet</em></small>
----------------------------------------------------------------------------------------------

### A Nuts-and-Bolts Description

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

### A Services Description

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
        Programming Interfaces">APIs</abbr> that specify how a program
    on one end system asks the Internet infrastucture to deliver data to
    a specific destination.

### What Is a Protocol?

> A **protocol** defines the format and the order of messages exchanged
> between two or more communicating entities, as well as the actions
> taken on the trans- mission and/or receipt of a message or other
> event.

### The Network Edge

-   Hosts are grouped into two categories:
    -   **Clients**, which tend to be desktops, mobile PCs, smartphones,
        etc.
    -   **Servers**, which tend to be more powerful machines that store
        and distribute Web pages, stream video, relay email, etc.
    -   **Data centers** have possibly thousands of servers.

#### Access Networks <small>Home Access: DSL, Cable, FTTH, Dial-Up and Stellite</small>

-   <abbr title="Digital subscriber line">DSL</abbr> and cable are the
    two most prevelant types of broadband.
-   **Cable Internet access** makes use of cable television's existing
    cable television infrastructure.
-   <abbr title="Fiber to the home">FTTH</abbr> is growing.

### Physical media

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

#### Twisted-Pair Copper Wire

-   This is the least expensive and most commonly used transmission
    medium.
    -   For hundreds of years, it has been used for telephones.
    -   99 percet of wired connections use twisted-pair copper wire.

-   <abbr title="Unshielded twisted pair">UTP</abbr> is commonly used
    for computer netowkrs withing a building, for LAN.

#### Coaxial Cable

-   Like twisted pair, coaxial consists of two copper conductors.
    -   But they're concentric rather than parallel.
    -   Used for television.

-   Coaxial cable can be used as a guided **shared medium**.
    -   A number of end systems can be connected directly to the cable.
    -   With each end receiving whatever is sent by the other end
        system.

#### Fiber Optics

-   Thin, flexible medium that conducts pulses of light, each pulse
    representing a bit.
-   Long distance communication uses this.

### The Network Core

#### Packet Switching

-   End systems enchange **messages** with each other.
    -   These contain anything the application designer wants.
    -   To send a message from source end systems to destination end
        systems, the source breaks long messages into smaller chunks of
        data known as **packets**.
    -   **Packet switches** are where the information travels tbhrough.
        There are:
        -   **Routers**
        -   **Link-layer switches**

July 1st, 2013 <small>Assessment <em>Chapter 1</em></small>
-----------------------------------------------------------

### Question 1 <small>(5 points)</small>

> Write out the canonical OSI 7-layer stack from highest to lowest:

-   Layer 7: **Application**
-   Layer 6: **Presentation**
-   Layer 5: **Session**
-   Layer 4: **Transport**
-   Layer 3: **Network**
-   Layer 2: **Link**
-   Layer 1: **Physical**

### Question 2 <small>(5 points)</small>

> Consider an application that transmits data at a steady rate (for
> example, the sender generates an $N$-bit unit of data every $k$ time
> units, where $k$ is small and fixed). Also, when such an application
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

### Question 3 <small>(7 points)</small>

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
        <th>
Offline Application
</th>
        <th>
Utilizes Network Access
</th>
        <th>
Software as a Service/Cloud Application
</th>
    </tr>
    <tr>
        <td>
Google Maps
</td>
        <td></td>
        <td></td>
        <td>
<i class="icon-ok"></i>
</td>
    </tr>
    <tr>
        <td>
Bittorrent
</td>
        <td></td>
        <td>
<i class="icon-ok"></i>
</td>
        <td></td>
    </tr>
    <tr>
        <td>
Microsoft Office
</td>
        <td>
<i class="icon-ok"></i>
</td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>
Mozilla Firefox
</td>
        <td></td>
        <td>
<i class="icon-ok"></i>
</td>
        <td></td>
    </tr>
    <tr>
        <td>
Solitaire
</td>
        <td>
<i class="icon-ok"></i>
</td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>
Adobe Photoshop
</td>
        <td>
<i class="icon-ok"></i>
</td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>
Yahoo! Mail
</td>
        <td></td>
        <td></td>
        <td>
<i class="icon-ok">
</td>
    </tr>
</tbody>
</table>

### Question 4 <small>(3 points)</small>

The network core is defined as:

1.  The technicians and administrators in charge of the network's
    computers.
2.  The collection of routers, switches, and network links responsible
    for routing packets from host to host.<i class="icon-ok"></i>\
3.  The collection of web servers, email servers, and personal computers
    connected to the network.
4.  The telecommunication (telecom) companies responsible for the
    majority of the packet routing performed in the network.

### Question 5 <small>(10 points)</small>

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

July 1st, 2013 <small>Homework: <em>Simple Socket Programming</em></small>
--------------------------------------------------------------------------

### Overview

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

### Specifics of Operation

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

### Grading Outline

-   Source code organization and comments: 30%
-   Reading command-line parameters: 10%
-   Establishing socket to the server based on parameters: 20%
-   Reading user input and sending it to the server: 15%
-   Reading server response and printing it to the user: 15%
-   Closing all Sockets/IOStreams before exit: 10%

### Hints and Suggestions

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

July 1st, 2013 <small>Project \#0</small>
-----------------------------------------

### Updates

Before jumping into the project I would like to mention one thing. Most
of the time your first attempt at a software project is either too slow,
too buggy, or is difficult to maintain/expand. Be prepared to throw away
the first versions of most of your code. You can even plan to have them
as throw-aways. You don't waste time doing this because you learn where
you can make improvements in your final version.

### Theory of Operation

In this project, you will build a simple BitTorrent(BT) client which
will serve as the foundation for a fully-featured BT client you will
build in later assignments. For project 1, your client will load a
.torrent file, interface with a tracker and a single peer and will
download a single file (JPEG) from that peer. When the file is finished
downloading, you will save it to the hard disk. All communication will
be done over TCP.

The file your program will read in is a .torrent file containing
metadata for the file to be downloaded.

### Assignment Specifics

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

### Files Available

There are several files available in the Resources section of the site
in the folder "Project files."  The most important is the "Project 1
torrent file" (project1.torrent), which is the "testbed" torrent you can
use to develop your client.  The other files available are helpful, but
not necessary.  Be sure to check the resources section for updates or
changes as the semester progresses.

### Programming Style

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
    a O(n\*lg(n)) algorithm than a O(n^2^) algorithm.
-   Encapsulation - Encapsulation is a useful feature of object-oriented
    languages, and so you should try to write classes that expose as
    little as possible. This way you can change the implementation of a
    class without affecting the rest of your program.

### Bencoding (Pronounced "Bee Encoding")

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

### Communication With the Tracker

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

### Communicating With the Peer

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

### The Write-Up

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

### Submitting the Project

The project should be submitted through Sakai.

-   Make sure your name is in comments at the top of every file
    submitted.
-   The "main" method should be in a file called RUBTClient.java.
-   The write-up in HTML or PDF format saved as a writeup.
    <html/pdf>
    .
-   All files should be submitted as a compressed archive. Acceptable
    formats are `.zip`, `.tgz`/`.tar.gz`, and `.tar.bz2`. This file
    should be named `<NetID>.<EXT>`, where `<NetID>` is your eden NetID
    and `<EXT>` is the file type extension.

### Grading

-   Programming Style: 15%
-   Correctly setting up TCP sockets/connections: 15%
-   Correctly interfacing with the tracker: 20%
-   Correctly interfacing with the peer: 20%
-   Correctly downloading and verifying the file: 20%
-   Write-up 10%

### Resources

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

### Frequently Asked Questions

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


