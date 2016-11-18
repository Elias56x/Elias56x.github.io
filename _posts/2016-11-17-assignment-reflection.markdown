---
layout: post
title:  "Assignment reflection"
date:   2016-11-17 20:43:32
categories: assignment
comments: true
---

### What do you think of pre-compiling your CSS? 

Using a CSS preprocessor for my CSS felt like a refreshing way to create the style for this website.

* Compare to regular CSS

Compared to regular CSS pre-complied CSS allows you to make calculated measurements in your CSS, the use of variables, and gives you a clear and organized way to write your CSS through techniques such as mixin and nesting.  

* Which techniques did you use?

Some of the techniques I used were variables, darken function for hover links, and nesting.

* Pros and cons?

1. Pros: Organized files, calculations, the use of variables. 

2. Cons: Code is harder to debug, increased building time, greater complexity.

### What do you think of static site generators?

Static site generators seems to be a great way to build simple websites. 

*  What type of projects are they suitable for?

Projects which do not require any user input or realtime content, such as a campaign site or a blog. 

### What is robots.txt and how have you configure it for your site?

Robots.txt is a way for web robots to read the instructions on a website concerning which paths it should not visit.

I have configured my robots.txt file to exclude all robots from the entire server.

### What is humans.txt and how have you configure it for your site?

Humans.txt is a way for humans to read information about the people who have created the website and additional information about the website, such as the last update and or software used.

I have configured my humans.txt to include my name, twitter username, place of residence and last update information.

#### How did you implements comments to blog posts?

I've implemented comments to my blog posts through the use of Disqus by following their Jekyll install instructions.

You add 'comments:true' to the YAML Front Matter and place the Disqus Universal Embed Code between the "if page.comments" tag.

#### What is Open Graph and how do you make use of it?

Open Graph allows your web page to become a rich object in a social graph. I've made use of Open Graph by implementing

{% highlight html %}
<html prefix="og: http://ogp.me/ns/article#">
{% endhighlight %}
In default.html, and
{% highlight html %}
<meta property="og:title" content="{{ page.title }}"/>
<meta property="og:url" content="https://elias56x.github.io{{ page.url }}" />
{% endhighlight %}
In head.html.


{% if page.comments %} 
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = '//efqv.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
                                                        
{% endif %}
