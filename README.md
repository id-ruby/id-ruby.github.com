# Id-Ruby

Source code of id-ruby.org

## How to Add New Post

Add the new post in a relevant category folder (e.g. `events/_posts/` or `videos/_posts/`).

Add the date in front of the file name (e.g. `2012-20-12-the-world-will-end-lets-get-wasted.html`).

Use the minimum format shown below. Change the content of `title`, `cat`, and `author`, but keep the `layout` variable value to `post` unless you know what you're doing. For `cat`, use the corresponding folder name that you drop the post into (e.g. `videos` for `videos/_posts/`):

``` html
---
layout: post
title: post title here
cat: events
author: your name
---

<p>You don't have to write the title again. Just go straight to the content</p>

<p>Use `<p>` tag for each paragraph. The post must contain at least one paragraph.</p>

<h2>Use `<h2>` for subheadings</h2>

<p>Uh huh.</p>
```

You may want to use `excerpt` variable so the post will be truncated correctly on the home page. `excerpt` should contain _one and only one_ paragraph tag:

``` html
---
layout: post
title: post title here
cat: events
author: your name
excerpt: <p>You don't have to write the title again. Just go straight to the content</p>
---

<p>You don't have to write the title again. Just go straight to the content</p>

<p>Use `<p>` tag for each paragraph. The post must contain at least one paragraph.</p>

<h2>Use `<h2>` for subheading</h2>

<p>Uh huh.</p>
```
    
Fancy for a code snippet? Use the provided liquid extension:

``` liquid
{% highlight ruby linenos %}
def you
  "suck"
end
{% endhighlight %}
```

For a `video` post, you may want to use `smaller` variable that will be used to show a smaller video on the sidebar.

## Check It Out Before You Commit

Make sure you have jekyll:

``` bash
gem install jekyll
```

Make sure you have `pygmentize` executable to show highlighted code snippet:

``` bash
sudo apt-get install python-pygments
```

Go to the root dir of this project. Run `jekyll`. Check on `localhost:3000`.


## To Do List

* Syntax highlight css
* Jobs page format
* Resources page
* Companies
* Jobs section on the sidebar
* Tags section on the sidebar