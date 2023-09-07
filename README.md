# Name: Ash Hoskins - Student #S559245
# Course CS-44-671
# Module 2 Assignment 1

# Goal: Concurrent Processing and Shared Resources.

## Module 2 Coding

At the end of this module students will be able to:

1. Define concurrency and multiprocessing. (L03)
2. Describe multiprocessing issues and mitigations. (L03)
3. Execute a script using multiprocessing to access a shared resource. (L04)
4. Introduce locking issues on a shared resource. (L04)
5. Write a script generate a stream from data-at-rest. (L02)
 



# streaming-02-getting-started
In this project:

You'll review how one multiprocessing example behaves when tasks are quick and sharing goes well (generally).
You'll change to using longer-running concurrent tasks and explore what happens.
You'll implement a scaffolded process that streams from a csv file. 
You'll write your own streaming process that reads from a unique csv data source of your choice. 
 

Multiprocessing
In streaming, we often have multiple processes running concurrently (search this term as needed).

In this example, we run all processes in a single terminal window using the multiprocessing package from the Python standard library.
In later assignments, we'll start up different terminal windows for different applications. You'll want to know both approaches for maximum benefit.
When running multiple terminals (later), you can use the integrated terminal in VS Code, or in Terminal (on a Mac). Explore the options and see what works best for you. 
 

Starter Repository
Read the code and comments carefully - the code and comments are the main textbook for the course. We are very "hands on". 

https://github.com/denisecase/streaming-02-multiple-processesLinks to an external site.
Additional resources:

Module 0: Course Text
Streaming and Sockets
Module 0: FAQ
 

Do These General Tasks (Every Project)
Fork the repo into your GitHub account.
Clone your new repo down to your local machine.
Run the about file to generate some information about your machine and your local Python setup. 
Execute the project code files. 
Read the code and comments carefully.
Modify the examples as requested.
Document your results - don't forget this key step! 
Commit and push / sync your changes back up to GitHub
Customize your README.md to reflect the focus, add your name and notes. 
Customize and comment your code as recommended by the Python Style GuideLinks to an external site..
Demonstrate your project and communication skills.
 

Task 1 - Concurrent Multiprocessing Example (quick processes)
Explore the output from concurrent processes.

Were activities performed in order? Does the order vary on multiple runs? What would happen if a process - or machine - dies? Is information lost? These considerations are important when deciding how to implement distributed analytics solutions. 
 

Task 2 - Concurrent Multiprocessing Example (longer-running processes)
Increase the time and see how things go.

What happens? 
 

Task 3 - Stream Processing Example
Stream processing is different because the data is unbound - it could be infinite. Think tweets being generated in real time, or sensor data, like GPS, temperature, stocks, or web analytics. These are examples of "data in motion".

copy process_streaming_0.py from the Module 1 repo.
copy the other file you need to make it work. Hint: read the code. Look for the name of another (data) file to read from.
This will simulate an infinite source of information, process it, and output a continuous steam of information. If all goes well - it will run for quite a while. Many processes run continuously until a failure occurs or the user stops the process by shutting it down, or interrupting it with Control C (to close).  See the Module 0: FAQ for more help. 

 

Task 4 - Custom Stream from CSV Script
Stream your own unique CSV data by modifying the example approach provided.

Create a new Python script in your repo named process_streaming_yourname.py
Create a new CSV file in your repo using any data you like.
Stream from your CSV file into a new file named out9.txt.
Use the examples provided as the basis for your implementation. 
Generate one record every 1-3 seconds. Let it run long enough to write ten or more records to out9.txt.
For the output file, either open a file for writing and have your code write to the file (as we did in Project 1) -  or you can manually copy and paste into the output file - or use logging like we did in project 1.  There are many output options. 
Tell us which output option you chose - and why - in your submission.
What changes did you have to make when reading from a different csv file? See Hint hereLinks to an external site.. 

Task 5 - Learn about UDP and TCP 
Python provides a standard library named socket that allows for the creation of both UDP and TCP sockets. You want to (a) be aware of UDP vs TCP and (b) be able to read and understand a project using either. 

UDP
UDP stands for User Datagram Protocol, and it is connectionless -  you just send the data without establishing a formal connection. 
UDP is the easiest - just chunk up the data and send the chunks.
UDP is somewhat casual - like getting multiple packages shipped from the Amazon warehouse to your porch. 
UDP doesn’t guarantee delivery, order of the packets, or error checks.
TCP
TCP (Transmission Control Protocol) is connection-oriented, ensuring data integrity, order, and delivery acknowledgment.
TCP is used for many of the primary internet functions, including web browsing and email.
TCP includes a more elaborate set of greeting protocols conducted before transmission begins - much like the bows, courtesies, and/or handshakes often followed when beginning important diplomatic conversations. 
To learn more about the TCP protocol, see the quiz this module and do a bit of searching.
Learning many of the popular libraries, packages, and modules are why companies ask for years of experience in a language. The language syntax takes only hours or days to learn, but becoming aware of all the libraries available can take many years. Learning how to learn the ones you need is an important skill.


> 