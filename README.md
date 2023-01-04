# 42-philosophers
Eat, Sleep, Spaghetti, repeat. This project is about learning how threads work by precisely timing a group of philosophers on when to pick up forks and eat spaghetti without dying from hunger.


## Starting ##

```bash
# Compile the program
make

# To run (example)
./philo 5 800 200 200

# To remove objects and executable
make fclean
```

## Links ##
- [Dining Philosophers Problem 1](https://www.youtube.com/watch?v=NbwbQQB7xNQ)
- [Proses and thread](https://www.youtube.com/watch?v=R_EgvEOhV9U)
- [Proses and thread](https://www.youtube.com/watch?v=KBLfAuen-eA)
- [Proses and thread](https://www.youtube.com/watch?v=pIp4OXhnB0U)
- [what is mutex](https://medium.com/@gokhansengun/semaphore-mutex-ve-spinlock-nedir-ve-ne-i%C5%9Fe-yarar-ba552a17c03#:~:text=Mutex'ler%20uygulaman%C4%B1n%20yaz%C4%B1ld%C4%B1%C4%9F%C4%B1%20dil,b%C3%B6lgesi%20Critical%20Section%20olarak%20adland%C4%B1r%C4%B1l%C4%B1r.)
- [Thread logic](https://www.cs.cmu.edu/afs/cs/academic/class/15492-f07/www/pthreads.html)
- [What are the differences between process and thread? ](https://www.geeksforgeeks.org/multithreading-c-2/)

## Starting ##
```bash
Threads that the operating system runs concurrently are called processes. Processes can also have threads running concurrently within themselves, and they are also called Threads.

Synchronization is needed from time to time between different processes or between Threads in the same process because these Threads want to access a shared resource provided by the operating system or maintained within the process itself to perform their tasks. As an example, let's take the case where Threads wants to write logs to a log file or screen. If two Threads try to write to the log file at the same time, the logs written to the file will be mixed up and become unreadable. Here a mechanism is needed to queue Threads to write to the log file.

Mutex (MUTual EXclusions) is designed to provide exactly this mechanism. Mutexs are simple data structures provided by the language in which the application is written and the Runtime. For each resource shared by different Threads, a Mutex is created to regulate access to the resource. The code region in which the shared resource is accessed is called the Critical Section. Thread with resource tries to take ownership of Mutex (Acquire). If the mutex is not currently held by another Thread, it takes the Thread Mutex, enters the Critical Section and uses the relevant resource. In the other case, that is, if the Mutex is currently being used by another Thread, the second Thread is put on hold by the processor. When the Thread holding the Mutex finishes the Critical Segment and leaves the Mutex, the Thread awaiting the release of the Mutex awakens and takes ownership of the Mutex and gains access to the shared resource by entering the Critical Segment.

```
