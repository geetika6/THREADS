# THREADS
To break the process into threads

TODO 
To solve problems with multiple threads
http://stackoverflow.com/questions/22881045/2nd-thread-not-able-to-receive-messages-via-message-queue-sent-by-thread-1-in-c

Also implement client server app using thread
1. To create Server which check for shared mem, semaphore etc 
Eg in first case:If we use shared mem:

2. spawns thread for every operation to recieve data when there is any new entry and save in local mem befor sending to procssing client
        |_Shared_mem| |__Semaphore on it| 
|RC1
|RC2
|RC3

when RC1 writes it lowers semaphore to 0 and then when server reads it it releases this Semaphore.
so there will be 4 threads for 4 operations
3.Main thread selects the thread to be created with switch case
now after completing the processing , the result is stored in another Shared mem

4.The sginal for that particular client is set
RC keeps waiting for the signal
When it receieves this signal it reads data from Shared mem



