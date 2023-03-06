
 #Lab03-1
 
 
The program sets up a signal handler using the signal() function to handle the SIGALRM signal. When the program receives the SIGALRM signal, the function handler() is called, which prints "Hello World!" and sets an alarm for 1 second using the alarm() function.
In the main() function, the signal() function is used to associate the SIGALRM signal with the handler() function. Then the alarm() function is called to set an initial alarm for 1 second.
The program then enters an infinite loop that sleeps for 1 second using the sleep() function and prints "Turing was right!" to the console. Since an alarm is set to go off every 1 second by the signal handler, the program will print "Hello World!" every second, in addition to the "Turing was right!" message.
The program continues to run until it is interrupted or terminated by an external signal.



 #Lab03-2.c
 

The program sets up two signal handlers: handler() and handler2(). The handler() function handles the SIGALRM signal, which is set to be triggered every 1 second by the alarm() function. When the SIGALRM signal is received, the handler() function prints "Hello World!", increments the counter variable, and sets another alarm for 1 second using the alarm() function.
The handler2() function handles the SIGINT signal, which is triggered when the user presses CTRL+C in the terminal. When the SIGINT signal is received, the handler2() function prints the total time elapsed since the program started (in seconds) using the counter variable and exits the program using the exit() function.
In the main() function, the signal() function is used to associate the SIGALRM signal with the handler() function and the SIGINT signal with the handler2() function. The alarm() function is then called to set an initial alarm for 1 second.
The program then enters an infinite loop that sleeps for 1 second using the sleep() function and prints "Turing was right!" to the console. Every second, the SIGALRM signal is triggered, which calls the handler() function to print "Hello World!" and increment the counter variable. The program continues to run until the user interrupts it by pressing CTRL+C or until it is terminated by an external signal. When the program is terminated, the handler2() function prints the total time elapsed since the program started and exits the program.




