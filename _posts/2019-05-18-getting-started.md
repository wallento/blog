---
layout: post
title:  "Getting Started"
date:   2019-05-18
categories:
---

Since nearly three months I am a professor at [Munich University of
Applied Sciences](https://hm.edu/en) now. My primary role is teaching
computer architecture, computer engineering, and related topics. This
semester I am teaching *Computer Architecture* and *Operating Systems*
as basic undergraduate courses.

For a long time before my current role, I have been working with open
source. I have become an enthusiast and contributor to a variety of
projects. I have been involved with open source hardware and the
ecosystem surrounding it and I am a director at the [Free and Open
Source Silicon Foundation](https://fossi.foundation). The
accessibility of projects always has been my major concern. For
example, in my main project [OpTiMSoC](https://optimsoc.org), we
always try to lower the barrier of using it and make it usable for the
casual user. With the natural complexity of such projects, this can
become a heavy task and often hard to have in focus.

With the goal of teaching students state-of-the-art technology and my
love for open source, my ambition is, of course, to base my courses
entirely on open source technologies. Students at universities for
applied sciences are learning with an extremely high practical
orientation. The fact that the vast majority of them work already in
companies on bleeding edge technologies leads to that most of them
already understand open source. On the other hand, it puts a high
pressure on me to use relevant technologies in a semi-professional
setting. Which I enjoy a lot.

It didn't take long for me to encounter the first issues. For example,
I want to use very sophisticated RISC-V processor cores. I am in the
computer science faculty and the students are generally very software
focused. So I want to give them the best experience for someone who
doesn't know about HDLs at all but wants to have a look at the inner
workings. I also want to give them, for example, the possibility to
match what they are practically doing to the basic educational
representations used during the lectures. Most of the readers probably
know that this is not necessarily trivial for many projects where
distinguished researchers validate their newest ideas in computer
architecture. But even getting a simple trace of POSIX mutexes and
their usage in threads (for my other lecture) turned out to be far
harder than I expected.

The idea of this blog is to show you what problems I faced when
applying open source projects and how I solved them. I also want to
write about why I came to the conclusion that using a particular kind
of project in teaching is more confusing than helping. I hope that
this approach is useful to other teachers, but also to the community
to keep that aspect in mind. It is my goal to get all the changes I
had to make upstream in a timely manner, everything will be on my
repositories too.

In particular, I am currently teaching the following courses and want
to use new technologies (compared to previous editions):

 * **Computer Architecture** I want to switch the entire course to
   RISC-V. In the lecture that is more or less a no-brainer and I was
   very happy to find that the students loved RISC-V as an open, but
   highly relevant instruction set. In the first part of the lab the
   students played around with assembler and educational
   ([venus](https://venus.cs61c.org/),
   [Ripes](https://github.com/mortbopet/Ripes)) and instruction set
   simulators ([rv8](https://rv8.io/),
   [spike](https://github.com/riscv/riscv-isa-sim)). I will share my
   experiences here soon. In the current stage, we transition from
   instruction set simulation to micro-architecture
   implementations. As said the challenge is to make it easily
   accessible for the students. In the last stage, we will turn to
   FPGA-based development and benchmarking, including tracing the
   entire system and evaluating bottlenecks. That will be a lot of
   fun!

 * **Operating Systems** You would tend to think that teaching
     operating systems and developing a lab with modern open source
     technology is very simple. This is mostly true, but I, for
     example, want to highlight the importance of tracing and use
     tools like [LTTNG]() with [TraceCompass](). But there have been
     surprises where stuff got so complicated or did not exist, that I
     started working on my own solutions. For example, I am currently
     working on providing POSIX threading traces to the students in a
     good way. I will report about this soon.

I hope I can put up my first results pretty soon, stay tuned!

Cheers,
Stefan

![](https://vg08.met.vgwort.de/na/3cb97981c2b440bb9004390b123eca0e)