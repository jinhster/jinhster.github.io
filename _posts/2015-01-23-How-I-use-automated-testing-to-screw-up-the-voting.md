---
layout: post
title:  "How I use automated testing to screw up the voting for the award they
the office prepared for the holiday"
date:   2015-01-23
categories: Test
---
The place where I am working had a holiday party at the beginning of
the year( This month =) Yeah ). This year they decided to have an awards voting contest.
Awards including: Best rookies, best team player and so on. The voting
took place in surveymonkey (link was sent via email) and there's no one person per IP rule (
  We all share the same IP, so I doubt making it one person per IP is
  a smart idea).

Nevertheless I was trying to have fun with it so I decided
  to use selenium to automated the voting process. The voting contains
  two categories of checkboxes and seven input textfields. The steps are pretty
  simple I look up the Name tag(In html, I think name tag is suitable for this because I am dealing with names) of the checkboxes that I want to select and
  wrote the script in ruby to look for it, textfields are pretty much the
  same other than the fact that I had to enter/send in the name of the ones
  that I want to win. What I found interesting about this was that browserstack
  is really slow for doing it on cloud and doing locally was much faster. I eneded up
  with around 45K of submissions (I don't have the exact number because I don't have access to
  the surveymonkey account). At the end they discounted a lot of the votes (I mean how is it possible
    to not raise any red flag when there's 45K votes and only ~100 employee. )
    I had a loop inside the script and had a lot of scripts executing at the same
    time, it didn't take long since its in parallels. Selenium could come in
    really handy when you do input on web.
