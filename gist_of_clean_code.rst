=========================
Gist of Clean Code (book)
=========================

**Clean Code - by Robert C Martin** is a book that I went through recently. This is one of the most well structured and well written technical books I have ever read. I have gathered some points to share the gist.


​​Why to read this?
-------------------


Generally debugging a bad piece of code consumes more time than developing it. A developer should be able to visualize the amount of time to write good code and estimate accordingly. Not doing so, most of the times will often incur huge and unforeseen expenses and the author(not me :P) considers such acts as unprofessional too.

​​How to avoid that?
--------------------

- Probably the following are the ones you have come across many a times: SINGLE RESPONSIBILITY PRINCIPLE and DON'T REPEAT YOURSELF. Avoid giving ​a ​class too many responsibilities and make templates to avoid repeating the code.

- Make classes, functions(methods) and variables name self explainable.​ We can do that by starting to give Nouns for class names, Verbs for Method names.​

- Avoid Number series naming and Noise words eg: user_registration1, user_registration2 etc or ProductInfo, ProductData etc​​

- Always use pronounceable and Searchable names​.​

- Use named variables for constants. For ex: NUM_OF_SECONDS_PER_DAY for 86400 or DAYS_PER_WEEK for 7.

- Passing more than 3 arguments to a function is not advised. But under some circumstances we might need that completely. For eg: consider the constructor of a class Animal containing its properties has_wings, is_four_legged, has_tail and has_fur we should make these arguments compulsory for the constructor. For the sake of disagreement if we pass a dictionary to the constructor and then extract the variables we might have chances of a partially instantiated object if someone doesn't pass all its properties to the dictionary.

- Passing a boolean into a function is a truly terrible practice. It immediately complicates the signature of the method, loudly proclaiming that this function does more than one thing. It does one thing if the flag is true and another if the flag is false!

- Comments are always failures. So when you find yourself in a position where you need to write a comment, think it through and see whether there isn’t some way to turn the tables and express yourself in the code. Every time you express yourself in code, you should pat yourself on the back. Every time you write a comment, you should grimace and feel the failure of your ability of expression.

- The Newspaper Metaphor: Think of a well-written newspaper article. You read it vertically. At the top you expect a headline that will tell you what the story is about and allows you to decide whether it is something you want to read. The first paragraph gives you a synopsis of the whole story, hiding all the details while giving you the broad-brush concepts. As you continue downward, the details increase until you have all the dates, names, quotes, claims, and other minutia. We would like a source file to be like a newspaper article.
- Don’t Return/Pass Null. In doing so we only might complicate the cases of handling such scenarios.

- If we find ourselves anytime making changes to a code that is heavily dependent on a 3rd party make use of the Inversion of control principle where in we split the code further more into pieces following the Single Responsibility Principle. This way we can have less code that is dependent and more control if some change needs to be accommodated.
- Last but not least If you have tests, you do not fear making changes to the code! (I personally feel this one the most difficult!)

​​What should I do now?
-------------------------


We all should admit that no one can write clean code​ at one go​. We all have broken the rules at one point or another. To write clean code we have to write dirty code at first and then clean it. ​Always remember "​​Bad schedules can be redone, Bad requirements can be redefined but Bad code just rots and ferments sitting there dragging teams down".


