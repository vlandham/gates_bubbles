# Animated Bubble Chart

Creating Animated Bubble Charts using D3.

## Description

This repository contains code to create your own animated bubble chart.

It goes along with the tutorial here:

http://vallandingham.me/bubble_charts_in_d3.html

A live version of this code is here:

http://vallandingham.me/gates_bubbles/

## Running

D3 needs to be run from a webserver due to how it imports data files. 

See more here: https://github.com/mbostock/d3/wiki#using

So, to run this visualization locally, from the Terminal, navigate to the directory you checked it out to

     cd ~/code/path/to/gates_bubbles

Then start a webserver locally. If you are on a Linux or Mac, you should be able to use python's built in webserver:

     python -m SimpleHTTPServer 3000

I always use Ruby's thin gem to get things started

     gem install thin # <- just do once
     thin start

Once the server has started, open up your web browser to:

http://0.0.0.0:3000/

And you should see your bubbles!

## Pure JS version

For folks not wanting to dive into Coffeescript, I've added a JS version that is just the compiled Coffeescript. You can see it by navigating to the page:

http://0.0.0.0:3000/index_js.html

This was compiled with Coffeescript 1.8, using the command:

     coffee -o js/ -c coffee/vis.coffee

If you would like to try it on your own modified version of the Bubbles.

## Remove the Google Analytics Code!

Because this same code is used to run the live version on my site, I (perhaps foolishly) added my own Google Analytics code to the index.html page.

If you build anything with this - and that thing gets put on the internet, just try to remember to change the GA code down at the bottom of the page. At least you could remove the GA call.

## Things to consider

Here are a few things that may be issues for you, or may not be

* Written in Coffeescript

Coffeescript compiles down to JavasScript, and is a really fun language to learn. Try it out!

http://coffeescript.org/

But if you want, you should be able to compile this tutorial back down to JavaScript - and start from there. People in the comments of the tutorial have already done this.

* Bubbles might not be the answer to your problems

While the bubbles are flashy and are fun to watch move around, they may not be the best visual form to display your information in. In most cases, when bubbles are used to encode a single variable, the two dimensional bubble inflates and obscures the one dimensional value it is attempting to display. 

Kaiser Fung hates bubble charts. You can see lots of reasons why here: http://junkcharts.typepad.com/junk_charts/bubble_chart/

Just keep in mind when you are working with your data.

