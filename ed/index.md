---
layout: default
title: Ed.
permalink: /ed/
nav_order: 3
---

# Minicomp/Ed.

## About


Ed is a [Jekyll](https://jekyllrb.com/) theme designed for textual editors based on [minimal computing](http://go-dh.github.io/mincomp/) principles, and focused on legibility, durability, ease and flexibility.


One of our most pressing and ever revolving needs as scholars is to pass on our textual artifacts from one generation to another. The art of textual editing, among other practices, has helped many cultures to remember and interpret for centuries. Alas, that art is practiced and encouraged in its highest form by a dwindling number of scholars. In a digital environment the problem is compounded by the difficulties of the medium. While vast repositories, and "e-publications" appear on the online scene yearly, very few manifest a textual scholar's disciplined attention to detail. In contrast, most textual scholars who have made the leap to a rigorous digital practice have focused on markup, relying on technical teams to deploy and maintain their work. This makes your average scholarly digital edition a very costly, and therefore limited affair.

As we see it, a minimal edition is one that aims to reduce the size and complexity of the back and front end, and the learning curves for the user and the producer. Out of-the-box, this theme can help you build a simple reading edition, or a traditional scholarly edition with footnotes and a bibliography without breaking the bank. In our estimate, these are the two most immediately useful type of editions for editors and readers. An edition produced with Ed consists of static pages whose rate of decay is substantially lower than database-driven systems. As an added bonus, these static pages require less bandwith. Our hope is that our approach can help beginners or veterans deploy beautiful editions with less effort, that it can help us teach a 'full stack' [in one academic semester](https://github.com/susannalles/MinimalEditions/blob/master/README.md), allow us to care for our projects at less cost, and perhaps, just perhaps, allow us to generate high-quality editions on github.io in large quantities based on the [git-lit](http://jonreeve.com/2015/09/introducing-git-lit/) model by Jonathan Reeve. We're coming for you, Kindle!


### Sample Ed editions.

- [Our sample site](http://minicomp.github.io/ed/) is the first edition built with Ed.
- [Fugitive Verses](http://fugitiverses.viraltexts.org/): Popular Reprinted Poetry from Nineteenth Century Newspapers
- [mini lazarillo](http://minilazarillo.github.io/): A minimal edition of the *Lazarillo de Tormes*
- [Making and Knowing](https://cu-mkp.github.io/GR8975-edition/): The BnF Ms Fr 640 in Translation
- [Daisy Miller: A Comedy in Three Acts](https://britaneeelizabeth.github.io/ed/texts/DaisyMillerPlay/)



### Current Features
- Templates for narrative, drama and poetry
- Responsive design for mobile phones, tablets and PCs.
- Relatively easy to learn and teach
- Works well in high- or low- bandwitdh scenarios
- Easier for digital archives and libraries to preserve
- Open source, open access
- Unobtrusive footnotes
- Metadata in Dublin Core and OpenGraph to play nice with Zotero, libraries and social media.
- Automatic table of content generation
- Simple search functionality
- Annotations via [hypothes.is](https://hypothes.is/)
- Optional: Ability to generate well-formatted bibliographies and linked citations

## Getting Started

### Prerequisites

This documentation was built with beginners in mind, but has the necessary information for more seasoned producers.

To install and use Ed you will be using your terminal. If you need a refresher, I highly recommend "[The Command Line Crash Course](https://www.computervillage.org/articles/CommandLine.pdf)." Working knowledge of HTML and CSS is also taken for granted. If you're new to HTML and CSS, you may want to check out the relevant courses on [codecademy.com](https://www.codecademy.com/learn/web).

Jekyll does not run very well on Windows machines for now. If you are using Windows, this theme won't work for you, but we hope that you simply deploy our principles, and parts of our stylesheet, on a system like [Hugo](https://gohugo.io/), which does work on Windows.

---

### Installing Ed: Easy

The easy way to do this is not necessarily the more robust, and may simply not work on your system. The easy way could also be called the 'lucky' way. It will work if your system is ready for Ed. Two major caveats to keep in mind if you go the easy route: a) You may run into problems later when some Ed components need updating; and, b) You may run into conflicts if you run several Ruby environments for different projects. That said, if you just want to quickly try Ed, and you don't run into problems installing, this is perhaps the best approach.


If you're using a Mac, make sure you have the appropriate version of [XCode command line tools](https://developer.apple.com/xcode/download/) for your OSX. Using the terminal's `cd` command, switch to the directory where you want to install your project. Once inside the folder, you are ready to download and start using Ed. Enter each of these lines into your terminal (remember to ignore the `$`):

~~~ bash
$ git clone https://github.com/minicomp/ed.git
$ cd ed
$ gem install bundler
$ bundle install
~~~

That's it. To see if Ed is working properly we will take advantage of Jekyll's built in server. You can build the first version of your site and run the jekyll server at the same time by entering:

~~~ bash
$ jekyll serve
~~~

If at any point during this process you had an error you could not resolve, move on to the next section. If the site was rendered fine, copy the url from your terminal log and paste it into your browser of choice (I recommend Firefox). This url usually looks something like this `http://127.0.0.1:4000/ed`. At this point you should be looking at your very own working version of Ed:

![Your very own Ed]({{ site.baseurl }}/assets/screenshot-home.png)

---

### Installing Ed: Robust

The first step to install Ed is to download the source files from GitHub. To do so you must have git installed on your computer. You probably have git already, but if you don't, the easiest way is probably to install [Github Desktop](https://desktop.github.com/) (even though we will be using git and github from the terminal in this tutorial). Mac users may want to ensure they have [Xcode](https://developer.apple.com/xcode/) and its command line tools installed as well. To check if git is running on your system enter the following line on your terminal (remember to ignore the $):

~~~ bash
$ git --version
~~~

If you don't get an error, you're good to go. Using the `cd` command on your terminal, navigate to the folder where you keep your web projects. Once you're in the folder where you want Ed to live, download it from github using the following line (remember you can copy and paste):

~~~ bash
$ git clone https://github.com/minicomp/ed.git
~~~

At this point you should navigate inside your Ed project folder and stay there until further notice:

~~~ bash
$ cd ed
~~~

Jekyll is a Ruby gem (Ruby's name for software packages). The best way to ensure you have the right environment is to use Ruby Version Manager, or [rvm](https://rvm.io/), and the latest stable version of Ruby. To install rvm *and* a recent version of Ruby at the same time, follow the instructions on rvm's site. Remember to add `--ruby=2.3.0` at the end of the `curl` command to install ruby at the same time.

After the process runs succesfully, read the last few lines generated by the terminal. You will see final instructions for making rvm run. Once you finish the process, check to see if rvm is running by entering:

~~~ bash
$ rvm --version
~~~

If you don't get an error, you're ready for the next step. If you do get an error, and don't feel comfortable troubleshooting on the terminal, this is a good opportunity to reach out to a friend who can help. You can leave me a note on [the issues page](https://github.com/minicomp/ed/issues), for example. I'll try to get to it as soon as my other commitments permit. If you're comfortable troubleshooting on your own, I recommend Jekyll's own [troubleshooting documentation](http://jekyllrb.com/docs/troubleshooting/). Another great strategy for troubleshooting on the terminal is to copy and paste the errors you receive (sans personal information) into your favorite search engine.

The next step is to create a gemset for your jekyll projects. A gemset is a set of gems. If you don't create and use a gemset, every gem you install will be applied system-wide. This is not necessarily a bad thing, but if you will have several projects with several setups, this strategy will serve you well in the long run. To create a gemset:

~~~ bash
$ rvm gemset create ed
~~~

To use the gemset you just created:

~~~ bash
$ rvm gemset use ed
~~~

N.B. Everytime you open a new tab or window on your terminal you need to declare your gemset using `rvm gemset use ed`, or else it will revert to `(default)`.

Now that rvm and Ruby are set up, we're ready to install our first gem: Bundler. Bundler is a gem that allows you to install many gems at the same time using Gemfiles, which is a simple list of specific gems that lives in your project folder. Once you install it, you will be ready to run the Gemfile I provided in the source files. To install Bundler:

~~~ bash
$ gem install bundler
~~~

You're very close. Now that Bundler is installed, the final step is to install the right version of Jekyll. To do so run the Gemfile this way (remember you must be inside the `ed` folder for this to work):

~~~ bash
$ bundle install
~~~


If you don't get any errors, Ed should work at this point. To see if Ed is working properly we will take advantage of Jekyll's built in server. You can build the first version of your site and run the jekyll server at the same time by entering:

~~~ bash
$ jekyll serve
~~~

If you are running multiple Ruby environments using bundler, you will need to add `bundle exec` to the command:

~~~ bash
$ bundle exec jekyll serve
~~~

Copy the url from your terminal log and paste it into your browser of choice (I recommend Firefox). This url usually looks something like this `http://127.0.0.1:4000/ed`. At this point you should be looking at your very own working version of Ed:

![Your very own Ed]({{ site.baseurl }}/assets/screenshot-home.png)

---

### Installing Ed: Replacing an existing Jekyll theme

Ed, like Jekyll, is also a gem. Jekyll gives you the option to switch themes, as long as those themes are gems as well. If you have existing content and would like to use Ed, you need to add the following line to your \_config.yml file, usually at the bottom:

~~~
theme: "ed."
~~~

You also need to add the gem to your Gemfile file:

~~~
gem "ed."
~~~

Make sure to replace the version number with the one you need. I will do my best to document what changes come with each new gem. If your current theme does not have a Gemfile, you would need to create one and add the line above. The Gemfile is a plain text file like all other files in Jekyll, and should not have a file extension.

After these files have been modified, you need to update your Bundle in the terminal:

~~~ bash
$ bundle update
~~~

When using the gem on top of a previous theme, you will not have all the files of a full Ed install immediately available to you. More importantly, you may not have a \_texts folder. You need to create one or copy them from a full installation of Ed. You might also want to add the search and index file. The gem comes bundled with all these files once you install it on your system, but they won't be in the same folder as your project. To locate them you can refer to the [Jekyll documentation for gem-based themes](https://jekyllrb.com/docs/themes/). With some previous themes you might need to erase lingering files that interfere with the functioning of Ed. This can be an advanced operation I can't do justice to here. At that point you might need to familiarize yourself with the architecture of Jekyll, or pay close attention to errors when you try to serve the site, and reverse-engineer from there.

Going forward, updating to a new version of Ed is as simple as changing the release version and running the bundle update. I will try to keep changes in the actual markup to a minimum, but will let users know if any changes require a global find and replace in your editions.

---

### Jekyll

Ed is a Jekyll theme. That means you will need some familiarity with Jekyll to take advantage of its full potential. While running a Jekyll site is a bit more involved than Wordpress and other similar tools, the payoff in the long term is worth the effort to learn it. If you are new to Jekyll, I recommend you take a look at ["How (and Why) to Generate a Static Website Using Jekyll"](http://chronicle.com/blogs/profhacker/jekyll1/60913) at ProfHacker, Amanda Visconti's excellent [Building a static website with Jekyll and GitHub Pages](http://programminghistorian.org/lessons/building-static-sites-with-jekyll-github-pages) on *The Programming Historian* and [Jekyll's own documentation](http://jekyllrb.com/) to start getting a sense of how it works.

Once you have gone through these tutorials, you can get started using Ed by replacing the sample texts included in in the `_texts` folder in Ed with your own edited texts. Remember to always and only edit files in Ed using [a plain text editor](https://en.wikipedia.org/wiki/Text_editor), and *not* a word processor. I'm composing this file using a plain text editor called [Sublime Text](http://www.sublimetext.com/).  

An easy way to make new texts is to copy an existing text, replace the content and rename the file. Remember to always use the jekyll convention for naming files: `your-title.md`. You should also make sure that all your texts have the YAML front matter (the information at the top of the file). YAML stands for "YAML Ain't Markup Language"---no disrespect to XML---and it's the main way that Jekyll handles named data. Here's an example of YAML front matter:

~~~ yaml
---
layout: poem
title: "Cahier d'un retour au pays natal"
author: Aimé Césaire
---
~~~

Besides replacing content and creating new texts, you will probably  want to edit the `_config.yml` file to replace the boilerplate information we provided with your own personalized information in the relevant categories. Avoid replacing the information in categories that are not clear to you. Make sure to use proper YAML formatting when writing in the `_config.yml` file. Here's [a good reference source](http://docs.ansible.com/ansible/YAMLSyntax.html) in case you have doubts.

---

### Markdown and kramdown

Ed is designed for scholars and amateur editors who want to produce either a clean reading edition or a scholarly annotated edition of a text. The main language we use to write in the Jekyll environment is called Markdown. To learn more about the Markdown family, see Dennis Tenen and Grant Wythoff's "[Sustainable Authorship in Plain Text using Pandoc and Markdown](http://programminghistorian.org/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown)."

Our version of Jekyll uses a special Markdown processor called kramdown. The processor can be said to use it's own 'flavor' of Markdown, and sometimes the Markdown syntax will be different than other flavors of Markdown. Kramdown is convenient for scholars because of the way it handles footnotes. You can become familiar with the kramdown syntax in the [kramdown documentation](http://kramdown.gettalong.org/syntax.html). Another way to become familiar is to examine the sample text source files we provided.

---

## Components

### Genres

Ed offers three different layouts: poem, narrative and drama. The genre is indicated in the YAML front matter on your texts. The templates that govern how these genres are displayed can be found in the `_layouts` folder. Using these layouts will allow you to tweak the stylesheets according to your different needs. Out of the box, Ed contains some special instructions for poetry in its stylesheets that allow you to deal with some of the peculiarities of poetry layouts.

To indicate lines in poetry we use the line syntax from Markdown:

~~~ markdown
- Hold fast to dreams
- For if dreams die
- Life is a broken-winged bird
- That cannot fly.
- Hold fast to dreams
- For when dreams go
- Life is a barren field
- Frozen with snow.
~~~

To indent specific lines we take advantage of a feature in kramdown that allows us to indicate classes for a line. This approach still allows the line to be readable while editing.

~~~ markdown
- {:.indent-3} But O heart! heart! heart!
- {:.indent-4} O the bleeding drops of red,
- {:.indent-5} Where on the deck my Captain lies,
- {:.indent-6} Fallen cold and dead.
~~~

The `-` at the beginning of each line indicates that these are lines. The `{:.indent-3}` is what we need to in order to indicate the indent value for that line. Values can range from 1-10. You can expand the range or adjust the values in the Ed stylesheet (`_ed.scss`) in the `_sass` folder.

The example from Raisin in the Sun shows us that we don't need much special markup for theater as long as we use CAPITAL LETTERS for speakers. Italics for directions are easy enough. Just use `*` around the words you want to italicize.

*Narrative of the Life of Frederick Douglass* shows us an example of narrative that includes footnotes and quoted poetry. See the sections below for how to accomplish these different effects.

---

### Footnotes

Footnotes are the bread and butter of scholarship. Kramdown makes footnotes a fairly simple affair:


~~~
- O Captain! my Captain! rise up and hear the bells;
- Rise up—for you the flag is flung—for you the bugle[^fn2] trills,

...

[^fn2]: The bugle is a small trumpet implicated in the military industrial complex.
~~~

These footnotes can be placed anywhere, but they will always be generated at the bottom of the document. To have a multi-paragraph footnote you need to start the footnote text on the next line after the footnote anchor and indent it:

~~~
[^fn3]:
	Ugh pinterest fixie cronut pitchfork beard. Literally deep
	cold-pressed distillery pabst austin.

	Typewriter 90's roof party poutine, kickstarter raw
	denim pabst readymade biodiesel umami chicharrones XOXO.
~~~

The footnotes system provided by kramdown does have one limitation: It generates the numeration for you automatically, and it only allows you to have one set of footnotes for a text. In some cases we have to separate the author's footnotes from our own, in others we want to represent the author's own footnote style. In these cases we have to use HTML. Here's the example from *Narrative of the Life*:

~~~ html
... At this time, Anna,<sup><a href="#fn2" id="ref2">\*</a></sup> my intended wife, came on;

...

<sup id="fn2">*</sup> She was free. [&#x21a9;&#xfe0e;](#ref2)
~~~

Notice the double HTML Entity (hex), `&#x21a9;&#xfe0e;`, used at the end of the footnote to return us to the top. The first hex is the &#x21a9;&#xfe0e; symbol proper. The second assigns the proper variant glyph. This is a necessary hack while we wait for Apple devices to stop turning everything into unseemly emojis.

---

### Blockquotes

*Narrative of the Life* also includes several blockquotes. You can also find another example of blockquote use in the footnote of "O Captain! My Captain!" Simple blockquotes are simple enough in kramdown:

~~~
> This is to certify that I, the undersigned, have given the bearer, my servant, full liberty to go to Baltimore, and spend the Easter holidays.
>
> Written with mine own hand, &c., 1835.  
> WILLIAM HAMILTON,
~~~

To use a line break in block elements add two spaces after the end of the line where you want the break. You can't see them after `&c., 1835.` but they are there.

Things get a bit complicated when we want to use poetry inside the block or when the block is included in another block element, like a footnote. Here's the last two stanzas from "A Parody" in *Narrative of the Life*, which shows an example of a blockquote of poetry:

~~~
...
> - Two others oped their iron jaws,
> - And waved their children-stealing paws;
> - There sat their children in gewgaws;
> - By stinting negroes' backs and maws,
> - They kept up heavenly union.
> ^
> - All good from Jack another takes,
> - And entertains their flirts and rakes,
> - Who dress as sleek as glossy snakes,
> - And cram their mouths with sweetened cakes;
> - And this goes down for union.
{:.poetry}
~~~

The `{:.poetry}` tag at the end tells the processor to think of the lines above it as poetry. The `{:.poetry}` tag is an example of kramdown class assignments for block-elements. Because this segment of poetry exists in the 'narrative' layout, and because it is part of a blockquote, we need to signal to the processor to process poetry this way, so that the right class is invoked in the stylesheet. Notice also the `^` separating the stanzas. This bit of kramdown syntax helps us separate the stanzas while staying within the blockquote. The good news is this is the most complex kramdown syntax layout you will encounter in Ed.


### Pages

Your editions are treated as [collections](https://jekyllrb.com/docs/collections/) in Ed. Other web pages in your site exist outside the `_texts` folder. The homepage, for example, is constructed from the `index.html` file found on the root folder of your Ed project.

You will notice that the homepage in particular has a `.html` file ending instead of a `.md` ending. All template files in Jekyll are HTML, and the index behaves as a template file. Although these files are mostly written in HTML, notice that they still contain YAML front matter and liquid tags. To edit the homepage replace the content on the file shipped with Ed, making sure that your changes to `index.html` are written in valid HTML. The same goes for the template files in the `_layouts` folder.

Ed also comes with a search page, `search.html`. This page implements [elastic lunr](http://elasticlunr.com/), "a lightweight full-text search engine in Javascript for browser search and offline search." This simple search page can be useful if you have large collections of texts. If you don't, and don't feel the need, go ahead and delete it along with the `assets/js` folder.

Besides the homepage and the search page, Ed ships with an About page, `about.md` and a documentation page, `documentation.md`, i.e. this page. As you can see, these are regular `.md` files. You can replace the contents of each file using normal kramdown syntax. This also applies to any new page you create, which you should remember to save with an `.md` extension. When editing the `bibliography.md` file, be careful not to replace the liquid tag that generates your bibliography, unless you don't want to have a bibliography at all.

---

### Tables of Content

You will find three kinds of Tables of Content in Ed. The first example is in the list of Sample Texts in the Homepage. This list is generated using the [Liquid Templating language](http://liquidmarkup.org/). This is one of the major components of Jekyll, and I recommend you deepen your knowledge of it if you want to modify the logic that automates much of Ed. Here is the code that generates the Sample Texts list on the homepage:

~~~ html
<div class="toc">
  <h2>Sample texts</h2>
  <ul class="post">
  {% for item in site.texts %}  
    <li class="text-title">
      <a href="{{ site.baseurl }}{{ item.url }}">
        {{ item.title }}
      </a>
    </li>
  {% endfor %}
  </ul>
</div>
~~~

As you can see, the liquid tags `{%raw%}{% %}{%endraw%}` and `{%raw%}{{ }}{%endraw%}` are embedded into the HTML. Those with `{%raw%}{% %}{%endraw%}` often use programmatic logic, as is the case here. If you are not already familiar with programming languages, you may need to start elsewhere. I recommend learning Ruby, since this is the language used to build jekyll and jekyll-scholar in the first place (it's also the first programming language I used, so I'm biased). The `{%raw%}{{ }}{%endraw%}` simply pulls data from your project. In the example above it pulls the title from each 'post', i.e. each edited text. As you may have noticed already, we are basically adapting the blogging features of Jekyll to our own ends, what Cuban designer and theorist Ernesto Oroza would call "[technological dissobedience](http://www.ernestooroza.com/)."

The second kind of table of content is exemplified in this documentation. If you open the source file for the documentation, you will notice at the top this snippet:

~~~ markdown
## Contents
{:.no_toc}

* ToC
{:toc}
~~~

This is the kramdown way. The first tag, `{:.no_toc}` tells the processor not to add `## Contents` to the ToC. The second part creates an empty list and then tells the processor to replace it with a table of contents based on headers in the document. You can use this syntax in any page on the site that uses headers.

The third way is slightly more involved, but very useful for long texts. If we add the table of contents to the YAML front matter of a page, Ed will activate the optional table of content sidebar (`_includes/sidebar-toc.html`) and move the table of contents to a special sidebar for that page. *Narrative of the Life* uses this method for its table of content. If you would like to replicate this functionality in your own long texts, make sure to use the same syntax:

~~~ yaml
toc:
- Title Page
- Preface
- Letter From Wendell Phillips
- Chapter I
- Chapter II
~~~

The internal links pointing to the right sections in your document are generated from the title names automatically. In order for the links to work the names on section headings must contain the same words as the section headers. The punctuation and capitalization is irrelevant. If you can figure out how Ed accomplishes this trick, you have graduated from the Ed school of minimal editions.

---

### Bibliographies

If you want to include a small bibliography, and you feel it would be easier to write it out directly, Ed can help you render it with hanging indentation.  To achieve this effect make sure to use the `.bibliography` class in an ordered list. For example:

~~~ markdown
1. Douglass, Frederick et al. Narrative of the Life of Frederick Douglass: An American Slave. Charlottesville, Va.: University of Virginia Library, 1996. Open WorldCat. Web. 17 Apr. 2016.
2. Hansberry, Lorraine, and Robert Nemiroff. A Raisin in the Sun. Rep Rei edition. New York: Vintage, 2004. Print.
{.bibliography}
~~~

Which should display like this:

1. Douglass, Frederick et al. Narrative of the Life of Frederick Douglass: An American Slave. Charlottesville, Va.: University of Virginia Library, 1996. Open WorldCat. Web. 17 Apr. 2016.
2. Hansberry, Lorraine, and Robert Nemiroff. A Raisin in the Sun. Rep Rei edition. New York: Vintage, 2004. Print.
{:.bibliography}

---


To help us style and generate bibliographies and citations *automatically*, Ed can use the jekyll-scholar gem by [Sylvester Keil](https://github.com/inukshuk/). To learn more about the gem beyond the basic instructions below, make sure to read the documentation on the [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar) GitHub page. Keep in mind, though, that installing jekyll-scholar and working with it may be a bit difficult for beginners.


If you can get over the hurdles, jekyll-scholar can save you enormous amounts of time in the long term for your citation and bibliographic work. To begin, you must move the contents of the `jekyll-scholar starter kit` in your `optional` folder into the root folder. This will effectively replace the original `_config.yml` and `Gemfile` files, and add a `_bibliography` folder, and the `bibliography.md` and `Rakefile` files. To enable jekyll-scholar you must re-run `bundle install` again.

If everything goes smoothly, you should be able to start using jekyll-scholar at this point. The first thing you may want to do is provide Jekyll with your own bibliographic information in the form of a `.bib` file to replace the content of the `references.bib` file we've provided in the `_bibliography` folder.

To make it easy to create your own version of this file and to keep track of your bibliography for your project, in general I recommend you use [Zotero](http://zotero.org/). To export from Zotero in this format select the references you need from within your Zotero library, right click and select `export in...` and choose the BibLaTeX format. Rename your file to `references.bib` and move it into the `_bibliography` folder. You are, of course, free to create your `references.bib` file using any method you prefer as long as it is a BibTeX file.

Because as textual editors we are more likely than not to use citations in footnotes or pages that contain footnotes, and because footnotes will be necessarily generated at the bottom of the page, Ed also needs a separate page for your Bibliography or works cited. This is the role of the `bibliography.md` file. Feel free to edit the sample text, but make sure to leave the following line intact:

<pre>
&#123;% bibliography %&#125;
</pre>

To link your citations to the bibliography page, instead of writing them by hand, you can use the cite function in jekyll-scholar:

<pre>
&#123;% cite cesaire_discourse_2001 %&#125;
</pre>

Here's the breakdown:

* `cite` is the jekyllscholar command.
* `cesaire_discourse_2001` is the unique ID for Césaire's *Discourse on Colonialism* entry included in the reference.bib file.

Note that our jekyll-scholar starter kit comes ready for MLA style. To use Chicago style or more advanced citation features, refer to the documentation on jekyll-scholar to make the appropriate changes.

**Publishing your site on Github Pages with jekyll-scholar**

If you install jekyll-scholar, or most other plugins in Jekyll, you will need a workaround to publish your site on Github Pages, which only runs in 'safe mode.' I've provided a slightly modified version of a `Rakefile` originally created by [Robert Rawlins](https://blog.sorryapp.com/blogging-with-jekyll/2014/01/31/using-jekyll-plugins-on-github-pages.html) that will help you accomplish this task. Once you are ready to publish, switch to your `gh-pages` branch and run the following command:

~~~ bash
$ rake ed:publish
~~~

---

## Tips and Tricks

- The folding sidebar menu is generated from the `sidebar.html` file in the `_includes` folder. The top menu items are generated automatically from your pages. The bottom menu items are manually written in HTML. This structure can allow you to add external links. If you don't have that many pages, you may choose to do all the links by hand.
- For more hand-crafted layouts---such as [the title page in *The Narrative of the Life*](https://minicomp.github.io/ed/texts/narrative/index.html#title-page)---you may choose to work directly with HTML. One of the great advantages of working with the kramdown processor is that we have a lot of flexibility to mix HTML with the kramdown syntax. Note though, that even in the case of the title page, you can achieve these effects using kramdown syntax.
- Make sure to add horizontal rules, `---`, to separate sections in your texts. This creates a more pleasant layout.
- You can clean unnecessary folders and files from the original Ed package before publishing your site. This will help you reduce overhead. For example, you can erase this page, the sample texts and the `syntax.css` file (used for styling code).
- Consider providing tips for your readers on how to make their font bigger or smaller by taking advantage of <kbd>Command</kbd> + <kbd>+</kbd> and <kbd>Command</kbd> + <kbd>-</kbd>. Or returning to the top of the page using <kbd>Command</kbd> + <kbd>Up Arrow</kbd>. Part of the philosophy behind Ed is to avoid duplicating features that are already easily available in most web ecosystems.
- If you want to allow annotations on your site, consider providing a `via.hypothes.is` link. Our sample site can be annotated, for example, using the following link: `https://via.hypothes.is/http://minicomp.github.io/ed/`, which readers can access on the sidebar. Once you've indicated your own URL in the config file, the link will update automatically. Make sure to visit [hypothes.is](https://hypothes.is/) to learn more.
- Ed includes metadata in the headers that makes it easier for users of Zotero, and other systems to grab bibliographic information for the site and individual texts. Our metadata functionality may not be enough to generate a full proper citation. Consider providing visible citation information in your about page or homepage.
- Make sure to deepen your knowledge of the building blocks of Ed: Jekyll, YAML and Liquid. A great list of resources can be found in the blog "[Jekyll for Web Designers](http://jameswillweb.github.io/jekyll-for-designers/resources.html)".
- Our base themes Poole/Lanyon allow for easily customization of the interface. You can, for example, switch the position of the sidebar, change the theme colors and overlay options. To learn more check out the [Lanyon documentation](https://github.com/poole/lanyon#themes), and make sure to try the green, `.theme-base-0b`, it's really nice.
- You can change the look and feel of the site as a whole by changing the `color-scheme` in the `_config.yml` file. If you want to have more granularity, short of editing the `css`, you can change the variable values in the `assets/css/style.scss` file.
- In the `optional` folder you will find a sample `xslt` to help you get started converting TEI to Ed. You will also find css for adding pop-up "balloons" or tooltips to your texts.

---

## Publishing

### To a UNIX server

Publishing and Ed edition can be done in one of two ways. One way is to host it on a server you rent, own or have access to. Most mortals pay a hosting provider to host their sites. I recommend [Reclaim Hosting](https://reclaimhosting.com/), which is run by scholars for scholars. If you are affiliated with a university, chances are that your institution provides you with a UNIX account and a bit of server space. Since Jekyll generates a full static site for you, that means you can park it there too. To do so you need to build the site first. If you have been keeping your eye on your project by using `jekyll serve`, chances are you have a current built site in your project folder labelled `_site`.

If you don't already, you can build one easily by using the following Jekyll command:

~~~ bash
$ jekyll build
~~~

Or, again, if you have multiple environments:

~~~ bash
$ bundle exec jekyll serve
~~~

Using an FTP client like [Filezilla](https://filezilla-project.org/), or [SSH on your terminal](https://www.siteground.com/tutorials/ssh/), you need to push the contents of the `_site` folder to the folder on your server where you would like your project to exist. Depending on your host provider, you may be able to receive help from the sys admins with this step.

Please refer to the [note below on base urls](#a-note-on-your-base-url) to make sure your new links work on your new site.

### To GitHub pages

The second option is to publish your site for free on GitHub Pages.
Whether you decide to publish on GitHub pages or not, we recommend that you still use git and GitHub to version your edition and make the data available via another channel other than your webpage. This is one of the great advantages of using our system, increasing the chances of survival of your work and opening new audiences for it.

If you do decide to use the GitHub pages option, please make sure to read the [note below on base urls](#a-note-on-your-base-url).

To publish on GitHub pages, you must have a copy of the repository in GitHub. That means you also need an account there. Once you've created the repository that you will use, you must link your local repository to the one on GitHub. Notice that because you cloned the original source files from my repository, it will be linked to my repository (to which you don't have writing privileges) until you do this step. Instructions for changing the remote URL can be found [here](https://help.github.com/articles/changing-a-remote-s-url/).

The usual way of doing it is to create a different git branch called `gh-pages` within your local repository for your site. This is a branch is published by GitHub by default. GitHub also gives you the option to select [any branch you want to publish](https://github.com/blog/2228-simpler-github-pages-publishing), including the master branch.

In the following I use the gh-pages branch. To create and use that branch use the following command:

~~~ bash
$ git checkout -b gh-pages
~~~

Once you are using that branch, you are ready to publish your site. To do so use simply push the gh-pages branch to github:

~~~ bash
$ git push origin gh-pages
~~~

You can now access your site using an address that looks like `http://your-username.github.io/your-project-name`. The sample page for Ed, for example, is hosted at [minicomp.github.io/ed](http://minicomp.github.io/ed).

**<span id="a-note-on-your-base-url">A note on your base url</span>**

When you publish on a subfolder—automatic on GitHub pages—many of your links will break unless you indicate the name of your sub-folder in the `baseurl` value in your `_config.html` file. In addition, you need to make sure that your site-wide links (your links to your CSS files, for example) are preceded by the `{{ site.baseurl }}` tag. The base Ed install already uses this system, so you can simply replace the value `/ed` in your `baseurl` to `/your-project-slug`.

If on the other hand you are running your site on a root folder, simply erase `/ed`, but do make sure to leave the single quotes:

~~~ yaml
baseurl: ''
~~~

---

That should do it. If you have suggestions on how to improve Ed, make sure to leave us a line on [our issues page](https://github.com/minicomp/ed/issues), or send us a pull request.

Happy editing!

Alex Gil  
April 2016


*Copied from the original at* <br>[https://minicomp.github.io/ed/documentation/](https://minicomp.github.io/ed/documentation/)
