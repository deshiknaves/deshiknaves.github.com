---
layout: post
title: "Droption.js - Simple select replacement"
date: 2013-03-03 18:17
comments: true
categories: [Javascript, jQuery, Plugins] 
---

{% img center http://www.deshiknaves.com/droption/droption.png Droption %}

I really wish that browsers has the option to customize inputs as easily as other things can be customized. Unfortunately to acheive what we really want to in our designs, we have to rely on Javascript. This is not all bad, but we can potentially spend a lot of time trying to make the tweaks that we need to. We have been using a few different **select** replacements over the last few weeks and a lot of them either have issues in different browsers or don't have the customizabitly that you would want. So I decided to make something that was simple but still achieved what you wanted to achieve. Enter Droption. The idea is that it's a simple replacement for any customized select input. It doesn't target all elements with a class, rather you tell it which select inputs it should target.

The css for the plugin is written in sass, and can be fully customized by changing the css to what you need it to be. The supplied css is just a starting point, and you can customize it to your heart's content. The other thing that's was also important was the abiltiy to have different select inputs on the same site of have different themes. This can be achieved quite easily by giving that element a custom **class** and customizing it that way.

The thing that bugged me about a lot of the other select replacements out there was the fact that it would make the page change height when the select input is replaced by the faux select element. This looks really ugly and I wanted to avoid this. So I recommend that you set the add a class to the body of your document as to whether or not the client has js (This is quite common now and you can check html5 boilerplate, if this is new to you), and if they have js, then hide the select input to start off with. Then in the markup, just have a div with the class of your theme and droption:

``` html
<div class="my-theme droption"></div>
```

That way the height of the div is defined in the css and you won't see the jerky change that I'm talking about. Finally Droption can be called on the div passing in the **select** element to load in the funcitonality of the select list.

``` javascript
$('.my-theme.droption').droption({ select: '.my-select' });
```

This is just the first draft of plugin. I plan on adding options for height and width as well as the ability for the dropdown div to be able to calculate how much room it has and show the menu accordingly. But it's quite usuable now and feel free to add to it.

You can view a demo <http://www.deshiknaves.com/droption>
Visit the github page <https://github.com/deshiknaves/droption.js>
