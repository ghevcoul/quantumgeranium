---
layout: post
title: Jumping into the Unknown
subtitle: A Journey from Research to Devops
author: Gavin
slug: unknown-devops
---

About a year ago, a new director was hired to lead the organization I'm part of at work. 
Normally, this wouldn't be a particularly noteworthy event, but her arrival ultimately had a profound impact on the work I'm doing today.
First, let's provide some context.

In August of 2019, I transferred from the Research organization at HERE to an R&D team working in the autonomous driving group developing technology to derive a high-definition map from sensor data.
I had actually been embedded in this team since the beginning of the year as part of a collaboration between them and Research to develop new algorithms for change detection in the map, so when I transferred the only thing that really changed for me was reporting to a new manager -- I was still a research engineer doing algorithm development, only now it was on a mixed team of research and software engineers.
The project was wrapping up the preliminary research at the end of the summer and we were looking ahead to stabilizing the code and productionizing our deployment in the fall. 

So, this was the situation when the new director took over on September 1.
She is based in our Boulder office and has people spread across Boulder, Chicago, and Berkeley on the team.
Sometime in September 2019, she came to visit the Berkeley office to get a chance to meet us.
During that visit, she scheduled one-on-one meetings with each of us and it was during that first face-to-face interaction that I took a risk that paid off.
There was the usual get to know you questions, "what are you working on?", "how long have you been with the company?", etc.
And then, she asked a question that I wasn't expecting.
Something to the effect of "I like my people to be happy in their work, so is there anything you aren't currently doing that you would like to?".
I've been interested in developer tooling for a long time and had been looking for an excuse to learn more about devops for a few years, so I told her basically that.
I didn't think much of it at that point and assumed I'd continue working on research problems for the foreseeable future, finding excuses to tinker with a Gitlab pipeline or stick my fingers in an AWS deployment when I could.
After that conversation, things progressed forward as one would expect.
I returned to my project, continued to do algorithm improvements and bug fixes as we moved toward production.
I did get an opportunity to overhaul our AWS deployment to allow for better horizontal scaling that was quite fun.
I didn't have much interaction with my director.

Then, this spring I got an entirely unexpected message.
She said that there was a re-org coming in a few weeks and a new project was spinning up under a newly hired manager and wanted to know if would I be interested in joining it?
The interesting part was this wouldn't be a research-heavy project, it was going to be a classic data engineering codebase, where we would be building a pipeline to read a firehose of streaming sensor data.
There were already a few engineers assigned to the project, but they needed someone to own the testing and deployment process and she wanted to offer that role to me.
To say I was stunned would be an understatement.
Here was a director I barely knew and a manager I'd never met willing to give me, a PhD chemist with a very research-heavy background, a chance to learn devops on the job while driving it for a brand new project.
There wouldn't even be existing practices for me to pick up and extend, everything was being built from the ground up.
Of course, I accepted the offer (what would be the point of writing this if I had said no and continued doing research?).

After learning more about what the expected tech stack for this project would be, I got to work learning all I needed to know.
This was going to be a Scala app, using the Flink framework, that would be deployed onto a Kubernetes cluster.
If you are keeping track at home, that's three for three on technologies I had never used.
I hadn't written more than a couple hundred lines of code in any JVM language since my undergrad and while I'd done a decent amount with Docker, I'd never gotten a chance to use Kubernetes.
We have a subscription to LinkedIn Learning at work, so I took a couple intro courses on Scala and Kubernetes and then dived into a sandbox for some hands-on learning.
I put together a simple hello world REST app with Akka-HTTP (a really fun framework, with some interesting design patterns) and figured out how to deploy it onto Kubernetes.
We've gone through a number of iterations and made some mistakes (and hopefully learned from them), but I'm proud to say at this point, a little over 4 months after starting on this project, we have a fully automated Gitlab pipeline that runs unit tests, builds the code, and can deploys it onto Kubernetes in multiple environments. 

All of this is a rather long-winded way of saying thank you to the director of my team for listening to me a year ago and when an opportunity arose, taking a gamble that I was capable and giving me a chance to learn a whole new set of skills on the job. 
Also, to my manager, who sight-unseen agreed to take on a researcher coming off a computational geometry C++ project as the owner of the devops processes for his Scala streaming pipeline.
I will forever be grateful to both of them for believing in me and trusting that I could do the job despite having nothing in my background proving that.
