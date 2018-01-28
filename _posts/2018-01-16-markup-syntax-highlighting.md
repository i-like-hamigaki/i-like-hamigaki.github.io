---
title: "University of Alberta Cryptocurrency Group has first official meeting"
excerpt: "Post displaying the various ways one can highlight code blocks with Jekyll. Some options include standard Markdown, GitHub Flavored Markdown, and Jekyll's `{% highlight %}` tag."
last_modified_at: 2018-01-28T10:27:01-05:00
tags: 
  - cryptocurrency
  - meeting minutes
author: reed
---

The Crypto Club (or may be names the Blockchain Group in the future) had its very first formal meeting on January 16, 2018. 10 members were in attendance, of 18 members who have signed on to join. The group went over a variety of topics outlined in the minutes below, and intends to register the group officially, very soon. [^1]

[^1]: <http://en.wikipedia.org/wiki/Syntax_highlighting>

## Call to order
A meeting of The Blockchain and Cryptocurrency Group/The Crypto Club was held at DICE Building on January 16, 2018.

## Attendees
Attendees included Reed Sutton, Raafay Tariq, Joe Dang, Mark Pekar, Robin Park, Spencer Shupe, Gonzalo Rubio, Raymond Sarinas, Melissa Doroteo, Jacob Wong. 

## Members not in attendance
Members not in attendance included Matthew Pietrosanu, Laura Petrich, Taleana Huff, Matthew Sheldrake, Sophie Shi.

## Agenda items
1.	ICEBREAKER – All went around the room and stated name, faculty/degree, and what got them interested in cryptocurrency. 
2.	Overview of constitution
  * Drafted by RS and JD
  * Mission statement + goals of the group reviewed
  * Public education vs. within-group development
  * Open to any affiliated with university (alumni, etc)
  * Types of membership and divisions of standing. 
  * Committees – formation and purpose
3.	Discussion of issues and challenges so far
a.	Logistics of managing crypto funds
b.	Where to store hard wallet
4.	Brainstorming project ideas
a.	ICO research / due diligence meetups 
b.	Mock crypto investing (NOT with real funds) – need a platform..
c.	Bitcoin atm – catm.io – UofCalgary already purchasing and negotiating placement on campus.
d.	Host  a blockchain themed hackathon
5.	Fundraising ideas
a.	Copytrading services (investy, blockport, covesting) – require startup cashflow
b.	Consulting / education (eg. stia.io) – also longer term
c.	Public on campus education events (charge non-members to attend)
d.	Standard fundraising – bake sales, bbq
i.	Bitcoin and other themed cookies for example
e.	Selling cryptocurrency themed socks or other paraphernalia on website?
6.	Discussion of Executive roles and responsibilities
a.	Self-nominations
b.	Imperative: need a VP Finance / treasurer

## Action items
1.	ALL to let Reed/Joe know if any mistakes or clarifications in the constitution
2.	EXECUTIVE to decide on what percentage attendance required to attain ‘gold’ standing
3.	EXECUTIVE to meet again with SGS and provide clarifications regarding cryptocurrency
4.	ALL to decide when and how often to regularly meet for ICO evaluations
5.	EXECUTIVE to research and consult with CS majors re. difficulty of creating a mock investing software.
6.	 ALL to contact Reed if interested in executive position and send CV.
7.	EXECUTIVE to set date for next meeting

## Meeting ajourned at 1 hour. 


GitHub Flavored Markdown [fenced code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) are supported by default with Jekyll. You may need to update your `_config.yml` file to enable them if you're using an older version.

```yaml
kramdown:
  input: GFM
```

Here's an example of a CSS code snippet written in GFM:

```css
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
```

Yet another code snippet for demonstration purposes:

```ruby
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
      @site = site
      @base = base
      @dir = dir
      @name = 'index.html'
      self.process(@name)
      self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
      self.data['tag'] = tag
      tag_title_prefix = site.config['tag_title_prefix'] || 'Tagged: '
      tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
      self.data['title'] = "#{tag_title_prefix}#{tag}"
      self.data['description'] = "An archive of posts tagged #{tag}."
    end
  end
end
```

## Jekyll Highlight Liquid Tag

Jekyll also has built-in support for syntax highlighting of code snippets using either Rouge or Pygments, using a dedicated Liquid tag as follows:

```liquid
{% raw %}{% highlight scss %}
.highlight {
  margin: 0;
  padding: 1em;
  font-family: $monospace;
  font-size: $type-size-7;
  line-height: 1.8;
}
{% endhighlight %}{% endraw %}
```

And the output will look like this:

{% highlight scss %}
.highlight {
  margin: 0;
  padding: 1em;
  font-family: $monospace;
  font-size: $type-size-7;
  line-height: 1.8;
}
{% endhighlight %}

Here's an example of a code snippet using the Liquid tag and `linenos` enabled.

{% highlight html linenos %}
{% raw %}<nav class="pagination" role="navigation">
  {% if page.previous %}
    <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
  {% endif %}
  {% if page.next %}
    <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
  {% endif %}
</nav><!-- /.pagination -->{% endraw %}
{% endhighlight %}

## Code Blocks in Lists

Indentation matters. Be sure the indent of the code block aligns with the first non-space character after the list item marker (e.g., `1.`). Usually this will mean indenting 3 spaces instead of 4.

1. Do step 1.
2. Now do this:
   
   ```ruby
   def print_hi(name)
     puts "Hi, #{name}"
   end
   print_hi('Tom')
   #=> prints 'Hi, Tom' to STDOUT.
   ```
        
3. Now you can do this.

## GitHub Gist Embed

GitHub Gist embeds can also be used:

```html
<script src="https://gist.github.com/mmistakes/77c68fbb07731a456805a7b473f47841.js"></script>
```

Which outputs as:

<script src="https://gist.github.com/mmistakes/77c68fbb07731a456805a7b473f47841.js"></script>
