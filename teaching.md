#Teaching Scala to the Statically Challenged

### Index

1. What is this?
2. Who are we teaching?
3. Why dynamic programmers?
4. How to pick a first project
5. General advice
6. Topics to introduce right away
7. Topics to postpone

---

### 1. What is this?

This is a guide for experienced developers who find themselves tasked with introducing Scala to a (probably junior) programmer with no experience in statically-typed languages.

---

### 2. Who are we teaching?

Many software engineers who enter tech from non-traditional backgrounds (bootcampers, self-taught coders, career changers, students who take only a few CS courses) have never worked in statically-typed languages like Java, C, or Haskell.  This guide assumes that the learner you are trying to teach/mentor is already proficient in a dynamic language (Javascript, Python, Ruby, etc.) but has limited understanding of static concepts (explicit typing, compilers, etc.) that are taken for granted in software engineers from traditional backgrounds.

---

### 3. Why dynamic programmers?

Reasons to teach Scala to the dynamic programmer your team just hired:

1. Scala developers don't grow on trees.  It can be easier and cheaper to train your own than to compete for the limited pool of existing Scala devs looking for jobs.
2. Teaching a skill set to someone else is a rewarding experience.
3. Learn through a beginner's eyes.  As they say, the best way to learn is to teach.
4. Expand the diversity of perspectives and experiences on your team; [diverse teams perform better](https://hbr.org/2016/11/why-diverse-teams-are-smarter).
5. Mold your teammates in your image.
6. You might end up creating the author of your future favorite library.
7. As a community, Scala could benefit from more "silly" questions.  Beginners question assumptions that experts take for granted.  Also, when your learner asks basic questions online they lower the barrier to entry for other Scala learners.  This can ultimately result in a larger pool of experienced Scala devs for your team to hire from.

---

### 4. How to pick a first project

The ideal first project is:

- Small
- Straightforward
- Not reliant on domain-specific knowledge that takes more than half an hour to explain

In my experience, writing unit tests is an excellent way to start.  Unit tests are simple to understand, give your learner quick wins to build their confidence, expose them to your code base, and offer instantaneous feedback.  Give a few examples of what unit tests should look like to get them started.

Next-best are partially-complete projects; you control the high-level structure of the project and they can look to the code you've already written for guidance.

Warm-up exercises can also be a good way to start, but both you and the learner lose the benefits of having them contribute meaningfully from the outset.

I have found that the following don't make good first projects:

- Dependency upgrades
    - What takes you half an hour could take days for someone who isn't familiar with your code/deployment process/dependencies.
- Giant tasks that will take weeks to complete
- Bug fixes
- Concepts new to you
    - Who can they turn to for help?
    - What if they thing you assign isn't actually possible?

---

### 5. General advice

####Dos:

- Ask how they like to learn
    - Don't waste your time on approaches that are less effective for their preferred learning style.
- Encourage questions
    - Remind yourself that basic != bad.  Be glad that they're coming to you for foundational concepts.
- Check in mid-lecture
    - Don't waste time; ask to make sure that they don't already know the concept you're about to teach.
        - Maybe they know it by a different name.
    - Make it clear that you want to know if something is unclear.
        - Power dynamics can make it hard to cut you off, but nobody benefits if you lose them twenty seconds into a twelve-minute lecture because something you said was confusing.
- Dig up resources for them
    - If they got the job, they know how to find resources.  How much faster can you find them?
    - Prevent journeys into rabbit holes by pulling up the docs for them.
- Set project timelines
    - Reevaluate as needed.
- Model good code
    - Write clean code.  Be explicit about types when they might not be clear.  Write tests and readmes and samples.  All the things you should be doing anyway. 
- Introduce them to the community
    - Lighten your load.
    - Speed their learning.
    - Convince them you have friends.
    
####Don'ts:

- Don't say "Martin Odersky has a course on Coursera" and disappear for two weeks
    - Don't do this with any online resource.  It doesn't feel good, and you're wasting their time.
    - Feel free to suggest the Coursera course as a supplementary resource.
- Never say the word "just"
    - What feels obvious to you may not be to them - be careful about how your tone and word choice affect their understanding of your expectations.
- Don't mistake inexperience for incompetence
- Don't mistake vocabulary ignorance for conceptual ignorance


---

### 6. Topics to introduce right away

- Types and type signatures
- Tools
    - Just one IDE (preferably something fully-featured like IntelliJ)
    - Just one build tool
    - Just one test library
- FP basics
    - val not var
- Object / Class / Trait / Method / Type
- Compiler basics
- Options

---

### 7. Topics to postpone

- Monads
- Implicits
- Currying
- Anonymous functions
- Case classes
- Recursion
- Compiler intricacies

You may feel that some of these are so fundamental to Scala that they should be introduced early.  I suggest instead introducing them as they come up naturally in your code reviews.  For example, case classes aren't going to be particularly meaningful until you show your learner how they can replace the (String, Option[Int], Array[(String, List[(String, Double)])]) that they just put into their code.
