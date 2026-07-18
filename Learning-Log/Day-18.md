# Day 18 - Getting More Comfortable with Node.js

## What did I learn?

Today was one of those days where I didn't learn one big concept, but instead learned a lot of small things that made me understand Node.js much better.

Yesterday, I learned what Node.js is and even created my first server. That felt exciting because it was my first step into backend development. Today, I explored some of the built-in modules that Node.js provides, and honestly, I didn't expect JavaScript to be capable of doing so many things.

One thing that surprised me the most was the **File System module**.

I always thought JavaScript was only meant to make websites interactive. I never imagined it could create files, read them, update them, or even delete them from my computer. Seeing that happen completely changed the way I look at JavaScript.

I also learned about the **Path module**. At first, I didn't really understand why it existed because it just seemed like another way of writing file paths. But after reading more and looking at examples, I realized it saves us from a lot of problems, especially when the same application has to work on different operating systems.

Another topic I enjoyed was the **OS module**.

It felt interesting to see that Node.js can actually tell us details about the computer it's running on, like the operating system, processor, and memory. I hadn't thought about backend applications interacting with the computer itself before today.

I also spent some time learning about the **Events module**.

Yesterday I learned that Node.js is event-driven, but today I actually got to see how events are created and triggered. It made yesterday's theory much easier to understand.

Towards the end, I learned about **Buffers**, `__dirname`, `__filename`, and how developers organize code by splitting it into different files using `module.exports` and `require()`.

None of these topics felt huge on their own, but together they made me realize that backend development is much more than just creating servers. There are so many small building blocks that come together to make everything work.

## What challenges did I face?

Today's biggest challenge wasn't writing code.

It was understanding *why* certain things are done in a particular way.

For example, when I first saw `module.exports` and `require()`, I kept wondering why developers don't just write everything in one file. It seemed simpler.

But after thinking about it for a while, I realized that if a project keeps growing, one file would quickly become impossible to manage. Splitting the code into different files suddenly started making a lot more sense.

I also found the **Buffer** topic a little difficult.

I understood the basic idea that it's used to handle binary data, but I still can't clearly picture where I'll actually use it in a real project. I think that's something I'll understand better once I start building larger applications.

Some of the File System methods also looked almost identical in the beginning, so I had to read through the examples carefully before I could remember what each one was used for.

## What new concepts did I understand?

### File System (FS) Module

Today I learned that Node.js can directly work with files on the computer.

Creating files, reading them, updating them, and deleting them using JavaScript honestly felt a little strange at first because it's something I never thought JavaScript could do.

### Path Module

I understood that the Path module helps us work with files and folders in a cleaner and safer way.

Instead of worrying about different path formats on Windows or Linux, Node.js handles those differences for us.

### OS Module

The OS module showed me that backend applications can access useful information about the system they're running on.

Seeing details like the operating system and memory made me realize that backend development interacts much more closely with the computer than frontend development does.

### Events Module

Learning about events made the idea of event-driven programming much clearer.

Creating and triggering my own event helped me understand what actually happens behind the scenes instead of just reading about it.

### Buffers

Buffers were completely new to me.

I don't fully understand them yet, but I know they're important when working with things like images, videos, or other binary data.

I'll definitely need more practice before this topic becomes comfortable.

### Modules

Probably my favorite thing I learned today was how Node.js lets us organize code.

Using `module.exports` and `require()`, we can separate different parts of a project into different files and reuse them whenever we need.

It seems like such a simple idea, but I can already imagine how useful it'll be when I start working on bigger projects.

## What computer/software engineering fundamentals did I learn today?

Today's learning reminded me that writing software isn't just about getting the correct output.

It's also about keeping the code organized.

As projects grow, readability and structure become just as important as making the program work.

I also realized that many of the tools developers use every day are already built into Node.js. Instead of writing everything from scratch, we can use these modules to solve common problems much more efficiently.

## What changed in my thinking?

Before today, I used to think backend development was mostly about databases and APIs.

Now I'm slowly realizing that there's a lot happening before we even get to those topics.

Learning about these built-in modules made me appreciate how much Node.js already offers.

I also don't feel as overwhelmed as I did when I first started learning backend development.

Each day, things that looked completely unfamiliar yesterday are starting to feel a little more normal today.

I'm still very much a beginner, but I'm enjoying the process of slowly connecting all these concepts together.

It feels like every day I'm understanding one more piece of how real applications are built.

## Today's One-Line Summary

**"Today I realized that backend development isn't just about writing server code—it's also about learning the small tools and concepts that quietly make everything work together."**
