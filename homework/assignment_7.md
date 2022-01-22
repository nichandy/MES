---
date: Jan 22nd, 2022
title: Exercise 7
author: Nick Handy
---

### Exercise 7
- Each chapter in the book ends with an interview question followed by the analysis of what an
interviewer would look for in an answer. Write one of these yourself.
- Start with an interview question you have asked or one that you’ve been asked (or one from the
internet). Then write up what an interviewer would look for in an answer. Be specific about how
the interviewer might help the interviewee if they get stuck.

---

### Interview Question
> 1. What does the keyword volatile mean? Give three examples of its use.

The question indicates whether a candidate has done embedded systems programming as opposed to c programming. The `volatile` keyword plays an important role in dealing with hardware, interrupts, RTOSes etc. If the candidate answers correctly, then the interviewer can probe a little deeper by asking about specific situations where volatile is used. For example:
    
> 2. Can a parameter be both `const` and `volatile`?

Additional questions like this, can show if the candidate has a deeper understanding of the significance of `volatile`. 


### Answers

1. A `volatile` variable can change unexpectedly. The compiler should make know assumptions about the value of the variable and should not optimize it out. Examples:
    - Hardware registers in peripherals (ex. status registers)
    - Non-stack variables referenced within an interrupt service routine
    - Variables shared by multiple tasks in a multi-threaded application

2. Yes, a parameter can be both `const` and `volatile`. The parameter may change unexpectedly and the program should not attempt to modify it. (ex. read-only status register)