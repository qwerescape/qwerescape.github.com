---
layout: page
title:
tagline:
---
{% include JB/setup %}
##Me
<div class="intro">I am scared to describe myself because changes happen faster than I could update this. Here is the accurate version at this moment
<ul>
  <li>I went to school in Elelctrical Engineering @ University of Toronto.</li>
  <li>Messed around with FPGAs and <a href="http://www.youtube.com/watch?v=qNmnLPYVrww">won an award from Xilinx.</a></li>
  <li>Flirted with: C++, Objective-C, Cocos2d, Java, Spring, Android, C#, WPF, Javascript, ExtJS, JQuery, Perl, Ruby, Rails.</li>
  <li>Got quite serious with: Java EE, Spring, Android, Javascript, ExtJS, C++, C#, WPF.</li>
  <li>I really like OO, thinking about OO puts a smile on my face everytime.</li>
  <li>Because of OO I also like TDD, BDD, DI.</li>
  <li>My crossover from right to left is golden, but I can't dribble with my left very well after that.</li>
  <li>I drain three pointers like I am using an aimbot, but my mid/close range jumpers are on and off.</li>
  <li>I've tried wordpress, blogger, squarespace, my own site, never got passed 2 posts</li>
  <li>I sing to release stress, luckily I play the guitar too so the overall outcome is bearable</li>
</ul></div>


##Recent Posts
<ul class="posts intro">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


