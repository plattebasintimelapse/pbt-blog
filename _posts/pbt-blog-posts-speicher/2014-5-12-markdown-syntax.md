---
layout: post
title: Markdown Syntax
description: This is a breakdown of the markdown syntax. Use this as a syntax walkthrough.
author: Steven Speicher
draft: true

---

# Outline

- [Writing for the Web](#web-writing)
- [Headers](#headers)
- [Links](#links)
- [Images](#images)
- [Videos](#videos)
- [Line Breaks](#lines)
- [Block quotes](#quotes)
- [Lists](#lists)
- [Code](#code)

# <a name="web-writing"></a>Writing for the Web

Our blog is run on [Jekyll](http://jekyllrb.com/), a static site generator. It is free and open-source and quite simple and elegant. A blog post is drafted in a text document called [Markdown](http://daringfireball.net/projects/markdown/). Markdown is a text-to-HTML conversion tool for web writers, written in a plain text format.

To create a plain text document, you can use TextEdit on your Mac. Or I prefer [Mou](http://mouapp.com/) which is nice and pretty. If you're on a windows machine, try [MarkdownPad](http://markdownpad.com/).

Whatever way you write, make sure you save your plain text document with the `.md` extension. Save the file into the `Dropbox/pbt-blog-posts-name` folder that is shared with you. Whenever a change is made inside this folder (or the `pbt-blog-uploads` folder), Jekyll will automatically create or update the post.

Visit your post at `www.plattebasintimelapse.com/blog`. Write, create, and update files and view changes in real time!

#### Make sure to…

Save the file following this convention:
`yyyy-mm-dd-title-of-post.md`

Include the following front matter. That is, include these lines at the head of every text document you write for the blog.

    layout: post
    title: Your Post Title
    description: A short description of the post.
    author: First Last

You may add `draft: true` for drafting purposes. Manually type in the following URL to review the post, hidden from the blog's front page feed.

##### www.plattebasintimelapse.com/blog/*yyyy*/*title-of-post*

Delete `draft: true` when ready to publish.

___

# <a name="headers"></a>Headers

Headers are used to mark key points in the blog post. They are not necessary but can be handy.

##### This is an H5
#### This is an H4
### This is an H3
## This is an H2
# This is an H1

Use them like this:

    ##### This is an H5
    #### This is an H4
    ### This is an H3
    ## This is an H2
    # This is an H1
    
___

# <a name="links"></a>Links

Links are used to link users to outside pages or to other pages on our website.

They are written with `[ ]`. The URL should follow immediately after inside a `( )`.

This is an example link to the [Markdown Syntax guide](http://daringfireball.net/projects/markdown/syntax).

    This is an example link to the [Markdown Syntax guide](http://daringfireball.net/projects/markdown/syntax).
    
___

# <a name="images"></a>Images

There are two ways to upload pictures to our blog.

### Upload Image to our Server

First resize the image to ~300kb and create a folder titled your post under the `pbt-blog-uploads`. Then reference the file in your Markdown with this syntax:

    ![Alt text]({% raw %}{{ site.url }}{% endraw %}/images/pbt-blog-uploads/title-of-post/title.jpg "Optional title")
    
The `{% raw %}{{ site.url }}{% endraw %}` is an absolute file path necessary for web deployment.

### Embed Image from outside Source
    
If embedding an image from outside our server such as [Flickr](https://www.flickr.com/groups/plattebasin/), use this syntax:

    ![Alt text](https://farm3.staticflickr.com/image/location/ "Optional title")
    
or copy the HTML code directly from the source:

	<img src="https://farm4.staticflickr.com/3814/9398436996_d47671db6f_s.jpg" alt="Ysha the Lion">
	
Make sure you delete the height and width properties from the img tag.
    
To give an image a caption use:

	###### This is an H6 tag but used under an image to be a caption.

![rooster](https://farm3.staticflickr.com/2937/14169679614_efc1a16533_o.jpg "rooster")
###### This is an H6 tag but used under an image to be a caption.
     
___

# <a name="videos"></a>Videos

Video iframes should be copied right into the markdown document.
    
    <div class="video-wrapper">
        <iframe src="//player.vimeo.com/video/75656312?title=0&amp;byline=0&amp;portrait=0" frameborder="0"></iframe>
    </div>
    
<div class="video-wrapper">
    <iframe src="//player.vimeo.com/video/75656312?title=0&amp;byline=0&amp;portrait=0" frameborder="0"></iframe>
</div>
    
When copying the URL embed code, clean up the iframe, delete height/width paramters, and delete the trailing `<p>` tag and `<a>` tag.
 
In the parent `<div>` tag, use:

- `class="video-wrapper"` if the video is standard aspect ratio 16x9 etc.
- `class="video-wrapper-tl"` if the video is a timelapse sequence aspect ratio 3x2.

___

# <a name="lines"></a> Line Breaks

To enter a line break, like the spacers between each section in this post, use three consecutive underscores `___`.

___

# <a name="quotes"></a>Block quotes

Use `>` to type block quotes...

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

___

# <a name="lists"></a>Lists

An unordered list uses the `*`, `+`, or `-` character.

* This
* is 
* a 
* list

is equivalent to:

+ so
+ is
+ this

and:

- and
- this
- too!

Ordered lists use numbers!

1. This
2. is
3. an
4. ordered
5. list

___

# <a name="code"></a>Code

Inline code is written with `` `code goes here` ``.

Code blocks are written by identing text...

    # This is an H1
    ## This is an H2
    ### This is an H3
    #### This is an H4
    ##### This is an H5
    ###### This is an H6
    # This is all in a code block!

    Use `>` to type block quotes...

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.
