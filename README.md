Download Link: https://assignmentchef.com/product/solved-comp2560-lab-7-ps-kill-and-signals
<br>
Use shell terminal to launch a GUI-based application to be executed in the background. Here are examples to start image viewer <em>gimp</em> on CS server:

&gt;&gt;&gt;&gt;&gt; gimp &amp;

<h1>&gt;&gt;&gt;&gt;&gt; gimp imagefile.ppm &amp;</h1>

Use command <em>kill -9 pid</em> to terminate this application.

Part II

Repeat the above. This time, do not use the ampersand. The application is executed in fore ground. Open another terminal. Use command <em>ps </em>to find out the process id of the application that you have launched, and then use command <em>kill -9 pid</em> to terminate it.

Part III

Write a C program where two child processes are created using <em>fork()</em>. The parent process and child processes all write into a shared file using system call <em>write()</em>. The file name is given from command line.

Define three strings like this:

buf[0] = “EXAM! EXAM! EXAM!
”;

buf[1] = “HELP! HELP! HELP!
”;

buf[2] = “STUDY! STUDY! STUDY!
”;




The parent process will open the file using <em>open()</em> before the fork. The first child will write the content of <em>buf[0]</em> into the file. Then the second child will write the content of <em>buf[1]</em> into the file. Finally, the parent will write the content of <em>buf[2]</em> into the file and close the file. Add <em>sleep(5)</em> after each <em>write()</em> statement.




Use signal to coordinate the access to the shared file, so that the file is accessed with mutual exclusion.




In addition to writing to the file, both parent and child processes should also write some related information to the terminal according to what the sample shows.

Sample run:


