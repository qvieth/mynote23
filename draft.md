## the art of clean code <- good book that has many idea to discuss

my best friend recommended me clean code

- [ ] the problem with doing book summary is that book like 600 pages to summarize it properly it would take me to write like at least 50 pages, a summary like this would be only useful for me to read meself not suitable for do it on a blog book on simplicity

- my writing goal: summary that make sense and provide useful idea
  - learning -> need feedback

my reader: 2 people: someone who doesn't like coding just find something to read and some how find good ideas, other programmer this is place for you

exhautive endeavor to cover all the point to be honest my summary will only about 20% of the book, what relevant and easy for me and you the reader to access.

Once upon a time, Bill Gates’ parents invited legendary investor Warren Buffett to his family home to spend some time together. In a CNBC interview, Warren Buffett recounts how on this occasion, Bill’s father asked Warren and Bill to write down the secret of their successes

a video suggeseted by the author of the book entitled "One word that accounted for Bill Gates' and my success: Focus" — Warren Buffett
and these 2 guys who may only met twice didn't know what the other one is writing down, both write the same word which was focus.

this book provide 9 principles how to improve your potential as a programmer,.. but many lesson and idea here are also useful in life also many other area
the author seems to use many principle from many other book two of them are famous like 80/20, element of style a book on writing, lean startup

structure the summary into 2 parts:

- productivity related, philosophy
- explicit coder problem, lesson

1. complexity -> regconize complexity
2. 80/20
3. mvp
4. write clean and simple code
5. optimization
6. flow
7. unix philosophy
8. minimilism in ux design
9. focus

- 3 things: goal, feedback, opportunity must go with capacity

# part 1

# 1. complexity -> regconize complexity

In different fields, the term “complexity” comes with different meanings. Sometimes, it’s strictly defined
Other times, it’s loosely defined as the amount or structure of interactions between system components. In this book, we’re going to use it more generically.
We’ll define complexity as follows:
Complexity  “a whole, made up of parts, that is difficult to analyze, understand, or explain”
Complexity describes a whole system or entity. Because of the diffi- culty in explaining this system, complexity causes struggle and confusion. Because real-world systems are messy, you’ll find complexity everywhere: the stock market, social trends, emerging political viewpoints, and big com- puter programs with hundreds of thousands of lines of code—such as the Windows operating system.

- If you’re a coder, you are especially prone to overwhelming complexity, such as from these different sources that we’ll cover in this chapter:
  - Complexity in a project life cycle
  - Complexity in software and algorithmic theory
  - Complexity in learning
  - Complexity in processes
  - Complexity in social networks
  - Complexity in your daily life
- We’re getting kind of abstract here, so let’s have an applicable example!
  Say you want to program a trading bot that buys and sells assets accord-
  ing to a set of sophisticated rules. You could learn lots of useful knowledge
  before starting your project: the basics of programming, distributed sys-
  tems, databases, application programming interfaces (APIs), web services,
  machine learning, and data science and the related mathematics. You
  could learn about practical tools such as Python, NumPy, scikit-learn, ccxt,
  TensorFlow, and Flask. You could learn about trading strategies and stock
  market philosophies. Many people approach these problems with such a
  mindset and so never feel ready to start the project. The problem is that
  the more you learn, the less knowledgeable you feel. You’ll never attain suf-
  ficient mastery in all those fields to truly satisfy your desire to feel prepared.
  Overwhelmed by the complexity of the whole endeavor, you feel like quit-
  ting. Complexity is about to take its next victim: you
- . Complexity is about to take its next victim: you.
  Fortunately, in the chapters of this book, you’ll learn skills to combat
  complexity: focus, simplification, scaling down, reduction, and minimalism.
  This book will teach you those skills.
- Complexity is the enemy of efficiency. The solution here is minimalism: to
  keep your processes efficient, you must radically weed out unnecessary steps
  and actions. It’s very unlikely that you’ll find your processes oversimplified.
- Computer science professor Cal Newport
  talks about this in his excellent book Deep Work: Rules for Focused Success in
  a Distracted World (Grand Central Publishing, 2016). He argues that there’s
  both an increasing demand for work that requires deep thinking—such as
  programming, researching, medicine, and writing—and a decreasing sup-
  ply due to the proliferation of communication devices, opportunities, and
  entertainment systems. If increasing demand meets decreasing supply, eco-
  nomic theory suggests that prices will rise. If you are capable of engaging in
  deep work, your economic value will increase. There has never been a bet-
  ter time for programmers who can engage in deep work.
  Here, too, the
  answer lies in applying radical minimalism to the root of the problem: unin-
  stall social media apps rather than trying to manage consumption, reduce the
  number of projects and tasks you’re involved in rather than trying to do more
  by working more, go deep into one programming language rather than spend-
  ing lots of time switching between many.
- Complexity harms productivity and reduces focus. If you don’t take
  early control over complexity, it will quickly consume your most precious
  resource: time
- Complexity harms productivity and reduces focus. If you don’t take
  early control over complexity, it will quickly consume your most precious
  resource: time

author recommend learning by doing project, don't just read book or watch tutorial => so sad this is what i did mostly in my past
by doing project, we will face lot of complexity, question arises. so the question is how do we combat this: "the answer is simplicity"
If you take only one thing away from this book, let it be this: take a radically minimalistic position in every area you encounter in programming
throughout the remaining part of the book, we will discuss all the following methods:

- chapter 2: Declutter your day, do fewer tasks, and focus your efforts on the tasks that matter. For example, instead of starting ten new interesting code projects in parallel, carefully select one and focus all your efforts on finishing this one project. In Chapter 2, you’ll learn about the 80/20 principle in programming in greater detail.
  on the minimum viable product (see Chapter 3), ship it, and validate
  your hypotheses quickly and efficiently

# 2. 80/20

The 80/20 approach allows you to identify the activities on which you
must focus. Doing more of the success metrics, preferably actionable lead
measures, will increase your professional success, and that’s all that should
matter. Spend less time on all the different tasks. Refuse to die the death of
a thousand cuts
Instead of becoming a “Jack of all trades, master of none,” you gain
expertise in the area that is most important to you. You heavily focus on the
vital few and ignore the trivial many. You lead a less stressful life, but you
enjoy more fruits from your invested labor, efforts, time, and money

- Most players suffer from a lack of focus, and even if they are very
  skilled, intelligent, and well-connected, they have no chance of competing
  against a focused, dedicated, and Pareto-knowledgeable programmer.
  e.g.

Bob may spend his time reading three general books (let’s call them Introduction to Python, Introduction to C++, and Introduction to Java) while Alice
reads three books diving deep into machine learning with Python (let’s call them Introduction to Python, Introduction to Machine Learning with Python, and Machine Learning for Experts). As a result, Alice will focus on becoming
a machine learning expert and can demand a higher salary for her specialized skill set.
By focusing on the success metrics in your industry, you will manipulate the probabilities in your favor. As an 80/20 thinker, you are the house—and the house mostly wins.
80/20 Practice Tips
Figure out your success metrics.
for example writer: words write perday, programmer line of code write perday, researcher number of citation,...
Create a spreadsheet and track your success metric every day. Make it a game to stick to it and surpass yourself. Set a minimum threshold, and don’t end the day until you’ve accomplished the minimal threshold each day. Better yet, don’t start the day until you have!
Figure out your big goals in life.
Look for ways to achieve the same things with fewer resources. -> remove acitvity take 80 percent of the time but only lead to 20 percent of result, If not, can you out- source them? Fiverr and Upwork are cheap ways to find talent, and it pays to leverage the skills of other people.
Reflect on your own successes&failure? What did you do that led to great/bad results? How can you do more of those things?

covers a well-known idea popularized in Eric Ries’ book The Lean Startup
Stealth mode is when you work on a project to completion without seeking any feedback from potential users.
wrong assumption
Unnecessary Complexity
by releasing the package of four features at once rather than
one or two features at a time
, you don’t know whether the market would’ve
accepted, or even preferred, any subset of features
figure 3-4 page 43

stealth mode is unlikely to suceed -> build MVP

# 3. mvp

# 4. write clean and simple code

# 5. optimization

# 6. flow

# 7. unix philosophy

# 8. minimilism in ux design

# 9. focus

# part 2

complexity -> algorithmic complexity
k
complexity in a software development life cycle(SDLC)
six conceptual phases of a software project based on the official Institute of Electrical and Electronics Engineers (IEEE) standard for software engineering. 6 phases are:

1. planning; crucial because it can save you from wasting massive amounts of energy later, The planning phase is a time to apply your newly acquired skill of 80/20 thinking(chapter 2)
2. defining: translating the results from the planning phase into properly specified software requirements.
3. designing: create a crystal-clear picture of how the final software product will look and how it’s built 4. create a crystal-clear picture of how the final software product will
   look and how it’s built, benefit-and-costs ratio is maximized
4. building: The building phase is where many coders want to spend all their time. where the transformation from the architectural draft to the software
   product happens. Your ideas transform into tangible results
5. testing: You still must test the behavior
   of your software product for different user inputs and usage patterns. This
   phase is often the most important of all—so much so that many practitioners
   now advocate the use of test-driven development where you don’t even start to
   implement (in the building phase) without having written all tests.
6. deployment:after The software has now passed the rigorous testing phase. It’s time to deploy
   it!depending on your concrete project, this phase
   requires you to launch the product, create marketing campaigns, talk to
   early users of the product, fix new bugs that will surely come to light after
   being exposed to users, orchestrate the deployment of the software on dif-
   ferent operating systems, support and troubleshoot different kinds of prob-
   lems, or maintain the codebase to adapt and improve over time

algorithmic complexity, a thoroughly researched field, improved algorithms produced from this research are among the
most valuable technological assets of humanity, allowing us to solve the
same problems with fewer resources, over and over. by using the algorithm from these reserch We truly stand on the shoulders of giants.

cyclomatic complexity
code with an if statement would result in two independent paths
through your code, so it would have a higher cyclomatic complexity than flat
code without any branching like that in an if statement
figure to show cyclomatic complexity
however, cyclomatic complexity ignores the cognitive complexity
that comes from, say, nesting multiple for loops compared to a flat for loop.
That’s why other measures such as NPath complexity improve upon cyclomatic
complexity. To sum

- complexity in learning: skill to combat complexity: focus, simplification ,scaling down, reductiona, minimilism
- complexity in process
- complexity in your daily life
  - The purpose of this book is to increase the productivity of your program-
    ming efforts. This can be interrupted by your own personal daily habits
    and routines. You must tackle the daily distractions and the constant com-
    petition for your valuable time.
- The purpose of this book is to increase the productivity of your program-
  ming efforts. This can be interrupted by your own personal daily habits
  and routines. You must tackle the daily distractions and the constant com-
  petition for your valuable time.
  There has never been a bet-
  ter time for programmers who can engage in deep work.
  Now, the caveat: it has become almost impossible to engage in deep
  work if you don’t brutally enforce it. The external world demands your
  attention. Your colleagues pop into your office. Your smartphone demands
  your attention every 20 minutes. Your inbox pops up a new email dozens of
  times a day—each asking for a slice of your time
- Deep work results in delayed gratification;
- However, what you desire in most moments is instant gratification. Your subconsciousness often looks for ways to escape from the effort of deep work
- The promise of delayed gratification becomes less and less attractive compared to the happy, colorful, and lively world of instant gratification.
- Your efforts to stay focused and productive are prone to dying the
  death of a thousand cuts
- Here, too, the
  answer lies in applying radical minimalism to the root of the problem: unin-
  stall social media apps rather than trying to manage consumption, reduce the
  number of projects and tasks you’re involved in rather than trying to do more
  by working more, go deep into one programming language rather than spend-
  ing lots of time switching between many.
- complexity harms productivity and reduces focus. If you don’t take
  early control over complexity, it will quickly consume your most precious
  resource: time.
- By learning
  how to handle complexity, by keeping it simple, you’ll be able to fight com-
  plexity and give yourself a powerful competitive advantage.
  In Chapter 2, you’ll learn about the power of the 80/20 p
  The principle says that the majority of effects come from the minority of causes.
  By focusing on the vital few rather than the trivial many, you can increase your
  productivity by a factor of 10, even 100. easy to understand but can be unintuitive to apply it to your daily life
  -> productivity -> putting your effort to few
