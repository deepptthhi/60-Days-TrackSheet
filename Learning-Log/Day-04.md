# Day 4 – Python Conditional Statements, Loops & Git

## What did I learn?

Today I learned how Python programs make decisions and repeat tasks.

I learned different types of conditional statements like `if`, `if-else`, `if-elif-else`, nested `if`, shorthand `if`, and shorthand `if-else`. I also learned how loops work, including `for` loops, `while` loops, `while True`, and nested loops.

Along with loops, I learned about `range()`, `break`, `continue`, and `pass`, and how they change the way a loop behaves.

I also spent some time improving my Git knowledge by learning how to rename the last commit and update it on GitHub correctly.


## What new concepts did I understand?

### Python Conditional Statements

The biggest thing I understood today is that a program doesn't always execute every line one after another. It can decide what to do based on different conditions.

I also understood how comparison operators return either `True` or `False`, and those values decide which block of code gets executed.

At first, all the different `if` statements looked almost the same, but after writing examples for each one, I understood where each type is useful.

### Python Loops

Loops made me realize how much time they can save by avoiding repeated code.

Instead of writing the same code multiple times, I can write it once inside a loop and let Python repeat it automatically.

I also understood the difference between `for` and `while` loops. A `for` loop is useful when I already know how many times something should repeat, whereas a `while` loop is useful when the loop depends on a condition.

Learning about `break`, `continue`, and `pass` also helped me understand that loops don't always have to run in the same way. We can stop a loop, skip an iteration, or leave a placeholder when needed.

### Git

Today I learned that a Git commit message isn't permanent.

If I make a mistake in the latest commit message, I can change it using:

```bash
git commit --amend -m "Added Day 4 learning log file"
```

After changing the commit message, Git creates a **new commit with a different commit ID (hash)**.

Since I had already pushed the previous commit to GitHub, a normal `git push` didn't work because my local commit history no longer matched the remote repository.

To update the commit on GitHub, I used:

```bash
git push --force-with-lease
```

I learned that `--force-with-lease` is safer than `--force` because it checks whether the remote branch has changed before updating it. This helps avoid accidentally overwriting someone else's work.

While exploring this further, I also found out that `git commit --amend` is mainly used for changing the **most recent commit**. If I ever need to rename or edit an older commit, Git provides another feature called **interactive rebase (`git rebase -i`)**.

I haven't practiced interactive rebase yet because it's a more advanced Git feature that rewrites commit history. For now, I understand when to use `git commit --amend`, and I'll learn interactive rebase in more detail later.


## What computer/software engineering fundamentals did I learn today?

Today's topics helped me understand that programming isn't just about writing code.

A program needs to make decisions based on different situations, and it also needs an efficient way to repeat tasks without writing the same code over and over again.

Conditional statements and loops are two of the most basic concepts because almost every real program uses them.

I also learned a little more about version control. Even small things like writing meaningful commit messages and knowing how to safely update commits are part of a good development workflow.


## What changed in my thinking?

Before today, I thought conditional statements and loops were just basic Python syntax that I had to learn.

Now I understand that they are the foundation of programming logic. Every program needs to make decisions and repeat tasks, and these concepts make that possible.

I also realized that Git isn't only about saving code. It also lets me improve my commit history by correcting mistakes when needed.

I'm still learning the basics, but I can already see how these concepts will be useful when I start solving programming problems and building projects.

Right now I understand the concepts, but I think they'll become more natural once I use them in practice.


## Today's One-Line Summary

> "Today I learned how conditional statements and loops help to control the flow of a program, and how to safely update Git commit messages."