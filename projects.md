---
layout: page
title: Projects
permalink: /projects/
show_page: true
---

# TBA Dancer

Created over winter break 2016/2017, this app is built specifically for the collegiate ballroom community. Often times competitive ballroom dancers find themselves without a partner for an upcoming competition, and when this happens, they are said to be "dancing TBA," meaning that their partner is to be announced. Sometimes TBA dancers try to find each other through the Facebook pages of the competitions, and sometimes the competitions themselves try to pair up dancers ahead of time, but usually dancers end up frantically scrambling to find a partner moments before competing. This is super stressful!

So, partially to ameliorate this situation, and partially for my own educatoinal benefit, I spent this past winter break building TBA Dancer. This Ruby on Rails webapp allows users to sign in with Google auth and browse current posts by other dancers who need partners. Then, if they don't find a suitable partner already listed, they can create their own post. Unlike the Facebook pages, my app is only for finding partners, and each page displays only the open partner searches for a single competition. As I continue to work on this app, I hope to add a filter feature as well, which will hopefully make finding a TBA partner easier than ever.

If you're interested, check out the app [here](http://tba-dancer.herokuapp.com), or the source code [here](http://github.com/galantlex/tba-dancer). If you're even *more* interested, you can also check out a little blog I kept while tinkering and learning how to make the app, [here](http://github.com/galantlex/tba-dancer/wiki)!

  <hr/>
# Megabites

Have you ever wanted to order food for delivery, but haven't wanted to foot the whole delivery charge or meet the minimum yourself? Maybe you live in a dorm with all your friends, so you can simply ask the group chat, "Who's up for dim sum?" But maybe you're instead in an office building, or a computer science lab, so you're instead surrounded by acquaintances with whom you are <em>not</em> in a group chat. What to do?

This app, built for Tufts Polyhack 2016, gives users an online platform to connect with other people in their vicinity who also want to split a delivery order. The app is built on Rails, and is currently hosted [here](http://mighty-refuge-19588.herokuapp.com), with the source code [here](http://github.com/galantlex/megabites). Working with my team at my first hackathon was a blast!

  <hr/>
# Boolean Satisfiability Solver

Written for Tufts' Programming Languages class in 2017, this project is built in Scheme and is able to solve complex boolean formulas using continuation passing style, or CPS. CPS is a trial-and-error technique similar to recursion that passes blocks of code, or "continuations", through repeated function calls. Typically this includes `success` and `failure` continuations, which are called when one of those trial-and-error solutions either succeeds or fails, respectively.

In the case of this project, the solver takes a pre-fix boolean formula, such as `(and a b)`, and tries to find boolean substitutions which make the formula true. It looks at the operator, `and`in this case, and knows that for the whole formula to be true, the rest of the terms in the list must all be true. It then looks at the first term, `a`, and makes that true by trying the substitution `{a => #t}`. Finally, it calls the `success` continuation, which sees `b` and adds the substitution `{b => #t}`.

Now it has `{a => #t, b => #t}`, and the formula is solved! It now calls the final "success" continuation, which delivers the substitution to the user. The process is more complicated when you throw in `not`s and `or`s, but that's essentially it! If, in the end, there is no solution that can make the formula true, then the solver returns the final failure continuation of `no-solution`.

<hr/>

# Hindley-Milner Type Inferencer

Also written for Programming Languages in 2016, this project is built in SML and implements Hindley-Milner type inferencing rules for an nML interpreter otherwise written by [Norman Ramsey](http://www.cs.tufts.edu/~nr/). This project was great for learning about type inferencing and constraints, as well as type checking, which all comes in handy every time I'm coding and get an unexpected type clash!

  <hr/>

# Image Compressor

This program was written in C with [Evgeni Dobranov](http://edobranov.github.io/) for Tufts' Machine Structure and Assembly Programming course in Fall 2016. Given a PPM image, it compresses the file down through 8 stages of a JPEG-like compression, resulting in an output about 1/3rd the size of the original file. Then, the program can read in that compressed file and decompress it, producing an image with less than 4% error compared with the original image, on all test images.
