- Multiple threads in a single program, which improves performance and UX. 
- Own stack, allowing it to perform a separate task independently. 
- Max of 1024 threads

Thread class to create and manage them, they can be started and stopped, but we should not stop them abruptly. 

Runnable interface is very similar as the thread class. 

| Benefits                                                         |
| ---------------------------------------------------------------- |
| Improved performance - Less time to complete task                |
| Improved responsiveness - Background tasks don't block interface |
| Resource utilisation - share resources efficiently               |
| Can be used in many scenarios                                    |
**Thread lifecycle and states**
1. New: created but not started
2. Runnable: ready to be executed by cpu
3. Blocked: waiting for monitor lock
4. Waiting: waiting for condition to be met
5. Timed waiting: waiting for condition for specified time. 
6. Terminated: thread has completed execution. 

Thread interruptions need to be handled gracefully, without causing damage to the system. 

**Synchronisation**
Coordinating access to resources. 
- Prevent race condition
- Ensure data consistency
- Use synchronised methods and blocks

**Callbacks and Async**
- Callbacks: Pass function as parameter to another function at later point in time. 
	- Functional interfaces: Single method. 
	- Lambda Expressions: Anonymous class. 
- Futures: Async features
- Reactive programming

**Synchronous**
- Execute tasks sequentially one after the other
- I/O operations
- Small scale programs (CLI)
- Simple computations (Data and Statistics)
- Simple, modular and testable. 

**Multithreading**