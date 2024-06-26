Dining Philosophers Problem

Problem Statement There are five silent Persons (P1 – P5) sitting around a circular table, spending their lives eating and thinking. There are five forks for them to share (1 – 5) and to be able to eat, a Person needs to have forks in both his hands. After eating, he puts both of them down and then they can be picked by another Person who repeats the same cycle. The goal is to come up with a scheme/protocol that helps the philosophers achieve their goal of eating and thinking without getting starved to death.

Solutions:

AltDiningPhilosopher.java This solution uses a synchronized block to control access to shared resources (forks). Each philosopher will wait for their turn to pick up the forks and eat, ensuring that no two philosophers eat simultaneously and preventing starvation.

Key Features:

Each philosopher has a unique ID.
Synchronization ensures that only one philosopher can pick up the forks at a time.
Philosophers alternate between thinking and eating.
The program ensures that all philosophers get a chance to eat without any deadlock.
DiningPhilosopher.java This solution uses java.util.concurrent.locks.Lock for each fork and ensures that each philosopher picks up the left fork first, then the right fork. This approach prevents deadlock by ensuring that no two adjacent philosophers can pick up forks at the same time.

Key Features:

Uses ReentrantLock for each fork.
Philosophers pick up the left fork first, then the right fork.
Implements a mechanism to stop philosophers after a certain time.
Ensures that all philosophers can eat and think without getting starved.
How to Run

Clone this repository to your local machine.
Navigate to the directory where you have saved the files.
Compile the Java files using:
