# WebDev Playground

So it all started on the 9th of September, 2018. Out of sheer frustration I
posted [a tweet](https://twitter.com/wingedrhino/status/1038856651711959042)
about how I'd rather be publicly shamed than not know enough HTML/CSS to
reproduce all elements needed for a site equivalent to my current (at the time
of writing this tweet) [WordPress site](https://wingedrhino.com).

This repository is to capture my learning process as I go about building this
site.

I'd be happy if I just have a bunch of static pages that look clean, consistent
and modern.

Eventually I intend to also figure out other stuff like a couple of frontend
frameworks (I'm eyeing [Vue.js](https://vuejs.org) most keenly) and maybe write
a simple CMS-like app in Go that would power a basic site.

## View It Online

Site at [webdev-play.aruba.myelin42.net](https://webdev-play.aruba.myelin42.net/)

It is just NGINX acting as a static file server and file browser, secured by
Let's Encrypt. The server is pointed to this repository's root and thus all you
can see at first load is a file browser. Click the sub-directories there that
correspond to sub-directories in this repository!

## Resources

This section documents whatever I'm using to learn web development.

### Microsoft Internet Explorer and old browser compatibility

This is a rant, not a resource. But I'm going to start here because you are very
likely to be mislead into believing you absolutely NEED to support obsolete
platforms.

If you are just starting out, please develop only for evergreen browsers: the
current versions of Mozilla Firefox, Google Chrome, Microsoft Edge and Apple
Safari. It is hard to support older browsers and many of the technologies used
to support them feel awful and clunky when compared to modern CSS techniques.
CSS3 is easy and reduces the number of lines you need to type. HTML5 improves
readability of your website's raw sourc code. JavaScript at ECMAScript 2017 and
above makes it easy to reason about code thanks to native module support and the
async/await syntax to avoid deeply nested functions as callbacks.

If you are Amazon or Google, you can afford to have a dedicated team to enable
support for old browsers because small percentage differences in accessibility
can make huge profits in terms of absolute dollar value for your company. But as
an indie developer, most of your paying or money-making customers would use
updated browsers anyway. Even the ones who are stuck with an old-ish Android
phone and the stock browser have the option to install Chrome or Firefox. If you
sell a product or service online, consider this. Is a person who doesn't bother
to update their device more likely to make a purchase on your platform and be a
recurring customer, or is a person with a modern device and/or browser more
likely to do the same? The later has already proven their intention to seek the
latest and greatest. Making these customers happy in the initial stages of your
product would lead to a better piece of mind. You can also iterate on features
much, much faster. When you have several million dollars of surplous net annual
revenue, you can saet thinking about optimizing your site for the older devices.

Many of the courses below discuss compatibility with older versions of browsers.
Make note of these, but ignore the workarounds as you go about building your
first website or prototype. I've observed that even maintaining compatibility
between current versions of Edge, Safari, Chrome and Firefox isn't an easy job.
Especially the laggard Safari, which is the ONLY browser engine allowed on an
iOS device. Until recently, it did not support the Service Worker standard.

### Node.js

Link: [Website](https://nodejs.org)

Install version 10.10 of Node.js (the latest and soon to be an LTS). IMO if a
package is incompatible with the current version of Node.js and the current
version has been out for a few months, the package may not be worth investing
in.

Your Linux Distro usually ships with an outdated version (unless it's called
ArchLinux) so install Node.js from this website!

### Yarn Package Manager

Link: [Website](https://yarnpkg.com/)

You should be using this for package management instead of NPM. Since I come
from a backend development background anway, I was pretty familiar with Yarn. It
does local caching of components so it is very easy to use while on a slow
network like when wrestling with code inside an Uber cab.

Anyway, install Yarn following instructions on this website after you have
installed Node.js!

### VSCode

Link: [Website](https://code.visualstudio.com/)

The best web IDE there is which is also cross-platform.

I suggest installing this alongside the following plugins:

1. Beautify (or alternatively, Prettier)
2. Better TOML
3. Color Picker
4. Debugger for Chrome
5. DotENV
6. ESLint
7. Live Sass Compiler
8. Live Server
9. Markdown Theme Kit
10. Markdown Lint
11. Prettier - Code formatter
12. Sass
13. TSLint
14. VS Live Share
15. XML Tools

That should be enough for a functional JavaScript, TypeScript, Web Dev and
Node.js development environment.

### Sass

Link: [Website](https://sass-lang.com/)

Sass is a CSS pre-processor. You'd learn how to use it in the web design for
beginners course linked to below.

Install it via `yarn global add sass`.

Oh and if you use the `Live Sass Compiler` and `Live Server` VSCode plugins, you
will have a much easier time dealing with Sass! Again, don't fuss about it until
you encounter it in a course below.

### Web Design For Beginners: Real World Coding in HTML and CSS

Link: [Udemy](https://www.udemy.com/web-design-for-beginners-real-world-coding-in-html-css/)

This course is a great jump-off point for someone who isn't exposed to the bare
basics of HTML and CSS, or someone looking to fill in their knowledge gaps which
can be rather crippling (this was my own primary use-case).

I started with this course, and although I had to watch everything at 2x speed,
it really opened my eyes.

My own approach to this course has been to zip through the HTML section in one
go, build the skeleton for a website with only HTML content and then repeat the
same process for the CSS section. I refer back to the course materials for links
with code snippets I can copy-paste. Nobody expects you to learn these by-heart
anyway.

### Learn Layout

Link: [Website](http://learnlayout.com/)

This is a free website to teach you everything about layouts on a website. It is
a great way to add to your knowledge after completing the web design for
beginners course. Some concepts may not make immediate sense but it is a great
reference site to come back to after a while!

### Bootstrap 4 From Scratch with 5 Projects

Link: [Udemy](https://www.udemy.com/bootstrap-4-from-scratch-with-5-projects/)

Bootstrap is a CSS toolkit of sorts. It comes with basic themes, utilities and a
whole lot of widgets that should be enough to make most basic websites. It is
super popular to build admin dashboards and the like.

A common gripe with Bootstrap is that if you use everything they provide, all
sites start to look the same. But at the same time, Bootstrap provides a lot of
things which you needn't do yourself like a grid system, various alignment and
responsive utilities and mixins. It also acts as reset of sorts so that pages
look consistent across browsers.

So the trick is to pay _extra attention_ to anything in Bootstrap that does not
seem like it locks you down to a specific look and feel and use this in those
projects where a unique look and feel is very important.

Back to the course, it starts off with a sandbox where every single element is
explained. Once you are done with the sandbox, I recommend re-watching it a few
times and then trying to design your own basic home page. You can check out the
sandbox source code - both the unstyled `bootstrap_sandbox_starter.zip` and the
styled `bootstrap_sandbox_final.zip` and quickly learn how to style individual
elements. This sandbox seems way better organized (to my eyes) than Bootstrap's
own documentation.

Then there's some realistic apps as projects you build one by one.

I'm still doing this course at the time of writing this and I'll remove this
disclaimer as soon as I'm done. Don't consider my views to be final till I
finish this course.
