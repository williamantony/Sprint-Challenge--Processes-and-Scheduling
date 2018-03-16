  
## Sprint - Processes & Scheduling
### Answers


1. List all of the main states a process may be in at any point in time on a standard Unix system. Briefly explain what each of these states mean.

    * **CREATED**: New process created by scheduler, and added to the process table.
    * **READY**: Process that is *waiting* for execution
    * **RUNNING**: Process that is currently *running*
    * **BLOCKED**: Process that is currently put *on-hold*
    * **TERMINATED**: Process that is killed, and removed from the process table.

1. What is a Zombie Process? How does it get created? How does it get destroyed?

    **Zombie Process** is a process that has completed execution, but it remains in the process table. This happens when a child process is required to let its parent process know about its exit status. When the parent process is notified about its exit (requires parent to call wait()), the zombie process is destroyed and removed from the process table.

    >Note: a zombie process cannot be terminated by `kill -9` command, because it's already dead.

1. Describe the job of the Scheduler in the OS in general.

    **Scheduler** is responsible for managing that processes in the Operating System. It manages the order of operations based on priority and allocated system resources.

1. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.

    **Round-Robin** is a first-in-first-out (queue) scheduling algorithm. It doesn't care about priority, it executes processes in the order they are enqueued.

    **Multi-Level-Feedback-Queue** is a scheduling algorithm that give preference to short-running & I/O bound processes. It also separates processes into categories based on their processing needs.
