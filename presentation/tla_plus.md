TODO: 
- https://lamport.azurewebsites.net/video/intro.html
- Matts paper (and clock example)
- https://www.youtube.com/watch?v=l9XZYI3jta0 (nice case of helicopters, and XP)
- https://www.youtube.com/watch?v=_9B__0S21y8 (banking account model)
- - Amazon Paper on using TLA+: https://cacm.acm.org/research/how-amazon-web-services-uses-formal-methods/

----

From Amazon paper:

On learning about TLA+, engineers usually ask, “How do we know that the executable code correctly implements the verified design?” The answer is we do not know. Despite this, formal methods still help in multiple ways:

- Get design right. Formal methods help engineers get the design right, which is a necessary first step toward getting the code right. If the design is broken, then the code is almost certainly broken, as mistakes during coding are extremely unlikely to compensate for mistakes in design. Worse, engineers are likely to be deceived into believing the code is “correct” because it appears to correctly implement the (broken) design. Engineers are unlikely to realize the design is incorrect while focused on coding;

- Gain better understanding Formal methods help engineers gain a better understanding of the design. Improved understanding can only increase the chances they will get the code right; and

- Write better code. Formal methods can help engineers write better “self-diagnosing code” in the form of assertions. Independent evidence10 and our own experience suggest pervasive use of assertions is a good way to reduce errors in code. An assertion checks a small, local part of an overall system invariant. A good system invariant captures the fundamental reason the system works; the system will not do anything wrong that could violate a safety property as long as it continuously maintains the system invariant. The challenge is to find a good system invariant, one strong enough to ensure no safety properties are violated. Formal methods help engineers find strong invariants, so formal methods can help improve assertions that help improve the quality of code.

----

Another idea from Amazon papaer:
call the presentation "Debugging designs"
