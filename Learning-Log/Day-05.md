# Day 5 – Python Strings, Lists, Tuples & Git

## What did I learn?

Today I learned about **strings, lists, and tuples** in Python.

I started with strings and learned how indexing and slicing work. I also practiced a few string methods like `upper()`, `lower()`, `strip()`, `split()`, `join()`, and `replace()`. Along the way, I learned two ways of formatting strings using **f-strings** and the `.format()` method.

After that, I moved on to lists. I learned how to create a list, access elements, use indexing and slicing, and go through a list using both `for` and `while` loops. I also practiced methods like `append()`, `insert()`, `remove()`, `pop()`, `sort()`, `reverse()`, `extend()`, `copy()`, and `clear()`. I also came across **list comprehension**, which is a shorter way to create a list.

Towards the end, I learned about tuples. I understood that they are similar to lists, but they cannot be changed after they are created.

I also spent some time learning a few Git commands for removing or undoing commits that have already been pushed to GitHub.

## What new concepts did I understand?

### Python Strings

Before today, I mostly used strings only for printing text.

After trying different methods, I realized that Python already has many built-in functions that make working with strings much easier. Instead of writing everything manually, I can use these methods whenever I need them.

I also understood the difference between indexing and slicing. Indexing gives me a single character, while slicing gives me part of the string.

### Python Lists

Lists became much easier once I started writing programs instead of only reading about them.

The biggest thing I understood is that lists are **mutable**, so I can add, remove, or update elements whenever I want.

I also practiced different ways of looping through a list. Using `range()` with `len()` was new to me, but after trying a few examples, I understood why it is useful.

List comprehension looked confusing at first, but after writing a few simple programs, I understood the basic idea behind it.

### Python Tuples

At first, tuples looked exactly like lists except for the brackets.

After learning more about them, I understood why Python has both. If the data should never change, a tuple is a better choice. If the data needs to change, a list is more suitable.

The easiest way for me to remember the difference is that **lists can be changed, but tuples cannot**.

### Git

Today I learned that even after pushing a commit to GitHub, there are different ways to fix mistakes.

I learned about `git revert`, which is useful when I want to undo changes without changing the commit history.

I also learned about `git reset --hard HEAD~1`, which completely removes the latest commit, and `git reset --soft HEAD~1`, which removes the commit but keeps all the changes so I can commit them again.

One thing I understood today is that Git doesn't have one command for every situation. The command depends on what I'm trying to do.

> **Note:**
>
> Yesterday I learned how to edit the latest commit using `git commit --amend`. Today I learned something different. Instead of editing a commit, I learned how to undo or remove a commit after it has already been pushed to GitHub. That helped me understand that Git has different commands for different kinds of mistakes.

## What computer/software engineering fundamentals did I learn today?

Today's topics showed me that choosing the right data structure is important.

Strings, lists, and tuples can all store data, but each one is meant for a different purpose. I think knowing **when** to use them is just as important as knowing how to write the syntax.

I also noticed that Python provides many built-in methods, which makes programming much easier because I don't have to write every small operation from scratch.

From Git, I learned that version control is not only about saving code. It also helps fix mistakes without starting over.

## What changed in my thinking?

Before today, I used to think strings, lists, and tuples were almost the same because they all store values.

After practicing them, I realized that each one has its own purpose. Strings are for text, lists are useful when data changes, and tuples are better when the data should stay the same.

I also thought that if I pushed a wrong commit to GitHub, there wasn't much I could do. Now I know that Git provides different ways to undo or remove commits depending on the situation.

Today's topics took a little more time than I expected, but writing notes and trying the examples helped me understand them much better. I think these are concepts that I'll keep using as I continue learning Python.

## Today's One-Line Summary

> "Today I learned how to work with strings, lists, and tuples in Python, and I also learned that Git gives different ways to fix mistakes depending on what I want to do."
