# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 25, 2026 - 11:45 PM]

**What I did:**
Setting up GitHub and VS Code.

**Details:**
I created my GitHub account and forked the project. I downloaded the files to my computer and changed my student ID in the code. I also installed VS Code to start coding.

**Challenges:**
It was hard to use VS Code because I am used to NetBeans. Also, downloading the files and connecting them to GitHub was not easy at first.

**Solution:**
I watched some YouTube videos and used AI  to understand how VS Code works. Finally, I fixed the sync and everything worked.

**Time spent:**
 1 hours.

---

**Entry 2 - [March 26, 2026 - 01:00 AM]**

**What I did:**
Code analysis and understanding the project structure.

**Details:**
I spent time reading the code to understand it. 

**Challenges:**
The code was a bit difficult to read because the grapical code was mixed with the logic. Also, I had an "Encoding" problem where the output characters in the terminal looked strange and unreadable.

**Solution:**
I focused more on the logic parts of the code and ignored the grapical parts  I started to understand the flow of the program after some time. For the encoding issue, I couldn't find a perfect fix, but I learned how to track the logic through the code itself.

**Time spent:**
 30 minutes.

---

**Entry 3 - [March 26, 2026 - 09:30 AM]**
**What I did:**
 Adding the Priority feature.

**Details:**
I added a new priority variable (integer) to the Process class and updated the constructor. I also created a method to get the priority value. Then, I updated the Main and Scheduler classes to print the priority for each process.

**Challenges:**
The code was complex because it was already built with many connections between classes. Also,the method     ** random.nextInt()**      was new to me. I had to research  to understand how to use it  to genrate and choose the boundries 

**Solution:**
I searched for the Random class in Java documentation to understand how it works. Then, I carefully added my code in the right places without breaking the existing parts.

**Time spent:**
 40 min.

---

**Entry 4 - [March 26, 2026 - 10:20 AM]**
**What I did:**
 Implementing the Context Switch counter.

**Details:**
This was the easiest part because it is basic Java logic. I created a static variable Counter before the main method. Then, I added the increment code ++ at the end of the while loop in the scheduler to count every time the CPU switches. Finally, I added a print statement to show the total count.

**Challenges:**
The main challenge was making sure the counter is in the right place so it only counts real switches and doesn't reset.

**Solution:**
I used a static variable to keep the value safe during the program execution and placed the print statement after the loop finishes.

**Time spent:**
 30 minutes.

---

**Entry 5 - [March 26, 2026, 11:00 AM*]**
**What I did:**
Added time tracking futrue to calculate the waiting time for each process.

**Details:**
 I used a built-in Java method called System.currentTimeMillis() as it counts the time into queue also. I created a method named markEnteredQueue() to save the exact time a process goes into the ready queue. Then, I created another method called markStartedRunning() to measure how much time passed before the process actually started running.

**Challenges:**
The hardest part was understanding how the built-in System.currentTimeMillis() method works. It was confusing to figure out how to use it because it was new to me.
Solution:

**Time spent:**
30 minutes.

---

**Entry 6 - [March 26, 2026, 11:35 AM]**
**What I did:**
Final testing of the scheduler simulation and pushing the code to GitHub.

**Details:**
I ran the program several times to make sure everything was working perfectly. I checked the Round Robin logic, the context switch counter, and the new waiting time calculations. I prepared the code for submission. I committed the final changes and pushed the project to my GitHub repository.


**Time spent:**
15 minutes.

---

**Summary**

**Total time spent on assignment:**
 3 hours and 25 minutes.

**Most challenging part:**
 The hardest part was understanding how to calculate the waiting time for processes that stop and start multiple times. It was confusing to figure out how System.currentTimeMillis() works and how to use it to subtract the exact time a process spent in the ready queue without resetting the total time.

**Most interesting learning:**
 Seeing how a CPU scheduler actually works behind the scenes! It was very interesting to learn how the Round Robin algorithm uses a queue to switch between processes, and the difference between giving a process a specific time slice (run()) versus letting the last process finish everything at once (runToCompletion()).

**What I would do differently next time:**
 Next time, I would write down the math and logic on a piece of paper first before typing the code (especially for the time calculations). I would also try to solve the terminal encoding issue early on so the output looks perfect from the beginning. 