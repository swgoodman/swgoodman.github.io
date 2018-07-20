---
layout: post
title:      "Rake. What is it?"
date:       2018-07-20 18:12:06 +0000
permalink:  rake_what_is_it
---



As I progress through the curriculum I am becoming more and more interested in what is happening under the hood of our favorite frameworks and gems. I came across Rake in the ORM and Active Record portion of the course and decided to make a guide to help myself better understand Rake and how it makes important gems, such as Active Record work.

![](http://www.rubyrake.org/wp-content/uploads/2016/09/ruby-favicon.png)

So, what is Rake? Rake is all about

***automation.***

According to the curriculum Rake is "a tool that is available to us in Ruby that allows us to automate certain jobs... " and it "allows us to define something called 'Rake tasks' that execute these jobs. Once we define a task, that task can be executed from the command line."

What does this all mean? Every program has tasks that are menial or repetitive. Before Rake, programmers had to write scripts in BASH to help them speed up and accomplish these, largely administrative, tasks. This process was difficult and there was no standard procedure for organizing or executing the scripts. 

Enter Jim Weirich and his creation, Rake. Rake software, packaged as a Ruby gem, allows programmers to easily write and execute tasks. These tasks can be called from the command line and follow a standard format of syntax, organization, and execution. The tasks can be co-dependent and execute contigently on other tasks. Another big benfit is Rake's ease of use with Ruby built programs.

![](https://qph.ec.quoracdn.net/main-qimg-6b9504fa1329fd0f63b0931adc88bcdf-c)

So what can we use Rake for? An infinite number of things. But common applications include database creation, migration, file compiling, file generation, HTML conversion, and other repetitive, tedious, but important tasks.

So, what are you waiting for?

`gem install rake`
