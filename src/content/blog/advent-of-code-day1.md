---
author: Joe Baranski
pubDatetime: 2023-07-17T02:09:56.916Z
title: Day 1 solution to AOC 2022
postSlug: day-1-solution-to-AOC-2022
featured: true
draft: false
tags:
  - learning
  - rust
  - challenges
ogImage: ""
description: My solution to Day 1 of the 2022 Advent of Code challenge.
---

This is my first blog post about Advent of Code (AOC) 2022, and this will be part of a series on the topic. If you've never done these challenges before, I highly recommend [them](https://adventofcode.com/2022). They are language agnostic, and incredibly original. You make an account, and then the puzzle inputs are randomly generated for your specific account, so you can't just copy and paste the answer into the solution text box, but if you do need help, there is an entire [subreddit](https://www.reddit.com/r/adventofcode/) dedicated to helping you figure out how to solve each day. There are **two** parts to each day, with the second problem being a variation of the first problem, using the same puzzle input. You are typically helping the elves with various issues they encounter on their holiday expedition.

![elf for AOC 2022](/assets/elf.png)

My first test was handling the puzzle input for the challenge. The last time I did AOC, I wrote the solutions in **TypeScript**, but this time I wanted to do them in **Rust**, so I had to think of a whole new workflow for dealing with the puzzle input.

**Disclaimer**: I'm going to treat the reader like they have no experience coding in Rust, but they do have a base level of understanding of coding principles and practices in general.

Rust has a really awesome standard [module](https://doc.rust-lang.org/std/fs/) called fs that can read input files, so I just make a new text file in my root project folder (unfortunately, you still have to copy and paste the text from the window in the browser, and if you think of a better way to do this part, please let me know).
