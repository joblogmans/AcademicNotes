Reading material lecture 1.

Question: Do software life- cycle processes (henceforth simply called software processes) benefit software design? Yes! However, sometimes they don't work together well and either can start to smell bad due to the other.

Three software design smells:
1. Duplicate abstraction (either identical name or identical implementation)
2. Insufficient modularization
3. Multipath hierarchy - arises when a subtype inherits both directly and indirectly from a supertype, causing unnecessary inheritance paths in the hierarchy.

Example of the interplay between process and design: expert team has to review all code changes, the other team will avoid this process as much as possible. Refactoring was deemed inferior to functionality changes, so refactoring didn't happen.

Make sure to improve the process in such a way that benefits the development in the long run. Unnecessary restrictions will only bite you later.